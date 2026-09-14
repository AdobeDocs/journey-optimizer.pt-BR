---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# Rodada de verificação — a porta de qualidade final obrigatória

Esta é a porta 2 de 2 e a etapa que garante que cada bloco seja **válido, verdadeiro e livre de
ambiguidade&#x200B;**. &#x200B;** não é opcional e não pode ser ignorado**, inclusive para atualizações de página única.

## Por que está separado

O autor do bloco (porta 1) está muito próximo do bloco para capturar seus próprios erros de aterramento. Portão 2
é uma **reverificação adversária independente**: um revisor novo que presume que o bloqueio pode estar errado
e tenta provar, usando **somente** o corpo da página como verdade. Executá-lo como um **subagente separado**
isso não viu como o bloco foi escrito — essa independência é o que torna efetivo. Para
um lote de páginas, um subagente verificador, pode abranger toda a pasta.

## O que o verificador faz, por página

1. Leia a **página de origem completa** `help/using/<folder>/<page>.md`. HTML-comment /
o conteúdo comentado é **não** uma fonte válida.
2. Leia o **bloco** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`.
3. Classificar declaração de **a cada** como COM BASE/IMPRECISA/SEM FUNDO em relação ao corpo da página.
4. **Corrija todos os problemas editando somente o arquivo de bloco** — preserve as duas aberturas fixas
parágrafos, as `+++ … +++` fronteiras e o comentário de sincronização. Nunca modifique a página de origem.
5. Relatório por página: `clean` ou `N issues` + as correções exatas aplicadas.

## Lista de verificação contraditória (elementos de risco mais elevado primeiro)

- **Números e limites.** Cada valor exato. Um limite é `(hard limit)` somente se a página usar
imposição/texto máximo; `(default)` se passível de ação/padrão/configurável (incluindo &quot;solicitação
mais pelo representante da Adobe&quot; ou &quot;passível de extração pela API&quot;); `(recommended)` para consultoria; não
qualificador se a página não fornecer nenhum. **Rebaixe qualquer limite que o gerador tenha rotulado como rígido.**
Cada valor de taxa de transferência carrega seu escopo.
- **Datas, IDs, nomes de produto/campo, identificadores SQL, enumerações de status, cadeias de caracteres de erro** — textualmente
na página. Tolerância zero em prazos legais/de conformidade: nunca invente um SLA, retenção,
ou data de aplicação; mantenha qualquer data exatamente como a página declara e rotulada como a página
enquadra-o.
- **Sinônimos vs. Não confundir.** Um Sinônimo (`"A" = "B"`) requer ambos os formulários na página
significa a mesma coisa. Qualquer contraste (`"X" ≠ "Y"`) pertence a &quot;Não confundir&quot;. Mover
rótulos errados.
- **Modos de validação/teste** nomeados com os termos exatos da página, não combinados entre
experiências clássicas vs reprojetadas ou entre canais.
- **Aterramento.** Nada importado de outra página, do conhecimento geral do produto ou de uma HTML
comentário. Remova tudo o que o corpo da página não suporta.
- **Estilo.** Nenhuma contração (fora da cadeia de caracteres `[!UICONTROL ...]` / `[!DNL ...]`). None
das palavras proibidas (&quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;, &quot;reverter&quot;, &quot;reverter&quot;)
a menos que na página. As cadeias de caracteres da interface do usuário foram preservadas exatamente.
- **Estrutura.** Dois parágrafos de abertura fixos intactos e textualmente; seis seções presentes e em
ordenar onde a página os suporta; sincronizar comentário presente.

## Prompt do subagente de verificador reutilizável

Preencha a lista de pastas e páginas. Inicie-o como um subagente independente de uso geral.

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## Critérios de saída

A pasta passa pela porta 2 somente quando o verificador relata cada página como `clean` (ela pode ser encontrada)
nada ou aplicou correções e o bloco agora está limpo). Se ele tiver aplicado correções, elas já estarão
nos arquivos de bloco — inclua-os no relatório final e prossiga para a varredura e confirmação.
