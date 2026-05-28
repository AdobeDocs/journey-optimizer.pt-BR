---
solution: Journey Optimizer
product: journey optimizer
title: Definir as propriedades da campanha acionada pela API
description: Saiba como definir as propriedades da campanha acionada pela API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: bda7e337-a246-4f01-b935-4a234d4c4baa
TQID: https://experienceleague.adobe.com/qUWCJifjUbLmapOtZlk9elkRZLcr-XGXNzuy0rayx-8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 301
ht-degree: 19%

---

# Definir as propriedades da campanha acionada pela API {#api-properties}

Para criar uma nova campanha acionada por API, siga estas etapas:

1. Navegue até o menu **[!UICONTROL Campanhas]** e selecione a guia **[!UICONTROL API acionada]**.

1. Clique no botão **[!UICONTROL Criar campanha]** e selecione o tipo de campanha:

   * **[!UICONTROL API acionada - Marketing]** - Selecione esse tipo de campanha acionada por API para enviar comunicações de marketing personalizadas a públicos-alvo direcionados.

   * **[!UICONTROL API acionada - Transacional]** - As campanhas transacionais são destinadas a enviar mensagens transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: solicitação de redefinição de senha, compra de carrinho, etc.

     +++Modo de alto rendimento

     Para campanhas acionadas por API transacional, é possível habilitar o modo **[!UICONTROL Alta Taxa de Transferência]**. Esse modo foi projetado para mensagens em tempo real em larga escala (até 5.000 transações por segundo) e fornece maior disponibilidade com menor latência. [Saiba como trabalhar com o modo de Reagrupamento](../campaigns/api-triggered-high-throughput.md)

     >[!AVAILABILITY]
     >
     >Atualmente, o modo de alta taxa de transferência está disponível somente para o canal de email e na região dos EUA.
     >
     >Esse recurso só está disponível para organizações que compraram a oferta complementar **Mensagens transacionais de alta taxa de transferência** da Adobe. Entre em contato com o representante da Adobe para obter mais informações.

     +++

   ![](assets/api-triggered-modal.png)

1. Na guia **[!UICONTROL Propriedades]**, digite um nome e uma descrição para a campanha.

   ![](assets/create-campaign-properties.png)

1. Use o campo **Tags** para atribuir Tags unificadas do Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags).

1. Você pode limitar o acesso a esta campanha com base nos rótulos de acesso. Para adicionar uma limitação de acesso, navegue até o botão **[!UICONTROL Gerenciar acesso]** na parte superior desta página. Selecione apenas os rótulos para os quais você tem permissão. [Saiba mais sobre o Controle de Acesso em Nível de Objeto](../administration/object-based-access.md).

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá configurar sua ação. [Saiba mais](api-triggered-campaign-action.md)
