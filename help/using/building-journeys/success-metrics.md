---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como criar relatórios sobre suas métricas do jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: f26083c222efa71176ce5c78f5f35f2c208240e6
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 6%

---

# Configurar e rastrear as métricas da jornada {#success-metrics}

Obtenha visibilidade clara sobre a eficácia das jornadas do cliente com as métricas do jornada. Esse recurso permite rastrear o desempenho em relação aos KPIs definidos, descobrir insights sobre o que está funcionando e identificar áreas para otimização. Ao medir o impacto em tempo real, você pode impulsionar melhorias contínuas e tomar decisões informadas por dados que elevam o engajamento do cliente.

## Pré-requisitos {#prerequisites}

Antes de usar suas métricas do jornada, você deve adicionar um conjunto de dados que inclua os `Commerce Details`, `Web` e `Mobile` [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} em Configuração > Relatórios no Adobe Experience Platform.

Esses grupos de campos devem ser selecionados nas opções internas, não em grupos personalizados. Consulte a seção [Adicionar conjuntos de dados](../reports/reporting-configuration.md#add-datasets).

## Métricas disponíveis {#metrics}

A lista de métricas varia dependendo dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} incluídos no seu conjunto de dados.

Se seu conjunto de dados não estiver configurado, apenas as seguintes métricas estarão disponíveis: **[!UICONTROL Clique]**, **[!UICONTROL Clique Único]**, **[!UICONTROL Taxa de Click-through]** e **[!UICONTROL Taxa de Abertura]**.

Observe que com uma licença do Customer Journey Analytics é possível criar métricas de sucesso personalizadas. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Métricas | Grupo de campos relacionado |
|-|-|
| Cliques | Nenhum grupo de campos necessário |
| Cliques únicos | Nenhum grupo de campos necessário |
| Taxa de cliques (CTR) | Nenhum grupo de campos necessário |
| Taxa de abertura de cliques (CTOR) | Nenhum grupo de campos necessário |
| Page Views | Grupo de campos da Web |
| Inicializações do aplicativo | Grupo de campos móvel |
| Primeiras inicializações do aplicativo | Grupo de campos móvel |
| Instalações de aplicativo | Grupo de campos móvel |
| Atualizações do aplicativo | Grupo de campos móvel |
| Compras | Grupo de campos Detalhes do Commerce |
| Check-outs | Grupo de campos Detalhes do Commerce |
| Adições ao carrinho | Grupo de campos Detalhes do Commerce |
| Aberturas do carrinho | Grupo de campos Detalhes do Commerce |
| Visualizações do carrinho | Grupo de campos Detalhes do Commerce |
| Remoções do carrinho | Grupo de campos Detalhes do Commerce |
| Visualizações de produto | Grupo de campos Detalhes do Commerce |
| Salvos para mais tarde | Grupo de campos Detalhes do Commerce |

## Atribuição {#attribution}

Cada métrica vem com uma atribuição definida que determina quais pontos de contato ou interações contribuíram para um resultado específico.

* **Atribuição de métricas com a licença do Journey Optimizer**:

  Somente com a licença do Journey Optimizer, a janela de pesquisa máxima disponível para qualquer métrica selecionada é definida como 7 dias. Para essas métricas, o modelo de atribuição é definido por padrão como **Último contato**, ou seja, a interação mais recente antes da conversão.

  Por exemplo, você pode acompanhar se uma compra foi feita depois que um cliente interagiu com sua jornada nos últimos 7 dias.

* **Atribuição de métricas com a licença do Customer Journey Analytics**:

  Com as licenças do Journey Optimizer e da Customer Journey Analytics, é possível criar métricas personalizadas com configurações de atribuição específicas ou alterar as atribuições das métricas integradas.

  Saiba mais sobre [Modelos de atribuição](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Atribuir suas métricas de jornada {#assign}

>[!IMPORTANT]
>
>Somente uma métrica de jornada é permitida por jornada.

Para começar a rastrear suas métricas do jornada, siga as etapas descritas abaixo:

1. No menu do **[!UICONTROL Jornada]**, clique em **[!UICONTROL Criar Jornada]**.

1. Edite o painel de configuração da jornada para definir o nome da jornada e definir suas propriedades. Saiba como definir as propriedades da sua jornada [nesta página](../building-journeys/journey-properties.md).

1. Escolha as **[!UICONTROL métricas de Jornada]** que serão usadas para medir a eficácia da jornada.

   Observe que as métricas se aplicam à própria jornada e se aplicam a todos os elementos da jornada.

   ![](assets/success_metric.png)

1. Clique em **[!UICONTROL Salvar]**.

1. Projete sua jornada com as **[!UICONTROL Atividades]** necessárias.

1. Teste e publique sua jornada.

1. Abra o relatório de jornada para acompanhar o desempenho das métricas de sucesso atribuídas.

   As métricas escolhidas são exibidas na tabela KPIs e estatísticas da Jornada do relatório.

   ![](assets/success_metric_2.png)

