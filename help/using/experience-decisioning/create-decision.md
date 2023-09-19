---
title: Criar decisões
description: Saiba como criar decisões
feature: Offers
topic: Integrations
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 5%

---

# Criar políticas de decisão {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="O que é uma decisão?"
>abstract="As políticas de decisão usam o mecanismo de decisão da experiência para escolher o melhor conteúdo a ser entregue, dependendo do público-alvo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=pt-BR" text="Sobre o Experience Decisioning"

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Experience Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* **[Criar políticas de decisão](create-decision.md)**

>[!ENDSHADEBOX]

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo do Experience Decisioning para escolher o melhor conteúdo a ser entregue, dependendo do público.

>[!NOTE]
>
>No [!DNL Journey Optimizer] interface do usuário, as políticas de decisão são rotuladas como decisões<!--but they are decision policies. TBC if this note is needed-->.

## Adicionar uma política de decisão a uma campanha baseada em código {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definir o número de itens a serem retornados"
>abstract="Selecione o número de itens de decisão que você deseja retornar. Por exemplo, se você selecionar 2, as 2 melhores ofertas qualificadas serão apresentadas para a superfície atual."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selecionar um fallback"
>abstract="Um item de fallback é exibido ao usuário quando nenhuma das estratégias de seleção definidas para essa política de decisão é qualificada."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="O que é uma estratégia?"
>abstract="A sequência da estratégia de seleção determina qual estratégia será avaliada primeiro. Pelo menos uma estratégia é necessária. Os itens de decisão em estratégias combinadas serão avaliados em conjunto."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=pt-BR" text="Criar estratégias"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=pt-BR" text="Ordem de avaliação"

Para apresentar a melhor oferta dinâmica e experiência aos visitantes em seu site ou aplicativo móvel, adicione uma política de decisão a uma campanha baseada em código. Para isso, siga as etapas abaixo.

1. Crie uma campanha e selecione o **[!UICONTROL Experiência baseada em código (Beta)]** ação. [Saiba mais](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >O recurso de experiência baseada em código está disponível no momento como uma versão beta somente para usuários selecionados.

1. No [editor de código](../code-based/create-code-based.md#edit-code), selecione o **[!UICONTROL Decisões]** e clique em **[!UICONTROL Criar uma decisão]**.

   ![](assets/decision-code-based-create.png)

1. Preencha os detalhes da sua política de decisão: adicione um nome e selecione um catálogo.

   >[!NOTE]
   >
   >Atualmente, apenas o padrão **[!UICONTROL Ofertas]** catálogo está disponível.

   ![](assets/decision-code-based-details.png)

1. Selecione o número de itens que você deseja retornar. Por exemplo, se você selecionar 2, as 2 melhores ofertas qualificadas serão apresentadas para a superfície atual. Clique em **[!UICONTROL Próximo]**

1. Use o **[!UICONTROL Adicionar estratégia]** botão para definir as estratégias de seleção para sua política de decisão. Cada estratégia consiste em uma coleção de ofertas associada a uma restrição de qualificação e um método de classificação para determinar as ofertas a serem exibidas. [Saiba mais](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >Pelo menos uma estratégia é necessária. Não é possível adicionar mais de 10 estratégias.

1. No **[!UICONTROL Adicionar estratégia]** também é possível criar uma estratégia. A variável **[!UICONTROL Criar estratégia de seleção]** O botão redireciona você para a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Configurações]** menu. [Saiba mais](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. Ao adicionar várias estratégias, elas serão avaliadas em uma ordem específica. A primeira estratégia que foi adicionada à sequência será avaliada primeiro e assim por diante. [Saiba mais](#evaluation-order)

   Para alterar a sequência padrão, você pode arrastar e soltar as estratégias e/ou os grupos para reorganizá-los como desejado.

   ![](assets/decision-code-based-strategy-groups.png)

1. Adicione um fallback. Um item de fallback será exibido para o usuário se nenhuma das estratégias de seleção acima for qualificada.

   ![](assets/decision-code-based-strategy-fallback.png)

   Você pode selecionar qualquer item da lista, que exibe todos os itens de decisão criados na sandbox atual. Se nenhuma estratégia de seleção for qualificada, o fallback será exibido para o usuário, independentemente das datas e da restrição de qualificação aplicada ao item selecionado<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >Um fallback é opcional. Se nenhum fallback for selecionado e se nenhuma estratégia for qualificada, nada será exibido por [!DNL Journey Optimizer].

1. Salve a seleção e clique em **[!UICONTROL Criar]**. A nova política de decisão é adicionada em **[!UICONTROL Decisões]**.

   ![](assets/decision-code-based-decision-added.png)

Agora que a política de decisão foi criada, você pode usar os atributos de decisão dentro do conteúdo de experiência baseado em código. [Saiba mais](#use-decision-policy)

## Ordem de avaliação {#evaluation-order}

Conforme descrito acima, uma estratégia consiste em uma coleção, um método de classificação e restrições de qualificação.

É possível:

* Defina a ordem sequencial que deseja para que as estratégias sejam avaliadas,
* Combine várias estratégias para que sejam avaliadas juntas e não separadamente.

Várias estratégias e seus agrupamentos determinam a prioridade das estratégias e a classificação das ofertas elegíveis. A primeira estratégia tem a prioridade mais alta e as estratégias combinadas dentro do mesmo grupo têm a mesma prioridade.

Por exemplo, você tem duas coleções, uma na estratégia A e uma na estratégia B. A solicitação é para que dois itens de decisão sejam enviados de volta. Digamos que haja duas ofertas qualificadas da estratégia A e três ofertas qualificadas da estratégia B.

* Se as duas estratégias forem **não combinado** ou em ordem sequencial (1 e 2), as duas principais ofertas qualificadas da primeira estratégia serão retornadas na primeira linha. Se não houver duas ofertas elegíveis para a primeira estratégia, o mecanismo de decisão seguirá para a próxima estratégia em sequência para encontrar quantas ofertas ainda são necessárias e, em última análise, retornará um fallback, se necessário.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Se as duas coleções forem **avaliada ao mesmo tempo**, como há duas ofertas elegíveis da estratégia A e três ofertas elegíveis da estratégia B, as cinco ofertas serão empilhadas juntas com base no valor determinado pelos respectivos métodos de classificação. Duas ofertas são solicitadas, portanto, as duas principais ofertas qualificadas dessas cinco ofertas serão retornadas.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Exemplo com várias estratégias**

Agora, vamos considerar um exemplo em que você tem várias estratégias divididas em grupos diferentes.

Você definiu três estratégias. A Estratégia 1 e a Estratégia 2 são combinadas no Grupo 1 e a Estratégia 3 é independente (Grupo 2).

As ofertas elegíveis para cada estratégia e sua prioridade (usada na avaliação da função de classificação) são as seguintes:

* Grupo 1:
   * Estratégia 1 - (Oferta 1, Oferta 2, Oferta 3) - Prioridade 1
   * Estratégia 2 - (Oferta 3, Oferta 4, Oferta 5) - Prioridade 1

* Grupo 2:
   * Estratégia 3 - (Oferta 5, Oferta 6) - Prioridade 0

As ofertas de estratégia de maior prioridade são avaliadas primeiro e adicionadas à lista de ofertas classificadas.

**Iteração 1:**

As ofertas de Estratégia 1 e Estratégia 2 são avaliadas juntas (Oferta 1, Oferta 2, Oferta 3, Oferta 4, Oferta 5). Digamos que o resultado seja:

Oferta 1 - 10 Oferta 2 - 20 Oferta 3 - 30 da Estratégia 1, 45 da Estratégia 2. O mais alto de ambos será considerado, portanto, 45 é considerado.
Oferta 4 - 40 Oferta 5 - 50

As ofertas classificadas agora são: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

**Iteração 2:**

As ofertas da Estratégia 3 são avaliadas (Oferta 5, Oferta 6). Digamos que o resultado seja:

* Oferta 5 - Não será avaliado, pois já existe no resultado acima.
* Oferta 6 - 60

As ofertas classificadas agora são as seguintes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

+++

## Usar a política de decisão no editor de código {#use-decision-policy}

Depois de criada, a política de decisão pode ser usada na variável [editor de código](../code-based/create-code-based.md#edit-code). Para isso, siga as etapas abaixo.

>[!NOTE]
>
>O editor de código aproveita o [!DNL Journey Optimizer] Editor de expressão com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Clique no ícone +. O código correspondente à política de decisão é adicionado. Agora você pode adicionar todos os atributos de decisão desejados dentro desse código.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Essa sequência será repetida o número de vezes que você deseja que a política de decisão seja retornada. Por exemplo, se você optar por retornar 2 itens quando [criação da decisão](#add-decision), a mesma sequência será repetida duas vezes.

1. Clique na política de decisão. Os atributos de decisão são exibidos.

   Esses atributos são armazenados no **[!UICONTROL Ofertas]** esquema do catálogo. Os atributos personalizados são armazenados no **_cjmstage** pasta e atributos padrão no **_experience** pasta. [Saiba mais sobre o schema do catálogo de ofertas](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

1. Clique em cada pasta para expandi-la. Coloque o cursor do mouse no local desejado e clique no ícone + ao lado do atributo que deseja adicionar. Você pode adicionar quantos atributos desejar ao código.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Para navegar de volta para a raiz da política de decisão, clique no ícone de pasta.

   ![](assets/decision-code-based-decision-folder.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de expressão, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)
