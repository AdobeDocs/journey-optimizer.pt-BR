---
title: Testar experiências baseadas em código
description: Saiba como testar experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 9a1c148c-a6c3-406b-8f2e-1cf8b8239e75
source-git-commit: c402a8ab41eb588eae47463fd0217693853d8ca7
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 25%

---

# Testar experiências baseadas em código {#test-code-based}

## Visualize sua experiência baseada em código {#preview-code-based}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Visualize sua experiência baseada em código"
>abstract="Acesse uma simulação de como será a sua experiência baseada em código."

Para exibir uma pré-visualização de sua experiência baseada em código modificada, siga as etapas abaixo.

>[!CAUTION]
>
>Você deve ter perfis de teste disponíveis para simular quais ofertas serão entregues a eles. Saiba como [criar perfis de teste](../audience/creating-test-profiles.md).

1. Na jornada ou campanha, na tela do editor de personalização ou de edição de conteúdo, selecione **[!UICONTROL Simular conteúdo]**.

   ![](assets/code-based-campaign-simulate.png)

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para selecionar um ou mais perfis de teste.

1. Uma visualização da sua experiência modificada baseada em código é exibida.

Informações detalhadas sobre como selecionar perfis de teste e visualizar seu conteúdo estão disponíveis em [esta seção](../content-management/preview.md).

## Visualização no dispositivo {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="Visualizar a experiência baseada em código em um dispositivo real"
>abstract="Obtenha uma visualização de suas experiências personalizadas diretamente no seu navegador ou em seus dispositivos móveis para ver como elas ficam em dispositivos reais."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="Visualizar a experiência da Web com base em código no dispositivo"
>abstract="Digitalize o código QR ou copie o link para visualizar no dispositivo."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="Visualizar a experiência móvel baseada em código no dispositivo"
>abstract="Digitalize o código QR ou copie o link para visualizar no dispositivo. Depois de conectado, insira o pin no dispositivo. Talvez seja necessário reiniciar o aplicativo para ver as alterações toda vez que atualizar os links de visualização."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="Atualizar o link de visualização para refletir a exibição atual"
>abstract="A visualização no dispositivo mostrará o conteúdo a partir de quando você criou ou atualizou o link de visualização. Se você modificou o conteúdo ou selecionou um perfil de teste ou tratamento diferente, atualize a visualização para que ela reflita a exibição atual."

Ao criar experiências baseadas em código para páginas da Web ou aplicativos móveis, você pode visualizar suas experiências personalizadas diretamente do seu navegador ou de seus dispositivos móveis, para ver como essas experiências são exibidas em dispositivos reais.

>[!WARNING]
>
>A visualização no dispositivo não está disponível ao usar [políticas de decisão](../experience-decisioning/create-decision.md) ou [personalização](../personalization/personalization-build-expressions.md) atributos contextuais.

1. Na tela **[!UICONTROL Simular]**, clique no botão **[!UICONTROL Abrir opções de visualização]**. As opções de visualização dependem da plataforma selecionada na sua [configuração baseada em código](code-based-configuration.md#create-code-based-configuration).

1. Se você estiver usando uma [plataforma da Web](code-based-configuration.md#web) em sua configuração baseada em código, o campo somente leitura da **[!UICONTROL URL de visualização do dispositivo]** será preenchido com a URL inserida para a configuração de canal atual.

   ![](assets/preview-on-device-web.png)

   É possível:

   * Selecione o botão **[!UICONTROL Copiar link]** e cole o link em uma guia do navegador. Você também pode compartilhar o link com sua equipe e as partes interessadas, que podem visualizar a nova experiência em qualquer navegador antes que as alterações entrem em vigor.

   * Clique em **[!UICONTROL Abrir em nova guia]** para abrir o link em seu navegador atual.

   * Digitalize o código QR com seu dispositivo móvel para abrir o link de visualização em um navegador móvel.

1. Se você estiver usando [Plataformas móveis](code-based-configuration.md#mobile) (iOS/Android) em sua configuração baseada em código, o campo somente leitura **[!UICONTROL Deeplink]** será preenchido automaticamente com o valor **[!UICONTROL Visualizar URL]** inserido na configuração de canal para a plataforma selecionada.

   Alterne entre as guias **[!UICONTROL iOS]** e **[!DNL Android]** para visualizar sua experiência para a plataforma de sua escolha.

   ![](assets/preview-on-device-mobile.png)

   É possível:

   * Selecione o botão **[!UICONTROL Copiar link]** e compartilhe o link com a equipe e as partes interessadas, que podem visualizar a nova experiência em qualquer navegador móvel antes que as alterações entrem em vigor.

   * Digitalize o código QR com seu dispositivo móvel para abrir o link de visualização diretamente no aplicativo móvel. Insira o PIN no dispositivo para estabelecer a sessão [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}.

     >[!NOTE]
     >
     >O **Adobe Experience Platform Assurance** é um produto da Adobe Experience Cloud que ajuda a inspecionar, testar, simular e validar a maneira como você coleta dados ou oferece experiências em seu aplicativo móvel. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/home){target="_blank"}

1. Se você estiver usando qualquer [outra plataforma](code-based-configuration.md#other) em sua configuração baseada em código, escolha o [URI da superfície](code-based-surface.md#surface-uri) que deseja visualizar na lista suspensa.

   ![](assets/preview-on-device-other.png)

   * Selecione o botão **[!UICONTROL Copiar link]** para colar o link em uma guia do navegador ou compartilhar o link com a equipe e as partes interessadas.

   * Se você adicionou vários URIs à sua configuração (até 10), é possível selecionar qualquer um deles para visualização.

1. Os links de visualização são gerados para o perfil de teste selecionado e, se estiver usando o [Experimento de Conteúdo](../content-management/content-experiment.md) na sua jornada ou campanha, para o tratamento selecionado.

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   Ao atualizar o conteúdo ou selecionar um perfil de teste ou tratamento diferente, o link de visualização é atualizado automaticamente. Você pode copiar o link em diferentes guias do navegador e comparar as experiências.
