---
title: Relatório global de email
description: Saiba como usar dados do relatório global de email
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 1%

---

# Relatório global de email {#email-global-report}

O email **[!UICONTROL Global report]** direciona somente um delivery de email específico.

No **[!UICONTROL Executions]** da guia **[!UICONTROL Messages]** selecione **[!UICONTROL Global view]** em seguida, no menu avançado do delivery selecionado, selecione **[!UICONTROL Global report]**.

![](assets/global_report_3.png)

O email **[!UICONTROL Global report]** O é dividido em diferentes widgets detalhando o sucesso e os erros do delivery. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte [seção](global-report.md#modify-dashboard).

![](assets/global_report_4.png)

**[!UICONTROL Email performance]** detalha as informações principais relativas à sua mensagem com KPIs:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounce Rate]**: Porcentagem de emails que retornaram em comparação aos emails enviados.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação aos emails enviados.

* **[!UICONTROL Open Rate]**: Porcentagem de mensagens abertas.

* **[!UICONTROL Click Rate]**: Porcentagem de cliques em um delivery.

* **[!UICONTROL Spam Complaint Rate]**: Porcentagem de emails que foram marcados como spam por recipients em comparação às mensagens entregues. Para obter mais informações sobre reclamações, consulte o [Guia de práticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Porcentagem de cancelamentos de subscrições exclusivas em comparação ao número de mensagens entregues. Esse indicador não depende do número de cliques no link de unsubscription, mas se baseia no número de unsubscriptions iniciadas pelos recipients. Saiba mais sobre unsubscriptions nesta seção [página](../messages/consent.md).

O **[!UICONTROL Email - Tracking statistics]** contém os dados disponíveis para a atividade do recipient para o delivery:

* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.

* **[!UICONTROL Unique Opens]**: Porcentagem de deliveries abertos.

* **[!UICONTROL Open Rate]**: Número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Click through rate]**: Porcentagem de usuários que interagiram com a jornada.

O **[!UICONTROL Sending Statistics]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

![](assets/global_report_5.png)

O **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** os widgets contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Hard bounce]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Soft bounce]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignored]**: O número total de temporários, como ausentes do escritório ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

Para obter mais informações sobre devoluções, consulte [Lista de supressão](../reports/suppression-list.md) página.

O **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

![](assets/global_report_6.png)

O **[!UICONTROL Email - Top recipient domain]** gráfico e tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.

O **[!UICONTROL Email - Top Url]** gráfico e tabela detalham quais URLs do seu delivery são os mais visitados.

O **[!UICONTROL Open vs Click]** identifica a interação dos recipients com o delivery:

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Unique Opens]**: Número de recipients que abriram o delivery.

<!--
![](assets/global_report_20.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.

The **[!UICONTROL Offers detailed statistic]** table contains the available data for recipient activity with your offer:

* **[!UICONTROL Placement name]**: Name of your placement used to display your offer. For more information on placement, refer to this [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Name of the offer added in the delivery. For more information on placement, refer to this [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression rate]**: Percentage of opened offers compared to the number of sent offers.

* **[!UICONTROL Offer click rate]**: Percentage of users who interacted with the offer.
-->
>[!NOTE]
>
>Os perfis com **[!UICONTROL Suppressed]** ou **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto a variável **Relatórios de Jornada** mostrará esses perfis como tendo sido movidos pela jornada ([Ler segmento](../building-journeys/read-segment.md) e [Mensagem](../building-journeys/journeys-message.md) atividades), **Relatórios de email** não os incluirá no **[!UICONTROL Sent]** métricas como são filtradas antes do envio do email.
>
>Saiba mais sobre o [Lista de supressão](../reports/suppression-list.md) e [Lista de permissões](allow-list.md). Para descobrir o motivo de todos os casos de exclusão, é possível usar a variável [Serviço de query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
