---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às Atividades em tempo real
description: Saiba como enviar Atividades em tempo real no Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 100%

---

# Introdução às Atividades em tempo real {#get-started-mobile-live}


As atividades em tempo real são elementos de interface persistentes e visíveis exibidos na tela de bloqueio do dispositivo. Elas permitem que seu aplicativo apresente informações atualizadas em tempo real, mantendo os usuários informados durante um evento contínuo, sem exigir que eles abram o aplicativo ou recebam notificações por push repetidas.

>[!AVAILABILITY]
>
>A Atividade em tempo real no Adobe Journey Optimizer é compatível somente com o Apple iOS.

Diferentemente das notificações por push tradicionais, as atividades em tempo real representam o **engajamento baseado em estado**: em vez de fornecer alertas únicos, elas mantêm uma presença contínua e contextual, atualizada dinamicamente à medida que os eventos evoluem.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Atividades em tempo real do iOS na Tela de bloqueio e no Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Principais benefícios</strong></p>
<p>As atividades em tempo real alteram o engajamento móvel de baseado em notificação para baseado em estado, permitindo que as marcas:</p>
<ul>
<li>Mantenham uma <strong>presença contínua</strong> na Tela de bloqueio durante eventos de alto valor</li>
<li><strong>Atualizem informações dinamicamente</strong> sem sobrecarregar os usuários com notificações repetidas</li>
<li>Entreguem <strong>momentos em dispositivos móveis mais relevantes e contextuais</strong> vinculados a eventos reais</li>
<li><strong>Aumentem o engajamento e a retenção</strong> durante transações ativas ou experiências em tempo real</li>
</ul>
</td>
</tr>
</table>

Com o Adobe Journey Optimizer, você pode **iniciar**, **atualizar** e **encerrar** atividades em tempo real de forma remota e programática por meio de campanhas acionadas por API, oferecendo suporte a casos de uso individuais e baseados em público-alvo em grande escala.

As atividades em tempo real podem ser iniciadas **apenas** por meio de campanhas **acionadas por API**, permitindo que você forneça conteúdos personalizados e realize toda a personalização por meio de seu próprio conteúdo.
O tipo de campanha **acionada por API** apropriado deve ser selecionado com base no caso de uso pretendido para a atividade em tempo real:

* Selecione **Marketing acionado por API** para casos de uso de transmissão: atualizações baseadas em público-alvo enviadas em grande escala:

   * Pontuações esportivas e contagem regressiva de eventos ao vivo
   * Atualizações sobre o status do voo para todos os passageiros em uma rota
   * Experiências compartilhadas em um segmento de usuário

* Selecione **Transacional acionado por API** para casos de uso individuais: 1:1 atualização em tempo real por usuário:

   * Rastreamento de pedido e progresso de entrega
   * Atualizações de status de viagem ou serviço
   * Confirmações de reservas e agendamentos em tempo real

## Guia de início rápido

Conclua as etapas abaixo para configurar e implementar Atividades em tempo real no aplicativo:

1. **[Configure o Adobe Journey Optimizer](mobile-live-configuration.md)**

   Defina o ambiente criando uma configuração de dispositivos móveis.

1. **[Integre o SDK para dispositivos móveis da Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Integre o SDK para dispositivos móveis da Adobe Experience Platform para habilitar atualizações dinâmicas e em tempo real na tela de bloqueio e na Dynamic Island.

1. **[Criar atividade em tempo real no Journey Optimizer](create-mobile-live.md)**

   Use campanhas acionadas por API no Journey Optimizer para iniciar uma atividade em tempo real.

1. **[Monitorar suas campanhas](../reports/campaign-global-report-cja-activity.md)**

   Comece medindo o impacto da atividade em tempo real com relatórios integrados.

## Vídeo tutorial

Descubra como configurar as atividades em tempo real do iOS com o Adobe Journey Optimizer para fornecer atualizações avançadas em tempo real na Tela de bloqueio do iPhone e no Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
