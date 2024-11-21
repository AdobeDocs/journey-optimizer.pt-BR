---
title: Coleções
description: Saiba como trabalhar com coleções
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: 6b0735f619379e01e87012ba4300c0ec41334fd4
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 48%

---

# Coleções {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Criar coleções"
>abstract="As coleções permitem categorizar e agrupar itens de decisão de acordo com as suas preferências. Essas categorias são criadas pela construção de regras que aproveitam os atributos de itens de decisão."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Definir regras para a coleção"
>abstract="Adicione uma ou várias regras para determinar os itens a serem incluídos na coleção. Escolha um atributo de item para usar como critério. Selecione o operador desejado e insira o valor para filtrar. Adicione quantas regras forem necessárias."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Escolha uma coleção"
>abstract="Selecione a coleção que contém as ofertas a serem consideradas. Esta etapa é obrigatória ao criar uma estratégia de seleção. As coleções permitem categorizar e agrupar itens de decisão de acordo com as suas preferências. Por exemplo, você pode criar uma coleção que inclui todos os itens de decisão com o valor “Yoga” no atributo personalizado “Categoria”."

As coleções permitem categorizar e agrupar itens de decisão de acordo com as suas preferências. Essas categorias são criadas pela construção de regras que aproveitam os atributos de itens de decisão.

Por exemplo, digamos que você tenha adicionado um atributo personalizado de &quot;Categoria&quot; ao esquema de catálogo dos itens de decisão. Isso permite criar uma coleção que inclui todos os itens de decisão com o valor &quot;Yoga&quot; no atributo &quot;Categoria&quot;.

A lista de coleções pode ser acessada no menu **[!UICONTROL Catálogos]**.

Para criar uma coleção, siga estas etapas:

1. Navegue até **[!UICONTROL Catálogos]** > **[!UICONTROL Coleções]** e clique em **[!UICONTROL Criar coleção]**.
1. Forneça um nome e uma descrição para a coleção.
1. Adicione uma ou várias regras para determinar os itens a serem incluídos na coleção. Para fazer isso:

   1. Escolha um atributo de item para usar como critério. A lista de atributos inclui todos os atributos padrão e personalizados definidos no esquema de catálogo. [Saiba mais sobre o catálogo de itens](catalogs.md)
   1. Selecione o operador desejado e insira o valor para filtrar.
   1. Repita essas etapas para adicionar quantas regras forem necessárias. Quando várias regras são adicionadas, você pode escolher entre os operadores **And** e **Or** para combiná-las. Para fazer isso, clique no selo do operador para alternar entre as duas opções.
   1. Clique no botão **[!UICONTROL Visualizar coleção]** para exibir os itens que atendem às regras definidas.

   ![](assets/collection-create.png)

1. Após definir as regras de coleção, clique em **[!UICONTROL Criar]**. A coleção agora é exibida na lista.

>[!NOTE]
>
>Cada coleção de itens pode conter até 500 itens de oferta. [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)
