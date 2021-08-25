---
title: Relatório global de email
description: Saiba como usar dados do relatório global de email
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 1%

---

# Relatório global de email {#email-global-report}

O email **[!UICONTROL Global report]** é direcionado apenas a um delivery de email específico.

Na guia **[!UICONTROL Executions]** do menu **[!UICONTROL Messages]**, selecione **[!UICONTROL Global view]** e, no menu avançado do delivery selecionado, selecione **[!UICONTROL Global report]**.

![](../assets/global_report_3.png)

O email **[!UICONTROL Global report]** é dividido em diferentes widgets detalhando o sucesso e os erros do delivery. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta [seção](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** detalha as informações principais relativas à sua mensagem com KPIs:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounce Rate]**: Porcentagem de emails que retornaram em comparação aos emails enviados.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação aos emails enviados.

* **[!UICONTROL Open Rate]**: Porcentagem de mensagens abertas.

* **[!UICONTROL Click Rate]**: Porcentagem de cliques em um delivery.

* **[!UICONTROL Spam Complaint Rate]**: Porcentagem de emails que foram marcados como spam por recipients em comparação às mensagens entregues. Para obter mais informações sobre reclamações, consulte o [Guia de Práticas Recomendadas de Deliverability](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Porcentagem de cancelamentos de subscrições exclusivas em comparação ao número de mensagens entregues. Esse indicador não depende do número de cliques no link de unsubscription, mas se baseia no número de unsubscriptions iniciadas pelos recipients. Saiba mais sobre unsubscriptions neste [page](../consent.md).

O **[!UICONTROL Email - Tracking statistics]** contém os dados disponíveis para a atividade do recipient para o seu delivery:

* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.

* **[!UICONTROL Unique Opens]**: Porcentagem de deliveries abertos.

* **[!UICONTROL Open Rate]**: Número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Click through rate]**: Porcentagem de usuários que interagiram com a jornada.

O gráfico **[!UICONTROL Sending Statistics]** detalha o sucesso do delivery:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

![](../assets/global_report_5.png)

Os widgets **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Hard bounce]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Soft bounce]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignored]**: O número total de temporários, como ausentes do escritório ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

Para obter mais informações sobre devoluções, consulte a página [Supressão list](../suppression-list.md).

O gráfico e a tabela **[!UICONTROL Error Reasons]** permitem ver qual erro ocorreu durante o delivery.

![](../assets/global_report_6.png)

O gráfico e a tabela **[!UICONTROL Email - Top recipient domain]** detalham quais domínios são os mais usados pelos recipients para abrir o email.

O gráfico e a tabela **[!UICONTROL Email - Top Url]** detalham quais URLs do delivery são os mais visitados.

O **[!UICONTROL Open vs Click]** identifica a interação dos recipients com o delivery:

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Unique Opens]**: Número de recipients que abriram o delivery.

>[!NOTE]
>
>Os perfis com status **[!UICONTROL Suppressed]** ou **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto os **Relatórios de Jornada** mostrarão esses perfis como tendo sido movidos pela jornada ([Ler segmento](../building-journeys/read-segment.md) e [Mensagem](../building-journeys/journeys-message.md) atividades), os **Relatórios de email** não os incluirão nas métricas **[!UICONTROL Sent]**, pois são filtrados antes do envio de email.
>
>Saiba mais sobre a [Lista de supressão](../suppression-list.md) e [Lista de permissões](../allow-list.md). Para descobrir o motivo de todos os casos de exclusão, você pode usar o [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.