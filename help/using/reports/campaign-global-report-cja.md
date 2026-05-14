---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar os dados do Campaign no relatório de campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: b74d3137-2dd9-4302-a56e-73503d318d18
TQID: https://experienceleague.adobe.com/-1IfHcdK07JLG54DYR1GNNN-sU0VyHjfBjCLbNdKA-8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 1%

---

# Relatório de campanha {#campaign-global-report-cja}

>[!BEGINSHADEBOX]

Você pode acessar o relatório de Campanha clicando no botão **[!UICONTROL Relatórios]** da campanha e selecionando **[!UICONTROL Exibir relatório de todos os tempos]**. [Saiba mais](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPIs de campanha {#campaign-kpis}

![](assets/cja-email-kpis.png)

Os KPIs (Indicadores-chave de desempenho) da **[!UICONTROL Campanha]** funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua campanha. Isso abrange detalhes como a contagem de cliques e o número de mensagens entregues, oferecendo uma insight abrangente na eficiência e no nível de engajamento da campanha.

Os KPIs variam com base nos canais usados em sua campanha.

+++ Saiba mais sobre as métricas de KPIs do Campaign

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a mensagem.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em sua mensagem.

* **[!UICONTROL Entregues]**: número de emails enviados com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Exibições]**: número de vezes que a mensagem foi aberta.

+++

>[!AVAILABILITY]
>As campanhas orquestradas são compatíveis apenas com os canais SMS, Email e Push. Outros canais (no aplicativo, Web, correspondência direta etc.) não estão disponíveis em campanhas orquestradas e não aparecem nos relatórios.

### Visão geral da campanha {#delivery-global}

![](assets/cja-campaign-overview.png)

A tabela **[!UICONTROL Visão geral da campanha]** serve como um painel abrangente, que oferece um detalhamento das principais métricas relacionadas à sua campanha. Isso inclui informações essenciais, como o número de perfis e as ações entregues, fornecendo uma compreensão completa do desempenho e do envolvimento da campanha.

Observe que as métricas variam com base nos canais usados na campanha.

+++ Saiba mais sobre as métricas de visão geral do Campaign

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com a mensagem.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em sua mensagem.

* **[!UICONTROL Cliques únicos]**: número de perfis que clicaram em um conteúdo em sua mensagem.

* **[!UICONTROL Entregues]**: número de emails enviados com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Rejeições para canais de saída]**: Número total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de mensagens enviadas.

* **[!UICONTROL Erros de Saída]**: Número total de erros ocorridos durante o processo de envio que impediram o envio para perfis.

* **[!UICONTROL Exclusões de saída]**: número de perfis excluídos pelo Adobe Journey Optimizer. [Saiba mais sobre como as exclusões são contadas](exclusion-list.md#exclusion-list).

* **[!UICONTROL Exibições]**: número de vezes que a mensagem foi aberta.

* **[!UICONTROL Exibições exclusivas]**: número de vezes que a mensagem foi aberta; várias interações de um perfil não são consideradas.

+++

### Resultados do funil de campanha {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

O gráfico de **[!UICONTROL resultados do Campaign funnel]** apresenta uma análise detalhada do engajamento dos seus perfis com as suas mensagens, oferecendo informações valiosas sobre como vários perfis interagiram com o seu conteúdo.

+++ Saiba mais sobre as métricas de resultados do Campaign funnel

* **[!UICONTROL Entregues]**: número de emails enviados com êxito em relação ao número total de mensagens enviadas.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em sua mensagem.
+++

### Rótulo do link rastreado {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

A tabela **[!UICONTROL Rótulo do link rastreado]** oferece informações essenciais sobre o envolvimento dos visitantes com as URLs incluídas em suas mensagens, fornecendo informações valiosas sobre quais links atraem mais interação.

+++ Saiba mais sobre Métricas de rótulo de link rastreado

* **[!UICONTROL Cliques únicos]**: número de perfis que clicaram em um conteúdo em sua mensagem.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em sua mensagem.

+++

## Visão geral de direcionamento {#targeting}

![](assets/cja-journey-targeting-overview.png)

Se você configurar **[!UICONTROL Regras de direcionamento]** para o seu conteúdo, a tabela **[!UICONTROL Visão geral do direcionamento]** fornecerá uma exibição detalhada das principais métricas de engajamento, mostrando como os perfis direcionados para cada regra interagiram com seu conteúdo.

➡️ [Saiba mais sobre as regras de direcionamento](../content-management/optimization-targeting.md)

+++ Saiba mais sobre as métricas da visão geral de direcionamento

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para seus eventos.

* **[!UICONTROL Cliques únicos]**: número de perfis que clicaram em um conteúdo em um email.

* **[!UICONTROL Taxa de cliques únicos]**: porcentagem de perfis segmentados que clicaram pelo menos uma vez.

+++
