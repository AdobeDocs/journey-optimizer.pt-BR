---
title: Adobe Stock
description: Introdução ao Adobe Stock
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: f2426b8696983b22dd2c80296e2c9dfc2426c439
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 3%

---

# Gerenciar [!DNL Adobe Stock] imagens {#stock}

## Introdução ao [!DNL Adobe Stock] {#get-started-stock}

[!DNL Adobe Stock] fornece acesso a milhões de fotos, vídeos, ilustrações e gráficos vetoriais de alta qualidade e com curadoria e isentos de royalties. Você pode optar por comprar um pacote de crédito para licenciar ativos ou comprar apenas uma licença Standard ou Extended para o ativo necessário. O Adobe Stock também fornece uma coleção gratuita de ativos.

Para obter mais informações sobre [!DNL Adobe Stock], consulte [Adobe Stock Introdução](https://helpx.adobe.com/stock/get-started.html).

Com [!DNL Adobe Journey Optimizer], você pode carregar imagens em seus emails diretamente de [!DNL Adobe Stock] e adicione-o à pasta Assets. O **[!UICONTROL Find Similar Image]** ajudará você a encontrar imagens que correspondam ao conteúdo, à cor e à composição do ativo usado no delivery.
[Saiba mais sobre design de email](design-emails.md).

## Inserir e importar [!DNL Adobe Stock] imagens {#add-stock-image}

>[!NOTE]
>
> O **[!UICONTROL Find Adobe Stock photos]** estará disponível somente para usuários com acesso a um Perfil de produto do AEM Assets Essentials. Para obter mais informações, consulte [Documentação essencial dos ativos](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-users-to-essentials).

Após editar e personalizar seu email, você pode adicionar imagens de [!DNL Adobe Stock] para o modelo:

1. Arrastar e soltar uma imagem **[!UICONTROL Content components]** ao seu email.

   ![](assets/stock_1.png)

1. No **[!UICONTROL Component settings]** selecione **[!UICONTROL Find Adobe Stock photos]**.

   ![](assets/stock_2.png)

1. Navegue pela biblioteca ou insira o termo de pesquisa no campo . Selecione a imagem escolhida e clique em **[!UICONTROL Save]**.

   ![](assets/stock_3.png)

1. Para licenciar e baixar a imagem, selecione a Imagem **[!UICONTROL Content components]** e clique em **[!UICONTROL License Adobe Stock image]**. Você será redirecionado para a função [!DNL Adobe Stock] site.

   >[!NOTE]
   > Se a imagem já tiver sido licenciada, ela será representada pela variável ![](assets/stock_10.png) ícone . Nesse caso, você pode pular para a etapa 7.

   ![](assets/stock_4.png)

1. No [!DNL Adobe Stock] no site, será necessário comprar o ativo para baixar a imagem e remover a marca d&#39;água.

   Essa compra dependerá do plano ou da assinatura da Adobe Stock. Observe que, se você tiver várias contas Adobe Stock, será redirecionado para a última ID de estoque usada. Nesse caso, verifique se você está conectado à conta correta antes de licenciar seu ativo.
Para obter mais informações, consulte esta [página](https://stock.adobe.com/plans).

   >[!WARNING]
   > Se um email incluindo uma imagem não licenciada for enviado, a imagem manterá seu formulário não licenciado com a marca d&#39;água.

   ![](assets/stock_5.png)

1. Assim que sua compra for concluída, você poderá retornar ao seu email em [!DNL Adobe Journey Optimizer] e selecione **[!UICONTROL Import stock image]** para importar a imagem licenciada para os ativos.

   ![](assets/stock_6.png)

1. Selecione em qual pasta seu ativo será armazenado. Para obter mais informações sobre [!DNL Assets Essentials]consulte esta seção [página](assets-essentials.md#get-started-assets-essentials).

   ![](assets/stock_7.png)

1. Depois de selecionar a imagem de [!DNL Adobe Stock], use o **[!UICONTROL Find similar Stock photos]** para localizar ativos que correspondam ao conteúdo, à cor e à composição de uma imagem.

   Observe que essa opção está disponível para imagens licenciadas/não licenciadas do Stock e imagens da sua pasta Ativos .

   ![](assets/stock_8.png)

1. Personalize ainda mais a imagem com o **[!UICONTROL Components settings]** menu. [Saiba mais sobre configurações de componentes](content-components.md)

   ![](assets/stock_11.png)

Depois que a mensagem é criada e personalizada, você pode publicá-la para disponibilizá-la para execução. [Saiba mais](../messages/publish-manage-message.md)
