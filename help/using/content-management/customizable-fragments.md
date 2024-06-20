---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos personalizáveis
description: Saiba como personalizar fragmentos tornando alguns de seus campos editáveis.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: c84c09aac2d888c689591f2517269c88bee0cda6
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---


# Fragmentos personalizáveis {#customizable-fragments}

Quando os fragmentos são usados em uma campanha ou ação de jornada, eles são bloqueados por padrão devido à herança. Isso significa que quaisquer alterações feitas em um fragmento são propagadas automaticamente para todas as campanhas e jornadas em que o fragmento é usado. Com fragmentos personalizáveis, campos específicos em um fragmento podem ser definidos como editáveis quando o fragmento é adicionado a uma campanha ou ação de jornada. Por exemplo, suponha que você tenha um fragmento com um banner, texto e botão. Você pode designar determinados campos, como imagem ou URL de destino do botão, como editáveis. Isso permite que os usuários modifiquem esses elementos quando incorporam o fragmento em sua campanha ou jornada, fornecendo uma experiência personalizada sem afetar o fragmento original.

Fragmentos personalizáveis eliminam a necessidade de interromper a herança do fragmento, que anteriormente impedia que as alterações centralizadas no nível do fragmento fossem propagadas para as campanhas e jornadas. Essa abordagem permite que partes do conteúdo sejam ajustadas no momento do uso, oferecendo a flexibilidade de substituir valores padrão por detalhes específicos do contexto.

Ao aproveitar fragmentos personalizáveis, você pode gerenciar e personalizar seu conteúdo com eficiência sem criar blocos de conteúdo totalmente novos ou interromper a herança do fragmento original. Isso garante que as alterações feitas no nível do fragmento ainda sejam propagadas, permitindo a personalização necessária no nível da campanha ou da jornada.

Os fragmentos visuais e de expressão podem ser marcados como personalizáveis. Para obter instruções detalhadas sobre como proceder com cada tipo de fragmento, consulte as seções abaixo.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Adicionar campos editáveis em fragmentos visuais {#visual}

Para tornar partes de um fragmento visual editáveis, siga estas etapas:

>[!NOTE]
>
>Campos editáveis podem ser adicionados a **imagem**, **texto** e **botão** componentes. Para **HTML** componentes e campos editáveis são adicionados usando o editor de personalização, semelhante aos fragmentos de expressão. [Saiba como adicionar campo editável em componentes de HTML e fragmentos de expressão](#expression)

1. Abra a tela de edição de conteúdo do fragmento.

1. Selecione o componente no fragmento onde deseja configurar campos editáveis.

1. O painel de propriedades do componente é aberto no lado direito. Selecione o **Campos editáveis** e alterne a guia **Ativar edição** opção.

1. Todos os campos que podem ser editados para o componente selecionado são listados no painel. Os campos disponíveis para edição dependem do tipo de componente selecionado.

   No exemplo abaixo, permitimos a edição do URL do botão &quot;Clique aqui&quot;.

   ![](assets/fragment-param-enable.png)

1. Clique em **Visão geral** para verificar todos os campos editáveis e seus valores padrão.

   Neste exemplo, o campo URL do botão é exibido com o valor padrão definido no componente. Esse valor será personalizável pelos usuários depois de adicionarem o fragmento ao conteúdo.

   ![](assets/fragment-param-preview.png)

1. Quando estiver pronto, salve as alterações para atualizar o fragmento.

1. Depois de adicionar o fragmento em um email, os usuários poderão personalizar todos os campos editáveis configurados no fragmento. [Saiba como personalizar campos editáveis em um fragmento visual](../email/use-visual-fragments.md#customize-fields)

## Adicionar campos editáveis em componentes de HTML e fragmentos de expressão {#expression}

Para tornar editáveis partes de um componente de HTML ou de um fragmento de expressão, é necessário usar uma sintaxe específica no editor de expressão. Isso envolve a declaração de um **variável** por um valor padrão que os usuários podem substituir após adicionar o fragmento ao seu conteúdo.

Por exemplo, suponha que você queira criar um fragmento para adicionar aos emails e permitir que os usuários personalizem uma cor específica usada em locais diferentes, como quadros ou cores de fundo dos botões. Ao criar o fragmento, é necessário declarar uma variável com um **identificador exclusivo**, por exemplo, &quot;cor&quot;, e chame-a nos locais desejados no conteúdo do fragmento, onde essa cor deve ser aplicada. Ao adicionar o fragmento ao conteúdo, os usuários poderão personalizar a cor usada sempre que a variável for referenciada.

Para componentes HTML, somente elementos específicos podem se tornar campos editáveis. Expanda a seção abaixo para obter mais informações.

+++Elementos editáveis nos componentes do HTML:

Os elementos abaixo podem se tornar campos editáveis em um componente HTML:

* Uma parte do texto
* Um URL completo para link ou imagem (não funciona com parte de um URL)
* Propriedade CSS inteira (não funciona com a propriedade parcial)

Por exemplo, no código abaixo, cada elemento destacado em vermelho pode se tornar uma propriedade:

![](assets/fragment-html.png){width="70%"}

+++

Para declarar uma variável e usá-la no fragmento, siga estas etapas:

1. Abra o fragmento de expressão e edite o conteúdo no editor de personalização. Para componentes de HTML, selecione o componente no fragmento e clique no **Mostrar o código-fonte** botão.

   ![](assets/fragment-html-edit.png)

1. Declarar a variável que você deseja que os usuários editem. Navegue até a **Funções auxiliares** no painel de navegação esquerdo e adicione a **em linha** função auxiliar. A sintaxe a ser declarada e chamada para a variável é adicionada automaticamente no conteúdo.

   ![](assets/fragment-add-helper.png)

1. Substituir `"name"` com uma ID exclusiva para identificar o campo editável.

   >[!NOTE]
   >
   >A ID do campo deve ser exclusiva e não deve ter espaços. Essa ID deve ser usada em qualquer lugar no conteúdo onde você deseja exibir o valor da variável.

1. Adapte a sintaxe de acordo com suas necessidades adicionando parâmetros detalhados na tabela abaixo:

   | Ação | Parâmetro | Exemplo |
   | ------- | ------- | ------- |
   | Declarar um campo editável com um **valor padrão**. Ao adicionar o fragmento ao conteúdo, esse valor padrão será usado se você não personalizá-lo. | Adicione o valor padrão entre as tags em linha. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Definir um **rótulo** para o campo editável. Esse rótulo será exibido no Designer de email ao editar os campos do fragmento. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Declarar um campo editável contendo um **Image source** que precisa ser publicado. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Declarar um campo editável contendo um **URL** que precisa ser rastreado.<br/>Observe que os blocos predefinidos prontos para uso &quot;Mirror page URL&quot; e &quot;Unsubscribe link&quot; não podem se tornar campos editáveis. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Use o `{{{name}}}` sintaxe no código em todos os locais onde deseja exibir o valor do campo editável. Substituir `name` com a ID exclusiva do campo definida anteriormente.

   ![](assets/fragment-call-variable.png)

1. Salve o fragmento.

Ao adicionar o fragmento ao conteúdo de email, os usuários agora podem substituir os valores padrão das variáveis pelos valores escolhidos:

* Para fragmentos de expressão, uma sintaxe específica é usada para substituir valores de variáveis. [Saiba como personalizar campos editáveis em um fragmento de expressão](../personalization/use-expression-fragments.md#customize-fields)

* Para componentes HTML, a variável é exibida na lista de campos editáveis no Designer de email. [Saiba como personalizar campos editáveis em um fragmento visual](../email/use-visual-fragments.md#customize-fields)

## Exemplo de fragmento de expressão editável {#example}

No exemplo abaixo, estamos criando um fragmento de expressão que apresenta novas coleções de esportes. Por padrão, o fragmento exibe este conteúdo: *Procurando mais? Não perca nossa mais recente coleção de esportes!*

Queremos permitir que os usuários substituam &quot;esportes&quot; nesse conteúdo pelo esporte de sua escolha. Por exemplo: *Procurando mais? Não perca nossa última coleção de ioga!*

Para fazer isso:

1. Declarar uma variável &quot;sport&quot; com a ID &quot;sport&quot;.

   Por padrão, se os usuários não alterarem o valor da variável depois de adicionar o fragmento ao conteúdo, ele mostrará o valor definido entre as variáveis `{{#inline}}` e `{{/inline}}` tags, ou seja, &quot;esportes&quot;.

1. Adicione o ``{{{sport}}}`` no conteúdo do fragmento, onde você deseja exibir o valor da variável, ou seja, &quot;esportes&quot; por padrão ou o valor escolhido pelos usuários.

   ![](assets/fragment-expression-custom.png)

1. Ao adicionar o fragmento de expressão ao seu conteúdo, os usuários podem alterar o valor da variável com sua escolha diretamente no editor de expressão. [Saiba como personalizar campos editáveis em um fragmento de expressão](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
