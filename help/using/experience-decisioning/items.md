---
title: Itens de decisão
description: Saiba como trabalhar com itens de decisão
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: 50d3be8fb8ae04e1cab747f6ba4b1024c5e3ec97
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 25%

---

# Itens de decisão {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Gerenciar itens de decisão"
>abstract="O Journey Optimizer permite gerar ofertas de marketing, conhecidas como itens de decisão, que você pode criar e organizar em catálogos e coleções centralizados. Atualmente, todos os itens de decisão criados são consolidados em um único catálogo de “Ofertas”. Nessa tela, você também pode acessar o esquema do catálogo clicando em **Editar esquema** e criar atributos personalizados para itens de decisão."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=pt-BR" text="Configurar o catálogo de itens"

>[!BEGINSHADEBOX &quot;O que você encontrará neste guia de documentação&quot;]

* [Introdução ao Experience Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão: [Configurar o catálogo de itens](catalogs.md) - **[Criar itens de decisão](items.md)** - [Gerenciar coleções de itens](collections.md)
* Configurar a seleção dos itens: [Criar regras de decisão](rules.md) - [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

O Journey Optimizer permite gerar ofertas de marketing, conhecidas como itens de decisão, que você pode criar e organizar em catálogos e coleções centralizados. Eles são compostos de atributos padrão e personalizados projetados para se alinharem com precisão às suas necessidades. Além disso, incorporam restrições de perfil que permitem definir para quem um item de decisão pode ser exibido.

Antes de criar um item de decisão, verifique se você criou um **regra de decisão** se quiser definir condições para determinar para quem o item de decisão pode ser exibido. [Saiba como criar regras de decisão](rules.md).

## Crie o primeiro item de decisão

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Defina a prioridade do item de decisão"
>abstract="Se um perfil for qualificado para vários itens, a prioridade permitirá a comparação entre esse item de decisão e outros. Uma prioridade mais alta concede ao item precedência sobre outros."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Definir os atributos personalizados"
>abstract="Atributos personalizados são atributos específicos adaptados às suas necessidades que podem ser atribuídos a um item de decisão. Eles são criados no esquema de catálogo dos itens de decisão. Esta seção só será exibida se você tiver adicionado pelo menos um atributo personalizado ao esquema de catálogo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=pt-BR" text="Configurar o catálogo de itens"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Adicionar públicos-alvo ou regras de decisão"
>abstract="Por padrão, todos os perfis estão qualificados para receber o item de decisão, mas você pode usar públicos-alvo ou regras para restringir o item somente a perfis específicos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=pt-BR" text="Usar públicos-alvo"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html?lang=pt-BR" text="Usar regras de decisão"

Para criar um item de decisão, siga estas etapas:

1. Navegue até **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Itens]**.

1. Defina os atributos padrão do item de decisão:

   1. Forneça um nome e uma descrição.
   1. Especifique datas de início e término. O item só será considerado pelo mecanismo de decisão nessas datas.
   1. Defina o **[!UICONTROL Prioridade]** do item de decisão em comparação a outros, se um perfil se qualificar para vários itens. Uma prioridade mais alta concede ao item precedência sobre outros.
   1. A variável **Tags** permite atribuir Tags unificadas do Adobe Experience Platform aos itens de decisão. Isso permite classificá-los facilmente e melhorar a pesquisa. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >A prioridade é um tipo de dados inteiro. Todos os atributos que são tipos de dados inteiros devem conter valores inteiros (sem decimais).

1. Atributos personalizados são atributos específicos adaptados às suas necessidades que podem ser atribuídos a um item de decisão. Eles são definidos no schema do catálogo dos itens de decisão. [Saiba como trabalhar com catálogos](catalogs.md)

1. Após definir os atributos do item de decisão, clique em **[!UICONTROL Próxima]** para definir restrições de perfil para o item.

   Por padrão, todos os perfis estarão qualificados para receber o item de decisão, mas você pode usar públicos ou regras para restringir o item somente a perfis específicos, ambas as soluções correspondentes a usos diferentes. Expanda a seção abaixo para obter mais informações:

   +++Uso de públicos-alvo vs. regras de decisão

   Basicamente, a saída de um público-alvo é uma lista de perfis, enquanto uma regra de decisão é uma função executada sob demanda em relação a um único perfil durante o processo de decisão.

   * **Públicos-alvo**: por um lado, os públicos-alvo são um grupo de perfis do Adobe Experience Platform que correspondem a determinada lógica com base em atributos de perfil e eventos de experiência. No entanto, o Gerenciamento de ofertas não recalcula o público-alvo, que pode não estar atualizado ao apresentar a oferta.

   * **Regras de decisão**: por outro lado, uma regra de decisão se baseia nos dados disponíveis no Adobe Experience Platform e determina para quem uma oferta pode ser exibida. Uma vez selecionada em uma oferta ou em uma decisão para um determinado posicionamento, a regra é executada sempre que uma decisão é tomada, o que garante que cada perfil receba a melhor e mais recente oferta.

+++

   ![](assets/item-constraints.png)

   * Para limitar a apresentação do item de decisão aos membros de um ou vários públicos-alvo da Adobe Experience Platform, selecione o **[!UICONTROL Visitantes que se encaixam em um ou vários públicos-alvo]** e, em seguida, adicione um ou vários públicos-alvo do painel esquerdo e combine-os usando a **[!UICONTROL E]** / **[!UICONTROL Ou]** operadores lógicos. [Saiba mais sobre públicos](../audience/about-audiences.md).

   * Para associar uma regra de decisão específica ao item de decisão, selecione **[!UICONTROL Por regra]**, em seguida, arraste a regra desejada do painel esquerdo para a área central. [Saiba mais sobre regras de decisão](rules.md).

   Ao selecionar públicos ou regras de decisão, você pode ver informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar dados.

   >[!NOTE]
   >
   >As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que exige que o tempo atual seja ≥ 80 graus.

1. Depois que as restrições do item de decisão forem definidas, clique em **[!UICONTROL Próxima]** para revisar e salvar o item.

1. O item de decisão agora aparece na lista, com a variável **[!UICONTROL Rascunho]** status. Quando estiver pronto para ser apresentado aos perfis, clique no botão de reticências e selecione **[!UICONTROL Aprovar]**.

   ![](assets/item-approve.png)

## Gerenciar itens de decisão

Na lista de itens de decisão, é possível editar um item de decisão e alterar seu status (**Rascunho**, **Aprovado**, **Arquivado**), duplicá-lo ou excluí-lo.

Para modificar um item de decisão, abra-o, faça suas modificações e salve-o.

Selecionar um item de decisão ou clicar no botão de reticências permite as ações descritas abaixo.

* **[!UICONTROL Aprovar]**: define o status do item de decisão como Aprovado.
* **[!UICONTROL Desfazer aprovação]**: define o status do item de decisão novamente como **[!UICONTROL Rascunho]**.
* **[!UICONTROL Duplicar]**: cria um item de decisão com atributos e restrições idênticos. Por padrão, o novo item tem a variável **[!UICONTROL Rascunho]** status.
* **[!UICONTROL Excluir]**: remove o item de decisão da lista.

  >[!IMPORTANT]
  >
  >Depois de excluído, o item de decisão e seu conteúdo não estarão mais acessíveis. Essa ação não pode ser desfeita. Se o item de decisão for usado em uma coleção ou uma decisão, ele não poderá ser excluído. Você deve remover o item de decisão de qualquer objeto primeiro.

* **[!UICONTROL Arquivar]**: define o status do item de decisão como **[!UICONTROL Arquivado]**. O item de decisão ainda está disponível na lista, mas você não pode definir seu status novamente como **[!UICONTROL Rascunho]** ou **[!UICONTROL Aprovado]**. Você só pode duplicá-la ou excluí-la.
