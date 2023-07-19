---
solution: Journey Optimizer
product: journey optimizer
title: Criar seu primeiro fluxo de trabalho de composição
description: Saiba como criar workflows de composição para combinar e organizar públicos existentes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: f924af0e1baadabb97167f42457b1b419256fa8c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 7%

---

# Criar seu primeiro fluxo de trabalho de composição {#create-compositions}

>[!BEGINSHADEBOX]

Estas documentações fornecem informações detalhadas sobre como trabalhar com a composição de público-alvo no Adobe Journey Optimizer. Se você não estiver usando o Adobe Journey Optimizer, [clique aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html)

>[!ENDSHADEBOX]

## Criar um fluxo de trabalho de composição {#create}

Para criar um fluxo de trabalho de composição, siga estas etapas:

1. Acesse o **[!UICONTROL Públicos-alvo]** e selecione **[!UICONTROL Criar público-alvo]**.

1. Selecionar **[!UICONTROL Compor público]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >A variável **[!UICONTROL Criar regra]** método de criação permite criar uma nova definição de segmento usando o método [Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. A tela de composição é exibida com duas atividades padrão:

   * **[!UICONTROL Público]**: o ponto inicial da sua composição. Essa atividade permite selecionar um ou vários públicos-alvo como base para o fluxo de trabalho,

   * **[!UICONTROL Salvar]**: a última etapa da sua composição. Essa atividade permite salvar o resultado do fluxo de trabalho em um novo público-alvo.

   Para obter mais informações sobre como configurar atividades na tela de workflow de composição, consulte [Trabalhar com a tela de composição](composition-canvas.md).

1. Abra as propriedades de composição para especificar um título e uma descrição.

   Se nenhum título for definido nas propriedades, o rótulo da composição é definido como &quot;Composição&quot;, seguido pela data e hora de criação.

   ![](assets/audiences-properties.png)

1. Configure sua composição adicionando quantas atividades forem necessárias entre as **[!UICONTROL Público]** e **[!UICONTROL Salvar]** atividades. [Saiba como trabalhar com a tela de composição](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Quando a composição estiver pronta, clique no link **[!UICONTROL Publish]** botão para publicar a composição e salvar os públicos resultantes no Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Você pode publicar até 10 composições em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

   Se ocorrer algum erro durante a publicação, os alertas serão exibidos com informações sobre como resolver o problema.

   ![](assets/audiences-alerts.png)

1. A composição é publicada. Os públicos-alvo resultantes são salvos no Adobe Experience Platform e estão prontos para serem direcionados em campanhas do Journey Optimizer. [Saiba como trabalhar com campanhas](../campaigns/get-started-with-campaigns.md)

## Acessar composições {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar o público"
>abstract="Publique a composição para salvar os públicos resultantes na Adobe Experience Platform."

Todas as composições criadas podem ser acessadas no **[!UICONTROL Composições]** guia. Eles podem ter vários status:

* **[!UICONTROL Rascunho]**: a composição está em andamento e não foi publicada.
* **[!UICONTROL Publicado]**: a composição foi publicada, os públicos resultantes foram salvos e estão disponíveis para uso.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>É possível duplicar ou excluir uma composição existente a qualquer momento usando o botão de reticências na lista.
