---
title: Criar coleções
description: Saiba como organizar ofertas usando coleções
feature: Offers, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 8%

---

# Criar coleções {#create-collections}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Sobre coleções de ofertas"
>abstract="Com as coleções de ofertas, você pode organizar as ofertas, reagrupando-as em categorias de sua escolha."

As coleções permitem organizar as ofertas reagrupando-as em categorias de sua escolha. Por exemplo, é possível criar uma coleção &quot;sport&quot; que conterá apenas ofertas relacionadas a esportes.

➡️ [Descubra este recurso no vídeo](#video)

A lista de coleções de ofertas pode ser acessada na **[!UICONTROL Ofertas]** menu.

![](../assets/collections_list.png)

Você pode criar dois tipos de coleções:

* **Coleções dinâmicas** são coleções de ofertas com base em qualificadores de coleção (anteriormente conhecidos como &quot;tags&quot;). Essas coleções são atualizadas automaticamente. Por exemplo, se uma nova oferta for criada com o qualificador de coleção selecionado, ela será adicionada automaticamente à coleção.

* **Coleções estáticas** são coleções criadas por meio da seleção manual de ofertas individuais a serem incluídas na coleção. A coleção só pode ser atualizada adicionando manualmente mais ofertas a ela.

Para criar uma coleção, siga estas etapas:

1. Vá para a **[!UICONTROL Coleções]** e clique em **[!UICONTROL Criar coleção]**.

1. Especifique o nome e o tipo da coleção a ser criada.

   ![](../assets/collection_create.png)

1. Para criar uma coleção dinâmica, use o painel esquerdo para selecionar o qualificador da coleção das ofertas a serem adicionadas à coleção e clique em **[!UICONTROL Salvar]**. Todas as ofertas com o qualificador de coleção selecionado serão salvas na coleção.

   Para obter mais informações sobre a criação de qualificadores de coleta, consulte [Criar qualificadores de coleção](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. Para criar uma coleção estática, use o painel esquerdo para filtrar a lista de ofertas (status, qualificador de coleção, data, canal, tipo de conteúdo) e selecione as ofertas a serem adicionadas à coleção.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >As coleções estáticas não são atualizadas automaticamente. Para adicionar ofertas a uma coleção estática, é necessário editá-la e adicioná-las manualmente.

1. Para atribuir rótulos de uso de dados principais ou personalizados a uma coleção estática, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >O uso de OLAC não está disponível para coleções dinâmicas. Ele deve ser gerenciado no nível da oferta. Consequentemente, é possível que você não veja nenhuma oferta em uma coleção dinâmica se não tiver acesso a nenhuma dessas ofertas.

1. Depois que a coleção é criada, ela é exibida na lista. Você pode selecioná-la para editá-la ou excluí-la.

   ![](../assets/collection_created.png)

## Vídeo explicativo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


