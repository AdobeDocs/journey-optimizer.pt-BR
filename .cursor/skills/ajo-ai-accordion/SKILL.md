---
name: ajo-ai-accordion
description: Enriquece as páginas da documentação do Adobe Journey Optimizer com uma seção da opção Assistente de IA anexada ao final de cada arquivo de Markdown. Lê cada página, gera automaticamente conteúdo relevante do AI Assistant com base no tópico da página e o insere como um acordeão recolhível. Use quando o usuário quiser adicionar informações de IA aos documentos do AJO, enriquecer as páginas do AJO Markdown com conteúdo de IA ou processar um arquivo ou pasta de arquivos do Markdown com seções de acordeão de IA.
disable-model-invocation: true
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# Enriquecimento do Acordeão do AJO AI

Adiciona uma opção de Assistente de IA gerada automaticamente ao final de um ou mais arquivos de marcação no repositório da documentação do Journey Optimizer.

## Repositório de destino

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## Sintaxe do acordeão (Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regras:**
- `+++Title` em uma linha — o título segue imediatamente `+++`, sem espaço entre
- `+++` sozinho em uma linha fecha o acordeão
- Linha em branco antes da abertura de `+++` e após o fechamento de `+++`

&#x200B;---

## Fluxo de trabalho

### Etapa 1 — Solicitar o(s) target(s)

Pergunte ao usuário:

> Que arquivo ou pasta você deseja enriquecer?
> - Arquivo único: caminho relativo à raiz do repositório (ex.: `help/using/email/get-started-email.md`)
> - Pasta: processa todos os `.md` arquivos dentro de forma recursiva (por exemplo, `help/using/email`)
> - Lista de arquivos/pastas

Use `AskQuestion`, se disponível; caso contrário, pergunte de forma conversacional.

Se uma pasta for fornecida, liste todos os `.md` arquivos encontrados e confirme com o usuário antes do processamento.

### Etapa 2 — Para cada arquivo: leia e gere

Para cada arquivo de destino:

1. **Leia o arquivo** por completo.
2. **Entenda o tópico da página** — que recurso, conceito ou tarefa ele aborda?
3. **Gere o conteúdo do acordeão** usando as regras de geração de conteúdo abaixo.
4. **Verifique** se uma opção de IA já existe no final do arquivo (procure `+++` perto do final). Se isso acontecer, pergunte ao usuário se ele deseja substituir ou ignorar.

### Etapa 3 — Anexar o acordeão

Anexar no final do arquivo:

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

Nenhum outro conteúdo no arquivo deve ser modificado.

### Etapa 4 — Relatório

Depois que todos os arquivos forem processados:
- Listar arquivos modificados ✓
- Listar arquivos ignorados e o motivo (já tem a opção, arquivo vazio, não relevante etc.)

&#x200B;---

## Regras de geração de conteúdo

Gere o conteúdo do acordeão analisando a página de marcação. Produza as seguintes seções **em ordem**, formatadas como listas de marcadores de markdown. Ignore qualquer seção para a qual nenhum conteúdo significativo possa ser extraído da página.

&#x200B;---

### Título do acordeão

Uso: `+++AI Assistant — Page context`

&#x200B;---

### Seções a serem geradas (em ordem)

**1. TL;DR**

Uma frase. O que esta página ensina ou habilita?

```markdown
- **TL;DR:** [one sentence summary]
```

&#x200B;---

**2. Intenções**

Lista com marcadores do que um usuário pode realizar após ler esta página (3 a 6 itens).

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

&#x200B;---

**3. Glossário**

Termos principais específicos desta página/recurso, com uma breve definição. Sinalizar termos específicos do produto.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

Inclua somente termos relevantes ao tópico desta página. Não compartilhe com termos de marketing genéricos.

&#x200B;---

**4. Medidas de proteção**

Limitações, pré-requisitos, permissões ou restrições mencionadas na página.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

&#x200B;---

**5. Terminologia**

Nomes canônicos de produtos, siglas, variantes aceitas, sinônimos e dicas de desambiguação. Esta seção é principalmente para normalização de pipeline de IA.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

Inclua somente entradas presentes ou implícitas na página.

&#x200B;---

**6. Perguntas frequentes**

3 a 6 perguntas que um usuário pode fazer sobre o conteúdo desta página, com respostas curtas.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

&#x200B;---

### O que NÃO incluir

- **não** regravar ou resumir o conteúdo do corpo da página (ela já existe).
- **não** inclua instruções passo a passo (elas estão na página).
- **não** invente conteúdo que não seja suportado pela página.

&#x200B;---

### Modelo do acordeão completo

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## Notas

- Processar arquivos um por um, não em massa, para manter alta a qualidade da geração.
- Se a página for muito curta ou meramente uma página de redirecionamento/índice, sinalize-a e pergunte ao usuário se ele deseja ignorá-la.
- Não criar novos arquivos — editar apenas arquivos `.md` existentes.
