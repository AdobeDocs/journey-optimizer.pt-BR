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
source-git-commit: b604ab6d94f414b96378f15986edbcf92cee77dc
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# Relatório ao vivo na tela de jornada {#report-journey}

>[!NOTE]
>
>Se você não conseguir ver os dados no seu relatório jornada live, seus direitos de acesso deverão ser estendidos para incluir a permissão **[!UICONTROL Exibir relatório do jornada]**. [Saiba mais](../administration/permissions.md)

Após a publicação da sua jornada, o **Live Reporting** fornece métricas das últimas 24 horas, diretamente na tela de jornada.

Os eventos exibidos ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos entre o evento e sua exibição, normalmente dentro de cinco minutos.

![](assets/journey_live_report.png)

Para sua jornada em tempo real, você tem acesso a:

* **[!UICONTROL Perfis inseridos]**: número total de pessoas que inseriram a jornada.
* **[!UICONTROL Perfis encerrados]**: número total de indivíduos que saíram da jornada (incluindo erros).
* **[!UICONTROL Perfis com erro]**: número total de indivíduos que encontraram um erro durante a jornada.
* **[!UICONTROL Perfis descartados]**: Número total de indivíduos que foram descartados da jornada por um dos seguintes motivos:

   * Para atividades de **Qualificação de público-alvo**, pode ocorrer um descarte se o verbo esperado para qualificação de público-alvo não corresponder ao que a jornada recebeu (por exemplo, &quot;encerrado&quot; em vez de &quot;realizado&quot;).
   * Para jornadas **acionadas por evento**, poderá ocorrer um descarte se o indivíduo tentar entrar novamente na jornada muito cedo ou quando a reentrada não foi permitida.
   * Em jornadas **recorrentes**, um descarte será contado em cada recorrência se o indivíduo já estiver na jornada e a política de reentrada não estiver definida como &quot;forçar reentrada&quot;.
   * Nas atividades **Ler Público**, ocorrerá um descarte se nenhuma identidade for definida para o indivíduo exportado ou se o namespace de identidade recebido não corresponder ao esperado para a jornada.

Para cada atividade em cada jornada ativa, você tem acesso a:

* **[!UICONTROL Informado]**: número total de indivíduos que entraram nesta atividade.
* **[!UICONTROL Saída (atender aos critérios de saída)]**: Número total de indivíduos que saíram da jornada dessa atividade devido a um critério de saída.
* **[!UICONTROL Erro]**: número total de indivíduos que tiveram um erro nessa atividade.
