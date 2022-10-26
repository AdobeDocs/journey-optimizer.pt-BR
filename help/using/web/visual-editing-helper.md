---
title: Extensão Auxiliar de edição visual
description: Descubra a extensão do Visual Editing Helper Chrome que permite criar e visualizar páginas da Web no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 14%

---

# Extensão Auxiliar de edição visual {#visual-editing-helper}

Para criar e visualizar rapidamente suas experiências da Web, a extensão do navegador Adobe Experience Cloud Visual Editing Helper para Google Chrome permite carregar sites de maneira confiável no Adobe. [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>O recurso de canal da Web está disponível no momento como um beta somente para usuários selecionados.

## Instalar a extensão do Visual Editing Helper {#install-visual-editing-helper}

Para obter e instalar a extensão do navegador do Visual Editing Helper, siga as etapas abaixo.

1. Na Google Chrome Web Store, navegue até o [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca)Extensão do navegador {target=&quot;_blank&quot;}.

1. Clique em **[!UICONTROL Adicionar ao Chrome]** > **[!UICONTROL Adicionar extensão]**.

1. Crie uma campanha de canal da Web em [!DNL Journey Optimizer]. [Saiba como](author-web.md#create-web-campaign)

1. Abra o [!DNL Journey Optimizer] web designer para começar a criar sua experiência na web. [Saiba mais](author-web.md)

1. Certifique-se de que a extensão do navegador do Visual Editing Helper está ativada na barra de ferramentas do navegador Chrome clicando no ícone correspondente.

   ![](assets/web-visual-editing-extension.png)

O Adobe Experience Cloud Visual Editing Helper agora é ativado automaticamente quando um site é aberto no [!DNL Journey Optimizer] web designer para criação de energia.

A extensão não tem configurações condicionais e trata todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável na [!DNL Journey Optimizer] web designer por um dos seguintes motivos:
>
> * O site tem políticas de segurança estritas.
> * O site está em um iframe.
> * O site de controle de qualidade e/ou preparo do cliente não está disponível para partes externas (o site é interno).


## Solução de problemas

Ao usar o Adobe [!DNL Journey Optimizer] web designer, se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale o [Extensão do navegador do Visual Editing Helper](#install-visual-editing-helper).

Se o SDK da Web da Adobe Experience Platform ainda não estiver implementado no site, uma mensagem será exibida no web designer sugerindo que você instale a extensão do navegador do Visual Editing Helper e implemente o [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target=&quot;_blank&quot;}.

Se o site não carregar ou se comportar inesperadamente, uma possível correção é aceitar cookies em seu site no navegador antes de tentar carregá-los no Adobe [!DNL Journey Optimizer].

Para páginas sob autenticação, se a página de logon não carregar ou se, depois de tentar fazer logon, você ainda não estiver conectado, tente fazer logon primeiro em uma guia diferente do navegador e, em seguida, carregar o site no Adobe [!DNL Journey Optimizer] web designer.
