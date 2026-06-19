---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos personalizáveis
description: Saiba como personalizar fragmentos tornando alguns de seus campos editáveis.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: cd47ca1d-f707-4425-b865-14f3fbbe5fd1
TQID: https://experienceleague.adobe.com/cwg-nGPftYg6UgVSKXZPdW6DZr4-m5UM5Wqzfx3w028
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 69ba57a83a35331f05d782588a26f7f45579c180
workflow-type: tm+mt
source-wordcount: 1658
ht-degree: 5%

---

# Fragmentos personalizáveis {#customizable-fragments}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como tornar editáveis campos específicos em fragmentos visuais e de expressão para que os usuários possam personalizá-los ao adicionar o fragmento a uma campanha ou jornada, sem quebrar a herança do fragmento original.

>[!ENDSHADEBOX]

Quando os fragmentos são usados em uma campanha ou ação de jornada, eles são bloqueados por padrão devido à herança. Isso significa que quaisquer alterações feitas em um fragmento são propagadas automaticamente para todas as campanhas e jornadas em que o fragmento é usado.

Com **fragmentos personalizáveis**, campos específicos dentro de um fragmento podem ser definidos como editáveis quando o fragmento é adicionado a uma campanha ou ação de jornada. Por exemplo, suponha que você tenha um fragmento com um banner, texto e botão. Você pode designar determinados campos, como imagem ou URL de destino do botão, como editáveis. Isso permite que os usuários modifiquem esses elementos quando incorporam o fragmento em sua campanha ou jornada, fornecendo uma experiência personalizada sem afetar o fragmento original.

Fragmentos personalizáveis eliminam a necessidade de interromper a herança do fragmento, que anteriormente impedia que as alterações centralizadas no nível do fragmento fossem propagadas para as campanhas e jornadas. Essa abordagem permite que partes do conteúdo sejam ajustadas no momento do uso, oferecendo a flexibilidade de substituir valores padrão por detalhes específicos do contexto.

Ao aproveitar fragmentos personalizáveis, você pode gerenciar e personalizar seu conteúdo com eficiência sem criar blocos de conteúdo totalmente novos ou interromper a herança do fragmento original. Isso garante que as alterações feitas no nível do fragmento ainda sejam propagadas, permitindo a personalização necessária no nível da campanha ou da jornada.

Os fragmentos visuais e de expressão podem ser marcados como personalizáveis. Para obter instruções detalhadas sobre como proceder com cada tipo de fragmento, consulte as seções abaixo.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Adicionar campos editáveis a fragmentos visuais {#visual}

Para tornar partes de um fragmento visual editáveis, siga estas etapas:

>[!NOTE]
>
>Campos editáveis podem ser adicionados aos componentes **imagem**, **texto** e **botão**. Para componentes do **HTML**, os campos editáveis são adicionados usando o editor de personalização, semelhante aos fragmentos de expressão. [Saiba como adicionar campo editável em componentes do HTML e fragmentos de expressão](#expression)

1. Abra a tela de edição de conteúdo do fragmento.

1. Selecione o componente no fragmento onde deseja configurar campos editáveis.

1. O painel de propriedades do componente é aberto no lado direito. Selecione a guia **Campos editáveis** e alterne a opção **Habilitar edição**.

1. Todos os campos que podem ser editados para o componente selecionado são listados no painel. Os campos disponíveis para edição dependem do tipo de componente selecionado.

   No exemplo abaixo, permitimos a edição do URL do botão &quot;Clique aqui&quot;.

   ![](assets/fragment-param-enable.png)

1. Clique em **Visão geral** para verificar todos os campos editáveis e seus valores padrão.

   Neste exemplo, o campo URL do botão é exibido com o valor padrão definido no componente. Esse valor será personalizável pelos usuários depois de adicionarem o fragmento ao conteúdo.

   ![](assets/fragment-param-preview.png)

1. Quando estiver pronto, salve as alterações para atualizar o fragmento.

1. Depois de adicionar o fragmento em um email, os usuários poderão personalizar todos os campos editáveis configurados no fragmento. [Saiba como personalizar campos editáveis em um fragmento visual](../email/use-visual-fragments.md#customize-fields)

>[!CAUTION]
>
>Quando o **rótulo** e a **URL** de um componente de botão se tornam editáveis em um fragmento, os relatórios de rastreamento mostram a URL em vez do rótulo do botão. [Saiba mais sobre o rastreamento](../email/message-tracking.md)

## Ativar a edição de rich text em um fragmento visual personalizável {#rich-text-visual}

>[!CONTEXTUALHELP]
>id="ajo_editable_fragment_compatibility"
>title="Fragmento herdado"
>abstract="Os campos editáveis neste fragmento estão no modo somente texto. Isso significa que você só pode inserir texto sem formatação ao editar esse fragmento em emails. As opções de formatação completas, como negrito, itálico, hiperlinks e quebras de linha, não são compatíveis. Clique em <b>Habilitar</b> para permitir rich text em campos editáveis ao usar o fragmento em um email."

>[!CONTEXTUALHELP]
>id="ajo_editable_field_compatibility"
>title="Fragmento herdado"
>abstract="Este campo editável está no modo somente texto. Opções completas de formatação (negrito, itálico, hiperlinks, quebras de linha etc.) não estarão disponíveis até que o fragmento seja atualizado para o modo rich text. Vá para as configurações do corpo do fragmento e clique em <b>Habilitar</b> para desbloquear rich text em campos editáveis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personalizar campos editáveis em um fragmento"

>[!CONTEXTUALHELP]
>id="ac_editable_fragment_compatibility"
>title="Fragmento herdado"
>abstract="Os campos editáveis neste fragmento estão no modo somente texto. Opções completas de formatação (negrito, itálico, hiperlinks, quebras de linha etc.) não estarão disponíveis até que o fragmento seja atualizado para o modo rich text. Para desbloquear este modo, abra o editor de fragmentos e clique em <b>Habilitar</b>."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personalizar campos editáveis em um fragmento"

O Rich Text <!--— including bold, italic, line breaks, and hyperlinks —--> agora tem suporte nativo em fragmentos visuais personalizáveis.

Quando um fragmento visual personalizável é usado em um email, você pode aproveitar as opções de formatação completas, como negrito, itálico, quebras de linha, listas com marcadores e hiperlinks, diretamente em qualquer campo editável nos componentes do **[!UICONTROL Texto]**, **[!UICONTROL Botão]** e **[!UICONTROL Html]** do fragmento. [Saiba como personalizar campos editáveis](../email/use-visual-fragments.md#customize-fields)

No entanto, se você tiver criado fragmentos e definido campos editáveis antes da introdução do recurso rich text, os campos editáveis serão definidos como modo somente texto por padrão.

* Um aviso de compatibilidade é exibido no editor de fragmentos.

  ![](assets/fragment-custom-compatibility.png)

  Para desbloquear o modo rich-text para esses campos editáveis ao usar o fragmento em um email, clique no botão **Habilitar** e salve o fragmento.

* Depois de adicionado o fragmento a um email, um aviso de compatibilidade também é exibido ao selecionar o fragmento no Designer de email.

  ![](assets/email-fragment-custom-compatibility.png)

  Para atualizar o fragmento para o modo rich text, use o botão **Abrir fragmento** para acessar o editor de fragmentos, clique no botão **Habilitar** e salve o fragmento.

Até que o modo rich text seja desbloqueado, os fragmentos visuais personalizáveis herdados continuarão a suportar somente texto simples. Os usuários não podem inserir rich text nos campos editáveis desses fragmentos.

## Adicionar campos editáveis a componentes do HTML e fragmentos de expressão {#expression}

Para tornar editáveis partes de um componente do HTML ou de um fragmento de expressão, é necessário usar uma sintaxe específica no editor de expressão. Isso envolve declarar uma **variável** com um valor padrão que os usuários podem substituir após adicionar o fragmento ao seu conteúdo.

Por exemplo, suponha que você queira criar um fragmento para adicionar aos emails e permitir que os usuários personalizem uma cor específica usada em locais diferentes, como quadros ou cores de fundo dos botões. Ao criar o fragmento, é necessário declarar uma variável com uma **ID exclusiva**, por exemplo, &quot;cor&quot;, e chamá-la nos locais desejados no conteúdo do fragmento onde deseja aplicar essa cor. Ao adicionar o fragmento ao conteúdo, os usuários poderão personalizar a cor usada sempre que a variável for referenciada.

Para componentes do HTML, somente elementos específicos podem se tornar campos editáveis. Expanda a seção abaixo para obter mais informações.

+++Elementos editáveis em componentes do HTML:

Os elementos abaixo podem se tornar campos editáveis em um componente do HTML:

* Uma parte do texto
* Um URL completo para link ou imagem (não funciona com parte de um URL)
* Propriedade CSS inteira (não funciona com a propriedade parcial)

Por exemplo, no código abaixo, cada elemento destacado em vermelho pode se tornar uma propriedade:

![](assets/fragment-html.png){width="70%"}

+++

Para declarar uma variável e usá-la no fragmento, siga estas etapas:

1. Abra o fragmento de expressão e edite o conteúdo no editor de personalização.

   ![](assets/fragment-html-edit.png)

   Para componentes do HTML, selecione o componente no fragmento e clique no botão **Mostrar o código-fonte**.

1. Declarar a variável que você deseja que os usuários editem. Navegue até o menu **Funções auxiliares** no painel de navegação esquerdo e adicione a função auxiliar **embutida**. A sintaxe a ser declarada e chamada para a variável é adicionada automaticamente no conteúdo.

   ![](assets/fragment-add-helper.png)

1. Substitua `"name"` por uma ID exclusiva para identificar o campo editável.

   >[!NOTE]
   >
   >A ID do campo deve ser exclusiva e não deve ter espaços. Essa ID deve ser usada em qualquer lugar no conteúdo onde você deseja exibir o valor da variável.

1. Adapte a sintaxe de acordo com suas necessidades adicionando parâmetros detalhados na tabela abaixo:

   | Ação | Parâmetro | Exemplo |
   | ------- | ------- | ------- |
   | Declarar um campo editável com um **valor padrão**. Ao adicionar o fragmento ao conteúdo, esse valor padrão será usado se você não personalizá-lo. | Adicione o valor padrão entre as tags em linha. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Defina um **rótulo** para o campo editável. Esse rótulo será exibido no Designer de email ao editar os campos do fragmento. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Declare um campo editável contendo uma **origem da imagem** que precisa ser publicada. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Declarar um campo editável contendo um **URL** que precisa ser rastreado.<br/>Observe que os blocos predefinidos de &quot;URL da mirror page&quot; e &quot;Cancelar inscrição do link&quot; não podem se tornar campos editáveis. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Use a sintaxe `{{{name}}}` no código em todos os locais onde deseja exibir o valor do campo editável. Substitua `name` pela ID exclusiva do campo definido anteriormente.

   ![](assets/fragment-call-variable.png)

1. Salve e publique o fragmento.

Ao adicionar o fragmento ao conteúdo de email, os usuários agora podem substituir os valores padrão das variáveis pelos valores escolhidos:

* Para fragmentos de expressão, uma sintaxe específica é usada para substituir valores de variáveis. [Saiba como personalizar campos editáveis em um fragmento de expressão](../personalization/use-expression-fragments.md#customize-fields)

* Para componentes do HTML, a variável é exibida na lista de campos editáveis no Designer de email. [Saiba como personalizar campos editáveis em um fragmento visual](../email/use-visual-fragments.md#customize-fields)

### Exemplo: fragmento de expressão personalizável {#example}

No exemplo abaixo, estamos criando um fragmento de expressão que apresenta novas coleções de esportes. Por padrão, o fragmento exibe este conteúdo: *Procurando mais? Não perca nossa última coleção de esportes!*

Queremos permitir que os usuários substituam &quot;esportes&quot; nesse conteúdo pelo esporte de sua escolha. Por exemplo: *Procurando mais? Não perca nossa última coleção de ioga!*

Para fazer isso:

1. Declarar uma variável &quot;sport&quot; com a ID &quot;sport&quot;.

   Por padrão, se os usuários não alterarem o valor da variável após adicionar o fragmento ao conteúdo, ele mostrará o valor definido entre as tags `{{#inline}}` e `{{/inline}}`, ou seja, &quot;esportes&quot;.

1. Adicione a sintaxe ``{{{sport}}}`` no conteúdo do fragmento em que deseja exibir o valor da variável, ou seja, &quot;esportes&quot; por padrão ou o valor escolhido pelos usuários.

   ![](assets/fragment-expression-custom.png)

1. Ao adicionar o fragmento de expressão ao seu conteúdo, os usuários podem alterar o valor da variável com sua escolha diretamente no editor de expressão. [Saiba como personalizar campos editáveis em um fragmento de expressão](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)

<!--
## Add rich text to a customizable fragment {#rich-text}

Rich text such as line breaks, bold, italics etc., can be added to a customizable fragment by using HTML components. To do so, follow the steps below.

➡️ [Learn how to add and use rich text in a customizable fragment in this video](#video)

### Create a fragment including rich text {#add-rich-text}

The approach below (using HTML components with inline variables) remains fully supported for advanced HTML-based scenarios??

1. Create a visual [fragment](create-fragments.md) and start adding components.

1. Add an [HTML component](../email/content-components.md#HTML) and open the HTML editor.

1. Navigate to the **[!UICONTROL Helper functions]** menu in the left navigation pane and add the **inline** helper function.

1. Replace `"name"` with the ID you want to use for your editable content, for example "EditableContent".

1. Replace `render_content` with the HTML code corresponding to the default rich content you want. You can add bold, italic, line breaks, bulleted lists, etc.

    ![](assets/fragment-rich-editable-content.png)

1. Within the same HTML component, add another **inline** helper function for your styling elements.

1. Replace `"name"` and `render_content` with the ID and HTML code corresponding to the default styling you want.

    ![](assets/fragment-rich-editable-styling.png)

1. Save your content. The selected editable fields are displayed on the right-hand side.

    ![](assets/fragment-rich-editable-fields.png)

1. Save and [publish](create-fragments.md#publish) the fragment.

### Use rich text in customizable fragments {#use-rich-text}

When adding the fragment to your email, you can now edit the rich text content and styling that you created. As a marketer, follow the steps below.

1. [Create an email](../email/create-email.md) in a campaign or a journey, then add the fragment with rich text that was [created](#add-rich-text).

    You can see the two editable fields that were created on the right-hand side.

    ![](assets/fragment-use-rich-editable-fields.png)

1. Use either simulation method to see how the editable content and styling render: click **[!UICONTROL Simulate content]** to test content variations with sample input data or AI auto-generation, or click **[!UICONTROL Simulate content]**, then select **[!UICONTROL Simulate content (AEP profiles)]** from the dropdown to preview with test profiles. [Learn more on previewing content](preview-test.md)

1. Select the **[!UICONTROL Add personalization]** icon next to one of the editable fields.

1. In the personalization editor that opens, update the styling and/or content as wanted by adding or removing elements of the editable field.

    ![](assets/fragment-rich-editable-fields-update-styling.png)

## How-to video {#video}

This video shows how to make HTML components within a fragment editable, allowing for dynamic updates to both content and styling.

>[!VIDEO](https://video.tv.adobe.com/v/3464373/?captions=por_br&learn=on&#x26;enablevpops)
-->