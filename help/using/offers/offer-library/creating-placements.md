---
title: Criar posicionamentos
description: Saiba como criar inserções para suas ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 9e8bac0c908646213a9d9a0598e3aa4750084b50
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 5%

---

# Criar posicionamentos {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="Disposição"
>abstract="Uma inserção é um container usado para exibir ofertas. Isso ajuda a garantir que o conteúdo de oferta correto seja exibido no local certo na mensagem. As disposições são criadas no menu &quot;Componentes&quot;."

Uma disposição ajuda a garantir que o conteúdo de oferta correto seja exibido no local certo na mensagem. Ao adicionar conteúdo a uma oferta, você será solicitado a selecionar uma disposição na qual o conteúdo possa ser exibido.

➡️ [Saiba como criar inserções neste vídeo](#video)

No exemplo abaixo, há três disposições correspondentes a diferentes tipos de conteúdo (imagem, texto, HTML).

![](../assets/offers_placement_schema.png)

A lista de disposições pode ser acessada no **[!UICONTROL Componentes]** menu. Os filtros estão disponíveis para ajudá-lo a recuperar inserções de acordo com um canal ou conteúdo específico.

![](../assets/placements_filter.png)

Para criar uma inserção, siga estas etapas:

1. Clique em **[!UICONTROL Criar posicionamento]**.

   ![](../assets/offers_placement_creation.png)

1. Defina as propriedades da disposição:

   * **[!UICONTROL Nome]**: o nome do posicionamento. Defina um nome significativo para recuperá-lo mais facilmente.
   * **[!UICONTROL Tipo de canal]**: o canal para o qual o posicionamento será usado.
   * **[!UICONTROL Tipo de conteúdo]**: O tipo de conteúdo que o posicionamento poderá exibir: Texto, HTML, Link de imagem ou JSON.
   * **[!UICONTROL Descrição]**: uma descrição do posicionamento (opcional).

   ![](../assets/offers_placement_creation_properties.png)


1. A variável **[!UICONTROL Configurações de solicitação]** e **[!UICONTROL Formato de resposta]** As seções fornecem parâmetros adicionais:

   * **[!UICONTROL Permitir duplicações em posicionamentos]**: controla se a mesma oferta pode ser proposta várias vezes em diferentes posicionamentos. Se ativado, o sistema considerará a mesma oferta para vários posicionamentos.

      Se essa opção for definida como falso para qualquer posicionamento em uma solicitação de decisão, todas as inserções na solicitação herdarão a configuração &quot;falso&quot;.

   * **[!UICONTROL Solicitar oferta]**: por padrão, uma oferta do escopo de decisão é retornada para cada perfil. Você pode ajustar o número de ofertas retornadas usando essa opção. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para o escopo de decisão selecionado.

   * **[!UICONTROL Incluir conteúdo]** / **[!UICONTROL Incluir metadados]**: especifique se o conteúdo e os metadados da oferta devem ser retornados na resposta da API. É possível incluir todos os metadados ou campos específicos apenas.
   Esses parâmetros também podem ser definidos diretamente na sua solicitação de API se você estiver trabalhando com o [API de decisão](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). No entanto, configurá-los na interface pode ajudar a economizar tempo, pois não será necessário transmiti-los em cada solicitação de API. Observe que, se você configurar os parâmetros na interface do usuário do e na solicitação de API, os valores da solicitação de API prevalecerão sobre os da interface.

   >[!NOTE]
   >
   >Se você estiver trabalhando com a variável [API do Edge Decisioning](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?), não é possível definir esses parâmetros em sua solicitação. Você precisa defini-los nesta tela. Se você estiver trabalhando com a variável [API de decisão em lote](../api-reference/offer-delivery-api/batch-decisioning-api.md), é necessário incluir esses parâmetros diretamente na solicitação da API, pois os parâmetros definidos nessa tela não são considerados para o envio do delivery em lote.

1. Clique em **[!UICONTROL Salvar]** para confirmar.

1. Depois que a disposição é criada, ela é exibida na lista de disposições. Você pode selecioná-la para exibir suas propriedades e editá-la.

   ![](../assets/placement_created.png)

## Vídeo explicativo{#video}

Saiba como criar inserções na gestão de decisões.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

