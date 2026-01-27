---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com filtros predefinidos
description: Saiba como salvar, aplicar e gerenciar filtros predefinidos em campanhas orquestradas
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# Trabalhar com filtros predefinidos {#predefined-filters}

Filtros predefinidos são regras salvas que podem ser reutilizadas no construtor de regras. Use-as para evitar a reconstrução de consultas comuns e padronizar a lógica de direcionamento em campanhas orquestradas.

Você pode marcar filtros predefinidos como favoritos, compartilhá-los com outros usuários e adicionar parâmetros para que os campos selecionados possam ser editados quando o filtro for aplicado.

## Criar um filtro predefinido {#create}

Salve um filtro personalizado no construtor de regras para disponibilizá-lo para uso futuro. Siga estas etapas:

1. Abra o construtor de regras e defina as condições de filtragem. [Saiba como criar uma regra](../orchestrated/build-query.md)

1. Opcional: Para tornar determinados campos editáveis ao usar o filtro, selecione o campo e alterne em **[!UICONTROL Definir como parâmetro]**. Ao aplicar o filtro, somente esses campos podem ser editados.

   ![](assets/predefined-filter-parameter-enable.png)

1. Para salvar o filtro, clique em **[!UICONTROL Selecionar ou salvar filtro]** e selecione **[!UICONTROL Salvar como filtro]**.

   ![](assets/predefined-filter-save.png)

1. Insira um rótulo e uma descrição para o filtro e clique em **[!UICONTROL Salvar]**.

   * Para salvar o filtro como favorito, alterne a opção **[!UICONTROL Filtro favorito]**. Saiba mais [nesta seção](#fav-filter).
   * Para tornar o filtro acessível a outros usuários, habilite a opção **[!UICONTROL Filtro compartilhado]**. Saiba mais [nesta seção](#share-filter).

   ![](assets/predefined-filter-save-name.png)

Seu filtro personalizado agora está disponível na lista **Filtros predefinidos**.

## Usar um filtro predefinido em uma regra {#apply}

Filtros predefinidos estão disponíveis ao definir consultas no construtor de regras.

1. No painel **[!UICONTROL Propriedades da regra]**, clique em **[!UICONTROL Selecionar ou salvar filtro]**.

1. Escolha **[!UICONTROL Selecionar filtro predefinido]** e selecione um filtro. Você também pode selecionar diretamente um filtro predefinido na lista se ele tiver sido adicionado aos favoritos.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >A seleção de um filtro predefinido substitui a regra que foi criada na tela pelo filtro selecionado.

1. O filtro é aberto na tela. Continue editando a condição conforme necessário.

   ![](assets/predefined-filter-added.png)

   Se o filtro selecionado incluir parâmetros, somente os campos marcados como parâmetros poderão ser editados. Elas são exibidas no painel ao lado do painel **[!UICONTROL Propriedades da regra]**.

   ![](assets/predefined-filter-parameter-apply.png)

   Para editar o próprio filtro predefinido, clique no ![botão de reticências](assets/do-not-localize/rule-builder-icon-more.svg) e selecione **[!UICONTROL Alternar para a edição de regras]**. Todas as alterações se aplicam somente à regra atual que você está criando. O filtro predefinido não é modificado.

   ![](assets/predefined-filter-parameter-edit.png)

## Salvar um filtro como favorito {#fav-filter}

Ao criar um filtro predefinido, habilite a opção **[!UICONTROL Filtro de favoritos]** para ver esse filtro predefinido em seus favoritos.

Quando um filtro é salvo como favorito, ele aparece na seção **[!UICONTROL Filtros favoritos]** da lista de filtros, conforme mostrado abaixo:

![Seção de filtros favoritos](assets/predefined-filter-favorites.png)

## Compartilhar um filtro predefinido {#share-filter}

Por padrão, os filtros predefinidos criados são privados e visíveis somente para você. Para tornar um filtro acessível a outros operadores em sua organização, habilite a opção **[!UICONTROL Filtro compartilhado]**.

![Opção de filtro compartilhado](assets/predefined-filter-shared.png)

Os filtros compartilhados aparecem na lista de filtros predefinida para todos os usuários, permitindo que eles usem esses filtros em suas próprias regras.

## Gerenciar filtros predefinidos {#manage-predefined-filter}

Para editar ou excluir filtros predefinidos, siga estas etapas:

1. Abra a lista de filtros predefinidos usando o botão **[!UICONTROL Selecionar ou salvar filtro]** na compilação de regras.

1. Selecione o botão de reticências ![](assets/do-not-localize/rule-builder-icon-more.svg) ao lado de um filtro e escolha a ação desejada.

![](assets/predefined-filters-edit.png)
