---
title: Pré-requisitos da experiência baseada em código
description: Para editar aplicativos e páginas da Web usando o recurso baseado em código do Journey Optimizer, siga os pré-requisitos desta página
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
TQID: https://experienceleague.adobe.com/BeT89I19rYUhWyUl65EkUNrtGgw08ErvJGwIiGzcUCg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2:
  - id: f88eedcc-cf3e-46b8-9e94-0293589325f3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: ffb7556c4fef469982c3216fa0fcab2efaec862d
workflow-type: tm+mt
source-wordcount: 832
ht-degree: 10%

---

# Pré-requisitos da experiência baseada em código {#code-based-prerequisites}

>[!BEGINSHADEBOX]

**Nesta página:** Examine os pré-requisitos de implementação, entrega e relatórios necessários para fornecer experiências baseadas em código aos seus aplicativos e páginas da Web.

>[!ENDSHADEBOX]

Para poder usar ações de experiência baseadas em código no [!DNL Journey Optimizer] e fornecer carga de conteúdo de código que pode ser usada por seus aplicativos, siga os pré-requisitos abaixo:

* Para adicionar modificações aos seus aplicativos, é necessário ter uma implementação específica. [Saiba mais](#implementation-prerequisites)

* Para que as experiências baseadas em código sejam entregues corretamente, defina as configurações do Adobe Experience Platform detalhadas [aqui](#delivery-prerequisites).

* Para habilitar a exibição de dados em seus relatórios de experiência baseados em código, siga estes [pré-requisitos de relatórios](#reporting-prerequisites).

* Ao criar uma [configuração de canal de experiência baseada em código](code-based-configuration.md), insira uma cadeia de caracteres/caminho ou um URI de superfície que corresponda àquele declarado em sua própria implementação. Isso garante que o conteúdo seja entregue no local desejado dentro do aplicativo ou página especificada. Caso contrário, as alterações não poderão ser entregues. [Leia mais](code-based-surface.md)

>[!CAUTION]
>
>Ao direcionar perfis pseudônimos (visitantes não autenticados) com suas experiências baseadas em código, considere definir um Tempo de vida (TTL) para exclusão automática de perfil para gerenciar a contagem de perfis ativáveis e os custos associados. [Saiba mais](../start/guardrails.md#profile-management-inbound)

## Pré-requisitos de implementação {#implementation-prerequisites}

A experiência baseada em código é compatível com qualquer tipo de implementação de cliente, conforme mostrado nas opções abaixo. Você pode usar um método de implementação do lado do cliente, do lado do servidor ou híbrido para suas propriedades:

* Somente no lado do cliente - Para adicionar modificações às suas páginas da Web ou aplicativos móveis, é necessário implementar a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} no seu site ou a [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} nos seus aplicativos móveis.

* Modo híbrido - Você pode usar a [API do AEP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=pt-BR){target="_blank"} para solicitar personalização no lado do servidor; a resposta é fornecida ao Adobe Experience Platform Web SDK para renderizar as modificações no lado do cliente. Saiba mais na [documentação da API do Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"} do Adobe Experience Platform. Você pode obter mais informações sobre o modo híbrido e verificar alguns exemplos de implementação em [esta publicação do blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Lado do servidor - Você pode usar a [API do AEP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=pt-BR){target="_blank"} para solicitar personalização do lado do servidor. Sua equipe de desenvolvimento deve lidar com a resposta e renderizar as modificações no lado do cliente na implementação do aplicativo.

Você pode encontrar amostras para cada método de implementação acima em [esta seção](code-based-implementation-samples.md).

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que as experiências baseadas em código sejam entregues corretamente, as seguintes configurações devem ser definidas:

* Na [Coleção de Dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem uma sequência de dados definida; por exemplo, no serviço **[!UICONTROL Adobe Experience Platform]**, a opção **[!UICONTROL Adobe Journey Optimizer]** está habilitada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Na [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, verifique se você tem uma política de mesclagem com a opção **[!UICONTROL Política de mesclagem Ative-On-Edge]** habilitada. Para fazer isso, selecione uma política no menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Mesclar Políticas]**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Essa política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Para solucionar problemas de entrega de experiências na Web do Journey Optimizer, você pode usar a exibição **Edge Delivery** no **Adobe Experience Platform Assurance**. Este plug-in permite que você inspecione chamadas de solicitação em detalhes, verifique se as chamadas de borda esperadas ocorrem conforme previsto e examine dados de perfil, incluindo mapas de identidade, associações de segmento e configurações de consentimento. Além disso, você pode revisar as atividades para as quais a solicitação se qualificou e identificar aquelas que não foram qualificadas.

  O uso do plug-in **Edge Delivery** ajuda a obter os insights necessários para entender e solucionar problemas de implementações de entrada de maneira eficaz.

  [Saiba mais sobre a visualização do Edge Delivery](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## Pré-requisitos de relatórios {#reporting-prerequisites}

Para habilitar relatórios para o canal baseado em código, você precisa verificar se o [conjunto de dados](../data/get-started-datasets.md) usado na implementação do aplicativo [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na configuração de relatórios.

Em outras palavras, ao configurar os relatórios, se você adicionar um conjunto de dados que não esteja presente no fluxo de dados do aplicativo, os dados do aplicativo não serão exibidos nos relatórios.

Saiba como adicionar conjuntos de dados para relatórios em [esta seção](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo sistema de relatórios [!DNL Journey Optimizer] e não afeta a coleta ou a assimilação de dados.

