---
title: Caso de uso de decisão
description: Saiba como criar decisões usando experimentos com o canal baseado em código
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 7%

---

# Caso de uso de decisão {#experience-decisioning-uc}

Este caso de uso apresenta todas as etapas necessárias para usar a Decisão com o canal baseado em código [!DNL Journey Optimizer].

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

Nesse caso de uso, você não tem certeza se uma fórmula de classificação específica terá melhor desempenho do que as prioridades de oferta pré-atribuídas.

Para medir qual tem melhor desempenho para seu público-alvo, crie uma campanha onde você define dois tratamentos de delivery:

<!--Set up the experiment such that:-->

* O primeiro tratamento contém uma estratégia de seleção com prioridade como o método de classificação.
* O segundo tratamento contém uma estratégia de seleção diferente para a qual uma fórmula é o método de classificação.

## Criar estratégias de seleção

Primeiro, é necessário criar duas estratégias de seleção: uma com prioridade como o método de classificação e outra com uma fórmula como o método de classificação.

### Criar a primeira estratégia de seleção

Na primeira estratégia de seleção, selecione prioridade como o método de classificação. Siga as etapas abaixo.

1. Criar um item de decisão. [Saiba como](items.md)

1. Defina a **[!UICONTROL Prioridade]** do item de decisão em comparação a outros. Se um perfil se qualificar para vários itens, uma prioridade mais alta concederá ao item prioridade sobre outros.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >A prioridade é um tipo de dados inteiro. Todos os atributos que são tipos de dados inteiros devem conter valores inteiros (sem decimais).

1. Defina públicos ou regras para restringir o item somente a perfis específicos. [Saiba como definir a qualificação do item de decisão](items.md#eligibility)

1. Defina regras de limite para definir o número máximo de vezes que uma oferta pode ser apresentada. [Saiba como](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Crie uma **coleção** onde seus itens de decisão serão incluídos. [Saiba mais](collections.md)

1. Crie uma **estratégia de seleção**. [Saiba como](selection-strategies.md#create-selection-strategy)

1. Selecione a [coleção](collections.md) que contém a(s) oferta(s) a serem consideradas.

1. [Escolha o método de classificação](#select-ranking-method) a ser usado para selecionar a melhor oferta para cada perfil. Nesse caso, selecione **[!UICONTROL Prioridade da oferta]**. [Saiba mais](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Criar a segunda estratégia de seleção

Na segunda estratégia de seleção, selecione uma fórmula como o método de classificação. Siga as etapas abaixo.

1. Criar um item de decisão. [Saiba como](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Defina públicos ou regras para restringir o item somente a perfis específicos. [Saiba como definir a qualificação do item de decisão](items.md#eligibility)

1. Defina regras de limite para definir o número máximo de vezes que uma oferta pode ser apresentada. [Saiba como](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Crie uma **coleção** onde seus itens de decisão serão incluídos. [Saiba mais](collections.md)

1. Crie uma **estratégia de seleção**. [Saiba como](selection-strategies.md#create-selection-strategy)

1. Selecione a [coleção](collections.md) que contém a(s) oferta(s) a serem consideradas.

1. [Selecione o método de classificação](#select-ranking-method) que deseja usar para selecionar a melhor oferta para cada perfil. Nesse caso, selecione **[!UICONTROL Formula]** para usar uma pontuação calculada específica para escolher qual oferta qualificada fornecer. [Saiba mais](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Criar políticas de decisão

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Crie uma campanha e selecione a ação **[!UICONTROL Experiência baseada em código]**. [Saiba mais](../code-based/create-code-based.md)

1. Na janela **[!UICONTROL Editar conteúdo]**, comece a personalizar o tratamento A.

1. Selecione o ícone **[!UICONTROL Decisões]**, clique em **[!UICONTROL Criar uma decisão]** e preencha os detalhes da decisão. [Saiba mais](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Selecione a primeira estratégia que você criou. Clique em **[!UICONTROL Adicionar estratégia]**.

1. Clique em **[!UICONTROL Criar]**. A nova decisão é adicionada em **[!UICONTROL Decisões]**.

   ![](assets/decision-code-based-decision-added.png)

1. Clique no ícone de mais ações (três pontos) e selecione **[!UICONTROL Adicionar]**. Agora você pode adicionar todos os atributos de decisão desejados aqui.

   ![](assets/decision-code-based-add-decision.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de personalização, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Na página de resumo da campanha, clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo. [Saiba mais](../content-management/content-experiment.md)

1. Na janela **[!UICONTROL Editar conteúdo]**, selecione o tratamento B e repita as etapas acima para criar outra decisão.

1. Selecione a segunda estratégia que você criou. Clique em **[!UICONTROL Adicionar estratégia]**.

1. Salve o conteúdo.
