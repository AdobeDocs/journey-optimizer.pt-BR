---
solution: Journey Optimizer
product: journey optimizer
title: Aprimoramentos de ação personalizada
description: Saiba mais sobre os últimos aprimoramentos das ações personalizadas
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
exl-id: d88daa58-20af-4dac-ae5d-4c10c1db6956
source-git-commit: 7e850261f1a82492c5df93c4437b4e3c6859a2d7
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 6%

---

# Usar as respostas de chamada da API em ações personalizadas {#custom-action-enhancements}

Você pode aproveitar as respostas de chamada da API em ações personalizadas e orquestrar suas jornadas com base nessas respostas.

<!--
You can now leverage API call responses in custom actions and orchestrate your journeys based on these responses.

This capability was previously only available when using data sources. You can now use it with custom actions. 
-->

## Observações importantes{#custom-action-enhancements-notes}

<!--
* Custom actions should only be used with private or internal endpoints, and used with an appropriate capping or throttling limit. See [this page](../configuration/external-systems.md). 
-->

* Os arrays escalares são compatíveis com a carga de resposta:

  ```
  "dummyScalarArray": [
  "val1",
  "val2"
  ]
  ```

* Arrays heterogêneos não são aceitos na carga de resposta:

  ```
  "dummyRandomArray": [
  20,
  "aafw",
  false
  ]
  ```

<!--
## Best practices{#custom-action-enhancements-best-practices}

A capping limit of 5000 calls/s is defined for all custom actions. This limit has been set based on customers usage, to protect external endpoints targeted by custom actions. You need to take this into account in your audience-based journeys by defining an appropriate reading rate (5000 profiles/s when custom actions are used). If needed, you can override this setting by defining a greater capping or throttling limit through our Capping/Throttling APIs. See [this page](../configuration/external-systems.md).

You should not target public endpoints with custom actions for various reasons:

* Without proper capping or throttling, there is a risk of sending too many calls to a public endpoint that may not support such volume.
* Profile data can be sent through custom actions, so targeting a public endpoint could lead to inadvertently sharing personal information externally.
* You have no control on the data being returned by public endpoints. If an endpoint changes its API or starts sending incorrect information, those will be made available in communications sent, with potential negative impacts.
-->

<!--
## Define the custom action {#define-custom-action}

When defining the custom action, two enhancements have been made available: the addition of the GET method and the new payload response field. The other options and parameters are unchanged. See [this page](../action/about-custom-action-configuration.md).

### Endpoint configuration {#endpoint-configuration}

The **URL configuration** section has been renamed **Endpoint configuration**.

In the **Method** drop-down, you can now select **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads {#payloads-new}

The **Action parameters** section has been renamed **Payloads**. Two fields are available:

* The **Request** field: this field is only available for POST and PUT calling methods.
* The **Response** field: this is the new capability. This field as available for all calling methods.

>[!NOTE]
> 
>Both these fields are optional.

![](assets/action-response2.png){width="70%" align="left"}
-->

## Configurar a ação personalizada {#config-response}

1. Crie a ação personalizada. Consulte [esta página](../action/about-custom-action-configuration.md).

1. Clique dentro do campo **Resposta**.

   ![](assets/action-response2.png){width="80%" align="left"}

1. Cole um exemplo da carga útil retornada pela chamada. Verifique se os tipos de campo estão corretos (sequência, número inteiro etc.). Este é um exemplo de carga de resposta capturada durante a chamada. Nosso terminal local envia o número de pontos de fidelidade e o status de um perfil.

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   Cada vez que a API é chamada, o sistema recuperará todos os campos incluídos no exemplo de carga útil.

1. Também vamos adicionar a customerID como parâmetro de consulta.

   ![](assets/action-response9.png){width="80%" align="left"}

1. Clique em **Salvar**.

## Aproveitar a resposta em uma jornada {#response-in-journey}

Basta adicionar a ação personalizada a uma jornada. Em seguida, você pode aproveitar os campos de carga de resposta em condições, outras ações e personalização de mensagens.

Por exemplo, você pode adicionar uma condição para verificar o número de pontos de fidelidade. Quando a pessoa entra no restaurante, o terminal local envia uma chamada com as informações de fidelidade do perfil. Você pode enviar um push se o perfil for um cliente gold. Se um erro for detectado na chamada, envie uma ação personalizada para notificar o administrador do sistema.

![](assets/action-response5.png)

1. Adicione o evento e a ação personalizada Fidelidade criada anteriormente.

1. Na ação personalizada de Fidelidade, mapeie o parâmetro de consulta da ID do cliente com a ID do perfil. Marque a opção **Adicionar um caminho alternativo em caso de tempo limite ou erro**.

   ![](assets/action-response10.png)

1. Na primeira ramificação, adicione uma condição e use o editor avançado para aproveitar os campos de resposta de ação, no nó **Contexto**.

   ![](assets/action-response6.png)

1. Em seguida, adicione o push e personalize a mensagem usando os campos de resposta. No nosso exemplo, personalizamos o conteúdo usando o número de pontos de fidelidade e o status do cliente. Os campos de resposta de ação estão disponíveis em **Atributos contextuais** > **Journey Orchestration** > **Ações**.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >Cada perfil que entra na ação personalizada acionará uma chamada. Mesmo que a resposta seja sempre a mesma, o Jornada ainda executará uma chamada por perfil.

1. Na ramificação de tempo limite e erro, adicione uma condição e utilize o campo interno **jo_status_code**. No nosso exemplo, estamos usando a variável
   Tipo de erro **http_400**. Consulte [esta seção](#error-status).

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. Adicione uma ação personalizada que será enviada para sua organização.

   ![](assets/action-response11.png)

## Logs do modo de teste {#test-mode-logs}

Você pode acessar, por meio do modo de teste, os logs de status relacionados às respostas de ação personalizadas. Se você tiver definido ações personalizadas com respostas na jornada, verá uma seção **actionsHistory** nesses logs exibindo a carga retornada pelo ponto de extremidade externo (como resposta dessa ação personalizada). Isso pode ser muito útil em termos de depuração.

![](assets/action-response12.png)

## Status do erro {#error-status}

O campo **jo_status_code** está sempre disponível mesmo quando nenhuma carga de resposta é definida.

Estes são os valores possíveis para este campo:

* código de status http: http_`<HTTP API call returned code>`, por exemplo http_200 ou http_400
* erro de tempo limite: **tempo limite**
* erro de limite: **limite**
* erro interno: **internalError**

Uma chamada de ação é considerada com erro quando o código http retornado é maior que 2xx ou se ocorrer um erro. A jornada flui para a ramificação de tempo limite ou erro dedicada nesses casos.

>[!WARNING]
>
>Somente as ações personalizadas recém-criadas incluem o campo **jo_status_code** pronto para uso. Se quiser usá-la com uma ação personalizada existente, será necessário atualizar a ação. Por exemplo, você pode atualizar a descrição e salvar.

## Sintaxe da expressão {#exp-syntax}

Esta é a sintaxe:

```json
#@action{myAction.myField} 
```

Veja alguns exemplos:

```json
 // action response field
 @action{<action name>.<path to the field>}
 @action{ActionLoyalty.status}
```

```json
 // action response field
 @action{<action name>.<path to the field>, defaultValue: <default value expression>}
 @action{ActionLoyalty.points, defaultValue: 0}
 @action{ActionLoyalty.points, defaultValue: @event{myEvent.newPoints}}
```

Ao manipular coleções em uma resposta de ação personalizada, você pode confiar em `currentActionField` para acessar o item atual:

```json
count(
@action{MyAction.MyCollection.all(
currentActionField.description == "abc"
)}
)
```

## Recursos adicionais

Para obter mais informações, consulte estas páginas:

* [Referências de campo](../building-journeys/expression/field-references.md).
* [Funções de gerenciamento de coleções](../building-journeys/expression/collection-management-functions.md)
