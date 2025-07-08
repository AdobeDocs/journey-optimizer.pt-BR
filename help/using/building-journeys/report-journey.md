---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como criar relatórios sobre sua jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
source-git-commit: 62525caa9b065538c090b98d38c15dbd960dafe7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 2%

---

# Relatório ao vivo na tela de jornada {#report-journey}

Após a publicação da sua jornada, no momento em que o [Modo de execução a seco](journey-dry-run.md) é ativado, o **Relatórios ao Vivo** fornece métricas das últimas 24 horas, diretamente na tela de jornada.


>[!AVAILABILITY]
>
>Se você não conseguir ver os dados no seu relatório jornada live, seus direitos de acesso deverão ser estendidos para incluir a permissão **[!UICONTROL Exibir relatório do jornada]**. [Saiba mais](../administration/permissions.md)


Os eventos exibidos ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos entre o evento e sua exibição, normalmente dentro de cinco minutos.

![](assets/journey_live_report.png)

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


>[!MORELIKETHIS]
>
>* [Introdução aos relatórios](../reports/gs-reports.md)
>* [Publicar sua jornada](publishing-the-journey.md)
>* [Jornada execução seca](journey-dry-run.md)
>* [Configurar e acompanhar suas métricas do jornada](success-metrics.md)
>* [Relatórios de jornada personalizados](../reports/sharing-overview.md)