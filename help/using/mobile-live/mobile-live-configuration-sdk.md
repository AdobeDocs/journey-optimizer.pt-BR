---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de atividade do Live
description: Saiba como configurar a integração do Adobe Experience Platform Mobile SDK
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 02ca7c8e-105a-4e77-9aad-2381904255d0
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Integração de atividade ao vivo com o Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}


O Adobe Experience Platform Mobile SDK fornece suporte integrado para a atividade do Apple Live. Isso permite que seu aplicativo exiba atualizações dinâmicas e em tempo real diretamente na Tela de bloqueio e na Ilha dinâmica sem abrir o aplicativo.

1. [Importar módulos obrigatórios](#import)

   Importar os seguintes módulos: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Definir atributos](#attributes)

   Em conformidade com `LiveActivityAttributes`, inclua `LiveActivityData` e um `ContentState` atributos.

1. [Registrar atividade ao vivo](#register)

   Use `Messaging.registerLiveActivity()` após a inicialização do SDK.

1. [Criar configuração de widget](#widget)

   Implemente `ActivityConfiguration` para a interface Tela de Bloqueio e Ilha Dinâmica.

1. [Iniciar uma atividade Live localmente (opcional)](#local)

   A atividade online pode ser iniciada remotamente por meio do Journey Optimizer ou localmente dentro do código do aplicativo.

1. [Adicionar suporte de depuração (opcional)](#debug)

   Implementar o `LiveActivityAssuranceDebuggable` para Assurance.

Verifique se as versões mínimas a seguir estão instaladas para garantir a configuração e a compatibilidade corretas.

>[!BEGINSHADEBOX]

**Pré-requisitos:**

* **iOS:**
   * **iOS16.1 ou posterior**: funcionalidade básica de atividade online
   * **iOS 17.2+**: suporte push-to-start
   * **iOS 18+**: suporte ao canal de transmissão
* **Xcode:** 14.0 ou posterior
* **Swift:** 5.7 ou posterior
* **Dependências:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit
* **AEP Mobile SDK versão**: iOS Messaging 5.11.0 ou posterior

>[!ENDSHADEBOX]

## Etapa 1: importar módulos obrigatórios {#import}

Para começar, primeiro você precisa importar os seguintes módulos: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Etapa 2: definir seus atributos de atividade Live {#attributes}

Crie uma estrutura que esteja em conformidade com o protocolo `LiveActivityAttributes`. Isso define o estado dos dados estáticos e do conteúdo dinâmico para a atividade Live.

Os principais componentes incluem:

* **`liveActivityData`** (obrigatório) que contém dados específicos do Adobe Experience Platform.
   * Para usuários individuais: Use `LiveActivityData(liveActivityID: "unique-id")`
   * Para difusão: Use `LiveActivityData(channelID: "channel-id")`

* Atributos estáticos, propriedades personalizadas específicas ao seu caso de uso, por exemplo, `restaurantName`.

* **`ContentState`** que define dados dinâmicos que podem ser atualizados durante o ciclo de vida da atividade Live. Deve estar em conformidade com `Codable` e `Hashable`.

* A enumeração `LiveActivityOrigin` especifica se uma atividade foi iniciada localmente no aplicativo ou remotamente por meio de uma notificação push-to-start, com suporte no iOS 17.2 e posterior. Esse valor permite que o SDK diferencie entre atividades online iniciadas localmente e acionadas remotamente durante a coleta de dados.

**Exemplos**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activity
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activity
    public init(liveActivityID: String)   // For individual Live activity
}
```

Você também pode registrar vários tipos de atividade ao vivo para seu aplicativo:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Etapa 3: Registrar atividade Live {#register}

Registre seus tipos de atividade Live no `AppDelegate` após a inicialização do SDK. Isso permite:

* Habilita a coleção automática de token de push-para-início (iOS 17.2+)
* Coleta tokens de atualização de atividade em tempo real automaticamente
* Permite o gerenciamento do ciclo de vida e o rastreamento de eventos

**Exemplo de uma atividade Live de entrega de alimentos:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Etapa 4: Criar widgets de atividade ao vivo {#widgets}

A atividade ao vivo é exibida por meio de widgets, é necessário criar um pacote de widgets e uma configuração:

**Exemplo de uma atividade Live de entrega de alimentos:**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## Etapa 5: iniciar uma atividade Live localmente (opcional) {#local}

Embora o Journey Optimizer possa iniciar remotamente a atividade Live, você também pode iniciá-la localmente:

**Exemplo de uma atividade Live de entrega de alimentos:**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## Etapa 6: adicionar suporte de depuração (opcional) {#debug}

Se necessário, você pode depurar esquemas de atividade ao vivo no Adobe Assurance:

**Exemplo de uma atividade Live de entrega de alimentos:**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```
