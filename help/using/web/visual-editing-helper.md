---
title: Extensão Auxiliar de edição visual
description: Descubra a extensão Chrome do Auxiliar de edição visual que permite criar e visualizar páginas da Web no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 18%

---

# Extensão Auxiliar de edição visual {#visual-editing-helper}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao canal Web](get-started-web.md)
* [Criação de experiências da Web](create-web.md)
* [Páginas da Web de autor](author-web.md)
* **[Extensão Auxiliar de edição visual](visual-editing-helper.md)**
* [Relatórios da Web](web-report.md)

>[!ENDSHADEBOX]

Para criar e visualizar rapidamente suas experiências na web, a extensão de navegador da Adobe Experience Cloud para o Google Chrome, Auxiliar de edição visual, permite carregar sites de maneira confiável no Adobe [!DNL Journey Optimizer] web designer.

## Instalar a extensão Auxiliar de edição visual {#install-visual-editing-helper}

Para obter e instalar a extensão de navegador Auxiliar de edição visual, siga as etapas abaixo.

1. Na loja da Web do Google Chrome, navegue até a [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensão do navegador.

1. Clique em **[!UICONTROL Adicionar ao Chrome]** > **[!UICONTROL Adicionar extensão]**.

1. Criar uma campanha de canal da Web no [!DNL Journey Optimizer]. [Saiba como](author-web.md#create-web-campaign)

1. Abra o [!DNL Journey Optimizer] web designer para começar a criar sua experiência na web. [Saiba mais](author-web.md)

1. Certifique-se de que a extensão de navegador Auxiliar de edição visual está ativada na barra de ferramentas do navegador Chrome clicando no ícone correspondente.

   ![](assets/web-visual-editing-extension.png)

O Auxiliar de edição visual do Adobe Experience Cloud agora é ativado automaticamente quando um site é aberto na [!DNL Journey Optimizer] web designer para potencializar a criação.

A extensão não tem configurações condicionais e lida com todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável no [!DNL Journey Optimizer] web designer devido a um dos seguintes motivos:
>
> * O site tem políticas de segurança estritas.
> * O site está em um iframe.
> * O site de controle de qualidade e/ou preparo do cliente não está disponível para partes externas (o site é interno).


## Solução de problemas

Ao usar o Adobe [!DNL Journey Optimizer] web designer, se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale o [Extensão de navegador Auxiliar de edição visual](#install-visual-editing-helper).

Se o SDK da Web do Adobe Experience Platform ainda não estiver implementado no site, uma mensagem será exibida no designer da Web sugerindo que você instale a extensão de navegador Auxiliar de edição visual e implemente a [SDK da Web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}.

Se o site não carregar ou se comportar inesperadamente, uma possível correção é aceitar cookies em seu site no navegador antes de tentar carregá-lo no Adobe [!DNL Journey Optimizer].

Para páginas em autenticação, se a página de logon não for carregada ou se, após tentar fazer logon, você ainda não estiver conectado, tente fazer logon primeiro em uma guia diferente do navegador e carregue o site na Adobe [!DNL Journey Optimizer] web designer.
