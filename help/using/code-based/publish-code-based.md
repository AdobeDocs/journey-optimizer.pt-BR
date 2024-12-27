---
title: Publish e gerenciar experiências baseadas em código
description: Saiba como publicar e parar experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: a1daf6f7-c26c-4d70-984b-0b4eeb04a1a8
source-git-commit: f247ef3c3cd7d1d270893ae6bf88fadf3932d05e
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# Gerenciar experiências baseadas em código {#publish-code-based}

## Ative sua experiência baseada em código {#code-based-experience-live}

>[!IMPORTANT]
>
> Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para ativar suas experiências baseadas em código. [Saiba mais](../test-approve/gs-approval.md)

Depois de definir sua experiência baseada em código e editar seu conteúdo conforme desejado usando o [editor baseado em código](create-code-based.md#edit-code), você pode ativar sua jornada ou campanha para tornar as alterações visíveis para o público-alvo.

Você também pode visualizar seu conteúdo de experiência baseado em código antes de ativá-lo. [Saiba mais](test-code-based.md)

>[!NOTE]
>
>Se você ativar uma jornada/campanha baseada em código e afetar as mesmas páginas que outra jornada ou campanha que já está ativa, todas as alterações serão aplicadas ao conteúdo.
>
>Se várias jornadas ou campanhas baseadas em código atualizarem os mesmos elementos do conteúdo, a jornada/campanha de prioridade mais alta terá prioridade.

Assim que a jornada ou campanha baseada em código estiver ativa, a equipe de implementação do aplicativo será responsável por fazer chamadas explícitas à API ou ao SDK para buscar conteúdo para as superfícies definidas na [configuração de experiência baseada em código](code-based-configuration.md) selecionada. Saiba mais sobre as diferentes implementações de clientes em [esta seção](code-based-implementation-samples.md).

### Publish uma jornada baseada em código {#publish-code-based-journey}

Para ativar sua experiência baseada em código a partir de uma jornada, siga as etapas abaixo.

1. Verifique se a jornada é válida e se não há erros. [Saiba mais](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. Na jornada, selecione a opção **[!UICONTROL Publish]**, localizada no menu suspenso no canto superior direito.

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >Saiba mais sobre a publicação de jornadas em [esta seção](../building-journeys/publishing-the-journey.md).

Sua jornada baseada em código pega o status do **[!UICONTROL Live]** e agora está visível para o público selecionado. Cada recipient da jornada pode ver suas modificações.

>[!NOTE]
>
>Após clicar em **[!UICONTROL Publish]**, pode levar até 15 minutos para que as alterações fiquem disponíveis online.

### Ativar uma campanha baseada em código {#activate-code-based-campaign}

1. Em sua campanha baseada em código, selecione **[!UICONTROL Revisar para ativar]**.

   ![](assets/code-based-campaign-review.png)

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a configuração, o público-alvo e o agendamento.

1. Selecione **[!UICONTROL Ativar]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Saiba mais sobre como ativar campanhas em [esta seção](../campaigns/review-activate-campaign.md).

Sua campanha baseada em código pega o status do **[!UICONTROL Live]** e agora está visível para o público selecionado. Cada recipient da campanha pode ver as modificações que você adicionou ao conteúdo.

>[!NOTE]
>
>Após clicar em **[!UICONTROL Ativar]**, pode levar até 15 minutos para que as alterações fiquem disponíveis ao vivo.
>
>Se você definiu um agendamento para sua campanha baseada em código, ele tem o status **[!UICONTROL Agendado]** até que a data e a hora de início sejam atingidas.

## Interromper uma jornada ou campanha baseada em código {#stop-code-based-experience}

Quando uma experiência baseada em código está ativa, você pode interrompê-la para impedir que o público-alvo veja suas modificações. Siga as etapas abaixo.

1. Selecione uma jornada ou campanha ao vivo na respectiva lista.

1. Execute a ação relevante de acordo com seu caso:

   * No menu superior da campanha, selecione **[!UICONTROL Parar campanha]**.

     ![](assets/code-based-campaign-stop.png)

   * No menu superior de jornada, clique no botão **[!UICONTROL Mais]** e selecione **[!UICONTROL Parar]**.

     ![](assets/code-based-journey-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma jornada ou campanha baseada em código é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a jornada/campanha duplicada.

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report-cja.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

-->
