---
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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
3. **Gere o conteúdo do acordeão** usando as regras abaixo.
4. **Verifique** se uma opção de IA já existe no final (procure `+++AI Assistant` perto do final). Em caso afirmativo, perguntar ao usuário: substituir ou ignorar?

### Etapa 3 — Anexar o acordeão

Anexar no final do arquivo. Não modifique nenhum outro conteúdo.

### Etapa 4 — Relatório

- Arquivos modificados ✓
- Arquivos ignorados + motivo (já tem a opção acordeão / vazia / página de índice)

---

## Regras de geração de conteúdo

Analise a página e produza as seções abaixo de **em ordem** como listas de marcadores de marcação. Ignore as seções em que nenhum conteúdo significativo pode ser extraído.

### Título do acordeão

`+++AI Assistant — Page context`

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

### &#x200B;4. Medidas de proteção

Limitações, pré-requisitos, permissões ou restrições mencionadas na página.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. Terminologia

Nomes canônicos, siglas, variantes aceitas, sinônimos, desambiguação. Principalmente para normalização de pipeline de IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. Perguntas frequentes

3 a 6 perguntas que um usuário pode fazer, com respostas curtas.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### O que NÃO incluir

- **não** regravar ou resumir o conteúdo do corpo (ele já está na página)
- **não** incluir instruções passo a passo
- **não** inventar conteúdo não suportado pela página

### Modelo completo

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
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## Notas

- Processar arquivos um por um para qualidade.
- Sinalizar páginas muito curtas ou somente índice e perguntar ao usuário se ele deve ignorar.
- Não criar novos arquivos — editar apenas arquivos `.md` existentes.
