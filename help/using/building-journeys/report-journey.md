---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como criar relatórios sobre sua jornada
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1134
ht-degree: 0%

---

# Relatório ao vivo na tela de jornada {#report-journey}

>[!BEGINSHADEBOX]

**Nesta página:** Aprenda a usar os Relatórios ao Vivo para monitorar as métricas principais de jornada das últimas 24 horas diretamente na tela de jornada.

>[!ENDSHADEBOX]

Após a publicação da sua jornada, no momento em que o [Modo de execução a seco](journey-dry-run.md) é ativado, o **Relatórios ao Vivo** fornece métricas das últimas 24 horas, diretamente na tela de jornada.


>[!AVAILABILITY]
>
>Se você não conseguir ver os dados no seu relatório jornada live, seus direitos de acesso deverão ser estendidos para incluir a permissão **[!UICONTROL Exibir relatório do jornada]**. [Saiba mais](../administration/permissions.md)


Os eventos exibidos ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos entre o evento e sua exibição, normalmente dentro de cinco minutos.

![Jornada painel de relatório ao vivo mostrando métricas de desempenho em tempo real](assets/journey_live_report.png)

Para suas jornadas no modo Live ou [Dry run](journey-dry-run.md), você pode verificar:

* **[!UICONTROL Perfis inseridos]**: número total de pessoas que inseriram a jornada.
* **[!UICONTROL Perfis encerrados]**: número total de indivíduos que saíram da jornada (incluindo erros).
* **[!UICONTROL Perfis com erro]**: número total de indivíduos que encontraram um erro durante a jornada.
* **[!UICONTROL Perfis descartados]**: Número total de indivíduos que foram descartados da jornada por um dos seguintes motivos:

   * Para atividades de **Qualificação de público-alvo**, pode ocorrer um descarte se o verbo esperado para qualificação de público-alvo não corresponder ao que a jornada recebeu (por exemplo, &quot;encerrado&quot; em vez de &quot;realizado&quot;).
   * Para jornadas **acionadas por evento**, poderá ocorrer um descarte se o indivíduo tentar entrar novamente na jornada muito cedo ou quando a reentrada não foi permitida.
   * Em jornadas **recorrentes**, um descarte será contado em cada recorrência se o indivíduo já estiver na jornada e a política de reentrada não estiver definida como &quot;forçar reentrada&quot;.
   * Nas atividades **Ler Público**, ocorrerá um descarte se nenhuma identidade for definida para o indivíduo exportado ou se o namespace de identidade recebido não corresponder ao esperado para a jornada.

Para cada atividade em cada jornada no modo Live ou [Dry run](journey-dry-run.md), você tem acesso a:

* **[!UICONTROL Informado]**: número total de indivíduos que entraram nesta atividade. Para atividades de **Ação**, como não são executadas no modo de execução em andamento, essa métrica indica que os perfis estão passando.
* **[!UICONTROL Saída (atender aos critérios de saída)]**: Número total de indivíduos que saíram da jornada dessa atividade devido a um critério de saída (incluindo erros).
* **[!UICONTROL Saída (saída forçada)]**: Número total de indivíduos que saíram da jornada enquanto ela estava pausada devido a uma configuração de profissional de jornada. Essa métrica é sempre igual a zero para jornadas no modo de Execução em tempo real.
* **[!UICONTROL Erro]**: número total de indivíduos que tiveram um erro nessa atividade.

## Solução de problemas de dados de relatórios ausentes {#troubleshooting-missing-data}

Se você não vir os dados esperados em seus relatórios do jornada, considere o seguinte:

* **Sincronização de nome de Jornada**: verifique se o nome de jornada em [!DNL Adobe Journey Optimizer] corresponde ao nome armazenado no conjunto de dados de relatórios. Uma incompatibilidade entre esses nomes pode impedir que os dados de relatório apareçam corretamente.

* **Tempo de atualização de dados**: depois de atualizar um nome ou uma configuração de jornada, aguarde tempo suficiente para que os dados sejam atualizados. Os dados de relatórios normalmente são exibidos em alguns minutos, mas em alguns casos podem levar mais tempo.

* **Permissões de acesso**: verifique se você tem as permissões necessárias para exibir relatórios de jornada. Se você não vir dados, verifique com o administrador se a permissão **[!UICONTROL Exibir relatório do jornada]** está habilitada. [Saiba mais sobre permissões](../administration/permissions.md)

* **Status da Jornada**: os dados de relatório só estão disponíveis para jornadas ou jornadas publicadas em execução no [Modo de execução a seco](journey-dry-run.md). As jornadas de rascunho não geram dados de relatório.

Se os problemas persistirem após a verificação desses itens, entre em contato com o administrador do Adobe ou com o [suporte da Adobe](../start/user-interface.md#support-ticket-guidelines) para obter assistência.

>[!MORELIKETHIS]
>
>* [Introdução aos relatórios](../reports/gs-reports.md)
>* [Publicar sua jornada](publish-journey.md)
>* [Jornada execução seca](journey-dry-run.md)
>* [Configurar e acompanhar suas métricas do jornada](success-metrics.md)
>* [Relatórios de jornada personalizados](../reports/sharing-overview.md)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como exibir e interpretar o relatório ao vivo incorporado na tela de jornada, abordando as principais métricas de fluxo de perfil disponíveis para jornadas e jornadas publicadas no modo de Execução em tempo real.

**Intenções:**
* Exibir métricas de desempenho da jornada em tempo real diretamente na tela de jornada
* Interpretar as contagens de perfil Inserido, Encerrado, Erro e Descartado para a jornada e cada atividade
* Entender por que os perfis são descartados de uma jornada
* Solução de problemas de dados ausentes ou inesperados nos relatórios do jornada live
* Verifique a permissão necessária para acessar os relatórios ao vivo do jornada

**Glossário:**
* **Relatórios ao Vivo**: métricas em tempo real exibidas diretamente na tela de jornada que abrangem as últimas 24 horas *(específico do produto)*
* **Modo de execução direta**: um modo de execução de jornada que simula a jornada sem enviar mensagens reais, no qual relatórios dinâmicos também estão disponíveis *(específico do produto)*
* **Perfis descartados**: perfis que tentaram entrar na jornada, mas foram rejeitados devido a incompatibilidades de qualificação, restrições de reentrada ou problemas de identidade *(específico do produto)*
* **Saída (saída forçada)**: Perfis que foram removidos da jornada enquanto ela estava pausada por um profissional de jornada; sempre zero no modo de execução Seca *(específico do produto)*

**Medidas de Proteção:**
* Os dados do relatório ao vivo abrangem apenas as últimas 24 horas.
* Os eventos são exibidos com um intervalo mínimo de dois minutos a partir da ocorrência, normalmente dentro de cinco minutos.
* A permissão de relatório Exibir jornadas é necessária para ver os dados do relatório em tempo real.
* Os dados de relatório só estão disponíveis para jornadas ou jornadas publicadas no modo de Execução a seco; jornadas de rascunho não geram dados.
* Para atividades de Ação, a métrica Inserido mostra perfis que passam (não executados) no modo de Execução em tempo real.
* A métrica Sair (saída forçada) é sempre zero no modo de execução a seco.

**Terminologia:**
* Nome canônico: Relatório ao vivo (tela de jornada) — Acrônimo: nenhum — variantes: Relatório ao vivo da jornada, relatórios na tela
* Sinônimos: &quot;Perfis inseridos&quot; = &quot;perfis que entraram na jornada&quot;
* Não confunda: &quot;Relatório ao vivo&quot; ≠ &quot;Relatório global do Jornada&quot; (relatório ao vivo são as últimas 24 horas na tela; relatório global cobre um intervalo de tempo histórico mais amplo na interface de relatório)

**Perguntas frequentes:**
* **P: Qual é a atualidade dos dados mostrados no relatório em tempo real?** — Os eventos das últimas 24 horas são exibidos, com um atraso mínimo de exibição de dois minutos e, normalmente, em cinco minutos.
* **P: Por que não posso ver nenhum dado no meu relatório de jornada ao vivo?** — Verifique se você tem a permissão de relatório Exibir jornadas, se a jornada foi publicada (não no rascunho) e se o nome da jornada corresponde ao nome no conjunto de dados de relatórios.
* **P: O que faz com que os perfis sejam descartados?** — podem ocorrer descartes devido a incompatibilidades de verbos de qualificação de público-alvo, violações de políticas de reentrada em jornadas recorrentes ou acionadas por eventos ou namespace de identidade ausente/incompatível em atividades Ler público-alvo.
* **P: O relatório ao vivo está disponível durante o modo de Execução sem Interrupção?** — Sim; o relatório em tempo real está disponível para jornadas publicadas e jornadas executadas no modo de simulação.
* **P: O que a métrica Inserida significa para atividades de Ação no modo de Execução em disco?** — Indica perfis que passam pela atividade, já que as ações não são realmente executadas no modo Dry run.

+++
