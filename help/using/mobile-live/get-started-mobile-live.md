---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à Atividade em tempo real
description: Saiba como enviar uma atividade em tempo real no Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 4f599e46c35bc328057247b84193a4db670fee83
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 21%

---

# Introdução à Atividade em tempo real {#get-started-mobile-live}


As atividades em tempo real são elementos de interface do usuário persistentes e visíveis, exibidos na tela de bloqueio do dispositivo. Eles permitem que seu aplicativo apresente informações atualizadas em tempo real, mantendo os usuários informados durante um evento contínuo, sem exigir que eles abram o aplicativo ou recebam notificações por push repetidas.

>[!AVAILABILITY]
>
>A atividade online no Adobe Journey Optimizer é compatível somente com o Apple iOS.

Diferentemente das notificações por push tradicionais, as Atividades ativas representam o **engajamento baseado em estado**: em vez de fornecer alertas únicos, elas mantêm uma presença contínua e contextual, atualizada dinamicamente à medida que os eventos evoluem.


![](assets/do-not-localize/live-activity.jpeg){width="50%" align="left"}

Com o Adobe Journey Optimizer, você pode **iniciar**, **atualizar** e **terminar** atividades online de forma remota e programática por meio de campanhas acionadas por API, oferecendo suporte a casos de uso individuais e baseados em público-alvo em escala.

A atividade online pode **ser iniciada somente** por meio de campanhas **acionadas por API**, permitindo que você forneça cargas personalizadas e execute toda a personalização por meio de sua própria carga.
O tipo de campanha **acionada por API** apropriado deve ser selecionado com base no caso de uso de atividade Online pretendido:

* Selecione **Marketing acionado por API** para casos de uso de difusão — atualizações baseadas em público enviadas em escala:

   * Pontuações esportivas e contagem regressiva de eventos ao vivo
   * Atualizações do estado do voo para todos os passageiros numa rota
   * Experiências compartilhadas em um segmento de usuário

* Selecione **Transacional acionado por API** para casos de uso individuais — 1:1 atualizações em tempo real por usuário:

   * Rastreamento de pedido e progresso de entrega
   * Atualizações de status de viagem ou serviço
   * Confirmações de agendamento e compromisso em tempo real

## Principais benefícios

As atividades online alteram o engajamento móvel de baseado em notificação para baseado em estado, permitindo que as marcas:

* Mantenha uma **presença contínua** na Tela de Bloqueio durante eventos de alto valor
* **Atualizar informações dinamicamente** sem sobrecarregar os usuários com notificações repetidas
* Entregue **momentos móveis mais ricos e contextuais** vinculados a eventos do mundo real
* **Aumentar o engajamento e a retenção** durante transações ativas ou experiências ativas

## Guia de início rápido

Conclua as etapas abaixo para configurar e implementar a atividade Live no seu aplicativo:

1. **[Configure o Adobe Journey Optimizer](mobile-live-configuration.md)**

   Defina o ambiente criando uma configuração de dispositivos móveis.

1. **[Integre o SDK para dispositivos móveis da Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Integre o SDK para dispositivos móveis da Adobe Experience Platform para habilitar atualizações dinâmicas e em tempo real na tela de bloqueio e na Dynamic Island.

1. **[Criar atividade online no Journey Optimizer](create-mobile-live.md)**

   Use campanhas acionadas por API no Journey Optimizer para iniciar sua atividade Live.

1. **[Monitorar suas campanhas](../reports/campaign-global-report-cja-activity.md)**

   Comece a medir o impacto da sua atividade Live com relatórios integrados.

## Vídeo tutorial

Descubra como configurar as atividades do iOS Live com o Adobe Journey Optimizer para fornecer atualizações avançadas em tempo real na Tela de bloqueio do iPhone e no Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479869/?captions=por_br&learn=on)
