---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global da campanha
description: Saiba como usar os dados do relatório global do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 51cbe27f-3f3f-471e-a5d9-e3a88fcfdd68
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '4251'
ht-degree: 2%

---

# Relatório de campanhas {#campaign-global-report-cja}

A variável **Relatório de campanha** O atua como um painel abrangente, fornecendo uma análise detalhada das principais métricas associadas à sua campanha. Ele inclui dados como contagens de cliques, mensagens enviadas, números de perfil e ações tomadas. Ao oferecer uma visão geral completa da eficácia e dos níveis de engajamento da sua campanha, o relatório garante uma compreensão completa do desempenho geral da campanha.

Os relatórios do Campaign podem ser acessados diretamente do Campaign com o **[!UICONTROL Relatórios]** botão.

![](assets/gs-cja-report-2.png)

A variável **Relatório de campanha** será exibida com as seguintes guias, dependendo do canal escolhido:

* [Campaign](#campaign-global)
* [Experimentação](#experimentation)
* [Email](#email-global)
* [SMS](#sms)
* [Notificações por push](#push-notification)
* [Correspondência direta](#direct-mail)
* [Web](#web)

Para saber mais sobre o Customer Journey Analytics Workspace e como filtrar e analisar dados, consulte [esta página](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Campaign {#campaign-global}

### KPIs de campanha {#campaign-kpis}

![](assets/cja-email-kpis.png)

A variável **[!UICONTROL Campaign]** Os indicadores principais de desempenho (KPIs) funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua campanha. Isso abrange detalhes como a contagem de cliques e o número de mensagens entregues, oferecendo uma visão abrangente da eficiência e do nível de engajamento da campanha.

Os KPIs variam com base nos canais usados em sua campanha.

+++ Saiba mais sobre as métricas de KPIs do Campaign

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a mensagem.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em sua mensagem.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

+++

### Visão geral da campanha {#delivery-global}

![](assets/cja-campaign-overview.png)

A variável **[!UICONTROL Visão geral da campanha]** Essa tabela serve como um painel abrangente, oferecendo um detalhamento das principais métricas relacionadas à sua campanha. Isso inclui informações essenciais, como o número de perfis e as ações entregues, fornecendo uma compreensão completa do desempenho e do envolvimento da campanha.

Observe que as métricas variam com base nos canais usados na campanha.

+++ Saiba mais sobre as métricas de visão geral do Campaign

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para suas mensagens.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a mensagem.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em sua mensagem.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em sua mensagem.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições para canais de saída]**: Número total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++

### Resultados do funil de campanha {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

A variável **[!UICONTROL Resultados do funil de campanha]** o gráfico apresenta uma análise detalhada do envolvimento dos perfis com as mensagens, oferecendo insights valiosos sobre como vários perfis interagiram com o conteúdo.

+++ Saiba mais sobre as métricas de resultados do funil do Campaign

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em sua mensagem.
+++

### Rótulo do link rastreado {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

A variável **[!UICONTROL Rótulo do link rastreado]** A tabela oferece insights essenciais sobre o envolvimento dos visitantes com os URLs incluídos em suas mensagens, fornecendo informações valiosas sobre quais links atraem mais interação.

+++ Saiba mais sobre métricas de rótulo de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em sua mensagem.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em sua mensagem.

+++

## Experimentação {#experimentation}

A variável **[!UICONTROL Experimentação]** A guia fornece informações importantes sobre o desempenho de cada variante e identifica a mais bem-sucedida.

Observe que a definição do melhor desempenho pode levar algum tempo. Se o experimento não for bem-sucedido, ele será definido como **Inconclusivo**.

![](assets/cja-experimentation-1.png)

### KPIs de experimentação {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

A variável **[!UICONTROL Experimentação]** Os indicadores principais de desempenho (KPIs) funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua experimentação.

+++ Saiba mais sobre métricas de KPIs de experimentação

* **[!UICONTROL Elevação]**: Medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é igual ao tratamento inicial. [Saiba mais](../content-management/experiment-calculations.md#understand-confidence)

+++

### Variante por cliques de entrada {#variant-inbound}

![](assets/cja-experimentation-variants.png)

A variável **[!UICONTROL Variante por cliques de entrada]** o widget detalha o desempenho de cada variante.
Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).

+++ Saiba mais sobre as métricas Variante por cliques de entrada

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para suas mensagens.

* **[!UICONTROL Cliques de entrada]**: Contagem total de cliques nos canais de saída.

* **[!UICONTROL Índice de conversão]**: Valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis.

* **[!UICONTROL Elevação]**: Medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é igual ao tratamento inicial. [Saiba mais](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:
* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### Taxa de conversão para cliques de entrada {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

A variável **[!UICONTROL Intervalo de confiança]** O gráfico mede a incerteza em torno da melhoria. Ela detalha a diferença percentual de desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../content-management/experiment-calculations.md#confidence-intervals).

## Email {#email-global}

### Tendência de Entregas vs. Cliques {#delivered-click}

![](assets/cja-email-delivered-click.png)

A variável **[!UICONTROL Tendência de Entregas vs. Cliques]** O gráfico apresenta uma análise detalhada do envolvimento dos perfis com seus emails, oferecendo insights valiosos sobre como os perfis interagem com seu conteúdo.

+++ Saiba mais sobre métricas de tendência Entregue versus Clique

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

+++


### Status da entrega {#delivery-status}

![](assets/cja-email-delivery-status.png)

A variável **[!UICONTROL Status da entrega]** o gráfico fornece uma visualização abrangente dos dados relacionados aos emails enviados em sua campanha, oferecendo insights sobre as métricas principais, como entregas e rejeições. Isso permite uma análise detalhada do processo de envio de email, fornecendo informações valiosas sobre a eficiência e o desempenho de suas campanhas.

+++ Saiba mais sobre Métricas de status de entrega

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Rejeições para canais de saída]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante um processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Estatísticas de envio {#sending-statistics-email}

![](assets/cja-email-sending-stat.png)

A variável **[!UICONTROL Estatísticas de envio]** A tabela fornece um resumo abrangente de dados essenciais sobre emails em suas campanhas. Ele detalha as principais métricas, como as interações com seus emails e o número de emails entregues com êxito, oferecendo insights valiosos sobre a eficácia e o alcance de seus emails e campanhas.

+++ Saiba mais sobre como enviar métricas de estatísticas

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para suas mensagens.

* **[!UICONTROL Direcionado]**: número total de emails processados durante o processo de envio.

* **[!UICONTROL Envios]**: Número total de envios para o seu email.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições para canais de saída]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Estatísticas de rastreamento {#tracking-statistics-email}

![](assets/cja-email-track-stat.png)

A variável **[!UICONTROL Email - Estatísticas de rastreamento]** A tabela oferece uma conta detalhada da atividade do perfil relacionada aos emails incluídos na campanha. Isso inclui métricas sobre aberturas, cliques e outros indicadores de engajamento relevantes, oferecendo uma visualização abrangente de como os perfis interagem com seu conteúdo de email.

+++ Saiba mais sobre métricas de estatísticas de rastreamento

* **[!UICONTROL Taxa de cliques (CTR)]**: porcentagem de usuários que interagiram com o email.

* **[!UICONTROL Taxa de abertura de cliques (CTOR)]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em um email.

* **[!UICONTROL Aberturas de email]**: Número de vezes que seus emails foram abertos em uma campanha.

* **[!UICONTROL Aberturas de email únicas]**: porcentagem de emails abertos.

* **[!UICONTROL Reclamações de spam]**: Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.

* **[!UICONTROL Cancelamentos de assinatura]**: Número de cliques no link unsubscription.

+++


### Domínios de email {#email-domains}

![](assets/cja-email-email-domains.png)

A variável **[!UICONTROL Domínios de email]** A tabela oferece um detalhamento detalhado de emails categorizados por domínio, fornecendo insights abrangentes sobre as métricas de desempenho de suas campanhas de email. Essa análise abrangente permite que você entenda o comportamento de domínios diferentes em resposta ao seu conteúdo de email.

+++ Saiba mais sobre métricas de domínios de email

* **[!UICONTROL Envios]**: Número total de envios para o seu email.

* **[!UICONTROL Entregue]**: Número de emails enviados com êxito, em relação ao número total de emails enviados.

* **[!UICONTROL Aberturas de email]**: Número de vezes que seus emails foram abertos em uma campanha.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

* **[!UICONTROL Rejeições para canais de saída]**: Número total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de emails enviados.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.
+++

### Rótulos de link rastreado {#track-link-label}

![](assets/cja-email-tracked-link.png)

A variável **[!UICONTROL Rótulos de link rastreado]** A tabela oferece uma visão geral abrangente dos rótulos de link em seus emails, destacando aqueles que geram o maior tráfego de visitantes. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre métricas de rótulos de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em um email.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

+++

### URLs do link rastreado {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

A variável **[!UICONTROL URLs de link rastreado]** A tabela fornece uma visão geral abrangente dos URLs em seu email que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão do envolvimento do perfil com conteúdo específico em seus emails.

+++ Saiba mais sobre métricas de URLs de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em um email.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em seus emails.

* **[!UICONTROL Exibições]**: Número de vezes que o email foi aberto.

* **[!UICONTROL Exibições únicas]**: Número de vezes que o email foi aberto, várias interações de um perfil não são consideradas.

+++

### Assuntos de email {#email-subjects}

![](assets/cja-email-subject.png)

A variável **[!UICONTROL Assuntos de email]** a tabela apresenta uma visão geral completa de assuntos de email que atraíram o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas de assuntos de email

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para seus emails.

+++

### Motivos para exclusão {#excluded-reasons}

A variável **[!UICONTROL Motivos excluídos]** a tabela apresenta uma visualização abrangente dos diferentes fatores que resultaram na exclusão de perfis de usuário do público-alvo, resultando no não recebimento da mensagem.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

### Motivos de rejeição {#bounce-reasons-email}

A variável **[!UICONTROL Motivos de rejeição]** A tabela compila os dados disponíveis relacionados às mensagens rejeitadas, fornecendo insights detalhados sobre os motivos específicos por trás das rejeições de email.

Para obter mais informações sobre rejeições, consulte o [Lista de supressão](../reports/suppression-list.md) página.

### Motivos do erro {#error-reasons-email}

A variável **[!UICONTROL Motivos de erro]** A tabela oferece visibilidade dos erros específicos que ocorreram durante o processo de envio, fornecendo informações valiosas sobre a natureza e a ocorrência de erros.

## SMS {#sms}

### Tendência de Entregas vs. Cliques {#delivered-click-sms}

A variável **[!UICONTROL Tendência de Entregas vs. Cliques]** O gráfico apresenta uma análise detalhada do envolvimento dos perfis com seus emails, oferecendo insights valiosos sobre como os perfis interagem com seu conteúdo.

+++ Saiba mais sobre métricas de tendência Entregue versus Clique

* **[!UICONTROL Entregue]**: Número de mensagens SMS enviadas com êxito, em relação ao número total de mensagens SMS.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas mensagens SMS.

+++

### Status da entrega {#delivery-status-sms}

A variável **[!UICONTROL Status da entrega]** A tabela oferece uma conta detalhada da atividade do perfil relacionada às suas campanhas de SMS. Isso inclui métricas sobre entregas, cliques e outros indicadores de envolvimento relevantes, oferecendo uma visualização abrangente de como os perfis interagem com seu conteúdo de SMS.

+++ Saiba mais sobre Métricas de status de entrega

* **[!UICONTROL Entregue]**: Número de mensagens SMS enviadas com êxito, em relação ao número total de mensagens SMS.

* **[!UICONTROL Rejeições para canais de saída]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Rótulos de link rastreado {#track-link-label-sms}

A variável **[!UICONTROL Rótulos de link rastreado]** A tabela oferece uma visão geral abrangente dos rótulos de links em suas mensagens SMS, destacando aquelas que geram o maior tráfego de visitantes. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre métricas de rótulos de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em sua mensagem SMS.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas mensagens SMS.

+++

### URLs do link rastreado {#track-link-url-sms}

A variável **[!UICONTROL URLs de link rastreado]** A tabela fornece uma visão geral abrangente dos URLs em suas mensagens SMS que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão da participação do perfil com conteúdo específico em suas mensagens SMS.

+++ Saiba mais sobre métricas de URLs de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo em sua mensagem SMS.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas mensagens SMS.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++

### Mensagem por SMS de entrada {#sms-inbound}

A variável **[!UICONTROL Mensagem de entrada de SMS]** A tabela apresenta uma visão geral completa de quais mensagens SMS atraíram o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas de mensagem de entrada SMS

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de destino para suas mensagens SMS.

+++

### Tipo de mensagem SMS {#sms-message-type}

A variável **[!UICONTROL Tipo de mensagem SMS]** A tabela apresenta uma visão geral completa de qual tipo de mensagem SMS atraiu o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas do tipo de mensagem SMS

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de destino para suas mensagens SMS.

+++

### Provedores de SMS {#sms-providers}

A variável **[!UICONTROL Provedores de SMS]** A tabela apresenta uma visão geral completa de quais provedores de SMS atraíram o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas de provedores SMS

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de destino para suas mensagens SMS.

+++

### Motivos de rejeição {#bounce-reasons-sms}

A variável **[!UICONTROL Motivos de rejeições]** A tabela fornece uma visão geral abrangente dos dados relacionados às mensagens SMS rejeitadas, fornecendo insights valiosos sobre os motivos específicos por trás das instâncias de rejeições de mensagens SMS.

### Motivos do erro {#error-reasons-sms}

A variável **[!UICONTROL Motivos de erro]** A tabela permite identificar os erros específicos que ocorreram durante o processo de envio de suas mensagens SMS, facilitando uma análise completa de todos os problemas encontrados.

### Motivos para exclusão {#excluded-reasons-sms}

A variável **[!UICONTROL Excluir motivos]** A tabela representa visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens SMS.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

## Notificações por push {#push-notification}

### Estatísticas de envio {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

A variável **[!UICONTROL Estatísticas de envio]** A tabela fornece um resumo abrangente de dados essenciais sobre suas campanhas de notificação por push. Ele detalha as principais métricas, como o tamanho do público-alvo e o número de notificações por push entregues com êxito, oferecendo insights valiosos sobre a eficácia e o alcance da notificação por push.

+++ Saiba mais sobre como enviar métricas de estatísticas

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de destino para suas notificações por push.

* **[!UICONTROL Direcionado]**: número total de notificações por push processadas durante a análise.

* **[!UICONTROL Envios]**: número total de envios para a notificação por push.

* **[!UICONTROL Entregue]**: número de notificações por push enviadas com êxito em relação ao número total de notificações por push enviadas.

* **[!UICONTROL Rejeições para canais de saída]**: Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de notificações por push.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram que impediram o envio para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Estatísticas de rastreamento {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

A variável **[!UICONTROL Estatísticas de rastreamento]** A tabela oferece um instantâneo detalhado da atividade do perfil vinculada às suas notificações por push, fornecendo insights essenciais sobre a eficácia das notificações por push e de engajamento.

+++ Saiba mais sobre métricas de estatísticas de rastreamento

* **[!UICONTROL Taxa de cliques (CTR)]**: porcentagem de usuários que interagiram com as notificações por push.

* **[!UICONTROL Taxa de abertura de cliques (CTOR)]**: Número de vezes que as notificações por push foram abertas.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas notificações por push.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas notificações por push.

<!--
* **[!UICONTROL Push custom actions]**: 
-->
+++

### Rótulos de link rastreado {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

A variável **[!UICONTROL Rótulos de link rastreado]** A tabela oferece uma visão geral abrangente dos rótulos de links em suas notificações por push, destacando aquelas que geram o maior tráfego de visitantes. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre métricas de rótulos de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas notificações por push.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas notificações por push.

+++

### URLs do link rastreado {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

A variável **[!UICONTROL URLs de link rastreado]** A tabela fornece uma visão geral abrangente dos URLs em suas notificações por push que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão do envolvimento do perfil com conteúdo específico em suas notificações por push.

+++ Saiba mais sobre métricas de URLs de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas notificações por push.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado em suas notificações por push.

+++

### Motivos de rejeição {#bounce-reasons-push}

A variável **[!UICONTROL Motivos de rejeições]** A tabela fornece uma visão geral abrangente dos dados relacionados às notificações por push rejeitadas, fornecendo insights valiosos sobre os motivos específicos por trás das instâncias de rejeições de notificações por push.

### Motivos do erro {#error-reasons-push}

A variável **[!UICONTROL Motivos de erro]** A tabela permite identificar os erros específicos que ocorreram durante o processo de envio de suas notificações por push, facilitando uma análise completa de todos os problemas encontrados.

### Motivos para exclusão {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

A variável **[!UICONTROL Excluir motivos]** A tabela representa visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas notificações por push.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

## No aplicativo {#in-app}

### Tendência de impressão e clique {#impression-click-trend}

![](assets/cja-inapp-impressions-click.png)

A variável **[!UICONTROL Tendência de impressão e clique]** O gráfico apresenta uma análise detalhada do envolvimento dos perfis com as mensagens no aplicativo, oferecendo insights valiosos sobre como os perfis interagem com o seu conteúdo.

+++ Saiba mais sobre métricas de tendência de Impressão e Clique

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas mensagens no aplicativo.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

+++

### Cliques {#clicks-inapp}

A variável **[!UICONTROL Cliques]** O gráfico exibe métricas de cliques no aplicativo, ilustrando o número total de cliques no conteúdo e o número de perfis únicos que clicaram no conteúdo.

+++ Saiba mais sobre métricas de cliques

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas mensagens no aplicativo

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas mensagens no aplicativo.

+++

### Exibir {#display-inapp}

A variável **[!UICONTROL Exibições]** O gráfico ajuda você a entender o alcance geral da mensagem e o número de perfis únicos que se envolvem com ela.

+++ Saiba mais sobre Métricas de exibição

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++

### Dados de rastreamento {#tracking-data-inapp}

A variável **[!UICONTROL Dados de rastreamento]** A tabela oferece um instantâneo detalhado da atividade do perfil vinculada às mensagens no aplicativo, fornecendo insights essenciais sobre a participação e a eficácia das mensagens no aplicativo.

+++ Saiba mais sobre Rastreamento de métricas de dados

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de destino para suas mensagens no aplicativo.

* **[!UICONTROL Taxa de cliques (CTR)]**: porcentagem de usuários que interagiram com as mensagens no aplicativo.

* **[!UICONTROL Taxa de abertura de cliques (CTOR)]**: Número de vezes que as mensagens no aplicativo foram abertas.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas mensagens no aplicativo.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas mensagens no aplicativo.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

* **[!UICONTROL Envios]**: Número total de envios para suas mensagens no aplicativo.

<!--
* **[!UICONTROL Inbound triggered]**: 

* **[!UICONTROL Inbound dismisses]**: 
-->
+++

### Rótulos de link rastreado {#track-link-label-inapp}

![](assets/cja-inapp-tracked-link-labels.png)

A variável **[!UICONTROL Rótulos de link rastreado]** A tabela oferece uma visão geral abrangente dos rótulos de link em suas mensagens no aplicativo, destacando aquelas que geram o maior tráfego de visitantes. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre métricas de rótulos de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas mensagens no aplicativo.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas mensagens no aplicativo.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++

### URLs do link rastreado {#track-link-url-inapp}

![](assets/cja-inapp-tracked-link-urls.png)

A variável **[!UICONTROL URLs de link rastreado]** Essa tabela fornece uma visão geral abrangente dos URLs nas mensagens no aplicativo que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão da participação do perfil com conteúdo específico em suas mensagens no aplicativo.

+++ Saiba mais sobre métricas de URLs de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas mensagens no aplicativo.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas mensagens no aplicativo.

+++

## Correspondência direta {#direct-mail}

### Estatísticas de envio {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

A variável **[!UICONTROL Estatísticas de envio]** A tabela fornece um resumo abrangente dos dados essenciais relativos às campanhas de correspondência direta. Ele detalha as principais métricas, como o tamanho do público-alvo e o número de correspondência direta entregue com sucesso, oferecendo informações valiosas sobre a eficácia e o alcance das mensagens de correspondência direta.

+++ Saiba mais sobre como enviar métricas de estatísticas

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para suas mensagens.

* **[!UICONTROL Direcionado]**: Número total de mensagens de correspondência direta processadas durante o processo de envio.

* **[!UICONTROL Envios]**: Número total de envios para suas mensagens de correspondência direta.

* **[!UICONTROL Entregue]**: Número de mensagens de correspondência direta enviadas com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado para perfis.

* **[!UICONTROL Exclusões de saída]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Status da entrega {#delivery-status-directmail}

![](assets/cja-direct-delivery-status.png)

A variável **[!UICONTROL Status da entrega]** o gráfico fornece uma visualização abrangente dos dados relacionados às mensagens de correspondência direta enviadas na campanha, oferecendo insights sobre as principais métricas, como entregas e erros. Isso permite uma análise detalhada do processo de envio de mensagens de correspondência direta, fornecendo informações valiosas sobre a eficiência e o desempenho de suas campanhas.

+++ Saiba mais sobre Métricas de status de entrega

* **[!UICONTROL Entregue]**: Número de mensagens de correspondência direta enviadas com êxito em relação ao número total de mensagens de correspondência direta enviadas.

* **[!UICONTROL Erros de saída]**: Número total de erros que ocorreram durante um processo de envio, impedindo que suas mensagens de correspondência direta fossem enviadas para perfis.

* **[!UICONTROL Exclusões não vinculadas]**: Número de perfis excluídos pelo Adobe Journey Optimizer.

+++

### Motivos do erro {#error-reasons-directmail}

A variável **[!UICONTROL Motivos de erro]** A tabela permite identificar os erros específicos que ocorreram durante o processo de envio de suas mensagens de correspondência direta, facilitando uma análise completa de todos os problemas encontrados.

### Motivos para exclusão {#exclude-reasons-directmail}

[](assets/cja-direct-excluded.png)

A variável **[!UICONTROL Excluir motivos]** A tabela representa visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens de correspondência direta.

Consulte [esta página](exclusion-list.md) para obter a lista abrangente dos motivos de exclusão.

## Web {#web}

### Tendência de impressão e clique {#impressions-web}

![](assets/cja-web-impression.png)

A variável **[!UICONTROL Tendência de impressão e clique]** O gráfico apresenta uma análise detalhada do envolvimento dos perfis com as páginas da Web, oferecendo insights valiosos sobre como os perfis interagem com o seu conteúdo.

+++ Saiba mais sobre métricas de tendência de Impressão e Clique

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas páginas da Web.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

+++

### Cliques {#clicks-web}

![](assets/cja-web-clicks.png)

A variável **[!UICONTROL Cliques]** O gráfico exibe as métricas de clique na página da Web, ilustrando o número total de cliques no conteúdo e o número de perfis únicos que clicaram no conteúdo.

+++ Saiba mais sobre métricas de cliques

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas suas páginas da Web.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas páginas da Web.

+++

### Exibições {#displays-web}

![](assets/cja-web-displays.png)

A variável **[!UICONTROL Exibições]** O gráfico ajuda você a entender o alcance geral da mensagem e o número de perfis únicos que se envolvem com ela.

+++ Saiba mais sobre Métricas de exibição

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++


### Dados de rastreamento {#track-data-web}

![](assets/cja-web-tracking-data.png)

A variável **[!UICONTROL Dados de rastreamento]** A tabela oferece um instantâneo detalhado da atividade do perfil vinculada às suas páginas da Web, fornecendo insights essenciais sobre o engajamento e a eficácia das páginas da Web.

+++ Saiba mais sobre Rastreamento de métricas de dados

* **[!UICONTROL Pessoas]**: Número de perfis de usuário que se qualificam como perfis de público-alvo para suas páginas da Web.

* **[!UICONTROL Taxa de cliques (CTR)]**: porcentagem de usuários que interagiram com as páginas da Web.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas páginas da Web.

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas suas páginas da Web.

* **[!UICONTROL Exibições]**: Número de vezes que a página da Web foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a página da Web foi aberta, várias interações de um perfil não são consideradas.

+++

### Rótulos de link rastreado {#track-link-web}

![](assets/cja-web-tracked-link-labels.png)

A variável **[!UICONTROL Rótulos de link rastreado]** A tabela oferece uma visão geral abrangente dos rótulos de link em suas páginas da Web, destacando aquelas que geram o maior tráfego de visitante. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre métricas de rótulos de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas suas páginas da Web.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas páginas da Web.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++

### URLs do link rastreado {#track-url-web}

![](assets/cja-web-tracked-link-urls.png)

A variável **[!UICONTROL URLs de link rastreado]** A tabela fornece uma visão geral abrangente dos URLs nas páginas da Web que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, aprimorando sua compreensão do envolvimento do perfil com conteúdo específico em suas páginas da Web.

+++ Saiba mais sobre métricas de URLs de link rastreado

* **[!UICONTROL Cliques únicos]**: Número de perfis que clicaram em um conteúdo nas suas páginas da Web.

* **[!UICONTROL Cliques]**: Número de vezes que um conteúdo foi clicado nas páginas da Web.

* **[!UICONTROL Exibições]**: Número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições únicas]**: Número de vezes que a mensagem foi aberta, várias interações de um perfil não são consideradas.

+++
