---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Criar coleções
description: Saiba como organizar ofertas usando coleções
badge: label="Legado" type="Informative"
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7IXZss-Qpg5D67uPfkFbo3Gmp1n2gdSD24Y4rbL3-Fk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 34%

---

# Criar coleções {#create-collections}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Sobre coleções de ofertas"
>abstract="Com as coleções de ofertas, você pode organizar as ofertas, reagrupando-as em categorias de sua escolha."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="Coleção dinâmica"
>abstract="Use qualificadores de coleção para criar uma coleção de ofertas dinâmica."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="Coleção estática"
>abstract="Selecione e agrupe ofertas manualmente, usando critérios como status, qualificadores de coleção, data e canal."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="Visualização de coleções estáticas"
>abstract="As coleções estáticas são criadas por meio da seleção manual de ofertas individuais para incluir na coleção. A coleção só pode ser atualizada por meio da adição manual de ofertas."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="Visualização de coleções dinâmicas"
>abstract="As coleções dinâmicas reúnem ofertas com base em qualificadores de coleção. Essas coleções são atualizadas automaticamente. Por exemplo, se você criar uma nova oferta com o qualificador de coleção “esportes”, ela será adicionada automaticamente à coleção correspondente."

As coleções permitem organizar as ofertas reagrupando-as em categorias de sua escolha. Por exemplo, é possível criar uma coleção &quot;sport&quot; que conterá apenas ofertas relacionadas a esportes.

➡️ [Conheça este recurso no vídeo](#video)

A lista de coleções de ofertas está acessível no menu **[!UICONTROL Ofertas]**.

![](../assets/collections_list.png)

Você pode criar dois tipos de coleções:

* **Coleções dinâmicas** são coleções de ofertas baseadas em qualificadores de coleção (anteriormente conhecidas como &quot;marcas&quot;). Essas coleções são atualizadas automaticamente. Por exemplo, se uma nova oferta for criada com o qualificador de coleção selecionado, ela será adicionada automaticamente à coleção.

* **Coleções estáticas** são coleções criadas por meio da seleção manual de ofertas individuais a serem incluídas na Coleção. A coleção só pode ser atualizada por meio da adição manual de ofertas.

Para criar uma coleção, siga estas etapas:

1. Vá para a guia **[!UICONTROL Coleções]** e clique em **[!UICONTROL Criar coleção]**.

1. Especifique o nome e o tipo da coleção a ser criada.

   ![](../assets/collection_create.png)

1. Para criar uma coleção dinâmica, use o painel esquerdo para selecionar o qualificador da coleção das ofertas a serem adicionadas à coleção e clique em **[!UICONTROL Salvar]**. Todas as ofertas com o qualificador de coleção selecionado serão salvas na coleção.

   Para obter mais informações sobre a criação de qualificadores de coleção, consulte [Criar qualificadores de coleção](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. Para criar uma coleção estática, use o painel esquerdo para filtrar a lista de ofertas (status, qualificador de coleção, data, canal, tipo de conteúdo) e selecione as ofertas a serem adicionadas à coleção.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >As coleções estáticas não são atualizadas automaticamente. Para adicionar ofertas a uma coleção estática, é necessário editá-la e adicioná-las manualmente.

1. Para atribuir rótulos de uso de dados principais ou personalizados a uma coleção estática, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >O uso de OLAC não está disponível para coleções dinâmicas. Ele deve ser gerenciado no nível da oferta. Consequentemente, é possível que você não veja nenhuma oferta em uma coleção dinâmica se não tiver acesso a nenhuma dessas ofertas.

1. Depois que a coleção é criada, ela é exibida na lista. Você pode selecioná-la para editá-la ou excluí-la.

   ![](../assets/collection_created.png)

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


