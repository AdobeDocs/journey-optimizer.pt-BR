---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com imagens do Adobe Stock
description: Introdução ao Adobe Stock
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: estoque, imagens, integração, fotos
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: 17dd8e2226555ba6bf74f813c11bdeecac05ddd2
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 13%

---

# Trabalhar com [!DNL Adobe Stock] imagens {#stock}

## Introdução ao [!DNL Adobe Stock] {#get-started-stock}

O plug-in de integração do Designer de email para o [!DNL Adobe Stock] e [!DNL Adobe Journey Optimizer] fornece aos clientes uma maneira fácil de navegar, licenciar e salvar imagens para uso na criação de mensagens.

[Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target="_blank"} O fornece acesso a milhões de fotos, vídeos, ilustrações e gráficos vetoriais de alta qualidade, preparados e gratuitos. Você pode optar por comprar um pacote de crédito para licenciar ativos ou comprar apenas uma licença Padrão ou Estendida para o ativo necessário. O Adobe Stock também fornece uma coleção gratuita de ativos.

Com o [!DNL Adobe Journey Optimizer], você pode fazer upload de imagens para seus emails diretamente do [!DNL Adobe Stock] e adicioná-las à pasta **[!UICONTROL Ativos]** usando a opção **[!UICONTROL Encontrar fotos do Adobe Stock]**. Além disso, a opção **[!UICONTROL Encontrar fotos semelhantes do Stock]** ajuda a encontrar imagens que correspondam ao conteúdo, à cor e à composição do ativo usado na entrega.

## Permissões{#stock-permissions}

A variável **[!UICONTROL Localizar fotos do Adobe Stock]** e **[!UICONTROL Localizar Imagem Semelhante]** As opções do estão disponíveis para usuários com acesso a um Perfil de produto do AEM Assets Essentials.

Para obter mais informações, consulte [Documentação essencial dos ativos](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-users-to-essentials){target="_blank"}.

## Inserir uma imagem de [!DNL Adobe Stock] {#add-stock-image}

Para adicionar imagens de [!DNL Adobe Stock] para acessar seu conteúdo, siga as etapas abaixo:

1. No **[!UICONTROL Componentes do conteúdo]** do Designer de email, arraste e solte uma **Imagem**.

1. Clique em **[!UICONTROL Localizar fotos do Adobe Stock]** no lado esquerdo do Designer de email.

   ![](assets/stock-find-photos.png)

1. Navegue pela biblioteca ou insira um termo no campo de pesquisa.

   ![](assets/stock-select-from-lib.png)

1. Selecione a imagem escolhida e clique em **[!UICONTROL Salvar]**.

   Se a imagem selecionada não estiver licenciada, você deverá [obter a licença](#license-stock-image).

## Localizar fotos semelhantes {#similar-stock-image}

Você pode substituir qualquer imagem existente em seu conteúdo de email por uma foto de [!DNL Adobe Stock]. Observe que essa opção está disponível para todas as imagens: imagens do Stock licenciadas/não licenciadas e imagens da sua pasta de ativos.

Para procurar fotos semelhantes, siga as etapas abaixo:

1. Selecione a imagem a ser substituída.
1. Clique em **[!UICONTROL Encontrar fotos semelhantes do Stock]** botão para exibir ativos no [!DNL Adobe Stock] que correspondem ao conteúdo, cor e composição da imagem.

   ![](assets/stock-similar.png)

1. Selecione a imagem escolhida e clique em **[!UICONTROL Salvar]**.

   ![](assets/stock-similar-results.png)

   Se a imagem selecionada não estiver licenciada, você deverá [obter a licença](#license-stock-image).

1. Personalize a imagem, se necessário, com o **[!UICONTROL Configurações]** e **[!UICONTROL Estilos]** guias. [Saiba mais sobre configurações de componentes](../email/content-components.md).

## Obter a licença do [!DNL Adobe Stock] {#license-stock-image}

Se sua imagem já estiver licenciada, ela será representada pela variável ![](assets/stock_10.png) ícone. Caso contrário, você deve licenciá-lo.

Para licenciar e baixar a imagem, siga as etapas abaixo:

1. Selecione-a e clique no botão **[!UICONTROL Licenciar imagem do Adobe Stock]** ícone.

   ![](assets/stock-license-icon.png)

   Você será redirecionado para a [!DNL Adobe Stock] site para comprar a licença.

   ![](assets/stock-license-photo.png)

1. No [!DNL Adobe Stock] site, você precisa comprar seu ativo para baixar a imagem e remover a marca d&#39;água.

   Essa compra depende do seu plano ou assinatura da Adobe Stock. Observe que, se você tiver várias contas do Adobe Stock, será redirecionado para a última ID do Stock usada. Nesse caso, verifique se você está conectado à conta correta antes de licenciar seu ativo.

   Para obter mais informações sobre planos e preços do Adobe Stock em [Documentação do Adobe Stock](https://stock.adobe.com/plans){target="_blank"}.

   >[!WARNING]
   > Se um email incluindo uma imagem não licenciada for enviado, a imagem manterá seu formulário não licenciado com a marca d&#39;água.

1. Após concluir a compra, você pode voltar para o email no [!DNL Adobe Journey Optimizer] e selecione **[!UICONTROL Importar imagem de estoque]** para importar a imagem licenciada para os ativos.

   ![](assets/stock_6.png)

1. Selecione em qual pasta armazenar o ativo. Para obter mais informações sobre [!DNL Assets Essentials], consulte este [página](assets-essentials.md#get-started-assets-essentials).

## Tópicos relacionados{#stock-related-topics}

* [Design de email no Journey Optimizer](../email/get-started-email-design.md)
* [Configurações de componentes para design de email](../email/content-components.md)
* [Introdução ao Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target="_blank"}.

