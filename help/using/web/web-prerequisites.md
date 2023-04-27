---
title: Pré-requisitos do canal da Web
description: Para acessar e criar páginas da Web na interface do usuário do Journey Optimizer, siga os pré-requisitos desta página
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 11%

---

# Pré-requisitos do canal da Web {#web-prerequisites}

Para acessar e criar páginas da Web no [!DNL Journey Optimizer] na interface do usuário, siga os pré-requisitos abaixo:

* Para adicionar modificações ao seu site, você precisa ter uma implementação específica. [Saiba mais](#implementation-prerequisites)

* Para acessar o [!DNL Journey Optimizer] web designer, você deve ter uma extensão de navegador Google Chrome específica instalada. [Saiba mais](#visual-authoring-prerequesites)

* Para que a experiência da Web seja entregue corretamente, defina as configurações do Adobe Experience Platform detalhadas [here](#delivery-prerequisites).

## Pré-requisitos da implementação {#implementation-prerequisites}

Atualmente, dois tipos de implementações são compatíveis para permitir a criação e o delivery de campanhas de canais da Web em suas propriedades da Web:

* Somente no lado do cliente - Para adicionar modificações ao seu site, é necessário implementar o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} no seu site.

* Modo híbrido - Você pode usar o [API do Servidor de rede de borda da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=pt-BR){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>No momento, não há suporte para a implementação somente do lado do servidor.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Pré-requisitos de criação visual {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Para abrir, criar e visualizar as páginas da Web de maneira confiável no [!DNL Journey Optimizer] web designer, você deve ter o [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensão do navegador instalada em seu navegador da Web.

>[!CAUTION]
>
>Atualmente, o Google Chrome e o Microsoft Edge são os únicos navegadores compatíveis com a criação de páginas da Web no [!DNL Journey Optimizer].

### Instalar a extensão do Visual Editing Helper {#install-visual-editing-helper}

Para baixar e instalar a extensão do navegador do Visual Editing Helper, siga as etapas abaixo.

1. Abra uma nova guia no navegador (Google Chrome ou Microsoft Edge).

1. Vá para o [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Se estiver usando o Microsoft Edge, selecione **[!UICONTROL Permitir extensões de outros armazenamentos]** no banner superior. Isso permitirá adicionar extensões da Chrome Web Store ao Microsoft Edge.

1. Pesquise e navegue até o [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensão do navegador.

1. Clique em **[!UICONTROL Adicionar ao Chrome]** > **[!UICONTROL Adicionar extensão]**.

   >[!NOTE]
   >
   >Se você estiver usando o Microsoft Edge, isso adicionará a extensão ao Edge mesmo que o botão seja rotulado **[!UICONTROL Adicionar ao Chrome]**.

1. Certifique-se de que a extensão do navegador do Visual Editing Helper está ativada corretamente na barra de ferramentas do seu navegador.

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

O Adobe Experience Cloud Visual Editing Helper agora é ativado automaticamente quando um site é aberto no [!DNL Journey Optimizer] web designer para criação de energia.

A extensão não tem configurações condicionais e trata todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável na [!DNL Journey Optimizer] web designer por um dos seguintes motivos:
>
> * O site tem políticas de segurança estritas.
> * O site está em um iframe.
> * O site de controle de qualidade e/ou preparo do cliente não está disponível para partes externas (o site é interno).


### Solução de problemas do site que não está carregando {#troubleshooting}

Ao usar o Adobe [!DNL Journey Optimizer] web designer, se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale o [Extensão do navegador do Visual Editing Helper](#install-visual-editing-helper).

Se a extensão do navegador do Visual Editing Helper estiver instalada corretamente, mas o site ainda não carregar ou se comportar inesperadamente, uma possível correção é abrir seu site no navegador e aceitar cookies antes de tentar carregá-los no [!DNL Journey Optimizer] web designer.

Em páginas sob autenticação, se a página de logon não carregar ou se, depois de tentar fazer logon, você ainda não estiver conectado:

* Tente fazer logon primeiro em uma nova guia do navegador e navegue até a página desejada, copie o URL e tente abri-lo no [!DNL Journey Optimizer] web designer.

* Se você ainda não conseguir carregar seu site na [!DNL Journey Optimizer] web designer, entre em contato com o Atendimento ao Cliente do Adobe para relatar o problema, certificando-se de especificar o URL com falha.

## Pré-requisitos de delivery {#delivery-prerequisites}

Para que a experiência da Web seja entregue corretamente, as seguintes configurações devem ser definidas:

* No [Coleta de dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem um conjunto de dados definido como no **[!UICONTROL Adobe Experience Platform]** você tem o **[!UICONTROL Segmentação de borda]** e **[!UICONTROL Adobe Journey Optimizer]** opções ativadas.

   Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=pt-BR){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >O **[!UICONTROL Adobe Journey Optimizer]** pode ser ativada somente quando a variável **[!UICONTROL Segmentação de borda]** já está ativada.

* Em [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   Essa política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

<!--
Branded domains for assets

When authoring web experiences, if you add content coming from the [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) library, you  must set up the subdomain that will be used to publish this content. [Learn more](web-delegated-subdomains.md)-->



