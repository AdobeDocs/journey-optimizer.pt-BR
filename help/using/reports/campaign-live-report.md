---
solution: Journey Optimizer
product: journey optimizer
title: Relatório em tempo real da campanha
description: Saiba como usar os dados do relatório Campaign live
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 40%

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

## Guia Email {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="Email: estatísticas de envio"
>abstract="O gráfico “Email: estatísticas de envio” resume dados essenciais sobre o email, como se ele foi direcionado ou entregue nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="Email: estatísticas"
>abstract="A tabela “Email: estatísticas” fornece dados sobre a atividade de perfil do email nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="Email: categorias de rejeição"
>abstract="A tabela “Email: categorias de rejeição” e seus gráficos fornecem dados sobre erros temporários e permanentes nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="Email: desempenho por data"
>abstract="O gráfico “Email: desempenho por data” apresenta dados abrangentes das últimas 24 horas a respeito de emails enviados, oferecendo insights acerca de métricas principais, como entregas e rejeições, o que permite uma análise detalhada do processo de entrega de email."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="Email: motivos de rejeições"
>abstract="A tabela “Email: motivos de rejeições” e seus gráficos contêm dados relacionados às mensagens rejeitadas nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="Email: motivos de erro"
>abstract="A tabela “Email: motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="Email: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="Email: melhor domínio do destinatário"
>abstract="A tabela “Email: Melhor domínio do destinatário” e seu gráfico fornecem um detalhamento dos domínios que os destinatários usam com mais frequência para abrir o email, oferecendo insights valiosos sobre o comportamento do destinatário nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL E-mail]** A guia detalha as principais informações relacionadas ao email enviado em sua campanha.

![](assets/campaign_report_live_1.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de email.

A variável **[!UICONTROL Estatísticas de envio de email]** o widget detalha as principais informações relacionadas à sua mensagem:

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

A variável **[!UICONTROL Métricas de envio por email]** tabela e **[!UICONTROL Resumo de email]** o gráfico detalha o sucesso do seu email:

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado.

* **[!UICONTROL Cancelar inscrição]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

A variável **[!UICONTROL Motivos de rejeição]** e **[!UICONTROL Categorias de rejeição]** os widgets contêm os dados disponíveis relacionados às mensagens rejeitadas, como:

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

A variável **[!UICONTROL Motivos de erro]** e **[!UICONTROL Excluir motivos]** os gráficos e as tabelas permitem ver quais erros e exclusões ocorreram durante o processo de envio.

A variável **[!UICONTROL Email - Melhor domínio de destinatário]** O gráfico e a tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.
+++

## Guia No aplicativo {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Desempenho no aplicativo"
>abstract="Os KPIs de desempenho no aplicativo fornecem insights essenciais sobre o engajamento de visitantes com mensagens no aplicativo nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interações por tipo"
>abstract="A tabela “Interações por tipo” e seus gráficos detalham como usuários interagiram com a mensagem no aplicativo por meio do rastreamento de cliques, mensagens ignoradas ou interações nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Resumo no aplicativo"
>abstract="O gráfico “Resumo no aplicativo” ilustra o progresso das impressões e interações no aplicativo nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL No aplicativo]** A guia detalha as principais informações relativas às mensagens no aplicativo enviadas em sua campanha.

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório No aplicativo.

A variável **[!UICONTROL Desempenho no aplicativo]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as mensagens no aplicativo, como:

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo enviadas para todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.

A variável **[!UICONTROL Resumo no aplicativo]** O gráfico mostra a evolução de suas impressões e interações no aplicativo para o período relacionado.

A variável **[!UICONTROL Interações por tipo]** os gráficos e tabelas detalham como os usuários interagiram com a mensagem no aplicativo rastreando qualquer clique, descarte ou interação.

+++

## Guia Notificação por push {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Notificações por push: desempenho do envio"
>abstract="O gráfico “Notificações por push: desempenho do envio” resume dados essenciais sobre notificações por push, como erros ou mensagens entregues nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Notificação por push: estatísticas"
>abstract="A tabela “Estatísticas de push” fornece dados sobre a atividade de destinatários relacionada a notificações por push nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Notificações por push: resumo de envio"
>abstract="O gráfico “Notificações por push: resumo do envio” exibe os dados disponíveis para notificações por push enviadas nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Notificações por push: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Notificações por push: motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram nas últimas 24 horas durante o processo de envio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Notificações por push: detalhamento por plataforma"
>abstract="A tabela “Detalhamento por plataforma” e seus gráficos fornecem uma análise do sucesso das notificações por push nas últimas 24 horas baseada no sistema operacional do destinatário."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Notificação por push]** A guia detalha as principais informações relativas à notificação por push enviada em sua campanha.

![](assets/campaign_report_live_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Push.

**[!UICONTROL Desempenho de envio de notificação por push]**, **[!UICONTROL Resumo da notificação por push]** e **[!UICONTROL Notificação por push - Estatísticas]** widgets detalha as principais informações relacionadas à sua mensagem:

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Envolvimentos]**: Número total de aberturas e ações para esta notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

A variável **[!UICONTROL Motivos de erro]** e **[!UICONTROL Excluir motivos]** os gráficos e as tabelas permitem que você veja quais erros e exclusões ocorreram durante o processo de envio.

A variável **[!UICONTROL Estatísticas de envio - Com falha]** permite ver quantos erros e devoluções ocorreram.

A variável **[!UICONTROL Rastreamento por plataforma]**, **[!UICONTROL Envio por plataforma]** e **[!UICONTROL Detalhamento por plataforma]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional.
+++

## Guia SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS: estatísticas"
>abstract="A tabela “Estatísticas de envio de SMS” resume dados essenciais sobre as mensagens SMS, como mensagens direcionadas ou entregues nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS: desempenho por data"
>abstract="O dispositivo “SMS: desempenho por data” fornece informações importantes sobre mensagens nas últimas 24 horas por meio de uma representação gráfica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS: motivos de erro"
>abstract="A tabela “SMS: motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram nas últimas 24 horas durante o processo de envio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS: motivos de rejeições"
>abstract="A tabela “Motivos de rejeições” e seus gráficos contêm dados relacionados a mensagens rejeitadas nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL SMS]** A guia detalha as principais informações relacionadas à mensagem SMS enviada em sua campanha.

![](assets/campaign_report_live_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

A variável **[!UICONTROL SMS - Estatísticas]** A tabela detalha o sucesso da mensagem SMS:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário qualificados como perfis de público-alvo.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Cliques]**: Número total de visitas a URL.

A variável **[!UICONTROL Desempenho do SMS por data]** o widget detalha as principais informações relacionadas à sua mensagem com um gráfico:

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento automático de retorno.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

A variável **[!UICONTROL Excluir motivos]**, **[!UICONTROL Motivos de rejeições]** e **[!UICONTROL Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o processo de envio.
+++

## Guia Web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Desempenho na Web"
>abstract="Os KPIs de desempenho da Web fornecem informações abrangentes sobre o engajamento de visitantes com as experiências da Web nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Resumo da Web"
>abstract="O gráfico “Resumo da Web” ilustra a progressão das experiências na Web nas últimas 24 horas, incluindo impressões, impressões únicas e interações."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interações por elemento"
>abstract="A tabela “Interações por elemento” fornece informações importantes sobre o engajamento de visitantes com diferentes elementos das páginas da Web nas últimas 24 horas."

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
>title="Correspondência direta: estatísticas de envio"
>abstract="A tabela “Correspondência direta: estatísticas de envio” resume dados essenciais das últimas 24 horas sobre mensagens de correspondência direta, como mensagens direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Correspondência direta: motivos de erro"
>abstract="A tabela “Correspondência direta: motivos de erro” e seus gráficos permitem identificar os erros específicos ocorridos nas últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Correspondência direta: motivos de exclusão"
>abstract="A tabela “Correspondência direta: motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem nas últimas 24 horas."

Da sua campanha **[!UICONTROL Relatório ao vivo]**, o **[!UICONTROL Correspondência direta]** A guia detalha as principais informações relacionadas à correspondência direta.

![](assets/direct-mail-report_2.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de correspondência direta.

A variável **[!UICONTROL Correspondência direta - Estatísticas de envio]** A tabela detalha o sucesso da correspondência direta:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário qualificados como perfis de público-alvo.

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam sua correspondência direta.

A variável **[!UICONTROL Correspondência direta - Motivos excluídos]** e **[!UICONTROL Correspondência direta - Motivos de erro]** os gráficos e as tabelas permitem ver quais erros e exclusões ocorreram durante o processo de envio.
+++

## Recursos adicionais

* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório global da campanha](campaign-global-report.md)
