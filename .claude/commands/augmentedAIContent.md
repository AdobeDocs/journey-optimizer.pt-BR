---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# aumentedAIContent

Acrescenta uma seção de **Referência rápida** gerada automaticamente ao final de um ou mais arquivos de marcação no repositório da documentação do Journey Optimizer.

## Repositório de destino

`help/using/` (relativo à raiz do repositório)

## Sintaxe de seção e guia (Experience League)

### Título da seção

```
## Quick reference {#quick-reference}
```

### Guias

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**Regras:**

- `>[!BEGINTABS]` e `>[!ENDTABS]` cada um na sua própria linha, cercado por linhas em branco
- `>[!TAB Name]` na sua própria linha, seguido por uma linha em branco antes do conteúdo
- Os nomes das guias são letras maiúsculas e minúsculas (1-3 palavras)
- Linha em branco antes de `>[!BEGINTABS]` e depois de `>[!ENDTABS]`

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
3. **Gere o conteúdo da seção** usando as regras de geração de conteúdo abaixo.
4. **Executar a lista de verificação de validação de pós-geração** (veja abaixo) — não ignorar.
5. **Verifique** se já existe uma seção de Referência rápida no final (procure `## Quick reference` próximo ao final). Em caso afirmativo, perguntar ao usuário: substituir ou ignorar?

### Etapa 3 — verificar todas as reclamações em relação ao corpo da página

Antes de anexar, leia novamente a declaração de seção gerada por declaração. Esta etapa é **obrigatória e não pode ser ignorada**, mesmo para arquivos curtos. Corrija qualquer falha antes de prosseguir para a Etapa 4.

**Terminologia e rótulos**

- [ ] Cada termo, rótulo e nome de interface na seção aparece no corpo da página — não é importado de outra página ou inferido a partir do conhecimento geral do produto
- [ ] Nenhum sinônimo é listado, a menos que ambos os formulários apareçam na página
- [ ] Cada entrada &quot;Não confunda&quot; faz referência apenas aos conceitos mencionados nesta página

**Medidas de proteção e limites**

- [ ] Cada valor numérico corresponde exatamente ao corpo da página
- [ ] Um limite é chamado de **hard** somente se o corpo da página usar essa palavra ou implicar claramente que o sistema a impõe (por exemplo, &quot;não pode exceder&quot;, &quot;máximo ... permitido&quot;, &quot;apenas ... com suporte&quot;)
- [ ] Um limite é chamado de **recomendado** somente se o corpo da página usar essa palavra ou uma equivalente (&quot;para melhor desempenho&quot;, &quot;é recomendado&quot;)
- [ ] Se o corpo da página não fornecer nenhum qualificador, a seção não fornecerá nenhum — não invente um
- [ ] Nenhum meta-comentário sobre o que a página de origem diz ou não diz (por exemplo, &quot;nenhum número específico é declarado nesta página&quot;)

**Definições de glossário**

- [ ] Nenhuma definição contém detalhes técnicos ausentes no corpo da página
- [ ] Nenhuma entrada elabora usando informações de outras páginas no conjunto de documentação

**Perguntas frequentes**

- [ ] Cada detalhe específico (recursos da interface, nomes de botão, nomes de campo, sequências de etapas) é declarado no corpo da página, não inferido ou importado de outras páginas
- [ ] Nenhuma resposta introduz informações que o corpo da página não endereça

**Regra de correção:** Se qualquer verificação falhar, corrija o conteúdo **antes** ao anexar. Registre cada correção no relatório de Etapa 5.

---

### Etapa 4 — Anexar a seção

Use o bloco de abertura fixo e o modelo completo definidos nas **Regras de geração de conteúdo** abaixo. Anexe no final do arquivo, seguido imediatamente pelo comentário de sincronização:

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

Esse comentário permite que ferramentas e autores futuros detectem quando o corpo da página foi deslocado da seção. Não modifique nenhum outro conteúdo.

### Etapa 5 — Relatório

- Arquivos modificados ✓
- Arquivos ignorados + motivo (já tem seção / vazia / página de índice)
- Quaisquer avisos de validação gerados durante a Etapa 2

---

## Regras de geração de conteúdo

Analise a página e produza as guias abaixo de **em ordem**. Ignore totalmente uma guia se nenhum conteúdo significativo puder ser extraído para ela.

### Título da seção e abertura fixa — textualmente, não modificar

Cada seção de Referência rápida deve começar com este bloco exato. Copie como está; não parafraseie, condense ou reordene:

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

O bloco `>[!BEGINTABS]` segue imediatamente após esses dois parágrafos.

### Guia 1 - Visão geral

Resumo de TL;DR em uma frase sobre o que a página ensina ou habilita, seguido de 3 a 6 coisas que um usuário pode realizar após ler esta página.

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### Guia 2 - Glossário

Termos principais específicos desta página/recurso com definições curtas. Sinalizar termos específicos do produto.

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

Inclua somente termos relevantes a esta página. Não compartilhe com termos de marketing genéricos.

**Regra de precisão de modo de validação — obrigatória:**
Se a página abranger qualquer forma de teste, pré-visualização ou execução simulada, você DEVERÁ distinguir entre todos os modos que a página realmente descreve. Não recolha modos distintos em uma única entrada abreviada:
- **Simulação** — renderiza o conteúdo da mensagem sem enviar; usa perfis reais
- **Modo de teste** — envia somente para perfis de teste designados; usa perfis de teste persistentes do AEP (não perfis sintéticos ou falsos)
- **Dry run** — executa a lógica de jornada completa sem ativar ações; usa dados de público-alvo reais

Inclua apenas os modos presentes na página. Copie o termo preciso do produto no corpo da página — não substitua &quot;perfis sintéticos&quot;, &quot;dados falsos&quot; ou &quot;sem dados reais&quot; por nenhum desses.

### Guia 3 - Terminologia

Nomes canônicos, siglas, variantes aceitas, sinônimos, desambiguação. Principalmente para normalização de pipeline de IA.

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**Regra de precisão de status e ciclo de vida:**
Quando a página descreve um ciclo de vida (status da jornada, status da mensagem, estados da campanha etc.), copie os rótulos de status exatos do corpo da página. Não parafraseie. Use entradas &quot;Não confunda&quot; para desfazer a ambiguidade de status que compartilham uma palavra raiz, mas têm significado distinto. Exemplo:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### Guia 4 — Medidas de proteção e limitações

Limitações, pré-requisitos, permissões ou restrições mencionadas na página.

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**Regras de precisão da grade de proteção — obrigatório:**

- **Qualifique todos os limites numéricos** como recomendados ou rígidos. Exemplo: &quot;Máximo de 10 pesquisas de conjunto de dados por mensagem (limite rígido)&quot; e não &quot;Máximo de 10 pesquisas de conjunto de dados&quot;.
- **Qualifique cada taxa de transferência ou figura** com seu escopo. Exemplo: &quot;Limite de TPS de 150.000 mensagens/hora (por sandbox)&quot; e não &quot;Limite de 150.000 mensagens/hora&quot;.
- **Verifique todas as medidas de proteção em relação ao corpo da página** antes de incluí-la. Se a página disser 10 e a seção disser 5, a seção está errada. O corpo da página é autoritativo.
- **Não inferir as medidas de proteção** que não estão indicadas na página. Se uma restrição existir, mas a página não a indicar, omita-a.

### Guia 5 — Perguntas frequentes

3 a 6 perguntas que um usuário pode fazer, com respostas curtas. Formate cada uma delas como um cabeçalho em negrito de pergunta seguido por uma resposta de parágrafo.

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
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

Execute esta lista de verificação em cada seção antes de anexar. Sinalize ao usuário qualquer falha antes de continuar.

### Verificação da grade de proteção

- [ ] Todos os valores numéricos na seção existem textualmente ou são derivados do corpo da página
- [ ] Todo limite é qualificado conforme recomendado ou fixo
- [ ] Cada figura de taxa de transferência inclui seu escopo (sandbox/organização/instância)

### Verificação de terminologia
- [ ] Todos os modos de validação (Simulação, Modo de teste, Execução a seco) presentes na página são incluídos e nomeados com termos precisos da página
- [ ] Todos os status do ciclo de vida usam os rótulos exatos do corpo da página
- [ ] Não há verbos imprecisos nas respostas das perguntas frequentes (&quot;reverter&quot;, &quot;sintético&quot;, &quot;dados falsos&quot;, &quot;sem dados reais&quot;) a menos que presentes textualmente na página

### Verificação de escopo
- [ O Glossário de ] não contém termos de marketing genéricos não relacionados à página
- [ As respostas de perguntas frequentes do ] não apresentam informações ausentes na página

Se alguma verificação falhar, corrija a seção antes de anexar. Registre a correção no relatório Etapa 4.

---

## Sincronizar responsabilidade

A seção Referência rápida é uma derivada do corpo da página em um ponto no tempo. Ele deve ser tratado como parte da página.

**Quando o corpo da página for atualizado (liberar PRs, correções etc.):**

- Se a atualização alterar qualquer garantia, limite, rótulo de status ou modo de validação descrito na seção → gere novamente ou atualize manualmente a seção na mesma PR.
- Se a atualização não estiver relacionada ao conteúdo da seção (por exemplo, etapas de procedimento, atualizações de captura de tela) → a seção pode permanecer inalterada, mas revise-a brevemente.

O comentário de sincronização anexado após a seção (`<!-- ai-section-version -->`) é o sinal: se o conteúdo do arquivo antes da seção tiver sido alterado desde que esse hash foi gravado, a seção será candidata para revisão.

---

## Modelo completo

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## Notas

- Processar arquivos um por um para qualidade.
- Sinalizar páginas muito curtas ou somente índice e perguntar ao usuário se ele deve ignorar.
- Não criar novos arquivos — editar apenas arquivos `.md` existentes.
- A lista de verificação de validação pós-geração não é opcional. Execute-o para cada arquivo, incluindo operações em massa.
