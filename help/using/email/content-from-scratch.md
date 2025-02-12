---
solution: Journey Optimizer
product: journey optimizer
title: Criar conteúdo do zero no Journey Optimizer
description: Saiba como projetar seu conteúdo do zero
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: conteúdo, editor, email, iniciar
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 54%

---

# Crie um conteúdo do zero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do email. Arraste e solte um componente de **Estrutura** na tela para iniciar a criação do conteúdo de email."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout da página de destino. Arraste e solte um componente de **Estrutura** na tela para começar a criação do conteúdo da página de destino."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do fragmento. Arraste e solte um componente de **Estrutura** na tela para começar a criação do conteúdo do fragmento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do modelo. Arraste e solte um componente de **Estrutura** na tela para começar a criação do conteúdo do modelo."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definir colunas de email"
>abstract="O Designer de email permite definir facilmente o layout do email selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definir as colunas da página de destino"
>abstract="O Designer permite definir facilmente o layout da página de destino selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definir colunas de fragmento"
>abstract="O Designer permite definir facilmente o layout do fragmento selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definir colunas de modelo"
>abstract="O Designer permite definir facilmente o layout do modelo selecionando a estrutura da coluna."


Use o Adobe Journey Optimizer Designer para definir facilmente a estrutura do seu conteúdo. Ao adicionar e mover elementos estruturais com ações simples de arrastar e soltar, você pode projetar a forma do conteúdo em segundos.

Para começar a criar o conteúdo, siga as etapas abaixo:

1. Na página inicial do Designer, selecione a opção **[!UICONTROL Design do zero]**.

   ![](assets/email_designer.png)

1. Comece a criar seu conteúdo arrastando e soltando **[!UICONTROL Estruturas]** na tela para definir o layout do seu email.

   >[!NOTE]
   >
   >O empilhamento de colunas não é compatível com todos os programas de email. Quando não houver suporte, as colunas não serão empilhadas.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Adicione quantas **[!UICONTROL Estruturas]** forem necessárias e edite suas configurações no painel dedicado à direita.

   ![](assets/email_designer_structure_components.png)

   Selecione o componente **[!UICONTROL coluna n:n]** para definir um número de colunas (entre 3 e 10). Você também pode definir a largura de cada coluna movendo as setas na parte inferior de cada coluna.

   >[!NOTE]
   >
   >O tamanho de cada coluna não pode ser inferior a 10% da largura total do componente de estrutura. Não é possível remover uma coluna que não esteja vazia.

1. Expanda a seção **[!UICONTROL Conteúdo]** e adicione quantos elementos forem necessários em um ou mais componentes da estrutura. [Saiba mais sobre componentes de conteúdo](content-components.md)

1. Cada componente pode ser personalizado ainda mais com as guias **[!UICONTROL Configurações]** ou **[!UICONTROL Estilo]** do menu direito. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. No **[!UICONTROL Seletor de ativos]**, você pode selecionar diretamente os ativos armazenados na **[!UICONTROL biblioteca do Assets]**. [Saiba mais sobre o gerenciamento de ativos](../integrations/assets.md)

   Clique duas vezes na pasta que contém seus ativos. Arraste e solte-os em um componente de estrutura.

   ![](assets/email_designer_asset_picker.png)

1. Insira campos de personalização para personalizar seu conteúdo de atributos de perfis, associações de público-alvo, atributos contextuais e muito mais. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Clique em **[!UICONTROL Habilitar conteúdo de condição]** para adicionar conteúdo dinâmico e adaptar o conteúdo aos perfis direcionados com base em regras condicionais. [Introdução ao conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Clique na guia **[!UICONTROL Links]** no painel esquerdo para exibir todas as URLs do seu conteúdo que serão rastreadas. Você pode modificar o **[!UICONTROL Tipo de Rastreamento]** ou o **[!UICONTROL Rótulo]** e adicionar **[!UICONTROL Marcas]**, se necessário. [Saiba mais sobre links e rastreamento](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Se necessário, é possível personalizar ainda mais o email clicando em **[!UICONTROL Alternar para o editor de código]** no menu avançado. Isso permite editar o código-fonte do email, por exemplo, para adicionar rastreamento ou tags de HTML personalizadas. [Saiba mais sobre o editor de código](code-content.md)

   >[!CAUTION]
   >
   >Não é possível reverter para o designer visual desse email após alternar para o editor de código.

1. Quando o conteúdo estiver pronto, clique no botão **[!UICONTROL Simular conteúdo]** para verificar a renderização. Você pode escolher exibir no desktop ou em um dispositivo móvel. Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

   ![](assets/email_designer_simulate_content.png)

1. Quando o conteúdo estiver pronto, clique em **[!UICONTROL Salvar]**.
