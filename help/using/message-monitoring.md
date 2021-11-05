---
title: Monitorar execução de mensagem
description: Saiba mais sobre as diretrizes de monitoramento
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 950f8186-07f6-4cc1-936c-d0984fb0f988
source-git-commit: f99471ce5bca7272a6f25339c2de1d5f21657088
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Monitoramento de mensagens {#monitor-message-execution}

Para garantir que suas mensagens sejam executadas, enviadas e entregues com êxito, [!DNL Journey Optimizer] O oferece recursos para monitorar as mensagens publicadas e acionadas no momento. Você pode ver o desempenho de suas mensagens em jornadas <!--and APIs--> em tempo real da **[!UICONTROL Executions]** lista.

Para acessar essa lista, no **[!DNL Journey Optimizer]** página inicial, selecione **[!UICONTROL Messages]** e clique no botão **[!UICONTROL Executions]** guia .

Esta guia fornece duas exibições: **[!UICONTROL Live view]** e **[!UICONTROL Global view]**.

* O **[!UICONTROL Live view]** A guia fornece um **visão geral em tempo real de todas as mensagens executadas** acionado por um ou mais [jornada](building-journeys/journey.md) **apenas nas últimas 24 horas**.

   ![](assets/message-execution-tab-live.png)

   Essa lista é atualizada automaticamente a cada sessenta segundos. Se nenhuma execução tiver ocorrido nas últimas 24 horas para uma mensagem específica, todas as colunas exibirão valores nulos (0) para essa mensagem.

* O **[!UICONTROL Global view]** A guia fornece uma **visão geral de todas as mensagens executadas** acionado por um ou mais [jornada](building-journeys/journey.md) **desde a data de início da mensagem**.

   ![](assets/message-execution-tab-global.png)

   Esta lista é atualizada automaticamente a cada noventa minutos. Os dados são agregados ao longo do tempo desde cada data de início da mensagem.

Se uma mensagem for publicada, mas ainda não for acionada por uma jornada, ela não estará listada em nenhuma das guias. Somente os seguintes elementos são listados:
* Mensagens que foram acionadas, mas que ainda não foram iniciadas (pendentes).
* Mensagens que foram acionadas e que estão em execução no momento (em andamento).

<!--For multichannel messages, one row per channel is displayed for each message. STILL VALID? looks like NOT-->

>[!NOTE]
>
>Se uma mensagem tiver sido usada em várias jornadas, uma linha por jornada será exibida para cada execução.

<!--![](assets/message-execution-multichannel.png)-->

<!--If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.-->

Por padrão, as mensagens são exibidas a partir da data de execução mais recente. Clique no botão **[!UICONTROL Filters]** ícone para pesquisar as mensagens de acordo com o canal, a data de início e/ou a data de término.

![](assets/message-execution-tab-filters.png)

O <!--**[!UICONTROL Quick action]**-->a segunda coluna permite abrir a correspondente [message](create-message.md) e para acessar o [Relatório ao vivo](reports/live-report.md) se você estiver no **[!UICONTROL Live view]** ou o [Relatório Global](reports/global-report.md) se você estiver no **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Para cada execução de mensagem, vários indicadores são exibidos:

* **[!UICONTROL Message label]**: Título de mensagem definido em [criação da mensagem](create-message.md). A ID de execução, que é gerada automaticamente, é exibida entre parênteses.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: Nome da jornada que utiliza a mensagem, a versão da jornada e o rótulo da ação que utiliza a mensagem na jornada.

* **[!UICONTROL Status]**: Status de execução da mensagem. <!--List all the possible statuses? For now only Live status? The user cannot stop or cancel the execution. TBC by Fred-->

* **[!UICONTROL Start date]**: Data e hora em que a mensagem foi executada a partir da jornada.

* **[!UICONTROL Targeted]**: Número de perfis segmentados para cada execução de mensagem.

* **[!UICONTROL Excluded]**: Número de perfis que foram excluídos do público-alvo inicial devido às regras de exclusão.

* **[!UICONTROL Sent]**: Número de mensagens enviadas.

* **[!UICONTROL Delivered]**: Número de mensagens entregues com êxito na caixa de correio do recipient (email) ou no dispositivo (push) sem gerar uma devolução ou qualquer outro erro de delivery.

* **[!UICONTROL Bounces]**: Número de mensagens que não podem ser entregues devido a uma falha de delivery. [Saiba mais sobre devoluções](suppression-list.md).

* **[!UICONTROL Opens]**: Número de mensagens que foram abertas.

* **[!UICONTROL Clicks]**: Número de cliques nos links em um email.

   >[!NOTE]
   >
   >Os cliques não existem para notificações por push: quando um usuário clica em uma notificação por push, ele abre o aplicativo, que só pode ser considerado como uma abertura.

* **[!UICONTROL Errors]**: Número de mensagens que não podem ser enviadas devido a uma falha técnica.

* **[!UICONTROL Spam complaints]**: Número de mensagens que foram marcadas como spam por recipients. Saiba mais sobre reclamações na [Guia de práticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

Você pode escolher quais colunas exibir na tabela. Para fazer isso, clique no botão **[!UICONTROL Customize table]** na parte superior da tela e selecione as colunas que deseja mostrar.

![](assets/message-execution-customize-table.png)

Em **Exibição global** somente é possível escolher se deseja exibir os dados como números, porcentagens ou ambos. Clique no botão **Formato dos dados** lista suspensa para alternar entre as três opções.

![](assets/message-execution-data-format.png)

Clicar em cada hiperlink abrirá a exibição de resumo de mensagem correspondente. [Saiba mais sobre mensagens](create-message.md).
