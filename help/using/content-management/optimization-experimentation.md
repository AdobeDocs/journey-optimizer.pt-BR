---
solution: Journey Optimizer
product: journey optimizer
title: Usar experimentação na otimização de mensagens
description: Saiba como usar experimentos de conteúdo para testar várias versões de conteúdo e determinar qual tem melhor desempenho.
role: User
level: Intermediate
keywords: experimentação, otimização, teste A/B, experimento de conteúdo, tratamentos
source-git-commit: f4eb982ba0840acfe336e759fcbf9cfd47b3b98c
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# Usar experimentação {#experimentation}

>[!NOTE]
>
>Esta página fornece uma visão geral de como usar a experimentação na otimização do conteúdo. Para obter informações detalhadas sobre experimentos de conteúdo, incluindo opções de configuração, métricas e análise, consulte a [Documentação do experimento de conteúdo](../content-management/get-started-experiment.md).

A experimentação permite testar várias versões do conteúdo para determinar qual tem o melhor desempenho com base em métricas de sucesso predefinidas.

Para configurar a experimentação, siga as etapas abaixo.

Digamos que você queira testar as seguintes mensagens promocionais em uma campanha:

* **Tratamento A**: &quot;20% de desconto em sua próxima compra&quot;
* **Tratamento B**: &quot;Envio gratuito em pedidos acima de US$ 50&quot;
* **Tratamento C**: &quot;Obtenha seu vale-presente de $10&quot;

Para configurar a experimentação e determinar qual mensagem impulsiona mais compras, siga as etapas abaixo.

1. Crie uma [jornada](../building-journeys/journey-gs.md#jo-build) ou uma [campanha](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Se você estiver em uma jornada, adicione uma atividade de **[!UICONTROL Ação]**, escolha uma atividade de canal e selecione **[!UICONTROL Configurar ação]**. [Saiba mais](../building-journeys/journey-action.md#add-action)

1. Na guia **[!UICONTROL Ações]**, selecione duas ações de entrada, por exemplo, [experiência baseada em código](../code-based/get-started-code-based.md) e [No aplicativo](../../rp_landing_pages/in-app-landing-page.md).

1. Na seção **[!UICONTROL Otimização]**, selecione **[!UICONTROL Criar experimento]**.

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. Projete e configure seu experimento de conteúdo conforme desejado. [Saiba como](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   Uma vez definido o experimento, ele se aplica a todas as ações inseridas nessa campanha ou por meio da atividade **[!UICONTROL Ação]** da jornada, o que significa que os mesmos clientes veem as mesmas ofertas em todas as superfícies.

   >[!NOTE]
   >
   >Você pode selecionar outras ações: a experimentação se aplica a todas as ações adicionadas à campanha ou à [atividade de Ação](../building-journeys/journey-action.md) da jornada.

1. [Ative](../campaigns/review-activate-campaign.md) sua jornada ou campanha.

Quando a jornada/campanha estiver ativa, os usuários serão atribuídos aleatoriamente às diferentes variações de conteúdo. [!DNL Journey Optimizer] rastreia qual variação gera mais compras e fornece insights acionáveis.

Siga o sucesso da sua campanha com os relatórios da [jornada](../reports/journey-global-report-cja.md) e da [campanha](../reports/campaign-global-report-cja-experimentation.md). <!--Link to Experimentation journey reportis missing-->

