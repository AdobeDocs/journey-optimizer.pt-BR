---
solution: Journey Optimizer
product: journey optimizer
title: Integração com o Adobe Campaign v7/v8
description: Saiba como integrar com o Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Integração com o Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Ações do Adobe Campaign v7/v8"
>abstract="Essa integração está disponível para o Adobe Campaign Classic v7 e v8. Ele permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign. A conexão entre as instâncias do Journey Otimizer e do Campaign é configurada pela Adobe no momento do provisionamento."

Essa integração está disponível para o Adobe Campaign Classic v7, a partir da versão 7.1, e para o Adobe Campaign v8. Ele permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Otimizer e do Campaign é configurada pela Adobe no momento do provisionamento.

Um caso de uso completo é apresentado nesta [seção](../building-journeys/ajo-ac.md).

Para cada ação configurada, uma atividade de ação está disponível na paleta designer de jornada. Consulte esta [seção](../building-journeys/using-adobe-campaign-classic.md).

## Observações importantes {#important-notes}

* Não há limitação de mensagens. O sistema limita o número de mensagens que podem ser enviadas para 4000 por 5 minutos, com base no SLA atual do Campaign. Por isso, o Journey Otimizer deve ser usado somente em casos de uso unitários (eventos individuais, não segmentos).

* É necessário configurar uma ação na tela por modelo que deseja usar. Você precisa configurar uma ação no Journey Otimizer para cada modelo que deseja usar do Adobe Campaign.

* Recomendamos que você use uma instância dedicada do Centro de Mensagens que esteja hospedada para essa integração, a fim de evitar o impacto de outras operações do Campaign que possam ter sido realizadas. O servidor de marketing pode ser hospedado ou no local. A build necessária é 21.1 Release Candidate ou superior.

* Não há validação de que a carga ou a mensagem do Campaign esteja correta.

* Não é possível usar uma ação Campanha com um evento de qualificação de segmento.

## Pré-requisitos {#prerequisites}

No Campaign, é necessário criar e publicar uma mensagem transacional e seu evento associado. Consulte a [Documentação do Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

Você pode criar sua carga JSON correspondente a cada mensagem seguindo o padrão abaixo. Em seguida, você colará essa carga ao configurar a ação no Journey Otimizer (veja abaixo)

Veja um exemplo:

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

* **canal**: o canal definido para o template transacional do Campaign
* **eventType**: o nome interno do evento do Campaign
* **ctx**: com base na personalização que você tem em sua mensagem.

## Configurar a ação {#configure-action}

No Journey Otimizer, é necessário configurar uma ação por mensagem transacional. Siga estas etapas:

1. Crie uma nova ação. Consulte esta [seção](../action/action.md).
1. Insira um nome e uma descrição.
1. No **Tipo de ação** , selecione **Adobe Campaign Classic**.
1. Clique no botão **Carga** e cole um exemplo da carga JSON correspondente à mensagem Campaign . Entre em contato com a Adobe para obter essa carga.
1. Ajuste os diferentes campos para serem estáticos ou variáveis, dependendo se você deseja mapeá-los na tela Jornada. Determinados campos, como parâmetros de canal para endereços de email e campos de personalização (ctx), você provavelmente desejará defini-los como variáveis para mapeamento no contexto da jornada.
1. Clique em **Salvar**.

![](assets/accintegration1.png)
