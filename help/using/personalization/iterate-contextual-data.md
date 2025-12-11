---
solution: Journey Optimizer
product: journey optimizer
title: Iterar em dados contextuais
description: Saiba como iterar matrizes de várias fontes de contexto usando a sintaxe Handlebars
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: expressão, editor, handlebars, iteração, matrizes, contexto, personalização
source-git-commit: a67707e50960e4848197fa1bd39ce95af3ef14ab
workflow-type: tm+mt
source-wordcount: '2484'
ht-degree: 3%

---

# Iterar em dados contextuais {#personalization-contexts}

Saiba como usar a sintaxe de iteração do Handlebars para exibir listas dinâmicas de dados de várias fontes em suas mensagens, incluindo eventos, respostas de ação personalizadas e outros dados contextuais.

## Visão geral {#overview}

O Journey Optimizer fornece acesso a dados contextuais de várias fontes durante a [personalização da mensagem](personalize.md). Você pode iterar matrizes dessas fontes usando a sintaxe Handlebars em canais nativos ([email](../email/get-started-email-design.md), [push](../push/create-push.md), [SMS](../sms/create-sms.md)) para exibir conteúdo dinâmico como listas de produtos, recomendações ou outros elementos repetitivos.

**Fontes de contexto disponíveis:**

* **[Eventos](#event-data)**: dados de eventos de jornada (eventos comerciais, eventos unitários)
* **[Respostas da ação personalizada](#custom-action-responses)**: dados retornados de chamadas de API externas por meio de ações personalizadas
* **[Pesquisa de conjunto de dados](#dataset-lookup)**: dados enriquecidos recuperados de conjuntos de dados do Adobe Experience Platform
* **[Propriedades técnicas](#technical-properties)**: metadados de Jornada, como ID de jornada e identificadores complementares
* **[Contexto de Jornada](#other-contexts)**: outros dados relacionados à jornada acessíveis durante a execução

Este guia mostra como iterar sobre matrizes de cada uma dessas fontes em suas mensagens e como trabalhar com matrizes ao configurar atividades de jornada. Comece com [Sintaxe de iteração Handlebars](#syntax) para entender as noções básicas de personalização de mensagens ou vá para [Trabalhe com matrizes em expressões de Jornada](#arrays-in-journeys) para saber como transmitir dados de matriz para ações personalizadas e pesquisas de conjuntos de dados.

## Sintaxe de iteração de Handlebars {#syntax}

Handlebars fornece o `{{#each}}` [auxiliar](functions/helpers.md) para iterar sobre matrizes. A sintaxe básica é:

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Pontos principais:**

* Substituir `arrayPath` pelo caminho para os dados da matriz
* Substitua `item` com qualquer nome de variável que você preferir (por exemplo, `product`, `response`, `element`)
* Acessar propriedades de cada item usando `{{item.propertyName}}`
* Você pode aninhar vários blocos `{{#each}}` para matrizes de vários níveis

## Iterar dados do evento {#event-data}

Os dados do evento estão disponíveis quando a sua jornada é acionada por um [evento](../event/about-events.md). Isso é útil para exibir dados capturados no momento em que a jornada foi iniciada, como conteúdo do carrinho, itens de pedido ou envios de formulário.

>[!TIP]
>
>Você pode combinar dados do evento com outras fontes. Consulte [Combinar várias fontes de contexto](#combine-sources) para obter exemplos.

### Caminho de contexto para eventos

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: o identificador exclusivo do evento conforme configurado na jornada
* `<fieldPath>`: O caminho para o campo ou matriz no esquema de evento

### Exemplo: itens do carrinho de um evento

Se o [esquema de eventos](../event/experience-event-schema.md) incluir uma matriz `productListItems` (formato [XDM padrão](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}), você poderá exibir o conteúdo do carrinho da seguinte maneira:

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

### Exemplo: matrizes aninhadas em eventos

Para estruturas aninhadas, use `{{#each}}` blocos aninhados. Saiba mais sobre o aninhamento em [Práticas recomendadas](#best-practices).

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

## Iterar sobre respostas de ação personalizadas {#custom-action-responses}

[As respostas de ação personalizada](../action/about-custom-action-configuration.md) contêm dados retornados de chamadas de API externas. Isso é útil para exibir informações em tempo real de seus sistemas, como pontos de fidelidade, recomendações de produtos, status do inventário ou ofertas personalizadas.

>[!NOTE]
>
>As ações personalizadas devem ser configuradas com uma carga de resposta para usar esse recurso. Saiba mais em [esta seção](../action/action-response.md#config-response). Você também pode combinar respostas de ação personalizadas com dados de evento ou pesquisas de conjunto de dados. Consulte [Combinar várias fontes de contexto](#combine-sources) para obter exemplos.

### Caminho de contexto para ações personalizadas

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: O nome da sua [ação personalizada](../action/about-custom-action-configuration.md) conforme configurado na jornada
* `<fieldPath>`: O caminho para o campo ou matriz na carga de resposta

### Exemplo: recomendações de produto de uma API

Se sua ação personalizada retornar recomendações de produto:

**Resposta da API:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**Personalização da mensagem:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

### Exemplo: matrizes aninhadas de ações personalizadas

Se sua ação personalizada retornar matrizes aninhadas (por exemplo, categorias com produtos). Para obter padrões de aninhamento mais complexos, consulte [Práticas recomendadas](#best-practices).

**Resposta da API:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**Personalização da mensagem:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

### Exemplo: benefícios do nível de fidelidade

Exibir benefícios dinâmicos com base no status de fidelidade:

**Resposta da API:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**Personalização da mensagem:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

## Repetir nos resultados da pesquisa do conjunto de dados {#dataset-lookup}

A [Atividade de Pesquisa de Conjunto de Dados](../building-journeys/dataset-lookup.md) permite recuperar dados de [conjuntos de dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=pt-BR){target="_blank"} durante o tempo de execução da jornada. Os dados enriquecidos são armazenados como uma matriz e podem ser repetidos em suas mensagens.

>[!AVAILABILITY]
>
>A atividade Pesquisa de conjunto de dados só está disponível para um conjunto limitado de organizações. Para obter acesso, entre em contato com o representante da Adobe.

Saiba mais sobre como configurar a atividade Pesquisa de Conjunto de Dados em [esta seção](../building-journeys/dataset-lookup.md). A pesquisa de conjunto de dados é particularmente eficiente quando combinada com dados de evento. Consulte [Exemplo: dados de evento enriquecidos com a pesquisa de conjunto de dados](#combine-sources) para obter um caso de uso prático.

### Caminho de contexto para pesquisas de conjunto de dados

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: o identificador exclusivo da sua atividade de Pesquisa de Conjunto de Dados
* `entities`: A matriz de dados enriquecidos recuperados do conjunto de dados

### Exemplo: detalhes do produto de um conjunto de dados

Se você estiver usando uma atividade de Pesquisa de conjunto de dados para recuperar informações do produto com base em SKUs:

**Configuração de Pesquisa de Conjunto de Dados:**

* Chaves de Pesquisa: `list(@event{purchase_event.products.sku})`
* Campos a Serem Retornados: `["SKU", "category", "price", "name"]`

**Personalização da mensagem:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

### Exemplo: iteração filtrada com dados do conjunto de dados

Exibir somente produtos de uma categoria específica. Saiba mais sobre a filtragem condicional em [Práticas recomendadas](#best-practices).

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

### Exemplo: Calcular totais a partir da pesquisa do conjunto de dados

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

## Usar propriedades técnicas do jornada {#technical-properties}

As propriedades técnicas do Jornada fornecem acesso aos metadados sobre a execução da jornada, como a ID da jornada e os identificadores complementares. Eles podem ser úteis quando combinados com padrões de iteração, especialmente para filtrar matrizes com base em instâncias de jornada específicas.

### Propriedades técnicas disponíveis

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Exemplo: filtrar itens de matriz usando o identificador complementar

Ao usar identificadores complementares em jornadas acionadas por eventos com matrizes, você pode filtrar para mostrar somente o item relevante para a instância de jornada atual. Saiba mais sobre identificadores complementares em [este guia](../building-journeys/supplemental-identifier.md).

**Cenário**: uma jornada é acionada com várias reservas, mas você deseja exibir informações somente para a reserva específica (identificada pela ID complementar) que acionou essa instância de jornada.

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

### Exemplo: incluir ID da jornada para rastreamento

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

## Combinar várias fontes de contexto {#combine-sources}

Você pode combinar dados de diferentes fontes na mesma mensagem para criar experiências ricas e personalizadas. Esta seção mostra exemplos práticos de uso de várias fontes de contexto juntas.

**Fontes de contexto que você pode combinar:**

* [Dados do evento](#event-data) + [Respostas da ação personalizada](#custom-action-responses)
* [Dados do evento](#event-data) + [Pesquisa de conjunto de dados](#dataset-lookup)
* [Várias fontes](#combine-sources) + [Propriedades técnicas](#technical-properties)

### Exemplo: itens do carrinho com inventário em tempo real

Combinar dados do evento (conteúdo do carrinho) com dados de ação personalizados (status do inventário):

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

### Exemplo: dados de evento enriquecidos com pesquisa de conjunto de dados

Combine [SKUs de evento](#event-data) com informações detalhadas do produto de uma [pesquisa de conjunto de dados](#dataset-lookup):

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

### Exemplo: combinar várias fontes com propriedades técnicas

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

## Outros tipos de contexto {#other-contexts}

Embora este guia se concentre na iteração sobre matrizes, outros tipos de contexto estão disponíveis para personalização que normalmente não exigem iteração. Elas são acessadas diretamente em vez de serem colocadas em loop:

* **[Atributos do perfil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}** (`profile.*`): campos de perfil individuais do Adobe Experience Platform
* **[Públicos-alvo](../audience/about-audiences.md)** (`inAudience()`): verificações de associação de público-alvo
* **[Decisões de oferta](../offers/get-started/starting-offer-decisioning.md)**: ofertas de gerenciamento de decisão
* **[Atributos do público-alvo](../orchestrated/activities/channels.md#add-personalization)** (somente campanhas orquestradas): atributos calculados na tela da campanha
* **Token** (`context.token`): tokens de sessão ou autenticação

Para obter a sintaxe de personalização completa e exemplos usando essas fontes, consulte:

* [Adicionar personalização](personalization-build-expressions.md)
* [Sintaxe de personalização](personalization-syntax.md)

## Trabalhar com matrizes em expressões de Jornada {#arrays-in-journeys}

Embora as seções anteriores se concentrem em iterar sobre matrizes na personalização de mensagens usando Handlebars, você também trabalha com matrizes ao configurar atividades de jornada. Esta seção explica como usar dados de matriz de eventos em expressões de Jornada, especialmente ao transmitir dados para ações personalizadas ou usar matrizes com pesquisas de conjunto de dados.

>[!IMPORTANT]
>
>As expressões de jornada usam uma sintaxe diferente da personalização Handlebars. Na configuração da jornada (como parâmetros ou condições de ação personalizada), use o [editor de expressão de Jornada](../building-journeys/expression/expressionadvanced.md) com funções como `first`, `all` e `serializeList`. No conteúdo da mensagem, você usa a sintaxe Handlebars com `{{#each}}` loops.

### Envio de valores de matriz para parâmetros de ação personalizados {#arrays-to-custom-actions}

Ao configurar [ações personalizadas](../action/about-custom-action-configuration.md), geralmente é necessário extrair valores de matrizes de eventos e passá-los como parâmetros. Esta seção aborda padrões comuns.

Saiba mais sobre como transmitir coleções em [Transmitir coleções para parâmetros de ação personalizados](../building-journeys/collections.md#passing-collection).

#### Extrair um valor único de uma matriz

**Caso de uso**: obtenha um campo específico de uma matriz de eventos para passar como parâmetro de consulta em uma solicitação GET.

**Exemplo de cenário**: extraia o primeiro SKU com um preço maior que 0 de uma lista de produtos.

**Exemplo de esquema de evento**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**Configuração de ação personalizada**:

1. Em sua ação personalizada, configure um parâmetro de consulta (por exemplo, `sku`) com tipo `string`
2. Marcar como `Variable` para permitir valores dinâmicos

**Expressão de Jornada no parâmetro de ação**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Explicação**:

* `@event{YourEventName}`: Referencia seu evento de jornada
* `.first(currentEventField.condition)`: retorna o primeiro item de matriz correspondente à condição
* `currentEventField`: representa cada item na matriz de eventos à medida que você a percorre
* `.SKU`: extrai o campo SKU do item correspondente
* Resultado: `"SKU-1"` (uma cadeia de caracteres adequada ao parâmetro de ação)

Saiba mais sobre a função `first` em [Funções de gerenciamento de coleção](../building-journeys/expression/collection-management-functions.md).

#### Criar uma lista de valores de uma matriz

**Caso de uso**: crie uma lista separada por vírgulas de IDs a serem transmitidas como um parâmetro de consulta (por exemplo, `/products?ids=sku1,sku2,sku3`).

**Configuração de ação personalizada**:

1. Configurar um parâmetro de consulta (por exemplo, `ids`) com tipo `string`
2. Marcar como `Variable`

**Expressão de Jornada**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Explicação**:

* `.all(currentEventField.condition)`: retorna todos os itens de matriz correspondentes à condição (retorna uma lista)
* `currentEventField`: representa cada item na matriz de eventos à medida que você a percorre
* `.SKU`: Projeta a lista para incluir apenas valores de SKU
* `serializeList(list, delimiter, addQuotes)`: Ingressa a lista em uma cadeia de caracteres
   * `","`: usar vírgula como delimitador
   * `true`: adicionar aspas em cada elemento da cadeia de caracteres
* Resultado: `"SKU-1,SKU-3"` (adequado para um parâmetro de consulta)

Saiba mais sobre:

* [`all`](../building-journeys/expression/collection-management-functions.md)
* [`serializeList`](../building-journeys/functions/list-functions.md#serializeList)

O manuseio de coleção para ações personalizadas é abordado em [Transmitir coleções para parâmetros de ação personalizados](../building-journeys/collections.md#passing-collection).

#### Passar uma matriz de objetos para uma ação personalizada

**Caso de uso**: enviar uma matriz completa de objetos em um corpo de solicitação (para POST ou GET com corpo).

**Solicitar exemplo de corpo**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**Configuração de ação personalizada**:

1. No corpo da solicitação, defina `products` como tipo `listObject`
2. Marcar como `Variable`
3. Definir os campos de objeto: `id`, `name`, `price`, `color` (cada um se torna mapeável)

**Configuração da tela de Jornada**:

1. No modo Avançado, defina a expressão de coleção:

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. Na interface de mapeamento de coleção:
   * Mapa `id` → `productListItems.SKU`
   * Mapa `name` → `productListItems.name`
   * Mapa `price` → `productListItems.priceTotal`
   * Mapa `color` → `productListItems.color`

O Journey Optimizer constrói a matriz de objetos que correspondem à estrutura de carga da ação.

>[!NOTE]
>
>Ao trabalhar com matrizes de eventos, use `currentEventField` para fazer referência a cada item. Para coleções de fonte de dados (Adobe Experience Platform), use `currentDataPackField`. Para coleções de resposta de ação personalizada, use `currentActionField`.

Saiba mais em [Transmitir coleções para parâmetros de ação personalizados](../building-journeys/collections.md#passing-collection).

### Usar matrizes com pesquisas de conjunto de dados {#arrays-with-dataset-lookup}

Ao usar a [atividade de Pesquisa de Conjunto de Dados](../building-journeys/dataset-lookup.md), você pode passar uma matriz de valores como chaves de pesquisa para recuperar dados enriquecidos.

**Exemplo**: pesquisar detalhes do produto para todas as SKUs em uma matriz de eventos.

**Configuração de Pesquisa do Conjunto de Dados**:

No campo de chaves de pesquisa, use `list()` para converter um caminho de matriz em uma lista:

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Isso cria uma lista de todos os valores de SKU a serem pesquisados no conjunto de dados. Os resultados estão disponíveis como uma matriz em `context.journey.datasetLookup.<activityID>.entities` que você pode iterar na sua mensagem (consulte [Iterar nos resultados da pesquisa do conjunto de dados](#dataset-lookup)).

### Limitações e padrões {#array-limitations}

Esteja ciente destas limitações ao trabalhar com arrays no jornada:

#### Nenhum loop dinâmico em arrays no fluxo de jornada

O Jornada não pode criar loops dinâmicos em que um nó de ação é executado várias vezes para cada item em uma matriz. Isso é intencional para evitar problemas de desempenho descontrolados.

**O que você não pode fazer**:

* Executar uma ação personalizada uma vez por item do array dinamicamente
* Criar várias ramificações de jornada com base no comprimento da matriz

**Padrões recomendados**:

1. **Enviar todos os itens de uma só vez**: passar toda a matriz ou uma lista serializada para uma única ação personalizada que processa todos os itens. Consulte [Criar uma lista de valores de uma matriz](#arrays-to-custom-actions).

2. **Usar agregação externa**: faça com que sua API externa aceite várias IDs e retorne resultados combinados em uma única chamada.

3. **Pré-calcular no AEP**: use [atributos computados](../audience/computed-attributes.md) para pré-calcular valores de matrizes no nível do perfil.

4. **Extração de valor único**: se você precisar de apenas um valor, extraia-o usando `first` ou `head`. Consulte [Extrair um único valor de uma matriz](#arrays-to-custom-actions).

Saiba mais em [Medidas de proteção e limitações](../start/guardrails.md).

#### Considerações sobre o tamanho da matriz

Arrays grandes podem afetar o desempenho da jornada:

* **Matrizes de eventos**: manter cargas de evento abaixo do total de 50 KB
* **Respostas da ação personalizada**: as cargas de resposta devem ter menos de 100KB
* **Resultados da pesquisa do conjunto de dados**: Limitar o número de chaves de pesquisa e entidades retornadas

### Exemplo completo: matriz de eventos para ação personalizada {#complete-example}

Este é um fluxo de trabalho completo que mostra como usar uma matriz de eventos com uma ação personalizada.

**Cenário**: quando um usuário abandona o carrinho, envie os dados do carrinho para uma API de recomendação externa para obter sugestões personalizadas e, em seguida, as exiba em um email.

**Etapa 1: configurar a ação personalizada**

Crie uma ação personalizada &quot;GetCartRecommendations&quot;:

* **Método**: POST
* **URL**: `https://api.example.com/recommendations`
* **Corpo da solicitação**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* Marcar `cartItems` como tipo `listObject` e `Variable`
* Definir campos: `sku` (cadeia de caracteres), `price` (número), `quantity` (inteiro)

Saiba mais em [Configurar uma ação personalizada](../action/about-custom-action-configuration.md).

**Etapa 2: configurar carga de resposta**

Na ação personalizada, configure a resposta:

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

Saiba mais em [Usar respostas de chamada de API](../action/action-response.md).

**Etapa 3: conectar a ação na jornada**

1. Após o evento de abandono do carrinho, adicione a ação personalizada
1. No modo Avançado para a coleção `cartItems`:

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. Mapeie os campos da coleção:
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Etapa 4: usar a resposta no seu email**

No conteúdo do email, repita as recomendações:

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Etapa 5: testar sua configuração**

Antes de executar uma jornada em tempo real, teste a ação personalizada usando o recurso &quot;Enviar solicitação de teste&quot; na configuração da ação para verificar a solicitação e os valores criados.

1. Usar [modo de teste de jornada](../building-journeys/testing-the-journey.md)
2. Acionar com dados de evento de exemplo, incluindo uma matriz `productListItems`
3. Verifique se a ação personalizada recebe a estrutura de matriz correta
4. Verificar os [logs de teste de ação](../action/action-response.md#test-mode-logs)
5. Visualize o e-mail para confirmar se os dois storages são exibidos corretamente

Saiba mais em [Solucionar problemas de ações personalizadas](../action/troubleshoot-custom-action.md).

## Práticas recomendadas {#best-practices}

Siga essas práticas recomendadas ao iterar em dados contextuais para criar personalização executável e que possa ser mantida.

### Usar nomes de variáveis descritivas

Escolha nomes de variáveis que indiquem claramente sobre o que você está iterando. Isso torna o código mais legível e fácil de manter. Saiba mais sobre a [sintaxe de personalização](personalization-syntax.md):

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

### Lidar com matrizes vazias

Use a cláusula `{{else}}` para fornecer conteúdo de fallback quando uma matriz estiver vazia. Saiba mais sobre [funções auxiliares](functions/helpers.md):

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

### Combinar com auxiliares condicionais

Use `{{#if}}` em loops para conteúdo condicional. Saiba mais sobre [regras condicionais](create-conditions.md) e veja exemplos nas seções [Respostas de ação personalizadas](#custom-action-responses) e [Pesquisa de conjunto de dados](#dataset-lookup).

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

### Limitar iteração para desempenho

Para matrizes grandes, considere limitar o número de iterações:

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

### Acessar metadados da matriz

Handlebars fornecem variáveis especiais em loops que ajudam nos padrões avançados de iteração:

* `@index`: Índice de iteração atual (baseado em 0)
* `@first`: verdadeiro para a primeira iteração
* `@last`: verdadeiro para a última iteração

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

>[!NOTE]
>
>Essas variáveis Handlebars (`@index`, `@first`, `@last`) só estão disponíveis nos loops `{{#each}}` de personalização de mensagens. Para trabalhar com matrizes em expressões de Jornada (como obter o primeiro item de uma matriz antes de passar para uma ação personalizada), use funções de matriz como [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) ou [`all`](../building-journeys/expression/collection-management-functions.md). Consulte [Trabalhar com matrizes em expressões de Jornada](#arrays-in-journeys) para obter mais detalhes.

## Solução de problemas {#troubleshooting}

Problemas com a iteração? Esta seção aborda problemas e soluções comuns.

### Matriz não exibida

**Problema**: sua iteração de matriz não está mostrando conteúdo.

**Possíveis causas e soluções**:

1. **Caminho incorreto**: verifique o caminho exato para a matriz com base na fonte do contexto:
   * Para [eventos](#event-data): `context.journey.events.<event_ID>.<fieldPath>`
   * Para [ações personalizadas](#custom-action-responses): `context.journey.actions.<actionName>.<fieldPath>`
   * Para [pesquisas do conjunto de dados](#dataset-lookup): `context.journey.datasetLookup.<activityID>.entities`

2. **A matriz está vazia**: adicione uma cláusula `{{else}}` para verificar se a matriz não tem dados. Consulte [Práticas recomendadas](#best-practices) para ver exemplos.

3. **Dados ainda não disponíveis**: verifique se a ação personalizada, o evento ou a atividade de pesquisa do conjunto de dados foi executada antes da atividade de mensagem no fluxo de jornada.

### Erros de sintaxe

**Problema**: falha na validação da expressão ou a mensagem não é renderizada.

**Erros comuns**:

* Marcas de fechamento ausentes: todo `{{#each}}` deve ter um `{{/each}}`. Revise a [sintaxe de iteração de Handlebars](#syntax) para obter a estrutura adequada.
* Nome de variável incorreto: garanta o uso consistente do nome da variável em todo o bloco. Consulte [Práticas recomendadas](#best-practices) para convenções de nomenclatura.
* Separadores de caminho incorretos: use pontos (`.`), não barras ou outros caracteres

### Teste das iterações

Use o [modo de teste de jornada](../building-journeys/testing-the-journey.md) para verificar suas iterações. Isso é especialmente importante ao usar [ações personalizadas](#custom-action-responses) ou [pesquisas de conjunto de dados](#dataset-lookup):

1. Inicie sua jornada no [modo de teste](../building-journeys/testing-the-journey.md)
2. Acionar o evento ou a ação personalizada com dados de amostra
3. Verifique a [visualização da mensagem](../content-management/preview.md) para verificar se a iteração é exibida corretamente
4. Revise os logs do modo de teste para quaisquer erros (consulte [Logs do modo de teste de ação personalizada](../action/action-response.md#test-mode-logs))

## Tópicos relacionados {#related-topics}

**Fundamentos do Personalization:**

* [Introdução à personalização](personalize.md)
* [Adicionar personalização](personalization-build-expressions.md)
* [Sintaxe de personalização](personalization-syntax.md)
* [Funções de ajuda](functions/helpers.md)
* [Criar regras condicionais](create-conditions.md)

**Configuração de Jornada:**

* [Sobre eventos](../event/about-events.md)
* [Configurar ações personalizadas](../action/about-custom-action-configuration.md)
* [Passar coleções para parâmetros de ação personalizada](../building-journeys/collections.md#passing-collection)
* [Usar as respostas de chamada da API em ações personalizadas](../action/action-response.md)
* [Solucionar problemas de ações personalizadas](../action/troubleshoot-custom-action.md)
* [Usar dados do Adobe Experience Platform no jornada](../building-journeys/dataset-lookup.md)
* [Usar identificadores complementares em jornadas](../building-journeys/supplemental-identifier.md)
* [Medidas de proteção e limitações](../start/guardrails.md)
* [Teste a jornada](../building-journeys/testing-the-journey.md)

**Funções de expressão de Jornada:**

* [Editor de expressão avançado](../building-journeys/expression/expressionadvanced.md)
* [Funções de gerenciamento de coleção](../building-journeys/expression/collection-management-functions.md) (primeiro, todos, último)
* [Listar funções](../building-journeys/functions/list-functions.md) (serializeList, filtro, classificação)
* [Funções de matriz](../personalization/functions/arrays-list.md) (head, tail)

**Casos de uso do Personalization:**

* [Email de abandono do carrinho](personalization-use-case-helper-functions.md)
* [Notificação do status do pedido](personalization-use-case.md)

**Design da mensagem:**

* [Introdução ao design de email](../email/get-started-email-design.md)
* [Criar notificações por push](../push/create-push.md)
* [Criar mensagens SMS](../sms/create-sms.md)
* [Visualizar e testar o conteúdo](../content-management/preview-test.md)

