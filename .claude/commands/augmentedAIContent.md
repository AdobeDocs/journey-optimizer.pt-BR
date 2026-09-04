---
source-git-commit: 341538e14ef7de012cce89561727bdecb44d8183
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 0%

---
# aumentedAIContent

Gera uma opção **Referência de conhecimento de IA** criada automaticamente para uma ou mais páginas de Markdown no repositório de documentação do Journey Optimizer e a armazena como uma **inclusão não localizada** para que não seja traduzida.

## Repositório de destino

`help/using/` (relativo à raiz do repositório)

## Sintaxe do acordeão (Experience League)

```
+++ AI Knowledge Reference

Content here — any standard markdown is valid.

+++
```

**Regras:**

- `+++ AI Knowledge Reference` abre o acordeão (um espaço após `+++`); `+++` sozinho em uma linha o fecha
- Linha em branco antes da abertura de `+++` e após o fechamento de `+++`
- O título é sempre exatamente `AI Knowledge Reference`

## Incluir sintaxe (Experience League)

```
{{$include /help/_includes/do-not-localize/<folder>/<include-file>.md}}
```

O conteúdo extraído via `{{$include}}` de `help/_includes/do-not-localize/` está **excluído da localização**. É assim que o bloco permanece não traduzido.

---

## Fluxo de trabalho

### Etapa 1 — Solicitar o(s) target(s)

Pergunte ao usuário:
> Que arquivo ou pasta você deseja enriquecer?
> - Arquivo único: caminho relativo à raiz do repositório (ex.: `help/using/email/get-started-email.md`)
> - Pasta: todos os `.md` arquivos recursivamente (ex.: `help/using/email`)
> - Lista de arquivos/pastas

Se uma pasta for fornecida, liste os `.md` arquivos encontrados e confirme antes do processamento.

### Etapa 2 — Para cada arquivo: leia e gere

1. **Leia o arquivo** por completo.
2. **Entenda o tópico da página** — que recurso, conceito ou tarefa ele aborda?
3. **Gerar o conteúdo do bloco** usando as regras de geração de conteúdo abaixo.
4. **Executar a lista de verificação de validação de pós-geração** (veja abaixo) — não ignorar.
5. **Verifique** se um bloco de Referência de Conhecimento de IA já existe — embutido (`+++ AI Knowledge Reference` próximo ao final) ou já externalizado (uma linha `{{$include /help/_includes/do-not-localize/.../ai-augmented-...}}`). Em caso afirmativo, perguntar ao usuário: substituir ou ignorar? Ao substituir, substitua o arquivo de inclusão (e se o bloco ainda estiver em linha, remova o bloco em linha e adicione a linha de inclusão no lugar).

### Etapa 3 — verificar todas as reclamações em relação ao corpo da página

Antes de gravar o bloco, leia novamente a declaração de conteúdo gerado por declaração. Esta etapa é **obrigatória e não pode ser ignorada**, mesmo para arquivos curtos. Corrija qualquer falha antes de prosseguir para a Etapa 4.

**Terminologia e rótulos**

- [ ] Cada termo, rótulo e nome de interface no bloco aparece no corpo da página — não é importado de outra página ou inferido a partir do conhecimento geral do produto
- [ ] Nenhum sinônimo é listado, a menos que ambos os formulários apareçam na página
- [ ] Cada entrada &quot;Não confunda&quot; faz referência apenas aos conceitos mencionados nesta página

**Medidas de proteção e limites**

- [ ] Cada valor numérico corresponde exatamente ao corpo da página
- [ ] Um limite é chamado de **hard** somente se o corpo da página usar essa palavra ou implicar claramente que o sistema a impõe (por exemplo, &quot;não pode exceder&quot;, &quot;máximo ... permitido&quot;, &quot;apenas ... com suporte&quot;)
- [ ] Um limite é chamado de **recomendado** somente se o corpo da página usar essa palavra ou uma equivalente (&quot;para melhor desempenho&quot;, &quot;é recomendado&quot;)
- [ ] Se o corpo da página não fornecer nenhum qualificador, o bloco não fornecerá nenhum — não invente um
- [ ] Nenhum meta-comentário sobre o que a página de origem diz ou não diz (por exemplo, &quot;nenhum número específico é declarado nesta página&quot;)

**Definições de glossário**

- [ ] Nenhuma definição contém detalhes técnicos ausentes no corpo da página
- [ ] Nenhuma entrada elabora usando informações de outras páginas no conjunto de documentação

**Perguntas frequentes**

- [ ] Cada detalhe específico (recursos da interface, nomes de botão, nomes de campo, sequências de etapas) é declarado no corpo da página, não inferido ou importado de outras páginas
- [ ] Nenhuma resposta introduz informações que o corpo da página não endereça

**Regra de correção:** se houver falha na verificação, corrija o conteúdo **antes** de gravar o bloco. Registre cada correção no relatório de Etapa 5.

---

### Etapa 4 — Gravar o bloco em um include não localizado e, em seguida, incluí-lo

O bloco gerado deve **não estar localizado**, portanto, não está inserido na página. Em vez disso, ele fica em um arquivo de inclusão separado em `help/_includes/do-not-localize/`, que é excluído da tradução, e a página o puxa com `{{$include}}`. (Esta é a convenção DOCAC-15581.)

**a. Derive o nome de arquivo de inclusão** do caminho da página relativo à sua pasta de seção de nível superior em `help/using/`: remova a extensão `.md`, substitua qualquer `/` restante por `-` e adicione o prefixo `ai-augmented-`. Esse nivelamento mantém o diretório de inclusão plana livre de colisões.

Exemplos (seção `building-journeys`):

| Página | Incluir arquivo |
|---|---|
| `help/using/building-journeys/end-journey.md` | `ai-augmented-end-journey.md` |
| `help/using/building-journeys/expression/journey-properties.md` | `ai-augmented-expression-journey-properties.md` |

**b. Grave o arquivo de inclusão** em `help/_includes/do-not-localize/<section-folder>/<include-file>` (crie o subdiretório `<section-folder>` se ele não existir — uma subpasta por seção AJO de nível superior, por exemplo, `building-journeys/`, `email/`). Use exatamente esta estrutura — `title` primeiro plano, um cabeçalho `# AI Knowledge Reference`, a opção completa do **Modelo completo** abaixo e, em seguida, o comentário de sincronização:

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

[complete "+++ AI Knowledge Reference" accordion from the Full template below]

<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of the including page's body, excluding the {{$include}} line] -->
```

**c Adicione a chamada de inclusão** como a última linha da página, precedida por uma linha em branco. Não modifique qualquer outro conteúdo da página:

```
{{$include /help/_includes/do-not-localize/<section-folder>/<include-file>}}
```

O comentário de sincronização ainda permite a detecção de desvio: o hash de origem é calculado sobre o corpo da página incluída, para que ferramentas e escritores futuros possam saber quando a página foi desviada do bloco. Dois arquivos foram alterados por página: o **arquivo de inclusão** (criado) e a **página** (uma linha `{{$include}}` adicionada).

### Etapa 5 — Relatório

- Arquivos modificados ✓ (incluir arquivo criado + linha `{{$include}}` da página)
- Arquivos ignorados + motivo (já tem página de bloco/vazia/índice)
- Quaisquer avisos de validação gerados durante a Etapa 2

---

## Regras de geração de conteúdo

Analise a página e produza as seções abaixo **em ordem** dentro do acordeão. Ignore completamente uma seção se nenhum conteúdo significativo puder ser extraído para ela.

### Abertura fixa — textualmente, não modificar

Cada opção de Referência de conhecimento de IA deve começar com esse bloco exato. Copie como está; não parafraseie, condense ou reordene:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

As seções específicas da página abaixo seguem imediatamente após esses dois parágrafos, ainda dentro do mesmo acordeão. (A opção inteira é gravada no arquivo de inclusão não localizado, por Etapa 4 — não incorporado na página.)

### 1. TL;DR

Uma frase: o que essa página ensina ou permite?

```
* **TL;DR:** [one sentence]
```

### &#x200B;2. Intenções

3 a 6 coisas que um usuário pode realizar após ler esta página.

```
**Intents:**

* [action]
* [action]
```

### &#x200B;3. Glossário

Termos principais específicos desta página/recurso com definições curtas. Sinalizar termos específicos do produto.

```
**Glossary:**

* **[Term]**: [definition] *(product-specific)*
```

Inclua somente termos relevantes a esta página. Não compartilhe com termos de marketing genéricos.

**Regra de precisão de modo de validação — obrigatória:**
Se a página abranger qualquer forma de teste, pré-visualização ou execução simulada, você DEVERÁ distinguir entre todos os modos que a página realmente descreve. Não recolha modos distintos em uma única entrada abreviada:
- **Simulação** — renderiza o conteúdo da mensagem sem enviar; usa perfis reais
- **Modo de teste** — envia somente para perfis de teste designados; usa perfis de teste persistentes do AEP (não perfis sintéticos ou falsos)
- **Dry run** — executa a lógica de jornada completa sem ativar ações; usa dados de público-alvo reais

Inclua apenas os modos presentes na página. Copie o termo preciso do produto no corpo da página — não substitua &quot;perfis sintéticos&quot;, &quot;dados falsos&quot; ou &quot;sem dados reais&quot; por nenhum desses.

### &#x200B;4. Medidas de proteção

Limitações, pré-requisitos, permissões ou restrições mencionadas na página.

```
**Guardrails:**

* [guardrail]
```

**Regras de precisão da grade de proteção — obrigatório:**

- **Qualifique todos os limites numéricos** como recomendados ou rígidos. Exemplo: &quot;Máximo de 10 pesquisas de conjunto de dados por mensagem (limite rígido)&quot; e não &quot;Máximo de 10 pesquisas de conjunto de dados&quot;.
- **Qualifique cada taxa de transferência ou figura** com seu escopo. Exemplo: &quot;Limite de TPS de 150.000 mensagens/hora (por sandbox)&quot; e não &quot;Limite de 150.000 mensagens/hora&quot;.
- **Verifique todas as medidas de proteção em relação ao corpo da página** antes de incluí-la. Se a página exibir 10 e o bloco exibir 5, o bloco estará errado. O corpo da página é autoritativo.
- **Não inferir as medidas de proteção** que não estão indicadas na página. Se uma restrição existir, mas a página não a indicar, omita-a.

### &#x200B;5. Terminologia

Nomes canônicos, siglas, variantes aceitas, sinônimos, desambiguação. Principalmente para normalização de pipeline de IA.

```
**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [list]
* Synonyms: "[term A]" = "[term B]"
* Do not confuse: "[term]" ≠ "[other term]"
```

**Regra de precisão de status e ciclo de vida:**
Quando a página descreve um ciclo de vida (status da jornada, status da mensagem, estados da campanha etc.), copie os rótulos de status exatos do corpo da página. Não parafraseie. Use entradas &quot;Não confunda&quot; para desfazer a ambiguidade de status que compartilham uma palavra raiz, mas têm significado distinto. Exemplo:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Perguntas frequentes

3 a 6 perguntas que um usuário pode fazer, com respostas curtas.

```
**FAQ:**

* **Q: [question]** — [short answer]
```

**Regra de precisão de perguntas frequentes:**
As respostas devem usar as mesmas opções de verbo e substantivo que o corpo da página. Não introduza verbos como &quot;reverter&quot;, &quot;redefinir&quot; ou &quot;reverter&quot;, a menos que a página os use. Se uma transição encerrar uma sessão (por exemplo, sair do modo de teste retorna a jornada ao seu estado anterior), diga exatamente isso: não diga &quot;a jornada reverte para Rascunho&quot;.

### O que NÃO incluir

- **não** regravar ou resumir o conteúdo do corpo (ele já está na página)
- **não** incluir instruções passo a passo
- **não** inventar conteúdo não suportado pela página
- **não** usar os termos imprecisos a seguir, a menos que eles apareçam textualmente no corpo da página: &quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;, &quot;reverter&quot;, &quot;reverter&quot; (ao descrever as transições de estado do produto)

---

## Lista de verificação de validação pós-geração

Execute essa lista de verificação em cada bloco antes de gravar a inclusão. Sinalize ao usuário qualquer falha antes de continuar.

### Verificação da grade de proteção

- [ ] Todos os valores numéricos no bloco existem textualmente ou são derivados do corpo da página
- [ ] Todo limite é qualificado conforme recomendado ou fixo
- [ ] Cada figura de taxa de transferência inclui seu escopo (sandbox/organização/instância)

### Verificação de terminologia
- [ ] Todos os modos de validação (Simulação, Modo de teste, Execução a seco) presentes na página são incluídos e nomeados com termos precisos da página
- [ ] Todos os status do ciclo de vida usam os rótulos exatos do corpo da página
- [ ] Não há verbos imprecisos nas respostas das perguntas frequentes (&quot;reverter&quot;, &quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;) a menos que presentes textualmente na página

### Verificação de escopo
- [ O Glossário de ] não contém termos de marketing genéricos não relacionados à página
- [ As respostas de perguntas frequentes do ] não apresentam informações ausentes na página

Se alguma verificação falhar, corrija o bloco antes de gravar a inclusão. Registre a correção no relatório Etapa 5.

---

## Sincronizar responsabilidade

O bloco de Referência de conhecimento de IA é um derivado do corpo da página em um momento específico. Ele deve ser tratado como parte da página.

**Quando o corpo da página for atualizado (liberar PRs, correções etc.):**

- Se a atualização alterar qualquer garantia, limite, rótulo de status ou modo de validação descrito no bloco → regenerar ou atualizar manualmente o bloco na mesma PR.
- Se a atualização não estiver relacionada ao conteúdo do bloco (por exemplo, etapas de procedimento, atualizações de captura de tela) → o bloco pode permanecer inalterado, mas revise-o brevemente.

O comentário de sincronização dentro do arquivo de inclusão (`<!-- ai-section-version -->`) é o sinal: se o corpo da página de inclusão tiver sido alterado desde que esse hash foi gravado, o bloco será um candidato para revisão. Ao atualizar, edite o arquivo de inclusão em `help/_includes/do-not-localize/`, não a página.

---

## Modelo completo

Incluir arquivo (`help/_includes/do-not-localize/<section-folder>/ai-augmented-<page>.md`):

```markdown
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

* **TL;DR:** [one sentence]

**Intents:**

* [intent]

**Glossary:**

* **[Term]**: [definition] *(product-specific)*

**Guardrails:**

* [guardrail — qualify each numeric limit as recommended|hard, each throughput figure with scope sandbox|org]

**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [variants]
* Synonyms: "[a]" = "[b]"
* Do not confuse: "[x]" ≠ "[y]"

**FAQ:**

* **Q: [question]** — [short answer]

+++

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

Linha adicionada à página:

```
{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-end-journey.md}}
```

## Notas

- Processar arquivos um por um para qualidade.
- Sinalizar páginas muito curtas ou somente índice e perguntar ao usuário se ele deve ignorar.
- O único novo arquivo criado por página é a inclusão do tipo não localizado (Etapa 4); a própria página é editada apenas para adicionar a única linha `{{$include}}`. Não crie ou reestruture arquivos de outra forma.
- A lista de verificação de validação pós-geração não é opcional. Execute-o para cada arquivo, incluindo operações em massa.
