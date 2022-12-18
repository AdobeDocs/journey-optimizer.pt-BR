---
solution: Journey Optimizer
product: journey optimizer
title: Projetar a jornada
description: Saiba como criar sua jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 3%

---

# Projetar a jornada {#design-your-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Projetar a jornada"
>abstract="A interface de jornada permite arrastar e soltar facilmente as atividades da paleta na tela. Você também pode clicar duas vezes em uma atividade para adicioná-la à tela na próxima etapa disponível."

O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite que os profissionais de marketing harmonizem o alcance de marketing com o envolvimento de um para um cliente. A interface do usuário permite arrastar e soltar facilmente as atividades da paleta na tela para criar a jornada. Observe que também é possível clicar duas vezes em uma atividade para adicioná-la à tela, na próxima etapa disponível.

Os eventos, as atividades de orquestração e ação têm uma função e um lugar específicos no processo. As atividades são sequenciadas: quando uma atividade é concluída, o fluxo continua e processa a próxima atividade e assim por diante.

## Introdução ao design do jornada {#gs-journey-design}

O **paleta** está no lado esquerdo da tela. Todas as atividades disponíveis são classificadas em várias categorias: [Eventos](#jo-event), [Orquestração](#jo-orch) e [Ações](#jo-actions). É possível expandir/recolher as diferentes categorias clicando no nome. Para usar uma atividade na jornada, arraste-a e solte-a da paleta na tela.

Ao iniciar uma nova jornada, os elementos que não podem ser soltos na tela como a primeira etapa são ocultos. Isso se refere a todas as ações, à atividade de condição, espera e reação.

![](assets/journey38.png)

O **[!UICONTROL Filtrar itens]** no canto superior esquerdo, é possível exibir os seguintes filtros:

* **Mostrar apenas itens disponíveis**: ocultar ou exibir elementos indisponíveis na paleta, por exemplo, os eventos que usam um namespace diferente daqueles usados na jornada. Por padrão, os itens indisponíveis ficam ocultos. Se você optar por exibi-las, elas aparecerão esmaecidas.

* **Mostrar apenas itens recentes**: esse filtro permite exibir somente os cinco últimos eventos e ações usados, além dos prontos para uso. Isso é específico para cada usuário. Por padrão, todos os itens são exibidos.

Também é possível usar a variável **[!UICONTROL Pesquisar]** campo. Somente eventos e ações são filtrados.

O **tela** é a zona central no designer de jornadas. É nessa zona que você pode soltar suas atividades e configurá-las. Clique em uma atividade na tela para configurá-la. Isso abre o painel de configuração da atividade no lado direito.

![](assets/journey39.png)

O **painel de configuração da atividade** é exibida ao clicar em uma atividade na paleta. Preencha os campos obrigatórios. Clique no botão **[!UICONTROL Excluir]** ícone para excluir a atividade. Clique em **[!UICONTROL Cancelar]** para anular as modificações ou **[!UICONTROL Ok]** para confirmar. Para excluir atividades, você também pode selecionar uma atividade (ou várias) e pressionar a tecla Backspace. Pressionar a tecla escape fechará o painel de configuração da atividade.

Por padrão, os campos somente leitura ficam ocultos. Para mostrar campos somente leitura, clique no botão **Mostrar campos somente leitura** ícone na parte superior esquerda do painel de configuração da atividade. Essa configuração se aplica a todas as atividades em todas as jornadas.

![](assets/journey59bis.png)

Dependendo do status da jornada, você pode executar ações diferentes em sua jornada usando os botões disponíveis no canto superior direito: **[!UICONTROL Publicar]**, **[!UICONTROL Duplicar]**, **[!UICONTROL Excluir]**, **[!UICONTROL Propriedades da jornada]**, **[!UICONTROL Teste]**. Esses botões são exibidos quando nenhuma atividade é selecionada. Alguns botões serão exibidos contextualmente. O botão log do modo de teste é exibido quando o modo de teste é ativado.

![](assets/journey41.png)

## Inicie a jornada {#start-your-journey}

Ao projetar sua jornada, a primeira pergunta que você deseja fazer é como os perfis entrarão na jornada. Há duas possibilidades:

1. **Começar com um evento**: quando uma jornada é definida para ouvir eventos, os indivíduos entram na jornada **unitaneamente** em tempo real. As mensagens incluídas na sua jornada são enviadas à pessoa que está fluindo atualmente para a jornada. [Saiba mais sobre eventos](../event/about-events.md)

1. **Começar com um segmento de leitura**: é possível definir a jornada para ouvir os segmentos do Adobe Experience Platform. Nesse caso, todos os indivíduos pertencentes ao segmento especificado entram na jornada. As mensagens incluídas na jornada são enviadas aos indivíduos pertencentes ao segmento. [Saiba mais sobre como ler segmentos](read-segment.md).

## Definir as próximas etapas{#define-next-steps}

Após o primeiro evento ou Ler segmento, é possível combinar as diferentes atividades para criar cenários de vários canais em várias etapas. Escolha, na paleta, as etapas necessárias.

### Eventos{#jo-event}

Eventos são o que aciona uma jornada personalizada, como uma compra online. Uma vez que alguém entra em uma jornada, eles se movem como um indivíduo, e nenhum dos dois indivíduos se movem ao mesmo ritmo ou ao longo do mesmo caminho.

Quando você inicia a jornada com um evento, a jornada é acionada quando o evento é recebido. Cada pessoa na jornada segue, individualmente, as próximas etapas definidas na jornada.

Você pode adicionar **vários eventos** na sua jornada, desde que eles usem o mesmo namespace. Os eventos são configurados antecipadamente. [Saiba mais sobre eventos do jornada](about-journey-activities.md#event-activities)

Você também pode adicionar uma **Reação** depois de uma mensagem para reagir a dados de rastreamento relacionados à mensagem. Isso permite, por exemplo, enviar outra mensagem se o indivíduo tiver aberto a mensagem anterior ou clicado nela. [Saiba mais sobre eventos de reação](reaction-events.md).

Use **Qualificação do segmento** atividade de evento para fazer indivíduos entrarem ou avançarem em uma jornada com base nas entradas e saídas do segmento do Adobe Experience Platform. Você pode fazer com que todos os novos clientes prateados insiram uma jornada e enviem mensagens personalizadas. Saiba mais nesta [seção](segment-qualification-events.md).

### Orquestração{#jo-orch}

As atividades de orquestração são condições diferentes que ajudam a determinar a próxima etapa na jornada.

Nas atividades de orquestração, use a variável **Ler segmento** para definir sua jornada para ouvir um segmento do Adobe Experience Platform. [Saiba mais sobre a atividade Ler segmento](read-segment.md).

As outras atividades permitem adicionar condições à jornada para definir vários caminhos, definir um tempo de espera antes de executar a próxima atividade ou terminar a jornada. [Saiba mais sobre atividades de orquestração](about-journey-activities.md#orchestration-activities).

### Ações{#jo-actions}

As ações são o que você deseja que ocorra como resultado de algum tipo de acionador, como enviar uma mensagem. É a jornada que o cliente experimenta. Pode ser um email, SMS ou mensagem de push ou uma ação de terceiros, como uma mensagem de Slack.

As atividades de ação de canal permitem incluir uma mensagem criada em [!DNL Journey Optimizer]. [Saiba mais sobre as atividades de ação de canal](journeys-message.md)

Nas atividades de ação, use ações personalizadas para enviar mensagens com sistemas de terceiros. [Saiba mais sobre Ações personalizadas](about-journey-activities.md#action-activities).

## Adicionar caminhos alternativos{#paths}

Você pode definir uma ação de fallback em caso de erro ou tempo limite para as seguintes atividades de jornada: **[!UICONTROL Condição]** e **[!UICONTROL Ação]**.

Para adicionar uma ação de fallback a uma atividade, selecione a **[!UICONTROL Adicione um caminho alternativo em caso de tempo limite ou erro]** nas propriedades da atividade: outro caminho é adicionado após a atividade . A duração do tempo limite é definida pelos usuários administradores na variável [Propriedades da jornada](../building-journeys/journey-gs.md#change-properties). Por exemplo, se um email demorar muito para ser enviado ou estiver com erro, você pode decidir enviar uma notificação por push.

![](assets/journey42.png)

Várias atividades (evento, ação, espera) permitem adicionar vários caminhos após elas. Para fazer isso, coloque o cursor na atividade e clique no símbolo &quot;+&quot;. Somente atividades de evento e espera podem ser definidas em paralelo. Se vários eventos forem definidos em paralelo, o caminho escolhido será o primeiro evento que ocorrer.

Ao ouvir um evento, recomendamos que você não espere o evento indefinidamente. Não é obrigatório, é apenas uma boa prática. Se quiser ouvir um ou vários eventos somente durante um determinado tempo, você colocará um ou vários eventos e uma atividade de espera em paralelo. Consulte [esta seção](../building-journeys/general-events.md#events-specific-time).

Para excluir o caminho, coloque o cursor nele e clique no botão **[!UICONTROL Excluir caminho]** ícone .

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
