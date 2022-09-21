---
title: Relatório em tempo real da campanha
description: Saiba como usar dados do relatório ao vivo do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 3%

---

# Relatório em tempo real da campanha {#campaign-live-report}

O relatório ao vivo da campanha pode ser acessado diretamente da sua campanha com o **[!UICONTROL Exibição ao vivo]** botão.

A campanha **[!UICONTROL Relatório ao vivo]** será exibida com as seguintes guias:

* [Campaign](#campaign-live)
* [Email](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)


A campanha **[!UICONTROL Relatório ao vivo]** O é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/live-report.md#modify-dashboard).

Para obter uma lista detalhada de todas as métricas disponíveis no Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## Guia Campaign {#campaign-global}

### Entrega {#delivery-global}

O **[!UICONTROL Estatísticas de campanha]** o widget detalha as informações principais relativas à sua campanha:

* **[!UICONTROL Perfis inseridos]**: Número de perfis que iniciaram a jornada.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## Guia Email {#email-live}

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Email]** detalha as informações principais relativas aos deliveries de email enviados na campanha.

![](assets/campaign_report_live_1.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de email.

O **[!UICONTROL Email Sending Statistics]** o widget detalha as informações principais relativas à sua mensagem:

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Envio de métricas por email]** tabela e **[!UICONTROL Resumo do email]** gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Abre]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um delivery.

* **[!UICONTROL Cancelar inscrição]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

O **[!UICONTROL Motivos da rejeição]**, **[!UICONTROL Categorias de rejeição]** e **[!UICONTROL Resíduo e devolução - por email]** os widgets contêm os dados disponíveis relacionados às mensagens devolvidas, como:

* **[!UICONTROL Rejeição permanente]**: O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.

* **[!UICONTROL Rejeição suave]**: O número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: O número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

O **[!UICONTROL Motivos do erro]** e **[!UICONTROL Excluir motivos]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

O **[!UICONTROL Email - Domínio do recipient principal]** gráfico e tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.
+++

## Guia Notificação por push {#push-live}

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Notificação por push]** detalha as informações principais relativas aos deliveries por push enviados na campanha.

![](assets/campaign_report_live_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de push.

**[!UICONTROL Desempenho de envio de notificação por push]**, **[!UICONTROL Resumo da notificação por push]** e **[!UICONTROL Enviar métricas - por push]** os widgets detalham as informações principais relativas à sua mensagem:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Abre]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.

* **[!UICONTROL Envolvimentos]**: Número total de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

O **[!UICONTROL Motivos do erro]** e **[!UICONTROL Excluir motivos]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

O **[!UICONTROL Envio de estatísticas - Falha]** permite ver quantos erros e rejeições ocorreram.

O **[!UICONTROL Rastreamento por plataforma]**, **[!UICONTROL Envio por plataforma]** e **[!UICONTROL Detalhamento por plataforma]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional.
+++

## Guia SMS {#sms-live}

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL SMS]** detalha as informações principais relativas aos deliveries de SMS enviados na campanha.

![](assets/campaign_report_live_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

O **[!UICONTROL SMS - Envio de estatísticas]** tabela detalha o sucesso do delivery:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificaram como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis segmentados, que não receberam a mensagem.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Desempenho do SMS por data]** o widget detalha as informações principais relativas à sua mensagem com um gráfico:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o delivery e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.

O **[!UICONTROL Excluir motivos]**, **[!UICONTROL Motivos das rejeições]** e **[!UICONTROL Motivos do erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++

## Recursos adicionais

* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório global da campanha](campaign-global-report.md)
