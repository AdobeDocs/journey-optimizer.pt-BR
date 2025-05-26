---
title: Criar políticas de decisões
description: Saiba como criar políticas de decisões
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 0b7f76ca43ef8dda3861abf2c3b058cef725e967
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 12%

---

# Criar políticas de decisão {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="O que é uma decisão?"
>abstract="As políticas de decisão contêm toda a lógica de seleção, para que o mecanismo de decisão escolha o melhor conteúdo. As políticas de decisão são específicas de cada campanha. Sua finalidade é selecionar as melhores ofertas para cada perfil, enquanto a criação da campanha permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos dos itens devem ser incluídos na mensagem."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Sobre a decisão"

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo de decisão para escolher o melhor conteúdo a ser entregue, dependendo do público.

<!--Decision policies contain all of the selection logic for the decisioning engine to pick the best content. Decision policies are campaign specific. -->O objetivo é selecionar as melhores ofertas para cada perfil, enquanto a criação de campanha/jornada permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos de item devem ser incluídos na mensagem.

>[!NOTE]
>
>Na interface do usuário [!DNL Journey Optimizer], as políticas de decisão são rotuladas como decisões<!--but they are decision policies. TBC if this note is needed-->.

As principais etapas para aproveitar as políticas de decisão em suas campanhas baseadas em código são as seguintes:

1. [Adicionar uma política de decisão a uma experiência baseada em código](#add-decision)
1. [Usar a política de decisão](#use-decision-policy)
1. [Criar painéis de relatórios personalizados do Customer Journey Analytics](cja-reporting.md)

## Adicionar uma política de decisão a uma experiência baseada em código {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Defina o número de itens a serem retornados"
>abstract="Selecione o número de itens de decisão que deseja que sejam retornados. Por exemplo, se você selecionar 2, as duas melhores ofertas elegíveis serão apresentadas para a configuração atual."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selecione uma alternativa"
>abstract="Um item alternativo é exibido ao usuário(a) quando nenhuma das estratégias de seleção definidas para essa política de decisão está qualificada."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="O que é uma estratégia?"
>abstract="A sequência da estratégia de seleção determina qual estratégia será avaliada primeiro. Pelo menos uma estratégia é necessária. Os itens de decisão em estratégias combinadas serão avaliados em conjunto."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Criação de estratégias"

Para apresentar a melhor oferta dinâmica e experiência aos visitantes em seu site ou aplicativo móvel, adicione uma política de decisão a uma campanha ou jornada baseada em código. Para isso, siga as etapas abaixo.

### Criar a política de decisão {#add}

1. Crie uma campanha e selecione a ação **[!UICONTROL Experiência baseada em código]**. [Saiba mais](../code-based/create-code-based.md)

1. No [editor de código](../code-based/create-code-based.md#edit-code), selecione **[!UICONTROL Política de decisão]** e clique em **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-code-based-create.png)

1. Por padrão, crie uma nova política.

   >[!NOTE]
   >
   >Você também pode optar por selecionar uma política existente.

1. Preencha os detalhes da sua política de decisão: adicione um nome e selecione um catálogo.

   >[!NOTE]
   >
   >Atualmente, apenas o catálogo padrão **[!UICONTROL Ofertas]** está disponível.

1. Selecione o número de itens que você deseja retornar. Por exemplo, se você selecionar 2, as 2 melhores ofertas qualificadas serão apresentadas para a configuração atual. Clique em **[!UICONTROL Next]**.

   ![](assets/decision-code-based-details.png)

### Selecionar itens e estratégias de seleção {#select}

A seção **[!UICONTROL Sequência de estratégia]** permite selecionar os itens de decisão e as estratégias de seleção a serem apresentados com a política de decisão.

1. Clique no botão **[!UICONTROL Add]**.

1. Escolha o tipo de objeto a ser incluído na política:

   * **[!UICONTROL Estratégia de seleção]**: adicione uma ou várias estratégias de seleção. As estratégias de decisão usam coleções associadas a restrições de qualificação e métodos de classificação para determinar os itens a serem mostrados. Você pode selecionar uma estratégia de seleção existente ou criar uma nova usando o botão **[!UICONTROL Criar estratégia de seleção]**. [Saiba como criar estratégias de seleção](selection-strategies.md)

   * **[!UICONTROL Item de decisão]**: adicione itens de decisão únicos para apresentar sem ter que executar uma estratégia de seleção. Você só pode selecionar um item de decisão por vez. Quaisquer restrições de qualificação definidas para o item serão aplicadas.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >Uma política de decisão suporta até 10 estratégias de seleção e itens de decisão combinados. [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)

1. Ao adicionar vários itens e/ou estratégias de decisão, eles serão avaliados em uma ordem específica. O primeiro objeto adicionado à sequência será avaliado primeiro e assim por diante.

   Para alterar a sequência padrão, você pode arrastar e soltar os objetos e/ou grupos para reordená-los como desejado. [Saiba mais](#evaluation-order)

### Gerenciar ordem de avaliação em uma política de decisão {#evaluation-order}

Depois de adicionar itens de decisão e estratégias de seleção à sua política, você pode organizar a ordem para determinar a ordem de avaliação e combinar estratégias de seleção para avaliá-los juntos.

A **ordem sequencial** na qual os itens e as estratégias serão avaliados é indicada com números à esquerda de cada objeto ou grupo de objetos. Para mover a posição de uma estratégia de seleção (ou um grupo de estratégias) dentro da sequência, arraste e solte-a em outra posição.

>[!NOTE]
>
>Somente estratégias de seleção podem ser arrastadas e soltas em uma sequência. Para alterar a posição de um item de decisão, é necessário removê-lo e adicioná-lo novamente usando o botão **[!UICONTROL Adicionar]** depois de adicionar os outros itens que você deseja avaliar antes.

![](assets/decision-code-based-strategy-groups.png)

Você também pode **combinar** várias estratégias de seleção em grupos para que sejam avaliadas juntas e não separadamente. Para fazer isso, clique no botão **`+`** em uma estratégia de seleção para combiná-la com outra. Você também pode arrastar e soltar uma estratégia de seleção em outra para agrupar as duas estratégias em um grupo.

>[!NOTE]
>
>Os itens de decisão não podem ser agrupados com outros itens ou estratégias de seleção.

Várias estratégias e seus agrupamentos determinam a prioridade das estratégias e a classificação das ofertas elegíveis. A primeira estratégia tem a prioridade mais alta e as estratégias combinadas dentro do mesmo grupo têm a mesma prioridade.

Por exemplo, você tem duas coleções, uma na estratégia A e uma na estratégia B. A solicitação é para que dois itens de decisão sejam enviados de volta. Digamos que haja duas ofertas qualificadas da estratégia A e três ofertas qualificadas da estratégia B.

* Se as duas estratégias forem **não combinadas** ou em ordem sequencial (1 e 2), as duas principais ofertas qualificadas da primeira estratégia serão retornadas na primeira linha. Se não houver duas ofertas elegíveis para a primeira estratégia, o mecanismo de decisão seguirá para a próxima estratégia em sequência para encontrar quantas ofertas ainda são necessárias e, em última análise, retornará um fallback, se necessário.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Se as duas coleções forem **avaliadas ao mesmo tempo**, como há duas ofertas qualificadas da estratégia A e três ofertas qualificadas da estratégia B, as cinco ofertas serão empilhadas juntas com base no valor determinado pelos respectivos métodos de classificação. Duas ofertas são solicitadas, portanto, as duas principais ofertas qualificadas dessas cinco ofertas serão retornadas.

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

Oferta 1 - 10
Oferta 2 - 20
Oferta 3 - 30 da Estratégia 1, 45 da Estratégia 2. O mais alto de ambos será considerado, portanto, 45 é considerado.
Oferta 4 - 40
Oferta 5 - 50

As ofertas classificadas agora são: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

**Iteração 2:**

As ofertas da Estratégia 3 são avaliadas (Oferta 5, Oferta 6). Digamos que o resultado seja:

* Oferta 5 - Não será avaliado, pois já existe no resultado acima.
* Oferta 6 - 60

As ofertas classificadas agora são as seguintes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

+++

### Adicionar ofertas substitutas {#fallback}

Depois de selecionar itens de decisão e/ou estratégias de seleção, você pode adicionar ofertas substitutas que serão exibidas para os usuários se nenhum dos itens ou estratégias de seleção acima for qualificado.

![](assets/decision-code-based-strategy-fallback.png)

Você pode selecionar qualquer item da lista, que exibe todos os itens de decisão criados na sandbox atual. Se nenhuma estratégia de seleção for qualificada, o fallback será exibido para o usuário, independentemente das datas e da restrição de qualificação aplicada ao item selecionado<!--nor frequency capping when available - TO CLARIFY-->.

>[!NOTE]
>
>Um fallback é opcional. Se nenhum fallback for selecionado e nenhuma estratégia for qualificada, nada será exibido por [!DNL Journey Optimizer]. Você pode adicionar até o número de itens que a política de decisão está solicitando. Isso garante que um determinado número de itens seja retornado, se desejado, para o caso de uso.

Quando a política de decisão estiver pronta, salve-a e clique em **[!UICONTROL Criar]**. Agora que a política de decisão foi criada, você pode usar os atributos de decisão dentro do conteúdo de experiência baseado em código. [Saiba mais](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## Usar a política de decisão no editor de código {#use-decision-policy}

Depois de criada, a política de decisão pode ser usada no [editor de personalização](../code-based/create-code-based.md#edit-code). Para isso, siga as etapas abaixo.

>[!NOTE]
>
>A experiência baseada em código aproveita o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Clique no botão **[!UICONTROL Inserir política]**. O código correspondente à política de decisão é adicionado.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Essa sequência será repetida o número de vezes que você deseja que a política de decisão seja retornada. Por exemplo, se você optar por retornar dois itens ao [criar a decisão](#add-decision), a mesma sequência será repetida duas vezes.

1. Agora você pode adicionar todos os atributos de decisão desejados dentro desse código. Os atributos disponíveis são armazenados no esquema do catálogo **[!UICONTROL Ofertas]**. Os atributos personalizados são armazenados na pasta **`_<imsOrg`>** e os atributos padrão na pasta **`_experience`**. [Saiba mais sobre o esquema do catálogo de Ofertas](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Para o rastreamento de itens da política de decisão, o atributo `trackingToken` precisa ser adicionado da seguinte maneira para o conteúdo da política de decisão:
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Clique em cada pasta para expandi-la. Coloque o cursor do mouse no local desejado e clique no ícone + ao lado do atributo que deseja adicionar. Você pode adicionar quantos atributos desejar ao código.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Você também pode adicionar qualquer outro atributo disponível no editor de personalização, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Clique em **[!UICONTROL Salvar e fechar]** para confirmar as alterações.

1. Revise e publique sua campanha de experiência ou jornada baseada em código. [Saiba como](../code-based/publish-code-based.md)

   Agora, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

   >[!NOTE]
   >
   >Atualmente não é possível simular o conteúdo da interface do usuário em uma campanha ou jornada de [experiência baseada em código](../code-based/create-code-based.md) usando decisões. Uma solução alternativa está disponível em [esta seção](../code-based/code-based-decisioning-implementations.md).

1. Para ver o desempenho de suas decisões, você pode criar [painéis de relatórios personalizados do Customer Journey Analytics](cja-reporting.md).


