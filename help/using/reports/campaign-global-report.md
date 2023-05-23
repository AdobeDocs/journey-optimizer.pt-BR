---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global da campanha
description: Saiba como usar os dados do relatório global do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2036'
ht-degree: 3%

---

# Relatório global da campanha {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Relatório global da campanha"
>abstract="O Relatório global da campanha permite medir o impacto de suas campanhas durante um período selecionado. O relatório é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada painel de relatórios pode ser modificado redimensionando ou removendo widgets."

O relatório global da campanha pode ser acessado diretamente do seu Campaign com o **[!UICONTROL Exibir relatório]** botão.

![](assets/campaign_report_global_5.png)

A campanha **[!UICONTROL Relatório global]** será exibida com as seguintes guias:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [No aplicativo](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

A campanha **[!UICONTROL Relatório global]** O é dividido em widgets diferentes detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Guia Campanha {#campaign-global}

### Entrega {#delivery-global}

![](assets/campaign_report_global_1.png)

A variável **[!UICONTROL Estatísticas da campanha]** o widget detalha as principais informações relacionadas à sua campanha:

* **[!UICONTROL Perfis inseridos]**: Número de perfis que iniciaram a jornada.

* **[!UICONTROL Ações entregues]**: Número total de vezes que uma ação na jornada foi entregue.

* **[!UICONTROL Ações com falha em %]**: Número total de vezes que uma ação falhou na jornada em comparação ao número total de vezes que uma ação foi entregue.

## Guia E-mail {#email-global}

![](assets/campaign_report_global_2.png)

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL E-mail]** A guia detalha as principais informações relativas aos deliveries de email enviados no Campaign.

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de email.

A variável **[!UICONTROL Estatísticas de envio de email]** O gráfico detalha o sucesso do seu delivery:

* **[!UICONTROL Direcionado]**: Número total de mensagens processadas durante a análise de delivery.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de entrega]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de rejeição]**: porcentagem de emails que foram rejeitados em comparação aos emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante um delivery, impedindo que ele seja enviado, em comparação aos emails enviados.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL Email - Estatísticas de rastreamento]** O widget contém os dados disponíveis para a atividade do recipient para seu delivery:

* **[!UICONTROL Aberturas]**: Número de vezes que o delivery foi aberto em um delivery.

* **[!UICONTROL Aberturas únicas]**: Porcentagem de deliveries abertos.

* **[!UICONTROL Taxa de abertura]**: número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Cliques únicos]**: Número de recipients que clicaram em um conteúdo em um email.

* **[!UICONTROL Taxa de cliques únicos]**: Porcentagem de usuários que interagiram com o delivery.

* **[!UICONTROL Cancelamentos de assinatura]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

A variável **[!UICONTROL Estatísticas de envio]** O gráfico contém os dados disponíveis para emails enviados, como:

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

A variável **[!UICONTROL Motivos de rejeição]** e **[!UICONTROL Categorias de rejeição]** os widgets contêm os dados disponíveis relacionados às mensagens rejeitadas, como:

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

Para obter mais informações sobre rejeições, consulte o [Lista de supressão](../reports/suppression-list.md) página.

A variável **[!UICONTROL Motivos de erro]** O gráfico e a tabela permitem ver qual erro ocorreu durante o delivery.

A variável **[!UICONTROL Motivos excluídos]** o gráfico e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber a mensagem.

A variável **[!UICONTROL Email - URL superior]** gráfico e tabela detalha quais URLs do seu delivery são os mais visitados.

A variável **[!UICONTROL Email - Principal domínio de destinatário]** O gráfico e a tabela detalham quais domínios são os mais usados pelos recipients para abrir o email.

>[!NOTE]
>
>A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  Os widgets do só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimizado vs. não otimizado]** o gráfico detalha as principais informações relativas à mensagem, sejam elas otimizadas ou não:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.
* **[!UICONTROL Aberturas]**: Número de vezes que o delivery foi aberto em um delivery.
* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

A variável **[!UICONTROL Otimização da hora de envio]** detalha o sucesso do delivery dependendo do método de envio: otimizado ou normal.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.
+++

## Guia No aplicativo {#inapp-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL No aplicativo]** A guia detalha as principais informações relativas aos deliveries no aplicativo enviados em sua campanha.

![](assets/campaign_report_global_6.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório No aplicativo.

A variável **[!UICONTROL Desempenho no aplicativo]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as mensagens no aplicativo, como:

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos para os quais a mensagem no aplicativo foi entregue.

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que viram a mensagem.

* **[!UICONTROL Taxa de descarte]**: porcentagem de mensagens no aplicativo que os recipients rejeitaram.

A variável **[!UICONTROL Resumo no aplicativo]** O gráfico mostra a evolução das impressões no aplicativo para o período relacionado.

A variável **[!UICONTROL Cliques por botão]** o gráfico e a tabela contêm os dados disponíveis para o comportamento do recipient por botão:

* **[!UICONTROL Cliques]**: número total de recipients que interagiram com os botões incluídos na mensagem no aplicativo.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que viram a mensagem.
+++

## Guia Notificação por push {#push-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Notificação por push]** A guia detalha as principais informações relativas aos deliveries por push enviados em sua campanha.

![](assets/campaign_report_global_3.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Push.

A variável **[!UICONTROL Notificação por push - Estatísticas de envio]** A tabela detalha as principais informações relativas às notificações por push com gráfico e KPIs:

* **[!UICONTROL Direcionado]**: Número total de mensagens processadas durante a análise de delivery.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de entrega]**: Porcentagem de mensagens enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de rejeição]**: Porcentagem de notificações por push que foram rejeitadas em comparação às notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante um delivery, impedindo que ele fosse enviado, em comparação ao envio de notificações por push.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL Push - Estatísticas de rastreamento]** contém os dados disponíveis para a atividade de recipient para seu delivery:

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Taxa de abertura]**: porcentagem de notificações por push abertas.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Envolvimentos]**: Número total de aberturas e ações para esta notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

* **[!UICONTROL Taxa de participação]**: Porcentagem de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

A variável **[!UICONTROL Resumo da notificação por push]** O gráfico contém os dados disponíveis para notificações por push enviadas, como:

* **[!UICONTROL Aberturas]**: Número de vezes que uma mensagem foi aberta em um delivery.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

>[!NOTE]
>
>A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  Os widgets do só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimizado vs. não otimizado]** o gráfico detalha as principais informações relativas à mensagem, sejam elas otimizadas ou não:

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Aberturas]**: Número de vezes que o delivery foi aberto em um delivery.
* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

A variável **[!UICONTROL Otimização da hora de envio]** detalha o sucesso do delivery dependendo do método de envio: otimizado ou normal.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

A variável **[!UICONTROL Motivos de erro]** O gráfico e a tabela permitem ver qual erro ocorreu durante o delivery.

A variável **[!UICONTROL Motivos excluídos]** o gráfico e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber a mensagem.

A variável **[!UICONTROL Rastreamento por plataforma]**, **[!UICONTROL Envio por plataforma]** e **[!UICONTROL Detalhamento por plataforma]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional do recipient.
+++

## Guia SMS {#sms-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL SMS]** A guia detalha as principais informações relativas aos deliveries de SMS enviados em sua campanha.

![](assets/campaign_report_global_4.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

A variável **[!UICONTROL SMS - Estatísticas de envio]** a tabela detalha o sucesso do seu delivery:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para este delivery.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

A variável **[!UICONTROL Desempenho do SMS por data]** o widget detalha as principais informações relacionadas à sua mensagem com um gráfico:

* **[!UICONTROL Enviado]**: Número total de envios para o delivery.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processamento de delivery e retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um delivery impedindo que ele fosse enviado a perfis.

A variável **[!UICONTROL Excluir motivos]**, **[!UICONTROL Motivos de rejeições]** e **[!UICONTROL Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram durante o delivery.

A variável **[!UICONTROL SMS - Cliques por links]** e **[!UICONTROL SMS - Estatísticas de rastreamento]** os widgets detalham as principais informações relativas ao engajamento dos visitantes com seus URLs.

+++

## Guia Web {#web-tab}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Web]** A guia detalha as informações principais relativas às páginas da Web.

![](assets/web-report.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório da Web.

A variável **[!UICONTROL Desempenho da Web]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as experiências da Web, como:

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos a quem a experiência da web foi entregue.

* **[!UICONTROL Impressões]**: número total de experiências da web entregues a todos os usuários.

* **[!UICONTROL Taxa de cliques]**: porcentagem de visitantes que interagiram com os vários elementos nas páginas da Web.

A variável **[!UICONTROL Resumo da Web]** o gráfico mostra a evolução de suas experiências da web (impressões, impressões exclusivas e cliques) para o período relacionado.

A variável **[!UICONTROL Cliques por elemento]** A tabela detalha as principais informações relativas ao envolvimento dos visitantes com os vários elementos em suas páginas da web.
+++

## Recursos adicionais

* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório em tempo real da campanha](campaign-live-report.md)
