---
solution: Journey Optimizer
product: journey optimizer
title: Guia de definição de recompensa
description: Saiba como configurar definições de recompensa para provedores de recompensa de Desafios de Fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 3%

---

# Guia de definição de recompensa {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="Guia de definição de recompensa"
>abstract="Use este guia para configurar definições de premiação para provedores de premiação de fidelidade, incluindo o comportamento de definição padrão e campos de carga de preenchimento."

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
* **Guia de Definição de Recompensa** ◀︎ **Você está aqui**
* [Guia do Transformador de eventos](event-transformer-guide.md)
* [Dados e conjuntos de dados de fidelidade](loyalty-data-and-datasets.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade em [!DNL Journey Optimizer], consulte [ciclo de lançamento](../rn/releases.md).

Quando uma tarefa de desafio, marco ou desafio é concluído **e tem um valor de recompensa configurado**, a plataforma emite uma recompensa ao chamar o ponto de extremidade HTTP do seu provedor de recompensa com uma carga JSON. Uma **Definição de Recompensa** descreve qual recompensa deve ser emitida e fornece uma expressão [JSONata](https://docs.jsonata.org/overview) — `rewardJsonata` — que molda a carga exata que seu provedor espera.

Este guia aborda como configurar um provedor de premiação, criar definições de premiação, escrever a expressão `rewardJsonata` e entender qual contexto está disponível para ele no momento da avaliação.

## Modelo de dois níveis

As recompensas são organizadas em dois níveis:

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

Um **Provedor de Recompensa** representa um único sistema de recompensas externo — ele contém a URL do ponto de extremidade de entrega, a autenticação e qualquer cabeçalho HTTP personalizado. Um provedor pode conter várias **Definições de Recompensa**, cada uma descrevendo um tipo ou denominação de recompensa distinta oferecida por esse provedor (por exemplo, &quot;50 Estrelas&quot;, &quot;Estrelas Duplas&quot;, &quot;Item Gratuito&quot;).

Um desafio faz referência ao provedor e à definição por GUID. Quando uma premiação é emitida, a plataforma avalia a expressão `rewardJsonata` da definição e faz o POST do resultado para o ponto de extremidade do provedor.

## Prestador de recompensas e campos de definição

+++Campos de provedor de recompensa

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Obrigatório</th><th>Descrição</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>Não (atribuído pelo sistema)</td><td>Identificador exclusivo. Somente leitura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sim</strong></td><td>Nome de exibição, exclusivo dentro da organização.</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>Não</td><td>Descrição legível do provedor.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>Não</td><td>Quando <code>false</code>, a entrega de premiação é<br>suspensa para todas as definições neste provedor.</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>Sim</strong></td><td>Endpoint HTTP que recebe a carga do prêmio.<br>A plataforma publica a saída<br><code>rewardJsonata</code> avaliada para esta URL.</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>Não</td><td>Cabeçalhos HTTP personalizados para incluir em cada<br>solicitação de entrega (por exemplo, chaves de API,<br>substituições de tipo de conteúdo).</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>Não</td><td>Limite de taxa por provedor opcional (1-5000).<br>Nulo significa ilimitado.</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>Não</td><td>Se o ponto de extremidade requer TLS mútuo.</td></tr>
</table>

+++

+++Campos de definição de recompensa

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Obrigatório</th><th>Descrição</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>Não (atribuído pelo sistema)</td><td>Identificador exclusivo. Somente leitura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sim</strong></td><td>Nome de exibição, exclusivo no provedor.</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>Não</td><td>A unidade da premiação, usada na exibição<br> e disponível em expressões como<br><code>reward.denomination</code><br> (por exemplo, <code>"Stars"</code>, <code>"Points"</code>, <code>"Miles"</code>).</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>Não</td><td>Descrição da premiação, disponível<br>em expressões como <code>reward.desc</code>.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>Não</td><td>Quando <code>false</code>, esta definição fica inativa<br> e não emitirá recompensas.</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>Não</td><td>Marca isso como a definição padrão<br>de recompensa em toda a sandbox. Somente uma definição<br>em todos os provedores pode ser padrão de cada vez;<br>a definição de um novo padrão limpa a anterior.<br>Usado para popular automaticamente os detalhes da premiação em<br>desafios personalizados no momento da publicação.</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>Sim</strong></td><td>Expressão JSONata avaliada em <br>tempo de emissão de recompensa. Recebe o contexto de premiação <br> completo e deve retornar a carga JSON<br> para POST para o provedor.</td></tr>
</table>

+++

## O contexto da recompensa

Quando `rewardJsonata` é avaliado, ele recebe um único objeto raiz contendo tudo o que se sabe sobre o evento de premiação. Todos os caminhos na expressão são relativos a essa raiz.

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ Campos de contexto

| Campo | Descrição |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | A sequência de caracteres do valor de premiação configurada no desafio, tarefa ou marco que provocou essa ocorrência. |
| `rewardContext.source` | O que acionou a premiação: `"task"`, `"challenge"` ou `"milestone"`. |
| `reward` | A própria RewardDefinition — `name`, `desc`, `denomination`. |
| `task` | A tarefa de conclusão, incluindo `accumulators`, `schedule` e `reward`. |
| `task.accumulators.spend` | Total de gastos de qualificação acumulados pela tarefa. |
| `task.accumulators.qty` | Contagem total de itens qualificados acumulada pela tarefa. |
| `task.accumulators.item_list` | Todos os itens qualificados aplicados à tarefa. Cada entrada tem `item`, `transactionId`, `timestamp`, `utcOffset`, `locationId`. |
| `task.accumulators.item_list[-1]` | O item mais recente aplicado (índice negativo JSONata). Útil para fornecer a ID da última transação ou carimbo de data e hora. |
| `task.schedule.currentStreak` | Contagem de sequências de visitas consecutivas atuais (para desafios de sequências). |
| `task.schedule.currentVisits` | Contagem total de visitas (para desafios de visitas). |
| `milestone` | O marco que disparou esta recompensa, ou `null` se não for uma recompensa por marcos. Inclui `count` e `reward.rewardValue`. |
| `challenge.profileId` | A ID de fidelidade do membro. |
| `challenge.kvpCustom` | Pares de valores-chave personalizados configurados no desafio. Um padrão comum para transmitir IDs de campanha, nomes de produtos ou metadados específicos do provedor. |
| `challenge.name` | Nome do desafio. |
| `challenge._id` | ID do desafio. |
| `timestamp` | Carimbo de data e hora ISO 8601 da emissão de recompensa. |

+++

## Escrever a expressão awardJsonata

A expressão recebe o contexto de premiação como sua entrada e deve retornar um objeto JSON — a carga POST para o endpoint do provedor. A forma desse objeto depende totalmente da API do provedor; mapeie os campos de contexto em qualquer estrutura que o provedor espere.

+++Carga fixa simples

O caso mais simples: o provedor precisa de uma contagem de pontos e uma ID de membro, ambos conhecidos do contexto.

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**Saída:**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue` é sempre uma cadeia de caracteres. Use `$number()` para convertê-lo se o provedor esperar um valor numérico.

+++

+++Usando `kvpCustom` para metadados específicos do provedor

Os provedores geralmente exigem campos como IDs de campanha ou códigos do sistema de origem específicos para cada execução de desafio. Armazene-os em `challenge.kvpCustom` ao criar o desafio e, em seguida, faça referência a eles na expressão — mantendo a expressão reutilizável em campanhas.

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

Você também pode usar `reward.kvpCustom` para constantes que são fixas para um determinado tipo de recompensa em vez de por desafio.

+++

+++Uso de dados do acumulador de tarefas

Os acumuladores de tarefas mantêm um registro de cada evento qualificado. Usar `item_list[-1]` para acessar o item aplicado mais recentemente — seus `transactionId` e `timestamp` são úteis para trilhas de auditoria e desduplicação no lado do provedor.

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++Construção de uma mensagem de texto

Para provedores baseados em notificação (Slack, SMS, email), você pode criar uma cadeia de caracteres de mensagem diretamente usando o operador de concatenação `&` do JSONata:

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**Saída:**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## Exemplos

+++Exemplo 1 — Provedor de pontos simples

**Cenário:** uma API básica de pontos de fidelidade espera uma ID de membro e um valor de ponto.

**Definição de recompensa:**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**Expressão formatada:**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**Carga postada para o provedor:**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++Exemplo 2 — Carga do provedor com metadados de campanha

**Cenário:** o provedor requer um registro de prêmio estruturado que inclua campos de auditoria, referências de campanha e descrição do membro. Os valores específicos de campanha são armazenados em `challenge.kvpCustom` para que a mesma definição de premiação funcione em campanhas sem editar a expressão.

**Desafio`kvpCustom`** (definido ao criar o desafio):

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**Definição de recompensa:**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**Expressão formatada:**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**Carga postada para o provedor:**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++Exemplo 3 — Recompensa de marco

**Cenário:** um desafio de sequência emite uma recompensa por marcos a cada N visitas. A expressão inclui a contagem de etapas e a listra atual para o contexto do provedor.

**Expressão formatada:**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**Carga postada para o provedor** (na segunda etapa de visita):

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> Quando `rewardContext.source` é `"milestone"`, o objeto `milestone` é preenchido com `count` e `reward.rewardValue`. Quando a origem é `"task"` ou `"challenge"`, `milestone` é `null`.

+++

## Referência da API

+++Provedores de recompensa

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

Todas as solicitações exigem `x-gw-ims-org-id` e `x-sandbox-name` cabeçalhos.

**Criar um provedor:**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++Definições de recompensa

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**Criar uma definição de premiação:**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## Validação de expressão

`rewardJsonata` expressões são validadas para sintaxe no momento da publicação. Se a expressão for inválida, a API retornará um erro `422` com uma descrição da falha de análise.

Para desenvolver e testar uma expressão antes de publicar, use o [JSONata Exerciser](https://try.jsonata.org/). Cole o JSON de contexto de premiação como o documento de entrada e sua expressão para verificar se a saída corresponde ao que o provedor espera. Um contexto de premiação representativo para cada tipo de gatilho (`task`, `milestone`, `challenge`) é mostrado nos exemplos acima.

## Erros comuns

| Erro | Efeito | Corrigir |
|---------|--------|-----|
| `rewardContext.rewardValue` usado como um número sem conversão | Digite incompatibilidade se o provedor validar o campo como numérico | Envolver com `$number(rewardContext.rewardValue)` |
| `challenge.kvpCustom.someKey` retorna nulo | Chave não definida no desafio no momento da criação | Verifique se a chave está presente em `kvpCustom` em cada desafio que usa essa definição |
| `task.accumulators.item_list[-1]` é nulo | Nenhum item foi aplicado antes da premiação emitida (evento que não seja de compra) | Proteger com um condicional ou usar `timestamp` do contexto |
| `milestone` acessado quando a origem é `"task"` ou `"challenge"` | `milestone` é nulo; a expressão lança ou produz campos nulos | Marque `rewardContext.source` antes de acessar `milestone`, ou use apenas `milestone` em definições anexadas a recompensas por etapas |
| A expressão retorna uma matriz em vez de um objeto | O provedor recebe uma estrutura de carga inesperada | Envolver expressões de retorno de matriz em um objeto externo: `{ "items": [...] }` |
