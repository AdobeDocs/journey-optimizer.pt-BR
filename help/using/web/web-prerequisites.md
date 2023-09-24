---
title: Pré-requisitos do canal web
description: Para acessar e criar páginas da Web na interface do usuário do Journey Optimizer, siga os pré-requisitos desta página
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: ec071392cec9933bb73ae9ab20618292b6089061
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 11%

---

# Pré-requisitos e medidas de proteção {#web-prerequisites}

Para acessar e criar páginas da Web na [!DNL Journey Optimizer] siga os pré-requisitos abaixo:

* Para adicionar modificações ao seu site, você precisa ter uma implementação específica. [Saiba mais](#implementation-prerequisites)

* Para acessar o [!DNL Journey Optimizer] web designer, é necessário ter uma extensão específica do navegador Google Chrome instalada. [Saiba mais](#visual-authoring-prerequesites)

* Para que a experiência da Web seja entregue corretamente, defina as configurações detalhadas do Adobe Experience Platform [aqui](#delivery-prerequisites).

## Observações de cuidado {#caution-notes-web}

* Atualmente em [!DNL Journey Optimizer] você só pode criar experiências da web no **campanhas**. [Saiba mais](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] as campanhas da web têm como alvo novos perfis que não foram engajados antes em outros canais. Isso aumentará a contagem total de perfis utilizáveis, o que pode ter implicações de custo se o número contratual de perfis utilizáveis que você adquiriu for excedido. As métricas de licença para cada pacote estão listadas no [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html) página.


>[!AVAILABILITY]
>
>Por enquanto, o canal da Web não está disponível para organizações que compraram a oferta complementar do Adobe Healthcare Shield.
>

## Pré-requisitos de implementação {#implementation-prerequisites}

Atualmente, há dois tipos de implementações compatíveis para habilitar a criação e o delivery de campanhas de canal da Web nas propriedades da Web:

* Somente no lado do cliente - Para adicionar modificações ao seu site, é necessário implementar a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} em seu site.

  >[!NOTE]
  >
  >Verifique se a versão do SDK da Web do AEP é a 2.16 ou superior.

* Modo híbrido - Você pode usar o [API do servidor da rede de borda da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=pt-BR){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>A implementação somente do lado do servidor não é compatível no momento.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Pré-requisitos de criação visual {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Para poder abrir, criar e visualizar suas páginas da Web de maneira confiável na [!DNL Journey Optimizer] web designer, você deve ter o [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensão do navegador instalada no navegador da web.

>[!CAUTION]
>
>O Google Chrome e o Microsoft Edge são, atualmente, os únicos navegadores compatíveis com a criação de páginas da Web no [!DNL Journey Optimizer].

### Instalar a extensão Auxiliar de edição visual {#install-visual-editing-helper}

Para baixar e instalar a extensão de navegador Auxiliar de edição visual, siga as etapas abaixo.

1. Abra uma nova guia no navegador (Google Chrome ou Microsoft Edge).

1. Vá para a [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Se estiver usando o Microsoft Edge, selecione **[!UICONTROL Permitir extensões de outros armazenamentos]** no banner superior. Isso permitirá que você adicione extensões da Chrome Web Store ao Microsoft Edge.

1. Pesquise e navegue até o [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensão do navegador.

1. Clique em **[!UICONTROL Adicionar ao Chrome]** > **[!UICONTROL Adicionar extensão]**.

   >[!NOTE]
   >
   >Se você estiver usando o Microsoft Edge, essa ação adicionará a extensão ao Edge, mesmo que o botão esteja rotulado **[!UICONTROL Adicionar ao Chrome]**.

1. Verifique se a extensão de navegador Auxiliar de edição visual está ativada corretamente na barra de ferramentas do navegador.

   ![](assets/web-visual-editing-extension-edge.png)

O Auxiliar de edição visual do Adobe Experience Cloud agora é ativado automaticamente quando um site é aberto na [!DNL Journey Optimizer] [web designer](edit-web-content.md#work-with-web-designer) para habilitar a criação.

A extensão não tem configurações condicionais e lida com todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável no [!DNL Journey Optimizer] web designer devido a um dos seguintes motivos:
>
> * O site tem políticas de segurança estritas.
> * O site está em um iframe.
> * O site de controle de qualidade e/ou preparo do cliente não está disponível para partes externas (o site é interno).

### Solução de problemas do site que não está carregando {#troubleshooting}

Ao usar o Adobe [!DNL Journey Optimizer] web designer, se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale o [Extensão de navegador Auxiliar de edição visual](#install-visual-editing-helper).

1. Verifique se a extensão de navegador Auxiliar de edição visual está instalada corretamente.

1. Se o site ainda se comportar inesperadamente, verifique se os cookies de terceiros são permitidos em seu navegador; caso contrário, a página da Web não poderá ser carregada dentro do [!DNL Journey Optimizer] web designer.

Para páginas em autenticação, se a página de logon não for carregada ou se, após tentar fazer logon, você ainda não estiver conectado:

1. Tente fazer logon primeiro em uma nova guia do navegador, navegue até a página desejada e copie o URL e tente abri-lo na guia [!DNL Journey Optimizer] web designer.

2. Se você ainda não conseguir carregar seu site na [!DNL Journey Optimizer] web designer, entre em contato com o Atendimento ao cliente da Adobe para relatar o problema, certificando-se de especificar o URL com falha.

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que a experiência da Web seja entregue corretamente, as seguintes configurações devem ser definidas:

* No [Coleta de dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem um fluxo de dados definido, como na seção **[!UICONTROL Adobe Experience Platform]** serviço que você tem **[!UICONTROL Adobe Journey Optimizer]** opção ativada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=pt-BR){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## Pré-requisitos do experimento de conteúdo {#experiment-prerequisites}

Para habilitar experimentos de conteúdo para o canal da Web, verifique se [conjunto de dados](../data/get-started-datasets.md) usado na implementação da Web [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=pt-BR){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios de experimento, se você adicionar um conjunto de dados que não esteja presente no seu fluxo de dados da Web, os dados da Web não serão exibidos nos relatórios de experimento de conteúdo.

Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo no [nesta seção](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo [!DNL Journey Optimizer] sistema de relatórios e não afeta a coleta ou a assimilação de dados.

Se você estiver **não** usando as seguintes opções [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), adicione os seguintes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, e `Web Details`. Estas são necessárias para a [!DNL Journey Optimizer] relatórios de experimento de conteúdo à medida que eles rastream em quais experimentos e tratamentos cada perfil está participando.

>[!NOTE]
>
>A adição desses grupos de campos não afeta a coleta de dados normal. É aditivo apenas para as páginas em que um experimento está sendo executado, deixando todos os outros rastreamentos intactos.

## Domínios com marca para ativos {#branded-domains-for-assets}

Ao criar experiências na Web, se você adicionar conteúdo proveniente da [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) , você deve configurar o subdomínio que será usado para publicar esse conteúdo. [Saiba mais](web-delegated-subdomains.md)
