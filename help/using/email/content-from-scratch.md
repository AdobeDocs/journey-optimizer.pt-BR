---
solution: Journey Optimizer
product: journey optimizer
title: Criar emails no Journey Optimizer
description: Saiba como criar seu conteúdo de e-mails do zero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: conteúdo, editor, email, iniciar
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# Iniciar do zero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Sobre componentes da estrutura"
>abstract="Os componentes da estrutura definem o layout do email."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Sobre componentes da estrutura"
>abstract="Componentes da estrutura definem o layout da landing page."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Sobre componentes da estrutura"
>abstract="Componentes da estrutura definem o layout do fragmento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Sobre componentes da estrutura"
>abstract="Componentes da estrutura definem o layout do modelo."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definição de colunas de email"
>abstract="O Designer de email permite definir facilmente o layout do email definindo a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definição de colunas de página de aterrissagem"
>abstract="O Designer de email permite definir facilmente o layout da página de aterrissagem definindo a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definição das colunas do fragmento"
>abstract="O Designer de email permite definir facilmente o layout do fragmento definindo a estrutura da coluna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definição de colunas de modelo"
>abstract="O Designer de email permite definir facilmente o layout do modelo definindo a estrutura da coluna."


O Designer de email permite que você defina facilmente a estrutura do seu email. Ao adicionar e mover elementos estruturais com ações simples de arrastar e soltar, você pode projetar a forma do seu email em segundos.

Para começar a criar seu conteúdo de email, siga as etapas abaixo:

1. Na página inicial do Designer de email, selecione o **[!UICONTROL Design do zero]** opção.

   ![](assets/email_designer.png)

1. Comece a criar o conteúdo de email arrastando e soltando **[!UICONTROL Componentes da estrutura]** na tela para definir o layout do email.

   >[!NOTE]
   >
   >O empilhamento de colunas não é compatível com todos os programas de email. Quando não houver suporte, as colunas não serão empilhadas.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Adicionar quantos **[!UICONTROL Componentes da estrutura]** conforme necessário, e edite suas configurações no painel dedicado à direita.

   ![](assets/email_designer_structure_components.png)

   Selecione o **[!UICONTROL coluna n:n]** para definir o número de colunas de sua escolha (entre 3 e 10). Você também pode definir a largura de cada coluna, movendo as setas na parte inferior de cada coluna.

   >[!NOTE]
   >
   >Cada tamanho de coluna não pode estar abaixo de 10% da largura total do componente de estrutura. Não é possível remover uma coluna que não esteja vazia.

1. No **[!UICONTROL Componentes de conteúdo]** , adicione quantos elementos forem necessários em um ou mais componentes de estrutura. [Saiba mais sobre componentes de conteúdo](content-components.md)

1. Cada componente pode ser personalizado ainda mais usando o **[!UICONTROL Configurações]** ou **[!UICONTROL Estilo]** no menu à direita. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. No **[!UICONTROL Seletor de ativos]**, é possível selecionar diretamente ativos armazenados no **[!UICONTROL Biblioteca de ativos]**. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md)

   Clique duas vezes na pasta que contém seus ativos. Arraste e solte-os em um componente de estrutura.

   ![](assets/email_designer_asset_picker.png)

1. Insira campos de personalização para personalizar seu conteúdo de email a partir de dados de perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Clique em **[!UICONTROL Ativar conteúdo de condição]** para adicionar conteúdo dinâmico e adaptar o conteúdo aos perfis segmentados com base em regras condicionais. [Introdução ao conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Clique no botão **[!UICONTROL Links]** no painel esquerdo para exibir todos os URLs do seu conteúdo que serão rastreados. Você pode modificar as **[!UICONTROL Tipo de rastreamento]** ou **[!UICONTROL Rótulo]** e adicionar **[!UICONTROL Tags]** se necessário. [Saiba mais sobre links e rastreamento de mensagens](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Você pode personalizar ainda mais seu email clicando em **[!UICONTROL Alternar para editor de código]** no menu avançado. [Saiba mais sobre o editor de código](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >Não será possível reverter para o designer visual desse email após alternar para o editor de códigos.

1. Quando o conteúdo estiver pronto, clique em **[!UICONTROL Simular conteúdo]** para verificar a renderização de email. Você pode escolher a área de trabalho ou exibição móvel. [Saiba mais sobre como visualizar seu email](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Quando o email estiver pronto, clique em **[!UICONTROL Salvar]**.

