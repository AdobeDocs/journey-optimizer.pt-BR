---
name: ai-augmented-blocks
description: Gerar e manter blocos de Referência de conhecimento de IA para documentos do Adobe Journey Optimizer (jornada-otimizer.en). Use quando uma nova página em Ajuda/uso/precisa de um bloco de IA, quando uma página existente foi alterada e seu bloco pode ter se movido ou quando for solicitado a adicionar/atualizar/verificar o conteúdo de Referência de conhecimento de IA (IA aumentada). Produz uma inclusão de não localização em help/_includes/do-not-localize/<folder>/ai-aumented-<page>.md, conecta a inclusão na página com {{$include}}, executa uma rodada de verificação independente obrigatória para que o bloco seja verdadeiro e inequívoco, rastreia o trabalho em uma tarefa DOCAC JIRA e (somente após perguntar ao autor) abre uma PR. NUNCA mescla.
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---


# Blocos de referência de conhecimento de IA

Esta habilidade gera e mantém os blocos de acordeão **Referência de conhecimento de IA** para a
Documentação do Adobe Journey Optimizer (`journey-optimizer.en`). Os blocos estão estruturados,
contexto não localizado anexado às páginas de documento para que o Assistente de IA responda a perguntas sobre
Journey Optimizer com mais precisão.

Cada bloco é armazenado como uma **inclusão de não localização** (para que nunca seja traduzido) e extraído
em sua página com `{{$include}}`. Um bloco contém **somente fatos derivados de sua própria página
corpo** — nada importado de outras páginas, conhecimento geral do produto ou comentários do HTML.

> **Leia os arquivos de referência antes de gerar qualquer coisa.** Eles contêm as regras reais, não
> Um resumo:
> - `references/generation-spec.md` — estrutura de bloco, a abertura fixa, seção por seção
>   regras de conteúdo e todas as regras de precisão (limites rígidos versus recomendados, modos de validação,
>   rótulos de status, sem contrações, a lista de palavras proibidas).
> - `references/verification-round.md` — a verificação de fatos **obrigatória** contraditória independente
>   essa é a porta de qualidade final. Isso não é opcional e não pode ser ignorado.
> - `references/git-jira-tracking.md` — fluxo de ramificação/confirmação/PR (pergunte ao autor antes de abrir uma
>   PR; **nunca mesclar**) e rastreamento JIRA DOCAC.

## Quando esta habilidade se aplica

- **Nova página** criada em `help/using/<folder>/` → gere um bloco para ela.
- **Página existente alterada** → verifique se seu bloco foi deslocado do corpo da página e atualize-o.
- Solicitado a **adicionar, atualizar, verificar ou auditar** referência de conhecimento de IA/blocos com IA aumentada.

## Escopo e exclusões

- **No escopo:** páginas em `help/using/<folder>/`.
- **Fora de escopo — nunca adicione blocos aqui:**
  - `help/rp_landing_pages/` (introdução/páginas de aterrissagem) — excluído pela regra de autor.
  - Navegação fina/hubs de link, páginas somente índice e páginas quase vazias. Quando uma página está nua
    lista de links sem conceitos substantivos, **ignore-a e diga o motivo** — não force um bloqueio.
  - Notas de versão (`help/using/rn/`, páginas de notas de versão).
- Na dúvida sobre se uma página é suficientemente substantiva, avalie por conteúdo: se ela ensina real
conceitos, restrições ou terminologia a abrangem; se ela só apontar para outro lugar, ignore-a.

## Fluxo de trabalho

Trabalhe **uma pasta (ou uma página) de cada vez**. Não coloque pastas não relacionadas em lote em uma ramificação.

### 1 - Determinar alvos e modo

Pergunte ao autor (ou deduza a partir da solicitação/abra arquivos) quais páginas processar e detecte o
por página:

- **CREATE** — a página não tem linha `{{$include .../ai-augmented-<page>.md}}` nem existe
bloco `+++ AI Knowledge Reference` embutido → gerar um novo bloco.
- **ATUALIZAÇÃO** — a página já tem um bloco. Calcule o hash do corpo da página e compare-o com o
  `source-hash` no comentário de sincronização da inclusão (veja abaixo). Se eles diferem, a página se deslocou →
  regenerar/atualizar o bloco. Se eles corresponderem, o bloco é atual → ignorar (relatório &quot;atualizado&quot;).
- **MIGRAR** — a página tem um bloco *embutido* `+++ AI Knowledge Reference` (ainda não
externalizado) → mova-o para um include não-localizado e substitua-o pelo `{{$include}}`
linha, preservando a fidelidade do conteúdo.

Calcular o hash do corpo da página da mesma maneira em todos os lugares (usado para o comentário de sincronização e verificação de descompasso):

```bash
md5 -q help/using/<folder>/<page>.md | cut -c1-8
```

Calcular **antes** de editar a página (o hash cobre o corpo como está quando o bloco é
gerada). No Linux, use `md5sum help/using/<folder>/<page>.md | cut -c1-8`.

### 2 — Gerar (ou atualizar) o bloco

Siga `references/generation-spec.md` exatamente para cada página. Invariantes de chave:

- Dois **parágrafos de abertura fixos**, textualmente, byte por byte (nunca parafraseados).
- Seções em ordem: **TL;DR, Intenções, Glossário, Medidas de Proteção, Terminologia, Perguntas frequentes**.
- Todas as solicitações são baseadas somente no corpo da página. Sem contrações. Qualificar números como
  `(hard limit)` / `(recommended)` **somente** quando a página usa imposição/recomendação
  texto; caso contrário, nenhum qualificador. Use o modo de validação exato da página e os rótulos de status.
  Preservar textualmente as sequências de caracteres `[!UICONTROL ...]` / `[!DNL ...]`. Nunca usar o impreciso banido
  termos, a menos que apareçam textualmente na página.

**Incluir arquivo** — `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`
(crie o subdiretório `<folder>`, se necessário; nivele qualquer caminho de página aninhado com `-`):

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening paragraphs + the six sections]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of the page body> -->
```

**Edição de página** — adicione exatamente uma linha, como a última linha de conteúdo, precedida por uma linha em branco
(não toque em mais nada na página):

```
{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}
```

Em ATUALIZAR, edite somente o arquivo de inclusão (e salte `ai-section-version` se desejar rastrear
revisões); a linha `{{$include}}` da página geralmente permanece a mesma. Atualizar o `source-hash` para
o hash do corpo da página atual assim que o bloco corresponder à página novamente.

Executar a **autoverificação** em `references/generation-spec.md` (Etapa 3 verify-every-claim + a
lista de verificação de pós-geração) antes de prosseguir. Esta é a porta 1 de 2.

### 3 — Ronda de verificação independente (porta final obrigatória)

Esta é a etapa que o autor exige especificamente: **confirme se cada bloco é válido, verdadeiro e
sem ambiguidade.** Executá-lo como uma *passagem recente, independente* — idealmente um subagente separado que
O vê apenas o corpo da página e o bloco, sem memória de como o bloco foi gravado — seguindo
`references/verification-round.md`. Verifica novamente cada reivindicação, reduz qualquer limite rotulado incorretamente,
Corrige erros de Sinônimos versus Não confundir e remove tudo o que não está aterrado na página. Aplicar
cada correção feita no arquivo include antes de continuar. Esta é a porta 2 de 2 e não pode ser ignorada.

### 4 — Varredura estrutural

Antes de confirmar, limpe cada bloco em busca de estrutura e higiene (consulte o trecho de limpeza em
`references/git-jira-tracking.md`): frente + `# AI Knowledge Reference` cabeçalho, o
`+++ … +++` cercas, o parágrafo de abertura fixo, o comentário de sincronização, sem contrações (excluindo
`[!UICONTROL ...]`) e uma linha `{{$include}}` correspondente na página.

### 5 — Rastrear no JIRA, depois perguntar sobre uma PR (nunca mesclar)

Seguir `references/git-jira-tracking.md`:

1. Confirmar em uma ramificação chamada para a tarefa JIRA (`DOCAC-<key>`), nunca em `main`. Verifique se
a confirmação chegou à ramificação (1 confirmação antes de `origin/main`), não em `main`.
2. Update the DOCAC task: comment with what changed + the verification result, set the fix (Atualizar a tarefa DOCAC: comente com o que mudou + o resultado da verificação, defina a correção)
e faça a transição conforme o processo da sua equipe exigir.
3. **Pergunte ao autor se ele deseja um pull request.** Só abra um se eles disserem sim.
4. **Nunca mesclar.** Essas PRs são para análise humana; a mesclagem é sempre a chamada do autor.

### 6 — Relatório

Relatório por página: criado / atualizado / migrado / ignorado (motivo +), o resultado da verificação
(limpo ou corrigido, com as correções), a tarefa JIRA e o link PR, se houver.

## Notas para escritores que executam esta habilidade

- O bloco é um **derivado do corpo da página em um ponto no tempo** — trate-o como parte do
página. Ao alterar uma página de uma forma que toque em uma grade de proteção, limite, rótulo de status ou
modo de validação, atualize o bloco na mesma alteração.
- As etapas de JIRA e PR precisam acessar a JIRA e o GitHub corporativos. Se você não tiver essa
acessar, ainda gerar + verificar o bloco e abrir a alteração localmente; executar as etapas JIRA/PR
a alguém que o faça.
- Essa habilidade vive no repositório então toda a equipe de redação compartilha um processo. Melhorar a
referencie arquivos aqui em vez de manter cópias privadas.
