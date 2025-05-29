---
solution: Journey Optimizer
product: journey optimizer
title: Integrar ao Adobe Campaign v7/v8
description: Saiba como integrar o Journey Optimizer ao Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, acc, integração
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 12%

---

# Integrar ao Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Ações do Adobe Campaign v7/v8"
>abstract="Essa integração está disponível para o Adobe Campaign v7 e v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign. A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento."

Se você tiver o Adobe Campaign Classic v7 ou o Campaign v8, uma ação personalizada específica estará disponível em suas jornadas para integrar o Adobe Journey Optimizer e o Adobe Campaign. Essa integração permite enviar emails, notificações por push e SMS usando recursos de mensagens transacionais do Adobe Campaign. Saiba mais neste [caso de uso completo](../building-journeys/ajo-ac.md).

Para cada ação configurada, uma [Atividade de ação de campanha](../building-journeys/using-adobe-campaign-v7-v8.md) está disponível na paleta do designer de jornada.

## Activation {#access}

Quando solicitado, a conexão entre os ambientes Journey Optimizer e Adobe Campaign é configurada pela Adobe no momento do provisionamento. Se você não solicitou a conexão no momento do provisionamento, entre em contato com o suporte da Adobe Journey Optimizer para solicitar a ativação. Você deve fornecer os seguintes detalhes:

>[!BEGINTABS]

>[!TAB Para Adobe Journey Optimizer]

* ID da organização (Adobe OrgID)
* Nome da sandbox

>[!TAB Para Adobe Campaign]

* URL do servidor do Campaign
* URL do servidor em tempo real
* Sua versão do Adobe Campaign

>[!ENDTABS]


## Medidas de proteção e limitações {#important-notes}

* Não há limitação de mensagens. O sistema limita o número de mensagens que podem ser enviadas a 4.000 a cada 5 minutos, com base no SLA do Campaign atual. Por esse motivo, o Journey Optimizer só deve ser usado em casos de uso unitários (eventos individuais, não públicos).

* Você deve configurar uma ação na tela por modelo a ser usado. É necessário configurar uma ação no Journey Optimizer para cada modelo que você deseja usar do Adobe Campaign.

* Recomendamos usar uma instância dedicada do Managed Services ou do Centro de mensagens hospedada para essa integração, a fim de evitar o impacto em outras operações do Campaign que você possa ter. O servidor de marketing pode ser hospedado ou no local.<!--The build required is 21.1 Release Candidate or greater. -->

* Não há validação para indicar que a carga ou mensagem da campanha está correta.

* Não é possível usar uma ação do Campaign com um evento de qualificação de público-alvo.

## Pré-requisitos {#prerequisites}

No Adobe Campaign, você deve criar e publicar uma mensagem transacional e seu evento associado. Consulte a [documentação do Adobe Campaign](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Você pode criar sua carga JSON correspondente a cada mensagem seguindo o padrão abaixo. Em seguida, você colará essa carga ao configurar a ação no Journey Optimizer (veja abaixo).

+++ Exemplo

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **canal**: o canal definido para o modelo transacional do Campaign
* **eventType**: o nome interno do evento do Campaign
* **ctx**: variável baseada na personalização que você tem em sua mensagem

+++

## Configurar a ação {#configure-action}

No Journey Optimizer, você deve configurar uma ação por mensagem transacional.

Para criar uma ação do Campaign, siga estas etapas:

1. Criar uma nova ação. [Saiba como criar ações personalizadas](../action/action.md).
1. Insira um nome e uma descrição.
1. No campo **Tipo de ação**, selecione **Adobe Campaign Classic**.
   ![](assets/accintegration1.png)
1. Clique no campo **Carga** e cole um exemplo da carga JSON correspondente à mensagem do Campaign. Entre em contato com a Adobe para obter essa carga.
1. Defina cada campo como estático ou variável com base em se você deseja que ele seja mapeado na tela de Jornada. Por exemplo, campos como parâmetros de canal de email e campos de personalização (`ctx`) normalmente devem ser definidos como variáveis para que possam se adaptar dinamicamente na jornada.
1. Clique em **Salvar**.

