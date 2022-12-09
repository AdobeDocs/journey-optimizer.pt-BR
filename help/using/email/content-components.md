---
solution: Journey Optimizer
product: journey optimizer
title: Usar componentes de conteúdo do designer de email
description: Saiba como usar componentes de conteúdo em seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 0%

---

# Usar os componentes de conteúdo do Email Designer {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Sobre componentes de conteúdo"
>abstract="Os componentes do conteúdo são espaços reservados para o conteúdo vazio que podem ser usados para criar o layout de um email."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Sobre componentes de conteúdo"
>abstract="Os componentes do conteúdo são espaços reservados vazios para o conteúdo que você pode usar para criar o layout de uma página de aterrissagem."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Sobre componentes de conteúdo"
>abstract="Os componentes do conteúdo são espaços reservados vazios para o conteúdo que você pode usar para criar o layout de um fragmento."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Sobre componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados para o conteúdo vazio que podem ser usados para criar o layout de um modelo."

Ao criar o conteúdo do email, **[!UICONTROL Content components]** O permite personalizar ainda mais o email com componentes brutos que podem ser editados depois de colocados no email.

Você pode adicionar quantos componentes de conteúdo forem necessários dentro de um ou mais componentes de estrutura, que definem o layout do email.

## Adicionar componentes de conteúdo {#add-content-components}

Para adicionar componentes de conteúdo ao seu email e ajustá-los às suas necessidades, siga as etapas abaixo.

1. No Designer de email, use um conteúdo existente ou arraste e solte **[!UICONTROL Structure components]** no conteúdo vazio para definir o layout do email. [Saiba como](content-from-scratch.md)

1. Para acessar o **[!UICONTROL Content components]** selecione o botão correspondente no painel esquerdo do Designer de email.

   ![](assets/email_designer_content_components.png)

1. Arraste e solte os componentes de conteúdo de sua escolha dentro dos componentes de estrutura relevantes.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >É possível adicionar vários componentes em um único componente de estrutura e em cada coluna de um componente de estrutura.

1. Ajuste os atributos de estilo para cada componente usando o **[!UICONTROL Component settings]** painel à direita. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Contêiner {#container}

Você pode adicionar um contêiner simples dentro do qual poderá adicionar outro componente de conteúdo. Isso permite aplicar um estilo específico ao contêiner, que será diferente do componente usado no .

Por exemplo, adicione uma **[!UICONTROL Container]** e, em seguida, adicione um [Botão](#button) componente dentro desse contêiner. Você pode usar um plano de fundo específico para o contêiner e outro para o botão .

![](assets/email_designer_container_component.png)

## Botão {#button}

Use o **[!UICONTROL Button]** para inserir um ou vários botões no email e redirecionar o público do email para outra página.

1. De **[!UICONTROL Content components]**, arraste e solte a **[!UICONTROL Button]** em um **[!UICONTROL Structure component]**.

1. Clique no botão recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Components settings]** no painel direito do Email Designer.

   ![](assets/email_designer_button_component.png)

1. No **[!UICONTROL Link]** adicione o URL para o qual deseja redirecionar ao clicar no botão .

1. Escolha como seu público será redirecionado com o **[!UICONTROL Target]** lista suspensa:

   * **[!UICONTROL None]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Blank]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Self]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Parent]**: abre o link no quadro principal.
   * **[!UICONTROL Top]**: abre o link no corpo completo da janela.

   ![](assets/email_designer_button_link.png)

1. Você pode personalizar ainda mais seu botão alterando atributos de estilo como **[!UICONTROL Border]**, **[!UICONTROL Size]**, **[!UICONTROL Margin]**, etc. do **[!UICONTROL Component settings]** painel.

## Texto {#text}

Use o **[!UICONTROL Text]** componente para inserir texto no email e ajustar o estilo (borda, tamanho, preenchimento etc.) usando o **[!UICONTROL Component settings]** painel.

![](assets/email_designer_text_component.png)

1. De **[!UICONTROL Content components]**, arraste e solte a **[!UICONTROL Text]** em um **[!UICONTROL Structure component]**.

1. Clique no componente recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Components Settings]** no painel direito do Designer de email.

1. Altere o texto com as seguintes opções disponíveis na barra de ferramentas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: aplique negrito, itálico, sublinhado ou riscado ao seu texto.
   * **Alterar alinhamento**: escolha entre alinhamento esquerdo, direito, central ou justificado para o texto.
   * **[!UICONTROL Create list]**: adicione marcadores ou listas de números ao texto.
   * **[!UICONTROL Set heading]**: adicione até seis níveis de cabeçalho ao texto.
   * **Tamanho da fonte**: selecione o tamanho da fonte do texto em pixels.
   * **[!UICONTROL Edit image]**: adicione uma imagem ou um ativo ao seu componente de texto. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md)
   * **[!UICONTROL Show the source code]**: exibir o código-fonte do texto. Ele não pode ser modificado.
   * **[!UICONTROL Duplicate]**: adicione uma cópia do seu componente de texto.
   * **[!UICONTROL Delete]**: exclua o componente de texto selecionado do seu email.
   * **[!UICONTROL Add personalization]**: adicione campos de personalização para personalizar o conteúdo dos dados de seus perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)
   * **[!UICONTROL Enable conditional content]**: adicione conteúdo condicional para adaptar o conteúdo do componente aos perfis segmentados. [Saiba mais sobre conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

1. Ajuste os outros atributos de estilo, como cor do texto, família da fonte, borda, preenchimento, margem etc. do **[!UICONTROL Component settings]** painel.

## Divisor {#divider}

Use o **[!UICONTROL Divider]** para inserir uma linha divisória para organizar o layout e o conteúdo do seu email.

É possível ajustar atributos de estilo, como cor da linha, estilo e altura da **[!UICONTROL Component settings]** painel.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Use o **[!UICONTROL HTML]** componente para copiar e colar as diferentes partes do seu HTML existente. Isso permite que você crie componentes HTML modulares gratuitos para reutilizar algum conteúdo externo.

1. De **[!UICONTROL Content Components]**, arraste e solte a **[!UICONTROL HTML]** em um **[!UICONTROL Structure component]**.

1. Clique no componente recém-adicionado e selecione **[!UICONTROL Show the source code]** na barra de ferramentas contextual para adicionar seu HTML.

   ![](assets/email_designer_html_component.png)

1. Copie e cole o código HTML que deseja adicionar ao seu email e clique em **[!UICONTROL Save]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Para simplesmente tornar um conteúdo externo compatível com o Designer de email, a Adobe recomenda criar uma mensagem do zero e copiar o conteúdo do email existente para componentes.

## Imagem {#image}

Use o **[!UICONTROL Image]** componente para inserir um arquivo de imagem de seu computador no conteúdo do email.

1. De **[!UICONTROL Content components]**, arraste e solte a **[!UICONTROL Image]** em um **[!UICONTROL Structure component]**.

1. Clique em **[!UICONTROL Browse]** para escolher um arquivo de imagem de seus ativos.

   Para saber mais sobre [!DNL Assets Essentials], consulte [Documentação do Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Clique no componente recém-adicionado e configure as propriedades da imagem usando o **[!UICONTROL Components settings]** painel:

   * **[!UICONTROL Image title]** permite definir um título para a imagem.
   * **[!UICONTROL Alt text]** permite definir a legenda vinculada à imagem. Isso corresponde ao atributo HTML alternativo.

   ![](assets/email_designer_10.png)

1. Ajuste os outros atributos de estilo, como margem, borda etc. ou adicionar um link para redirecionar seu público para outro conteúdo do **[!UICONTROL Component settings]** painel.

## Vídeo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Configurações de vídeo"
>abstract="Use esse componente para inserir um vídeo no seu email. Observe que os vídeos não funcionam em todos os clientes de email. Recomendamos definir uma imagem de fallback."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Configurações de vídeo"
>abstract="Use esse componente para inserir um vídeo na página de aterrissagem. Observe que os vídeos não funcionam em todos os clientes de mensagem. Recomendamos definir uma imagem de fallback."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Configurações de vídeo"
>abstract="Use esse componente para inserir um vídeo no fragmento. Observe que os vídeos não funcionam em todos os clientes de mensagem. Recomendamos definir uma imagem de fallback."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Configurações de vídeo"
>abstract="Use esse componente para inserir um vídeo no modelo. Observe que os vídeos não funcionam em todos os clientes de mensagem. Recomendamos definir uma imagem de fallback."

Use o **[!UICONTROL Video]** para inserir um vídeo no seu conteúdo de email por meio de um link de URL.

1. De **[!UICONTROL Content Components]**, arraste e solte a **[!UICONTROL Video]** componente em um **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Clique no componente recém-adicionado.

1. No **[!UICONTROL Video link]** do **[!UICONTROL Components settings]** adicione o URL do vídeo.

   ![](assets/email_designer_18.png)

1. Você pode adicionar uma **[!UICONTROL Poster image]** ao vídeo para especificar uma imagem a ser exibida até o público clicar no botão Reproduzir.

1. Ajuste os outros atributos de estilo, como estilo, margem, borda etc. do **[!UICONTROL Component settings]** painel.

## Social {#social}

Use o **[!UICONTROL Social]** componente para inserir links às páginas de mídia social no seu conteúdo de email.

1. De **[!UICONTROL Content Components]**, arraste e solte a **[!UICONTROL Social]** em um **[!UICONTROL Structure component]**.

1. Clique no componente recém-adicionado.

1. No **[!UICONTROL Social]** do **[!UICONTROL Components settings]** escolha que mídia social deseja adicionar ou remover.

   ![](assets/email_designer_20.png)

1. Escolha o tamanho dos ícones no campo dedicado.

1. Clique em cada um dos ícones de redes sociais para configurar o **[!UICONTROL URL]** para o qual o público-alvo será redirecionado.

   ![](assets/email_designer_21.png)

1. Você também pode alterar os ícones de cada uma das redes sociais, se necessário, na variável **[!UICONTROL Image]** campo.

1. Ajuste os outros atributos de estilo, como estilo, margem, borda etc. do **[!UICONTROL Component settings]** painel.

## Decisão da oferta {#offer-decision}

Use o **[!UICONTROL Offer decision]** componente para inserir ofertas em suas mensagens. O [gestão de decisões](../offers/get-started/starting-offer-decisioning.md) O mecanismo escolherá a melhor oferta a ser entregue aos clientes.

Saiba como adicionar ofertas personalizadas a um email em [esta seção](add-offers-email.md).

