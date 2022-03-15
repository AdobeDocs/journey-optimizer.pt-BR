---
title: Importe ou codifique seus emails
description: Saiba como importar conteúdo de email ou codificar seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 16%

---

# Importar ou codificar conteúdo de email {#existing-content}

O Journey Optimizer permite importar conteúdo HTML existente para criar seus emails. Esse conteúdo pode ser um código de HTML ou conteúdo bruto de um arquivo de HTML existente ou de uma pasta zip.

➡️ [Descubra este recurso no vídeo](#video)

Para codificar o conteúdo do HTML ou importar o conteúdo existente, siga as etapas abaixo:

1. [Criar uma mensagem](create-message.md)

1. Abra o **[!UICONTROL Email Designer]** do **[!UICONTROL Edit Content]** seção.

   ![](assets/import-html_1.png)

1. Selecione **[!UICONTROL Code your own]** ou **[!UICONTROL Import HTML]**. Consulte as seções abaixo para ver as próximas etapas.

## Codifique seu próprio {#import-raw-html-code}

Use o **[!UICONTROL Code your own]** para importar HTML bruto e/ou codificar o conteúdo do email. Este método requer competências de HTML.

>[!CAUTION]
>
> Imagens de [Adobe Experience Manager Assets Essentials](assets-essentials.md) não pode ser referenciado ao usar este método. As imagens referenciadas no código HTML devem ser armazenadas em um local público.

1. Na página inicial do Designer de email, selecione **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. Insira ou cole seu código de HTML bruto.

1. Usar o painel esquerdo para aproveitar [!DNL Journey Optimizer] recursos de personalização. Para obter mais informações, consulte [esta seção](../personalization/personalize.md).

   ![](assets/code-editor.png)

1. Para abrir o Designer de email para iniciar seu email a partir de um novo design, selecione **[!UICONTROL Change your design]** no menu de opções.

   ![](assets/code-editor-change-design.png)

1. Clique no botão **[!UICONTROL Preview]** para verificar o design e a personalização da mensagem usando perfis de teste. Para obter mais informações, consulte [esta seção](preview.md).

   ![](assets/code-editor-preview.png)

1. Quando o código estiver pronto, clique em **[!UICONTROL Save]** em seguida, volte para a tela de criação de mensagens para finalizar a mensagem.

   ![](assets/code-editor-save.png)

## Importar HTML {#import-html-content-from-file}

É possível importar conteúdo do HTML no designer de email. Esse conteúdo pode ser:

* Um **Arquivo HTML** com uma folha de estilos incorporada,
* A **pasta .zip** com o arquivo HTML, a folha de estilos (.css) e as imagens.

   >[!NOTE]
   >
   >Não há restrições na estrutura do arquivo .zip. No entanto, as referências devem ser relativas e se encaixar na estrutura de árvore da pasta .zip.

Para importar um arquivo contendo conteúdo de HTML, siga as etapas abaixo:

1. Na página inicial do Designer de email, selecione **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. Arraste e solte o HTML ou arquivo .zip contendo o conteúdo do HTML.

1. Depois que o conteúdo do HTML for carregado, você poderá aproveitar os recursos do Email Designer para editar e visualizar seu email. [Saiba mais nesta seção](create-email-content.md).

   ![](assets/html-imported.png)

## Vídeo tutorial {#video}

Saiba como importar conteúdo HTML existente, ajustar o design, adicionar mirror page e links para cancelar a inscrição e como codificar seu conteúdo.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
