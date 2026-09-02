---
solution: Journey Optimizer
product: journey optimizer
title: Referências de campo
description: Saiba mais sobre referências de campo em expressões avançadas
feature: Journeys
role: Developer
level: Experienced
keywords: jornada, campo, expressão, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 2%

---

# Referências de campo {#field-references}

Uma referência de campo pode ser anexada a um evento ou grupo de campos. As únicas informações relevantes são o nome do campo e seu caminho.

Se você estiver usando caracteres especiais em um campo, será necessário usar aspas duplas ou aspas simples. Estes são os casos em que as aspas são necessárias:

* o campo começa com caracteres numéricos
* o campo começa com o caractere &quot;-&quot;
* o campo contém qualquer item diferente de: _a_-_z_, _A_-_Z_, _0_-_9_, _,_-_

Por exemplo, se o seu campo é _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

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
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
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

### Função `entry`

Para recuperar um elemento em um mapa, usamos a função de entrada com uma determinada chave. Por exemplo, ele é usado ao definir a chave de um evento, de acordo com o namespace selecionado. Para obter mais informações, consulte [esta página](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

Nesta expressão, estamos obtendo a entrada da chave &quot;Email&quot; do campo &quot;IdentityMap&quot; de um evento. A entrada &#39;Email&#39; é uma coleção, da qual pegamos a &#39;id&#39; no primeiro elemento usando &#39;first()&#39;. Para obter mais informações, consulte [esta página](../expression/collection-management-functions.md).

### Função `firstEntryKey`

Para recuperar a primeira chave de entrada de um mapa, use a função `firstEntryKey`.

Este exemplo mostra como recuperar o primeiro endereço de email dos assinantes de uma lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

Neste exemplo, o nome da lista de assinaturas é `daily-email`. Os endereços de email são definidos como chaves no mapa `subscribers`, que está vinculado ao mapa da lista de assinaturas.

### Função `keys`

Para recuperar todas as chaves de um mapa, use a função `keys`.

Esse exemplo mostra como recuperar, para um perfil específico, todos os endereços de email associados aos assinantes de uma lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Valores de parâmetro de uma fonte de dados (valores dinâmicos da fonte de dados)

Se você selecionar um campo de uma fonte externa de dados que requer um parâmetro para ser chamado, uma nova guia será exibida à direita para permitir a especificação desse parâmetro. Consulte [esta página](../expression/expressionadvanced.md).

Para casos de uso mais complexos, se você quiser incluir os parâmetros da fonte de dados na expressão principal, defina os valores usando a palavra-chave _params_. Um parâmetro pode ser qualquer expressão válida mesmo de outra fonte de dados que também inclua outro parâmetro.

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como fazer referência a campos de eventos e grupos de campos de fonte de dados em expressões de jornada, incluindo a sintaxe de valor padrão, funções de acesso a mapa (`entry`, `firstEntryKey`, `keys`) e parâmetros de fonte de dados embutidos transmitindo com a palavra-chave `params`.

**Intenções:**

* Fazer referência a um campo de evento em uma expressão usando a sintaxe `@event{eventName.fieldPath}`
* Fazer referência a um grupo de campos de fonte de dados usando a sintaxe `#{dataSourceName.fieldGroupName.fieldPath}`
* Atribuir um valor padrão de fallback a uma referência de campo para que as expressões não retornem um valor nulo
* Recupere uma entrada específica de um mapa de identidade ou de assinatura usando a função `entry()`
* Recuperar todas as chaves de um campo de mapa usando a função `keys()`
* Passar valores de parâmetro para uma fonte de dados externa em linha usando a palavra-chave `params`

**Glossário:**

* **Referência de campo**: uma sintaxe de expressão que aponta para um campo nomeado dentro de uma carga do evento ou grupo de campos de fonte de dados *(específico do produto)*
* **defaultValue**: uma expressão de fallback opcional anexada a uma referência de campo que é retornada quando o campo está ausente ou é nula *(específica do produto)*
* **entry(key)**: uma função de mapa que recupera a entrada de coleção associada à chave fornecida *(específico do produto)*
* **firstEntryKey()**: uma função de mapa que retorna a primeira chave de um campo de mapa *(específico do produto)*
* **keys()**: uma função de mapa que retorna todas as chaves de um campo de mapa *(específico do produto)*
* **palavra-chave params**: sintaxe embutida para especificar valores de parâmetro para campos de fonte de dados externos na expressão principal *(específico do produto)*

**Medidas de Proteção:**

* Nomes de campos contendo caracteres especiais (começando com um dígito, contendo `-` ou caracteres fora de `a-z A-Z 0-9 _`) devem ser colocados entre aspas simples ou duplas
* A expressão de valor padrão deve retornar o mesmo tipo de dados que o campo — os tipos incompatíveis são inválidos
* Quando a palavra-chave `params` é usada para definir valores de parâmetro em linha, a guia de parâmetro separada à direita do editor desaparece
* As funções usadas como valores padrão devem ser encapsuladas entre parênteses

**Terminologia:**

* Nome canônico: Referências de campo — Acrônimo: none — variantes: caminho do campo, expressão do campo
* Sinônimos: `@event{...}` = &quot;referência de campo de evento&quot;; `#{...}` = &quot;referência de campo de fonte de dados&quot;
* Não confundir: campos de evento (com prefixo `@`) ≠ campos de fonte de dados (com prefixo `#`)

**Perguntas frequentes:**

* **P: Como faço referência a um campo cujo nome começa com um número?** — Envolva o nome do campo em aspas simples ou duplas, por exemplo: `#{OpenWeather.weatherData.rain.'3h'}`.
* **P: O que acontece quando um campo referenciado está ausente na carga do evento e nenhum valor padrão está definido?** — A expressão retorna `null`.
* **P: Como defino um valor padrão dinâmico usando uma função?** — Envolva a chamada de função entre parênteses, ex.: `defaultValue: (now())`.
* **P: Como faço para recuperar o endereço de email armazenado como a primeira chave em um mapa de assinantes?** — Use a função `firstEntryKey()` no campo de mapa de assinantes.
* **P: Como transfiro um parâmetro para uma fonte de dados externa sem usar a guia do lado direito?** — Use a palavra-chave `params` embutida: `#{DataSource.group.field, params: {paramName: value}}`.

+++
