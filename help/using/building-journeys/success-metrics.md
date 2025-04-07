---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como criar relatórios sobre a métrica de jornada escolhida
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
hide: true
hidefromtoc: true
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 5%

---

# Configurar e rastrear sua métrica de jornada {#success-metrics}

Com as métricas do jornada, você pode medir efetivamente o impacto das atividades rastreando o desempenho em relação às métricas predefinidas.
Ao rastrear essas métricas, você pode ver o desempenho da sua jornada, identificar áreas que precisam ser melhoradas e tomar decisões conscientes para aprimorar o engajamento do cliente.

## Pré-requisitos {#prerequisites}

Antes de usar sua métrica de jornada, você deve adicionar um conjunto de dados que inclua os `Commerce Details`, `Web`e `Mobile` [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"}.

## Métricas disponíveis {#metrics}

A lista de métricas varia dependendo dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} incluídos no seu conjunto de dados.

Se seu conjunto de dados não estiver configurado, apenas as seguintes métricas estarão disponíveis: **[!UICONTROL Clique]**, **[!UICONTROL Clique Único]**, **[!UICONTROL Taxa de Click-through]** e **[!UICONTROL Taxa de Abertura]**.

Observe que com uma licença do Customer Journey Analytics é possível criar métricas de sucesso personalizadas. [Saiba mais](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


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

  Saiba mais sobre [Modelos de atribuição](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Atribuir a métrica de Jornada {#assign}

Para começar a rastrear sua métrica do jornada, siga as etapas descritas abaixo:

1. No menu do **[!UICONTROL Jornada]**, clique em **[!UICONTROL Criar Jornada]**.

1. Edite o painel de configuração da jornada para definir o nome da jornada e definir suas propriedades. Saiba como definir as propriedades da sua jornada [nesta página](../building-journeys/journey-properties.md).

1. Escolha as **[!UICONTROL métricas de Jornada]** que serão usadas para medir a eficácia da jornada.

   Observe que as métricas se aplicam à própria jornada e se aplicam a todos os elementos da jornada.

   ![](assets/success_metric.png)

1. Clique em **[!UICONTROL Salvar]**.

1. Projete sua jornada com as **[!UICONTROL Atividades]** necessárias.

1. Teste e publique sua jornada.

1. Abra o relatório de jornada para acompanhar o desempenho da métrica de sucesso atribuída.

   A métrica escolhida é exibida na tabela KPIs e estatísticas da Jornada do relatório.

   ![](assets/success_metric_2.png)
