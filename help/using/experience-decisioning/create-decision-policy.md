---
title: Criar políticas de decisões
description: Saiba como criar políticas de decisões
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
exl-id: e7a89354-28ea-431f-a15d-a8c18946d266
source-git-commit: 743165991c3f4d351cd6ab15e94ece0309c8e82a
workflow-type: tm+mt
source-wordcount: '2108'
ht-degree: 6%

---

# Criar políticas de decisão {#create-decision}

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

Para apresentar a melhor oferta dinâmica e experiência aos seus clientes, adicione uma política de decisão ao seu conteúdo em uma campanha ou jornada e configure os itens a serem retornados e a estratégia de seleção a ser usada. Para isso, siga as etapas abaixo:

1. [Adicionar uma política de decisão](#add)
1. [Configurar a política de decisão](#configure) - Adicione um nome e especifique o número de itens a serem retornados para o canal de email.
1. [Configurar uma sequência de estratégia](#strategy) - Selecione os itens a serem retornados com a política de decisão.
1. [Selecionar ofertas substitutas](#fallback) (opcional) - Selecione os itens a serem exibidos se nenhum item ou estratégia de seleção estiver qualificado.
1. [Revisar e salvar](#review) a estratégia de seleção
1. [Atribuir um posicionamento](#placement) (Canal de email)

>[!AVAILABILITY]
>
>As políticas de decisão estão disponíveis para todos os clientes para a **Experiência baseada em código**, **Notificação por push** e canais SMS.
>
>A Decisão do canal de email está disponível com disponibilidade limitada. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Adicionar uma política de decisão {#add}

Para adicionar uma política de decisão em sua mensagem, abra uma jornada ou campanha e selecione uma [ação de canal](../building-journeys/journeys-message.md).

Edite o conteúdo da mensagem e navegue pelas guias abaixo para obter mais informações sobre como adicionar a política de decisão com base no canal selecionado.

>[!BEGINTABS]

>[!TAB Experiência baseada em código]

Para experiências baseadas em código, você pode adicionar uma nova política de decisão usando o **editor de código** ou o menu **Decisão** disponível no painel de propriedades.

+++Adicionar uma política de decisão do editor de código

1. Abra o editor de código usando o botão **[!UICONTROL Editar código]**.

1. Navegue até o menu **[!UICONTROL Política de decisão]** e clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Adicionar uma política de decisão no menu Decisão

1. Clique no ícone ![](assets/do-no-localize/decisioning-icon.png) no painel de propriedades para acessar o menu **[!UICONTROL Decisão]**.

1. Clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB Email]

1. Alterne a opção **[!UICONTROL Habilitar decisão]**.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >A ativação da decisão apaga o conteúdo de email existente. Se você já criou seu email, salve o conteúdo como um modelo antes.

1. Adicione uma nova política de decisão, usando o **editor de personalização** ou o menu **Decisão** disponível no Designer de email.

   +++Adicionar uma política de decisão do editor do Personalization

   1. Abra o editor de personalização usando o ícone ![](assets/do-no-localize/editor-icon.svg) disponível no campo de linha de assunto ou em qualquer campo no corpo do email, onde você pode adicionar personalização.

   1. Navegue até o menu **[!UICONTROL Políticas de decisão]** e clique no botão **[!UICONTROL Adicionar política de decisão]**.

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++Adicionar uma política de decisão no menu Decisão

   1. Abra o Designer de email e selecione qualquer componente na estrutura do email.

   1. Clique no ícone ![](assets/do-no-localize/decisioning-icon.png) no painel de propriedades para acessar o menu **[!UICONTROL Decisão]**.

   1. Clique no botão **[!UICONTROL Adicionar nova política]**.

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >A **[!UICONTROL Reutilizar saída de decisão]** permite reutilizar uma política de decisão que já foi criada neste email.

>[!TAB SMS]

Para SMS, você pode adicionar uma nova política de decisão usando o **editor de personalização** ou o menu **Decisão** disponível no painel de propriedades.

+++Adicionar uma política de decisão do editor de personalização

1. Abra o editor de personalização usando o ícone ![](assets/do-no-localize/editor-icon.svg).
1. Navegue até o menu **[!UICONTROL Políticas de decisão]** e clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++Adicionar uma política de decisão no menu Decisão

1. Clique no ícone ![](assets/do-no-localize/decisioning-icon.png) no painel de propriedades para acessar o menu **[!UICONTROL Decisão]**.

1. Clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-sms.png)

>[!TAB Notificação por push]

Para notificações por push, você pode adicionar uma nova política de decisão usando o **editor de personalização** ou o menu **Decisão** disponível no painel de propriedades.

+++Adicionar uma política de decisão do editor de personalização

1. Abra o editor de personalização usando o ícone ![](assets/do-no-localize/editor-icon.svg).
1. Navegue até o menu **[!UICONTROL Políticas de decisão]** e clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-push.png)

+++

+++Adicionar uma política de decisão no menu Decisão

1. Clique no ícone ![](assets/do-no-localize/decisioning-icon.png) no painel de propriedades para acessar o menu **[!UICONTROL Decisão]**.

1. Clique no botão **[!UICONTROL Adicionar política de decisão]**.

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>O Experience Decisioning com notificações por push requer uma versão específica do Mobile SDK. Antes de implementar este recurso, verifique as [notas de versão](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar a versão necessária e se você atualizou adequadamente. Você também pode exibir todas as versões do SDK disponíveis para sua plataforma [nesta seção](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

>[!ENDTABS]

## Configurar a política de decisão {#configure}

Após ter adicionado uma nova política de decisão ao seu conteúdo, a tela de configuração da política de decisão é aberta. Siga estas etapas para configurar a política de decisão:

1. Forneça um nome para a política de decisão e selecione um catálogo (atualmente limitado ao catálogo padrão **[!UICONTROL Ofertas]**).

   ![](assets/decision-code-based-details.png)

1. O campo **[!UICONTROL Número de itens]** permite definir o número de itens de decisão a serem retornados com a política de decisão. Por exemplo, se você selecionar 2, as duas melhores ofertas elegíveis serão apresentadas para a configuração atual.

   >[!NOTE]
   >
   >Essa opção está disponível somente para os canais de experiência baseados em email e código. Para todos os outros canais, somente um item de decisão pode ser retornado por ação.

   Para retornar vários itens para o Canal de email, é necessário adicionar a política de decisão em um componente de **[!UICONTROL Grade de Repetição]**. Expanda a seção abaixo para obter mais detalhes:

   +++Retornar vários itens de decisão por email

   1. Arraste um componente **[!UICONTROL Repetir Grade]** no seu email e configure-o como desejado usando o painel **[!UICONTROL Configurações]**.

      ![](assets/decision-policy-repeat.png)

   1. Clique no ícone **[!UICONTROL Decisão]** na barra de ferramentas da tela ou abra o painel **[!UICONTROL Decisão]** e selecione **[!UICONTROL Adicionar política de decisão]**.

   1. Especifique o número de itens a serem retornados no campo **[!UICONTROL Número de itens]** e configure a política de decisão conforme documentado abaixo. O número máximo de itens que você pode selecionar é limitado pelo número de blocos definido no componente **[!UICONTROL Repetir grade]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Clique em **[!UICONTROL Next]**.

## Configurar uma sequência de estratégia {#strategy}

A seção **[!UICONTROL Sequência de estratégia]** permite selecionar os itens de decisão e configurar estratégias de seleção para apresentar com a política de decisão.

1. Clique em **[!UICONTROL Adicionar]** e escolha o tipo de objeto a ser incluído na política:

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Estratégia de seleção]** - As estratégias de decisão usam coleções associadas a restrições de qualificação e métodos de classificação para determinar os itens a serem mostrados. Você pode selecionar uma ou várias estratégias de seleção existentes ou criar uma nova usando o botão **[!UICONTROL Criar estratégia de seleção]**. [Saiba como criar estratégias de seleção](selection-strategies.md)

   * **[!UICONTROL Item de decisão]** - Selecione itens de decisão únicos sem precisar executar uma estratégia de seleção. Você só pode selecionar um item de decisão por vez. Quaisquer restrições de qualificação definidas para o item serão aplicadas.

   >[!NOTE]
   >
   >Uma política de decisão suporta até 10 estratégias de seleção e itens de decisão combinados. [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)

1. Ao adicionar vários itens e/ou estratégias de decisão, eles serão avaliados em uma ordem específica. O primeiro objeto adicionado à sequência será avaliado primeiro e assim por diante. Para alterar a sequência padrão, arraste e solte os objetos e/ou grupos para reordená-los como desejado. Expanda a seção abaixo para obter mais detalhes.

   +++Gerenciar ordem de avaliação em uma política de decisão

   Depois de adicionar itens de decisão e estratégias de seleção à sua política, você pode organizar a ordem para determinar a ordem de avaliação e combinar estratégias de seleção para avaliá-los juntos.

   A **ordem sequencial** na qual os itens e as estratégias serão avaliados é indicada com números à esquerda de cada objeto ou grupo de objetos. Para mover a posição de uma estratégia de seleção (ou um grupo de estratégias) dentro da sequência, arraste e solte-a em outra posição.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Somente estratégias de seleção podem ser arrastadas e soltas em uma sequência. Para alterar a posição de um item de decisão, é necessário removê-lo e adicioná-lo novamente usando o botão **[!UICONTROL Adicionar]** depois de adicionar os outros itens que você deseja avaliar antes.

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

   **Exemplo com várias estratégias**

   Agora, vamos considerar um exemplo em que você tem várias estratégias divididas em grupos diferentes. Você definiu três estratégias. A Estratégia 1 e a Estratégia 2 são combinadas no Grupo 1 e a Estratégia 3 é independente (Grupo 2). As ofertas elegíveis para cada estratégia e sua prioridade (usada na avaliação da função de classificação) são as seguintes:

   * Grupo 1:
      * Estratégia 1 - (Oferta 1, Oferta 2, Oferta 3) - Prioridade 1
      * Estratégia 2 - (Oferta 3, Oferta 4, Oferta 5) - Prioridade 1

   * Grupo 2:
      * Estratégia 3 - (Oferta 5, Oferta 6) - Prioridade 0

   As ofertas de estratégia de maior prioridade são avaliadas primeiro e adicionadas à lista de ofertas classificadas.

   * **Iteração 1:**

     As ofertas de Estratégia 1 e Estratégia 2 são avaliadas juntas (Oferta 1, Oferta 2, Oferta 3, Oferta 4, Oferta 5). Digamos que o resultado seja:

     Oferta 1 - 10
Oferta 2 - 20
Oferta 3 - 30 da Estratégia 1, 45 da Estratégia 2. O mais alto de ambos será considerado, portanto, 45 é considerado.
Oferta 4 - 40
Oferta 5 - 50

     As ofertas classificadas agora são: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

   * **Iteração 2:**

     As ofertas da Estratégia 3 são avaliadas (Oferta 5, Oferta 6). Digamos que o resultado seja:

      * Oferta 5 - Não será avaliado, pois já existe no resultado acima.
      * Oferta 6 - 60

     As ofertas classificadas agora são as seguintes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

   +++

1. Quando a estratégia de seleção estiver pronta, clique em **[!UICONTROL Avançar]**.

## Adicionar ofertas substitutas {#fallback}

Depois de selecionar itens de decisão e/ou estratégias de seleção, você pode adicionar ofertas substitutas para exibir se nenhum dos itens ou estratégias de seleção acima for qualificado.

Você pode selecionar qualquer item da lista, que exibe todos os itens de decisão criados na sandbox atual. Se nenhuma estratégia de seleção for qualificada, o fallback será exibido para o usuário, independentemente das datas e da restrição de qualificação aplicada ao item selecionado<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Os fallbacks são opcionais. É possível selecionar até o número de itens solicitados. Se nenhum for elegível e nenhum fallback for definido, nada será exibido.

## Revisar e salvar a política de decisão {#review}

Após configurar uma estratégia de seleção e adicionar ofertas substitutas, clique em **[!UICONTROL Avançar]** para revisar e salvar sua política de decisão e em **[!UICONTROL Criar]** para confirmar a criação da política.

>[!IMPORTANT]
>
>Depois que uma política de decisão é criada, as alterações feitas nela podem levar até 15 minutos para se propagarem por todas as regiões de dados e até 30 minutos para o Canadá. Isso inclui alterações como adicionar um novo item de decisão a uma coleção, alterar uma regra em um item, alterar o conteúdo do item ou atualizar uma fórmula.

Você pode editar ou excluir uma política de decisão a qualquer momento usando o botão de reticências no editor de personalização ou no menu **[!UICONTROL Decisão]** no painel de propriedades do componente.

>[!BEGINTABS]

>[!TAB Editar ou excluir uma política do editor de personalização]

![](assets/decision-policy-edit.png)

>[!TAB Editar ou excluir uma política do menu de Decisões]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Atribuir uma inserção (email) {#placement}

Para emails, é necessário definir um posicionamento para o componente associado à política de decisão. Para fazer isso, clique no botão **[!UICONTROL Decisão]** no painel de propriedades do componente e selecione **[!UICONTROL Atribuir posicionamento]**. [Saiba como trabalhar com posicionamentos](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Próximas etapas {#next-steps}

Agora que você entende como criar uma política de decisão, você está pronto para usá-la em [!DNL Journey Optimizer] canais para entregar ofertas.

➡️ [Saiba como usar políticas de decisão em mensagens](../experience-decisioning/use-decision-policy.md)
