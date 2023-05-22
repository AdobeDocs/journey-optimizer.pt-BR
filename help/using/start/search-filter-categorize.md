---
solution: Journey Optimizer
product: journey optimizer
title: Interface do usuário
description: Saiba mais sobre a interface do usuário do Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: fc7f996fca8b1e8e5f6b7379cc3b2b7da764e0ed
workflow-type: ht
source-wordcount: '498'
ht-degree: 100%

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

Com as [tags unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=pt-BR) da Adobe Experience Platform, é possível classificar facilmente suas jornadas e campanhas do Journey Optimizer para melhorar a pesquisa nas listas.

>[!AVAILABILITY]
>
>As tags unificadas estão atualmente na versão beta. A documentação e a funcionalidade estão sujeitas a alterações.

### Adicionar tags a um objeto

O campo **Tags**, nas propriedades da [jornada](../building-journeys/journey-gs.md#change-properties) ou da [campanha](../campaigns/create-campaign.md#create), permite definir tags para o objeto. É possível selecionar uma tag já existente ou criar uma nova.

Comece a digitar o nome da tag desejada e selecione-a na lista. Se não estiver disponível, clique em **Criar** para criar uma nova tag e adicioná-la. É possível definir quantas tags forem necessárias.

![](assets/tags1.png)

A lista de tags definidas é exibida abaixo do campo **Tags**.

>[!NOTE]
>
> As tags não fazem distinção entre maiúsculas e minúsculas
> 
> Se duplicar ou criar uma nova versão de uma jornada ou campanha, as tags serão preservadas.

### Filtrar por tags

As listas de jornadas e campanhas exibem uma coluna dedicada para que você possa visualizar facilmente as tags.

Um filtro também está disponível para exibir somente jornadas ou campanhas com determinadas tags.

![](assets/tags2.png)

É possível adicionar ou remover tags de qualquer tipo de jornada ou campanha (ativa, rascunho etc.). Para fazer isso, clique no ícone **Mais ações** ao lado do objeto e selecione **Editar tags**.

![](assets/tags3.png)

### Gerenciar tags

Os administradores podem excluir tags e organizá-las por categorias usando o menu **Tags** em **ADMINISTRAÇÃO**. Saiba mais sobre o gerenciamento de tags na [documentação das tags unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=pt-BR).

>[!NOTE]
>
> Tags criadas diretamente do campo **[!UICONTROL Tags]** no Journey Optimizer são automaticamente adicionadas à categoria integrada “Não categorizada”.
