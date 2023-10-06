---
solution: Journey Optimizer
product: journey optimizer
title: Relatório em tempo real da campanha
description: Saiba como usar os dados do relatório Campaign live
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 4%

---

# Relatório em tempo real da campanha {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Relatório em tempo real da campanha"
>abstract="O Relatório em tempo real da campanha permite medir e visualizar em tempo real o impacto e o desempenho de suas campanhas nas últimas 24 horas. O relatório é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada painel de relatórios pode ser modificado redimensionando ou removendo widgets."

Os relatórios em tempo real, acessíveis a partir da guia Últimas 24 horas, exibem eventos que ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos a partir da ocorrência do evento. Em comparação, os Relatórios globais se concentram em eventos que ocorreram há pelo menos duas horas e abrangem eventos durante um período selecionado.

O relatório de campanha ao vivo pode ser acessado diretamente da sua campanha com o **[!UICONTROL Visualização em tempo real]** botão.

A campanha **[!UICONTROL Relatório ao vivo]** será exibida com as seguintes guias:

* [Campaign](#campaign-live)
* [Email](#email-live)
* [No aplicativo](#inapp-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Correspondência direta](#direct-mail-tab)

A campanha **[!UICONTROL Relatório ao vivo]** O é dividido em widgets diferentes detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/live-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## Guia Campanha {#campaign-live}

### Entrega {#delivery-live}

A variável **[!UICONTROL Estatísticas de campanha]** o widget detalha as principais informações relacionadas à sua campanha:

* **[!UICONTROL Perfis inseridos]**: Número de perfis que iniciaram a jornada.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Guia E-mail {#email-live}

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL E-mail]** A guia detalha as principais informações relativas aos deliveries de email enviados em sua campanha.

![](assets/campaign_report_live_1.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de email.

A variável **[!UICONTROL Estatísticas de envio de email]** o widget detalha as principais informações relacionadas à sua mensagem:

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

A variável **[!UICONTROL Métricas de envio por email]** tabela e **[!UICONTROL Resumo de email]** O gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um delivery.

* **[!UICONTROL Cancelar inscrição]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

A variável **[!UICONTROL Motivos de rejeição]**, **[!UICONTROL Categorias de rejeição]** e **[!UICONTROL Intensidade e rejeição - por email]** os widgets contêm os dados disponíveis relacionados às mensagens rejeitadas, como:

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

A variável **[!UICONTROL Motivos de erro]** e **[!UICONTROL Excluir motivos]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

A variável **[!UICONTROL Email - Principal domínio de destinatário]** O gráfico e a tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.
+++

## Guia No aplicativo {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Desempenho no aplicativo"
>abstract="Os KPIs de desempenho no aplicativo fornecem insights essenciais sobre o envolvimento dos visitantes com mensagens no aplicativo nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interações por tipo"
>abstract="Os gráficos de Interações por tipo e a tabela detalham como os usuários interagiram com sua mensagem no aplicativo rastreando qualquer clique, descarte ou interação nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Resumo no aplicativo"
>abstract="O gráfico de resumo no aplicativo ilustra o progresso de suas impressões e interações no aplicativo nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL No aplicativo]** A guia detalha as principais informações relativas aos deliveries no aplicativo enviados em sua campanha.

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório No aplicativo.

A variável **[!UICONTROL Desempenho no aplicativo]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as mensagens no aplicativo, como:

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.

A variável **[!UICONTROL Resumo no aplicativo]** O gráfico mostra a evolução de suas impressões e interações no aplicativo para o período relacionado.

A variável **[!UICONTROL Interações por tipo]** os gráficos e tabelas detalham como os usuários interagiram com a mensagem no aplicativo rastreando qualquer clique, descarte ou interação.

+++

## Guia Notificação por push {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Notificação por push - Desempenho de envio"
>abstract="O gráfico de Desempenho de envio de notificação por push resume dados essenciais sobre suas notificações por push, como Erros ou Mensagens entregues, das últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Notificação por push - Estatísticas"
>abstract="A tabela Estatísticas de push fornece dados sobre a atividade do recipient para seu delivery das últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Notificação por push - Resumo de envio"
>abstract="O gráfico Resumo do envio de notificações por push exibe os dados disponíveis para notificações por push enviadas nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Notificação por push - Motivos excluídos"
>abstract="Os gráficos e a tabela Motivos excluídos ilustram os vários fatores que levaram aos perfis de usuário, excluídos do público-alvo direcionado, a não receber a mensagem nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Notificação por push - Motivos de erro"
>abstract="Os gráficos e a tabela de Motivos de erro permitem identificar os erros específicos que ocorreram nas últimas 24 horas durante o delivery."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Notificação por push - Detalhamento por plataforma"
>abstract="Os gráficos e a tabela Detalhamento por plataforma fornecem uma análise do sucesso de suas notificações por push nas últimas 24 horas com base no sistema operacional do recipient."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Notificação por push]** A guia detalha as principais informações relativas aos deliveries por push enviados em sua campanha.

![](assets/campaign_report_live_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Push.

**[!UICONTROL Desempenho de envio de notificação por push]**, **[!UICONTROL Resumo da notificação por push]** e **[!UICONTROL Notificação por push - Estatísticas]** widgets detalha as principais informações relacionadas à sua mensagem:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Envolvimentos]**: Número total de aberturas e ações para esta notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

A variável **[!UICONTROL Motivos de erro]** e **[!UICONTROL Excluir motivos]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

A variável **[!UICONTROL Estatísticas de envio - Com falha]** permite ver quantos erros e devoluções ocorreram.

A variável **[!UICONTROL Rastreamento por plataforma]**, **[!UICONTROL Envio por plataforma]** e **[!UICONTROL Detalhamento por plataforma]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional.
+++

## Guia SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS - Estatísticas"
>abstract="A tabela Estatísticas de envio de SMS resume dados essenciais sobre suas mensagens SMS, como mensagens Segmentadas ou Entregues nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS - Desempenho por data"
>abstract="O widget Desempenho por data do SMS fornece informações importantes das últimas 24 horas sobre suas mensagens por meio de uma representação gráfica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS - Motivos de erro"
>abstract="Os gráficos e a tabela SMS - Error Reasons permitem identificar os erros específicos que ocorreram nas últimas 24 horas durante o delivery."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS - Motivos excluídos"
>abstract="Os gráficos e a tabela Motivos excluídos ilustram os vários fatores que levaram aos perfis de usuário, excluídos do público-alvo direcionado, a não receber a mensagem nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS - Motivos de rejeições"
>abstract="Os gráficos e a tabela de Motivos de rejeições contêm os dados disponíveis nas últimas 24 horas relacionadas às mensagens rejeitadas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL SMS]** A guia detalha as principais informações relativas aos deliveries de SMS enviados em sua campanha.

![](assets/campaign_report_live_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

A variável **[!UICONTROL SMS - Estatísticas]** a tabela detalha o sucesso do seu delivery:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Cliques]**: Número total de visitas a URL.

A variável **[!UICONTROL Desempenho do SMS por data]** o widget detalha as principais informações relacionadas à sua mensagem com um gráfico:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

A variável **[!UICONTROL Excluir motivos]**, **[!UICONTROL Motivos de rejeições]** e **[!UICONTROL Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++

## Guia Web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Desempenho da Web"
>abstract="Os KPIs de desempenho da Web fornecem informações abrangentes sobre o engajamento dos visitantes com as experiências da Web nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Resumo da Web"
>abstract="O gráfico Resumo da Web ilustra a progressão de suas experiências na Web, incluindo impressões, impressões exclusivas e interações, das últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interações por elemento"
>abstract="A tabela Interactions by Element fornece informações principais sobre o envolvimento dos visitantes com diferentes elementos em suas páginas da Web nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Web]** A guia detalha as informações principais relativas às páginas da Web.

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório da Web.

A variável **[!UICONTROL Desempenho da Web]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as experiências da Web, como:

* **[!UICONTROL Impressões]**: número total de experiências da web entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com sua página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

A variável **[!UICONTROL Resumo da Web]** o gráfico mostra a evolução de suas experiências da web (impressões, impressões exclusivas e interações) nas últimas 24 horas.

A variável **[!UICONTROL Interações por elemento]** A tabela detalha as principais informações relativas ao envolvimento dos visitantes com os vários elementos em suas páginas da web.
+++

## Guia Correspondência direta {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Correspondência direta - Estatísticas de envio"
>abstract="A tabela Estatísticas de envio de correspondência direta resume dados essenciais das últimas 24 horas sobre suas mensagens de correspondência direta, como mensagens direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Correspondência direta - Motivos de erro"
>abstract="Os gráficos e a tabela Mala direta - Motivos de erro permitem identificar os erros específicos ocorridos nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Correspondência direta - Motivos excluídos"
>abstract="Os gráficos e a tabela Motivos excluídos da correspondência direta ilustram os vários fatores que levaram aos perfis de usuário, excluídos do público-alvo direcionado, a não receber a mensagem nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Correspondência direta]** A guia detalha as principais informações relacionadas aos deliveries de correspondência direta.

![](assets/direct-mail-report_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de correspondência direta.

A variável **[!UICONTROL Correspondência direta - Estatísticas de envio]** a tabela detalha o sucesso do seu delivery:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para este delivery.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam o delivery.

A variável **[!UICONTROL Correspondência direta - Motivos excluídos]** e **[!UICONTROL Correspondência direta - Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.
+++

## Recursos adicionais

* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório global da campanha](campaign-global-report.md)
