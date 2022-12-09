---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar a execução da jornada
description: Saiba como iniciar sua jornada e enviar mensagens
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Execução da jornada {#message-execution}

## Testar sua jornada

Você pode testar sua jornada usando perfis de teste. Esta etapa é recomendada para validar suas configurações e mensagens.

Saiba mais nesta seção [seção](testing-the-journey.md).

## Ativar sua jornada

Você deve publicar sua jornada para ativá-la.

![](assets/jo-journeyuc2_32bis.png)

Saiba mais nesta seção [seção](publishing-the-journey.md).


Depois de publicada, você pode monitorar sua jornada usando as ferramentas de relatório dedicadas para medir a eficácia da jornada.

![](assets/jo-dynamic_report_journey_12.png)

[Saiba mais sobre relatórios](../reports/live-report.md)

## Enviar mensagens {#send-messages}

Quando a mensagem tiver um conteúdo definido, ela estará pronta para ser enviada por meio de um [jornada](journey.md).

Depois que uma mensagem é enviada, é possível monitorar a execução por meio de vários indicadores. [Saiba mais sobre Relatórios](../global-report.md).

## Programar mensagens {#schedule-messages}

As mensagens podem ser agendadas por meio do **[!UICONTROL Read Segment]** em uma [jornada](journey.md). Você pode especificar quando o segmento entrará na jornada. [Saiba mais sobre a atividade Ler segmento](read-segment.md).

Para fazer isso, siga as etapas abaixo:

1. Editar uma jornada, arrastar e soltar uma **[!UICONTROL Read Segment]** e comece a configurá-la. [Saiba mais sobre como configurar a atividade Ler segmento](read-segment.md#configuring-segment-trigger-activity).

1. Clique no botão **[!UICONTROL Edit journey schedule]** link para acessar as propriedades da jornada.

   ![](assets/message-read-segment-schedule.png)

1. Configure o **[!UICONTROL Scheduler type]** campo : selecione o valor desejado na lista para fazer com que o segmento entre na jornada em uma data/hora específica ou em uma base recorrente.

   >[!NOTE]
   >
   >O **[!UICONTROL Schedule]** só estará disponível quando uma **[!UICONTROL Read Segment]** foi colocada na tela.

   ![](assets/message-read-segment-scheduler.png)

1. Se você selecionar **[!UICONTROL Once]**, defina uma data e hora específicas em que o segmento entrará na jornada.

   ![](assets/message-read-segment-scheduler-once.png)

1. Se você selecionar um método recorrente, edite a data e a hora de início. Você também pode definir uma data e hora de término opcionais.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >Por padrão, os segmentos entram na jornada **[!UICONTROL As soon as possible]**, o que significa 1 hora após a publicação da jornada.

1. Clique em **[!UICONTROL OK]** para salvar as alterações.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
