---
solution: Journey Optimizer
product: journey optimizer
title: Relatórios no nível do canal
description: Saiba como usar os dados dos Relatórios de canal
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 3f9d85dc77d3c572b1bad751646153874a5584c8
workflow-type: tm+mt
source-wordcount: '2664'
ht-degree: 33%

---

# Relatórios de canal {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Relatório de nível de canal"
>abstract="Os relatórios de canal oferecem uma visão geral abrangente das métricas de engajamento e tráfego em todos os canais. Seus relatórios são divididos em diferentes dispositivos, os quais detalham o sucesso e os erros da campanha e das jornadas. Cada painel de relatórios pode ser modificado redimensionando ou removendo dispositivos."

>[!IMPORTANT]
>
> Para acessar o menu **Relatório**, é necessário ter a permissão **[!UICONTROL Exibir Relatórios de Canal.]** [Saiba mais](channel-report-gs.md#before-starting-manage-reports-prereq)

Os Relatórios de canal fornecem aos usuários uma visão geral abrangente do tráfego e das métricas de engajamento no nível do canal. As métricas são agregadas para apresentar valores consolidados para ações originárias do canal escolhido, abrangendo várias campanhas e jornadas.

É possível acessar os Relatórios de canal navegando até o **Relatórios** no menu **Gerenciamento de jornadas** seção. É totalmente personalizável, você pode filtrar seus dados dependendo da data do relatório ou da ação. [Saiba mais](channel-report-gs.md)

A página do relatório é exibida com as seguintes guias:

* [Email](#email)
* [Notificações por push](#push)
* [SMS](#sms)
* [No aplicativo](#inapp)
* [Web](#web)
* [Correspondência direta](#direct-mail)

➡️ [Descubra este recurso no vídeo](#channel-report-video)

## Email {#email}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="Email: estatísticas totais de envio"
>abstract="Os KPIs “Email: estatísticas totais de envio” resumem dados essenciais sobre as notificações por push, como mensagens direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="Email: estatísticas totais de rastreamento"
>abstract="Os KPIs “Email: estatísticas totais de rastreamento” fornecem dados sobre a atividade de perfil de emails."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="Email: estatísticas de envio ao longo do tempo"
>abstract="O gráfico “Email: estatísticas de envio ao longo do tempo” apresenta dados sobre emails enviados, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="Email: estatísticas de rastreamento ao longo do tempo"
>abstract="O gráfico “Email: estatísticas de rastreamento ao longo do tempo” fornece dados sobre a atividade de perfil de emails, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Categorias de rejeição"
>abstract="A tabela “Categorias de rejeição” e seus gráficos fornecem dados sobre erros temporários e permanentes."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Motivos de rejeição"
>abstract="A tabela “Motivos de rejeições” e seus gráficos contêm dados relacionados às mensagens rejeitadas."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Enviados e entregues por domínio"
>abstract="A tabela “Enviados e entregues por domínio” representam um detalhamento em nível de domínio de todos os dados importantes de envio de email."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Rejeições e erros por domínio"
>abstract="A tabela “Rejeições e erros por domínio” e seu gráfico representam um detalhamento em nível de domínio de erros específicos que ocorreram durante o processo de envio."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Aberturas e cliques por domínio"
>abstract="A tabela “Aberturas e cliques por domínio” e seu gráfico representam um detalhamento em nível de domínio do engajamento de visitantes com o email."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Motivos de rejeição por domínio"
>abstract="A tabela “Motivos de rejeição por domínio” e seu gráfico representam um detalhamento em nível de domínio de dados sobre erros temporários e permanentes."

Nos relatórios de Canal, o menu Email detalha as principais informações relativas aos emails enviados em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/email_channel_1.png)

+++ Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de email.

A variável **[!UICONTROL Estatísticas de envio total de email]** O gráfico detalha o sucesso dos emails:

* **[!UICONTROL Direcionado]**: número total de emails processados.

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de entrega]**: porcentagem de emails enviados com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de rejeição]**: porcentagem de emails que foram rejeitados em comparação aos emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram e impediram o envio em comparação aos emails enviados.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

* **[!UICONTROL Taxa de exclusão]**: porcentagem de perfis que foram excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL Estatísticas de rastreamento total de email]** O widget contém os dados disponíveis para a atividade de perfil dos seus Emails:

* **[!UICONTROL Aberturas]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Taxa de abertura]**: número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em uma mensagem.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com o email.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

* **[!UICONTROL Taxa de reclamações de spam]**: Porcentagem de mensagens declaradas como spam ou lixo eletrônico em comparação ao número de emails enviados.

* **[!UICONTROL Cancelamentos de assinatura]**: Número de cliques no link de subscrição.

* **[!UICONTROL Taxa de cancelamento de inscrição]**: Porcentagem de cancelamento de subscrição em comparação ao número de emails enviados.

A variável **[!UICONTROL Estatísticas de envio ao longo do tempo]** O gráfico contém os dados disponíveis para emails enviados, como:

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

A variável **[!UICONTROL Estatísticas de rastreamento de email de hora extra]** O gráfico contém os dados disponíveis para aberturas e cliques.

A variável **[!UICONTROL Motivos de rejeição]** e **[!UICONTROL Categorias de rejeição]** os widgets contêm os dados disponíveis relacionados às mensagens rejeitadas, como:

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

Para obter mais informações sobre rejeições, consulte o [Lista de supressão](../reports/suppression-list.md) página.

A variável **[!UICONTROL Motivos de erro]** o gráfico e a tabela permitem que você veja qual erro ocorreu.

A variável **[!UICONTROL Motivos excluídos]** o gráfico e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber a mensagem.

A variável **[!UICONTROL Motivos de rejeição por domínio]**, **[!UICONTROL Enviado e entregue por domínios]**, **[!UICONTROL Aberturas e cliques por domínio]**  e **[!UICONTROL Rejeição e erros por domínio]** tabelas e gráficos representam o detalhamento no nível de domínio de todos os dados importantes de delivery e rastreamento de email.
+++

## Notificações por push {#push}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Notificações por push: estatísticas totais de envio"
>abstract="Os KPIs “Notificações por push: estatísticas totais de envio” resumem dados essenciais sobre notificações por push, como se foram direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Notificações por push: estatísticas totais de rastreamento"
>abstract="As Estatísticas totais de rastreamento de notificações por push fornecem dados sobre a atividade de perfil de notificações por push."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Notificações por push: estatísticas de envio ao longo do tempo"
>abstract="O gráfico “Notificações por push: estatísticas de envio ao longo do tempo” apresenta dados sobre notificações por push enviadas, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Notificações por push: estatísticas de rastreamento ao longo do tempo"
>abstract="O gráfico “Notificações por push: estatísticas de rastreamento ao longo do tempo” fornece dados sobre a atividade de perfil das notificações por push, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Estatísticas de rastreamento por plataforma"
>abstract="A tabela “Estatísticas de rastreamento por plataforma” e seu gráfico fornecem dados sobre a atividade de perfil das notificações por push, dependendo do sistema operacional do perfil."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Estatísticas de envio por plataforma"
>abstract="A tabela “Estatísticas de envio por platforma” e seu gráfico apresentam dados sobre as notificações por push enviadas."

Nos relatórios de Canal, o menu de Notificação por push detalha as principais informações relativas às notificações por push enviadas em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/push_channel_1.png)

+++  Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Push.

A variável **[!UICONTROL Notificações por push - Estatísticas totais de envio]** A tabela detalha as principais informações relativas às notificações por push com gráfico e KPIs:

* **[!UICONTROL Direcionado]**: Número total de notificações por push processadas.

* **[!UICONTROL Enviado]**: Número total de notificações por push enviadas.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Taxa de entrega]**: porcentagem de notificações por push enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de rejeição]**: Porcentagem de notificações por push que foram rejeitadas em comparação às notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram e impediram o envio, em comparação ao envio de notificações por push.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

* **[!UICONTROL Taxa de exclusão]**: porcentagem de perfis que foram excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL Notificação por push - Estatísticas totais de rastreamento]** contém os dados disponíveis para a atividade de perfil para suas notificações por push:

* **[!UICONTROL Aberturas]**: Número de vezes que uma notificação por push foi aberta.

* **[!UICONTROL Taxa de abertura]**: porcentagem de notificações por push abertas.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Taxa de ação]**: Porcentagem de ações na notificação por push entregue em comparação às notificações por push enviadas.

* **[!UICONTROL Taxa de participação]**: Porcentagem de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.

A variável **[!UICONTROL Notificações por push - Estatísticas de envio ao longo do tempo]** O gráfico contém os dados disponíveis para notificações por push enviadas, como:

* **[!UICONTROL Enviado]**: Número total de notificações por push enviadas.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

A variável **[!UICONTROL Motivos excluídos]** o gráfico e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber a mensagem.

A variável **[!UICONTROL Motivos de erro]** o gráfico e a tabela permitem que você veja qual erro ocorreu.

A variável **[!UICONTROL Rastreamento por plataforma]** e **[!UICONTROL Envio por plataforma]** gráficos e tabelas detalham o sucesso da sua notificação por push, dependendo do sistema operacional do seu perfil.
+++

## SMS {#sms}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="SMS: estatísticas totais de envio"
>abstract="Os KPIs “SMS: estatísticas totais de envio” resumem dados essenciais sobre mensagens SMS, como se foram direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="SMS: estatísticas totais de rastreamento"
>abstract="As “Estatísticas totais de rastreamento de SMS” fornecem dados sobre a atividade de perfil de mensagens SMS."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS: estatísticas de envio ao longo do tempo"
>abstract="O gráfico “SMS: estatísticas de envio ao longo do tempo” apresenta dados sobre mensagens SMS enviadas, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS: estatísticas de rastreamento ao longo do tempo"
>abstract="O gráfico “SMS: estatísticas de rastreamento ao longo do tempo” fornece dados sobre a atividade de perfil de mensagens SMS, detalhados por hora, dia, semana ou mês."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Motivos de rejeição"
>abstract="A tabela “Motivos de rejeições” e seus gráficos contêm dados relacionados às mensagens rejeitadas."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

Nos relatórios de Canal, o menu SMS detalha as principais informações relativas ao SMS enviado em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/sms_channel_1.png)

+++ Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório de SMS.

A variável **[!UICONTROL SMS - Estatísticas totais de envio]** A tabela detalha o sucesso do SMS:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para o canal SMS.

* **[!UICONTROL Enviado]**: Número total de mensagens SMS enviadas.

* **[!UICONTROL Entregue]**: Número de mensagens SMS enviadas com êxito em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Taxa de entrega]**: Porcentagem de mensagens SMS enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Taxa de rejeição]**: Porcentagem de mensagens SMS que foram rejeitadas em comparação às mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram e impediram o envio em comparação às mensagens SMS enviadas.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Taxa de exclusão]**: porcentagem de perfis que foram excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL SMS - Estatísticas de rastreamento total]** detalhe do widget as principais informações relativas ao engajamento dos visitantes com seus URLs:

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado na mensagem SMS.

* **[!UICONTROL Taxa de cliques]**: Porcentagem de usuários que interagiram com a mensagem SMS.

A variável **[!UICONTROL SMS - Estatísticas de envio ao longo do tempo]** o widget detalha as principais informações relacionadas à sua mensagem com um gráfico:

* **[!UICONTROL Enviado]**: Número total de mensagens SMS enviadas.

* **[!UICONTROL Entregue]**: Número de mensagens SMS enviadas com êxito em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

A variável **[!UICONTROL Excluir motivos]**, **[!UICONTROL Motivos de rejeições]** e **[!UICONTROL Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram.

+++

## Correspondência direta {#direct-mail}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Correspondência direta: estatísticas totais de envio"
>abstract="Os KPIs “Correspondência direta: estatísticas totais de envio” resumem dados essenciais sobre mensagens de correspondência direta, como se foram direcionadas ou entregues."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

Nos relatórios do Canal, o menu Direct mail detalha as principais informações relacionadas às mensagens de Direct mail enviadas em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/direct_mail_channel_1.png)

+++ Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Correspondência direta.

A variável **[!UICONTROL Correspondência direta - Total de estatísticas de envio]** a tabela detalha o sucesso de suas mensagens:

* **[!UICONTROL Direcionado]**: Número de perfis de usuário qualificados como perfis de público alvo para suas mensagens de correspondência direta.

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram e impediram o envio, em comparação ao envio de notificações por push.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Taxa de exclusão]**: porcentagem de perfis que foram excluídos pelo Adobe Journey Optimizer.

A variável **[!UICONTROL Excluir motivos]** e **[!UICONTROL Motivos de erro]** gráficos e tabelas permitem ver quais erros e exclusões ocorreram.
+++

## No aplicativo {#in-app}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="Total de engajamento no aplicativo"
>abstract="Os KPIs “Total de engajamento no aplicativo” fornecem informações abrangentes sobre o engajamento de visitantes com mensagens no aplicativo, incluindo métricas como impressões e interações."

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="Engajamento no aplicativo ao longo do tempo"
>abstract="O gráfico “Engajamento no aplicativo ao longo do tempo” rastreia impressões e interações no aplicativo, fornecendo detalhamentos por hora, dia, semana e mês."

Nos relatórios de Canal, o menu No aplicativo detalha as principais informações relacionadas às mensagens no aplicativo enviadas em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/inapp_channel_1.png)

+++  Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório No aplicativo.

A variável **[!UICONTROL Engajamento total no aplicativo]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as mensagens no aplicativo, como:

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Interações]**: Número total de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.

* **[!UICONTROL Destituições]**: Número total de mensagens no aplicativo que os perfis rejeitaram ao clicar no botão Fechar ou descartar automaticamente.

* **[!UICONTROL Taxa de descarte]**: porcentagem de mensagens no aplicativo que os perfis rejeitaram.

A variável **[!UICONTROL Hora extra de engajamento no aplicativo]** O gráfico mostra a evolução de suas impressões e interações no aplicativo para o período em questão, rastreando qualquer impressão, descarte ou interação.

+++

## Web {#web}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Total de engajamento na Web"
>abstract="Os KPIs “Total de engajamento na Web” fornecem informações abrangentes sobre o engajamento de visitantes com as páginas da Web, incluindo métricas como impressões e interações."

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Total de engajamento na web ao longo do tempo"
>abstract="O gráfico “Total de engajamento na web ao longo do tempo” rastreia as impressões e interações de páginas da Web, fornecendo detalhamentos por hora, dia, semana e mês."

Nos Relatórios de canal, o menu da Web detalha as principais informações relativas às páginas da Web incluídas em suas Campanhas e Jornadas. As métricas estão detalhadas abaixo.

![](assets/web_channel_1.png)

+++ Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório na Web.

A variável **[!UICONTROL Engajamento total na Web]** Os KPIs detalham as principais informações relativas ao envolvimento dos visitantes com as experiências da Web, como:

* **[!UICONTROL Impressões]**: número total de experiências da Web entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com sua página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

* **[!UICONTROL Destituições]**: Número total de páginas da Web cujos perfis foram rejeitados.

* **[!UICONTROL Taxa de descarte]**: porcentagem de páginas da Web com perfis rejeitados.

A variável **[!UICONTROL Hora extra do engajamento na Web]** O gráfico detalha as principais informações relativas ao envolvimento dos visitantes com as páginas da web.

+++

## Relatório de canal (vídeo) {#channel-report-video}

Saiba como acessar, navegar e exportar relatórios no nível do canal neste vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
