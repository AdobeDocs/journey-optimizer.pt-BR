---
solution: Journey Optimizer
product: journey optimizer
title: Funções de gerenciamento de coleções
description: Saiba mais sobre os tipos de dados nas funções de gerenciamento de coleções
feature: Journeys
hide: true
hidefromtoc: true
role: Data Engineer, Architect
level: Experienced
keywords: query, coleções, funções, carga, jornada
source-git-commit: ff05675fb132becf092dc6b79bbbaa249f01af96
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 1%

---

# Funções de gerenciamento de coleções

A linguagem de expressão também introduz um conjunto de funções para consultar coleções.

Essas funções são explicadas abaixo. No exemplo a seguir, vamos usar a carga do evento que contém uma coleção:

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**A função &quot;all(`<condition>`)&quot;**

A função **[!UICONTROL all]** habilita a definição de um filtro em uma determinada coleção usando uma expressão booliana.

```json
<listExpression>.all(<condition>)
```

Por exemplo, entre todos os usuários do aplicativo, você pode obter os usuários usando o IOS 13 (expressão booleana &quot;app used == IOS 13&quot;). O resultado dessa função é a lista filtrada que contém itens correspondentes à expressão booleana (exemplo: usuário do aplicativo 1, usuário do aplicativo 34, usuário do aplicativo 432).

Em uma atividade Data Source Condition, você pode verificar se o resultado da função **[!UICONTROL all]** é nulo ou não. Você também pode combinar essa função **[!UICONTROL all]** com outras funções, como **[!UICONTROL count]**. Para obter mais informações, consulte [Atividade de Condição Data Source](../condition-activity.md#data_source_condition).


## Exemplos

>[!CAUTION]
>
>O uso de eventos de experiência em expressões/condições de jornada é suportado, mas não recomendado. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos, como [atributos computados](../../audience/computed-attributes.md), ou criar um segmento usando os eventos e incorporar esse segmento em [`inAudience` expressões](../../building-journeys/functions/functioninaudience.md).

**Exemplo 1:**

Queremos verificar se um usuário instalou uma versão específica de um aplicativo. Para isso, obtemos todos os tokens de notificação por push associados a aplicativos móveis para os quais a versão é 1.0. Em seguida, executamos uma condição com a função **[!UICONTROL count]** para verificar se a lista retornada de tokens contém pelo menos um elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

O resultado é true.

**Exemplo 2:**

Aqui usamos a função **[!UICONTROL count]** para verificar se há tokens de notificação por push na coleção.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

O resultado será true.

<!--Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.-->

>[!NOTE]
>
>Quando a condição de filtragem na função **all()** estiver vazia, o filtro retornará todos os elementos da lista. **No entanto, para contar o número de elementos de uma coleção, a função all não é necessária.**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

O resultado da expressão é **3**.

**Exemplo 3:**

Aqui verificamos se um indivíduo não recebeu nenhuma comunicação nas últimas 24 horas. Filtramos a coleção de eventos de experiência recuperados da fonte de dados ExperiencePlatform, usando duas expressões com base em dois elementos da coleção. Especificamente, o carimbo de data e hora do evento é comparado ao dateTime retornado pela função **[!UICONTROL nowWithDelta]**.

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

O resultado será true se não houver evento de experiência correspondente às duas condições.

**Exemplo 4:**

Aqui, queremos verificar se um indivíduo foi iniciado pelo menos uma vez em um aplicativo nos últimos 7 dias, para acionar uma notificação por push convidando-o a iniciar um tutorial.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** só está disponível ao manipular coleções de eventos, **[!UICONTROL currentDataPackField]** ao manipular coleções de fonte de dados e **[!UICONTROL currentActionField]** ao manipular coleções de resposta de ação personalizada.
>
>Ao processar coleções com **[!UICONTROL all]**, **[!UICONTROL first]** e **[!UICONTROL last]**, executamos um loop em cada elemento da coleção, um por um. **[!UICONTROL currentEventField]**, **currentDataPackField** e **[!UICONTROL currentActionField]** correspondem ao elemento que está sendo repetido.

**As funções &quot;first(`<condition>`)&quot; e &quot;last(`<condition>`)&quot;**

As funções **[!UICONTROL first]** e **[!UICONTROL last]** também habilitam a definição de um filtro na coleção ao retornar o primeiro/último elemento da lista que atende ao filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**Exemplo 1:**

Essa expressão retorna o primeiro token de notificação por push associado aos aplicativos móveis para os quais a versão é 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

O resultado é &quot;token_1&quot;.

**Exemplo 2:**

Essa expressão retorna o último token de notificação por push associado aos aplicativos móveis para os quais a versão é 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

O resultado é &quot;token_2&quot;.

>[!NOTE]
>
>Os eventos de experiência são recuperados do Adobe Experience Platform como uma coleção em ordem cronológica inversa, portanto:
>
>* A função **[!UICONTROL primeira]** retornará o evento mais recente
>* A função **[!UICONTROL last]** retornará a mais antiga.

**Exemplo 3:**

Verificamos se o primeiro evento (mais recente) do Adobe Analytics com um valor diferente de zero para a ID de DMA tem um valor igual a 602.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**A função &quot;at(`<index>`)&quot;**

A função **[!UICONTROL às]** permite fazer referência a um elemento específico em uma coleção de acordo com um índice.
O índice 0 é o primeiro índice da coleção.

_`<listExpression>`.às(`<index>`)_

**Exemplo:**

Essa expressão retorna o segundo token de notificação por push da lista.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

O resultado é &quot;token_2&quot;.

**Outros exemplos**

Essa expressão retorna os nomes de produtos com base no valor SKU. A lista desses produtos está incluída na lista de eventos, com a condição sendo a ID do evento.

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

Esta expressão recupera o nome do último produto na lista de produtos de um evento comercial em que o tipo de evento é &quot;productListAdds&quot; e o preço total é maior ou igual a 150.

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```
