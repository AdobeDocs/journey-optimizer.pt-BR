---
title: Gerenciar modificações na Web
description: Saiba como gerenciar modificações no conteúdo da página da Web do Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 12%

---

# Gerenciar modificações na Web {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gerenciar facilmente todas as alterações"
>abstract="Usando esse painel, você pode navegar e gerenciar todos os ajustes e estilos adicionados à sua página da Web."

É possível gerenciar facilmente todos os componentes, ajustes e estilos adicionados à página da Web. Você também pode adicionar modificações diretamente no painel dedicado.

## Trabalhar com o painel Modificações {#use-modifications-pane}

1. Selecione o **[!UICONTROL Modificações]** ícone para exibir o painel correspondente à esquerda.

   ![](assets/web-designer-modifications-pane.png)

1. Você pode revisar cada uma das alterações feitas na página.

1. Selecione uma modificação indesejada e clique no botão **[!UICONTROL Excluir modificação]** opção no **[!UICONTROL Mais ações]** botão para removê-lo.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Continue com cuidado ao excluir uma ação, pois ela pode afetar as ações subsequentes.

1. Para excluir várias modificações ao mesmo tempo, clique no link **[!UICONTROL Selecionar]** na parte superior do **[!UICONTROL Modificações]** verifique as modificações de sua escolha e clique no botão **[!UICONTROL Excluir]** ícone.

   ![](assets/web-designer-modifications-select-delete.png)

1. Use o **[!UICONTROL Mais ações]** na parte superior do **[!UICONTROL Modificações]** para excluir todas as modificações de uma só vez.

   ![](assets/web-designer-delete-modifications.png)

1. Você também pode excluir somente as modificações inválidas, o que significa que as alterações foram substituídas por outras alterações. Por exemplo, se você modificar a cor de um texto e, em seguida, excluir esse texto, a modificação de cor se tornará inválida, pois o texto não existe mais.

1. É possível cancelar e refazer ações usando a variável **[!UICONTROL Desfazer/Refazer]** botão na parte superior direita da tela.

   ![](assets/web-designer-undo-redo.png)

   Clique e mantenha pressionado o botão para alternar entre as **[!UICONTROL Desfazer]** e **[!UICONTROL Refazer]** opções. Em seguida, clique no próprio botão para aplicar a ação desejada.

## Adicionar modificações do painel dedicado {#add-modifications}

Ao editar uma página usando o web designer, você pode adicionar novas alterações ao seu conteúdo diretamente do **[!UICONTROL Modificações]** painel - sem a necessidade de selecionar um componente e editá-lo na interface do web designer. Siga as etapas abaixo.

1. No **[!UICONTROL Modificações]** clique no botão **[!UICONTROL Mais ações]** botão.

1. Selecionar **[!UICONTROL Adicionar uma modificação]**.

   ![](assets/web-designer-add-modification.png)

1. Selecione o tipo de modificação:

   * **[!UICONTROL Seletor de CSS]** - [Saiba mais](#css-selector)
   * **[!UICONTROL Página`<Head>`]** - [Saiba mais](#page-head)

1. Insira seu conteúdo e **[!UICONTROL Salvar]** suas alterações.

1. Clique em **[!UICONTROL Mais ações]** botão ao lado da sua modificação e selecione **[!UICONTROL Informações]** para exibir seus detalhes.

   ![](assets/web-designer-add-modification-info.png)

### Seletor de CSS {#css-selector}

Para adicionar um **Seletor de CSS** tipo de modificação, siga as etapas abaixo.

1. Selecionar **[!UICONTROL Seletor de CSS]** como o tipo de modificação.

1. A variável **[!UICONTROL Seletor de elemento CSS]** ajuda a localizar e selecionar os elementos de HTML (ou nós na árvore DOM) aos quais deseja aplicar as alterações. <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. Selecionar um tipo de ação (**[!UICONTROL Definir conteúdo]** ou **[!UICONTROL Definir atributo]**) e preencha as informações/conteúdo necessários.

   * **[!UICONTROL Definir conteúdo]**: especifique o conteúdo que entra no elemento identificado pelo **[!UICONTROL Seletor de elemento CSS]** campo.

   * **[!UICONTROL Definir atributo]**: especifique um atributo a ser associado ao seletor de CSS atual para que esse seletor também possa ser identificado por esse atributo. Para fazer isso, insira um nome no campo **[!UICONTROL Nome do atributo]** e um valor no campo **[!UICONTROL Conteúdo]** campo. Se o atributo já existir, o valor será atualizado; caso contrário, um novo atributo será adicionado com o nome e o valor especificados.

     ![](assets/web-designer-add-modification-css-attribute.png)

### Página `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="Adicionar código personalizado"
>abstract="O elemento HEAD é um container de metadados que é inserido entre a tag HTML e a tag BODY. Adicionar apenas elementos SCRIPT e STYLE. Adicionar tags DIV e outros elementos pode fazer com que os elementos HEAD restantes sejam exibidos em BODY. "

É possível adicionar um código personalizado usando o **[!UICONTROL Página`<head>`]** tipo de modificação.

A variável `<head>` elemento é um container de metadados (dados sobre dados) e é colocado entre o `<html>` e a tag `<body>` tag. Nesse caso, o código não aguarda os eventos body ou page-load; ele é executado no início do carregamento da página.

A variável `<head>` O elemento é normalmente usado para adicionar JavaScript ou código CSS à parte superior da página. Os seletores para ações visuais subsequentes dependem dos elementos HTML adicionados nessa guia.

Para adicionar um **Página`<head>`** tipo de modificação, siga as etapas abaixo.

1. Selecionar **[!UICONTROL Página`<head>`]** como o tipo de modificação.

   ![](assets/web-designer-add-modification-head-type.png)

1. Adicione seu código personalizado no **[!UICONTROL Conteúdo]** caixa.

   >[!CAUTION]
   >
   >Você só pode adicionar `<script>` e `<style>` elementos para o `<head>` seção. Adicionar tags `<div>` e outros elementos pode fazer com que os elementos `<head>` restantes apareçam em `<body>`. 

1. Clique em **[!UICONTROL Opções de edição avançadas]** botão. O editor de expressão se abre.

   ![](assets/web-designer-add-modification-head-advanced.png)

   Você pode aproveitar o [!DNL Journey Optimizer] Editor de expressão com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

#### Exemplos de código personalizado {#custom-code-examples}

Você pode usar o **[!UICONTROL Página`<head>`]** tipo de modificação para:

* Use JavaScript em linha ou vincule a um arquivo JavaScript externo.

  Por exemplo, para alterar a cor de um elemento:

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* Configure um estilo em linha ou um link para uma folha de estilos externa.

  Por exemplo, para definir uma classe para um elemento de sobreposição:

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### Práticas recomendadas do código personalizado {#custom-code-best-practices}

+++ **Sempre envolva o código personalizado em um elemento.**

Por exemplo:

```
<script>
// Code goes here
</script>
```

Caso alguma modificação seja necessária, faça alterações dentro desse contêiner.

Se você não precisar mais do código personalizado, basta deixar este container vazio, mas não o remova. Isso garante que outras modificações na experiência não sejam afetadas.

+++

+++ **Não execute ações document.write em scripts de código personalizados.**

Os scripts são executados de modo assíncrono. Isso frequentemente faz com que as ações document.write apareçam no lugar errado na página. Não é recomendado usar document.write em scripts criados no código personalizado.

+++

+++ **Se você criar um elemento e depois modificá-lo, não exclua o elemento original.**

Cada alteração cria um novo elemento na variável **[!UICONTROL Modificações]** painel. Como a segunda ação modifica o Elemento 1, se você o excluir, essa ação não terá mais nada para modificar, e a alteração não funcionará mais.

+++

+++ **Tenha cuidado ao usar o**[!UICONTROL  Página `<head>`]**tipo de modificação para duas campanhas que afetam o mesmo URL.**

Se você usar o **[!UICONTROL Página`<head>`]** Tipo de modificação para duas campanhas que afetam o mesmo URL, o JavaScript é inserido na página de ambas as campanhas. [!DNL Journey Optimizer] determina automaticamente a ordem do conteúdo entregue. Certifique-se de que o código não dependa da disposição. Cabe a você garantir que não haja conflitos no código.

+++
