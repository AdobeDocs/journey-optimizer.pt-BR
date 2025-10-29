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
source-git-commit: afac93abcd2bacc4371748b94c0e66942a4c5076
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 35%

---


# Trabalhar com campanhas acionadas por API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campanhas acionadas por API"
>abstract="**Campanhas acionadas pela API transacional**<br/> Acionar mensagens em tempo real por meio de chamadas de API <br/><br/>**Mensagens de marketing**<br/> Conteúdo promocional (requer aceitação, sujeito às regras comerciais)<br/><br/>**Mensagens transacionais**<br/> Conteúdo relacionado a serviços (confirmação, alertas, não sujeito a consentimento de marketing)<br/><br/>**Canais disponíveis**<br/> Notificações por email, SMS, push"

## Sobre campanhas acionadas por API {#about}

As campanhas acionadas por API permitem que as comunicações de marketing alcancem um público-alvo na hora certa ou que mensagens transacionais/operacionais sejam enviadas a um indivíduo, como uma redefinição de senha, em que a necessidade pode envolver a personalização, não apenas usando atributos de perfil, mas também dados de contexto em tempo real no acionador, que é uma carga de API REST.

Para fazer isso, primeiro é necessário criar uma campanha acionada por API no Journey Optimizer e, em seguida, iniciar sua execução por meio de uma chamada de API usando a [API REST de Execução de Mensagem Interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

➡️ [Conheça este recurso no vídeo](#video)

>[!NOTE]
>
>Para obter mais informações sobre os canais com suporte, consulte a tabela nesta seção: [Canais em jornadas e campanhas](../channels/gs-channels.md#channels).
>
>Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.

## Etapas principais para a criação de campanhas acionadas por API {#steps}

Antes de começar com campanhas, verifique os seguintes pré-requisitos listados [nesta seção](get-started-with-campaigns.md#permissions). Depois que esses pré-requisitos forem atendidos, você poderá começar a criar sua campanha:

1. [Definir as propriedades da campanha](api-triggered-campaign-properties.md)
1. [Configurar a ação da campanha](api-triggered-campaign-action.md)
1. [Editar o conteúdo da campanha](api-triggered-campaign-content.md)
1. [Definir o público-alvo da campanha](api-triggered-campaign-audience.md)
1. [Agendar a campanha](api-triggered-campaign-schedule.md)
1. [Revisar e ativar a campanha](review-activate-api-triggered-campaign.md)
1. [Acionar a execução da campanha](trigger-campaigns.md)

## Vídeos tutoriais {#video}

Saiba como criar uma campanha e acioná-la a partir de um sistema externo com base em interações do usuário, usando a API REST de execução de mensagem interativa.

>[!VIDEO](https://video.tv.adobe.com/v/3452730?captions=por_br&quality=12)
