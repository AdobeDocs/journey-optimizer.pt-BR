---
title: Projetar a jornada
description: Saiba como criar sua jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1417'
ht-degree: 2%

---

# Projetar a jornada {#design-your-journey}

A interface de jornada permite arrastar e soltar facilmente as atividades da paleta na tela. Você também pode clicar duas vezes em uma atividade para adicioná-la à tela na próxima etapa disponível. Cada atividade tem uma função e um lugar específicos no processo. As atividades são sequenciadas. Quando uma atividade é concluída, o fluxo continua e processa a próxima atividade e assim por diante.

## Introdução ao design do jornada

O **paleta** está no lado esquerdo da tela. Todas as atividades disponíveis são classificadas em várias categorias: **[!UICONTROL Events]**, **[!UICONTROL Orchestration]** e **[!UICONTROL Actions]**. É possível expandir/recolher as diferentes categorias clicando no nome. Para usar uma atividade na jornada, arraste-a e solte-a da paleta na tela.

Ao iniciar uma nova jornada, os elementos que não podem ser soltos na tela como a primeira etapa são ocultos. Isso se refere a todas as ações, à atividade de condição, à espera e à reação.

![](assets/journey38.png)

O **[!UICONTROL Filter items]** no canto superior esquerdo, é possível exibir os seguintes filtros:

* **Mostrar apenas itens disponíveis**: ocultar ou exibir elementos indisponíveis na paleta, por exemplo, os eventos que usam um namespace diferente daqueles usados na jornada. Por padrão, os itens indisponíveis ficam ocultos. Se você optar por exibi-las, elas aparecerão esmaecidas.

* **Mostrar apenas itens recentes**: esse filtro permite exibir somente os cinco últimos eventos e ações usados, além dos prontos para uso. Isso é específico para cada usuário. Por padrão, todos os itens são exibidos.

Também é possível usar a variável **[!UICONTROL Search]** campo. Somente eventos e ações são filtrados.

O **tela** é a zona central no designer de jornadas. É nessa zona que você pode soltar suas atividades e configurá-las. Clique em uma atividade na tela para configurá-la. Isso abre o painel de configuração da atividade no lado direito.

![](assets/journey39.png)

O **painel de configuração da atividade** é exibida ao clicar em uma atividade na paleta. Preencha os campos obrigatórios. Clique no botão **[!UICONTROL Delete]** ícone para excluir a atividade. Clique em **[!UICONTROL Cancel]** para anular as modificações ou **[!UICONTROL Ok]** para confirmar. Para excluir atividades, você também pode selecionar uma atividade (ou várias) e pressionar a tecla Backspace. Pressionar a tecla escape fechará o painel de configuração da atividade.

Por padrão, os campos somente leitura ficam ocultos. Para mostrar campos somente leitura, clique no botão **Mostrar campos somente leitura** ícone na parte superior esquerda do painel de configuração da atividade. Essa configuração se aplica a todas as atividades em todas as jornadas.

![](assets/journey59bis.png)

Dependendo do status da jornada, você pode executar ações diferentes em sua jornada usando os botões disponíveis no canto superior direito: **[!UICONTROL Publish]**, **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]**, **[!UICONTROL Journey properties]**, **[!UICONTROL Test]**. Esses botões são exibidos quando nenhuma atividade é selecionada. Alguns botões serão exibidos contextualmente. O botão log do modo de teste é exibido quando o modo de teste é ativado.

![](assets/journey41.png)

## Iniciar a jornada

Ao projetar sua jornada, a primeira pergunta que você deseja fazer é como os perfis entrarão na jornada. Há duas possibilidades:

**Começar com um evento**: quando uma jornada é definida para ouvir eventos, os indivíduos entram na jornada **unitaneamente** em tempo real. As mensagens incluídas na sua jornada são enviadas à pessoa que está fluindo atualmente para a jornada. [Saiba mais sobre eventos](../event/about-events.md)

**Começar com um segmento de leitura**: é possível definir a jornada para ouvir os segmentos do Adobe Experience Platform. Nesse caso, todos os indivíduos pertencentes ao segmento especificado entram na jornada. As mensagens incluídas na jornada são enviadas aos indivíduos pertencentes ao segmento. [Saiba mais sobre como ler segmentos](read-segment.md).

## Definir as próximas etapas

Após o primeiro evento ou Ler segmento, é possível combinar as diferentes atividades para criar cenários de vários canais em várias etapas. Escolha, na paleta, as etapas necessárias.

**Eventos**

Quando você inicia a jornada com um evento, a jornada é acionada quando o evento é recebido. A pessoa seguirá, individualmente, as próximas etapas definidas na sua jornada.

Você pode adicionar **vários eventos** na sua jornada, desde que eles usem o mesmo namespace. Os eventos são configurados antecipadamente. [Saiba mais sobre eventos](about-journey-activities.md#event-activities)

Você também pode adicionar uma **Reação** depois de uma mensagem para reagir a dados de rastreamento relacionados à mensagem. Isso permite, por exemplo, enviar outra mensagem se o indivíduo tiver aberto a mensagem anterior ou clicado nela. Saiba mais nesta [seção](reaction-events.md).

O **Qualificação do segmento** A atividade de evento permite que você insira ou avance indivíduos em uma jornada com base nas entradas e saídas do segmento Adobe Experience Platform. Você pode fazer com que todos os novos clientes prateados insiram uma jornada e enviem mensagens personalizadas. Saiba mais nesta [seção](segment-qualification-events.md).

**Orquestração**

Nas atividades de orquestração, você encontrará a variável **Ler segmento** atividade que permite definir a jornada para ouvir um segmento do Adobe Experience Platform. [Saiba mais sobre a atividade Ler segmento](read-segment.md).

As outras atividades permitem adicionar condições à jornada para definir vários caminhos, definir um tempo de espera antes de executar a próxima atividade ou terminar a jornada. Saiba mais nesta [seção](about-journey-activities.md#orchestration-activities).

**Ações**

Você encontrará aqui o **Mensagem** atividade que permite incluir uma mensagem criada em [!DNL Journey Optimizer]. [Saiba mais sobre a atividade de mensagem](journeys-message.md)

Você também encontrará as ações personalizadas que configurou para enviar mensagens com sistemas de terceiros. Saiba mais nesta [seção](about-journey-activities.md#action-activities).

## O uso de caminhos na tela {#paths}

Várias atividades (**[!UICONTROL Condition]**, **[!UICONTROL Action]** atividades do ) permitem definir uma ação de fallback em caso de erro ou tempo limite. No painel de configuração da atividade, marque a caixa : **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Outro caminho é adicionado após a atividade . A duração do tempo limite é definida nas propriedades da jornada (consulte [esta página](../building-journeys/journey-gs.md#change-properties) por um usuário administrador. Por exemplo, se um email demorar muito para ser enviado ou estiver com erro, você pode decidir enviar um SMS.

![](assets/journey42.png)

Várias atividades (evento, ação, espera) permitem adicionar vários caminhos após elas. Para fazer isso, coloque o cursor na atividade e clique no símbolo &quot;+&quot;. Somente atividades de evento e espera podem ser definidas em paralelo. Se vários eventos forem definidos em paralelo, o caminho escolhido será o primeiro evento que ocorrer.

Ao ouvir um evento, recomendamos que você não espere o evento indefinidamente. Não é obrigatório, é apenas uma boa prática. Se quiser ouvir um ou vários eventos somente durante um determinado tempo, você colocará um ou vários eventos e uma atividade de espera em paralelo. Consulte [esta seção](../building-journeys/general-events.md#events-specific-time).

Para excluir o caminho, coloque o cursor nele e clique no botão **[!UICONTROL Delete path]** ícone .

![](assets/journey42ter.png)

Na tela, quando duas atividades são desconectadas, um aviso é exibido. Coloque o cursor no ícone de aviso para exibir a mensagem de erro. Para corrigir o problema, basta mover a atividade desconectada e conectá-la à atividade anterior.

![](assets/canvas-disconnected.png)

## Copiar e colar atividades {#copy-paste}

É possível copiar uma ou várias atividades de uma jornada e colá-las na mesma jornada ou em uma diferente. Isso permite economizar tempo se quiser reutilizar várias atividades que já foram configuradas em uma jornada anterior.

**Observações importantes**

* Você pode copiar/colar em diferentes guias e navegadores. Você só pode copiar/colar atividades na mesma instância.
* Não é possível copiar/colar um evento se a jornada de destino tiver um evento que use um namespace diferente.
* Atividades coladas podem fazer referência a dados que não existem na jornada de destino, por exemplo, se você copiar/colar em diferentes sandboxes. Sempre verifique se há erros e faça os ajustes necessários.
* Esteja ciente de que não é possível desfazer uma ação. Para excluir atividades coladas, é necessário selecioná-las e excluí-las. Portanto, selecione somente as atividades necessárias antes de copiá-las.
* Você pode copiar atividades de qualquer jornada, mesmo as que estão em somente leitura.
* Você pode selecionar qualquer atividade, mesmo aquelas que não estão vinculadas. As atividades vinculadas permanecerão vinculadas após serem coladas.

Estas são as etapas para copiar/colar atividades:

1. Abra uma jornada.
1. Selecione as atividades que deseja copiar movendo o mouse e clicando. Você também pode clicar em cada atividade enquanto pressiona o **Ctrl/Command** chave. Use **Ctrl/Command + A** se desejar selecionar todas as atividades.
   ![](assets/copy-paste1.png)
1. Press **Ctrl/Command + C**.
Se quiser copiar apenas uma atividade, clique nela e use a variável **Copiar** ícone na parte superior esquerda do painel de configuração da atividade.
   ![](assets/copy-paste2.png)
1. Em qualquer jornada, pressione **Ctrl/Command + V** para colar as atividades sem vinculá-las a um nó existente. As atividades coladas são colocadas na mesma ordem. Após serem coladas, as atividades permanecem selecionadas para que você possa movê-las facilmente. Também é possível colocar o cursor em um espaço reservado vazio e pressionar **Ctrl/Command + V**. As atividades coladas serão vinculadas ao nó .
   ![](assets/copy-paste3.png)
