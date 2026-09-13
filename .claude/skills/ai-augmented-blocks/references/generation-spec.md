---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# Especificação de geração — blocos de referência de conhecimento de IA

A única fonte da verdade sobre o que contém um bloco de referência de conhecimento de IA e como ele é
escrito. Siga exatamente para cada página. (Isso espelha o antigo
`.claude/commands/augmentedAIContent.md`; a habilidade é a versão canônica.)

## Regra dourada

Um bloco pode conter **somente o que é derivável do próprio corpo da página.** Não em outras páginas, não
conhecimento geral do produto, não conteúdo comentado/comentado no HTML. Se a página não informar
o bloco também não.

## Menu sanfonado + incluir sintaxe

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- `+++ AI Knowledge Reference` abre (um espaço após `+++`); `+++` sozinho fecha.
- Linha em branco antes da abertura de `+++` e após o fechamento de `+++`.
- O título é sempre exatamente `AI Knowledge Reference`.
- O acordeão inteiro vive em uma inclusão não localizada e a página o extrai com
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. Conteúdo em
  `help/_includes/do-not-localize/` está excluído da localização — é assim que o bloco permanece
  não traduzido.

## Incluir estrutura de arquivo

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **Nome do arquivo:** deriva do caminho da página relativo ao seu nível superior `help/using/<folder>/`
seção: remover `.md`, substituir qualquer `/` restante por `-`, prefixar por `ai-augmented-`.
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md` →
    `ai-augmented-expression-journey-properties.md`
- Uma subpasta por seção de nível superior (`building-journeys/`, `email/`, `data/`, ...).

## Abertura fixa — textualmente, nunca modificar

Cada bloco começa exatamente com esses dois parágrafos. Copiar byte por byte; não parafraseie,
condensar ou reordenar:

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## As seis seções, em ordem

Ignore uma seção somente se a página não produzir conteúdo significativo para ela.

### 1. TL;DR
Uma frase: o que a página ensina ou ativa. `* **TL;DR:** [one sentence]`

### &#x200B;2. Intenções
3 a 6 coisas que um usuário pode realizar após ler a página.

### &#x200B;3. Glossário
Principais termos específicos da página com definições curtas; sinalizar termos específicos do produto com
`*(product-specific)*`. Nenhum preenchimento de marketing genérico.

**Precisão do modo de validação (obrigatória):** se a página abranger teste/visualização/simulado
execução, distinguir cada modo que a página realmente nomeia — não recolha. Use os
termo exato da página (por exemplo `Simulate content`, `Simulate content (AEP profiles)`,
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). Nunca
substituir &quot;perfis sintéticos&quot;, &quot;dados falsos&quot; ou &quot;sem dados reais&quot; por qualquer um deles.

### &#x200B;4. Medidas de proteção
Limites, pré-requisitos, permissões e restrições declarados na página.

- **Qualificar cada limite numérico** como `(hard limit)` ou `(recommended)` — mas **somente** quando a variável
A página usa a redação de imposição (erro / rejeitado / máximo / não pode exceder / somente ... suportado)
ou texto de recomendação (para melhor desempenho / é recomendado). Se a página não fornecer
qualificador, não dê nenhum. **Nunca rotule um valor classificável, padrão ou configurável como rígido.**
Os valores que podem ser gerados &quot;entrando em contato com o representante da Adobe&quot; ou por meio de uma API são
  `(default)`, não é difícil.
- **Qualifique cada taxa/taxa de transferência com seu escopo** (por sandbox/por organização/por instância).
- **Faça a verificação cruzada de todos os números em relação ao corpo da página.** O corpo da página é autoritativo.
- **Não inferir** as medidas de proteção que a página não declara. Nenhum comentário meta (&quot;a página não
especificar ...&quot;).

### &#x200B;5. Terminologia
Nomes canônicos, siglas, variantes, sinônimos, desambiguação.

- **Sinônimos** (`"A" = "B"`) somente para **equivalentes verdadeiros** — ambos os formulários devem aparecer na página
significa a mesma coisa. Tudo que é um *contraste* fica em **Não confunda**
(`"X" ≠ "Y"`), não Sinônimos.
- **Precisão de status/ciclo de vida:** copie rótulos de status exatos do corpo da página; não
parafraseando. Use &quot;Não confundir&quot; para separar status que compartilham uma palavra-raiz.

### &#x200B;6. Perguntas frequentes
3 a 6 perguntas prováveis com respostas curtas. As respostas usam os **mesmos verbos e substantivos da página
corpo**. Não introduza &quot;reverter&quot;, &quot;redefinir&quot; ou &quot;reverter&quot;, a menos que a página os utilize.

## O que NÃO incluir

- Não reescreva nem resuma o conteúdo do corpo nem forneça instruções passo a passo.
- Não invente conteúdo não suportado pela página.
- Não use estes termos imprecisos a menos que eles apareçam **textualmente** na página:
&quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;, &quot;reverter&quot;, &quot;reverter&quot;.
- **Nenhuma contração** em qualquer lugar na prosa do bloco — soletre &quot;não é&quot;, &quot;não é&quot;, &quot;não pode&quot;,
&quot;é&quot;, etc. (A única exceção é uma cadeia de caracteres da interface do usuário do produto textual, como
  `[!UICONTROL configuration doesn't exist]`, que é preservado exatamente.)

## Etapa 3 — verificar todas as reclamações (autoverificação, porta 1)

Antes de gravar a inclusão, leia novamente a declaração de conteúdo gerado por declaração. Obrigatório, mesmo para
páginas curtas. Corrija qualquer falha antes de gravar e registre a correção no relatório.

- Cada termo/rótulo/nome de interface do usuário no bloco aparece no corpo da página.
- Nenhum sinônimo, a menos que ambos os formulários apareçam na página. Todas as referências a &quot;Não confundir&quot; são somente
nesta página.
- Cada valor numérico corresponde exatamente ao corpo da página; cada qualificador de limite é justificado pelo
texto da página; nenhum qualificador inventado.
- Nenhum detalhe de glossário/perguntas frequentes importado de outras páginas ou do conhecimento geral.
- Nenhum termo impreciso proibido, a menos que textualmente na página; sem contrações.

## Lista de verificação de pós-geração (porta 1, continuação)

- [ ] Todo valor numérico existe textualmente/é derivado do corpo da página.
- [ ] Todos os limites se qualificaram corretamente (rígido vs. recomendado vs. nenhum); sem valor padrão/passível de aumento
 rotulado incorretamente como rígido.
- [ ] Toda taxa de transferência tem seu escopo.
- [ ] Todos os modos de validação presentes na página são nomeados com termos precisos de página.
- [ ] Todos os status do ciclo de vida usam rótulos de página exatos.
- [ ] Sinônimos são verdadeiros equivalentes; os contrastes estão em &quot;Não confundir&quot;.
- [ ] Sem palavras proibidas/sem contrações (fora das cadeias de caracteres textuais).
- [ O Glossário do ] não tem termos genéricos; as Perguntas frequentes não apresentam nada ausente na página.

O portão 1 é o autor do bloco checando seu próprio trabalho. Ele **não** substitui o
rodada de verificação independente (porta 2) em `verification-round.md`.
