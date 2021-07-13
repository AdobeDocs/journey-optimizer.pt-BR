---
title: Integrar ao Adobe Campaign v7/v8
description: Saiba como integrar com o Adobe Campaign v7/v8
feature: Ações
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 7%

---

# Integrar ao Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

Essa integração está disponível para o Adobe Campaign Classic v7 a partir da versão 21.1 e Adobe Campaign v8. Ele permite enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pelo Adobe no momento do provisionamento.

Um caso de uso completo é apresentado nesta [seção](../building-journeys/campaign-classic-use-case.md).

Para cada ação configurada, uma atividade de ação está disponível na paleta Designer de jornadas. Consulte esta [seção](../building-journeys/using-adobe-campaign-classic.md).

## Observações importantes

* Não há limitação de mensagens. Limitamos o número de mensagens que podem ser enviadas para 50.000/hora com base em nosso SLA atual do Campaign. Por esse motivo, o Journey Optimizer deve ser usado somente em casos de uso unitários (eventos individuais, não segmentos).

* É necessário configurar uma ação na tela por modelo que deseja usar. É necessário configurar uma ação no Journey Optimizer para cada modelo que deseja usar no Adobe Campaign.

* Recomendamos que você use uma instância dedicada do Centro de Mensagens que esteja hospedada para essa integração, a fim de evitar o impacto de outras operações do Campaign que possam ter sido realizadas. O servidor de marketing pode ser hospedado ou no local. A build necessária é 21.1 Release Candidate ou superior.

* Não há validação de que a carga ou a mensagem do Campaign esteja correta.

* Não é possível usar uma ação Campanha com um evento de qualificação de segmento.

## Pré-requisitos

No Campaign, é necessário criar e publicar uma mensagem transacional e seu evento associado. Consulte a [documentação do Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

Você pode criar sua carga JSON correspondente a cada mensagem seguindo o padrão abaixo. Em seguida, você colará essa carga ao configurar a ação no Journey Orchestration (veja abaixo)

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

* **canal**: o canal definido para o template transacional do Campaign
* **eventType**: o nome interno do evento do Campaign
* **ctx**: com base na personalização que você tem em sua mensagem.

## Configurar a ação

No Journey Optimizer, é necessário configurar uma ação por mensagem transacional. Siga estas etapas:

1. Crie uma nova ação. Consulte esta [seção](../action/action.md).
1. Insira um nome e uma descrição.
1. No campo **Action type**, selecione **Adobe Campaign Classic**.
1. Clique no campo **Payload** e cole um exemplo da carga JSON correspondente à mensagem do Campaign. Entre em contato com o Adobe para obter essa carga.
1. Ajuste os diferentes campos para serem estáticos ou variáveis, dependendo de se deseja mapeá-los na tela de Jornada. Determinados campos, como parâmetros de canal para endereços de email e campos de personalização (ctx), você provavelmente desejará defini-los como variáveis para mapeamento no contexto da jornada.
1. Clique em **Salvar**.

![](../assets/accintegration1.png)


