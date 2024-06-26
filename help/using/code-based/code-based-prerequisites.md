---
title: Proteções e pré-requisitos de experiência baseados em código
description: Para editar aplicativos e páginas da Web usando o recurso baseado em código do Journey Optimizer, siga os pré-requisitos desta página
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 2%

---

# Medidas de proteção e pré-requisitos {#web-prerequisites}

Para poder usar ações de experiência baseadas em código no [!DNL Journey Optimizer] e fornecer carga de conteúdo de código que pode ser usada por seus aplicativos, siga os pré-requisitos abaixo:

* Para adicionar modificações aos seus aplicativos, é necessário ter uma implementação específica. [Saiba mais](#implementation-prerequisites)

* Para que as experiências baseadas em código sejam entregues corretamente, defina as configurações detalhadas do Adobe Experience Platform [aqui](#delivery-prerequisites).

>[!CAUTION]
>
>* O canal de experiência baseado em código não está disponível para organizações que compraram o Adobe **Healthcare Shield** e **Escudo de Proteção e Privacidade** ofertas complementares.
>
>* Você só pode criar experiências baseadas em código no **campanhas**. [Saiba mais](../campaigns/create-campaign.md#configure).

## Pré-requisitos de implementação {#implementation-prerequisites}

A experiência baseada em código é compatível com qualquer tipo de implementação de cliente, conforme mostrado nas opções abaixo. Você pode usar um método de implementação do lado do cliente, do lado do servidor ou híbrido para suas propriedades:

* Somente no lado do cliente - Para adicionar modificações às suas páginas da Web ou aplicativos móveis, é necessário implementar o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} no seu site ou [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} em seus aplicativos móveis.

* Modo híbrido - Você pode usar o [API do servidor Edge Network da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} para solicitar personalização no lado do servidor; a resposta é fornecida ao Adobe Experience Platform Web SDK para renderizar as modificações no lado do cliente. Saiba mais na Adobe Experience Platform [Documentação da API do servidor Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. Você pode obter mais informações sobre o modo híbrido e verificar alguns exemplos de implementação em [esta publicação do blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Lado do servidor - Você pode usar o [API do servidor Edge Network da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} para solicitar personalização no lado do servidor. Sua equipe de desenvolvimento deve lidar com a resposta e renderizar as modificações no lado do cliente na implementação do aplicativo.

Você pode encontrar amostras para cada método de implementação acima em [nesta seção](code-based-implementation-samples.md).

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que as experiências baseadas em código sejam entregues corretamente, as seguintes configurações devem ser definidas:

* No [Coleta de dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem um fluxo de dados definido, como na seção **[!UICONTROL Adobe Experience Platform]** serviço que você tem **[!UICONTROL Adobe Journey Optimizer]** opção ativada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, verifique se você tem uma política de mesclagem com o **[!UICONTROL Política de mesclagem ativa na borda]** opção ativada. Para fazer isso, selecione uma política na **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Políticas de mesclagem]** menu Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Para solucionar problemas de entrega de experiências na Web do Journey Optimizer, você pode usar o **Entrega de borda** exibir em **Adobe Experience Platform Assurance**. Este plug-in permite que você inspecione chamadas de solicitação em detalhes, verifique se as chamadas de borda esperadas ocorrem conforme previsto e examine dados de perfil, incluindo mapas de identidade, associações de segmento e configurações de consentimento. Além disso, você pode revisar as atividades para as quais a solicitação se qualificou e identificar aquelas que não foram qualificadas.

  Usar o **Entrega de borda** O plug-in ajuda você a obter os insights necessários para entender e solucionar problemas de suas implementações de entrada de maneira eficaz.

  [Saiba mais sobre a exibição Entrega de borda](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## Pré-requisitos do experimento de conteúdo {#experiment-prerequisites}

Para habilitar experimentos de conteúdo para o canal baseado em código, você precisa verificar se [conjunto de dados](../data/get-started-datasets.md) usado na implementação do aplicativo [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios de experimento, se você adicionar um conjunto de dados que não está presente no fluxo de dados do aplicativo, os dados do aplicativo não serão exibidos nos relatórios de experimento de conteúdo.

Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo no [nesta seção](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo [!DNL Journey Optimizer] sistema de relatórios e não afeta a coleta ou a assimilação de dados.
