---
solution: Journey Optimizer
product: journey optimizer
title: Uso do editor de expressão avançado
description: Saiba como criar expressões avançadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
hide: true
hidefromtoc: true
keywords: expressão, condição, casos de uso, eventos
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
source-git-commit: 7ac246c0aa6776d3ec67223c4b07536b8ed0c881
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 2%

---


# Exemplos de expressão avançada{#advanced-expression-examples}

O editor de expressão avançado pode ser usado para criar condições que permitem filtrar usuários em suas jornadas. Essas condições permitem direcionar os usuários no prazo, data, local, duração para que eles possam ser redirecionados na jornada.

>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../exp-event-lookup.md)


## Criação de condições em Eventos de experiência


>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../exp-event-lookup.md)
>



O editor de expressão avançado é obrigatório para executar consultas em séries de tempo, como uma lista de compras ou cliques anteriores em mensagens. Essas consultas não podem ser executadas usando o editor simples.

>[!NOTE]
>
>Eventos começam com @, fontes de dados com #.

Os eventos de experiência são recuperados do Adobe Experience Platform como uma coleção em ordem cronológica inversa, portanto:

* a primeira função retornará o evento mais recente
* a última função retornará a mais antiga.

Por exemplo, digamos que você queira direcionar os clientes com um abandono de carrinho nos últimos 7 dias para enviar uma mensagem quando o cliente estiver chegando perto de uma loja, com uma oferta nos itens desejados que estão na loja.

**Você precisa criar as seguintes condições:**

Primeiro de tudo, clientes-alvo que navegaram na loja online, mas não finalizaram o pedido nos últimos sete dias.

**Esta expressão procura um valor especificado em um valor de cadeia de caracteres:**

`In ("addToCart", #{field reference from experience event})`

**Esta expressão procura todos os eventos para este usuário especificado nos últimos 7 dias:**

Em seguida, ele seleciona todos os eventos de adição ao carrinho que não se transformaram em uma compra completa.

>[!NOTE]
>
>Para inserir campos na expressão rapidamente, clique duas vezes no campo no painel esquerdo do editor.

O carimbo de data e hora especificado está agindo como o valor de data e hora, o segundo é o número de dias.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Essa expressão retorna um valor booleano.

**Agora vamos criar uma expressão verificando se o produto está em estoque**

* No Inventário, essa expressão procura o campo de quantidade de um produto e especifica que ele deve ser maior que 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* À direita, os valores necessários são especificados, aqui, precisamos recuperar o local do armazenamento, que é mapeado do local do evento &quot;ArriveLumaStudio&quot;:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* E especifique SKU, usando a função `first` para recuperar a interação &quot;addToCart&quot; mais recente:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

A partir daí, você pode adicionar outro caminho na jornada para quando o produto não estiver na loja e enviar uma notificação com oferta de engajamento. Configure as mensagens de acordo e use dados de personalização para aprimorar o público-alvo da mensagem.

## Exemplos de manipulações de cadeias de caracteres com o editor de expressão avançado

**Em condições**

Essa condição recupera apenas os eventos de geofence acionados em &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explicação: Esta é uma comparação de sequência estrita (diferencia maiúsculas de minúsculas), equivalente a uma consulta no modo simples que usa `equal to` com `Is sensitive` marcado.

A mesma consulta com `Is sensitive` desmarcado gerará a seguinte expressão no modo avançado:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**Em ações**

A seguinte expressão permite definir a ID do CRM em um campo de personalização de ação:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Explicação: Este exemplo usa as funções `substr` e `lastIndexOf` para remover chaves que delimitam a ID do CRM transmitida com um evento de inicialização de aplicativo móvel.


Para obter mais informações sobre como usar o editor de expressão avançado, assista a [este vídeo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=pt-BR).
