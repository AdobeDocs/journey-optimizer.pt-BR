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
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '4648'
ht-degree: 19%

---

# Relatório global da campanha {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Relatório global da campanha"
>abstract="O Relatório global da campanha permite medir o impacto de suas campanhas durante um período selecionado. O relatório é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada painel de relatórios pode ser modificado redimensionando ou removendo widgets."

Relatórios globais, acessíveis pelo **O tempo todo** , exiba eventos que ocorreram há pelo menos duas horas e cubra eventos durante um período selecionado. Em comparação, os Relatórios em tempo real focalizam eventos que ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos a partir da ocorrência do evento.

O relatório global da campanha pode ser acessado diretamente do seu Campaign com o **[!UICONTROL Exibir relatório]** botão.

![](assets/campaign_report_global_5.png)

A campanha **[!UICONTROL Relatório global]** será exibida com as seguintes guias:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [No aplicativo](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)
* [Correspondência direta](#direct-mail-global)

A campanha **[!UICONTROL Relatório global]** O é dividido em widgets diferentes detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Guia Campanha {#campaign-global}

### Entrega {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Estatísticas da campanha"
>abstract="O dispositivo Estatísticas da campanha detalha as principais informações relacionadas à campanha, como perfis inseridos e ações entregues."

![](assets/campaign_report_global_1.png)

A variável **[!UICONTROL Estatísticas da campanha]** Os KPIs servem como um painel abrangente, oferecendo um detalhamento das principais métricas relacionadas à sua campanha. Isso inclui informações essenciais, como o número de perfis e as ações entregues, fornecendo uma compreensão completa do desempenho e do envolvimento da campanha.

+++ Saiba mais sobre as métricas de estatísticas do Campaign

* **[!UICONTROL Público]**: Número de perfis segmentados.

* **[!UICONTROL Ações entregues]**: Número total de vezes que uma ação foi entregue.

* **[!UICONTROL Ações com falha em %]**: Porcentagem de vezes que uma ação falhou em comparação ao número total de vezes que uma ação foi entregue.

+++

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Relatório de experimentação {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de sucesso"
>abstract="O valor total da métrica sucesso, anteriormente selecionado ao criar seus experimentos, dividido pelo número de perfis."

![](assets/experimentation_report_3.png)

A variável **[!UICONTROL Experimentação]** A guia fornece informações importantes sobre o desempenho de cada variante e identifica a mais bem-sucedida.

Observe que a definição do melhor desempenho pode levar algum tempo. Ela será representada por esse ícone ![](assets/experimentation_report_1.png).

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Experimentação.

A variável **[!UICONTROL Resultado do experimento]** o widget detalha o desempenho de cada variante. Você pode alterar sua linha de base selecionando um dos tratamentos nas **[!UICONTROL Linha de base]** o menu suspenso. O melhor tratamento será representado com um ícone de estrela.

Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Aumento sobre a linha de base]**: Medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é igual ao tratamento inicial. [Saiba mais](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Cliques de saída únicos]**: Contagem total de cliques nos canais de saída.

* **[!UICONTROL Perfis]**: Número de perfis direcionados para este tratamento.

* **[!UICONTROL Cliques/perfis de saída únicos]**: Valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis.

A variável **[!UICONTROL Intervalo de confiança]** O gráfico mede a incerteza em torno da melhoria. Ela detalha a diferença percentual de desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

O último widget fornece dados relacionados ao **[!UICONTROL Métrica de sucesso]** você selecionou anteriormente para os tratamentos. Você tem a opção de selecionar uma métrica direcionada diferente da variável **[!UICONTROL Métrica]** menu suspenso para rastrear dados alternativos.

>[!CAUTION]
>
>Ao trabalhar com métricas filtradas de experimentação, observe que alterar a seleção de Métrica do menu suspenso na página de comparação para experimentação não manterá o valor do filtro. Por exemplo, alternar de &quot;Cliques&quot; para &quot;Cliques únicos&quot; levará à perda do filtro aplicado, tornando a comparação imprecisa ou inválida.

+++

## Guia Email {#email-global}

### Email - Estatísticas de envio {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="Email: estatísticas de envio"
>abstract="A tabela “Email: estatísticas de envio” resume dados essenciais sobre o email, como se ele foi direcionado ou entregue."

![](assets/campaign_email_sending.png)

A variável **[!UICONTROL Estatísticas de envio de email]** A tabela fornece um resumo abrangente dos dados essenciais sobre suas campanhas de email. Ele detalha as principais métricas, como o tamanho do público-alvo e o número de emails entregues com êxito, oferecendo insights valiosos sobre a eficácia e o alcance de seus emails.

+++ Saiba mais sobre métricas de Estatísticas de envio de email

* **[!UICONTROL Direcionado]**: número total de emails processados durante o processo de envio.

* **[!UICONTROL Enviado]**: Número total de envios para o seu email.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de entrega]**: porcentagem de emails enviados com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Taxa de rejeição]**: porcentagem de emails que foram rejeitados em comparação aos emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado, em comparação aos emails enviados.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Email: estatísticas de rastreamento {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="Email: estatísticas de rastreamento"
>abstract="A tabela “Email: estatísticas de rastreamento” fornece dados sobre atividades de perfil do email."

![](assets/campaign_email_tracking.png)

A variável **[!UICONTROL Email - Estatísticas de rastreamento]** A tabela oferece uma conta detalhada da atividade do perfil relacionada às suas campanhas de email. Isso inclui métricas sobre aberturas, cliques e outros indicadores de engajamento relevantes, oferecendo uma visualização abrangente de como os perfis interagem com seu conteúdo de email.

+++ Saiba mais sobre Email - Métricas de estatísticas de rastreamento

* **[!UICONTROL Aberturas]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Aberturas únicas]**: porcentagem de emails abertos.

* **[!UICONTROL Taxa de abertura]**: número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em um email.

* **[!UICONTROL Taxa de cliques únicos]**: porcentagem de usuários que interagiram com seus emails.

* **[!UICONTROL Cancelamentos de assinatura]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

+++

### Email - Desempenho de envio {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="Email: desempenho de envio"
>abstract="O gráfico de desempenho Email - Envio apresenta dados abrangentes sobre emails enviados, oferecendo insights sobre as métricas principais, como entregues e rejeitados, permitindo uma análise detalhada do processo de delivery de email."

![](assets/campaign_email_sending_performance.png)

A variável **[!UICONTROL Email - Desempenho de envio]** O gráfico fornece uma visualização abrangente dos dados relacionados aos emails enviados, oferecendo insights sobre as métricas principais, como entregas e rejeições. Isso permite uma análise detalhada do processo de envio de email, fornecendo informações valiosas sobre a eficiência e o desempenho de suas campanhas de email.

+++ Saiba mais sobre Email - Envio de métricas de desempenho

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de emails enviados.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

+++

### Email - Motivos e categorias de rejeição {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="Email: categorias de rejeição"
>abstract="A tabela “Email: categorias de rejeição” e seus gráficos fornecem dados sobre erros temporários e permanentes."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="Email: motivos de rejeições"
>abstract="A tabela “Email: motivos de rejeições” e seus gráficos contêm dados relacionados às mensagens rejeitadas."

![](assets/campaign_email_bounces.png)

A variável **[!UICONTROL Email - Motivos de rejeição]** e **[!UICONTROL Email - Categorias de rejeição]** os widgets compilam os dados disponíveis relacionados às mensagens rejeitadas, fornecendo insights detalhados sobre os motivos e categorias específicas por trás das rejeições de email.

Para obter mais informações sobre rejeições, consulte o [Lista de supressão](../reports/suppression-list.md) página.

+++ Saiba mais sobre Email - Métricas de categorias de rejeição

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

+++


### Email: motivos de erro {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="Email: motivos de erro"
>abstract="A tabela “Email: motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

![](assets/campaign_email_error_reasons.png)

A variável **[!UICONTROL Motivos de erro]** gráficos e tabelas oferecem visibilidade dos erros específicos que ocorreram durante o processo de envio, fornecendo informações valiosas sobre a natureza e a ocorrência de erros.

Você pode optar por alternar entre uma tabela, um gráfico de barras ou uma rosca.

### Email: motivos de exclusão {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="Email: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

![](assets/campaign_email_excluded.png)

A variável **[!UICONTROL Motivos excluídos]** os gráficos e a tabela apresentam uma visão abrangente dos diferentes fatores que resultaram na exclusão de perfis de usuário do público-alvo direcionado, resultando no não recebimento da mensagem.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### Enviados e entregues por domínio {#sent-domains}

![](assets/campaign_email_sent_domains.png)

A variável  **[!UICONTROL Enviado e entregue por domínios]** A tabela e o gráfico fornecem um detalhamento dos emails no nível do domínio, oferecendo insights abrangentes sobre o desempenho dos emails.

+++ Saiba mais sobre métricas Enviado e entregue por domínios

* **[!UICONTROL Enviado]**: Número total de envios para o seu email.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

+++

### Rejeições e erros por domínio {#bounces-domains}

![](assets/campaign_email_bounce_domains.png)

A variável  **[!UICONTROL Rejeições e erros por domínios]** O gráfico e a tabela oferecem um detalhamento em nível de domínio de erros específicos encontrados durante o processo de envio, fornecendo uma análise detalhada dos problemas que ocorreram.

+++ Saiba mais sobre métricas de Rejeições e erros por domínios

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que seu email fosse enviado para perfis.

+++

### Aberturas e cliques por domínio {#opens-domains}

![](assets/campaign_email_open_domains.png)

A variável  **[!UICONTROL Abrir e clicar por domínios]** O gráfico e a tabela mostram um detalhamento em nível de domínio do envolvimento dos perfis com o email, fornecendo insights valiosos sobre como domínios diferentes interagem com o conteúdo.

+++ Saiba mais sobre métricas de Abertura e cliques por domínios

* **[!UICONTROL Aberturas]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

+++

### Motivos de rejeição por domínio {#bounce-reasons-domains}

![](assets/campaign_email_bounce_reasons_domains.png)

A variável  **[!UICONTROL Motivos de rejeição por domínio]** O gráfico e a tabela oferecem um detalhamento de dados em nível de domínio sobre erros temporários e permanentes, fornecendo insights detalhados sobre os motivos por trás das mensagens rejeitadas.

+++ Saiba mais sobre Motivos de rejeição por métricas de domínio

* **[!UICONTROL Aberturas]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

+++

### Email: URL principal {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="Email: URL principal"
>abstract="A tabela “Email: URL principal” e seu gráfico oferecem uma visão geral abrangente dos URLs do email que recebem o maior tráfego de visitantes, permitindo identificar os links mais populares."

![](assets/campaign_email_topurl.png)

A variável **[!UICONTROL Email - URL superior]** O gráfico e a tabela fornecem uma visão geral abrangente dos URLs em seu email que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão do envolvimento do perfil com conteúdo específico em seus emails.

### Email: melhor domínio do destinatário {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="Email: melhor domínio do destinatário"
>abstract="A tabela “Email: melhor domínio do destinatário” e seu gráfico fornecem um detalhamento dos domínios que os destinatários usam com mais frequência para abrir o email, oferecendo insights valiosos sobre o comportamento do destinatário."

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> A variável **[!UICONTROL Email - Melhor domínio de destinatário]** O widget tem uma taxa de precisão de 99,95%.

A variável **[!UICONTROL Email - Melhor domínio de destinatário]** O gráfico e a tabela oferecem um detalhamento dos domínios que os perfis usam com mais frequência para abrir seus emails. Isso fornece insights valiosos sobre o comportamento do perfil, ajudando você a entender as plataformas preferenciais.

+++ Saiba mais sobre Email - Melhores métricas de domínio de recipient

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Taxa de entrega]**: porcentagem de emails enviados com êxito.

* **[!UICONTROL Rejeições + Taxa de erros]**: porcentagem de emails que foram rejeitados em comparação aos emails enviados.

+++

### Email - Otimização {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  Os widgets do só estarão disponíveis se a opção Otimização de tempo de envio estiver ativada para o seu email. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]** os widgets detalham as principais informações relacionadas à sua mensagem, sejam eles otimizados ou não.

+++ Saiba mais sobre as métricas de otimização de tempo de envio

* **[!UICONTROL Enviado]**: número total de envios.

* **[!UICONTROL Aberturas]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

+++

### Email - Ofertas {#email-offers}

![](assets/campaign_email_offers.png)

A variável **[!UICONTROL Estatísticas de ofertas]**, **[!UICONTROL Estatísticas de ofertas ao longo do tempo]** e **[!UICONTROL Estatísticas detalhadas da oferta]** os widgets medem o sucesso e o impacto da sua oferta no público-alvo direcionado.

+++ Saiba mais sobre Email - Métricas de ofertas

* **[!UICONTROL Oferta enviada]**: número total de envios para a oferta.

* **[!UICONTROL Impressão da oferta]**: Número de vezes que a oferta foi aberta em seus emails.

* **[!UICONTROL Cliques de oferta]**: Número de vezes que uma oferta foi clicada em seus emails.

* **[!UICONTROL Nome do posicionamento]**: nome do posicionamento usado para exibir a oferta. Para obter mais informações sobre posicionamento, consulte esta [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nome da oferta]**: Nome da oferta adicionada no delivery. Para obter mais informações sobre posicionamento, consulte esta [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Oferta enviada]**: número total de envios para a oferta.

* **[!UICONTROL Taxa de impressões da oferta]**: Porcentagem de ofertas abertas em comparação ao número de ofertas enviadas.

+++

## Guia No aplicativo {#inapp-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL No aplicativo]** A guia detalha as principais informações relativas às mensagens no aplicativo enviadas em sua campanha.

### Desempenho no aplicativo {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="Desempenho no aplicativo"
>abstract="Os KPIs de desempenho no aplicativo fornecem insights essenciais sobre o engajamento de visitantes com as mensagens no aplicativo."

![](assets/campaign_inapp_performance.png)

A variável **[!UICONTROL Desempenho no aplicativo]** Os KPIs fornecem insights essenciais sobre o envolvimento de seus visitantes com mensagens no aplicativo, fornecendo métricas essenciais para avaliar a eficácia e o impacto de suas campanhas no aplicativo.

+++ Saiba mais sobre Métricas de desempenho no aplicativo

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos para os quais a mensagem no aplicativo foi entregue.

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.

+++

### Interações por tipo {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interações por tipo"
>abstract="A tabela “Interações por tipo” e seus gráficos detalham como usuários interagiram com a mensagem no aplicativo por meio do rastreamento de cliques, mensagens ignoradas ou interações."

![](assets/campaign_inapp_interactions.png)

A variável **[!UICONTROL Interações por tipo]** Os gráficos e a tabela fornecem uma conta detalhada de como os perfis interagiram com a mensagem no aplicativo, rastreando ações como cliques, rejeições ou qualquer outra forma de envolvimento.

### Resumo no aplicativo {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="Resumo no aplicativo"
>abstract="O gráfico “Resumo no aplicativo” ilustra a progressão das impressões e interações no aplicativo durante o período especificado."

![](assets/campaign_inapp_summary.png)

A variável **[!UICONTROL Resumo no aplicativo]** O gráfico ilustra a progressão de suas impressões e interações no aplicativo durante o período especificado, fornecendo uma visão geral abrangente do desempenho das mensagens no aplicativo.

+++ Saiba mais sobre Métricas de resumo no aplicativo

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos para os quais a mensagem no aplicativo foi entregue.

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.

+++

## Guia Notificação por push {#push-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Notificação por push]** A guia detalha as principais informações relativas às notificações por push enviadas em sua campanha.

### Notificações por push: estatísticas de envio {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Notificações por push: estatísticas de envio"
>abstract="A tabela “Notificações por push: estatísticas de envio” resume dados essenciais sobre notificações por push, como mensagens direcionadas ou entregues."

![](assets/campaign_push_sending.png)

A variável **[!UICONTROL Notificação por push - Estatísticas de envio]** A tabela fornece um resumo dos dados essenciais relacionados às suas notificações por push, incluindo as métricas principais, como o número de mensagens direcionadas e o número de mensagens entregues com êxito.

+++ Saiba mais sobre Notificação por push - Envio de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução da notificação por push recorrente. Para direcionar apenas uma ou várias notificações por push recorrentes, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: número total de notificações por push processadas durante a análise.

* **[!UICONTROL Enviado]**: número total de envios para a notificação por push.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Taxa de entrega]**: porcentagem de notificações por push enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de notificações por push.

* **[!UICONTROL Taxa de rejeição]**: Porcentagem de notificações por push que foram rejeitadas em comparação às notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante a prevenção do envio em comparação às notificações por push enviadas.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Notificações por push: estatísticas de rastreamento {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Notificações por push: estatísticas de rastreamento"
>abstract="As “Estatísticas de rastreamento de push” fornecem dados sobre as atividades de perfil das notificações por push."

![](assets/campaign_push_tracking.png)

A variável **[!UICONTROL Notificação por push - Estatísticas de rastreamento]** o widget oferece um instantâneo detalhado da atividade do perfil vinculada às suas notificações por push, fornecendo insights essenciais sobre a eficácia do engajamento e das notificações por push.

+++ Saiba mais sobre Notificação por push - Rastreamento de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução da notificação por push recorrente. Para direcionar apenas uma ou várias notificações por push recorrentes, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Aberturas]**: Número de vezes que sua notificação por push foi aberta.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

+++

### Notificações por push: resumo de envio {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Notificações por push: resumo de envio"
>abstract="O gráfico “Notificações por push: resumo de envio” exibe os dados disponíveis para notificações por push enviadas."

![](assets/campaign_push_sending_summary.png)

A variável **[!UICONTROL Notificação por push - Resumo de envio]** O gráfico oferece uma representação dinâmica, exibindo uma análise da atividade de notificações por push. Esta representação gráfica fornece um detalhamento abrangente das notificações por push enviadas.

+++ Saiba mais sobre Notificação por push - Envio de métricas de resumo

* **[!UICONTROL Aberturas]**: Número de vezes que sua notificação por push foi aberta.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

+++

### Notificação por push - Otimização {#push-optimized}

>[!NOTE]
>
>A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  Os widgets do só estarão disponíveis se a opção Otimização de tempo de envio estiver ativada para a notificação por push. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]** os widgets detalham as principais informações relacionadas à sua mensagem, sejam eles otimizados ou não.

+++ Saiba mais sobre Notificação por push - Enviar métricas de otimização de tempo

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Aberturas]**: Número de vezes que sua notificação por push foi aberta.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de notificações por push enviadas.

+++

### Notificações por push: motivos de erro {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Notificações por push: motivos de erro"
>abstract="A tabela “Motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

![](assets/campaign_push_error_reasons.png)

A variável **[!UICONTROL Motivos de erro]** A tabela e os gráficos fornecem a capacidade de identificar os erros específicos que ocorreram durante o processo de envio de suas notificações por push, oferecendo insights detalhados sobre quaisquer problemas encontrados ao longo do caminho.

### Notificações por push: motivos de exclusão {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Notificações por push: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

![](assets/campaign_push_excluded.png)

A variável **[!UICONTROL Motivos excluídos]** os gráficos e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber suas notificações por push.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### Notificações por push: detalhamento por plataforma {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Notificações por push: detalhamento por plataforma"
>abstract="A tabela “Detalhamento por plataforma” e seus gráficos fornecem uma análise do sucesso das notificações por push baseada no sistema operacional do perfil."

![](assets/campaign_push_breakdown.png)

A variável **[!UICONTROL Notificação por push - Detalhamento por plataforma]** O gráfico e a tabela fornecem uma análise detalhada do sucesso de suas notificações por push, oferecendo insights com base no sistema operacional do seu perfil. Esse detalhamento melhora a sua compreensão do desempenho das notificações por push em diferentes plataformas.

+++ Saiba mais sobre Notificação por push - Detalhamento por métricas de plataforma

* **[!UICONTROL Direcionado]**: número total de notificações por push processadas durante a análise.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Aberturas]**: Número de vezes que sua notificação por push foi aberta.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Rejeições]**: Total de erros acumulados e processamento de retorno automático em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

## Guia SMS {#sms-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL SMS]** A guia detalha as principais informações relativas às mensagens SMS enviadas em sua campanha.

### SMS: estatísticas de envio {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS: estatísticas de envio"
>abstract="A tabela “SMS: estatísticas de envio” resume dados essenciais sobre as mensagens SMS, como mensagens direcionadas ou entregues."

![](assets/campaign_sms_sending.png)

A variável **[!UICONTROL SMS - Estatísticas de envio]** A tabela fornece um resumo conciso dos dados essenciais relacionados às suas mensagens SMS, englobando as métricas principais, como o número de mensagens direcionadas e a contagem de mensagens entregues com êxito.

+++ Saiba mais sobre SMS - Envio de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução da mensagem SMS recorrente. Para direcionar apenas uma ou várias mensagens SMS recorrentes, selecione-as no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: Número de perfis de usuário qualificados como perfis de público-alvo.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam a mensagem.

* **[!UICONTROL Enviado]**: Número total de envios para suas mensagens SMS.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

+++

### SMS - Estatísticas de rastreamento {#sms-tracking-statistics}

![](assets/campaign_sms_tracking.png)

A variável **[!UICONTROL SMS - Estatísticas de rastreamento]** O widget fornece uma visão geral detalhada das principais informações relacionadas ao envolvimento dos visitantes com os URLs, oferecendo insights sobre a eficácia das mensagens SMS.

+++ Saiba mais sobre SMS - Rastreamento de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução do SMS recorrente. Para direcionar apenas um ou vários SMS recorrentes, selecione-o no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em uma mensagem SMS.

+++

### SMS: desempenho por data {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS: desempenho por data"
>abstract="O dispositivo “SMS: desempenho por data” fornece informações importantes sobre as mensagens por meio de uma representação gráfica."

![](assets/campaign_sms_performance.png)

A variável **[!UICONTROL Desempenho do SMS por data]** o widget oferece uma visão geral detalhada das principais informações relacionadas às suas mensagens, apresentadas por meio de um gráfico, fornecendo insights sobre as tendências de desempenho em períodos específicos.

+++ Saiba mais sobre SMS - Desempenho por métricas de data

* **[!UICONTROL Enviado]**: Número total de envios para suas mensagens SMS.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram que impediram o envio para perfis.

+++

### SMS: motivos de erro {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS: motivos de erro"
>abstract="A tabela “SMS: motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

![](assets/campaign_sms_error_reasons.png)

A variável **[!UICONTROL Motivos de erro]** Os gráficos e as tabelas permitem identificar os erros específicos que ocorreram durante o processo de envio de suas mensagens SMS, facilitando uma análise completa de todos os problemas encontrados.

### SMS: motivos de exclusão {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS: motivos de exclusão"
>abstract="A tabela “Motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

![](assets/campaign_sms_excluded.png)

A variável **[!UICONTROL Motivos de exclusão]** Os gráficos e as tabelas representam visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens SMS.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### SMS: motivos de rejeições {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS: motivos de rejeições"
>abstract="A tabela “Motivos de rejeições” e seus gráficos contêm dados relacionados às mensagens rejeitadas."

A variável **[!UICONTROL Motivos de rejeições]** Os gráficos e as tabelas fornecem uma visão geral abrangente dos dados relacionados às mensagens SMS rejeitadas, fornecendo insights valiosos sobre os motivos específicos por trás das instâncias de rejeições de mensagens SMS.

### SMS: cliques por link {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS: cliques por link"
>abstract="O dispositivo “SMS: cliques por link” fornece insights essenciais sobre o engajamento de visitantes com os URLs nas mensagens"

![](assets/campaign_sms_clicks.png)

A variável **[!UICONTROL SMS - Cliques por links]** O widget oferece informações essenciais sobre o envolvimento dos visitantes com os URLs incluídos em suas mensagens, fornecendo informações valiosas sobre quais links atraem mais interação.

## Guia Web {#web-tab}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Web]** A guia detalha as informações principais relativas às páginas da Web.

### Desempenho na Web {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Desempenho na Web"
>abstract="Os KPIs de desempenho na Web fornecem informações abrangentes sobre o engajamento de visitantes com as experiências da Web."

![](assets/campaign_web_performance.png)

A variável **[!UICONTROL Desempenho da Web]** Os KPIs oferecem insights abrangentes sobre o engajamento de seus visitantes com suas páginas da Web, abrangendo métricas principais, como Impressões e Interações.

+++ Saiba mais sobre métricas de desempenho da Web

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos a quem a experiência da web foi entregue.

* **[!UICONTROL Impressões]**: número total de experiências da web entregues a todos os usuários.

* **[!UICONTROL Taxa de interação]**: porcentagem de envolvimentos com a página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

+++

### Resumo da Web {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Resumo da Web"
>abstract="O gráfico “Resumo da Web” ilustra a progressão das experiências da Web, incluindo impressões, impressões únicas e interações, durante o período especificado."

![](assets/campaign_web_summary.png)

A variável **[!UICONTROL Resumo da Web]** o gráfico mostra a evolução de suas experiências da web (impressões, impressões exclusivas e interações) para o período relacionado.

+++ Saiba mais sobre métricas de resumo na Web

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos a quem a experiência da web foi entregue.

* **[!UICONTROL Impressões]**: número total de experiências da web entregues a todos os usuários.

* **[!UICONTROL Interação]**: número total de envolvimentos com sua página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

+++

### Interações por elemento {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interações por elemento"
>abstract="A tabela “Interações por elemento” fornece informações importantes sobre o engajamento de visitantes com diferentes elementos em suas páginas da Web."

![](assets/campaign_web_interactions.png)

A variável **[!UICONTROL Interações por elemento]** A tabela apresenta informações abrangentes sobre o envolvimento dos visitantes com os vários elementos em suas páginas da Web, oferecendo insights valiosos sobre as interações e preferências do usuário.

+++ Saiba mais sobre Interações por métricas de elementos

* **[!UICONTROL Interação]**: número total de envolvimentos com sua página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

* **[!UICONTROL Taxa de interação]**: porcentagem de envolvimentos com a página da Web. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

+++

## Guia Correspondência direta {#direct-mail-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Correspondência direta]** A guia detalha as principais informações relativas às mensagens de correspondência direta.

### Correspondência direta: estatísticas de envio {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Correspondência direta: estatísticas de envio"
>abstract="A tabela “Correspondência direta: estatísticas de envio” resume dados essenciais sobre mensagens de correspondência direta, como mensagens direcionadas ou entregues."

![](assets/campaign_direct_sending.png)

A variável **[!UICONTROL Correspondência direta - Estatísticas de envio]** A tabela fornece um resumo conciso dos dados essenciais relacionados às suas mensagens de correspondência direta, englobando as principais métricas, como o número de mensagens direcionadas e a contagem de mensagens entregues com êxito.

+++ Saiba mais sobre Correspondência direta - Envio de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução da correspondência direta recorrente. Para direcionar somente uma ou várias Correspondências diretas recorrentes, selecione-a no campo **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: Número de perfis de usuário qualificados como perfis de público alvo para suas mensagens de correspondência direta.

* **[!UICONTROL Enviado]**: Número total de envios para suas mensagens de correspondência direta.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam suas mensagens de correspondência direta.

+++

### Correspondência direta: motivos de erro {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Correspondência direta: motivos de erro"
>abstract="A tabela “Correspondência direta: motivos de erro” e seus gráficos permitem identificar os erros específicos que ocorreram durante o processo de envio."

![](assets/direct-mail-report_1.png)

A variável **[!UICONTROL Correspondência direta - Motivos de erro]** os gráficos e as tabelas fornecem os meios para identificar erros específicos que ocorreram durante o processo de envio das mensagens de correspondência direta, permitindo uma análise detalhada de quaisquer problemas encontrados.

### Correspondência direta: motivos de exclusão {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Correspondência direta: motivos de exclusão"
>abstract="A tabela “Correspondência direta: motivos de exclusão” e seus gráficos ilustram os vários fatores que levaram perfis de usuário excluídos do público-alvo a não receberem a mensagem."

![](assets/campaign_direct_excluded.png)

A variável **[!UICONTROL Correspondência direta - Motivos excluídos]** os gráficos e a tabela ilustram visualmente os vários fatores que resultaram na exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens de correspondência direta.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

## Recursos adicionais

* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](../campaigns/modify-stop-campaign.md)
* [Relatório em tempo real da campanha](campaign-live-report.md)
