---
solution: Journey Optimizer
product: journey optimizer
title: Criar seu primeiro fluxo de trabalho de composição
description: Saiba como criar workflows de composição para combinar e organizar públicos existentes.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 16%

---

# Criar seu primeiro fluxo de trabalho de composição {#create-compositions}

>[!BEGINSHADEBOX]

Estas documentações fornecem informações detalhadas sobre como trabalhar com a composição de público-alvo no Adobe Journey Optimizer. Se você não estiver usando o Adobe Journey Optimizer, [clique aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=pt-BR){target="_blank"}.

>[!ENDSHADEBOX]

## Criar um fluxo de trabalho de composição {#create}

Para criar um fluxo de trabalho de composição, siga estas etapas:

1. Acesse o menu **[!UICONTROL Públicos-alvo]** e selecione **[!UICONTROL Criar público-alvo]**.

1. Selecione **[!UICONTROL Compor Público]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >O método de criação da **[!UICONTROL regra de compilação]** permite criar uma nova definição de segmento usando o [Serviço de Segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=pt-BR).

1. A tela de composição é exibida com duas atividades padrão:

   * **[!UICONTROL Público-alvo]**: o ponto inicial da sua composição. Essa atividade permite selecionar um ou vários públicos-alvo como base para o fluxo de trabalho,

   * **[!UICONTROL Salvar]**: a última etapa da sua composição. Essa atividade permite salvar o resultado do fluxo de trabalho em um novo público-alvo.

   Para obter mais informações sobre como configurar atividades na tela de fluxo de trabalho de composição, consulte [Trabalhar com a tela de composição](composition-canvas.md).

1. Abra as propriedades de composição para especificar um título e uma descrição.

   Se nenhum título for definido nas propriedades, o rótulo da composição é definido como &quot;Composição&quot;, seguido pela data e hora de criação.

   ![](assets/audiences-properties.png)

1. Configure sua composição adicionando quantas atividades forem necessárias entre as atividades de **[!UICONTROL Público]** e **[!UICONTROL Salvar]**. [Saiba como trabalhar com a tela de composição](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Quando a composição estiver pronta, clique no botão **[!UICONTROL Publish]** para publicar a composição e salvar os públicos resultantes no Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Você pode publicar até 10 composições em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

   Se ocorrer algum erro durante a publicação, os alertas serão exibidos com informações sobre como resolver o problema.

   ![](assets/audiences-alerts.png)

1. A composição é publicada. Os públicos-alvo resultantes são salvos no Adobe Experience Platform e estão prontos para serem direcionados no Journey Optimizer. [Saiba como direcionar públicos no Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

## Acessar composições {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar o público"
>abstract="Publique a composição para salvar os públicos resultantes na Adobe Experience Platform."

Todas as composições criadas podem ser acessadas na guia **[!UICONTROL Composições]**. É possível duplicar ou excluir uma composição existente a qualquer momento usando o botão de reticências na lista.

As composições podem ter vários status:

* **[!UICONTROL Rascunho]**: a composição está em andamento e não foi publicada.
* **[!UICONTROL Publicado]**: a composição foi publicada, os públicos resultantes foram salvos e estão disponíveis para uso.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>No momento, a composição de público-alvo não está integrada ao recurso de redefinição da sandbox. Antes de iniciar uma redefinição de sandbox, é necessário excluir as composições manualmente para garantir que os dados do público-alvo associado sejam limpos corretamente. Informações detalhadas estão disponíveis na [Documentação de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions) do Adobe Experience Platform
