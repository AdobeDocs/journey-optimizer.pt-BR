---
solution: Journey Optimizer
product: journey optimizer
title: Funções de gerenciamento de coleções
description: Saiba mais sobre os tipos de dados nas funções de gerenciamento de coleções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: query, coleções, funções, carga, jornada
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
source-git-commit: 8e020f79e0f44e6fc804fcceb149146f9644c777
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# Funções de gerenciamento de coleções {#collection-management-functions}


## Sobre funções de coleção de consulta

A linguagem de expressão também introduz um conjunto de funções para consultar coleções. Essas funções são explicadas abaixo.

No exemplo a seguir, vamos usar a carga do evento que contém uma coleção:

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

## A função all(`<condition>`)

A função **[!UICONTROL all]** habilita a definição de um filtro em uma determinada coleção usando uma expressão booliana.

```json
<listExpression>.all(<condition>)
```

Por exemplo, entre todos os usuários do aplicativo, você pode obter os usuários usando o IOS 13 (expressão booleana &quot;app used == IOS 13&quot;). O resultado dessa função é a lista filtrada que contém itens correspondentes à expressão booleana (exemplo: usuário do aplicativo 1, usuário do aplicativo 34, usuário do aplicativo 432).

Em uma atividade Data Source Condition, você pode verificar se o resultado da função **[!UICONTROL all]** é nulo ou não. Você também pode combinar essa função **[!UICONTROL all]** com outras funções, como **[!UICONTROL count]**. Para obter mais informações, consulte [Atividade de Condição Data Source](../condition-activity.md#data_source_condition).


>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../exp-event-lookup.md)

### Exemplo 1

Queremos verificar se um usuário instalou uma versão específica de um aplicativo. Para isso, obtemos todos os tokens de notificação por push associados a aplicativos móveis para os quais a versão é 1.0. Em seguida, executamos uma condição com a função **[!UICONTROL count]** para verificar se a lista retornada de tokens contém pelo menos um elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

O resultado é true.

### Exemplo 2

Aqui usamos a função **[!UICONTROL count]** para verificar se há tokens de notificação por push na coleção.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


O resultado é true.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

O resultado da expressão é **3**.


>[!NOTE]
>
>* Quando a condição de filtragem na função **all()** estiver vazia, o filtro retornará todos os elementos da lista. **No entanto, para contar o número de elementos de uma coleção, a função all não é necessária.
>
>* `currentEventField` está disponível somente ao manipular coleções de eventos, `currentDataPackField` ao manipular coleções de fonte de dados e `currentActionField` ao manipular coleções de resposta de ação personalizada.
>
>  Ao processar coleções com `all`, `first` e `last`, repetimos cada elemento da coleção um por um. `currentEventField`, `currentDataPackField` e `currentActionField` correspondem ao elemento que está sendo repetido.


## As funções first(`<condition>`) e last(`<condition>`)

As funções **[!UICONTROL first]** e **[!UICONTROL last]** também habilitam a definição de um filtro na coleção ao retornar o primeiro/último elemento da lista que atende ao filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Exemplo 1

Essa expressão retorna o primeiro token de notificação por push associado aos aplicativos móveis para os quais a versão é 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

O resultado é `token_1`.

### Exemplo 2

Essa expressão retorna o último token de notificação por push associado aos aplicativos móveis para os quais a versão é 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

O resultado é `token_2`.

## A função at(`<index>`)

A função **[!UICONTROL às]** permite fazer referência a um elemento específico em uma coleção de acordo com um índice.
O índice 0 é o primeiro índice da coleção.

_`<listExpression>`.às(`<index>`)_

### Exemplo

Essa expressão retorna o segundo token de notificação por push da lista.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}`
```

O resultado é `token_2`.