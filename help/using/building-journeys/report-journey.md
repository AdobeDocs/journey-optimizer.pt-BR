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
source-git-commit: 63fb247449dfb989b191254ec6d117a403edd29d
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 1%

---

# Relatório ao vivo na tela de jornada {#report-journey}

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
