---
solution: Journey Optimizer
product: journey optimizer
title: Funções de gerenciamento de coleções
description: Saiba mais sobre os tipos de dados nas funções de gerenciamento de coleções
feature: Journeys
hide: true
role: Developer
level: Experienced
keywords: query, coleções, funções, carga, jornada
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1222
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

Em uma atividade Data Source Condition, você pode verificar se o resultado da função **[!UICONTROL all]** é nulo ou não. Você também pode combinar essa função **[!UICONTROL all]** com outras funções, como **[!UICONTROL count]**. Para obter mais informações, consulte [Atividade de Condição Data Source](../conditions.md#data_source_condition).


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

<!--
Alternatively, you can check if there is no token in the collection:

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
earlier timestamp) in order to only consider prior events.
-->

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

<!--
**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`
-->

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica as funções de gerenciamento de coleções `all()`, `first()`, `last()` e `at()` disponíveis na linguagem de expressão de Jornada, com exemplos usando cargas de token de notificação por push e dados de evento de experiência.

**Intenções:**

* Filtrar uma coleção usando uma condição booleana com `all(<condition>)` para recuperar elementos correspondentes
* Contar elementos em uma coleção usando a função `count()` combinada com `all()`
* Recuperar o primeiro ou último elemento de uma coleção filtrada usando `first()` ou `last()`
* Acessar um elemento específico em uma coleção pelo índice usando `at(<index>)`
* Combinar consultas de coleção aninhadas para pesquisar nomes de produtos por SKU ou por tipo de evento e limite de preço

**Glossário:**

* **all(condition)**: função de coleção que filtra uma lista e retorna itens correspondentes à expressão booleana especificada *(específico do produto)*
* **first(condition)**: função de coleção que retorna o primeiro elemento (mais recente, para eventos de experiência) correspondente à condição *(específico do produto)*
* **last(condition)**: função de coleção que retorna o último elemento (mais antigo, para eventos de experiência) correspondente à condição *(específico do produto)*
* **at(index)**: função de coleção que retorna o elemento em um índice de base zero específico *(product-specific)*
* **currentEventField**: Variável de loop disponível ao iterar coleções de eventos dentro de `all()`, `first()` ou `last()` *(específico do produto)*
* **currentDataPackField**: variável de loop disponível ao iterar em coleções de fonte de dados *(específico do produto)*
* **currentActionField**: variável de loop disponível ao iterar sobre coleções de resposta de ação personalizada *(específico do produto)*

**Medidas de Proteção:**

* O uso de eventos de experiência em expressões/condições de jornada é suportado, mas não recomendado; considere atributos computados ou segmentos de público-alvo como alternativas
* `currentEventField` está disponível somente para coleções de eventos; `currentDataPackField` para coleções de fonte de dados; `currentActionField` para coleções de resposta de ação personalizada
* A função `all` não é necessária para contar elementos de uma coleção — `count()` pode ser aplicada diretamente ao campo de coleção
* Os eventos de experiência são recuperados em ordem cronológica inversa: `first()` retorna o evento mais recente, `last()` retorna o mais antigo

**Terminologia:**

* Nome canônico: Funções de Gerenciamento de Coleta — Acrônimo: nenhum — variantes: funções de coleta, funções de coleta de consulta
* Sinônimos: &quot;all()&quot; = &quot;função de filtro&quot;; &quot;first()&quot; = &quot;função de elemento mais recente&quot; (para eventos de experiência)
* Não confunda: `first()` (evento de experiência mais recente) ≠ primeiro elemento por ordem de inserção

**Perguntas frequentes:**

* **P: O que `all()` retorna quando a condição está vazia?** — Retorna todos os elementos na lista, equivalente a sem filtragem.
* **P: Como posso contar o número de tokens de notificação por push em uma coleção?** — Use `count()` diretamente no caminho do campo de token sem exigir `all()`, por exemplo, `count(@event{...pushNotificationTokens.token})`.
* **P: Como faço para obter o segundo elemento de uma coleção?** — Use `at(1)`, pois o índice 0 é o primeiro elemento.
* **P: Por que `first()` retorna o evento de experiência mais recente?** — Os eventos de experiência são recuperados do Adobe Experience Platform em ordem cronológica inversa, portanto, `first()` escolhe o item superior (mais recente).
* **P: Como verificar se um usuário não recebeu nenhuma comunicação nas últimas 24 horas?** — Filtre a coleção de eventos de experiência com `nowWithDelta(-1, "days")` como um limite inferior de carimbo de data/hora e use `count(...) == 0`.

+++
