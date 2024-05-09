---
title: Criar políticas de decisões
description: Saiba como criar políticas de decisões
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilidade limitada"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 5b36d082e054b7b75b09bd0392f9a58527a9c0a3
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 10%

---

# Criar políticas de decisão {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="O que é uma decisão?"
>abstract="As políticas de decisão contêm toda a lógica de seleção para que o mecanismo de decisão escolha o melhor conteúdo. As políticas de decisão são específicas de campanha. O objetivo é selecionar as melhores ofertas para cada perfil, enquanto a criação da campanha permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos de item devem ser incluídos na mensagem."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Sobre o Offer Decisioning"

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo do Experience Decisioning para escolher o melhor conteúdo a ser entregue, dependendo do público.

As políticas de decisão contêm toda a lógica de seleção para que o mecanismo de decisão escolha o melhor conteúdo. As políticas de decisão são específicas de campanha. O objetivo é selecionar as melhores ofertas para cada perfil, enquanto a criação da campanha permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos de item devem ser incluídos na mensagem.

>[!NOTE]
>
>No [!DNL Journey Optimizer] interface do usuário, as políticas de decisão são rotuladas como decisões<!--but they are decision policies. TBC if this note is needed-->.

## Adicionar uma política de decisão a uma campanha baseada em código {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Defina o número de itens a serem retornados"
>abstract="Selecione o número de itens de decisão que deseja que sejam retornados. Por exemplo, se você selecionar 2, as 2 melhores ofertas elegíveis serão apresentadas para a superfície atual."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selecione uma alternativa"
>abstract="Um item alternativo é exibido ao usuário(a) quando nenhuma das estratégias de seleção definidas para essa política de decisão está qualificada."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="O que é uma estratégia?"
>abstract="A sequência da estratégia de seleção determina qual estratégia será avaliada primeiro. Pelo menos uma estratégia é necessária. Os itens de decisão em estratégias combinadas serão avaliados em conjunto."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Criação de estratégias"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Ordem de avaliação"

Para apresentar a melhor oferta dinâmica e experiência aos visitantes em seu site ou aplicativo móvel, adicione uma política de decisão a uma campanha baseada em código. Para isso, siga as etapas abaixo.

1. Crie uma campanha e selecione o **[!UICONTROL Experiência baseada em código]** ação. [Saiba mais](../code-based/create-code-based.md)

1. No [editor de código](../code-based/create-code-based.md#edit-code), selecione o **[!UICONTROL Política de decisão]** e clique em **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-code-based-create.png)

1. Preencha os detalhes da sua política de decisão: adicione um nome e selecione um catálogo.

   >[!NOTE]
   >
   >Atualmente, apenas o padrão **[!UICONTROL Ofertas]** catálogo está disponível.

   ![](assets/decision-code-based-details.png)

1. Selecione o número de itens que você deseja retornar. Por exemplo, se você selecionar 2, as 2 melhores ofertas qualificadas serão apresentadas para a superfície atual. Clique em **[!UICONTROL Próxima]**

1. Use o **[!UICONTROL Adicionar estratégia]** botão para definir as estratégias de seleção para sua política de decisão. Cada estratégia consiste em uma coleção de ofertas associada a uma restrição de qualificação e um método de classificação para determinar as ofertas a serem exibidas. [Saiba mais](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >Pelo menos uma estratégia é necessária. Não é possível adicionar mais de 10 estratégias.

1. No **[!UICONTROL Adicionar estratégia]** também é possível criar uma estratégia. A variável **[!UICONTROL Criar estratégia de seleção]** O botão redireciona você para a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Configuração da estratégia]** menu. [Saiba mais](selection-strategies.md)

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

1. Salve a seleção e clique em **[!UICONTROL Criar]**. Agora que a política de decisão foi criada, você pode usar os atributos de decisão dentro do conteúdo de experiência baseado em código. [Saiba mais](#use-decision-policy)

   ![](assets/decision-code-based-decision-added.png)

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

Depois de criada, a política de decisão pode ser usada na variável [Editor de expressão](../code-based/create-code-based.md#edit-code). Para isso, siga as etapas abaixo.

>[!NOTE]
>
>A experiência baseada em código aproveita o [!DNL Journey Optimizer] Editor de expressão com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Clique em **[!UICONTROL Inserir política]** botão. O código correspondente à política de decisão é adicionado.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Essa sequência será repetida o número de vezes que você deseja que a política de decisão seja retornada. Por exemplo, se você optar por retornar 2 itens quando [criação da decisão](#add-decision), a mesma sequência será repetida duas vezes.

1. Agora você pode adicionar todos os atributos de decisão desejados dentro desse código. Os atributos disponíveis são armazenados no **[!UICONTROL Ofertas]** esquema do catálogo. Os atributos personalizados são armazenados no **`_<imsOrg`>** pasta e atributos padrão no **`_experience`** pasta. [Saiba mais sobre o schema do catálogo de ofertas](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Para rastreamento de item da política de decisão, a variável `trackingToken`O atributo precisa ser adicionado da seguinte maneira para o conteúdo da política de decisão:
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Clique em cada pasta para expandi-la. Coloque o cursor do mouse no local desejado e clique no ícone + ao lado do atributo que deseja adicionar. Você pode adicionar quantos atributos desejar ao código.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de expressão, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

## Relatório no Customer Journey Analytics {#cja}

Se estiver trabalhando com o Customer Journey Analytics, você pode criar painéis de relatórios personalizados para suas campanhas baseadas em código aproveitando o Experience Decisioning.

As principais etapas estão listadas abaixo. Informações detalhadas sobre como trabalhar com o Customer Journey Analytics estão disponíveis no [Documentação do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Criar e configurar um **conexão** em Customer Journey Analytics. Isso permite que você se conecte ao conjunto de dados para o qual deseja relatórios. [Saiba como criar uma conexão](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Criar um **visualização de dados** e associá-lo à conexão criada anteriormente. No **[!UICONTROL Componentes]** escolha os campos de esquema relevantes que deseja exibir nos relatórios. Para o Experience Decisioning, inclua a variável **propositioninteraction** e **propositiondisplay** campos. [Saiba como criar e configurar visualizações de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combinar componentes de dados, tabelas e visualizações em **projetos do workspace** para criar e compartilhar relatórios para sua campanha baseada em código.[Saiba como criar projetos do Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
