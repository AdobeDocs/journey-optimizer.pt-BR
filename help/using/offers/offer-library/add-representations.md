---
title: Adicionar representações a uma oferta
description: Saiba como adicionar representações às suas ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 1%

---

# Adicionar representações a uma oferta {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Representações"
>abstract="Adicione representações para definir onde a oferta será exibida na mensagem. Quanto mais representações uma oferta tiver, mais oportunidades haverá para usar a oferta em diferentes contextos de posicionamento."

Uma oferta pode ser exibida em diferentes locais em uma mensagem: em um banner superior com uma imagem, como texto em um parágrafo, como um bloco de HTML, etc. Quanto mais representações uma oferta tiver, mais oportunidades haverá para usar a oferta em diferentes contextos de posicionamento.

## Configurar as representações da oferta {#representations}

Para adicionar uma ou várias representações à sua oferta e configurá-las, siga as etapas abaixo.

1. Para a primeira representação, comece selecionando o **[!UICONTROL Canal]** que será usado.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Somente as disposições disponíveis para o canal selecionado são exibidas na **[!UICONTROL Posicionamento]** lista suspensa.

1. Selecione uma disposição na lista.

   Também é possível usar o botão próximo ao **[!UICONTROL Posicionamento]** lista suspensa para navegar por todas as disposições.

   ![](../assets/browse-button-placements.png)

   Lá, ainda é possível filtrar as disposições de acordo com seu canal e/ou tipo de conteúdo. Escolha uma disposição e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/browse-placements.png)

1. Adicione conteúdo à sua representação. Saiba mais sobre como [esta seção](#content).

1. Ao adicionar conteúdo, como uma imagem ou URL, é possível especificar um **[!UICONTROL Link de destino]**: os usuários que clicarem na oferta serão direcionados para a página correspondente.

   ![](../assets/offer-destination-link.png)

1. Finalmente, selecione o idioma escolhido para ajudar a identificar e gerenciar o que será exibido aos usuários.

1. Para adicionar outra representação, use o **[!UICONTROL Adicionar representação]** e adicione quantas representações forem necessárias.

   ![](../assets/offer-add-representation.png)

1. Depois de adicionar todas as suas representações, selecione **[!UICONTROL Próximo]**.

## Definir conteúdo para suas representações {#content}

É possível adicionar diferentes tipos de conteúdo a uma representação.

>[!NOTE]
>
>Somente o conteúdo correspondente ao tipo de conteúdo da disposição está disponível para uso.

### Adicionar imagens {#images}

Se a disposição selecionada for do tipo imagem, você poderá adicionar conteúdo proveniente da variável **Adobe Experience Cloud Asset** , um repositório centralizado dos ativos fornecidos por [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Para trabalhar com [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html?lang=pt-BR){target="_blank"}.

1. Escolha a **[!UICONTROL Biblioteca de ativos]** opção.

1. Selecionar **[!UICONTROL Procurar]**.

   ![](../assets/offer-browse-asset-library.png)

1. Navegue pelos ativos para selecionar a imagem de sua escolha

1. Clique em **[!UICONTROL Selecionar]**.

   ![](../assets/offer-select-asset.png)

### Adicionar arquivos HTML ou JSON {#html-json}

Se a disposição selecionada for tipo HTML, também é possível adicionar HTML ou conteúdo JSON proveniente da variável [Biblioteca de ativos da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Por exemplo, você criou um modelo de email do HTML em [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} e deseja usar esse arquivo para o conteúdo da oferta. Em vez de criar um novo arquivo, você pode simplesmente fazer upload do modelo no **Biblioteca de ativos** para poder reutilizá-lo nas representações da sua oferta.

Para reutilizar o conteúdo em uma representação, navegue pelo **Biblioteca de ativos** conforme descrito em [esta seção](#images) e selecione o HTML ou o arquivo JSON de sua escolha.

![](../assets/offer-browse-asset-library-json.png)

### Adicionar URLs {#urls}

Para adicionar conteúdo de um local público externo, selecione **[!UICONTROL URL]**, em seguida, insira o endereço de URL do conteúdo a ser adicionado.

![](../assets/offer-content-url.png)

### Adicionar texto personalizado {#custom-text}

Você também pode inserir conteúdo do tipo texto ao selecionar uma disposição compatível.

1. Selecione o **[!UICONTROL Personalizado]** e clique em **[!UICONTROL Adicionar conteúdo]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Essa opção não está disponível para disposições do tipo imagem.

1. Digite o texto que será exibido na oferta.

   ![](../assets/offer-text-content.png)

   Você pode personalizar o conteúdo usando o editor de expressão. Saiba mais sobre [personalização](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Somente a variável **[!UICONTROL Atributos do perfil]**, **[!UICONTROL Associações de segmento]** e **[!UICONTROL Funções auxiliares]** As fontes estão disponíveis para o Gerenciamento de decisões.

