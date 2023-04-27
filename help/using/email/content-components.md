---
solution: Journey Optimizer
product: journey optimizer
title: Usar componentes de conteúdo do designer de email
description: Saiba como usar componentes de conteúdo em seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: componentes, designer de email, editor, email
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 7%

---

# Usar os componentes de conteúdo do Email Designer {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um email."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Sobre componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de uma página de destino."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Sobre os componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de um fragmento."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um modelo."

Ao criar o conteúdo do email, **[!UICONTROL Componentes de conteúdo]** O permite personalizar ainda mais o email com componentes brutos que podem ser editados depois de colocados no email.

Você pode adicionar quantos componentes de conteúdo forem necessários dentro de um ou mais componentes de estrutura, que definem o layout do email.

## Adicionar componentes de conteúdo {#add-content-components}

Para adicionar componentes de conteúdo ao seu email e ajustá-los às suas necessidades, siga as etapas abaixo.

1. No Designer de email, use um conteúdo existente ou arraste e solte **[!UICONTROL Componentes da estrutura]** no conteúdo vazio para definir o layout do email. [Saiba como](content-from-scratch.md)

1. Para acessar o **[!UICONTROL Componentes de conteúdo]** selecione o botão correspondente no painel esquerdo do Designer de email.

   ![](assets/email_designer_content_components.png)

1. Arraste e solte os componentes de conteúdo de sua escolha dentro dos componentes de estrutura relevantes.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >É possível adicionar vários componentes em um único componente de estrutura e em cada coluna de um componente de estrutura.

1. Ajuste os atributos de estilo para cada componente usando o **[!UICONTROL Configurações]** e **[!UICONTROL Estilo]** à direita. Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente. [Saiba mais sobre alinhamento e preenchimento](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

1. No menu avançado de **[!UICONTROL Componente de conteúdo]**, você pode excluir ou duplicar facilmente todos os componentes de conteúdo, conforme necessário.

   ![](assets/email_designer_content_components_settings_2.png)

## Contêiner {#container}

Para aplicar um estilo específico a um grupo de componentes de conteúdo, é possível adicionar um **[!UICONTROL Contêiner]** e, em seguida, adicione os componentes de conteúdo desejados. Isso permite aplicar um estilo distinto ao contêiner, que será diferente do estilo aplicado aos componentes de conteúdo dentro.

Por exemplo, adicione uma **[!UICONTROL Contêiner]** e, em seguida, adicione um [Botão](#button) componente dentro desse contêiner. Você pode usar um plano de fundo específico para o contêiner e outro para o botão .

![](assets/email_designer_container_component.png)

## Botão {#button}

Use o **[!UICONTROL Botão]** para inserir um ou vários botões no email e redirecionar o público do email para outra página.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL Botão]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique no botão recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** no painel direito do Designer de email.

   ![](assets/email_designer_button_component.png)

1. No **[!UICONTROL Link]** adicione o URL para o qual deseja redirecionar ao clicar no botão .

1. Escolha como seu público será redirecionado com o **[!UICONTROL Target]** lista suspensa:

   * **[!UICONTROL Nenhum]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Em branco]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Auto]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Pai]**: abre o link no quadro principal.
   * **[!UICONTROL Topo]**: abre o link no corpo completo da janela.

   ![](assets/email_designer_button_link.png)

1. Você pode personalizar ainda mais seu botão alterando atributos de estilo como **[!UICONTROL Borda]**, **[!UICONTROL Tamanho]**, **[!UICONTROL Margem]**, etc. do **[!UICONTROL Configurações do componente]** painel.

## Texto {#text}

Use o **[!UICONTROL Texto]** componente para inserir texto no email e ajustar o estilo (borda, tamanho, preenchimento etc.) usando o **[!UICONTROL Estilos]** guia .

![](assets/email_designer_text_component.png)

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL Texto]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique no componente recém-adicionado para personalizar o texto e ter acesso ao **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** no painel direito do Designer de email.

1. Altere o texto com as seguintes opções disponíveis na barra de ferramentas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Alterar estilo do texto]**: aplique negrito, itálico, sublinhado ou riscado ao seu texto.
   * **Alterar alinhamento**: escolha entre alinhamento esquerdo, direito, central ou justificado para o texto.
   * **[!UICONTROL Criar lista]**: adicione marcadores ou listas de números ao texto.
   * **[!UICONTROL Definir cabeçalho]**: adicione até seis níveis de cabeçalho ao texto.
   * **Tamanho da fonte**: selecione o tamanho da fonte do texto em pixels.
   * **[!UICONTROL Alterar cor da fonte]**: escolha a cor da fonte.
   * **[!UICONTROL Inserir link]**: adicione qualquer tipo de link ao seu conteúdo.
   * **[!UICONTROL Editar imagem]**: adicione uma imagem ou um ativo ao seu componente de texto. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md)
   * **[!UICONTROL Alterar cor da fonte]**: escolha a cor da fonte.
   * **[!UICONTROL Adicionar personalização]**: adicione campos de personalização para personalizar o conteúdo dos dados de seus perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md)
   * **[!UICONTROL Mostrar o código-fonte]**: exibir o código-fonte do texto. Ele não pode ser modificado.
   * **[!UICONTROL Habilitar conteúdo condicional]**: adicione conteúdo condicional para adaptar o conteúdo do componente aos perfis segmentados. [Saiba mais sobre conteúdo dinâmico](../personalization/get-started-dynamic-content.md)
   * **[!UICONTROL Duplicar]**: adicione uma cópia do seu componente de texto.
   * **[!UICONTROL Excluir]**: exclua o componente de texto selecionado do seu email.

1. Ajuste os outros atributos de estilo, como cor do texto, família da fonte, borda, preenchimento, margem etc. do **[!UICONTROL Estilos]** guia .

   ![](assets/email_designer_text_component_2.png)

## Divisor {#divider}

Use o **[!UICONTROL Divisor]** para inserir uma linha divisória para organizar o layout e o conteúdo do seu email.

É possível ajustar atributos de estilo, como cor da linha, estilo e altura da **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** guias.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Use o **[!UICONTROL HTML]** componente para copiar e colar as diferentes partes do HTML existente. Isso permite que você crie componentes de HTML modulares gratuitos para reutilizar algum conteúdo externo.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL HTML]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique no componente recém-adicionado e selecione **[!UICONTROL Mostrar o código-fonte]** na barra de ferramentas contextual para adicionar o HTML.

   ![](assets/email_designer_html_component.png)

1. Copie e cole o código do HTML que deseja adicionar ao seu email e clique em **[!UICONTROL Salvar]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Para simplesmente tornar um conteúdo externo compatível com o Designer de email, o Adobe recomenda criar uma mensagem do zero e copiar o conteúdo do email existente para componentes.

## Imagem {#image}

Use o **[!UICONTROL Imagem]** componente para inserir um arquivo de imagem de seu computador no conteúdo do email.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL Imagem]** em um **[!UICONTROL Componente Estrutura]**.

   ![](assets/email_designer_image_content.png)

1. Clique em **[!UICONTROL Procurar]** para escolher um arquivo de imagem de seus ativos.

   Para saber mais sobre [!DNL Assets Essentials], consulte [Documentação do Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Clique no componente recém-adicionado e configure as propriedades da imagem no **[!UICONTROL Configurações]** guia :

   * **[!UICONTROL Título da imagem]** permite definir um título para a imagem.
   * **[!UICONTROL Texto alternativo]** permite definir a legenda vinculada à imagem. Isso corresponde ao atributo HTML alt.

   ![](assets/email_designer_10.png)

1. Você também pode optar por **[!UICONTROL Localizar fotos semelhantes do Stock]**. [Saiba mais](stock.md)

1. No **[!UICONTROL Estilos]** , ajuste os outros atributos de estilo, como margem, borda etc. ou adicionar um link para redirecionar seu público para outro conteúdo do **[!UICONTROL Configurações do componente]** painel.

## Social {#social}

Use o **[!UICONTROL Social]** componente para inserir links às páginas de mídia social no seu conteúdo de email.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL Social]** em um **[!UICONTROL Componente Estrutura]**.

1. Selecione o componente recém-adicionado.

1. No **[!UICONTROL Social]** do **[!UICONTROL Configurações]** escolha a mídia social que deseja adicionar ou remover.

   ![](assets/email_designer_20.png)

1. Escolha o tamanho dos ícones no campo dedicado.

1. Clique em cada um dos ícones de redes sociais para configurar o **[!UICONTROL URL]** para o qual o público-alvo será redirecionado.

   ![](assets/email_designer_21.png)

1. Você também pode alterar os ícones de cada uma das mídias sociais, se necessário, em seus Ativos.

1. Ajuste os outros atributos de estilo, como estilo, margem, borda etc. do **[!UICONTROL Estilos]** guia .

## Decisão da oferta {#offer-decision}

Use o **[!UICONTROL Decisão da oferta]** componente para inserir ofertas em suas mensagens. O [gestão de decisões](../offers/get-started/starting-offer-decisioning.md) O mecanismo escolherá a melhor oferta a ser entregue aos clientes.

1. De **[!UICONTROL Componentes de conteúdo]**, arraste e solte a **[!UICONTROL Decisão da oferta]** em um **[!UICONTROL Componente Estrutura]**.

1. Clique em **[!UICONTROL Adicionar]** para selecionar seu **[!UICONTROL Decisão da oferta]**.

   ![](assets/component_offers.png)

1. No menu suspenso , selecione o **[!UICONTROL Posicionamentos]**.  Em seguida, selecione o **[!UICONTROL Decisão da oferta]** você deseja adicionar ao seu conteúdo e clique em **[!UICONTROL Adicionar]**.

   ![](assets/component_offers_2.png)

1. No **[!UICONTROL Decisão da oferta]** , é possível visualizar ou alterar a Oferta inserida.

Saiba como adicionar ofertas personalizadas a um email em [esta seção](add-offers-email.md).

>[!IMPORTANT]
>
>Se forem feitas alterações em uma decisão de oferta que está sendo usada em uma mensagem do jornada, será necessário desfazer a publicação da jornada e republicá-la.  Isso garantirá que as alterações sejam incorporadas na mensagem da jornada e que a mensagem seja consistente com as atualizações mais recentes.
