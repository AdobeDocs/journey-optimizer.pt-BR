---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Rastreamento de Git, PR e JIRA

Como efetuar a alteração com segurança e rastreá-la. Duas regras bem definidas do autor:

1. **Pergunte antes de abrir uma PR.** Gerar e verificar o bloco independentemente, mas apenas abrir um pull
solicite se o autor disser que sim.
2. **Nunca mesclar.** Essas relações públicas existem para análise humana. A mesclagem é sempre uma decisão do autor.

## Varredura estrutural (executar antes de confirmar)

Para cada página processada na pasta:

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

Qualquer linha impressa (diferente da &quot;varredura concluída&quot; e da lista `git status`) é um defeito a ser corrigido antes de
confirmando.

## Ramificar e confirmar (nunca confirmar no principal)

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**Verifique se a confirmação foi parar na ramificação, não em`main`** (uma arma conhecida — se você alternou para
`main` para inspecionar as páginas, uma confirmação posterior pode chegar lá):

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

Se uma confirmação aterrissou acidentalmente em `main`: `git branch -f DOCAC-<key> <sha>` para apontar para a ramificação
nele, `git checkout DOCAC-<key>`, depois `git branch -f main origin/main` para redefinir o principal local.
`origin/main` nunca é afetado por um erro local.

Push: `git push -u origin DOCAC-<key>` (use `--force-with-lease` se a ramificação já existir
remotamente em uma confirmação mais antiga).

## Pergunte sobre a PR

Pergunte ao autor claramente, por exemplo: *&quot;Blocos gerados e verificados para `<folder>`. Deseja
abrir uma PR para revisão?&quot;* Apenas em caso afirmativo:

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

O corpo da PR termina com a linha de atribuição necessária
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **Não mesclar** — deixe o
PR aberta para revisão.

## Rastreamento JIRA

Rastrear todas as alterações em uma tarefa DOCAC (imagem de implantação: `DOCAC-15582`). Localizar ou criar o da pasta
tarefa e, em seguida:

1. **Comente** com o que foi alterado e o resultado da verificação (páginas cobertas/ignoradas, verificador
limpo/corrigido, quaisquer chamadas hard-vs-default notáveis). Inclua o link da PR, se houver um aberto.
2. **Definir a versão de correção** (este programa usou `AJO26.9`).
3. **Transição** Novo → Em andamento → Resolvido (resolução &quot;Fixa&quot;), de acordo com seu fluxo de trabalho. Neste
projeto as ids de transição eram `4` (Progresso de Início) então `5` (Resolver, com resolução
   `{"name":"Fixed"}`); uma tarefa ainda em &quot;New&quot; deve ser iniciada antes de ser resolvida.

Usar as ferramentas corporativas do MCP JIRA (`add_jira_comment`, `update_jira_issue` para `fixVersions`,
`bulk_transition_jira_issues`) ou a interface JIRA. Se você não tiver acesso ao JIRA, passe esta etapa para
alguém que a tenha e anote no seu relatório.

## Uma pasta = uma ramificação = uma tarefa

Não misture pastas não relacionadas em uma única ramificação ou PR. Uma nova página adicionada posteriormente tem seu próprio pequeno
(modo CRIAR) e podem compartilhar a tarefa da pasta ou obter a sua própria tarefa, como a sua equipe preferir.
