---
solution: Journey Optimizer
product: journey optimizer
title: Relatório ao vivo da campanha
description: Saiba como usar dados do relatório ao vivo do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Relatório ao vivo da campanha {#campaign-live-report}

O relatório ao vivo da campanha pode ser acessado diretamente da sua campanha com o **[!UICONTROL Live view]** botão.

A campanha **[!UICONTROL Live report]** será exibida com as seguintes guias:

* [Campanha](#campaign-live)
* [Email](#email-live)
* [Empurrar](#push-live)
* [SMS](#sms-live)


A campanha **[!UICONTROL Live report]** O é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/live-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Otimizer, consulte [esta página](live-report.md#list-of-components-live).

## Guia Campaign {#campaign-global}

### Delivery {#delivery-global}

O **[!UICONTROL Campaign Statistics]** o widget detalha as informações principais relativas à sua campanha:

* **[!UICONTROL Entered profiles]**: Número de perfis que iniciaram a jornada.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Guia Email {#email-live}

Da sua campanha **[!UICONTROL Live report]**, o **[!UICONTROL Email]** detalha as informações principais relativas aos deliveries de email enviados na campanha.

![](assets/campaign_report_live_1.png)

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
+++

## Guia Notificação por push {#push-live}

Da sua campanha **[!UICONTROL Live report]**, o **[!UICONTROL Push notification]** detalha as informações principais relativas aos deliveries por push enviados na campanha.

![](assets/campaign_report_live_2.png)

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

Da sua campanha **[!UICONTROL Live report]**, o **[!UICONTROL SMS]** detalha as informações principais relativas aos deliveries de SMS enviados na campanha.

![](assets/campaign_report_live_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

O **[!UICONTROL SMS - Sending statistics]** tabela detalha o sucesso do delivery:

* **[!UICONTROL Targeted]**: Número de perfis de usuário que se qualificaram como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluded]**: Número de perfis de usuário, excluídos dos perfis segmentados, que não receberam a mensagem.

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL SMS Performance by date]** o widget detalha as informações principais relativas à sua mensagem com um gráfico:

* **[!UICONTROL Sent]**: Número total de envios para o delivery.

* **[!UICONTROL Delivered]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Bounces]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Errors]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** e **[!UICONTROL Error Reasons]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++

## Recursos adicionais

* [Introdução a campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou parar uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório global da campanha](campaign-global-report.md)
