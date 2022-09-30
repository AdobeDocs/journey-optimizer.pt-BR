---
title: Usar componentes de conteúdo do designer de email
description: Saiba como usar componentes de conteúdo em seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 1%

---

# Usar os componentes de conteúdo do Designer de email {#content-components}

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


Ao criar seu conteúdo de email do zero, **[!UICONTROL Componentes de conteúdo]** O permite personalizar ainda mais seu email com componentes brutos e vazios que podem ser usados depois de colocados no email.
Você pode adicionar quantos **[!UICONTROL Componentes de conteúdo]** conforme necessário dentro de um **[!UICONTROL Componente Estrutura]** que define o layout do email.

## Botão {#buttons}

Use o **[!UICONTROL Botão]** para inserir vários botões no email e redirecionar o público de email para outra página.

1. De **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL Botão]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_13.png)

1. Clique no botão recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Configurações de componentes]** no painel direito do designer de email.

   ![](assets/email_designer_14.png)

1. No **[!UICONTROL Link]** do **[!UICONTROL Configurações de componentes]**, adicione o URL para o qual você deseja que o público-alvo seja redirecionado ao clicar no botão .

1. Escolha como seu público será redirecionado com o **[!UICONTROL Target]** lista suspensa:

   * **[!UICONTROL Nenhum]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Em branco]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Auto]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Pai]**: abre o link no quadro principal.
   * **[!UICONTROL Topo]**: abre o link no corpo completo da janela.

   ![](assets/email_designer_15.png)

1. Agora você pode personalizar ainda mais seu botão, alterando o **[!UICONTROL Estilo]**, **[!UICONTROL Margem]** e **[!UICONTROL Borda]** por exemplo.

## Texto {#text}

Use o **[!UICONTROL Texto]** componente para inserir texto no email. É possível ajustar a cor, o estilo e o tamanho do texto em **[!UICONTROL Configurações do componente]**.

1. Em **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL Texto]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_11.png)

1. Clique no componente recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Configurações de componentes]** no painel direito do designer de email.

1. Altere o texto com as seguintes opções disponíveis na barra de ferramentas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Alterar estilo do texto]**: aplique negrito, itálico, sublinhado ou riscado ao seu texto.
   * **Alterar alinhamento**: escolha entre alinhamento esquerdo, direito, central ou justificado para o texto.
   * **[!UICONTROL Criar lista]**: adicione marcadores ou listas de números ao texto.
   * **[!UICONTROL Definir cabeçalho]**: adicione até seis níveis de cabeçalho ao texto.
   * **Tamanho da fonte**: selecione o tamanho da fonte do texto em pixels.
   * **[!UICONTROL Editar imagem]**: adicione uma imagem ou um ativo ao seu componente de texto. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md).
   * **[!UICONTROL Mostrar o código-fonte]**: exibir o código-fonte do texto. Ele não pode ser modificado.
   * **[!UICONTROL Duplicar]**: adicione uma cópia do seu componente de texto.
   * **[!UICONTROL Excluir]**: exclua o componente de texto selecionado do seu email.
   * **[!UICONTROL Adicionar personalização]**: adicione campos de personalização para personalizar o conteúdo dos dados de seus perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md).
   * **[!UICONTROL Habilitar conteúdo condicional]**: adicione conteúdo condicional para adaptar o conteúdo do componente aos perfis segmentados. [Saiba mais sobre conteúdo dinâmico](../personalization/get-started-dynamic-content.md).

1. Ajuste o **[!UICONTROL Cor do texto]**, **[!UICONTROL Família de fontes]** e **[!UICONTROL Tamanho]** no **[!UICONTROL Configurações de componentes]**.

   ![](assets/email_designer_12.png)

## Divisor {#divider}

Use o **[!UICONTROL Divisor]** para inserir uma linha divisória para organizar o layout e o conteúdo do seu email.
Você pode selecionar a cor, o estilo e o tamanho da linha de quebra em **[!UICONTROL Configurações do componente]**.

![](assets/email_designer_16.png)

## HTML {#HTML}

Use o **[!UICONTROL HTML]** para copiar e colar as diferentes partes do HTML existente. Isso permite criar componentes HTML modulares gratuitos.

Para simplesmente tornar um conteúdo externo compatível com o Designer de email, o Adobe recomenda criar uma mensagem do zero e copiar o conteúdo do email existente para componentes.

1. Em **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL HTML]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_22.png)

1. Clique no componente recém-adicionado e **[!UICONTROL Mostrar o código-fonte]** para adicionar o HTML.

   ![](assets/email_designer_23.png)

1. Copie e cole o código do HTML que deseja adicionar ao seu email e clique em **[!UICONTROL Salvar]**.

1. Agora você pode personalizar ainda mais seu HTML alterando o **[!UICONTROL Estilo]**, **[!UICONTROL Margem]** e **[!UICONTROL Borda]** por exemplo, ou adicionar um link para redirecionar seu público para outro conteúdo.

## Imagem {#image}

Use o **[!UICONTROL Imagem]** componente para inserir um arquivo de imagem de seu computador no email.

1. Em **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL Imagem]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_9.png)

1. Clique em **[!UICONTROL Procurar]** para escolher um arquivo de imagem de seus ativos.

   Para saber mais sobre [!DNL Assets Essentials], consulte [Documentação do Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Clique no componente recém-adicionado para começar a configurar **[!UICONTROL Componentes de conteúdo]** e ter acesso ao **[!UICONTROL Configurações de componentes]** no painel direito do designer de email.

1. Configure suas propriedades da imagem:

   * **[!UICONTROL Título da imagem]** permite definir um título para a imagem.
   * **[!UICONTROL Texto alternativo]** permite definir a legenda vinculada à imagem. Isso corresponde ao atributo HTML alt.

   ![](assets/email_designer_10.png)

1. Agora você pode personalizar ainda mais sua imagem, alterando o **[!UICONTROL Estilo]**, **[!UICONTROL Margem]** e **[!UICONTROL Borda]** por exemplo, ou adicionar um link para redirecionar seu público para outro conteúdo.

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

Use o **[!UICONTROL Vídeo]** para inserir um vídeo no seu email por meio de um link de URL.

1. Em **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL Vídeo]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_17.png)

1. Clique no componente recém-adicionado para começar a configurar **[!UICONTROL Componentes de conteúdo]** e ter acesso ao **[!UICONTROL Configurações de componentes]** no painel direito do designer de email.

1. No **[!UICONTROL Link de vídeo]** do **[!UICONTROL Configurações de componentes]**, adicione o URL do vídeo.

   ![](assets/email_designer_18.png)

1. Você pode adicionar uma **[!UICONTROL Imagem do cartaz]** ao vídeo para especificar uma imagem a ser exibida até o público clicar no botão Reproduzir.

1. Agora você pode personalizar ainda mais sua imagem, alterando o **[!UICONTROL Estilo]**, **[!UICONTROL Margem]** e **[!UICONTROL Borda]** por exemplo.

## Social {#social}

Use o **[!UICONTROL Social]** para inserir links às páginas de mídia social no seu email.

1. Em **[!UICONTROL Componentes de conteúdo]**, arrastar e soltar **[!UICONTROL Social]** em **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_19.png)

1. Clique no componente recém-adicionado para começar a configurar **[!UICONTROL Componentes de conteúdo]** e ter acesso ao **[!UICONTROL Configurações de componentes]** no painel direito do designer de email.

1. No **[!UICONTROL Social]** do **[!UICONTROL Configurações de componentes]**, escolha que mídia social deseja adicionar ou remover.

   ![](assets/email_designer_20.png)

1. Escolha o tamanho dos ícones no **[!UICONTROL Tamanho das imagens]** campo.

1. Clique em cada um dos ícones de redes sociais para configurar o **[!UICONTROL URL]** para o qual o público-alvo será redirecionado.

   ![](assets/email_designer_21.png)

1. Você também pode alterar os ícones de cada uma das redes sociais, se necessário, na variável **[!UICONTROL Imagem]** campo.

1. Agora você pode personalizar ainda mais seus ícones de redes sociais alterando o **[!UICONTROL Estilo]**, **[!UICONTROL Margem]** e **[!UICONTROL Borda]**.

## Decisão da oferta {#offer-decision}

Use o **[!UICONTROL Decisão da oferta]** componente para inserir decisões (anteriormente conhecido como atividades de oferta) em suas mensagens. As decisões aproveitarão o Gerenciamento de decisões para escolher a melhor oferta a ser entregue aos clientes.

Tópicos relacionados:

* [Introdução à Gestão de decisões](../offers/get-started/starting-offer-decisioning.md)
* [Adicionar ofertas personalizadas aos emails](deliver-personalized-offers.md)
