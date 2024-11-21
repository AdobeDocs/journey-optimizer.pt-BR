---
solution: Journey Optimizer
product: journey optimizer
title: Pesquisar, filtrar, organizar
description: Saiba mais sobre a interface do Journey Optimizer
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
exl-id: 6151aea2-6a34-4000-ba48-161efe4d94d7
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 82%

---

# Pesquisar, filtrar, organizar {#search-filter-organize}

## Pesquisa{#unified-search}

Em qualquer lugar na interface do Adobe Journey Optimizer, use o recurso de pesquisa unificada da Adobe Experience Cloud no centro da barra superior para localizar ativos, jornadas, conjuntos de dados e muito mais em suas sandboxes.

Comece a inserir conteúdo para exibir os principais resultados. Artigos de ajuda sobre as palavras-chave inseridas também são exibidos nos resultados.

![](assets/unified-search.png)

Pressione **Enter** para acessar todos os resultados e filtrar por objeto comercial.

![](assets/search-and-filter.png)

## Listas de filtros{#filter-lists}

Na maioria das listas, use a barra de pesquisa para localizar itens específicos e definir critérios de filtragem.

Os filtros podem ser acessados com um clique no ícone de filtro na parte superior esquerda de uma lista. O menu de filtro permite filtrar os elementos exibidos de acordo com diferentes critérios: é possível optar por exibir apenas elementos de um determinado tipo ou status, os que você criou ou os que foram modificados nos últimos 30 dias. As opções diferem dependendo do contexto.

Além disso, é possível usar as tags unificadas para filtrar uma lista dependendo das tags atribuídas a um objeto. Por enquanto, as tags estão disponíveis para jornadas e campanhas. [Saiba como trabalhar com tags](#tags)

>[!NOTE]
>
>Observe que as colunas exibidas podem ser personalizadas usando o botão de configuração na parte superior direita das listas. A personalização é salva para cada usuário.

Nas listas, é possível executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item.

![](assets/journey4.png)

## Trabalhar com tags unificadas {#tags}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_tags"
>title="Tags"
>abstract="Esse campo permite atribuir tags unificadas da Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas."

Com as [Tags unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=pt-BR) da Adobe Experience Platform, você pode classificar facilmente os objetos da Journey Optimizer para melhorar a pesquisa nas listas.

![](../rn/assets/do-not-localize/campaigns-tag.gif)

Adicionar tags significativas a públicos na Journey Optimizer permite filtrar e pesquisar mais tarde para encontrar públicos com mais facilidade. As tags também podem ser usadas para organizar públicos-alvo em pastas relevantes e pesquisáveis, criar ofertas e experiências personalizadas e usar em regras de decisão da experiência.

### Adição de tags a um objeto {#add-tags}

O campo **[!UICONTROL Tags]** permite definir tags para o seu objeto. Tags estão disponíveis para os seguintes objetos:

* [Campanhas](../campaigns/create-campaign.md#create)
* [Itens de decisão](../experience-decisioning/items.md)
* [Fragmentos](../content-management/fragments.md)
* [Jornadas](../building-journeys/journey-properties.md)
* [Páginas de destino](../landing-pages/create-lp.md)
* [Listas de assinaturas](../landing-pages/subscription-list.md)
* [Modelos](../content-management/content-templates.md)

É possível selecionar uma tag já existente ou criar uma nova. Para isso, siga as etapas abaixo.

1. Comece digitando o nome da tag desejada e selecione-a na lista.

   ![](assets/tags1.png)

   >[!NOTE]
   >
   > As tags não diferenciam maiúsculas de minúsculas.

1. Se a marca que você está pesquisando não estiver disponível, clique em **[!UICONTROL Criar &quot;&quot;]** para definir uma nova - ela será adicionada automaticamente ao objeto atual e ficará disponível para todos os outros objetos.

   ![](assets/tags4.png)

1. A lista de tags selecionadas ou criadas é exibida abaixo do campo **[!UICONTROL Tags]**. É possível definir quantas tags forem necessárias.

>[!NOTE]
> 
> Se duplicar ou criar uma nova versão de um objeto, as tags serão preservadas.

### Filtrar por tags {#filter-on-tags}

Cada lista de objetos exibe uma coluna dedicada para que você possa visualizar facilmente suas tags.

Um filtro também está disponível para somente exibir objetos com determinadas tags.

![](assets/tags2.png)

É possível adicionar ou remover tags de qualquer tipo de jornada ou campanha (ativa, rascunho etc.). Para fazer isso, clique no ícone **[!UICONTROL Mais ações]** ao lado do objeto e selecione **[!UICONTROL Editar tags]**.

![](assets/tags3.png)

### Gerenciar tags {#manage-tags}

Os administradores podem excluir tags e organizá-las por categorias usando o menu **[!UICONTROL Tags]** em **[!UICONTROL ADMINISTRAÇÃO]**. Saiba mais sobre o gerenciamento de tags na [documentação das tags unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=pt-BR).

>[!NOTE]
>
> Tags criadas diretamente do campo **[!UICONTROL Tags]** no Journey Optimizer são automaticamente adicionadas à categoria integrada “Não categorizada”.
