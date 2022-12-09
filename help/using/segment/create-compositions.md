---
solution: Journey Optimizer
product: journey optimizer
title: Criar workflows de composição
description: Saiba como criar fluxos de trabalho de composição para combinar e organizar públicos existentes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Criar workflows de composição {#create-compositions}

Os fluxos de trabalho de composição permitem combinar e organizar os públicos-alvo existentes para criar novos públicos-alvo.

## Criar um fluxo de trabalho de composição {#create}

1. Acesse o **[!UICONTROL Segments]** e selecione **[!UICONTROL Create Audience]**.

1. Selecionar **[!UICONTROL Compose Audience]**.

   >[!NOTE]
   >
   >O **[!UICONTROL Build rule]** o método de criação permite criar uma nova definição de segmento usando o [Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. A tela de composição é exibida com duas atividades padrão:

   * **[!UICONTROL Audience]**: o ponto de partida da sua composição. Essa atividade permite selecionar um ou vários públicos-alvo como base para o fluxo de trabalho,

   * **[!UICONTROL Save]**: o último passo da sua composição. Essa atividade permite salvar o resultado do fluxo de trabalho em um novo público-alvo.
   Para obter mais informações sobre como configurar atividades na tela de fluxo de trabalho de composição, consulte [Trabalhar com a tela de composição](composition-canvas.md).

1. Abra as propriedades da composição para especificar um título e uma descrição.

   Se nenhum título estiver definido nas propriedades, o rótulo da composição será o do início **[!UICONTROL Audience]** atividade .

   ![](assets/audiences-properties.png)

1. Configure sua composição adicionando quantas atividades forem necessárias entre as **[!UICONTROL Audience]** e **[!UICONTROL Save]** atividades. [Saiba como trabalhar com a tela de composição](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Quando a composição estiver pronta, clique no botão **[!UICONTROL Publish]** para publicar a composição e salvar os públicos resultantes na Adobe Experience Platform.

   Se ocorrer algum erro durante a publicação, serão exibidos alertas com informações sobre como resolver o problema.

   ![](assets/audiences-alerts.png)

1. A composição é publicada. Os públicos-alvo resultantes são salvos na Adobe Experience Platform e estão prontos para serem direcionados em campanhas do Journey Otimizer. [Saiba como trabalhar com campanhas](../campaigns/get-started-with-campaigns.md)

## Composições de acesso {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar seu público-alvo"
>abstract="Publique sua composição para salvar os públicos-alvo resultantes na Adobe Experience Platform."

Todas as composições criadas podem ser acessadas na **[!UICONTROL Compositions]** guia . Eles podem ter vários status:

* **[!UICONTROL Draft]**: a composição está em curso e não foi publicada.
* **[!UICONTROL Published]**: a composição foi publicada, os públicos-alvo resultantes foram salvos e estão disponíveis para uso.
* **[!UICONTROL Archived]**: a composição foi arquivada.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>É possível duplicar ou excluir uma composição existente a qualquer momento usando o botão de elipse na lista.

Saiba mais:

* [Introdução à composição do público-alvo](get-started-audience-orchestration.md)
* [Trabalhar com a tela de composição](composition-canvas.md)
* [Acessar e gerenciar públicos](access-audiences.md)
