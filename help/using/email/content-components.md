---
solution: Journey Optimizer
product: journey optimizer
title: Usar componentes de conteúdo do designer de email
description: Saiba como usar componentes de conteúdo em seus emails
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: componentes, designer de email, editor, email
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 50%

---

# Usar os componentes de conteúdo do Designer de email {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um email."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Sobre os componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de uma página de destino."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Sobre os componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de um fragmento."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um modelo."

Ao criar seu conteúdo de email, os **[!UICONTROL Componentes de conteúdo]** permitem personalizar ainda mais seu email com componentes brutos que podem ser editados depois de colocados no email.

É possível adicionar quantos componentes de conteúdo forem necessários dentro de um ou mais componentes de estrutura, que definem o layout do seu email.

## Adicionar componentes de conteúdo {#add-content-components}

Para adicionar componentes de conteúdo ao seu email e ajustá-los às suas necessidades, siga as etapas abaixo.

1. No Designer de email, use um conteúdo existente ou arraste e solte os **[!UICONTROL Componentes da estrutura]** no conteúdo vazio para definir o layout do email. [Saiba como](content-from-scratch.md)

1. Para acessar a seção **[!UICONTROL Componentes de conteúdo]** selecione o botão correspondente no painel esquerdo do Designer de email.

   ![](assets/email_designer_content_components.png)

1. Arraste e solte os componentes de conteúdo de sua escolha dentro dos componentes de estrutura relevantes.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >É possível adicionar vários componentes em um único componente de estrutura e em cada coluna de um componente de estrutura.

1. Ajuste os atributos e o estilo de cada componente usando as guias **[!UICONTROL Configurações]** e **[!UICONTROL Estilo]** à direita. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

1. No menu avançado do seu **[!UICONTROL Componente de conteúdo]**, você pode excluir ou duplicar facilmente qualquer componente de conteúdo, conforme necessário.

   ![](assets/email_designer_content_components_settings_2.png)

## Contêiner {#container}

Para aplicar um estilo específico a um grupo de componentes de conteúdo, você pode adicionar um componente **[!UICONTROL Contêiner]** e depois adicionar o(s) componente(s) de conteúdo desejado(s) dentro dele. Isso permite aplicar um estilo distinto ao contêiner, que será diferente do estilo aplicado aos componentes de conteúdo dentro dele.

Por exemplo, adicione um componente **[!UICONTROL Container]** e, em seguida, adicione um componente [Botão](#button) dentro desse container. Você pode usar um plano de fundo específico para o container e outro para o botão.

![](assets/email_designer_container_component.png)

## Botão {#button}

Use o componente **[!UICONTROL Botão]** para inserir um ou vários botões no email e redirecionar o público-alvo do email para outra página.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte o componente **[!UICONTROL Botão]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique no botão recém-adicionado para personalizar o texto e ter acesso às guias **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** no painel direito do Email Designer.

   ![](assets/email_designer_button_component.png)

1. No menu **[!UICONTROL Link]**, adicione a URL para a qual você deseja redirecionar ao clicar no botão.

1. Escolha como o público será redirecionado com a lista suspensa **[!UICONTROL Target]**:

   * **[!UICONTROL Nenhum]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Branco]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Auto]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Principal]**: abre o link no quadro principal.
   * **[!UICONTROL Superior]**: abre o link no corpo completo da janela.

   ![](assets/email_designer_button_link.png)

1. Você pode personalizar ainda mais seu botão alterando atributos de estilo como **[!UICONTROL Borda]**, **[!UICONTROL Tamanho]**, **[!UICONTROL Margem]** etc., do painel **[!UICONTROL Configurações do componente]**.

## Texto {#text}

Use o componente **[!UICONTROL Texto]** para inserir texto no email e ajustar o estilo (borda, tamanho, preenchimento etc.) usando a guia **[!UICONTROL Estilos]**.

![](assets/email_designer_text_component.png)

1. Em **[!UICONTROL Componentes do conteúdo]**, arraste e solte o componente **[!UICONTROL Texto]** em um **[!UICONTROL componente de Estrutura]**.

1. Clique no componente recém-adicionado para personalizar o texto e ter acesso às guias **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** no painel direito do Designer de email.

1. Altere o texto com as seguintes opções disponíveis na barra de ferramentas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Alterar estilo do texto]**: aplique negrito, itálico, sublinhado ou riscado ao seu texto.
   * **Alterar alinhamento**: escolha entre alinhamento esquerdo, direito, central ou justificado para o texto.
   * **[!UICONTROL Criar lista]**: adicione marcadores ou listas de números ao texto.
   * **[!UICONTROL Definir cabeçalho]**: adicione até seis níveis de cabeçalho ao texto.
   * **Tamanho da fonte**: selecione o tamanho da fonte do texto em pixels.
   * **[!UICONTROL Alterar cor da fonte]**: escolha a cor da fonte.
   * **[!UICONTROL Inserir link]**: adicione qualquer tipo de link ao seu conteúdo.
   * **[!UICONTROL Editar imagem]**: adicione uma imagem ou um ativo ao seu componente de texto. [Saiba mais sobre o gerenciamento de ativos](../integrations/assets.md)
   * **[!UICONTROL Alterar cor da fonte]**: escolha a cor da fonte.
   * **[!UICONTROL Adicionar personalização]**: adicione campos de personalização para personalizar o conteúdo dos dados de seus perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)
   * **[!UICONTROL Mostrar o código-fonte]**: exibir o código-fonte do texto. Ele não pode ser modificado.
   * **[!UICONTROL Habilitar conteúdo condicional]**: adicione conteúdo condicional para adaptar o conteúdo do componente aos perfis direcionados. [Saiba mais sobre conteúdo dinâmico](../personalization/get-started-dynamic-content.md)
   * **[!UICONTROL Duplicar]**: adicione uma cópia do seu componente de texto.
   * **[!UICONTROL Excluir]**: exclua o componente de texto selecionado do seu email.

1. Ajuste os outros atributos de estilo, como cor do texto, família da fonte, borda, preenchimento, margem etc., na guia **[!UICONTROL Estilos]**.

   ![](assets/email_designer_text_component_2.png)

## Divisor {#divider}

Use o componente **[!UICONTROL Divisor]** para inserir uma linha divisória para organizar o layout e o conteúdo do email.

É possível ajustar atributos de estilo, como cor da linha, estilo e altura, a partir das guias **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]**.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Use o componente **[!UICONTROL HTML]** para copiar e colar as diferentes partes do HTML existente. Isso permite que você crie componentes de HTML modulares gratuitos para reutilizar algum conteúdo externo.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte o componente **[!UICONTROL HTML]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique no componente recém-adicionado e selecione **[!UICONTROL Mostrar o código-fonte]** na barra de ferramentas contextual para adicionar o HTML.

   ![](assets/email_designer_html_component.png)

1. Copie e cole o código HTML que deseja adicionar ao seu email e clique em **[!UICONTROL Salvar]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Para tornar de forma simples um conteúdo externo compatível com o Designer de email, a Adobe recomenda criar uma mensagem do zero e copiar o conteúdo do email existente para os componentes.

## Imagem {#image}

Use o componente **[!UICONTROL Imagem]** para inserir um arquivo de imagem do seu computador no conteúdo de email.

1. Em **[!UICONTROL Componentes do conteúdo]**, arraste e solte o componente **[!UICONTROL Imagem]** em um **[!UICONTROL componente de Estrutura]**.

   ![](assets/email_designer_image_content.png)

1. Na guia **[!UICONTROL Configurações]**, clique em **[!UICONTROL Procurar]** para escolher um arquivo de imagem de seus ativos ou em **[!UICONTROL Importar mídia]** para carregar um ativo para a Adobe Experience Manager Assets.

   Para saber mais sobre [!DNL Adobe Experience Manager Assets], consulte a [documentação do Adobe Experience Manager Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=pt-BR){target="_blank"}.

   >[!NOTE]
   >
   > Para garantir que seus links permaneçam ativos e evitar problemas de expiração, recomendamos usar o Adobe Assets em vez de depender de um URL de origem para suas imagens.

1. Você também pode pesquisar diretamente no Adobe Stock com a opção **[!UICONTROL Localizar fotos do Adobe Stock]**.

1. Clique no componente recém-adicionado e configure as propriedades da imagem:

   * **[!UICONTROL Título da imagem]** permite definir um título para a imagem.
   * **[!UICONTROL Texto alternativo]** permite definir a legenda vinculada à imagem. Isso corresponde ao atributo HTML alternativo.

   ![](assets/email_designer_10.png)

1. Você também pode optar por **[!UICONTROL Localizar fotos semelhantes do Stock]**. [Saiba mais](../integrations/stock.md)

1. Na guia **[!UICONTROL Estilos]**, ajuste os outros atributos de estilo, como margem, borda etc. ou adicione um link para redirecionar o seu público-alvo para outro conteúdo a partir do painel **[!UICONTROL Configurações do componente]**.

## Social {#social}

Use o componente **[!UICONTROL Social]** para inserir links às páginas de redes sociais no seu conteúdo de email.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte o componente **[!UICONTROL Social]** em um **[!UICONTROL Componente Estrutura]**.

1. Selecione o componente recém-adicionado.

1. No campo **[!UICONTROL Social]** da guia **[!UICONTROL Configurações]**, escolha qual rede social deseja adicionar ou remover.

   ![](assets/email_designer_20.png)

1. Escolha o tamanho dos ícones por meio do campo dedicado.

1. Clique em cada um dos ícones da rede social para configurar a **[!UICONTROL URL]** para a qual o público-alvo será redirecionado.

   ![](assets/email_designer_21.png)

1. Você também pode alterar os ícones de cada uma das mídias sociais, se necessário, no Assets.

1. Ajuste os outros atributos de estilo, como estilo, margem, borda etc., na guia **[!UICONTROL Estilos]**.

## Decisão de oferta {#offer-decision}

Use o componente **[!UICONTROL Offer decision]** para inserir ofertas em suas mensagens. O mecanismo da [gestão de decisões](../offers/get-started/starting-offer-decisioning.md) escolherá a melhor oferta para entregar aos seus clientes.

1. Em **[!UICONTROL Componentes do Conteúdo]**, arraste e solte o componente **[!UICONTROL Decisão de oferta]** em um **[!UICONTROL componente de Estrutura]**.

1. Clique em **[!UICONTROL Adicionar]** para selecionar sua **[!UICONTROL Decisão de oferta]**.

   ![](assets/component_offers.png)

1. Na lista suspensa, selecione seus **[!UICONTROL Posicionamentos]**.  Em seguida, selecione a **[!UICONTROL Decisão de oferta]** que deseja adicionar ao seu conteúdo e clique em **[!UICONTROL Adicionar]**.

   ![](assets/component_offers_2.png)

1. Na guia **[!UICONTROL Offer decision]**, você pode visualizar ou alterar a Oferta inserida.

Saiba como adicionar ofertas personalizadas a um email em [esta seção](add-offers-email.md).

>[!IMPORTANT]
>
>Se forem feitas alterações em uma decisão de oferta em uso na mensagem de uma jornada, será necessário desfazer a publicação da jornada e republicá-la.  Isso garantirá que as alterações sejam incorporadas à mensagem da jornada e que ela seja consistente com as atualizações mais recentes.
