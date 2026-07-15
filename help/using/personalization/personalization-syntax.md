---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, sintaxe, personalização
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1979
ht-degree: 2%

---

# Sintaxe de personalização {#personalization-syntax}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba mais sobre a sintaxe de personalização do Handlebars e do PQL no Adobe Journey Optimizer, incluindo regras gerais, palavras-chave reservadas, coerção de tipo, namespaces disponíveis e práticas recomendadas.

>[!ENDSHADEBOX]

O Personalization no [!DNL Journey Optimizer] usa duas sintaxes complementares que funcionam juntas na mesma expressão:

* **Handlebars** (`{{...}}`) — usado para renderizar atributos de perfil, sobrepor matrizes e auxiliares de bloco de chamadas. Consulte a [documentação de HandlebarsJS](https://handlebarsjs.com/) para obter uma referência completa.
* **Profile Query Language (PQL)** (`{%= ... %}`) — usado para chamar funções internas (por exemplo, `upperCase()`, `formatDate()`, `dateDiff()`) e avaliar expressões condicionais.

Entender em qual contexto você está é fundamental para evitar erros de tempo de execução. Por exemplo, uma chamada de função PQL colocada dentro de `{{...}}` falhará porque o Handlebars tenta resolvê-la como auxiliar, em vez de avaliá-la como uma expressão PQL.

**Exemplos:**

| Caso de uso | Sintaxe |
|----------|--------|
| Renderizar um atributo de perfil | `{{profile.person.name.firstName}}` |
| Chamar uma função PQL | `{%= upperCase(profile.person.name.firstName) %}` |
| Bloqueio condicional | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| Executar um loop em uma matriz | `{{#each profile.orders}}...{{/each}}` |

A estrutura de atributos é definida em um Esquema XDM do Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

>[!TIP]
>
>Para expressões prontas para uso que aplicam essas sintaxes a cenários do mundo real — formatação de data, contagem regressiva, fallbacks condicionais e muito mais — consulte a página **[Receitas do Personalization](personalization-recipes.md)**.

## Regras gerais de sintaxe {#general-rules}

* Os identificadores podem ser qualquer caractere unicode, exceto os seguintes caracteres especiais, que são reservados para a sintaxe Handlebars:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* A sintaxe diferencia maiúsculas de minúsculas.

* As palavras **true**, **false**, **null** e **undefined** só são permitidas na primeira parte de uma expressão de caminho.

* Em Handlebars, os valores retornados por {{expression}} são **HTML-escaped**. Se a expressão contiver `&`, a saída HTML-escaped retornada será gerada como `&amp;`. Se você não quiser que o Handlebars escape um valor, use o &quot;triple-stash&quot;.

  Suponha que o valor do campo `profile.person.name` seja &quot;Mark &amp; Mary&quot;. A sintaxe `{{profile.person.name}}` exibirá `Mark &amp; Mary`, enquanto `{{{profile.person.name}}}` exibirá `Mark & Mary`.

* Em relação a argumentos de funções literais, o analisador de linguagem de modelo não oferece suporte ao símbolo único de barra invertida sem escape (`\`). Este caractere deve ser evitado com um símbolo adicional de barra invertida (`\`). Exemplo:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* Para incluir uma **aspas duplas literais** dentro de um valor de sequência de caracteres (por exemplo, ao gerar saída JSON), use uma barra invertida (`\"`) para escapará-la:

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  Saída: `{ "message": "Hello \"John\"" }`

  Como alternativa, use o caractere triplo `{{{ }}}` para gerar HTML sem escape quando o próprio valor contiver caracteres especiais que você não deseja codificar em HTML.

## Palavras-chave reservadas {#reserved-keywords}

Determinadas palavras-chave são reservadas no Profile Query Language (PQL) e não podem ser usadas diretamente como nomes de campos ou variáveis em expressões de personalização. Se o esquema XDM contiver campos com nomes que correspondam a palavras-chave reservadas, você deverá fazer o escape com acentos graves (`` ` ``) para referenciá-los em suas expressões.

**As palavras-chave reservadas incluem:**

* `next`
* `last`
* `this`

**Exemplo:**

Se o esquema de perfil tiver um campo chamado `next`, você deverá envolvê-lo em acentos graves:

```
{{profile.person.`next`.name}}
```

Sem os backticks, o editor de personalização falhará a validação com um erro.

>[!NOTE]
>
>O escape de backtick para palavras-chave reservadas se aplica tanto a caminhos Handlebars `{{...}}` quanto a expressões PQL `{%= ... %}`, pois essas palavras-chave são reservadas no nível de resolução de caminho. Isso é diferente de nomes de campo hifenizados, em que o escape de backtick é compatível somente dentro de expressões PQL. Consulte [Chaves de atributo hifenizadas](#hyphenated-keys).

## Regras de sintaxe do PQL para chaves de atributo especiais {#pql-special-keys}

Além das palavras-chave reservadas, dois casos adicionais exigem o escape de backtick em expressões PQL.

### Chaves de atributo hifenizadas {#hyphenated-keys}

Se o esquema XDM contiver nomes de campo com hifens (por exemplo, `my-field`, `event-type`) ou nomes que comecem com ou contenham números, coloque a chave entre acentos graves dentro de expressões PQL:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>O escape de backtick só tem suporte em expressões PQL (`{%= ... %}`). Não há suporte para isso na interpolação Handlebars (`{{...}}`). No entanto, nomes de campos hifenizados podem ser referenciados diretamente em `{{...}}` blocos (por exemplo, `{{profile.my-custom-field}}`); somente a sintaxe de backtick falha lá.

Sem acentos graves em uma expressão PQL, o hífen é interpretado como um operador de subtração e causa um erro de sintaxe do PQL.

### IDs de evento numérico em atributos de contexto {#numeric-event-ids}

Ao fazer referência a atributos de evento de contexto em que a ID do evento é um número (por exemplo, `1697323153`), coloque-a entre acentos graves. Isso também se aplica dentro de funções como `formatDate()`:

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## Coerção de tipo {#type-coercion}

O PQL é altamente digitado. Ao comparar ou transmitir valores, ambos os lados devem ser do mesmo tipo. Casos comuns:

| Cenário | Solução |
|----------|----------|
| Valor numérico armazenado como uma string | Usar `stringToNumber()` antes da aritmética ou comparação: `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| Inteiro armazenado como cadeia de caracteres | Usar `string_to_integer()` ou `stringToNumber()` antes da aritmética |
| Booleano armazenado como string | Usar `toBool()` para converter: `{%= toBool(profile.consents.email.val) = true %}` |

## Namespaces disponíveis {#namespaces}

* **Perfil**

  Este namespace permite referenciar todos os atributos definidos no esquema de perfil descrito na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

  Os atributos precisam ser definidos no esquema antes de serem referenciados em um bloco de personalização [!DNL Journey Optimizer].

  Para obter mais informações sobre como utilizar atributos de perfil em condições, consulte [esta seção](functions/helpers.md#if-function).

  +++Exemplos de referências

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Público-alvo**

  Para saber mais sobre o serviço de segmentação, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.

* **Ofertas**

  Esse namespace permite fazer referência às decisões de ofertas existentes.

  Para fazer referência a uma oferta, é necessário declarar um caminho com as diferentes informações que definem uma oferta. Esse caminho tem a seguinte estrutura:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  em que:

   * `offers` identifica a expressão de caminho pertencente ao namespace da oferta
   * `Type` determina o tipo de representação da oferta. Os valores possíveis são: `image`, `html` e `text`
   * `Placement Id` e `Activity Id` são identificadores de posicionamento e atividade
   * `Attributes` são atributos específicos da oferta que dependem do tipo de oferta. Exemplo: `deliveryUrl` para imagens

  Para obter mais informações sobre a API de Decisões e representações de Oferta, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  Todas as referências são validadas em relação ao Esquema de Ofertas com um mecanismo de validação descrito em [esta página](../personalization/personalization-build-expressions.md)

  +++Exemplos de referências

   * Local onde a imagem está hospedada:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * URL do Target ao clicar na imagem:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Conteúdo de texto da oferta proveniente do mecanismo de decisão:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * Conteúdo HTML da oferta proveniente do mecanismo de decisão:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Auxiliares {#helpers-all}

Um auxiliar do Handlebars é um identificador simples que pode ser seguido por parâmetros. Cada parâmetro é uma expressão Handlebars. Esses auxiliares podem ser acessados de qualquer contexto em um modelo.

Esses auxiliares de bloco são identificados por um `#` precedendo o nome do auxiliar e exigem um `/` de fechamento correspondente, do mesmo nome.

Blocos são expressões que têm um bloco abrindo (`{{# }}`) e fechando (`{{/}}`).

Para obter mais informações sobre funções auxiliares, consulte [esta seção](functions/helpers.md).

## Tipos literais {#literal-types}

[!DNL Adobe Journey Optimizer] dá suporte aos seguintes tipos literais:

| Literal | Definição |
| ------- | ---------- |
| String | Um tipo de dados composto de caracteres entre aspas duplas. <br>Exemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Um tipo de dados que é verdadeiro ou falso. |
| Número inteiro | Um tipo de dados que representa um número inteiro. Pode ser positivo, negativo ou zero. <br>Exemplos: `-201`, `0`, `412` |
| Matriz | Um tipo de dados que é composto como um grupo de outros valores literais. Ela usa colchetes para agrupar e vírgulas para delimitar entre valores diferentes. <br> **Observação:** não é possível acessar diretamente as propriedades dos itens em uma matriz. <br> Exemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>O uso da variável **xEvent** não está disponível em expressões de personalização. Qualquer referência a xEvent resultará em falhas de validação.

## Práticas recomendadas {#best-practices}

Revise essas regras de sintaxe antes de criar expressões de personalização. A maioria dos erros de tempo de execução vem da combinação de contextos de Handlebars e PQL.

**Usar a sintaxe de bloco condicional correta**

Sempre usar `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`. Não há suporte para a sintaxe `{% if %}` / `{% elseif %}` / `{% endif %}`.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**Não chamar funções PQL dentro de `{{...}}` Handlebars**

`{{...}}` resolve somente variáveis Handlebars e auxiliares — não avalia o PQL. Encurtar uma função PQL como `upperCase()` dentro de `{{...}}` causa um erro &quot;não foi possível encontrar auxiliar&quot;. Em vez disso, use `{%= ... %}`:

| Incorreto | Correto |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**Usar um alias de loop nomeado ao combinar `{{#each}}` com`{%#if%}`**

`this.field` é resolvido pelo renderizador Handlebars, mas não pelo avaliador do PQL dentro de uma condição `{%#if%}`. Defina um alias nomeado com `as |item|` para que ambos os contextos possam resolver o campo:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**Atribuir os resultados da função PQL a uma variável antes do loop**

UDFs do PQL como `topN` não podem ser chamados diretamente dentro de `{{#each}}`. Avalie-as primeiro com `{% let %}` e depois repita sobre o resultado:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**Use `{% let %}` para evitar chamadas de função repetidas**

Quando um valor calculado for necessário mais de uma vez, armazene-o em uma variável. Isso melhora a legibilidade e evita avaliações redundantes:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**Usar a ordem correta de argumentos para`dateDiff`**

`dateDiff(start, end)` toma a data anterior primeiro. Para calcular os dias restantes até uma data futura, passe a data atual como o primeiro argumento:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**Use `=` para comparações de igualdade no PQL, não`==`**

O PQL usa um único operador `=` para igualdade. Usar `==` resulta em um erro de sintaxe.

**Usar acentos graves para nomes de campo hifenizados — somente em expressões PQL**

Se um nome de campo de esquema XDM contiver um hífen (por exemplo, `order-total`), coloque-o entre acentos graves para impedir que o hífen seja analisado como um operador de subtração. Só há suporte para isso dentro de `{%= ... %}` expressões PQL, não em `{{...}}` blocos Handlebars:

```sql
{%= profile.events.`order-total` > 100 %}
```

Para expressões prontas para uso que você pode copiar diretamente para o seu conteúdo, consulte [receitas do Personalization](personalization-recipes.md).

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página explica as sintaxes de personalização do Handlebars e do PQL no Journey Optimizer — suas regras gerais, palavras-chave reservadas, estrutura de namespace, sistema de tipos e práticas recomendadas para evitar erros comuns de tempo de execução.

**Intenções**

* Entenda quando usar a sintaxe Handlebars (`{{...}}`) vs. PQL (`{%= ... %}`)
* Aplicar regras gerais de sintaxe: caracteres reservados, diferenciação entre maiúsculas e minúsculas, escape do HTML, tratamento de barra invertida
* Evitar palavras-chave reservadas e chaves de atributo especiais (nomes hifenizados, IDs de evento numéricas) corretamente
* Aplicar coerção de tipo ao comparar ou transmitir valores de tipos incompatíveis
* Personalização de referência a partir dos namespaces disponíveis: Perfil, Público-alvo, Ofertas
* Seguir as práticas recomendadas para evitar os erros mais comuns de tempo de execução e validação

>[!TAB Glossário]

* **Handlebars**: a `{{...}}` sintaxe de modelo usada para renderizar atributos, looping sobre matrizes e chamar auxiliares de bloco; saída HTML-escapes por padrão. *(específico do produto)*
* **Profile Query Language (PQL)**: a sintaxe de expressão `{%= ... %}` usada para chamar funções internas (por exemplo, `upperCase()`, `formatDate()`) e avaliar expressões condicionais. *(específico do produto)*
* **Traço triplo (`{{{ }}}`)**: uma variante de sintaxe Handlebars que gera valores sem escape do HTML, útil quando o próprio valor contém caracteres HTML que não devem ser codificados.
* **Palavras-chave reservadas**: identificadores PQL (`next`, `last`, `this`) que não podem ser usados diretamente como nomes de campos ou variáveis; devem ser colocados em acentos graves quando um campo de esquema usar um desses nomes.
* **Coerção de tipo**: a conversão explícita de um valor de um tipo de dados para outro (por exemplo, sequência → número) usando funções como `stringToNumber()` ou `toBool()`, necessária antes da comparação ou aritmética no PQL.
* **Namespace**: o agrupamento de nível superior de dados de personalização — Perfil, Público-alvo, Ofertas — cada um com sua própria estrutura de caminho e regras de acesso.
* **Auxiliar de bloco**: um auxiliar Handlebars identificado por `#` antes do nome do auxiliar e um `/` de fechamento correspondente, usado para construções de bloco como `{{#each}}`.

>[!TAB Terminologia]

* **Nome canônico:** Handlebars — da sintaxe `{{...}}`; PQL — da sintaxe `{%= ... %}`
* **Não confunda:** `{{...}}` (Handlebars — renderiza variáveis e auxiliares, HTML-escaped) ≠ `{%= ... %}` (PQL — avalia funções e expressões) ≠ `{%#if%}` / `{%/if%}` (sintaxe de bloco condicional, chaves percentuais)
* **Não confundir:** `{{profile.person.name}}` (stash único — saída com escape de HTML) ≠ `{{{profile.person.name}}}` (stash triplo — saída sem escape)
* **Não confunda:** escape de backtick de palavra-chave reservada (aplica-se a `{{...}}` e `{%= ... %}`) ≠ escape de backtick de chave hifenizada (suportado somente em `{%= ... %}` expressões PQL, não em `{{...}}`)
* **Não confundir:** `=` (operador de igualdade do PQL — correto) ≠ `==` (PQL inválido — causa um erro de sintaxe)

>[!TAB Medidas de proteção e limitações]

* A variável `xEvent` não está disponível em expressões de personalização; qualquer referência a `xEvent` resulta em falhas de validação.
* As chamadas de função PQL dentro de `{{...}}` blocos Handlebars falharão; use `{%= ... %}`.
* A sintaxe condicional `{% if %}` / `{% elseif %}` / `{% endif %}` não tem suporte; use `{%#if%}` / `{%else if%}` / `{%/if%}`.
* O escape de backtick para nomes de campo hifenizados só tem suporte em expressões PQL (`{%= ... %}`). Na interpolação de Handlebars `{{...}}`, a sintaxe de backtick falha — mas nomes de campos hifenizados ainda podem ser referenciados diretamente (por exemplo, `{{profile.my-custom-field}}`).
* As palavras-chave reservadas (`next`, `last`, `this`) devem ser colocadas entre acentos graves quando usadas como nomes de campo de esquema; aplica-se a `{{...}}` e `{%= ... %}`.
* Não há suporte para a barra invertida única `\` como argumento de função literal; use a barra invertida dupla `\\`.
* O PQL é fortemente tipado; tipos incompatíveis em comparações ou aritmética exigem conversão explícita usando `stringToNumber()`, `toBool()` ou funções de coerção semelhantes.

>[!TAB Perguntas frequentes]

**P: Quando devo usar `{{...}}` vs. `{%= ... %}`?**

Use `{{...}}` (Handlebars) para renderizar valores de atributo, executar um loop sobre matrizes e chamar auxiliares de bloco. Use o `{%= ... %}` (PQL) para chamar funções internas como `upperCase()` e `formatDate()` e para avaliar expressões condicionais.

**P: Como saída um valor sem codificação HTML?**

Use o `{{{ }}}` de três stash em vez de `{{...}}`. Saída de HTML-escapes Handlebars de chave única (por exemplo, `&` torna-se `&amp;`); o escape de bypass de três stash.

**P: Qual é o operador de igualdade correto no PQL?**

Use um único `=` para comparações de igualdade no PQL. Usar `==` é um erro de sintaxe.

**P: Como faço referência a um campo de esquema cujo nome é uma palavra-chave reservada (por exemplo, `next`, `last`, `this`)?**

Envolva-o em acentos graves: `{{profile.person.\`next\`.name}`. Isso se aplica a caminhos Handlebars e a expressões PQL.

**P: Posso chamar funções PQL dentro de `{{...}}` Blocos Handlebars?**

Não. `{{...}}` resolve somente variáveis Handlebars e auxiliares. Uma função PQL dentro de `{{...}}` causa um erro &quot;não foi possível encontrar auxiliar&quot;. Em vez disso, use `{%= functionName(...) %}`.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 7fa07aa5 -->
