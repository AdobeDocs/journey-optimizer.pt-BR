---
title: Criar experiências baseadas em código
description: Saiba como criar experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---

# Criar experiências baseadas em código {#create-code-based}

No [!DNL Journey Optimizer], você pode criar experiências baseadas em código em uma jornada ou campanha.

## Adicionar uma experiência baseada em código por meio de uma jornada ou campanha {#create-code-based-experience}

Para começar a criar sua experiência baseada em código por meio de uma jornada ou campanha, siga as etapas abaixo.

>[!BEGINTABS]

>[!TAB Adicionar uma experiência baseada em código a uma jornada]

Para adicionar uma atividade de **experiência baseada em código** a uma jornada, siga estas etapas:

1. [Criar uma jornada](../building-journeys/journey-gs.md).

1. Inicie sua jornada com uma atividade [Evento](../building-journeys/general-events.md) ou [Ler público](../building-journeys/read-audience.md).

1. Arraste e solte uma atividade de **[!UICONTROL Experiência baseada em código]** da seção **[!UICONTROL Ações]** da paleta.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >Como a **experiência baseada em código** é uma atividade de experiência de entrada, ela vem com uma atividade de **Aguardar** de 3 dias. [Saiba mais](../building-journeys/wait-activity.md#auto-wait-node)

1. Insira um **[!UICONTROL Rótulo]** e uma **[!UICONTROL Descrição]** para a mensagem.

1. Selecione ou crie a configuração de experiência baseada em código para usar. [Saiba mais](code-based-configuration.md)

   ![](assets/code-based-activity-config.png)

   >[!NOTE]
   >
   >Quando você tem várias ações de experiência baseadas em código usando a mesma configuração de canal, a **[!UICONTROL Pontuação de prioridade]** da jornada determina o que é entregue ao usuário final se ele se qualificar para mais de uma ação. [Saiba mais sobre pontuações de prioridade](../conflict-prioritization/priority-scores.md)

1. Selecione o botão **[!UICONTROL Editar conteúdo]** e edite o conteúdo conforme desejado usando o editor de personalização. [Saiba mais](#edit-code)

   Você também pode usar um template de conteúdo existente como base para o conteúdo do código. Observe que os modelos disponíveis para escolha têm como escopo HTML ou JSON com base na configuração de canal escolhida anteriormente. [Saiba como usar modelos de conteúdo](../content-management/use-content-templates.md)

1. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

1. Quando sua experiência com base em código estiver pronta, finalize a configuração e publique sua jornada para ativá-la. [Saiba mais](../building-journeys/publishing-the-journey.md)

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Criar uma campanha de experiência baseada em código]

Para começar a criar sua **experiência baseada em código** por meio de uma campanha, siga as etapas abaixo.

1. Crie uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o tipo de campanha **Agendado - Marketing**.

1. Conclua as etapas para criar uma campanha, como as propriedades da campanha, [público-alvo](../audience/about-audiences.md) e [agendamento](../campaigns/create-campaign.md#schedule). Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. Selecione a ação **[!UICONTROL Experiência baseada em código]**.

1. Selecione ou crie a configuração de experiência baseada em código para usar. [Saiba mais](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

   >[!NOTE]
   >
   >Quando você tem várias ações de experiência baseadas em código usando a mesma configuração de canal, a **[!UICONTROL Pontuação de prioridade]** da campanha determina o que é entregue ao usuário final se ele se qualificar para mais de uma ação. [Saiba mais sobre pontuações de prioridade](../conflict-prioritization/priority-scores.md)

1. Edite o conteúdo conforme desejado usando o editor de personalização. [Saiba mais](#edit-code)

   Você também pode usar um template de conteúdo existente como base para o conteúdo do código. Observe que os modelos disponíveis para escolha têm como escopo HTML ou JSON com base na configuração de canal escolhida anteriormente. [Saiba como usar modelos de conteúdo](../content-management/use-content-templates.md)

   <!--![](assets/code-based-campaign-edit-content.png)-->

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

➡️ [Saiba como criar uma campanha de experiência baseada em código neste vídeo](#video)

>[!ENDTABS]

## Editar o conteúdo do código {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Usar o editor de personalização"
>abstract="Insira e edite o código que deseja entregar como parte desta ação de experiência baseada em código."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/personalization/personalization-build-expressions" text="Trabalhar com o editor de personalização"

Para editar o conteúdo de sua experiência baseada em código, siga as etapas abaixo.

1. Na atividade de jornada ou na tela de edição de campanha, selecione **[!UICONTROL Editar código]**.

   ![](assets/code-based-campaign-edit-code.png)

   >[!NOTE]
   >
   >Se estiver usando um modelo de conteúdo de experiência baseado em código com campos de formulário editáveis predefinidos, você poderá gerenciar o conteúdo desses campos sem abrir o editor de personalização. [Saiba mais](code-based-form-fields.md)

1. O [editor de personalização](../personalization/personalization-build-expressions.md) se abre. É uma interface de criação de experiência não visual que permite criar seu código.

1. Você pode alternar o modo de criação de HTML para JSON e vice-versa.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >Alterar o modo de criação resultará na perda de todo o código atual, portanto, alterne os modos antes de iniciar a criação.

1. Insira o código conforme necessário. Você pode aproveitar o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Você pode adicionar fragmentos de expressão HTML ou JSON, se necessário. [Saiba como](../personalization/use-expression-fragments.md)

   Também é possível salvar parte do conteúdo do código como fragmento. [Saiba como](../content-management/fragments.md#save-as-expression-fragment)

1. Com experiências baseadas em código, é possível usar o recurso Decisão. Selecione o ícone **[!UICONTROL Política de decisão]** na barra esquerda e clique em **[!UICONTROL Adicionar política de decisão]**. [Saiba mais](../experience-decisioning/create-decision.md#add-decision)

   ![](assets/code-based-campaign-create-decision.png)

   <!--![](../experience-decisioning/assets/decision-code-based-create.png)-->

   Na tela jornada ou campaign edition, também é possível adicionar diretamente uma política de decisão sem abrir o editor de personalização. Use o ícone dedicado no painel direito para exibir a seção **[!UICONTROL Decisão]**.

   <!--![](assets/code-based-campaign-show-decisioning.png)-->

   As etapas detalhadas para criar uma política de decisão são apresentadas em [esta seção](../experience-decisioning/create-decision.md#add-decision).

1. Clique em **[!UICONTROL Salvar e fechar]** para confirmar as alterações.

Agora, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma campanha de experiência baseada em código, configurar suas propriedades, testá-la e publicá-la.

>[!VIDEO](https://video.tv.adobe.com/v/3428868/?quality=12&learn=on)
