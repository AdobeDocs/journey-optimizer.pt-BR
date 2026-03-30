---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às Atividades em tempo real
description: Saiba como enviar Atividades em tempo real no Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: c6b36f31af29d21053cc455fd5dbba68ed5af63b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---

# Introdução às Atividades em tempo real {#get-started-mobile-live}


As atividades em tempo real são elementos de interface persistentes e visíveis exibidos na tela de bloqueio do dispositivo. Eles permitem que seu aplicativo apresente informações atualizadas em tempo real, mantendo os usuários informados durante um evento contínuo, sem exigir que eles abram o aplicativo ou recebam notificações por push repetidas.

>[!AVAILABILITY]
>
>As atividades ativas no Adobe Journey Optimizer são compatíveis apenas com o Apple iOS.

Diferentemente das notificações por push tradicionais, as atividades online representam o **engajamento baseado em estado**: em vez de fornecer alertas únicos, elas mantêm uma presença contínua e contextual, atualizada dinamicamente à medida que os eventos evoluem.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Atividades do iOS Live na Lock Screen e na Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Principais benefícios</strong></p>
<p>As atividades online alteram o engajamento móvel de baseado em notificação para baseado em estado, permitindo que as marcas:</p>
<ul>
<li>Mantenha uma <strong>presença contínua</strong> na Tela de Bloqueio durante eventos de alto valor</li>
<li><strong>Atualizar informações dinamicamente</strong> sem sobrecarregar os usuários com notificações repetidas</li>
<li>Entregue <strong>momentos móveis mais ricos e contextuais</strong> vinculados a eventos do mundo real</li>
<li><strong>Aumentar o engajamento e a retenção</strong> durante transações ativas ou experiências ativas</li>
</ul>
</td>
</tr>
</table>

Com o Adobe Journey Optimizer, você pode **iniciar**, **atualizar** e **terminar** atividades online de forma remota e programática por meio de campanhas acionadas por API, oferecendo suporte a casos de uso individuais e baseados em público-alvo em escala.

As atividades online podem **apenas** ser iniciadas por meio de campanhas **acionadas por API**, permitindo que você forneça cargas personalizadas e execute toda a personalização por meio de sua própria carga.
O tipo de campanha **acionada por API** apropriado deve ser selecionado com base no caso de uso de atividade Online pretendido:

* Selecione **Marketing acionado por API** para casos de uso de difusão — atualizações baseadas em público enviadas em escala:

   * Pontuações esportivas e contagem regressiva de eventos ao vivo
   * Atualizações do estado do voo para todos os passageiros numa rota
   * Experiências compartilhadas em um segmento de usuário

* Selecione **Transacional acionado por API** para casos de uso individuais — 1:1 atualizações em tempo real por usuário:

   * Rastreamento de pedido e progresso de entrega
   * Atualizações de status de viagem ou serviço
   * Confirmações de agendamento e compromisso em tempo real

## Guia de início rápido

Conclua as etapas abaixo para configurar e implementar Atividades em tempo real no aplicativo:

1. **[Configure o Adobe Journey Optimizer](mobile-live-configuration.md)**

   Defina o ambiente criando uma configuração de dispositivos móveis.

1. **[Integre o SDK para dispositivos móveis da Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Integre o SDK para dispositivos móveis da Adobe Experience Platform para habilitar atualizações dinâmicas e em tempo real na tela de bloqueio e na Dynamic Island.

1. **[Criar uma atividade online no Journey Optimizer](create-mobile-live.md)**

   Use campanhas acionadas por API no Journey Optimizer para iniciar sua atividade Live.

1. **[Monitorar suas campanhas](../reports/campaign-global-report-cja-activity.md)**

   Comece a medir o impacto da sua atividade Live com relatórios integrados.

## Vídeo tutorial

Saiba como configurar as atividades do iOS Live com o Adobe Journey Optimizer para fornecer atualizações avançadas em tempo real na Tela de bloqueio do iPhone e no Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479869/?captions=por_br&learn=on)
