---
solution: Journey Optimizer
product: journey optimizer
title: Relatório ao vivo da jornada
description: Saiba como usar dados do relatório ao vivo da jornada
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Relatório ao vivo da jornada {#journey-live-report}

O relatório de jornada ao vivo pode ser acessado diretamente da sua jornada com o **[!UICONTROL View report]** botão.

![](assets/report_journey.png)

A jornada **[!UICONTROL Live report]** será exibida com as seguintes guias:

* [Jornada](#journey-live)
* [Email](#email-live)
* [Empurrar](#push-live)
* [SMS](#sms-live)

A jornada **[!UICONTROL Live report]** O é dividido em diferentes widgets detalhando o sucesso e os erros da jornada. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](live-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Otimizer, consulte [esta página](live-report.md#list-of-components-live).

## Guia Jornada {#journey-live}

Da sua jornada **[!UICONTROL Live report]**, o **[!UICONTROL Journey]** A guia fornece uma exibição clara dos dados de rastreamento mais importantes sobre sua jornada.

![](assets/journey_live_1.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de jornada.

**[!UICONTROL Journey Performance]** O permite ver o caminho dos perfis segmentados passo a passo pela jornada.

O **[!UICONTROL Journey Statistics]** O widget exibe os seguintes KPIs:

* **[!UICONTROL Entered profiles]**: Número total de indivíduos que chegaram ao evento de entrada da jornada.

* **[!UICONTROL Exited profiles]**: Número total de indivíduos que saíram da jornada.

* **[!UICONTROL Failed individual journeys]**: Número total de jornadas individuais que não foram executadas com êxito.

O **[!UICONTROL Event executed over the last 24 hours]** e **[!UICONTROL Events]** os widgets permitem ver qual dos seus eventos foi executado com êxito por meio do número do resumo, gráfico e tabela.

O **[!UICONTROL Action executed over the last 24 hours]** e **[!UICONTROL Actions executed and errors]** os widgets representam a ação e os erros mais bem-sucedidos que ocorreram quando suas ações foram acionadas. O gráfico de Ação, a tabela e os números de resumo contêm os dados disponíveis para ações, como:

* **[!UICONTROL Actions executed]**: Número total de ações executadas com êxito para uma jornada.

* **[!UICONTROL Error in actions]**: Número total de erros que ocorreram para ações.
+++

## Guia Email {#email-live}

Da sua jornada **[!UICONTROL Live report]**, o **[!UICONTROL Email]** detalha as informações principais relativas aos deliveries de email enviados em sua jornada.

![](assets/journey_live_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de email.

O **[!UICONTROL Email Sending Statistics]** o widget detalha as informações principais relativas à sua mensagem:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Sending metrics by Email]** tabela e **[!UICONTROL Email Summary]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um delivery.

* **[!UICONTROL Unsubscribe]**: Número de cliques no link unsubscription.

* **[!UICONTROL Spam complaints]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

O **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** e **[!UICONTROL Hard and bounce - by Email]** os widgets contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Hard bounce]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Soft bounce]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignored]**: O número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

O **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

O **[!UICONTROL Email - Top recipient domain]** gráfico e tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.

>[!NOTE]
>
>Os widgets e métricas de Ofertas só estarão disponíveis se uma decisão tiver sido inserida em um email. Para obter mais informações sobre o Gerenciamento de decisões, consulte esta seção [página](../offers/get-started/starting-offer-decisioning.md).

O **[!UICONTROL Offers statistic]** e **[!UICONTROL Offers statistics]** com o passar do tempo, os widgets avaliam o sucesso e o impacto da oferta no público-alvo. Ela detalha as informações principais relativas à sua mensagem com KPIs:

* **[!UICONTROL Offer sent]**: Número total de envios para a oferta.

* **[!UICONTROL Offer impression]**: Número de vezes que a oferta foi aberta em um delivery.

* **[!UICONTROL Offer clicks]**: Número de vezes que uma oferta foi clicada em um delivery.
+++

## Guia Notificação por push {#push-live}

Da sua jornada **[!UICONTROL Live report]**, o **[!UICONTROL Push notification]** detalha as informações principais relativas às entregas por push enviadas em sua jornada.

![](assets/journey_live_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de push.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** e **[!UICONTROL Sending metrics - by Push]** os widgets detalham as informações principais relativas à sua mensagem:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Actions]**: Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.

* **[!UICONTROL Engagements]**: Número total de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

O **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

O **[!UICONTROL Sending statistics - Failed]** permite ver quantos erros e rejeições ocorreram.

O **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional.
+++

## Guia SMS {#sms-live}

![](assets/journey_live_4.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

O **[!UICONTROL SMS - Sending statistics]** tabela detalha o sucesso do delivery:

* **[!UICONTROL Targeted]**: Número de perfis de usuário que se qualificaram como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluded]**: Número de perfis de usuário, excluídos dos perfis segmentados, que não receberam a mensagem.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Opens]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Clicks]**: Número de vezes que um conteúdo foi clicado em um delivery.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL SMS Summary]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Exclude Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++
