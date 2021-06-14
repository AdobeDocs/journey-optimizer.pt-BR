---
title: Importe ou codifique seus emails
description: Saiba como importar conteúdo de email ou codificar seus emails
feature: Visão geral
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 10%

---

# Importar ou codificar conteúdo de email {#existing-content}

![](assets/do-not-localize/badge.png)

O Journey Optimizer permite importar conteúdo HTML existente para criar seus emails. Esse conteúdo pode ser um código HTML ou conteúdo bruto de um arquivo HTML existente ou uma pasta zip.

Para codificar conteúdo HTML ou importar conteúdo existente, siga as etapas abaixo:

1. [Criar uma mensagem](create-message.md)

1. Abra o **[!UICONTROL Email Designer]** da seção **[!UICONTROL Edit Content]**.

   ![](assets/import-html_1.png)

1. Selecione **[!UICONTROL Code your own]** ou **[!UICONTROL Import HTML]**. Consulte as seções abaixo para ver as próximas etapas.

## Codifique seu próprio {#import-raw-html-code}

Use o modo **[!UICONTROL Code your own]** para importar HTML bruto e/ou codificar seu conteúdo de email. Este método requer habilidades HTML.

>[!CAUTION]
>
> Imagens de [Adobe Experience Manager Assets Essentials](assets-essentials.md) não podem ser referenciadas ao usar este método. As imagens referenciadas em seu código HTML devem ser armazenadas em um local público.

1. Na página inicial do Designer de email, selecione **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. Insira ou cole seu código HTML bruto.

1. Use o painel esquerdo para aproveitar os recursos de personalização [!DNL Journey Optimizer]. Para obter mais informações, consulte [esta seção](personalization/personalize.md).

   ![](assets/code-editor.png)

1. Para abrir o Designer de email para iniciar seu email a partir de um novo design, selecione **[!UICONTROL Change your design]** no menu de opções.

   ![](assets/code-editor-change-design.png)

1. Clique no botão **[!UICONTROL Preview]** para verificar o design e a personalização da mensagem usando perfis de teste. Para obter mais informações, consulte [esta seção](preview.md).

   ![](assets/code-editor-preview.png)

1. Quando o código estiver pronto, clique em **[!UICONTROL Save]** e retorne à tela de criação de mensagens para finalizar a mensagem.

   ![](assets/code-editor-save.png)


## Importar HTML {#import-html-content-from-file}

Você pode importar conteúdo HTML no designer de email. Esse conteúdo pode ser:

* Um **arquivo HTML** com uma folha de estilos incorporada,
* Uma **.zip folder** com o arquivo HTML, a folha de estilos (.css) e as imagens.

   >[!NOTE]
   >
   >Não há restrições na estrutura do arquivo .zip. No entanto, as referências devem ser relativas e se encaixar na estrutura de árvore da pasta .zip.

Para importar um arquivo contendo conteúdo HTML, siga as etapas abaixo:

1. Na página inicial do Designer de email, selecione **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. Arraste e solte o arquivo HTML ou .zip que contém seu conteúdo HTML.

1. Depois que o conteúdo HTML for carregado, você poderá aproveitar os recursos do Email Designer para editar e visualizar seu email. [Saiba mais nesta seção](create-email-content.md).

   ![](assets/html-imported.png)
