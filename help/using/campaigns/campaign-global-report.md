---
title: Relatório global da campanha
description: Saiba como usar dados do relatório global de campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 4%

---

# Relatório global da campanha {#campaign-global-report}

O relatório global da campanha pode ser acessado diretamente da sua campanha com o **[!UICONTROL Global view]** botão.

A campanha **[!UICONTROL Global report]** será exibida com as seguintes guias:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [Push](#push-global)

A campanha **[!UICONTROL Global report]** O é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/global-report.md#modify-dashboard).

## Guia Campaign {#campaign-global}

### Entrega {#delivery-global}

![](assets/campaign_report_global_1.png)

O **[!UICONTROL Campaign's Statistics]** o widget detalha as informações principais relativas à sua campanha:

* **[!UICONTROL Entered profiles]**: Número de perfis que iniciaram a jornada.

* **[!UICONTROL Actions delivered]**: Número total de vezes únicas que uma ação na jornada foi entregue.

* **[!UICONTROL Actions failed in %]**: Número total de vezes exclusivas que uma ação falhou na jornada em comparação ao número total de vezes exclusivas que uma ação foi entregue.

<!--
### Experimentation tab (#experimentation-global)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Guia Email {#email-global}

Da sua campanha **[!UICONTROL Global report]**, o **[!UICONTROL Email]** detalha as informações principais relativas aos deliveries de email enviados no Campaign.

O **[!UICONTROL Email Sending Statistics]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Targeted]**: Número total de mensagens processadas durante a análise de delivery.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounce Rate]**: Porcentagem de emails que retornaram em comparação aos emails enviados.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação aos emails enviados.

* **[!UICONTROL Retries]**: Número de emails na fila para novas tentativas.

* **[!UICONTROL Excluded]**: Número de perfis que foram excluídos pelo Adobe Journey Optimizer.

O **[!UICONTROL Email - Tracking statistics]** contém os dados disponíveis para a atividade do recipient para o delivery:

* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.

* **[!UICONTROL Unique Opens]**: Porcentagem de deliveries abertos.

* **[!UICONTROL Open Rate]**: Número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Unique Click Rate]**: Porcentagem de usuários que interagiram com o delivery.

* **[!UICONTROL Unsubscriptions]**: Número de cliques no link unsubscription.

* **[!UICONTROL Spam complaints]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

O **[!UICONTROL Sending Statistics]** O gráfico contém os dados disponíveis para emails enviados, como:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Retries]**: Número de emails na fila para novas tentativas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** os widgets contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Hard bounce]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Soft bounce]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignored]**: O número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

Para obter mais informações sobre devoluções, consulte [Lista de supressão](../reports/suppression-list.md) página.

O **[!UICONTROL Error Reasons]** gráfico e tabela permitem ver qual erro ocorreu durante o delivery.

O **[!UICONTROL Excluded reasons]** gráfico e tabela exibem os diferentes motivos que impediam os perfis de usuário, excluídos dos perfis segmentados, de receber a mensagem.

O **[!UICONTROL Email - Top Url]** gráfico e tabela detalham quais URLs do seu delivery são os mais visitados.

O **[!UICONTROL Email - Top recipient domain]** gráfico e tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.

>[!NOTE]
>
>O **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  os widgets só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre Otimização de tempo de envio, consulte [esta página](../messages/send-time-optimization.md).

O **[!UICONTROL Optimized vs non optimized]** O gráfico detalha as informações principais relativas à sua mensagem, sejam elas otimizadas ou não:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.
* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.
* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

O **[!UICONTROL Send time optimization]** detalha o sucesso do delivery, dependendo do método de envio: otimizado ou normal.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

## Guia Empurrar {#push-global}

Da sua campanha **[!UICONTROL Global report]**, o **[!UICONTROL Push]** detalha as informações principais relativas aos deliveries por push enviados na campanha.

O **[!UICONTROL Push notification - Sending statistics]** A tabela detalha as principais informações relativas às suas notificações por push com gráficos e KPIs:

* **[!UICONTROL Targeted]**: Número total de mensagens processadas durante a análise de delivery.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounce Rate]**: Porcentagem de notificações por push que rejeição em comparação às notificações por push enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação ao envio de notificações por push.

* **[!UICONTROL Excluded]**: Número de perfis que foram excluídos pelo Adobe Journey Optimizer.

O **[!UICONTROL Push - Tracking statistics]** contém os dados disponíveis para a atividade do recipient para o delivery:

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Open Rate]**: Porcentagem de notificações por push abertas.

* **[!UICONTROL Actions]**: Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.

* **[!UICONTROL Engagements]**: Número total de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

* **[!UICONTROL Engagement Rate]**: Porcentagem de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

O **[!UICONTROL Push notification summary]** O gráfico contém os dados disponíveis para notificações por push enviadas, como:

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Actions]**: Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

>[!NOTE]
>
>O **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  os widgets só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre Otimização de tempo de envio, consulte [esta página](../messages/send-time-optimization.md).

O **[!UICONTROL Optimized vs non optimized]** O gráfico detalha as informações principais relativas à sua mensagem, sejam elas otimizadas ou não:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.
* **[!UICONTROL Actions]**: Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.

O **[!UICONTROL Send time optimization]** detalha o sucesso do delivery, dependendo do método de envio: otimizado ou normal.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

O **[!UICONTROL Error Reasons]** gráfico e tabela permitem ver qual erro ocorreu durante o delivery.

O **[!UICONTROL Excluded reasons]** gráfico e tabela exibem os diferentes motivos que impediam os perfis de usuário, excluídos dos perfis segmentados, de receber a mensagem.

O **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** os gráficos e tabelas detalham o sucesso da notificação por push, dependendo do sistema operacional do recipient.

## Recursos adicionais

* [Introdução às campanhas](get-started-with-campaigns.md)
* [Criar uma campanha](create-campaign.md)
* [Criar campanhas acionadas por API](api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](modify-stop-campaign.md)
* [Relatório em tempo real da campanha](campaign-live-report.md)
