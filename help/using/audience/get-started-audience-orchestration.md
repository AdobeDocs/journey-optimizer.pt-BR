---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à composição de público-alvo
description: Saiba mais sobre a composição de público-alvo
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 435898d7e806e93ee0154c3da22f6a011fc78175
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 28%

---

# Introdução à composição de público-alvo {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="Criar uma composição"
>abstract="Crie um fluxo de trabalho de composição para combinar públicos-alvo da Adobe Experience Platform em uma tela visual e aproveitar várias atividades (divisão, exclusão...) para criar novos públicos-alvo."

>[!BEGINSHADEBOX]

Estas documentações fornecem informações detalhadas sobre como trabalhar com a composição de público-alvo no Adobe Journey Optimizer. Se você for um cliente somente do Perfil do cliente em tempo real e não estiver usando o Adobe Journey Optimizer, [clique aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=pt-BR){target="_blank"}.

>[!ENDSHADEBOX]

A composição de público-alvo permite criar **fluxos de trabalho de composição**, nos quais você pode combinar públicos-alvo existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (dividir, excluir...) para criar novos públicos-alvo.

Depois de concluído, os **públicos-alvo resultantes** são salvos na Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados nas campanhas e jornadas da Journey Optimizer para clientes-alvo. Saiba como direcionar públicos-alvo no Journey Optimizer
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>O uso de públicos-alvo e atributos da composição de público-alvo está indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.
>
>Os atributos de enriquecimento ainda não estão integrados ao serviço de aplicação de políticas. Portanto, quaisquer rótulos de uso de dados que você aplicar aos atributos de enriquecimento não serão aplicados em campanhas ou jornadas do Journey Optimizer.

A composição de público-alvo é acessível no menu **[!UICONTROL Públicos-alvo]** do Adobe Journey Optimizer:

![](assets/audiences-browse.png)

* A guia **[!UICONTROL Visão geral]** fornece um painel dedicado com métricas principais relacionadas aos dados de público-alvo da sua organização. Para saber mais, consulte [Guia de painéis da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=pt-BR).

* A guia **[!UICONTROL Procurar]** lista todos os públicos-alvo existentes armazenados na Adobe Experience Platform.

* A guia **[!UICONTROL Composições]** permite criar workflows de composição em que é possível combinar e organizar públicos-alvo para criar novos.

## Criar um fluxo de trabalho de composição {#create}

Para criar um fluxo de trabalho de composição, siga estas etapas:

1. Acesse o menu **[!UICONTROL Públicos-alvo]** e selecione **[!UICONTROL Criar público-alvo]**.

1. Selecione **[!UICONTROL Compor Público]**.

   ![](assets/audiences-create.png)

1. A tela de composição é exibida com duas atividades padrão:

   * **[!UICONTROL Público-alvo]**: o ponto inicial da sua composição. Essa atividade permite selecionar um ou vários públicos-alvo como base para o fluxo de trabalho,

   * **[!UICONTROL Salvar]**: a última etapa da sua composição. Essa atividade permite salvar o resultado do fluxo de trabalho em um novo público-alvo.

1. Abra as propriedades de composição para especificar um título e uma descrição.

   Se nenhum título for definido nas propriedades, o rótulo da composição é definido como &quot;Composição&quot;, seguido pela data e hora de criação.

   ![](assets/audiences-properties.png)

1. Configure sua composição adicionando quantas atividades forem necessárias entre as atividades de **[!UICONTROL Público]** e **[!UICONTROL Salvar]**. Para obter mais informações sobre como criar uma composição, consulte a [Documentação de composição de público-alvo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition).

   ![](assets/audiences-publish.png)

1. Quando a composição estiver pronta, clique no botão **[!UICONTROL Publish]** para publicar a composição e salvar os públicos resultantes no Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Você pode publicar até 10 composições em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

   Se ocorrer algum erro durante a publicação, os alertas serão exibidos com informações sobre como resolver o problema.

   ![](assets/audiences-alerts.png)

1. A composição é publicada. Os públicos-alvo resultantes são salvos no Adobe Experience Platform e estão prontos para serem direcionados no Journey Optimizer. [Saiba como direcionar públicos no Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>Os públicos-alvo de **composição de público-alvo** são executados diariamente, portanto, talvez seja necessário aguardar até 24 horas para usá-los no Journey Optimizer. Os atributos enriquecidos nos públicos-alvo de composição do público-alvo estão tão atualizados quanto a última execução de composição, que pode durar até 24 horas no passado.

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
