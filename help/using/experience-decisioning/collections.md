---
title: Coleções
description: Saiba como trabalhar com coleções
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 17%

---

# Coleções {#collections}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Offer Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * **[Gerenciar coleções de itens](collections.md)**
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

As coleções permitem categorizar e agrupar os itens de decisão de acordo com suas preferências. Essas categorias são criadas pela criação de regras que aproveitam os atributos de itens de decisão.

Por exemplo, digamos que você tenha adicionado um atributo personalizado de &quot;Categoria&quot; ao esquema de catálogo dos itens de decisão. Isso permite criar uma coleção que inclui todos os itens de decisão com o valor &quot;Yoga&quot; no atributo &quot;Categoria&quot;.

A lista de coleções pode ser acessada no **[!UICONTROL Itens]** menu.

Para criar uma coleção, siga estas etapas:

1. Navegue até **[!UICONTROL Itens]** > **[!UICONTROL Coleções]** e clique em **[!UICONTROL Criar coleção]**.
1. Forneça um nome e uma descrição para a coleção.
1. Adicione uma ou várias regras para determinar os itens a serem incluídos na coleção. Para fazer isso:

   1. Escolha um atributo de item para usar como critério. A lista de atributos inclui todos os atributos padrão e personalizados definidos no esquema de catálogo. [Saiba mais sobre o catálogo de itens](catalogs.md)
   1. Selecione o operador desejado e insira o valor para filtrar.
   1. Repita essas etapas para adicionar quantas regras forem necessárias. Quando várias regras são adicionadas, você pode escolher entre as opções **E** e **Ou** operadores para combiná-los. Para fazer isso, clique no selo do operador para alternar entre as duas opções.

   ![](assets/collection-create.png)

1. Depois que as regras de coleção forem definidas, clique em **[!UICONTROL Criar]**. A coleção agora é exibida na lista.
