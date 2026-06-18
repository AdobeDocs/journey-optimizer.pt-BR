---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar dados de SMS no relatório do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bd743a3b-0317-45d9-8e76-98d5cc258752
TQID: https://experienceleague.adobe.com/dFM14bh1Yil9GUsCk3mkcqz6QNH3fUWmQCNtj-FnWfA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f10f2b6cbad242efca31c84ce8adf5a615f57c1e
workflow-type: tm+mt
source-wordcount: 955
ht-degree: 2%

---

# Relatório de campanha por SMS {#campaign-global-report-cja-sms}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como ler o relatório de campanha de SMS no Adobe Journey Optimizer para analisar tendências de entrega e cliques, status da entrega, links rastreados, mensagens de entrada e motivos de rejeição, erro e exclusão de suas mensagens SMS.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Você pode acessar o relatório de campanha de SMS clicando no botão **[!UICONTROL Relatórios]** da campanha e selecionando **[!UICONTROL Exibir relatório de todos os tempos]**. [Saiba mais](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Tendência de Entregas vs. Cliques {#delivered-click-sms}

![](assets/cja-campaign-sms-delivered.png)

O gráfico de tendência **[!UICONTROL Entregues versus Cliques]** apresenta uma análise detalhada do envolvimento dos seus perfis com seus emails, oferecendo insights valiosos sobre como os perfis interagem com seu conteúdo.

+++ Saiba mais sobre métricas de tendência Entregue versus Clique

* **[!UICONTROL Entregues]**: número de mensagens SMS enviadas com êxito em relação ao número total de mensagens SMS.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em suas mensagens SMS.

+++

## Status da entrega {#delivery-status-sms}

![](assets/cja-campaign-sms-status.png)

A tabela **[!UICONTROL Status da entrega]** oferece uma conta detalhada da atividade do perfil relacionada às suas campanhas de SMS. Isso inclui métricas sobre entregas, cliques e outros indicadores de envolvimento relevantes, oferecendo uma visualização abrangente de como os perfis interagem com seu conteúdo de SMS.

+++ Saiba mais sobre Métricas de status de entrega

* **[!UICONTROL Entregues]**: número de mensagens SMS enviadas com êxito em relação ao número total de mensagens SMS.

* **[!UICONTROL Rejeições]**: total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de mensagens SMS enviadas.

* **[!UICONTROL Enviar erros]**: Número total de erros que ocorreram, impedindo que fossem enviados a perfis.

* **[!UICONTROL Enviar exclusões]**: número de perfis excluídos pelo Adobe Journey Optimizer.

+++

## Visão geral da campanha {#campaign-global}

A tabela **[!UICONTROL Visão geral da campanha]** serve como um painel para o desempenho do SMS em sua campanha. Ele resume perfis direcionados, métricas de cliques e click-throughs (incluindo cliques estimados que excluem tráfego de interação de bot e não humano) e resultados do delivery, como rejeições, erros de envio e exclusões.

+++ Saiba mais sobre as métricas de visão geral do Campaign

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a mensagem.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em sua mensagem.

* **[!UICONTROL Cliques únicos]**: número de perfis únicos que clicaram em pelo menos um conteúdo na mensagem móvel.

* **[!UICONTROL Cliques estimados]**: número de vezes que um conteúdo foi clicado em sua mensagem, excluindo o tráfego identificado de bot e de interação não humana (NHI).

* **[!UICONTROL Entregues]**: número de emails enviados com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições]**: número total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Enviar erros]**: Número total de erros que ocorreram durante o processo de envio, impedindo que ele fosse enviado a perfis.

* **[!UICONTROL Enviar exclusões]**: número de perfis excluídos pelo Adobe Journey Optimizer. [Saiba mais sobre como as exclusões são contadas](exclusion-list.md#exclusion-list).

+++

## Etiquetas rastreadas {#track-label-sms}

A tabela **[!UICONTROL Rótulos rastreados]** oferece uma visão geral abrangente dos rótulos de links em suas mensagens SMS, destacando aqueles que geram o maior tráfego de visitantes. Esse recurso permite identificar e priorizar os links mais populares.

+++ Saiba mais sobre Métricas de rótulos de link rastreado

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em suas mensagens SMS.

* **[!UICONTROL Cliques estimados]**: número de vezes que um conteúdo foi clicado em sua mensagem, excluindo o tráfego identificado de bot e de interação não humana (NHI).

* **[!UICONTROL Cliques únicos]**: número de perfis únicos que clicaram em pelo menos um conteúdo na mensagem móvel.

+++

## URLs do link rastreado {#track-link-url-sms}

A tabela **[!UICONTROL URLs de links rastreados]** fornece uma visão geral abrangente das URLs em suas mensagens SMS que atraem o maior tráfego de visitantes. Isso permite identificar e priorizar os links mais populares, melhorando sua compreensão da participação do perfil com conteúdo específico em suas mensagens SMS.

+++ Saiba mais sobre Métricas de URLs de link rastreado

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em suas mensagens SMS.

* **[!UICONTROL Cliques estimados]**: número de vezes que um conteúdo foi clicado em sua mensagem, excluindo o tráfego identificado de bot e de interação não humana (NHI).

* **[!UICONTROL Cliques únicos]**: número de perfis únicos que clicaram em pelo menos um conteúdo na mensagem móvel.

* **[!UICONTROL Exibições]**: número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições exclusivas]**: número de vezes que a mensagem foi aberta; várias interações de um perfil não são consideradas.

+++

## Mensagem por SMS de entrada {#sms-inbound}

A tabela **[!UICONTROL Mensagem de entrada de SMS]** apresenta uma visão geral de quais mensagens SMS atraíram o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas de mensagem de entrada SMS

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens SMS.

+++

## Tipo de mensagem SMS {#sms-message-type}

A tabela **[!UICONTROL Tipo de mensagem SMS]** apresenta uma visão geral completa de qual tipo de mensagem SMS atraiu o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas do tipo Mensagem SMS

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens SMS.

+++

## Provedores de SMS {#sms-providers}

A tabela **[!UICONTROL Provedores de SMS]** apresenta uma visão geral completa de quais provedores de SMS atraíram o maior tráfego de visitantes. Esse recurso oferece informações valiosas sobre a dinâmica do envolvimento do público-alvo.

+++ Saiba mais sobre métricas de provedores de SMS

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens SMS.

+++

## Motivos de rejeição {#bounce-reasons-sms}

A tabela **[!UICONTROL Motivos de rejeições]** fornece uma visão geral abrangente dos dados relacionados às mensagens SMS rejeitadas, fornecendo insights valiosos sobre os motivos específicos por trás das instâncias de rejeições de mensagens SMS.

## Motivos do erro {#error-reasons-sms}

A tabela **[!UICONTROL Motivos de Erro]** permite identificar os erros específicos que ocorreram durante o processo de envio de suas mensagens SMS, facilitando uma análise completa de todos os problemas encontrados.

## Motivos para exclusão {#excluded-reasons-sms}

A tabela **[!UICONTROL Motivos da exclusão]** representa visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber suas mensagens SMS.

Consulte [esta página](exclusion-list.md) para obter uma lista abrangente dos motivos de exclusão.
