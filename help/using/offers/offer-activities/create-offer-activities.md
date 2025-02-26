---
title: Criar decisões
description: Saiba como criar decisões
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 2e1168f321d6f2c83733c6112e11d834d5e7eb95
workflow-type: tm+mt
source-wordcount: '2511'
ht-degree: 9%

---

# Criar decisões {#create-offer-activities}

As decisões são containers para suas ofertas que aproveitarão o Mecanismo do Offer Decisioning para escolher a melhor oferta a ser entregue, dependendo do target da entrega.

➡️ [Saiba como criar atividades de oferta neste vídeo](#video)

A lista de decisões está acessível no menu **[!UICONTROL Ofertas]** > na guia **[!UICONTROL Decisões]**. Os filtros estão disponíveis para ajudar você a recuperar decisões de acordo com seu status ou datas de início e término.

![](../assets/activities-list.png)

Antes de criar uma decisão, verifique se os componentes abaixo foram criados na Biblioteca de ofertas:

* [Disposições](../offer-library/creating-placements.md)
* [Coleções](../offer-library/creating-collections.md)
* [Ofertas personalizadas](../offer-library/creating-personalized-offers.md)
* [Ofertas substitutas](../offer-library/creating-fallback-offers.md)

## Criar a decisão {#create-activity}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_details"
>title="Detalhes da decisão de oferta"
>abstract="Especifique o nome da decisão e defina uma data e hora inicial e final, se necessário. Para atribuir rótulos de uso de dados personalizados ou principais à decisão, selecione **[!UICONTROL Gerenciar acesso]**."

1. Acesse a lista de decisões e clique em **[!UICONTROL Criar decisão]**.

1. Especifique o nome da decisão.

1. Defina uma data e hora de início e término, se necessário, e clique em **[!UICONTROL Avançar]**.

   ![](../assets/activities-name.png)

1. Para atribuir rótulos de uso de dados personalizados ou principais à decisão, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../../administration/object-based-access.md)

## Definir escopos de decisão {#add-decision-scopes}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_scopes"
>title="Escopos de decisão"
>abstract="Configure um ou vários escopos para a decisão de oferta, a fim de determinar as ofertas a serem exibidas. Para isso, selecione um posicionamento e um critério de avaliação associado para esse posicionamento."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_placement"
>title="Posicionamento"
>abstract="Selecione um posicionamento onde as ofertas serão entregues."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_evaluation"
>title="Critérios de avaliação"
>abstract="Os critérios de avaliação consistem em uma coleção de ofertas associada a uma restrição de qualificação e um método de classificação para determinar as ofertas que aparecerão no posicionamento. A sequência dos critérios de avaliação determina qual coleção será avaliada primeiro. É necessário pelo menos um critério de avaliação."

1. Selecione uma disposição na lista suspensa. Ele será adicionado ao escopo da primeira decisão na sua decisão.

   ![](../assets/activities-placement.png)

1. Clique em **[!UICONTROL Adicionar]** para selecionar os critérios de avaliação para este posicionamento.

   ![](../assets/activities-evaluation-criteria.png)

   Cada critério consiste em uma coleção de ofertas associada a uma restrição de qualificação e um método de classificação para determinar as ofertas a serem mostradas no posicionamento.

   >[!NOTE]
   >
   >É necessário pelo menos um critério de avaliação.

1. Selecione a coleção de ofertas que contém as ofertas a serem consideradas e clique em **[!UICONTROL Adicionar]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Você pode clicar no link **[!UICONTROL Abrir coleções de ofertas]** para exibir a lista de coleções em uma nova guia, que permite procurar as coleções e as ofertas que elas contêm.

   A coleção selecionada é adicionada aos critérios.

   ![](../assets/activities-collection-added.png)

1. Use o campo **[!UICONTROL Qualificação]** para restringir a seleção de ofertas para este posicionamento.

   Esta restrição pode ser aplicada usando uma **regra de decisão** ou um ou vários **públicos-alvo da Adobe Experience Platform**. Ambos estão detalhados em [esta seção](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * Para restringir a seleção das ofertas aos membros de um público do Experience Platform, selecione **[!UICONTROL Públicos-alvo]** e clique em **[!UICONTROL Adicionar públicos-alvo]**.

     ![](../assets/activity_constraint_segment.png)

     Adicione um ou vários públicos-alvo do painel esquerdo e combine-os usando os operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]**.

     ![](../assets/activity_constraint_segment2.png)

     Saiba como trabalhar com públicos-alvo [nesta seção](../../audience/about-audiences.md).

   * Se quiser adicionar uma restrição de seleção com uma regra de decisão, use a opção **[!UICONTROL Regra de decisão]** e selecione a regra de sua escolha.

     ![](../assets/activity_constraint_rule.png)

     Saiba como criar uma regra de decisão em [esta seção](../offer-library/creating-decision-rules.md).

1. Ao selecionar públicos ou regras de decisão, você pode ver informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar os dados.

   >[!NOTE]
   >
   >As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que exige que o tempo atual seja ≥ 80 graus.

   ![](../assets/activity_constraint-estimate.png)

1. Defina o método de classificação que deseja usar para selecionar a melhor oferta para cada perfil. [Saiba mais](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * Por padrão, se várias ofertas estiverem qualificadas para esta inserção, o método **[!UICONTROL Offer priority]** usará o valor definido nas ofertas: a oferta com a pontuação de prioridade mais alta será entregue ao usuário.

   * Se quiser usar uma pontuação calculada específica para escolher qual oferta qualificada fornecer, selecione **[!UICONTROL Fórmula]** ou **[!UICONTROL Modelo de IA]**. [Saiba mais](../offer-activities/configure-offer-selection.md).

1. Clique em **[!UICONTROL Adicionar]** para definir mais critérios para o mesmo posicionamento.

   ![](../assets/activity_add-collection.png)

1. Quando você adiciona vários critérios, eles são avaliados em uma ordem específica. A primeira coleção que foi adicionada à sequência será avaliada primeiro e assim por diante. [Saiba mais](#evaluation-criteria-order)

   Para alterar a sequência padrão, é possível arrastar e soltar as coleções para reorganizá-las conforme desejado.

   ![](../assets/activity_reorder-collections.png)

1. Você também pode avaliar vários critérios ao mesmo tempo. Para fazer isso, arraste e solte a coleção sobre outra.

   ![](../assets/activity_move-collection.png)

   Agora eles têm a mesma classificação e, portanto, serão avaliados ao mesmo tempo. [Saiba mais](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

   >[!CAUTION]
   >
   >* Se o [modelo de IA](../ranking/ai-models.md) for usado em um grupo de critérios de avaliação, todos os critérios de avaliação desse grupo deverão usar o método de classificação de IA e deverão usar o mesmo modelo de IA específico.
   >
   >* Somente um grupo de critérios de avaliação pode usar o modelo de IA. Quaisquer outros grupos dentro de um escopo de decisão devem usar outros métodos de classificação (prioridade ou fórmula). [Saiba mais sobre os métodos de classificação](../offer-activities/configure-offer-selection.md)

1. Para adicionar outro posicionamento para suas ofertas como parte desta decisão, use o botão **[!UICONTROL Novo escopo]**. Repita as etapas acima para cada escopo de decisão.

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >Ao adicionar vários escopos de decisão, a ordem dos critérios de avaliação será afetada. [Saiba mais](#multiple-scopes)

### Ordem dos critérios de avaliação {#evaluation-criteria-order}

Conforme descrito acima, um critério de avaliação consiste em uma coleção, restrições de elegibilidade e um método de classificação. Você pode definir a ordem sequencial desejada para que os critérios de avaliação sejam avaliados, mas também pode combinar vários critérios de avaliação para que eles sejam avaliados juntos e não separadamente.

#### Com um escopo {#one-scope}

Dentro de um único escopo de decisão, vários critérios e seus agrupamentos determinam a prioridade dos critérios e a classificação das ofertas qualificadas. O primeiro critério tem a prioridade mais alta e o critério combinado no mesmo &quot;grupo&quot; tem a mesma prioridade.

Por exemplo, você tem duas coleções, uma no critério de avaliação A e outra no critério de avaliação B. A solicitação é para que duas ofertas sejam enviadas de volta. Digamos que existam duas ofertas elegíveis do critério de avaliação A e três ofertas elegíveis do critério de avaliação B.

* Se os dois critérios de avaliação forem **não combinados** e/ou em ordem sequencial (1 e 2), as duas principais ofertas qualificadas dos critérios de avaliação serão retornadas na primeira linha. Se não houver duas ofertas elegíveis para o primeiro critério de avaliação, o mecanismo de decisão seguirá para os próximos critérios de avaliação em sequência para encontrar quantas ofertas ainda são necessárias e, em última análise, retornará um fallback, se necessário.

  ![](../assets/activity_consecutive-rank-collections.png)

* Se as duas coleções forem **avaliadas ao mesmo tempo**, como há duas ofertas qualificadas do critério de avaliação A e três ofertas qualificadas do critério de avaliação B, as cinco ofertas serão classificadas juntas com base no valor determinado pelos respectivos métodos de classificação. Duas ofertas são solicitadas, portanto, as duas principais ofertas qualificadas dessas cinco ofertas serão retornadas.

  ![](../assets/activity_same-rank-collections.png)

+++ **Exemplo com vários critérios**

Agora, vamos considerar um exemplo em que você tem vários critérios para um único escopo dividido em grupos diferentes.

Você definiu três critérios. O critério 1 e o critério 2 são combinados no grupo 1 e o critério 3 é independente (grupo 2).

As ofertas elegíveis para cada critério e sua prioridade (usada na avaliação da função de classificação) são as seguintes:

* Grupo 1:
   * Critério 1 - (Oferta 1, Oferta 2, Oferta 3) - Prioridade 1
   * Critério 2 - (Oferta 3, Oferta 4, Oferta 5) - Prioridade 1

* Grupo 2:
   * Critério 3 - (Oferta 5, Oferta 6) - Prioridade 0

As ofertas de critérios de prioridade mais alta são avaliadas primeiro e adicionadas à lista de ofertas classificadas.

**Iteração 1:**

As ofertas dos Critérios 1 e 2 são avaliadas em conjunto (Oferta 1, Oferta 2, Oferta 3, Oferta 4, Oferta 5). Digamos que o resultado seja:

Oferta 1 - 10
Oferta 2 - 20
Oferta 3 - 30 do Critério 1, 45 do Critério 2. O mais alto de ambos será considerado, portanto, 45 é considerado.
Oferta 4 - 40
Oferta 5 - 50

As ofertas classificadas agora são as seguintes: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

**Iteração 2:**

As ofertas do critério 3 são avaliadas (Oferta 5, Oferta 6). Digamos que o resultado seja:

* Oferta 5 - Não será avaliado, pois já existe no resultado acima.
* Oferta 6 - 60

As ofertas classificadas agora são as seguintes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

+++

#### Com vários escopos {#multiple-scopes}

**Se a duplicação estiver desativada**

Quando você adiciona vários escopos de decisão a uma decisão e se a duplicação não for permitida entre posicionamentos, as ofertas elegíveis serão selecionadas sequencialmente na ordem dos escopos de decisão na solicitação.

>[!NOTE]
>
>O parâmetro **[!UICONTROL Permitir Duplicatas em posicionamentos]** está definido no nível de posicionamento. Se a duplicação for definida como falso para qualquer posicionamento em uma solicitação de decisão, todas as inserções na solicitação herdarão a configuração falso. [Saiba mais sobre o parâmetro de duplicação](../offer-library/creating-placements.md)

Vamos ver um exemplo em que você adicionou dois escopos de decisão, como:

* Escopo 1: Há quatro ofertas qualificadas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) e a solicitação é para duas ofertas serem enviadas de volta.
* Escopo 2: há quatro ofertas qualificadas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) e a solicitação é para duas ofertas serem enviadas de volta.

+++ **Exemplo 1**

A seleção é a seguinte:

1. As duas principais ofertas qualificadas do Escopo 1 serão retornadas (Oferta 1, Oferta 2).
1. As duas principais ofertas qualificadas restantes do Escopo 2 serão retornadas (Oferta 3, Oferta 4).

+++

+++ **Exemplo 2**

Neste exemplo, a Oferta 1 atingiu seu limite de frequência. [Saiba mais sobre limite de frequência](../offer-library/add-constraints.md#capping)

A seleção é a seguinte:

1. As duas principais ofertas qualificadas restantes do Escopo 1 serão retornadas (Oferta 2, Oferta 3).
1. A oferta qualificada restante do Escopo 2 será retornada (Oferta 4).

+++

+++ **Exemplo 3**

Neste exemplo, a Oferta 1 e a Oferta 3 atingiram seu limite de frequência. [Saiba mais sobre limite de frequência](../offer-library/add-constraints.md#capping)

A seleção é a seguinte:

1. As duas principais ofertas qualificadas restantes do Escopo 1 serão retornadas (Oferta 2, Oferta 4).
1. Não há ofertas qualificadas restantes para o Escopo 2, portanto, a [oferta substituta](#add-fallback) é retornada.

+++

**Se a duplicação estiver ativada**

Quando a duplicação é permitida em todos os posicionamentos, a mesma oferta pode ser proposta várias vezes em diferentes posicionamentos. Se ativado, o sistema considerará a mesma oferta para vários posicionamentos. [Saiba mais sobre o parâmetro de duplicação](../offer-library/creating-placements.md)

Vamos ver o mesmo exemplo acima em que você adicionou dois escopos de decisão, como:

* Escopo 1: Há quatro ofertas qualificadas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) e a solicitação é para duas ofertas serem enviadas de volta.
* Escopo 2: há quatro ofertas qualificadas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) e a solicitação é para duas ofertas serem enviadas de volta.

+++ **Exemplo 1**

A seleção é a seguinte:

1. As duas principais ofertas qualificadas do Escopo 1 serão retornadas (Oferta 1, Oferta 2).
1. As mesmas duas principais ofertas qualificadas do Escopo 2 serão retornadas (Oferta 1, Oferta 2).

+++

+++ **Exemplo 2**

Neste exemplo, a Oferta 1 atingiu seu limite de frequência. [Saiba mais sobre limite de frequência](../offer-library/add-constraints.md#capping)

A seleção é a seguinte:

1. As duas principais ofertas qualificadas restantes do Escopo 1 serão retornadas (Oferta 2, Oferta 3).

1. As mesmas duas principais ofertas qualificadas restantes do Escopo 2 serão retornadas (Oferta 2, Oferta 3).

+++

+++ **Exemplo 3**

Neste exemplo, a Oferta 1 e a Oferta 3 atingiram seu limite de frequência. [Saiba mais sobre limite de frequência](../offer-library/add-constraints.md#capping)

A seleção é a seguinte:

1. As duas principais ofertas qualificadas restantes do Escopo 1 serão retornadas (Oferta 2, Oferta 4).

1. As mesmas duas principais ofertas qualificadas restantes do Escopo 2 serão retornadas (Oferta 2, Oferta 4).

+++

## Adicionar uma oferta substituta {#add-fallback}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_fallback"
>title="Adicionar uma oferta substituta"
>abstract="Depois de definir os escopos de decisão, defina a oferta substituta que será apresentada como último recurso a clientes que não corresponderem às restrições e regras de elegibilidade da oferta."

Depois de definir os escopos de decisão, defina a oferta substituta que será apresentada como último recurso a clientes que não corresponderem às restrições e regras de elegibilidade da oferta.

Para fazer isso, selecione-o na lista de ofertas substitutas disponíveis para os posicionamentos definidos na decisão e clique em **[!UICONTROL Avançar]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Você pode clicar no link **[!UICONTROL Abrir biblioteca de ofertas]** para exibir a lista de ofertas em uma nova guia.

## Revisar e salvar a decisão {#review}

Se tudo estiver configurado corretamente, um resumo das propriedades de decisão será exibido.

1. Verifique se a decisão está pronta para ser usada para apresentar ofertas aos clientes. Todos os escopos de decisão e a oferta substituta que ele contém são exibidos.

   ![](../assets/review-decision.png)

1. É possível expandir ou recolher cada posicionamento. É possível visualizar as ofertas disponíveis, a qualificação e os detalhes de classificação para cada posicionamento. Também é possível exibir informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar os dados.

   ![](../assets/review-decision-details.png)

1. Clique em **[!UICONTROL Concluir]**.
1. Selecione **[!UICONTROL Salvar e ativar]**.

   ![](../assets/save-activities.png)

   Você também pode salvar a decisão como rascunho para editá-la e ativá-la posteriormente.

A decisão é exibida na lista com o status **[!UICONTROL Ativo]** ou **[!UICONTROL Rascunho]**, dependendo se você o ativou ou não na etapa anterior.

Agora ele está pronto para ser usado para fornecer ofertas aos clientes.

## Lista de decisões {#decision-list}

Na lista de decisões, é possível selecionar a decisão para exibir suas propriedades. Você também pode editá-lo, alterar seu status (**Rascunho**, **Ao Vivo**, **Concluído**, **Arquivado**), duplicar a decisão ou excluí-la.

![](../assets/decision_created.png)

Selecione o botão **[!UICONTROL Editar]** para voltar para o modo de edição de decisão, no qual você pode modificar os [detalhes](#create-activity), [escopos de decisão](#add-decision-scopes) e [oferta substituta](#add-fallback) da decisão.

>[!IMPORTANT]
>
>Se forem feitas alterações em uma decisão de oferta em uso na mensagem de uma jornada, será necessário desfazer a publicação da jornada e republicá-la.  Isso garantirá que as alterações sejam incorporadas à mensagem da jornada e que ela seja consistente com as atualizações mais recentes.

Selecione uma decisão em tempo real e clique em **[!UICONTROL Desativar]** para retornar o status da decisão para **[!UICONTROL Rascunho]**.

Para definir novamente o status como **[!UICONTROL Live]**, selecione o botão **[!UICONTROL Ativar]** que agora é exibido.

![](../assets/decision_activate.png)

O botão **[!UICONTROL Mais ações]** habilita as ações descritas abaixo.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Concluído]**: define o status da decisão como **[!UICONTROL Concluído]**, o que significa que a decisão não pode mais ser chamada. Esta ação só está disponível para decisões ativadas. A decisão ainda está disponível na lista, mas você não pode definir seu status novamente como **[!UICONTROL Rascunho]** ou **[!UICONTROL Aprovado]**. Você só pode duplicá-lo, excluí-lo ou arquivá-lo.

* **[!UICONTROL Duplicar]**: cria uma decisão com as mesmas propriedades, escopos de decisão e oferta substituta. Por padrão, a nova decisão tem o status **[!UICONTROL Rascunho]**.

* **[!UICONTROL Excluir]**: remove a decisão da lista.

  >[!CAUTION]
  >
  >A decisão e seu conteúdo não estarão mais acessíveis. Essa ação não pode ser desfeita.
  >
  >Se a decisão for usada em outro objeto, ela não poderá ser excluída.

* **[!UICONTROL Arquivar]**: define o status de decisão como **[!UICONTROL Arquivado]**. A decisão ainda está disponível na lista, mas você não pode definir seu status novamente como **[!UICONTROL Rascunho]** ou **[!UICONTROL Aprovado]**. Você só pode duplicá-la ou excluí-la.

Você também pode excluir ou alterar o status de várias decisões ao mesmo tempo marcando as caixas de seleção correspondentes.

![](../assets/decision_multiple-selection.png)

Se você quiser alterar o status de várias decisões com status diferentes, somente os status relevantes serão alterados.

![](../assets/decision_change-status.png)

Depois que uma decisão for criada, você poderá clicar no nome na lista.

![](../assets/decision_click-name.png)

Isso permite que você acesse informações detalhadas para essa decisão. Selecione a guia **[!UICONTROL Log de alterações]** para [monitorar todas as alterações](../get-started/user-interface.md#changes-log) feitas na decisão.

![](../assets/decision_information.png)

## Vídeo tutorial{#video}

Saiba como criar atividades de oferta na gestão de decisões.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


