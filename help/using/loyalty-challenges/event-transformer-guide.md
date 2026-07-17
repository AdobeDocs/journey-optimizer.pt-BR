---
solution: Journey Optimizer
product: journey optimizer
title: Guia do Transformador de eventos
description: Saiba como definir configurações de esquema e transformador para definições de evento de Desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 2015
ht-degree: 1%

---

# Guia do Transformador de eventos {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="Guia do Transformador de eventos"
>abstract="Use este guia para configurar a validação de esquema e as expressões de transformador para as definições de evento de Desafios de Fidelidade."

>[!BEGINSHADEBOX]

**Sumário**

[Introdução aos desafios de fidelidade](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Criar e gerenciar desafios**

* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configurar desafios de fidelidade](loyalty-admin.md)
* [Guia de definição de recompensa](reward-definition-guide.md)
* **Guia do Transformador de Eventos** ◀︎ **Você está aqui**
* [Dados e conjuntos de dados de fidelidade](loyalty-data-and-datasets.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade em [!DNL Journey Optimizer], consulte [ciclo de lançamento](../rn/releases.md).

Para que uma transação de cliente possa ser aplicada a um desafio de fidelidade, ela deve estar no formato **Evento de Fidelidade do Adobe** que o Serviço de Desafio compreenda. Os eventos do cliente — de um sistema de PDV, um aplicativo móvel, uma plataforma de comércio eletrônico ou qualquer outra fonte — normalmente usam o esquema de dados do próprio cliente. **Transformadores de Eventos** fazem a ponte dessa lacuna sem exigir alterações no sistema upstream.

## Visão geral

Uma **Definição de Evento** informa à plataforma duas coisas:

* **Quais eventos declarar** — como reconhecer que um evento de entrada pertence a esta definição (correspondência)
* **Como remodelá-los** — uma expressão [JSONata](https://docs.jsonata.org/overview) que mapeia os campos do cliente para o formato de Evento de Fidelidade (transformação)

É possível configurar várias definições de evento por organização. A plataforma os avalia em ordem e aplica o primeiro que corresponder a. Eventos que não correspondem a nenhuma definição se enquadram na assimilação nativa (consulte [Fallback — Eventos de fidelidade nativa](#fallback--native-loyalty-events)).

## O formato do evento de fidelidade do Adobe

Toda definição de evento deve produzir um objeto JSON no formato a seguir. Essa é a contribuição para os processos do serviço de desafio.

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### Notas de campo

| Campo | Obrigatório | Notas |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **Sim** | Deve conter `id` — a ID de fidelidade do membro. |
| `item_list` | **Sim** | Deve conter pelo menos um item. Um `item_list` vazio faz com que o evento seja rejeitado como inválido. |
| `item_set` | **Sim** (por item) | Os identificadores nessa matriz são os que as listas de inclusão/exclusão de tarefas de desafio comparam. Inclua cada identificador relevante — SKU, categoria de produto, código de departamento, nome do evento — para que os filtros de tarefa funcionem corretamente. |
| `timestamp` | **Sim** | Usado para avaliação da janela de data. Deve ser ISO 8601. |
| `utc_offset` | Recomendado | Obrigatório para correspondência de janelas daypart e para calcular listras de dias consecutivos. Se omitido, a avaliação de daypart e a contagem de dias em sequência são ignoradas. |
| `_id` | Não | Se a detecção de duplicidades estiver habilitada para a organização, o Serviço de Desafio rejeitará um evento cujo `_id` já tenha sido processado. |
| `sub_total` | Não | Usado por tarefas de limite de gastos. Se omitido, o item contribui com gasto zero. |

## Campos de definição de evento

| Campo | Tipo | Obrigatório | Descrição |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | String | Não (atribuído pelo sistema) | Identificador exclusivo atribuído na criação. Somente leitura. |
| `name` | String | **Sim** | Rótulo legível, ex.: `"Starbucks POS Purchase"`. |
| `xdmSchemaId` | String | Não* | A ID do esquema XDM usada para corresponder aos eventos que chegam pela **rota de assimilação DCCS**. A plataforma lê a referência do schema incorporada no evento de entrada e a compara com esse valor. |
| `identifierPath` | String | Não* | O caminho de notação de pontos no JSON de evento usado para corresponder a eventos que chegam por meio da **rota HTTP direta (adobe.io)**. A plataforma lê o valor neste caminho e o verifica em relação a `identifier`. |
| `identifier` | Matriz de cadeias de caracteres | Não | Valores esperados em `identifierPath`. Se fornecido e não estiver vazio, o valor no caminho deve corresponder a um desses valores. Se estiver vazio, qualquer evento com um valor no caminho será correspondido. |
| `schema` | String | Não | Um documento de [Esquema JSON](https://json-schema.org/) (como uma sequência JSON) usado para validar o evento de entrada antes da transformação. Se a validação falhar, o evento será rejeitado com um erro descritivo. |
| `transformer` | String | **Sim** | Expressão JSONata que mapeia o evento de entrada para o formato de Evento de fidelidade do Adobe. |

\* Pelo menos um de `xdmSchemaId` ou `identifierPath` deve ser fornecido.

## Como a correspondência funciona

A estratégia correspondente depende de como o evento atinge a plataforma:

**Rota de assimilação de DCCS** — Os eventos que chegam pelo Serviço Principal de Coleta de Dados (DCCS) carregam uma referência de esquema XDM em seu envelope. A plataforma lê a ID do esquema de `/body/xdmMeta/schemaRef/id` e a compara com o `xdmSchemaId` de cada definição. Configurar `xdmSchemaId` nas definições destinadas a esta rota.

**Rota HTTP direta (adobe.io)** — Eventos postados diretamente na plataforma por meio da API adobe.io não trazem uma referência de esquema XDM. A plataforma, em vez disso, atravessa o JSON do evento usando `identifierPath` e verifica o valor encontrado lá:
* Se `identifier` não estiver vazio: o valor deve corresponder a uma das cadeias de caracteres configuradas.
* Se `identifier` estiver vazio: qualquer evento com um valor não nulo no caminho será correspondido.

Configurar `identifierPath` (e, opcionalmente, `identifier`) nas definições destinadas a esta rota.

A plataforma percorre as definições de evento da organização **em ordem** e aplica a primeira correspondência. Quando uma correspondência é encontrada, o corpo `xdmEntity` (para eventos DCCS) ou o corpo completo do evento (para eventos HTTP diretos) é passado para o transformador.

## Gravação do transformador

O campo `transformer` é uma expressão [JSONata](https://docs.jsonata.org/overview). Ele recebe o evento de entrada JSON como sua entrada e deve retornar um objeto Adobe Loyalty Event válido.

+++Padrão básico de mapeamento

Mapeie cada campo de nível superior do formato de destino para o caminho correspondente no evento de origem:

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++Codificação do nome do evento

Se todos os eventos correspondentes a esta definição representarem a mesma atividade lógica, codifique a `event_name`:

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name` é usado para métricas internas e relatórios. Ela não é usada como um filtro de tarefa — a qualificação da tarefa é determinada pelo conteúdo `item_set`, não pelo nome do evento.

+++

+++Identidade de mapeamento para eventos DCCS/XDM

Para eventos que chegam por meio da rota DCCS, a identidade do membro normalmente é transportada no campo XDM padrão `identityMap` em vez de uma propriedade de locatário personalizada. `identityMap` é um mapa digitado por namespace — a chave em si é o nome do namespace, e o valor é uma matriz de objetos de identidade.

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **Substituição de namespace:** Substitua `Email` pelo namespace que sua organização usar para membros do programa de fidelidade — `Loyalty`, `ECID`, `CRMID` etc. Sempre ler a partir do namespace que contém a identidade principal do perfil de fidelidade.

* **Sempre usar `[0]`:** `identityMap.Email` é uma matriz. Sem o índice, JSONata retornará uma sequência em vez de um único valor se mais de uma identidade estiver presente, e `loyalty_identity.id` se tornará uma lista. Fixe-o ao primeiro elemento com `[0]`.

* **Evite campos de locatário personalizados para a identidade:** Os grupos de campos personalizados às vezes expõem um campo com aparência de email (por exemplo, `_yourtenant.identification.core.email`). Nos dados de amostra, retorna um valor e parece correto, mas nos eventos de produção, geralmente está vazio. A fonte confiável de identidade é sempre `identityMap`.

+++

+++Compilando `item_set`

`item_set` é uma matriz de identificadores de sequência. Inclua todos os campos que suas tarefas de desafio possam filtrar:

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

Para eventos não transacionais (um check-in, uma conclusão de pesquisa, um acionador personalizado), um único identificador é suficiente:

```jsonata
"item_set": [eventName]
```

+++

+++Mapeando `unit_price`

`unit_price` deve ser um preço por unidade. Alguns esquemas de origem armazenam um total de linha (preço × quantidade) em vez disso. Se o campo de origem for um total de linha, divida por quantidade para obter o preço unitário:

```jsonata
"unit_price": priceTotal / quantity
```

> Dividir somente se o campo de origem for um total de linha. Se já armazenar um preço por unidade, mapeie-o diretamente — dividir um preço por quantidade produzirá silenciosamente um valor errado.

+++

+++Derivando `transaction_id`

Se o evento de origem não incluir um identificador de transação, você poderá derivar um estável a partir do carimbo de data e hora:

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

Isso converte o carimbo de data e hora ISO em milissegundos da época e produz um valor determinístico para um determinado evento. Use a função de geração de ID da própria plataforma, se disponível.

+++

+++Uso de funções JSONata

A biblioteca completa da função JSONata está disponível. Exemplos úteis:

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## Exemplos

+++Exemplo 1 — Evento personalizado simples (não transacional)

**Cenário:** um aplicativo móvel envia um evento de check-in. Não há itens de linha — o evento em si é a atividade qualificada.

**Evento de Entrada:**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definição de Evento:**

```json
{
  "name":           "Mobile Store Check-In",
  "identifierPath": "eventName",
  "identifier":     ["store-checkin"],
  "transformer":    "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**Transformador Formatado (para legibilidade):**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**Evento de fidelidade de saída do Adobe:**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

Uma tarefa de desafio sem restrições de inclusão/exclusão contará este evento como uma visita qualificada — a única `item_set` entrada `["store-checkin"]` corresponde a qualquer tarefa que permita todos os itens.

+++

+++Exemplo 2 — Compra de PDV com Itens de Linha

**Cenário:** um sistema de ponto de venda envia uma carga de transação. Cada item de linha tem um SKU e pertence a uma categoria. As tarefas de desafio usam SKU e categoria para determinar o que se qualifica.

**Evento de Entrada:**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definição de Evento:**

```json
{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**Transformador Formatado:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**Evento de fidelidade de saída do Adobe:**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

Uma tarefa de desafio com `include: ["BEVERAGE"]` veria o item de linha de café se qualificar (seu `item_set` contém `"BEVERAGE"`) e acumular US$ 9,00 de gastos com essa tarefa. O item de linha muffin seria excluído.

+++

+++Exemplo 3 — Evento de experiência do AEP (correspondência de esquema XDM)

**Cenário:** Os eventos fluem pelo Adobe Journey Optimizer. O evento de entrada é um Evento de experiência XDM com uma ID de esquema conhecida. A plataforma usa a ID do esquema para correspondência em vez de uma verificação de caminho/valor.

**Corpo da Entidade XDM de Entrada** (o `xdmEntity` extraído do evento AJO):

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**Definição de Evento:**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**Transformador Formatado:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **Observação:** quando um evento corresponde pela ID de esquema XDM, o transformador recebe apenas a parte `xdmEntity` do evento, não o envelope externo do AJO. Todos os caminhos na expressão do transformador são relativos ao corpo da entidade XDM.

+++

## Adicionar validação do esquema JSON (opcional)

Se você quiser que a plataforma valide a estrutura de eventos de entrada antes de tentar a transformação, defina o campo `schema` como um documento de [Esquema JSON](https://json-schema.org/draft-04) codificado como uma sequência de caracteres JSON.

Eventos que falham na validação do esquema são rejeitados antes da execução da transformação. A resposta do erro inclui a falha de validação específica, facilitando o diagnóstico de eventos upstream malformados.

+++Exemplo de esquema (para o Exemplo 2 acima)

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

Transmita este esquema como uma cadeia de caracteres JSON minificada no campo `schema` da definição do evento.

## Fallback — Eventos nativos de fidelidade

Se nenhuma definição de evento corresponder a um evento recebido, a plataforma tentará assimilá-lo diretamente como um Evento de fidelidade do Adobe nativo. Se a carga já estiver em conformidade com o formato de Evento de fidelidade descrito acima, nenhum transformador será necessário e o evento será aplicado como está. Isso permite que os clientes que pré-formataram seus eventos ignorem a transformação completamente.

## Referência da API

Todas as operações de definição de evento usam o caminho base `/loyalty/metadata/config/events`.

+++Criar uma definição de evento

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{ ... }"
}
```

+++

+++Definições de Evento de Lista

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++Atualizar uma definição de evento

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++Excluir uma definição de evento

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## Validação do transformador

As expressões JSONata são validadas para sintaxe quando a definição do evento é salva. Se a expressão for inválida, a API retornará um erro `422` com uma descrição da falha de análise.

Para testar um transformador antes de implantar, use o [JSONata Exerciser](https://try.jsonata.org/) — cole o evento de origem como a entrada e a expressão do transformador para verificar se a saída corresponde ao formato de Evento de fidelidade esperado.

## Armadilhas comuns

Todos esses erros são executados sem erro em uma carga de teste de item único simples, que é exatamente o motivo pelo qual eles são ignorados. Sempre teste seu transformador em relação a uma carga com dois ou mais produtos antes da implantação.

+++Criação de um objeto em vez de mapeamento sobre a matriz

O erro mais frequente. O uso de um único objeto literal com `productListItems.SKU` puxa cada SKU e cada quantidade em sequências agrupadas, em vez de produzir um item de linha por produto.

**✗Recolhe todos os itens em um:**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

Com dois produtos, `item_set` contém SKUs e `quantity` torna-se uma matriz, como `[1, 4]`.

**✓Um item de linha por produto:**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

O mapa `.{ }` é executado uma vez por produto para que cada um se torne sua própria entrada.

+++

+++Esquecendo o índice de matriz na identidade

`identityMap.Email` é uma matriz. Sem `[0]`, se um perfil tiver mais de uma identidade nesse namespace, `id` se tornará uma lista de valores em vez de uma única cadeia de caracteres.

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++Identidade de origem de um campo de locatário personalizado

Os grupos de campos personalizados às vezes expõem um campo com aparência de email, como `_yourtenant.identification.core.email`. Nos dados de amostra, ele retorna um valor e parece correto, mas nos eventos de produção é frequentemente vazio, fazendo com que `loyalty_identity.id` seja nulo. Sempre use `identityMap` como a fonte da identidade.

+++

+++Uma matriz aninhada vazando para `item_set`

A adição de um campo de categoria a `item_set` parece simples, mas se `productCategories` for ela mesma uma matriz, o resultado se expande imprevisivelmente.

**✗Pode produzir mais entradas do que o esperado:**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

Um produto com três categorias produz um `item_set` com quatro valores.

**✓Indexe a matriz aninhada para obter exatamente um valor:**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list` está vazio ou ausente

Um evento com um `item_list` vazio ou ausente é rejeitado como inválido. Para eventos não transacionais (check-ins, acionadores personalizados), não há itens de linha naturais, portanto, produza um sintético:

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp` como um inteiro da época Unix em vez de ISO 8601

A plataforma espera uma sequência de caracteres ISO 8601. Se o evento de origem levar milissegundos desde a época, converta-o:

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++`utc_offset` omitido

Sem `utc_offset`, a correspondência da janela daypart e a contagem de sequências de dias consecutivos são ignoradas. Mapeie o armazenamento ou o deslocamento UTC do dispositivo do evento de origem, onde quer que ele esteja disponível.

+++

+++Caminhos do transformador relativos ao envelope do AJO em um evento DCCS

Para eventos DCCS, o transformador recebe apenas o corpo `xdmEntity`, não o envelope externo do AJO. Todos os caminhos devem ser relativos à raiz da entidade XDM. Se sua expressão referenciar campos que residem no envelope externo (por exemplo, `/body/xdmMeta/...`), eles não serão encontrados e produzirão silenciosamente um valor nulo.

+++
