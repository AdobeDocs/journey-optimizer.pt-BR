---
title: Pré-requisitos do canal web
description: Para acessar e criar páginas da Web na interface do usuário do Journey Optimizer, siga os pré-requisitos desta página
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 5f261b4c097023557f95831635f2be141dfc5bc8
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 3%

---

# Pré-requisitos e medidas de proteção {#web-prerequisites}

Para acessar e criar páginas da Web na interface do usuário do [!DNL Journey Optimizer], siga os pré-requisitos abaixo:

* Para adicionar modificações ao seu site, você precisa ter uma implementação específica. [Saiba mais](#implementation-prerequisites)

* Para acessar o web designer [!DNL Journey Optimizer], é necessário ter uma extensão específica do navegador Google Chrome instalada. [Saiba mais](#visual-authoring-prerequisites)

* Para que a experiência online seja entregue corretamente, defina as configurações do Adobe Experience Platform detalhadas [aqui](#delivery-prerequisites).

* Para habilitar relatórios para o canal da Web, é necessário garantir que o conjunto de dados usado na sequência de dados de implementação da Web também esteja incluído na configuração de relatórios. [Saiba mais](#experiment-prerequisites)

>[!IMPORTANT]
>
>As campanhas da Web do [!DNL Journey Optimizer] direcionam novos perfis que não foram engajados anteriormente em outros canais. Isso aumenta a contagem total de perfis que podem ser ativados, o que pode ter implicações de custo se o número contratual de perfis que você adquiriu for excedido. As métricas de licença para cada pacote estão listadas na página [Descrição do Produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Você pode verificar o número de perfis ativáveis no [painel de uso de licença](../audience/license-usage.md).
>

## Pré-requisitos de implementação {#implementation-prerequisites}

Há suporte para dois tipos de implementações para habilitar a criação e o delivery de campanhas de canal da Web nas propriedades da Web:

* Somente no lado do cliente - Para adicionar modificações ao seu site, é necessário implementar o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} no seu site.

  >[!NOTE]
  >
  >Verifique se a sua [versão do Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/release-notes){target="_blank"} é 2.16 ou superior.

* Modo híbrido - Você pode usar a [API do servidor de Edge Network da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} para solicitar personalização no lado do servidor; a resposta é fornecida ao SDK da Web da Adobe Experience Platform para renderizar as modificações no lado do cliente. Saiba mais na [documentação de API do Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"} do Adobe Experience Platform. Você pode obter mais informações sobre o modo híbrido e verificar alguns exemplos de implementação em [esta publicação do blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>No momento, a implementação somente do lado do servidor não é compatível com o canal da Web. Se você tiver uma implementação somente do lado do servidor para suas páginas da Web, poderá usar o [Canal de experiência baseado em código](../code-based/get-started-code-based.md).

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Pré-requisitos de criação visual {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Para poder abrir, criar e visualizar suas páginas da Web de maneira confiável no web designer do [!DNL Journey Optimizer], você deve ter a extensão de navegador do [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} instalada em seu navegador da Web.

>[!CAUTION]
>
>O Google Chrome e o Microsoft Edge são os únicos navegadores com suporte para a criação de páginas da Web no [!DNL Journey Optimizer].

### Instalar a extensão Auxiliar de edição visual {#install-visual-editing-helper}

Para baixar e instalar a extensão de navegador Auxiliar de edição visual, siga as etapas abaixo.

1. Abra uma nova guia no navegador (Google Chrome ou Microsoft Edge).

1. Vá para a [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Se você estiver usando o Microsoft Edge, selecione **[!UICONTROL Permitir extensões de outras lojas]** no banner superior. Isso permitirá que você adicione extensões da Chrome Web Store ao Microsoft Edge.

1. Pesquise e navegue até a extensão de navegador [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}.

1. Clique em **[!UICONTROL Adicionar ao Chrome]** > **[!UICONTROL Adicionar Extensão]**.

   >[!NOTE]
   >
   >Se você estiver usando o Microsoft Edge, a extensão será adicionada ao Edge, mesmo que o botão esteja rotulado como **[!UICONTROL Adicionar ao Chrome]**.

1. Verifique se a extensão de navegador Auxiliar de edição visual está ativada corretamente na barra de ferramentas do navegador.

   ![](assets/web-visual-editing-extension-edge.png)

O Auxiliar de Edição Visual do Adobe Experience Cloud agora é habilitado automaticamente quando um site é aberto no [!DNL Journey Optimizer] [web designer](edit-web-content.md#work-with-web-designer) para habilitar a criação.

A extensão não tem configurações condicionais e lida com todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável no web designer [!DNL Journey Optimizer] devido a um dos seguintes motivos:
>
> * O site tem políticas de segurança rigorosas.
> * O site está em um iframe.
> * O site de controle de qualidade ou preparo do cliente não está disponível para o mundo externo (o site é interno).

### Solução de problemas do site que não está carregando {#troubleshooting}

Ao usar o web designer Adobe [!DNL Journey Optimizer], se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale a [extensão de navegador Auxiliar de edição visual](#install-visual-editing-helper).

1. Verifique se a extensão de navegador Auxiliar de edição visual está instalada corretamente.

1. Se o site ainda se comportar inesperadamente, verifique se os cookies de terceiros são permitidos em seu navegador; caso contrário, a página da Web não poderá ser carregada dentro do web designer [!DNL Journey Optimizer].

Para páginas em autenticação, se a página de logon não for carregada ou se, após tentar fazer logon, você ainda não estiver conectado:

1. Tente fazer logon primeiro em uma nova guia do navegador, navegue até a página desejada, copie a URL e tente abri-la no web designer [!DNL Journey Optimizer].

2. Se você ainda não conseguir carregar seu site no web designer do [!DNL Journey Optimizer], entre em contato com o Atendimento ao cliente da Adobe para relatar o problema, certificando-se de especificar a URL com falha.

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que a experiência da Web seja entregue corretamente, as seguintes configurações devem ser definidas:

* Na [Coleção de Dados da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem uma sequência de dados definida, como no serviço **[!UICONTROL Adobe Experience Platform]**, se a opção **[!UICONTROL Adobe Journey Optimizer]** está habilitada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* Em [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, verifique se você tem uma política de mesclagem com a opção **[!UICONTROL Política de mesclagem Ative-On-Edge]** habilitada. Para fazer isso, selecione uma política no menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Mesclar Políticas]**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Essa política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Para solucionar problemas de entrega de experiências na Web do Journey Optimizer, você pode usar a exibição **Edge Delivery** no **Adobe Experience Platform Assurance**. Este plug-in permite que você inspecione chamadas de solicitação em detalhes, verifique se as chamadas de borda esperadas ocorrem conforme previsto e examine dados de perfil, incluindo mapas de identidade, associações de segmento e configurações de consentimento. Além disso, você pode revisar as atividades para as quais a solicitação se qualificou e identificar aquelas que não foram qualificadas.

  O uso do plug-in **Edge Delivery** ajuda a obter os insights necessários para entender e solucionar problemas de implementações de entrada de maneira eficaz.

  [Saiba mais sobre a exibição do Edge Delivery](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery)

## Pré-requisitos de relatórios {#experiment-prerequisites}

Para habilitar relatórios para o canal Web, você precisa verificar se o [conjunto de dados](../data/get-started-datasets.md) usado na sua implementação da Web [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios, se você adicionar um conjunto de dados que não esteja presente no fluxo de dados da Web, os dados da Web não serão exibidos nos relatórios.

Saiba como adicionar conjuntos de dados para relatórios em [esta seção](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo sistema de relatórios [!DNL Journey Optimizer] e não afeta a coleta ou a assimilação de dados.

Se você estiver **não** usando os [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} predefinidos a seguir para o esquema do conjunto de dados: `AEP Web SDK ExperienceEvent` e `Consumer Experience Event` (conforme definido em [esta página](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), adicione os seguintes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` e `Web Details`. Eles são necessários aos relatórios de [!DNL Journey Optimizer], pois estão rastreando em quais campanhas e jornadas cada perfil está participando.

[Saiba mais sobre a configuração de relatórios](../reports/reporting-configuration.md)

>[!NOTE]
>
>A adição desses grupos de campos não afeta a coleta de dados normal. É aditivo apenas para as páginas em que uma campanha ou jornada está em execução, deixando todos os outros rastreamentos intactos.

## Domínios com marca para ativos {#branded-domains-for-assets}

Ao criar experiências na Web, se você adicionar conteúdo proveniente da biblioteca do [Adobe Experience Manager Assets](../content-management/assets.md), será necessário configurar o subdomínio que será usado para publicar esse conteúdo. [Saiba mais](web-delegated-subdomains.md)
