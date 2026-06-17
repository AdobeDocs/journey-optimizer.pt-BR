---
title: Criar caixa de entrada
description: Saiba como criar e configurar uma Caixa de entrada no Adobe Journey Optimizer para enviar mensagens persistentes e não intrusivas para os usuários.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 7d650278-4a62-4666-b8d7-f0b79ec527ea
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 5%

---

# Criar uma caixa de entrada {#inbox-create}

>[!BEGINSHADEBOX]

**Nesta página:** Crie uma campanha que use a ação Caixa de Entrada, direcione um público e agende ou acione-o, para que você possa entregar mensagens persistentes que os usuários possam revisitar em suas caixas de entrada.

>[!ENDSHADEBOX]

Antes de criar uma caixa de entrada, conclua as etapas da [Configuração da caixa de entrada](inbox-configuration.md). A configuração de canal identifica o aplicativo ou site de destino, a página ou regra e o posicionamento onde a caixa de entrada é renderizada.

Para criar uma caixa de entrada de mensagem por meio de uma campanha, siga estas etapas:

1. Crie uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o tipo de campanha que deseja executar:

   * **[!UICONTROL Agendado - Marketing]**: execute a campanha imediatamente ou em uma data especificada. As campanhas agendadas têm como objetivo enviar mensagens de **marketing**. Eles são configurados e executados na interface do usuário do.

   * **[!UICONTROL Acionado por API - Marketing/Transacional]**: execute a campanha usando uma chamada de API. As campanhas acionadas por API destinam-se ao envio de **mensagens de marketing** ou **mensagens transacionais**, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc. [Saiba como acionar uma campanha usando APIs](../campaigns/api-triggered-campaigns.md)

1. Na guia **[!UICONTROL Propriedades]**, especifique um nome e uma descrição para a campanha.

1. Na guia **[!UICONTROL Ação]**, selecione a ação **[!UICONTROL Caixa de Entrada]**.

   ![](assets/inbox-create-1.png)

1. Selecione ou crie uma nova [configuração da Caixa de Entrada](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Acesse a guia Conteúdo para criar sua mensagem usando o designer de conteúdo. [Saiba mais](inbox-design.md)

1. Na guia **[!UICONTROL Público-alvo]**, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais sobre públicos-alvo](../audience/about-audiences.md).

1. No campo **[!UICONTROL Namespace de identidade]**, escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

1. Você pode agendar sua campanha para uma data específica ou definir para recorrência em intervalos regulares. [Saiba mais](../campaigns/create-campaign.md#schedule)

1. Revise e ative sua campanha para enviar mensagens para a caixa de entrada.

Agora você pode escolher esta Caixa de Entrada ao criar sua [Campanha de cartão de conteúdo](../content-card/create-content-card.md).
