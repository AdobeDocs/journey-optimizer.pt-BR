---
title: Coleções
description: Saiba como trabalhar com coleções
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 36%

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
   1. Selecione o operador desejado e insira o valor para filtrar. Verifique explicitamente cada nome de oferta ou crie e atribua uma tag &quot;luma-summer&quot; a cada oferta.

      >[!NOTE]
      >
      >O operador **CONTAINS** não dá suporte a correspondências parciais ou curingas. Funciona como um operador **IN**, o que significa que você deve fornecer uma matriz de valores exatos para o atributo.
      >
      >Por exemplo, digamos que você tenha várias ofertas de verão que deseja incluir em uma coleção: *&quot;luma-summer-yoga&quot;*, *&quot;luma-summer-fitness&quot;* e *&quot;luma-summer-running&quot;*. Para incluir esses itens, você precisa definir uma regra, como &quot;Nome da oferta&quot; CONTÉM &quot;luma-summer-yoga&quot;, &quot;luma-summer-fitness&quot;, &quot;luma-summer-running&quot;. Essa regra retorna somente as ofertas que correspondem exatamente a um dos nomes na lista.
      >
      >Se você precisar de uma correspondência parcial (por exemplo, todas as ofertas que contêm *&quot;luma-summer&quot;*), isso não é suportado no momento. Você precisa especificar explicitamente cada nome de oferta ou atribuir uma tag *&quot;luma-summer&quot;* a cada oferta e usar essa tag na sua regra.

   1. Repita essas etapas para adicionar quantas regras forem necessárias. Quando várias regras são adicionadas, você pode escolher entre os operadores **And** e **Or** para combiná-las. Para fazer isso, clique no selo do operador para alternar entre as duas opções.
   1. Clique no botão **[!UICONTROL Visualizar coleção]** para exibir os itens que atendem às regras definidas.

   ![](assets/collection-create.png)

1. Após definir as regras de coleção, clique em **[!UICONTROL Criar]**. A coleção agora é exibida na lista.

>[!NOTE]
>
>Cada coleção de itens pode conter até 500 itens de oferta. [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)
