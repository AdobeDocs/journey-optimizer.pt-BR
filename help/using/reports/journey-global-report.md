---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global da jornada
description: Saiba como usar os dados do relatório global do jornada
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '3365'
ht-degree: 4%

---

# Relatório global da jornada {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Relatório global da jornada"
>abstract="O Relatório global da jornada permite medir o impacto das jornadas em um período selecionado. O relatório é dividido em diferentes widgets detalhando o sucesso e os erros da jornada. Cada painel de relatórios pode ser modificado redimensionando ou removendo widgets."

Os relatórios globais, acessíveis na guia Todos os tempos, exibem eventos que ocorreram pelo menos duas horas atrás e abordam eventos em um período selecionado. Em comparação, os Relatórios em tempo real focalizam eventos que ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos a partir da ocorrência do evento.

O relatório global de Jornada pode ser acessado diretamente da sua jornada com o **[!UICONTROL Exibir relatório]** botão.

![](assets/report_journey.png)

A JORNADA **[!UICONTROL Relatório global]** será exibida com as seguintes guias:

* [Jornada](#journey-global)
* [Email](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [No aplicativo](#in-app-global)

A JORNADA **[!UICONTROL Relatório global]** O é dividido em diferentes widgets detalhando o sucesso e os erros da sua jornada. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global).

## Guia Jornada {#journey-global}

Da sua jornada **[!UICONTROL Relatório global]**, o **[!UICONTROL Jornada]** A guia fornece uma visualização clara dos dados de rastreamento mais importantes sobre a jornada.

### Desempenho da jornada {#journey-perfomance}

![](assets/journey_performance.png)

A variável **[!UICONTROL Desempenho da jornada]** O widget permite rastrear visualmente a trajetória dos perfis direcionados à medida que eles navegam pela jornada.

### Jornada estatísticas {#journey-statistics}

![](assets/journey_statistics.png)

A variável **[!UICONTROL Jornada estatísticas]** Os indicadores principais de desempenho (KPIs) funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua jornada. Isso inclui detalhes como a contagem de perfis inseridos e instâncias de jornadas individuais com falha, oferecendo um insight abrangente sobre a eficácia e o nível de engajamento da jornada.

+++ Saiba mais sobre métricas de Estatísticas do Jornada

* **[!UICONTROL Perfis inseridos]**: Número total de indivíduos que atingiram o evento de entrada da jornada.

* **[!UICONTROL Perfis encerrados]**: número total de indivíduos que saíram da jornada.

* **[!UICONTROL Falha na jornada individual]**: Número total de jornadas individuais que não foram executadas com êxito.

+++

### Desempenho da ação {#action-performance}

![](assets/journey_action_performance.png)

A variável **[!UICONTROL Desempenho da ação]** O widget representa as ações mais bem-sucedidas que ocorreram quando seu **[!UICONTROL Ações]** foram acionados.

### Principais ações {#top-actions}

![](assets/journey_top_actions.png)

A variável **[!UICONTROL Principais ações]** A tabela compila os dados essenciais sobre o **[!UICONTROL Ações]**. Fornece informações sucintas sobre a frequência e o desempenho de cada ação.

+++ Saiba mais sobre as principais métricas de ações

* **[!UICONTROL Ações executadas com sucesso]**: Número total de **[!UICONTROL Ações]** executado com sucesso para uma jornada.

* **[!UICONTROL Erro na ação]**: Número total de erros que ocorreram para **[!UICONTROL Ações]**.

+++

### Motivos de erro de ações {#action-error}

![](assets/journey_action_error.png)

A variável **[!UICONTROL Motivos de erro de ação]**  A tabela e o gráfico oferecem uma visão geral abrangente dos erros ocorridos durante a execução do **[!UICONTROL Ações]**.

### Eventos por origem {#events-origin}

![](assets/journey_events_origin.png)

A variável **[!UICONTROL Eventos por origem]** tabela e gráficos fornecem uma perspectiva detalhada sobre a recepção bem-sucedida de seus **[!UICONTROL Eventos]**. Através dessas representações visuais, você pode discernir precisamente qual de seus **[!UICONTROL Eventos]** foram recebidos com eficiência, oferecendo insights valiosos sobre o desempenho e o impacto de eventos individuais na jornada.

### Eventos recebidos por evento {#events-received}

![](assets/journey_event_received.png)

A variável **[!UICONTROL Eventos recebidos por evento]** permite identificar e analisar quais variáveis **[!UICONTROL Evento]** na jornada foi executado com eficácia, fornecendo insights valiosos sobre o desempenho e as taxas de sucesso de eventos individuais.

### Principais eventos {#top-events}

![](assets/journey_top_events.png)

A variável **[!UICONTROL Principais eventos]** A tabela compila os dados essenciais sobre o **[!UICONTROL Eventos]**. Ele fornece insights sucintos sobre a frequência e o desempenho de cada **[!UICONTROL Evento]**.

### Políticas de consentimento {#consent-policies}

![](assets/journey_consent.png)

A variável **[!UICONTROL Políticas de consentimento]** A tabela e o gráfico mostram o número de perfis excluídos de cada política em suas ações personalizadas. Isso fornece um insight claro sobre o impacto de cada política de consentimento nas exclusões de perfil.

Para obter mais informações sobre ações personalizadas, consulte [a documentação detalhada](../action/about-custom-action-configuration.md).

Observe que para que esses widgets apareçam nos relatórios do Jornada, será necessário redefinir seus painéis. Para fazer isso, clique em **[!UICONTROL Modificar]** depois **[!UICONTROL Redefinir]** na parte superior do relatório.

## Guia Email {#email-global}

Da sua jornada **[!UICONTROL Relatório global]**, o **[!UICONTROL E-mail]** A guia detalha as principais informações relacionadas aos emails enviados na jornada.

### Estatísticas de envio de email {#email-sending-statistics}

![](assets/journey_email_statistics.png)

A variável **[!UICONTROL Estatísticas de envio de email]** A tabela fornece um resumo abrangente de dados essenciais sobre emails em suas jornadas. Ele detalha as principais métricas, como o tamanho do público-alvo e o número de emails entregues com êxito, oferecendo insights valiosos sobre a eficácia e o alcance de seus emails e jornadas.

+++ Saiba mais sobre métricas de Estatísticas de envio de email

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução de jornada em caso de jornadas recorrentes. Para direcionar apenas uma ou várias recorrências, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: Número de perfis direcionados para qualquer ação, como enviar email ou SMS.

* **[!UICONTROL Enviado]**: número total de emails enviados para a jornada.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Taxa de entrega]**: porcentagem de emails enviados com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de emails enviados.

* **[!UICONTROL Taxa de rejeição]**: porcentagem de emails que foram rejeitados em comparação aos emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado, em comparação aos emails enviados.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Email: estatísticas de rastreamento {#email-tracking}

![](assets/journey_email_tracking.png)

A variável **[!UICONTROL Email - Estatísticas de rastreamento]** A tabela oferece uma conta detalhada da atividade do perfil relacionada aos emails incluídos na jornada. Isso inclui métricas sobre aberturas, cliques e outros indicadores de engajamento relevantes, oferecendo uma visualização abrangente de como os perfis interagem com seu conteúdo de email.

+++ Saiba mais sobre Email - Métricas de estatísticas de rastreamento

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução do email recorrente na jornada. Para direcionar apenas um ou vários emails recorrentes, selecione-o no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Aberturas]**: Número de vezes que seus emails foram abertos em uma jornada.

* **[!UICONTROL Aberturas únicas]**: porcentagem de emails abertos.

* **[!UICONTROL Taxa de abertura única]**: número total de emails abertos em comparação ao número de emails entregues.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

* **[!UICONTROL Cliques únicos]**: Número de recipients que clicaram em um conteúdo em seus emails.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a jornada.

* **[!UICONTROL Cancelamentos de assinatura]**: Número de cliques no link unsubscription.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que seus emails foram declarados como spam ou lixo eletrônico.

+++

### Email: desempenho de envio {#email-performance}

![](assets/journey_email_performance.png)

A variável **[!UICONTROL Email - Desempenho de envio]** O gráfico fornece uma visualização abrangente dos dados relacionados aos emails enviados em sua jornada, oferecendo insights sobre as métricas principais, como entregas e rejeições. Isso permite uma análise detalhada do processo de envio de email, fornecendo informações valiosas sobre a eficiência e o desempenho de suas jornadas.

+++ Saiba mais sobre Email - Envio de métricas de desempenho

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Tentativas]**: Número de emails na fila para tentativas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante um processo de envio, impedindo que ele fosse enviado para perfis.

+++

### Email - Categorias e motivos de rejeição {#email-bounce-categories}

![](assets/journey_email_bounce_categories.png)

A variável **[!UICONTROL Motivos de rejeição]** e **[!UICONTROL Categorias de rejeição]** os widgets compilam os dados disponíveis relacionados às mensagens rejeitadas, fornecendo insights detalhados sobre os motivos e categorias específicas por trás das rejeições de email.

Para obter mais informações sobre rejeições, consulte o [Lista de supressão](../reports/suppression-list.md) página.

+++ Saiba mais sobre Email - Métricas de categorias de rejeição

* **[!UICONTROL Rejeição permanente]**: o número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.

* **[!UICONTROL Rejeição leve]**: o número total de erros temporários, como uma caixa de entrada cheia.

* **[!UICONTROL Ignorado]**: o número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.

+++

### Email: motivos de erro {#email-errors}

![](assets/journey_email_error.png)

A variável **[!UICONTROL Motivos de erro]** gráficos e tabelas oferecem visibilidade dos erros específicos que ocorreram durante o processo de envio, fornecendo informações valiosas sobre a natureza e a ocorrência de erros.

### Email: motivos de exclusão {#email-excluded}

![](assets/journey_email_excluded.png)

A variável **[!UICONTROL Motivos excluídos]** os gráficos e a tabela apresentam uma visão abrangente dos diferentes fatores que resultaram na exclusão de perfis de usuário do público-alvo direcionado, resultando no não recebimento da mensagem.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### Enviados e entregues por domínio {#sent-domains}

![](assets/journey_email_sent_domains.png)

A variável  **[!UICONTROL Enviado e entregue por domínios]** A tabela e o gráfico fornecem um detalhamento dos emails no nível do domínio, oferecendo insights abrangentes sobre o desempenho dos emails.

+++ Saiba mais sobre métricas Enviado e entregue por domínios

* **[!UICONTROL Enviado]**: número total de envios para seus emails.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

+++

### Aberturas e cliques por domínio {#open-domains}

![](assets/journey_email_open_domains.png)

A variável  **[!UICONTROL Abrir e clicar por domínios]** O gráfico e a tabela mostram um detalhamento em nível de domínio do envolvimento dos perfis com o email, fornecendo insights valiosos sobre como domínios diferentes interagem com o conteúdo.

+++ Saiba mais sobre métricas de Abertura e cliques por domínios

* **[!UICONTROL Aberturas]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em um email.

+++

### Rejeições e erros por domínio {#bounces-domains}

![](assets/journey_email_bounce_domains.png)

A variável  **[!UICONTROL Rejeições e erros por domínios]** O gráfico e a tabela oferecem um detalhamento em nível de domínio de erros específicos encontrados durante o processo de envio, fornecendo uma análise detalhada dos problemas que ocorreram.

+++ Saiba mais sobre métricas de Rejeições e erros por domínios

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de emails enviados.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

+++

### Motivos de rejeição por domínio {#bounce-reasons-domains}

![](assets/journey_email_bounce_reasons_domain.png)

A variável  **[!UICONTROL Motivos de rejeição por domínio]** O gráfico e a tabela oferecem um detalhamento de dados em nível de domínio sobre erros temporários e permanentes, fornecendo insights detalhados sobre os motivos por trás das mensagens rejeitadas.

### Email: URL principal {#email-top}

![](assets/journey_email_top.png)

A variável **[!UICONTROL Email - URL superior]** O gráfico e a tabela fornecem uma visão geral abrangente dos URLs em seu email que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão do envolvimento do perfil com conteúdo específico em seus emails.

### Email - Otimização {#email-sto}

>[!NOTE]
>
>A variável **[!UICONTROL Otimização da hora de envio]** e **[!UICONTROL Otimizado vs. não otimizado]** Os widgets do só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimização da hora de envio]** e **[!UICONTROL Otimizado vs. não otimizado]** os widgets detalham o sucesso de seus emails dependendo do método de envio: otimizado ou normal.

+++ Saiba mais sobre Otimização de tempo de envio e Métricas otimizadas versus não otimizadas

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.
* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Enviado]**: número total de emails enviados para a jornada.

* **[!UICONTROL Aberturas]**: Número de vezes que seus emails foram abertos na jornada.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

+++

### Email - Ofertas {#email-offers}

>[!NOTE]
>
>Os widgets e as métricas de Ofertas só estarão disponíveis se uma decisão tiver sido inserida em um email. Para obter mais informações sobre o Gerenciamento de decisões, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

A variável **[!UICONTROL Estatísticas de ofertas]** e **[!UICONTROL Estatísticas detalhadas da oferta]** ao longo do tempo, os widgets medem o sucesso e o impacto da sua oferta no público-alvo direcionado. Ele detalha as principais informações relacionadas à sua mensagem com KPIs.

+++ Saiba mais sobre Email - Métricas de ofertas

* **[!UICONTROL Oferta enviada]**: número total de envios para a oferta.

* **[!UICONTROL Impressão da oferta]**: Número de vezes que a oferta foi aberta em seus emails.

* **[!UICONTROL Cliques de oferta]**: Número de vezes que uma oferta foi clicada em seus emails.

* **[!UICONTROL Nome do posicionamento]**: nome do posicionamento usado para exibir a oferta. Para obter mais informações sobre posicionamento, consulte esta [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nome da oferta]**: nome da oferta adicionada em seus emails. Para obter mais informações sobre posicionamento, consulte esta [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Oferta enviada]**: número total de envios para a oferta.

* **[!UICONTROL Taxa de impressões da oferta]**: Porcentagem de ofertas abertas em comparação ao número de ofertas enviadas.

* **[!UICONTROL Taxa de cliques da oferta]**: Porcentagem de usuários que interagiram com a oferta.

+++

## Guia Notificação por push {#push-global}

Da sua jornada **[!UICONTROL Relatório global]**, o **[!UICONTROL Notificação por push]** A guia detalha as informações principais relativas às notificações por push enviadas em sua jornada.

### Notificações por push: estatísticas de envio {#push-sending-stat}

![](assets/journey_push_sending.png)

A variável **[!UICONTROL Notificação por push - Estatísticas de envio]** A tabela fornece um resumo dos dados essenciais relacionados às suas notificações por push, incluindo as métricas principais, como o número de mensagens direcionadas e o número de mensagens entregues com êxito.

+++ Saiba mais sobre Notificação por push - Envio de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução de jornada em caso de jornadas recorrentes. Para direcionar apenas uma ou várias recorrências, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: Número de perfis direcionados para qualquer ação, como enviar email ou SMS.

* **[!UICONTROL Enviado]**: Número total de notificações por push enviadas.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Taxa de entrega]**: porcentagem de notificações por push enviadas com êxito.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Taxa de rejeição]**: Porcentagem de notificações por push que foram rejeitadas em comparação às notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Taxa de erro]**: Porcentagem de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado, em comparação ao envio de notificações por push.

* **[!UICONTROL Excluído]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Notificações por push: estatísticas de rastreamento {#push-tracking-stat}

A variável **[!UICONTROL Push - Estatísticas de rastreamento]** o widget oferece um instantâneo detalhado da atividade do perfil vinculada às suas notificações por push, fornecendo insights essenciais sobre a eficácia do engajamento e das notificações por push.

+++ Saiba mais sobre Notificação por push - Rastreamento de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução de jornada em caso de jornadas recorrentes. Para direcionar apenas uma ou várias recorrências, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Aberturas]**: Número de vezes que suas notificações por push foram abertas na jornada.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

+++

### Notificações por push: resumo de envio {#push-summary}

![](assets/journey_push_summary.png)

A variável **[!UICONTROL Notificação por push - Resumo de envio]** O gráfico oferece uma representação dinâmica, exibindo uma análise da atividade de notificações por push. Esta representação gráfica fornece um detalhamento abrangente das notificações por push enviadas.

+++ Saiba mais sobre Notificação por push - Envio de métricas de resumo

* **[!UICONTROL Aberturas]**: Número de vezes que suas notificações por push foram abertas na jornada.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

+++

### Notificações por push: motivos de erro {#push-error-reasons}

![](assets/journey_push_error.png)

A variável **[!UICONTROL Motivos de erro]** A tabela e os gráficos fornecem a capacidade de identificar os erros específicos que ocorreram durante o processo de envio de suas notificações por push, oferecendo insights detalhados sobre quaisquer problemas encontrados ao longo do caminho.

### Notificações por push: motivos de exclusão {#push-excluded}

![](assets/journey_push_excluded.png)

A variável **[!UICONTROL Motivos excluídos]** os gráficos e a tabela exibem os diferentes motivos que impediram os perfis de usuário, excluídos dos perfis direcionados, de receber suas notificações por push.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### Notificações por push: detalhamento por plataforma {#push-breakdown}

![](assets/journey_push_breakdown.png)

A variável **[!UICONTROL Detalhamento por plataforma]** O gráfico e a tabela fornecem uma análise detalhada do sucesso de suas notificações por push, oferecendo insights com base no sistema operacional do seu perfil. Esse detalhamento melhora a sua compreensão do desempenho das notificações por push em diferentes plataformas.

### Notificação por push - Otimização {#push-sto}

>[!NOTE]
>
>A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  Os widgets do só estarão disponíveis se a opção Send-Time Otimization estiver ativada para o seu delivery. Para obter mais informações sobre a Otimização de tempo de envio, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

A variável **[!UICONTROL Otimizado vs. não otimizado]** e **[!UICONTROL Otimização da hora de envio]**  os widgets detalham as principais informações relacionadas à sua mensagem, sejam elas otimizadas ou não.

+++ Saiba mais sobre Notificação por push - Métricas de otimização

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Aberturas]**: Número de vezes que suas notificações por push foram abertas na jornada.

* **[!UICONTROL Ações]**: Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.

* **[!UICONTROL Entregue]**: Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

+++

## Guia SMS {#sms-global}

### SMS: estatísticas de envio {#sms-sending-stat}

![](assets/journey_sms_sending.png)

A variável **[!UICONTROL SMS - Estatísticas de envio]** A tabela fornece um resumo conciso dos dados essenciais relacionados às suas mensagens SMS, englobando as métricas principais, como o número de mensagens direcionadas e a contagem de mensagens entregues com êxito.

+++ Saiba mais sobre SMS - Envio de métricas de estatísticas

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução de jornada em caso de jornadas recorrentes. Para direcionar apenas uma ou várias recorrências, selecione-a no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Direcionado]**: Número de perfis de usuário que se qualificam como perfis de destino para suas mensagens SMS.

* **[!UICONTROL Excluído]**: Número de perfis de usuário, excluídos dos perfis direcionados, que não receberam suas mensagens SMS.

* **[!UICONTROL Enviado]**: Número total de mensagens SMS enviadas para a jornada.

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

+++

### SMS - Estatísticas de rastreamento {#sms-tracking-stat}

![](assets/journey_sms_tracking.png)

A variável **[!UICONTROL SMS - Estatísticas de rastreamento]** O widget fornece uma visão geral detalhada das principais informações relacionadas ao envolvimento dos visitantes com os URLs, oferecendo insights sobre a eficácia das mensagens SMS.

* **[!UICONTROL Tempo de execução]**: hora de início de cada execução do SMS recorrente. Para direcionar apenas um ou vários SMS recorrentes, selecione-o no **[!UICONTROL Tempo de execução]** menu suspenso.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas mensagens SMS.

### SMS: desempenho por data {#sms-performance-date}

![](assets/journey_sms_performance.png)

A variável **[!UICONTROL SMS - Desempenho por data]** o widget oferece uma visão geral detalhada das principais informações relacionadas às suas mensagens, apresentadas por meio de um gráfico, fornecendo insights sobre as tendências de desempenho em períodos específicos.

+++ Saiba mais sobre SMS - Desempenho por métricas de data

* **[!UICONTROL Enviado]**: Número total de mensagens SMS enviadas para a jornada

* **[!UICONTROL Rejeições]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

+++

### SMS: motivos de rejeições {#sms-bounce}

![](assets/journey_sms_bounce_reasons.png)

A variável **[!UICONTROL Motivos de rejeições]** Os gráficos e as tabelas fornecem uma visão geral abrangente dos dados relacionados às mensagens SMS rejeitadas, fornecendo insights valiosos sobre os motivos específicos por trás das instâncias de rejeições de mensagens SMS.

### SMS: motivos de erro {#sms-error}

![](assets/journey_sms_error.png)

A variável **[!UICONTROL Motivos de erro]** Os gráficos e as tabelas permitem identificar os erros específicos que ocorreram durante o processo de envio de suas mensagens SMS, facilitando uma análise completa de todos os problemas encontrados.

### SMS: motivos de exclusão {#sms-excluded}

![](assets/journey_sms_excluded.png)

A variável **[!UICONTROL Motivos excluídos]** Os gráficos e as tabelas representam visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens SMS.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### SMS: cliques por link {#sms-clicks}

![](assets/journey_sms_clicks.png)

A variável **[!UICONTROL SMS - Cliques por links]** O widget oferece informações essenciais sobre o envolvimento dos visitantes com os URLs incluídos em suas mensagens, fornecendo informações valiosas sobre quais links atraem mais interação.

## Guia No aplicativo {#in-app-global}

Da sua Jornada **[!UICONTROL Relatório global]**, o **[!UICONTROL No aplicativo]** A guia detalha as principais informações relacionadas às mensagens no aplicativo enviadas em suas jornadas.

### Desempenho no aplicativo {#inapp-performance}

![](assets/journey_inapp_performance.png)

A variável **[!UICONTROL Desempenho no aplicativo]**  Os KPIs fornecem insights essenciais sobre o envolvimento dos perfis com as mensagens no aplicativo, fornecendo métricas essenciais para avaliar a eficácia e o impacto das mensagens no aplicativo incluídas na jornada.

+++ Saiba mais sobre as métricas no aplicativo - Desempenho por data

* **[!UICONTROL Impressões exclusivas]**: número de usuários únicos para os quais a mensagem no aplicativo foi exibida.

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo exibidas para todos os usuários.

  >[!NOTE]
  >
  >Para garantir que uma Impressão seja contada, o usuário deve atender a dois critérios:
  >* Qualificação dentro da experiência no aplicativo, obtida ao atingir a atividade específica no aplicativo em sua jornada.
  >* Cumprimento das condições especificadas nas regras de acionador.
  > 
  >Devido ao segundo critério, pode haver variações notáveis entre o número de perfis segmentados e a contagem de impressões únicas.

* **[!UICONTROL Interação]**: número de envolvimentos com a mensagem no aplicativo. Isso inclui qualquer ação realizada pelos usuários, como cliques, rejeições ou quaisquer outras interações.
+++

### Resumo no aplicativo {#inapp-summary}

![](assets/journey_inapp_summary.png)

A variável **[!UICONTROL Resumo no aplicativo]** O gráfico ilustra a progressão de suas impressões e interações no aplicativo durante o período especificado, fornecendo uma visão geral abrangente do desempenho das mensagens no aplicativo.

### Interações por tipo {#interactions-type}

![](assets/journey_inapp_interactions.png)

A variável **[!UICONTROL Interações por tipo]** Os gráficos e a tabela fornecem uma conta detalhada de como os perfis interagiram com a mensagem no aplicativo, rastreando ações como cliques, rejeições ou qualquer outra forma de envolvimento.
