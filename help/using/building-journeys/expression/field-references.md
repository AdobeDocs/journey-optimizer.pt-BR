---
solution: Journey Optimizer
product: journey optimizer
title: Referências de campo
description: Saiba mais sobre referências de campo em expressões avançadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: jornada, campo, expressão, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
source-git-commit: 7e850261f1a82492c5df93c4437b4e3c6859a2d7
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 2%

---

# Referências de campo {#field-references}

Uma referência de campo pode ser anexada a um evento ou grupo de campos. As únicas informações relevantes são o nome do campo e seu caminho.

Se estiver usando caracteres especiais em um campo, você precisará usar aspas duplas ou aspas simples. Estes são os casos em que as aspas são necessárias:

* o campo começa com caracteres numéricos
* o campo começa com o caractere &quot;-&quot;
* o campo contém qualquer coisa diferente de: _a_-_z_, _A_-_Z_, _0_-_9_, _ , _-_

Por exemplo, se o campo for _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

Na expressão, os campos de evento são referenciados com &quot;@&quot; e os campos da fonte de dados com &quot;#&quot;.

Uma cor de sintaxe é usada para distinguir visualmente campos de eventos (verde) de grupos de campos (azul).

## Valores padrão para referências de campo {#default-value}

Um valor padrão pode ser associado a um nome de campo. A sintaxe é a seguinte:

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>O tipo de campo e o valor padrão devem ser iguais. Por exemplo, `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}` é inválido porque o valor padrão é um inteiro, enquanto o valor esperado deve ser uma cadeia de caracteres.

Exemplos:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.producdId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

Você pode adicionar qualquer tipo de expressão como valor padrão. A única restrição é que a expressão deve retornar o tipo de dados esperado. Ao usar uma função, é necessário encapsulá-la com ().

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Referência a um campo dentro das coleções

Os elementos definidos nas coleções são referenciados usando as funções específicas `all`, `first` e `last`. Para obter mais informações, consulte [esta página](../expression/collection-management-functions.md).

Exemplo:

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Referência a um campo definido em um mapa

### `entry` função

Para recuperar um elemento em um mapa, usamos a função de entrada com uma determinada chave. Por exemplo, ele é usado ao definir a chave de um evento, de acordo com o namespace selecionado. Para obter mais informações, consulte [esta página](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

Nesta expressão, estamos obtendo a entrada da chave &quot;Email&quot; do campo &quot;IdentityMap&quot; de um evento. A entrada &#39;Email&#39; é uma coleção, da qual pegamos a &#39;id&#39; no primeiro elemento usando &#39;first()&#39;. Para obter mais informações, consulte [esta página](../expression/collection-management-functions.md).

### `firstEntryKey` função

Para recuperar a primeira chave de entrada de um mapa, use o `firstEntryKey` função.

Este exemplo mostra como recuperar o primeiro endereço de email dos assinantes de uma lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

Neste exemplo, a lista de assinaturas é nomeada `daily-email`. Os endereços de email são definidos como chaves na variável `subscribers` que é vinculado ao mapa da lista de assinaturas.

### `keys` função

Para recuperar todas as chaves de um mapa, use o `keys` função.

Esse exemplo mostra como recuperar, para um perfil específico, todos os endereços de email associados aos assinantes de uma lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Valores de parâmetro de uma fonte de dados (valores dinâmicos da fonte de dados)

Se você selecionar um campo de uma fonte externa de dados que requer um parâmetro para ser chamado, uma nova guia será exibida à direita para permitir a especificação desse parâmetro. Consulte [esta página](../expression/expressionadvanced.md).

Para casos de uso mais complexos, se quiser incluir os parâmetros da fonte de dados na expressão principal, você poderá definir os valores usando a palavra-chave _params_. Um parâmetro pode ser qualquer expressão válida mesmo de outra fonte de dados que também inclua outro parâmetro.

>[!NOTE]
>
>Ao definir os valores de parâmetro na expressão, a guia à direita desaparece.

Use a seguinte sintaxe:

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: nome exato do primeiro parâmetro da fonte de dados.
* **`<params-1-value>`**: o valor do primeiro parâmetro. Pode ser qualquer expressão válida.

Exemplo:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```
