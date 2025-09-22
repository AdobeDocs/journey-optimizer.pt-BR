---
solution: Journey Optimizer
product: journey optimizer
title: agendar uma campanha acionada por API
description: Saiba como agendar uma campanha acionada por API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: d3570e2c3d6340deaba8ca0f342161ab43ad1c43
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# Programar a campanha acionada pela API {#api-schedule}

Use a guia **[!UICONTROL Agendamento]** para definir o agendamento da campanha.

## Definir datas de início e término

Por padrão, as campanhas acionadas pela API começam assim que são acionadas e terminam assim que a mensagem é enviada uma vez. Se você não quiser executar sua campanha logo após ela ser acionada, poderá especificar uma data e hora em que a mensagem deverá ser enviada usando a opção **[!UICONTROL Início da campanha]**.

A opção **[!UICONTROL Campaign end]** permite especificar quando uma campanha deve parar de ser executada. Fora das datas especificadas, a campanha não será executada.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Ao agendar campanhas em [!DNL Adobe Journey Optimizer], verifique se a data/hora de início está alinhada com a primeira entrega desejada.

## Definir controle de taxa

[!DNL Journey Optimizer] permite habilitar o controle de taxa para ações de saída (email, SMS, notificações por push).

Esse recurso é particularmente útil para evitar sobrecarga em sistemas downstream, como páginas de aterrissagem ou plataformas de atendimento ao cliente. Por exemplo, você pode definir um limite de taxa de 165 mensagens por segundo para garantir uma entrega estável sem sobrecarregar os sistemas de downstream.

Para definir o controle de taxa, habilite a opção **[!UICONTROL Entrega acelerada]** na seção **[!UICONTROL Configurações de entrega]** e especifique a **[!UICONTROL Taxa de entrega]** desejada por segundo.

* Taxa de entrega mínima com suporte: 1 por segundo.
* Taxa de delivery máxima com suporte: 2000 por segundo quando a opção &quot;Throttle delivery&quot; está habilitada.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Ao definir uma taxa de delivery, o período máximo para o qual o público-alvo da campanha pode ser executado é de 12 horas. Se a taxa de delivery for definida com um valor que não permita que todo o público-alvo receba a mensagem no período de 12 horas, os perfis restantes serão excluídos da campanha. Você pode ver a contagem desses perfis excluídos no relatório da campanha.

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá revisá-los e ativá-los. [Saiba mais](../campaigns/review-activate-api-triggered-campaign.md)
