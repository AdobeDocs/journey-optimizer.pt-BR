---
title: Caso de uso de decisão de experiência
description: Saiba como criar decisões usando experimentos com o canal baseado em código
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 18%

---

# Caso de uso de decisão de experiência {#experience-decisioning-uc}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Offer Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)
* **[Aprenda mais por meio de um caso de uso](experience-decisioning-uc.md)**

>[!ENDSHADEBOX]

Nesse caso de uso, você define dois tratamentos de delivery, cada um contendo uma política de decisão diferente para medir qual tem melhor desempenho para o público-alvo.

## Criar itens e estratégias

Primeiro, é necessário criar itens, agrupá-los em coleções, configurar regras e métodos de classificação. Esses elementos permitirão criar estratégias de seleção.

1. Navegue até **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Itens]** e criar vários itens de oferta. Defina restrições usando públicos ou regras para restringir cada item somente a perfis específicos. [Saiba mais](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Criar **coleções** para categorizar e agrupar seus itens de decisão de acordo com suas preferências. [Saiba mais](collections.md)

1. Criar **regras de decisão** para determinar para quem um item de decisão pode ser mostrado. [Saiba mais](rules.md)

1. Criar **métodos de classificação** e aplicá-las nas estratégias de decisão para determinar a ordem de prioridade para selecionar itens de decisão. [Saiba mais](ranking.md)

1. Build **estratégias de seleção** que usam coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis. [Saiba mais](selection-strategies.md)

## Criar políticas de decisão

Para apresentar a melhor oferta dinâmica e experiência aos visitantes em seu site ou aplicativo móvel, adicione uma política de decisão a uma campanha baseada em código.

Defina dois tratamentos de delivery, cada um contendo uma política de decisão diferente.

1. Crie uma campanha e selecione o **[!UICONTROL Experiência baseada em código (Beta)]** ação. [Saiba mais](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >O recurso de experiência baseada em código está disponível no momento como uma versão beta somente para usuários selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

1. Na página de resumo da campanha, clique em **[!UICONTROL Criar experimento]** para configurar seu experimento de conteúdo. [Saiba mais](../campaigns/content-experiment.md)

1. Selecione o **[!UICONTROL Decisões]** clique em **[!UICONTROL Criar uma decisão]** e preencha os detalhes da decisão. [Saiba mais](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Defina as estratégias de seleção para sua decisão. Clique em **[!UICONTROL Adicionar estratégia]**.

1. Clique em **[!UICONTROL Criar]**. A nova decisão é aditada em **[!UICONTROL Decisões]**.

   ![](assets/decision-code-based-decision-added.png)

1. Clique no ícone de mais ações (três pontos) e selecione **[!UICONTROL Adicionar]**. Agora você pode adicionar todos os atributos de decisão desejados aqui.

   ![](assets/decision-code-based-add-decision.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de expressão, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Crie o tratamento B e repita as etapas acima para criar outra decisão.

1. Salve o conteúdo.


