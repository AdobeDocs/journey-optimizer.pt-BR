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
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 22%

---

# Integrar ao Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Ações do Adobe Campaign v7/v8"
>abstract="Essa integração está disponível para o Adobe Campaign v7 e v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign. A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento."

Essa integração está disponível para o Adobe Campaign v7/v8 a partir da versão 7.1 e o Adobe Campaign v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento.

Um caso de uso completo é apresentado neste [seção](../building-journeys/ajo-ac.md).

Para cada ação configurada, uma atividade de ação está disponível na paleta do designer de jornada. Consulte esta [seção](../building-journeys/using-adobe-campaign-v7-v8.md).

## Observações importantes {#important-notes}

* Não há limitação de mensagens. O sistema limita o número de mensagens que podem ser enviadas a 4000 a cada 5 minutos, com base no SLA do Campaign atual. Por esse motivo, o Journey Optimizer só deve ser usado em casos de uso unitários (eventos individuais, não públicos).

* Você precisa configurar uma ação na tela por modelo que deseja usar. É necessário configurar uma ação no Journey Optimizer para cada modelo que você deseja usar do Adobe Campaign.

* Recomendamos que você use uma instância dedicada do Centro de mensagens hospedada para essa integração para evitar que você afete outras operações do Campaign que possam estar ocorrendo. O servidor de marketing pode ser hospedado ou no local. A build necessária é a versão 21.1 ou posterior.

* Não há validação para indicar que a carga ou mensagem da campanha está correta.

* Não é possível usar uma ação do Campaign com um evento de qualificação de público-alvo.

## Pré-requisitos {#prerequisites}

No Campaign, você precisa criar e publicar uma mensagem transacional e seu evento associado. Consulte a [Documentação do Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

Você pode criar sua carga JSON correspondente a cada mensagem seguindo o padrão abaixo. Em seguida, você colará essa carga ao configurar a ação no Journey Optimizer (veja abaixo)

Exemplo:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **channel**: o canal definido para o template transacional do Campaign
* **eventType**: o nome interno do evento do Campaign
* **ctx**: variável com base na personalização que você tem na mensagem.

## Configuração da ação {#configure-action}

No Journey Optimizer, é necessário configurar uma ação por mensagem transacional. Siga estas etapas:

1. Criar uma nova ação. Consulte esta [seção](../action/action.md).
1. Insira um nome e uma descrição.
1. No **Tipo de ação** selecione **Adobe Campaign Classic**.
1. Clique em **Carga** e cole um exemplo da carga JSON correspondente à mensagem do Campaign. Entre em contato com o Adobe para obter essa carga.
1. Ajuste os diferentes campos para serem estáticos ou variáveis, dependendo se deseja mapeá-los na tela de Jornada. Determinados campos, como parâmetros de canal para campos de endereço de email e personalização (ctx), provavelmente serão definidos como variáveis para mapeamento no contexto da jornada.
1. Clique em **Salvar**.

![](assets/accintegration1.png)