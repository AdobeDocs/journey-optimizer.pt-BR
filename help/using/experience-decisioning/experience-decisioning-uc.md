---
title: Caso de uso de decisão
description: Saiba como criar decisões usando experimentos com o canal baseado em código
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 7%

---

# Caso de uso de decisão {#experience-decisioning-uc}

Nesse caso de uso, você cria uma campanha em que define dois tratamentos de delivery, cada um contendo uma política de decisão diferente para medir qual tem melhor desempenho para seu público-alvo.

## Criar itens de decisão e estratégias de seleção

Primeiro, é necessário criar itens, agrupá-los em coleções, configurar regras e métodos de classificação. Esses elementos permitirão criar estratégias de seleção.

1. Navegue até **[!UICONTROL Decisão]** > **[!UICONTROL Catálogos]** e crie vários itens de decisão. Defina restrições usando públicos ou regras para restringir cada item somente a perfis específicos. [Saiba mais](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Crie **coleções** para categorizar e agrupar seus itens de decisão de acordo com suas preferências. [Saiba mais](collections.md)

1. Crie **regras de decisão** para determinar para quem um item de decisão pode ser mostrado. [Saiba mais](rules.md)

1. Crie **métodos de classificação** e aplique-os nas estratégias de decisão para determinar a ordem de prioridade para selecionar itens de decisão. [Saiba mais](ranking.md)

1. Crie **estratégias de seleção** que aproveitem as coleções, as regras de decisão e os métodos de classificação para identificar os itens de decisão adequados para exibição em perfis. [Saiba mais](selection-strategies.md)

## Criar políticas de decisão

Para apresentar a melhor oferta dinâmica e experiência aos visitantes em seu site ou aplicativo móvel, adicione uma política de decisão a uma campanha baseada em código.

<!--Define two delivery treatments each containing a different decision policy.-->

1. Crie uma campanha e selecione a ação **[!UICONTROL Experiência baseada em código]**. [Saiba mais](../code-based/create-code-based.md)

1. Na janela **[!UICONTROL Editar conteúdo]**, comece a personalizar o tratamento A.

1. Selecione o ícone **[!UICONTROL Decisões]**, clique em **[!UICONTROL Criar uma decisão]** e preencha os detalhes da decisão. [Saiba mais](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Defina as estratégias de seleção para sua decisão. Clique em **[!UICONTROL Adicionar estratégia]**.

1. Clique em **[!UICONTROL Criar]**. A nova decisão é adicionada em **[!UICONTROL Decisões]**.

   ![](assets/decision-code-based-decision-added.png)

1. Clique no ícone de mais ações (três pontos) e selecione **[!UICONTROL Adicionar]**. Agora você pode adicionar todos os atributos de decisão desejados aqui.

   ![](assets/decision-code-based-add-decision.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de personalização, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Na página de resumo da campanha, clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo. [Saiba mais](../content-management/content-experiment.md)

1. Na janela **[!UICONTROL Editar conteúdo]**, selecione seu tratamento B para alterar o conteúdo e repita as etapas acima para criar outra decisão.

1. Salve o conteúdo.


