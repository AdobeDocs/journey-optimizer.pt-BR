---
title: Usar componentes de conteúdo do designer de email
description: Saiba como usar componentes de conteúdo em seus emails
feature: Visão geral
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 2%

---

# Usar os componentes de conteúdo do Designer de email {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="Sobre componentes de conteúdo"
>abstract="Os componentes do conteúdo são espaços reservados para o conteúdo vazio que podem ser usados para criar o layout de um email."


Ao criar o conteúdo de email do zero, **[!UICONTROL Content components]** permite personalizar ainda mais o email com componentes brutos e vazios que podem ser usados depois de colocados no email.
Você pode adicionar quantos **[!UICONTROL Content components]** forem necessários dentro de um **[!UICONTROL Structure component]** que define o layout do email.

## Botão {#buttons}

Use o componente **[!UICONTROL Button]** para inserir vários botões no email e redirecionar o público do email para outra página.

1. A partir de **[!UICONTROL Content components]**, arraste e solte **[!UICONTROL Button]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_13.png)

1. Clique no botão recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do designer de email.

   ![](assets/email_designer_14.png)

1. No campo **[!UICONTROL Link]** do **[!UICONTROL Components Settings]**, adicione o URL ao qual deseja que o público-alvo seja redirecionado ao clicar no botão .

1. Escolha como seu público será redirecionado com o menu suspenso **[!UICONTROL Target]**:

   * **[!UICONTROL None]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Blank]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Self]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Parent]**: abre o link no quadro principal.
   * **[!UICONTROL Top]**: abre o link no corpo completo da janela.

   ![](assets/email_designer_15.png)

1. Agora você pode personalizar ainda mais seu botão alterando **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** por exemplo.

## Texto {#text}

Use o componente **[!UICONTROL Text]** para inserir texto no seu email. Você pode ajustar a cor, o estilo e o tamanho do texto em **[!UICONTROL Component Settings]**.

1. Em **[!UICONTROL Content Components]**, arraste e solte **[!UICONTROL Text]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_11.png)

1. Clique no componente recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do designer de email.

1. Altere o texto com as seguintes opções disponíveis na barra de ferramentas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: aplique negrito, itálico, sublinhado ou riscado ao seu texto.
   * **Alterar alinhamento**: escolha entre alinhamento esquerdo, direito, central ou justificado para o texto.
   * **[!UICONTROL Create list]**: adicione marcadores ou listas de números ao texto.
   * **[!UICONTROL Set heading]**: adicione até seis níveis de cabeçalho ao texto.
   * **Tamanho** da fonte: selecione o tamanho da fonte do texto em pixels.
   * **[!UICONTROL Edit image]**: adicione uma imagem ou um ativo ao seu componente de texto. [Saiba mais sobre o gerenciamento](assets-essentials.md) de ativos.
   * **[!UICONTROL Show the source code]**: exibir o código-fonte do texto. Ele não pode ser modificado.
   * **[!UICONTROL Duplicate]**: adicione uma cópia do seu componente de texto.
   * **[!UICONTROL Delete]**: exclua o componente de texto selecionado do seu email.
   * **[!UICONTROL Add personalization]**: adicione campos de personalização para personalizar o conteúdo dos dados de seus perfis. [Saiba mais sobre a personalização](personalization/personalize.md) de conteúdo.

1. Para obter uma melhor experiência do usuário, você pode adicionar campos de personalização para direcionar seu público-alvo. Para obter mais informações, consulte esta [seção](personalization/personalize.md).

1. Ajuste **[!UICONTROL Text color]**, **[!UICONTROL Font family]** e **[!UICONTROL Size]** no **[!UICONTROL Components Settings]**.

   ![](assets/email_designer_12.png)

## Divisor {#divider}

Use o componente **[!UICONTROL Divider]** para inserir uma linha divisória e organizar o layout e o conteúdo do seu email.
Você pode selecionar a cor, o estilo e o tamanho da linha de quebra em **[!UICONTROL Component Settings]**.

![](assets/email_designer_16.png)

## HTML {#HTML}

Use o **[!UICONTROL HTML]** para copiar e colar as diferentes partes do seu HTML existente. Isso permite criar componentes HTML modulares gratuitos.

Para simplesmente tornar um conteúdo externo compatível com o Designer de email, o Adobe recomenda criar uma mensagem do zero e copiar o conteúdo do email existente para componentes.

1. Em **[!UICONTROL Content Components]**, arraste e solte **[!UICONTROL HTML]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_22.png)

1. Clique no componente recém-adicionado e em **[!UICONTROL Show the source code]** para adicionar o HTML.

   ![](assets/email_designer_23.png)

1. Copie e cole o código HTML que deseja adicionar ao seu email e clique em **[!UICONTROL Save]**.

1. Agora é possível personalizar ainda mais seu HTML alterando **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** por exemplo, ou adicionando um link para redirecionar seu público para outro conteúdo.

## Imagem {#image}

Use o componente **[!UICONTROL Image]** para inserir um arquivo de imagem de seu computador no email.

1. Em **[!UICONTROL Content Components]**, arraste e solte **[!UICONTROL Image]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_9.png)

1. Clique em **[!UICONTROL Browse]** para escolher um arquivo de imagem a partir de seus ativos.

   Para saber mais sobre [!DNL Assets Essentials], consulte a [documentação do Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Clique no componente recém-adicionado para começar a configurar o **[!UICONTROL Content Components]** e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do designer de email.

1. Configure suas propriedades da imagem:

   * **[!UICONTROL Image Title]** permite definir um título para a imagem.
   * **[!UICONTROL Alt text]** permite definir a legenda vinculada à imagem. Isso corresponde ao atributo HTML alternativo.

   ![](assets/email_designer_10.png)

1. Agora é possível personalizar ainda mais sua imagem, alterando **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** por exemplo, ou adicionando um link para redirecionar seu público para outro conteúdo.

## Vídeo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="Configurações de vídeo"
>abstract="Use esse componente para inserir um vídeo no seu email. Observe que os vídeos não funcionam em todos os clientes de email. Recomendamos definir uma imagem de fallback."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="Informações adicionais"

Use o componente **[!UICONTROL Video]** para inserir um vídeo no seu email por meio de um link de URL.

1. Em **[!UICONTROL Content Components]**, arraste e solte **[!UICONTROL Video]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Clique no componente recém-adicionado para começar a configurar o **[!UICONTROL Content Components]** e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do designer de email.

1. No campo **[!UICONTROL Video link]** do **[!UICONTROL Components Settings]**, adicione o URL do vídeo.

   ![](assets/email_designer_18.png)

1. Você pode adicionar um **[!UICONTROL Poster image]** ao vídeo para especificar uma imagem a ser exibida até que o público-alvo clique no botão Reproduzir.

1. Agora você pode personalizar ainda mais sua imagem, alterando **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** por exemplo.

## Social {#social}

Use o componente **[!UICONTROL Social]** para inserir links para páginas de mídia social em seu email.

1. Em **[!UICONTROL Content Components]**, arraste e solte **[!UICONTROL Social]** em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_19.png)

1. Clique no componente recém-adicionado para começar a configurar o **[!UICONTROL Content Components]** e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do designer de email.

1. No campo **[!UICONTROL Social]** do **[!UICONTROL Components Settings]**, escolha a mídia social que deseja adicionar ou remover.

   ![](assets/email_designer_20.png)

1. Escolha o tamanho dos ícones no campo **[!UICONTROL Size of images]**.

1. Clique em cada um dos ícones de redes sociais para configurar o **[!UICONTROL URL]** para o qual o público-alvo será redirecionado.

   ![](assets/email_designer_21.png)

1. Você também pode alterar os ícones de cada mídia social, se necessário, no campo **[!UICONTROL Image]** .

1. Agora você pode personalizar ainda mais seus ícones de redes sociais alterando **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]**.

## Decisão da oferta {#offer-decision}

Use o componente **[!UICONTROL Offer decision]** para inserir decisões (anteriormente conhecido como atividades de oferta) em suas mensagens. As decisões aproveitarão o Gerenciamento de decisões para escolher a melhor oferta a ser entregue aos clientes.

Tópicos relacionados:

* [Introdução ao Gerenciamento de decisão](offers/get-started/starting-offer-decisioning.md).
* [Adicione ofertas personalizadas a mensagens](deliver-personalized-offers.md).

