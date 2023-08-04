---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: action, third-party, custom, jornada, API
hide: true
hidefromtoc: true
source-git-commit: d94988dd491759fe6ed8489403a3f1a295b19ef5
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 5%

---

# Aprimoramentos de ação personalizada

Agora você pode aproveitar as respostas de chamada da API em ações personalizadas e orquestrar suas jornadas com base nessas respostas.

Esse recurso só estava disponível ao usar fontes de dados. Agora você pode usá-lo com ações personalizadas.

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível como um beta privado.

## Definição da ação personalizada

Ao definir a ação personalizada, duas melhorias foram disponibilizadas: a adição do método GET e o novo campo de resposta de carga útil. As outras opções e parâmetros permanecem inalterados. Consulte [esta página](../action/about-custom-action-configuration.md).

### Configuração do endpoint

A variável **Configuração de URL** a seção foi renomeada **Configuração do endpoint**.

No **Método** , agora é possível selecionar **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Cargas

A variável **Parâmetros de ação** a seção foi renomeada **Cargas**. Dois campos estão disponíveis:

* A variável **Solicitação** field: este campo só está disponível para os métodos de chamada POST e PUT.
* A variável **Resposta** field: este é o novo recurso. Esse campo estava disponível para todos os métodos de chamada.

>[!NOTE]
> 
>Ambos os campos são opcionais.

![](assets/action-response2.png){width="70%" align="left"}

1. Clique dentro do **Resposta** campo.

   ![](assets/action-response3.png){width="80%" align="left"}

1. Cole um exemplo da carga útil retornada pela chamada. Verifique se os tipos de campo estão corretos (sequência, número inteiro etc.).

   ![](assets/action-response4.png){width="80%" align="left"}

1. Clique em **Salvar**.

Cada vez que a API é chamada, o sistema recuperará todos os campos incluídos no exemplo de carga útil. Observe que você pode clicar em **Colar uma nova carga** se quiser alterar a carga útil transmitida no momento.

Este é um exemplo de uma carga de resposta capturada durante a chamada para um serviço de API meteorológica:

```
{
    "coord": {
        "lon": 2.3488,
        "lat": 48.8534
    },
    "weather": [
        {
            "id": 800,
            "main": "Clear",
            "description": "clear sky",
            "icon": "01d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 29.78,
        "feels_like": 29.78,
        "temp_min": 29.92,
        "temp_max": 30.43,
        "pressure": 1016,
        "humidity": 31
    },
    "visibility": 10000,
    "wind": {
        "speed": 5.66,
        "deg": 70
    },
    "clouds": {
        "all": 0
    },
    "dt": 1686066467,
    "sys": {
        "type": 1,
        "id": 6550,
        "country": "FR",
        "sunrise": 1686023350,
        "sunset": 1686080973
    },
    "timezone": 7200,
    "id": 2988507,
    "name": "Paris",
    "cod": 200
}
```

## Como aproveitar a resposta em uma jornada

Basta adicionar a ação personalizada a uma jornada. Em seguida, você pode aproveitar os campos de carga de resposta em condições, outras ações e personalização de mensagens.

### Condições e ações

Por exemplo, você pode adicionar uma condição para verificar a velocidade do vento. Quando a pessoa entra na loja de surf você pode enviar um push se o tempo está muito ventoso .

![](assets/action-response5.png)

Na condição, é necessário usar o editor avançado para aproveitar os campos de resposta de ação, sob a **Contexto** nó.

![](assets/action-response6.png)

Você também pode aproveitar o **jo_status** para criar um novo caminho em caso de erro.

![](assets/action-response7.png)

>[!WARNING]
>
>Somente as ações personalizadas recém-criadas incluem esse campo pronto para uso. Se quiser usá-la com uma ação personalizada existente, será necessário atualizar a ação. Por exemplo, você pode atualizar a descrição e salvar.

Estes são os valores possíveis para este campo:

* código de status http: por exemplo **http_200** ou **http_400**
* erro de tempo limite: **tempo limite**
* erro de limite: **limitado**
* erro interno: **internalError**

Para obter mais informações sobre atividades de jornada, consulte [nesta seção](../building-journeys/about-journey-activities.md).

### Personalização da mensagem

Você pode personalizar suas mensagens usando os campos de resposta. No nosso exemplo, na notificação por push, personalizamos o conteúdo usando o valor de velocidade.

![](assets/action-response8.png)

>[!NOTE]
>
>A chamada é executada apenas uma vez por perfil em uma determinada jornada. Várias mensagens para o mesmo perfil não dispararão novas chamadas.

Para obter mais informações sobre a personalização da mensagem, consulte [nesta seção](../personalization/personalize.md).

## Sintaxe da expressão

Esta é a sintaxe:

```json
#@action{myAction.myField} 
```

Veja alguns exemplos:

```json
// action response field
@action{<action name>.<path to the field>}
@action{OpenWeatherMap.main.temp}
```

```json
// action response field
@action{<action name>.<path to the field>, defaultValue: <default value expression>}
@action{OpenWeatherMap.main.temp, defaultValue: 273.15}
@action{OpenWeatherMap.main.temp, defaultValue: @{myEvent.temperature}} 
```

Para obter mais informações sobre referências de campo, consulte [nesta seção](../building-journeys/expression/field-references.md).
