---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com campanhas acionadas por API
description: Saiba como acionar campanhas usando APIs do Journey Optimizer.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d4765f9084efac1fd241404dff365a66027ce5af
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 60%

---


# Trabalhar com campanhas acionadas por API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campanhas acionadas por API"
>abstract="**Campanhas acionadas pela API transacional**<br/> Acionar mensagens em tempo real por meio de chamadas de API <br/><br/>**Mensagens de marketing**<br/> Conteúdo promocional (requer aceitação, sujeito às regras comerciais)<br/><br/>**Mensagens transacionais**<br/> Conteúdo relacionado a serviços (confirmação, alertas, não sujeito a consentimento de marketing)<br/><br/>**Canais disponíveis**<br/> Notificações por email, SMS, push"

## Sobre campanhas acionadas por API {#about}

Campanhas acionadas por API permitem que as comunicações de marketing alcancem um público-alvo na hora certa ou que mensagens transacionais/operacionais cheguem a uma pessoa, como uma redefinição de senha, em que a necessidade pode envolver personalização, não apenas usando o atributo de perfil, mas também os dados de contexto em tempo real no acionador, que é um conteúdo da API REST.

Para fazer isso, primeiro é necessário criar uma campanha acionada por API no Journey Optimizer e, em seguida, iniciar sua execução por meio de uma chamada de API usando a [API REST de Execução de Mensagem Interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

Os canais disponíveis para campanhas acionadas por API são mensagens de email, SMS e push.

➡️ [Conheça este recurso no vídeo](#video)


>[!NOTE]
>
>Os canais com suporte são: [Email](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [Notificações por push](../push/get-started-push.md).
>
>Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.

## Etapas principais para a criação de campanhas acionadas por API {#steps}

1. [Definir as propriedades da campanha](api-triggered-campaign-properties.md)
1. [Configurar a ação da campanha](api-triggered-campaign-action.md)
1. [Editar o conteúdo da campanha](api-triggered-campaign-content.md)
1. [Definir o público-alvo da campanha](api-triggered-campaign-audience.md)
1. [Agendar a campanha](api-triggered-campaign-schedule.md)
1. [Revisar e ativar a campanha](review-activate-api-triggered-campaign.md)
1. [Acionar a execução da campanha](trigger-campaigns.md)

>[!IMPORTANT]
>
>Antes de criar sua campanha, verifique se você revisou os [pré-requisitos gerais da campanha](../campaigns/get-started-with-campaigns.md#prerequisites).

## Vídeos tutoriais {#video}

Saiba como criar uma campanha e acioná-la a partir de um sistema externo com base em interações do usuário, usando a API REST de execução de mensagem interativa.

>[!VIDEO](https://video.tv.adobe.com/v/3452730?quality=12&captions=por_br)
