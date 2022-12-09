---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global de jornada
description: Saiba como usar dados do relatório global de jornada
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 0%

---

# Relatório global de jornada {#journey-global-report}

O relatório global de jornada pode ser acessado diretamente da sua jornada com o **[!UICONTROL View report]** botão.

![](assets/report_journey.png)

A jornada **[!UICONTROL Global report]** será exibida com as seguintes guias:

* [Jornada](#journey-global)
* [Email](#email-global)
* [Empurrar](#push-global)
* [SMS](#sms-global)

A jornada **[!UICONTROL Global report]** O é dividido em diferentes widgets detalhando o sucesso e os erros da jornada. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Otimizer, consulte [esta página](global-report.md#list-of-components-global).

## Guia Jornada {#journey-global}

Da sua jornada **[!UICONTROL Global report]**, o **[!UICONTROL Journey]** A guia fornece uma exibição clara dos dados de rastreamento mais importantes sobre sua jornada.

![](assets/journey_global_1.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de jornada.

O **[!UICONTROL Journey Performance]** O widget permite ver o caminho dos perfis segmentados passo a passo na jornada.

O **[!UICONTROL Journey Statistics]** O widget exibe os seguintes KPIs:

* **[!UICONTROL Entered profiles]**: Número total de indivíduos que chegaram ao evento de entrada da jornada.

* **[!UICONTROL Exited profiles]**: Número total de indivíduos que saíram da jornada.

* **[!UICONTROL Failed individual journey]**: Número total de jornadas individuais que não foram executadas com êxito.

O **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** e **[!UICONTROL Top events]** os widgets permitem ver qual de seus **[!UICONTROL Events]** foi executado com êxito por meio de gráficos e tabelas.

**[!UICONTROL Action Performance]**, **[!UICONTROL Action Error Reasons]** e **[!UICONTROL Top Actions]** os widgets representam a ação e os erros mais bem-sucedidos que ocorreram quando seu **[!UICONTROL Actions]** foram acionados.

O **[!UICONTROL Top Actions]** contém os dados disponíveis para **[!UICONTROL Actions]**, como:

* **[!UICONTROL Actions successfully executed]**: Número total de **[!UICONTROL Actions]** executado com êxito para uma jornada.

* **[!UICONTROL Error in action]**: Número total de erros que ocorreram **[!UICONTROL Actions]**.

O **[!UICONTROL Consent policies]** tabela e gráfico exibem o número de perfis excluídos de cada política em suas ações personalizadas.
Para obter mais informações sobre ações personalizadas, consulte [documentação detalhada](../action/about-custom-action-configuration.md).

Observe que para que esses widgets apareçam em seus relatórios de jornadas, será necessário redefinir seus painéis. Para fazer isso, clique em **[!UICONTROL Modify]** then **[!UICONTROL Reset]** na parte superior do relatório.
+++

## Guia Email {#email-global}

Da sua jornada **[!UICONTROL Global report]**, o **[!UICONTROL Email]** detalha as informações principais relativas aos deliveries de email enviados em sua jornada.

![](assets/journey_global_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de email.

O **[!UICONTROL Email Sending Statistics]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Targeted]**: Número de perfis segmentados pelo Adobe Journey Orchestration para qualquer ação, como enviar email ou SMS.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounce Rate]**: Porcentagem de emails que retornaram em comparação aos emails enviados.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação aos emails enviados.

O **[!UICONTROL Email - Tracking statistics]** contém os dados disponíveis para a atividade do recipient para o delivery:

* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.

* **[!UICONTROL Unique Opens]**: Porcentagem de deliveries abertos.

* **[!UICONTROL Unique Open Rate]**: Número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Unique Clicks]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Click through rate]**: Porcentagem de usuários que interagiram com a jornada.

* **[!UICONTROL Unsubscribe]**: Número de cliques no link unsubscription.

* **[!UICONTROL Spam complaints]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

O **[!UICONTROL Sending Statistics]** O gráfico contém os dados disponíveis para emails enviados, como:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

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
>O **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  os widgets só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

O **[!UICONTROL Optimized vs non optimized]** O gráfico detalha as informações principais relativas à sua mensagem, sejam elas otimizadas ou não:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.
* **[!UICONTROL Opens]**: Número de vezes que o delivery foi aberto em um delivery.
* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um email.

O **[!UICONTROL Send time optimization]** detalha o sucesso do delivery, dependendo do método de envio: otimizado ou normal.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

>[!NOTE]
>
>Os widgets e métricas de Ofertas só estarão disponíveis se uma decisão tiver sido inserida em um email. Para obter mais informações sobre o Gerenciamento de decisões, consulte esta seção [página](../offers/get-started/starting-offer-decisioning.md).

O **[!UICONTROL Offers statistic]** e **[!UICONTROL Offers statistics]** com o passar do tempo, os widgets avaliam o sucesso e o impacto da oferta no público-alvo. Ela detalha as informações principais relativas à sua mensagem com KPIs:

* **[!UICONTROL Offer sent]**: Número total de envios para a oferta.

* **[!UICONTROL Offer impression]**: Número de vezes que a oferta foi aberta em um delivery.

* **[!UICONTROL Offer clicks]**: Número de vezes que uma oferta foi clicada em um delivery.

O **[!UICONTROL Offers detailed statistic]** A tabela contém os dados disponíveis para a atividade do recipient com a oferta:

* **[!UICONTROL Placement name]**: Nome da disposição usada para exibir sua oferta. Para obter mais informações sobre posicionamento, consulte esta seção [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Nome da oferta adicionada ao delivery. Para obter mais informações sobre posicionamento, consulte esta seção [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Número total de envios para a oferta.

* **[!UICONTROL Offer impression rate]**: Porcentagem de ofertas abertas em comparação ao número de ofertas enviadas.

* **[!UICONTROL Offer click rate]**: Porcentagem de usuários que interagiram com a oferta.
+++

## Guia Notificação por push {#push-global}

Da sua jornada **[!UICONTROL Global report]**, o **[!UICONTROL Push notification]** detalha as informações principais relativas às entregas por push enviadas em sua jornada.

![](assets/journey_global_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de push.

O **[!UICONTROL Push notification - Sending statistics]** A tabela detalha as principais informações relativas às suas notificações por push com gráficos e KPIs:

* **[!UICONTROL Targeted]**: Número de perfis segmentados pelo Adobe Journey Orchestration para qualquer ação, como enviar email ou SMS.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Delivery Rate]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounce Rate]**: Porcentagem de notificações por push que rejeição em comparação às notificações por push enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Error Rate]**: Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação ao envio de notificações por push.

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
>O **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  os widgets só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

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

O SMS **[!UICONTROL Global report]** O é dividido em diferentes widgets detalhando o sucesso e os erros do delivery. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte [seção](global-report.md#modify-dashboard).
+++

## Guia SMS {#sms-global}

![](assets/journey_global_4.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

O **[!UICONTROL SMS - Sending statistics]** tabela detalha o sucesso do delivery:

* **[!UICONTROL Targeted]**: Número de perfis de usuário que se qualificaram como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluded]**: Número de perfis de usuário, excluídos dos perfis segmentados, que não receberam a mensagem.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL SMS summary]** o widget detalha as informações principais relativas à sua mensagem com um gráfico:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Exclude Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++
