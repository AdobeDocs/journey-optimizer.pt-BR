---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# aumentedAIContent

Adiciona uma opção de Assistente de IA gerada automaticamente ao final de um ou mais arquivos de marcação no repositório da documentação do Journey Optimizer.

## Repositório de destino

`help/using/` (relativo à raiz do repositório)

## Sintaxe do acordeão (Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regras:**
- `+++Title` em uma linha — o título segue imediatamente `+++`
- `+++` sozinho em uma linha fecha o acordeão
- Linha em branco antes da abertura de `+++` e após o fechamento de `+++`

&#x200B;---

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
3. **Gere o conteúdo do acordeão** usando as regras de geração de conteúdo abaixo.
4. **Executar a lista de verificação de validação de pós-geração** (veja abaixo) — não ignorar.
5. **Verifique** se uma opção de IA já existe no final (procure `+++AI Knowledge Reference` perto do final). Em caso afirmativo, perguntar ao usuário: substituir ou ignorar?

### Etapa 3 — Anexar o acordeão

Use o bloco de abertura fixo e o modelo completo definidos nas **Regras de geração de conteúdo** abaixo. Anexe no final do arquivo, seguido imediatamente pelo comentário de sincronização:

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

Este comentário permite que ferramentas e autores futuros detectem quando o corpo da página foi deslocado do acordeão. Não modifique nenhum outro conteúdo.

### Etapa 4 — Relatório

- Arquivos modificados ✓
- Arquivos ignorados + motivo (já tem a opção acordeão / vazia / página de índice)
- Quaisquer avisos de validação gerados durante a Etapa 2

&#x200B;---

## Regras de geração de conteúdo

Analise a página e produza as seções abaixo de **em ordem** como listas de marcadores de marcação. Ignore as seções em que nenhum conteúdo significativo pode ser extraído.

### Título do acordeão e abertura fixa — textualmente, não modifique

Cada acordeão deve começar com este bloco exato. Copie como está; não parafraseie, condense ou reordene:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

As seções de conteúdo gerado seguem imediatamente após esses dois parágrafos.

### 1. TL;DR

Um resumo de frase do que a página ensina ou ativa.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. Intenções

3 a 6 coisas que um usuário pode realizar após ler esta página.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. Glossário

Termos principais específicos desta página/recurso com definições curtas. Sinalizar termos específicos do produto.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
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
- [guardrail]
```

**Regras de precisão da grade de proteção — obrigatório:**

- **Qualifique todos os limites numéricos** como recomendados ou rígidos. Exemplo: &quot;Máximo de 10 pesquisas de conjunto de dados por mensagem (limite rígido)&quot; e não &quot;Máximo de 10 pesquisas de conjunto de dados&quot;.
- **Qualifique cada taxa de transferência ou figura** com seu escopo. Exemplo: &quot;Limite de TPS de 150.000 mensagens/hora (por sandbox)&quot; e não &quot;Limite de 150.000 mensagens/hora&quot;.
- **Verifique todas as medidas de proteção em relação ao corpo da página** antes de incluí-la. Se a página disser 10 e o acordeão disser 5, o acordeão está errado. O corpo da página é autoritativo.
- **Não inferir as medidas de proteção** que não estão indicadas na página. Se uma restrição existir, mas a página não a indicar, omita-a.

### &#x200B;5. Terminologia

Nomes canônicos, siglas, variantes aceitas, sinônimos, desambiguação. Principalmente para normalização de pipeline de IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**Regra de precisão de status e ciclo de vida:**
Quando a página descreve um ciclo de vida (status da jornada, status da mensagem, estados da campanha etc.), copie os rótulos de status exatos do corpo da página. Não parafraseie. Use entradas &quot;Não confunda&quot; para desfazer a ambiguidade de status que compartilham uma palavra raiz, mas têm significado distinto. Exemplo:

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Perguntas frequentes

3 a 6 perguntas que um usuário pode fazer, com respostas curtas.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**Regra de precisão de perguntas frequentes:**
As respostas devem usar as mesmas opções de verbo e substantivo que o corpo da página. Não introduza verbos como &quot;reverter&quot;, &quot;redefinir&quot; ou &quot;reverter&quot;, a menos que a página os use. Se uma transição encerrar uma sessão (por exemplo, sair do modo de teste retorna a jornada ao seu estado anterior), diga exatamente isso: não diga &quot;a jornada reverte para Rascunho&quot;.

### O que NÃO incluir

- **não** regravar ou resumir o conteúdo do corpo (ele já está na página)
- **não** incluir instruções passo a passo
- **não** inventar conteúdo não suportado pela página
- **não** usar os termos imprecisos a seguir, a menos que eles apareçam textualmente no corpo da página: &quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;, &quot;reverter&quot;, &quot;reverter&quot; (ao descrever as transições de estado do produto)

&#x200B;---

## Lista de verificação de validação pós-geração

Execute esta lista de verificação em todas as opções antes de anexar. Sinalize ao usuário qualquer falha antes de continuar.

### Verificação da grade de proteção
- [ ] Todos os valores numéricos no acordeão existem textualmente ou são deriváveis do corpo da página
- [ ] Todo limite é qualificado conforme recomendado ou fixo
- [ ] Cada figura de taxa de transferência inclui seu escopo (sandbox/organização/instância)

### Verificação de terminologia
- [ ] Todos os modos de validação (Simulação, Modo de teste, Execução a seco) presentes na página são incluídos e nomeados com termos precisos da página
- [ ] Todos os status do ciclo de vida usam os rótulos exatos do corpo da página
- [ ] Não há verbos imprecisos nas respostas das perguntas frequentes (&quot;reverter&quot;, &quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;) a menos que presentes textualmente na página

### Verificação de escopo
- [ O Glossário de ] não contém termos de marketing genéricos não relacionados à página
- [ As respostas de perguntas frequentes do ] não apresentam informações ausentes na página

Se alguma verificação falhar, corrija a opção antes de anexar. Registre a correção no relatório Etapa 4.

&#x200B;---

## Sincronizar responsabilidade

O acordeão é uma derivada do corpo da página em um ponto no tempo. Ele deve ser tratado como parte da página.

**Quando o corpo da página for atualizado (liberar PRs, correções etc.):**
- Se a atualização alterar qualquer garantia, limite, rótulo de status ou modo de validação descrito no acordeão → regenerar ou atualizar manualmente o acordeão na mesma PR.
- Se a atualização não estiver relacionada ao conteúdo do acordeão (por exemplo, etapas de procedimento, atualizações de captura de tela) → o acordeão pode permanecer inalterado, mas analise-o brevemente.

O comentário de sincronização anexado após o acordeão (`<!-- ai-accordion-version -->`) é o sinal: se o conteúdo do arquivo antes do acordeão tiver sido alterado desde que esse hash foi gravado, o acordeão será um candidato para revisão.

&#x200B;---

## Modelo completo

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

&#x200B;---

## Notas

- Processar arquivos um por um para qualidade.
- Sinalizar páginas muito curtas ou somente índice e perguntar ao usuário se ele deve ignorar.
- Não criar novos arquivos — editar apenas arquivos `.md` existentes.
- A lista de verificação de validação pós-geração não é opcional. Execute-o para cada arquivo, incluindo operações em massa.
