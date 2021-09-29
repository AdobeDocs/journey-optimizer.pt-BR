---
title: Relatório ao vivo por email
description: Saiba como usar dados do relatório ao vivo do email
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: d814fa98a08d91f1c0744f106c53dd991d544dc2
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---

# Relatório ao vivo por email {#email-live-report}

O email **[!UICONTROL Live report]** é direcionado apenas a um delivery de email específico.

Na guia **[!UICONTROL Executions]** do menu **[!UICONTROL Messages]**, selecione **[!UICONTROL Live view]** e, no menu avançado do delivery selecionado, selecione **[!UICONTROL Live report]**.

![](../assets/live_report.png)

O email **[!UICONTROL Live report]** é dividido em diferentes widgets detalhando o sucesso e os erros do delivery. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta [seção](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** Os  **[!UICONTROL Email summary]** widgets e detalham as informações principais relativas à sua mensagem com um gráfico e KPIs:

* **[!UICONTROL Targeted]**: Número de perfis de usuário que se qualificaram como perfis de público-alvo para este delivery.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um delivery.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Spam complaints]**: Número de mensagens classificadas como spam.

* **[!UICONTROL Unsubscriptions]**: Número de cliques no link unsubscription.

* **[!UICONTROL Excluded]**: Número de perfis de usuário, excluídos dos perfis segmentados, que não receberam a mensagem.

O widget **[!UICONTROL Sending Statistics]** detalha o sucesso do delivery:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

![](../assets/live_report_6.png)

O gráfico e a tabela **[!UICONTROL Error Reasons]** permitem ver qual erro ocorreu durante o delivery.

Os widgets **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Hard bounce]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Soft bounce]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignored]**: O número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

>[!NOTE]
>
>Os perfis com status **[!UICONTROL Suppressed]** ou **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto os **Relatórios de Jornada** mostrarão esses perfis como tendo sido movidos pela jornada ([Ler segmento](../building-journeys/read-segment.md) e [Mensagem](../building-journeys/journeys-message.md) atividades), os **Relatórios de email** não os incluirão nas métricas **[!UICONTROL Sent]**, pois são filtrados antes do envio de email.
>
>Saiba mais sobre a [Lista de supressão](../suppression-list.md) e [Lista de permissões](../allow-list.md). Para descobrir o motivo de todos os casos de exclusão, você pode usar o [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
