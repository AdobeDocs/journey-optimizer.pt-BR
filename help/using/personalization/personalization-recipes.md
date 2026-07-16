---
title: Receitas de personalização
description: Padrões de personalização comuns e exemplos reais para o Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 18067b68e09b98e616126dd40b8ad729233c49fa
workflow-type: tm+mt
source-wordcount: 1530
ht-degree: 0%

---

# Receitas de personalização {#personalization-recipes}

>[!BEGINSHADEBOX]

**Nesta página:** encontre receitas de personalização prontas para uso para datas, matrizes, cadeias de caracteres, lógica condicional e casos de borda do PQL que você pode copiar diretamente para o conteúdo do Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Esta página fornece padrões de personalização prontos para uso para os casos de uso mais comuns no Adobe Journey Optimizer. Todos os exemplos usam a sintaxe do editor de personalização e podem ser copiados diretamente para o conteúdo de email, SMS ou push.

Para obter uma referência completa das funções disponíveis, consulte [Funções auxiliares](functions/helpers.md), [Funções de data/hora](functions/dates.md), [Funções de cadeia de caracteres](functions/string.md) e [Funções de matriz](functions/arrays-list.md).

>[!TIP]
>
>Antes de copiar os exemplos, analise as [práticas recomendadas da Personalization](personalization-syntax.md#best-practices) para evitar os erros de sintaxe mais comuns.

## Receitas de data e hora {#date-time-recipes}

### Receita 1 — Exibir a data atual em um formato legível {#recipe-current-date}

Use `formatDate` com `getCurrentZonedDateTime()` para renderizar a data de hoje em qualquer formato:

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

Saída (exemplo): `April 11, 2026`

**Padrões comuns de formato:**

| Padrão | Exemplo de saída |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>Use letras minúsculas `y` (ano civil) em vez de `Y` (ano baseado em semana) para evitar resultados inesperados nos limites do ano. Consulte [caracteres padrão](functions/dates.md#pattern-characters) para obter a referência completa.

### Receita 2 — Contagem regressiva para uma data de expiração ou de evento {#recipe-countdown}

Use `dateDiff` para calcular o número de dias restantes até um atributo de data de perfil e, em seguida, renderizá-lo dinamicamente:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

Saída (exemplo): `Your reward points expire in 7 days. Use them before they're gone!`

### Receita 3 — X dias antes de uma data final dinâmica {#recipe-days-before}

Para calcular uma data X dias antes de um atributo de perfil (por exemplo, para referência em conteúdo ou linhas de assunto), use `addDays` com um deslocamento negativo:

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

Saída (exemplo): `April 04, 2026` *(7 dias antes de 11 de abril)*

Para também definir uma hora fixa do dia (por exemplo, 9h), combine com `setHours`:

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### Fórmula 4 — Exibir a hora atual somente como HH:MM {#recipe-time-only}

Use `extractHours` e `extractMinutes` para mostrar apenas a parte de tempo, com uma proteção zero à esquerda por minutos:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Saída (exemplo): `Your appointment is at 14:05.`

### Fórmula 5 — Detectar fim de semana vs. dia da semana {#recipe-weekend}

Use `dayOfWeek` para adaptar o conteúdo com base no dia. A função retorna 1 (segunda-feira) a 7 (domingo). Usar o operador único `=` (sintaxe PQL, não `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()` é para adaptar o **conteúdo** com base no dia. Para perfis de roteamento diferentes em uma jornada com base no dia da semana, use a opção incorporada **Condição de tempo → Dia da semana** na atividade Condição de jornada. [Saiba mais](../building-journeys/condition-activity.md#date_condition)

## Receitas de matriz e loop {#array-recipes}

### Fórmula 6 — Listar todos os itens de uma matriz de perfis {#recipe-list-items}

Use `{{#each}}` para iterar sobre uma matriz de perfil e renderizar cada item. Isso está disponível somente no editor de personalização (email, SMS, push):

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

Saída (exemplo):

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>Não há suporte para `{{#each}}` na atividade de condição de jornada. Para filtragem de matriz em condições, use [funções de gerenciamento de coleção](../building-journeys/expression/collection-management-functions.md).

### Receita 7 — Mostrar os N itens principais de uma matriz por preço {#recipe-first-n}

Use `topN` para classificar e recuperar os N itens principais por um campo numérico. Como `topN` é uma função PQL, atribua-a a uma variável primeiro com `{% let %}` e, em seguida, execute um loop com `{{#each}}`:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)` classifica os pedidos por `price` em ordem decrescente e retorna os 3 primeiros — não retorna simplesmente os 3 primeiros itens na ordem original da matriz.

Ou use `head` para obter apenas o único item superior:

```sql
{%= head(profile.purchases.recentItems).name %}
```

### Fórmula 8 — Renderizar conteúdo condicionalmente por item da matriz {#recipe-conditional-loop}

Use `{%#if%}` dentro de `{{#each}}` para renderizar a saída somente para itens correspondentes. Defina um alias de loop com `as |order|` para que o avaliador do PQL possa resolver a referência de atributo na condição:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status` funciona em expressões Handlebars, mas não foi resolvido pelo avaliador do PQL dentro de `{%#if%}`. Usar um alias de loop nomeado (por exemplo, `order`) torna o atributo disponível para os contextos Handlebars e PQL.

## Cadeia de caracteres e receitas de formatação {#string-recipes}

### Receita 9 — Limpar uma string com replaceAll e reutilizá-la {#recipe-replaceall-reuse}

`replaceAll` retorna um novo valor — ele não modifica o original. Use `{% let %}` para armazenar o resultado e referenciá-lo várias vezes sem repetir a chamada de função:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

Saída (exemplo):

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### Receita 10 — Aspas duplas em um valor na saída JSON {#recipe-json-quotes}

Para incluir aspas duplas literais em uma cadeia de caracteres (por exemplo, gerando JSON para uma carga personalizada), use uma barra invertida (`\"`) para escapará-la:

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

Saída: `{ "greeting": "Hello \"John\"" }`

### Fórmula 11 — Formatar um componente de data em maiúsculas {#recipe-uppercase-date}

Combine `formatDate` com `upperCase` para renderizar os nomes de mês ou dia em maiúsculas:

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

Saída (exemplo): `APRIL`

Para uma string de data em maiúsculas completa:

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

Saída (exemplo): `WEDNESDAY JANUARY 01 2020`

## Receitas de lógica condicional {#conditional-recipes}

### Receita 12 — IF/ELSEIF/ELSE no conteúdo personalizado {#recipe-if-elseif}

Use `{%#if%}`, `{%else if%}` e `{%else%}` para lógica condicional de várias ramificações. Esse padrão funciona em conteúdo e fragmentos de email:

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### Receita 13 — Exibição de atributo seguro nulo {#recipe-null-safe}

Use um fallback condicional para evitar a renderização de valores vazios quando um atributo de perfil for nulo ou estiver ausente:

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

Ou incorporado com um padrão de estilo ternário usando `isEmpty`:

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## receitas de caso de borda do PQL {#pql-edge-cases}

### Fórmula 14 — Fazer referência a uma chave de atributo hifenizada {#recipe-hyphenated-key}

Se o nome do campo de esquema XDM contiver hifens (por exemplo, `order-total`, `event-type`), coloque-o entre acentos graves dentro de uma expressão PQL para impedir que o hífen seja interpretado como um operador de subtração:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>Os acentos graves só têm suporte em expressões PQL (`{%= ... %}`). Eles não são aceitos na interpolação (`{{...}}`) de Handlebars simples. Se você precisar renderizar um valor de campo hifenizado diretamente, avalie-o por meio de uma expressão PQL ou armazene-o em uma variável usando `{% let %}` primeiro.

### Receita 15 — Fazer referência a uma ID de evento numérica em um atributo de contexto {#recipe-numeric-event-id}

Ao usar um evento de contexto de jornada cuja ID é uma sequência numérica (por exemplo, `1697323153`), coloque a ID entre acentos graves e use `{% let %}` com `toDateTime()` e `formatDate()`:

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

Saída (exemplo): `Your appointment: 18/03/2026 14:30`

### Fórmula 16 — Coerção de tipo: comparar um campo de string com um número {#recipe-type-coercion}

O PQL é altamente digitado. Quando um campo de perfil é armazenado como uma cadeia de caracteres, mas você precisa compará-lo numericamente, converta-o primeiro com `stringToNumber()`:

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

Para campos booleanos armazenados como strings:

```sql
{%= toBool(profile.consents.email.val) = true %}
```

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página fornece 16 receitas de personalização prontas para uso do tipo copiar-colar, que abrangem datas, matrizes, strings, lógica condicional e casos de borda do PQL para uso em conteúdo de email, SMS e push do Journey Optimizer.

**Intenções**

* Copiar padrões de data/hora prontos para uso (data atual, contagem regressiva, datas de deslocamento, exibição de hora, detecção de fim de semana)
* Copiar padrões de matriz e loop (itens de lista, itens N principais, renderização condicional por item)
* Copiar padrões de formatação de cadeia de caracteres (limpar e reutilizar cadeias de caracteres, aspas JSON, componentes de data em maiúsculas)
* Copiar padrões lógicos condicionais (multi-branch if/elseif/else, exibição de atributo null-safe)
* Lidar com casos de borda do PQL (chaves hifenizadas, IDs de evento numéricas, coerção de tipo)

>[!TAB Glossário]

* **Receita do Personalization**: um padrão pronto para uso de copiar e colar para um caso de uso de personalização comum, usando a sintaxe do editor de personalização. *(específico do produto)*
* **`formatDate`**: uma função que converte uma data em uma cadeia de caracteres usando um padrão de formato especificado (por exemplo, `"MMMM dd, yyyy"`).
* **`dateDiff`**: uma função que calcula a diferença numérica entre duas datas.
* **`getCurrentZonedDateTime()`**: uma função que retorna a data e hora atuais em um formato sensível a fuso horário.
* **`topN`**: uma função PQL que classifica uma matriz por um campo numérico especificado em ordem decrescente e retorna os N itens principais. Deve ser atribuído via `{% let %}` antes do uso em um loop Handlebars.
* **`{% let %}`**: Sintaxe de atribuição de variável Handlebars para o armazenamento de valores calculados; necessário quando um resultado de função PQL precisa ser referenciado em um contexto Handlebars subsequente.
* **`replaceAll`**: uma função de cadeia de caracteres que substitui todas as ocorrências de um padrão em uma cadeia de caracteres; retorna uma nova cadeia de caracteres sem modificar o original.

>[!TAB Terminologia]

* **Nome canônico:** fórmula de personalização — variantes: padrão, modelo, exemplo, padrão copiar-colar
* **Não confundir:** `{%= ... %}` (sintaxe de expressão PQL — avaliada, retorna um valor calculado) ≠ `{{...}}` (Interpolação Handlebars — renderiza uma expressão de variável ou de modelo)
* **Não confunda:** `{%#if%}` / `{%/if%}` (sintaxe condicional Journey Optimizer, chaves percentuais) ≠ `{{#if}}` / `{{/if}}` (sintaxe condicional Handlebars padrão)
* **Não confundir:** `topN(array, field, n)` (classifica por campo em ordem decrescente, retorna o N superior) ≠ `head(array)` (retorna somente o primeiro item da matriz)
* **Não confunda:** `dayOfWeek()` (usado no conteúdo da mensagem para adaptar a exibição com base no dia) ≠ a opção Condição de tempo de jornada &quot;Dia da semana&quot; (usada na atividade de Condição de jornada para rotear perfis de forma diferente)
* **Não confunda:** padrão de formato de data `y` (ano civil — correto) ≠ `Y` (ano baseado em semana — pode produzir resultados inesperados em limites de ano)

>[!TAB Medidas de proteção e limitações]

* Não há suporte para `{{#each}}` na atividade de condição de jornada; use funções de gerenciamento de coleções para filtragem de matriz em condições de jornada.
* O escape de backtick para chaves de atributo hifenizadas só tem suporte em expressões PQL (`{%= ... %}`); backticks não são aceitos na interpolação Handlebars simples (`{{...}}`).
* `topN` é uma função PQL e deve ser atribuída a uma variável `{% let %}` antes de ser usada como um destino de loop `{{#each}}`.
* Ao usar uma variável de loop dentro de um bloco `{%#if%}`, declare um alias de loop nomeado (por exemplo, `as |order|`); `this.status` não é resolvido pelo avaliador do PQL dentro de `{%#if%}`.
* Use minúsculas `y` em `formatDate` padrões para o ano civil; `Y` (ano baseado em semana) pode produzir valores inesperados nos limites do final do ano.

>[!TAB Perguntas frequentes]

**P: Qual é a diferença entre `{%= ... %}` e `{{...}}` na personalização?**

`{%= ... %}` é a sintaxe de expressão do PQL — é avaliada e retorna um valor calculado (número, sequência, booleano). `{{...}}` é a interpolação Handlebars — ela renderiza uma variável ou expressão de modelo. Ambos aparecem no conteúdo de personalização, mas atendem a diferentes objetivos.

**P: Como usar um resultado de função PQL dentro de um loop Handlebars `{{#each}}`?**

Atribua o resultado da função PQL a uma variável usando `{% let variableName = pqlFunction(...) %}` e, em seguida, use `{{#each variableName}}` para iterar sobre ele.

**P: `{{#each}}` pode ser usado em uma atividade de condição de jornada?**

Não. `{{#each}}` está disponível somente no conteúdo de personalização de mensagens (email, SMS, push). Para filtragem de matriz em condições de jornada, use funções de gerenciamento de coleção.

**P: Como faço referência a um campo cujo nome contém um hífen?**

Envolva a chave hifenizada em acentos graves dentro de uma expressão PQL: ``{%= profile.events.`order-total` > 100 %}``. Os acentos graves não são suportados na interpolação Handlebars simples — use uma variável `{% let %}` como uma etapa intermediária, se necessário.

**P: Por que `topN` precisa de `{% let %}` antes de um loop `{{#each}}`?**

`topN` é uma função PQL que retorna uma lista PQL. Atribuí-lo a uma variável `{% let %}` torna o resultado disponível no contexto Handlebars para que ele possa ser iterado com `{{#each}}`.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 20c7ee0f -->

