---
title: Relatório de campanha global
description: Saiba como usar dados do relatório de Campanha Global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: b56df2c22f041114805e10fee7156855c2cbbfa9
workflow-type: tm+mt
source-wordcount: '1540'
ht-degree: 4%

---

# Relatório de campanha global {#campaign-global-report}

O relatório Campaign Global pode ser acessado diretamente de sua Campanha com a **[!UICONTROL Global view]** botão.

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

### Objetivos {#objectives-global}

>[!AVAILABILITY]
>
>O recurso de Experiência de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/performance_report.gif)

O **[!UICONTROL Objectives]** A guia do relatório Campanha permite ajustar melhor os relatórios dos deliveries, direcionando uma métrica específica.

O **[!UICONTROL Objectives]** listadas estão vinculadas a **[!UICONTROL Datasets]** que definem uma conexão com um sistema para recuperar informações adicionais. Uma lista de **[!UICONTROL Objectives]** está disponível, mas você pode adicionar o seu ao adicionar novo **[!UICONTROL Dataset]**. Para obter o procedimento detalhado, consulte esta documentação.

Após selecionar os Objetivos que deseja definir como meta, os dois **[!UICONTROL Performance overview]** e **[!UICONTROL Campaign objective]** os widgets fornecerão um resumo detalhado do desempenho do seu delivery.

Com o **[!UICONTROL Campaign objective]** no widget, você também pode optar por comparar seu objetivo principal com outra métrica.

Observe que cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/global-report.md#modify-dashboard).

### Experimentação {#experimentation-global}

>[!AVAILABILITY]
>
>O recurso de Experiência de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/experimentation_report_3.png)

Da sua campanha **[!UICONTROL Global report]**, o **[!UICONTROL Experimentation]** detalha as informações principais sobre o desempenho de cada variante e se há um melhor desempenho.

Observe que a definição do melhor desempenho pode levar algum tempo, ele será representado por este ícone ![](assets/experimentation_report_1.png).

O **[!UICONTROL Experiment result]** O widget detalha o desempenho de cada variante. Pode alterar o seu valor basal selecionando um dos tratamentos na **[!UICONTROL Baseline]** o menu suspenso. O melhor tratamento será representado com um ícone de estrela.

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Profiles]**: Número de perfis direcionados para este tratamento.

* **[!UICONTROL Unique outbound clicks]**: Contagem total de cliques em canais de saída.

* **[!UICONTROL Count per profile]**: O valor total da métrica de objetivo do Experimento dividido pelo número de perfis.

* **[!UICONTROL Confidence interval]**: Diferença percentual no desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Melhoria da percentagem na taxa de conversão de um determinado tratamento em relação ao valor basal. [Saiba mais](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Evidência de que um determinado tratamento é o mesmo que o tratamento inicial. [Saiba mais](../campaigns/experiment-calculations.md#understand-confidence)

Para detalhar esses resultados e como interpretá-los, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).

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

O **[!UICONTROL Email - Tracking statistics]** O widget contém os dados disponíveis para a atividade do recipient para o seu delivery:

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
