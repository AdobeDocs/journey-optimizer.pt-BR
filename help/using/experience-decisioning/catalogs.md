---
title: Catálogo de itens
description: Saiba como trabalhar com o catálogo de itens
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 7%

---


# Catálogo de itens {#catalog}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Experience Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * **[Configurar o catálogo de itens](catalogs.md)**
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

No Experience Decisioning, os catálogos servem como contêineres centrais para organizar itens de decisão. Cada catálogo está vinculado a um esquema do Adobe Experience Platform, abrangendo todos os atributos atribuíveis a um item de decisão.

Por enquanto, todos os itens de decisão criados são consolidados em um único catálogo de &quot;Ofertas&quot;, acessível por meio do **[!UICONTROL Itens]** menu.

![](assets/catalogs-list.png)

Para acessar o schema do catálogo em que os atributos dos itens de decisão são armazenados, siga estas etapas:

1. Na lista de itens, clique no botão **[!UICONTROL Editar esquema]** localizado ao lado do botão **[!UICONTROL Criar item]** botão.

1. O schema do catálogo é aberto em uma nova guia, seguindo a estrutura abaixo:

   * A variável **`_experience`** O nó inclui atributos de itens de decisão padrão, como nome, data inicial e final e descrição.
   * A variável **`_<imsOrg>`** O nó armazena atributos de itens de decisão personalizados. Por padrão, nenhum atributo personalizado é configurado, mas você pode adicionar quantos forem necessários para atender aos seus requisitos. Depois de concluído, os atributos personalizados aparecem na tela de criação do item de decisão ao lado dos atributos padrão.

   ![](assets/catalogs-schema.png)

1. Para adicionar um atributo personalizado ao esquema, expanda a **`_<imsOrg>`** e clique no botão &quot;+&quot; no local desejado na estrutura.

   ![](assets/catalogs-add.png)

1. Preencha os campos necessários para o atributo adicionado e clique em **[!UICONTROL Aplicar]**.

   >[!CAUTION]
   >
   >Por enquanto, o Experience Decisioning oferece suporte exclusivo aos tipos de dados listados abaixo. Qualquer campo fora desses tipos de dados não estará disponível para uso ao criar um item de decisão.
   >* String
   >* Booleano
   >* Número

   Informações detalhadas sobre como trabalhar com esquemas do Adobe Experience Platform estão disponíveis na [Documentação do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=pt-BR).

1. Depois que os atributos personalizados desejados forem adicionados, salve o esquema. O novo campo agora está disponível na tela de criação de decisões de item, no **[!UICONTROL Atributos personalizados]** seção.
