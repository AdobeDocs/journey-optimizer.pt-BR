---
solution: Journey Optimizer
product: journey optimizer
title: Criar conteúdo do zero no Journey Optimizer
description: Saiba como criar o conteúdo do zero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: conteúdo, editor, email, iniciar
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 6%

---

# Crie um conteúdo do zero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do email. Arraste e solte uma **Estrutura** na tela para iniciar a criação do conteúdo de email."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout da página de destino. Arraste e solte uma **Estrutura** na tela para começar a projetar o conteúdo da página de aterrissagem."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do fragmento. Arraste e solte uma **Estrutura** na tela para começar a projetar o conteúdo do fragmento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do modelo. Arraste e solte uma **Estrutura** na tela para começar a projetar o conteúdo do modelo."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definir colunas de email"
>abstract="O Designer de email permite definir facilmente o layout do email selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definir colunas de página de aterrissagem"
>abstract="O Designer permite definir facilmente o layout da landing page selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definir colunas de fragmento"
>abstract="O Designer permite definir facilmente o layout do fragmento selecionando a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definir colunas de modelo"
>abstract="O Designer permite definir facilmente o layout do modelo, selecionando a estrutura da coluna."


Use o Adobe Journey Optimizer Designer para definir facilmente a estrutura do seu conteúdo. Ao adicionar e mover elementos estruturais com ações simples de arrastar e soltar, você pode projetar a forma do seu conteúdo em segundos.

Para começar a criar seu conteúdo, siga as etapas abaixo:

1. Na página inicial do Designer, selecione o **[!UICONTROL Design do zero]** opção.

   ![](assets/email_designer.png)

1. Inicie a criação de conteúdo arrastando e soltando **[!UICONTROL Estruturas]** na tela para definir o layout do email.

   >[!NOTE]
   >
   >O empilhamento de colunas não é compatível com todos os programas de email. Quando não houver suporte, as colunas não serão empilhadas.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Adicionar quantos **[!UICONTROL Estruturas]** conforme necessário, e edite suas configurações no painel dedicado à direita.

   ![](assets/email_designer_structure_components.png)

   Selecione o **[!UICONTROL coluna n:n]** para definir o número de colunas de sua escolha (entre 3 e 10). Você também pode definir a largura de cada coluna, movendo as setas na parte inferior de cada coluna.

   >[!NOTE]
   >
   >Cada tamanho de coluna não pode estar abaixo de 10% da largura total do componente de estrutura. Não é possível remover uma coluna que não esteja vazia.

1. Expanda o **[!UICONTROL Conteúdo]** e adicione quantos elementos forem necessários em um ou mais componentes de estrutura. [Saiba mais sobre componentes de conteúdo](content-components.md)

1. Cada componente pode ser personalizado ainda mais usando o **[!UICONTROL Configurações]** ou **[!UICONTROL Estilo]** no menu à direita. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. No **[!UICONTROL Seletor de ativos]**, é possível selecionar diretamente ativos armazenados no **[!UICONTROL Biblioteca de ativos]**. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md)

   Clique duas vezes na pasta que contém seus ativos. Arraste e solte-os em um componente de estrutura.

   ![](assets/email_designer_asset_picker.png)

1. Insira campos de personalização para personalizar o conteúdo de atributos de perfis, associações de segmentos, atributos contextuais e muito mais. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Clique em **[!UICONTROL Ativar conteúdo de condição]** para adicionar conteúdo dinâmico e adaptar o conteúdo aos perfis segmentados com base em regras condicionais. [Introdução ao conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Clique no botão **[!UICONTROL Links]** no painel esquerdo para exibir todos os URLs do seu conteúdo que serão rastreados. Você pode modificar as **[!UICONTROL Tipo de rastreamento]** ou **[!UICONTROL Rótulo]** e adicionar **[!UICONTROL Tags]** se necessário. [Saiba mais sobre links e rastreamento](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Se necessário, você pode personalizar ainda mais seu email clicando em **[!UICONTROL Alternar para editor de código]** no menu avançado. Isso permite editar o código-fonte do email, por exemplo, para adicionar rastreamento ou tags de HTML personalizadas. [Saiba mais sobre o editor de código](code-content.md)

   >[!CAUTION]
   >
   >Não é possível reverter para o designer visual desse email após alternar para o editor de código.

1. Quando o conteúdo estiver pronto, clique no botão **[!UICONTROL Simular conteúdo]** para verificar a renderização. Você pode escolher a área de trabalho ou exibição móvel. [Saiba mais sobre como visualizar seu email](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Quando o conteúdo estiver pronto, clique em **[!UICONTROL Salvar]**.

