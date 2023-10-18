---
title: Adicionar representações a uma oferta
description: Saiba como adicionar representações às suas ofertas
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 9%

---

# Adicionar representações a uma oferta {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Representações"
>abstract="Adicione representações para definir onde a oferta será exibida na mensagem. Quanto mais representações uma oferta tiver, mais oportunidades haverá para usar a oferta em diferentes contextos de posicionamento."

Uma oferta pode ser exibida em diferentes locais em uma mensagem: em um banner superior com uma imagem, como texto em um parágrafo, como um bloco HTML etc. Quanto mais representações uma oferta tiver, mais oportunidades haverá para usar a oferta em diferentes contextos de posicionamento.

## Configurar as representações da oferta {#representations}

Para adicionar uma ou várias representações à sua oferta e configurá-las, siga as etapas abaixo.

1. Para a primeira representação, comece selecionando o **[!UICONTROL Canal]** que será usado.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Somente os posicionamentos disponíveis para o canal selecionado são exibidos no **[!UICONTROL Posicionamento]** lista suspensa.

1. Selecione uma disposição na lista.

   Também é possível usar o botão ao lado do botão **[!UICONTROL Posicionamento]** para procurar todos os posicionamentos.

   ![](../assets/browse-button-placements.png)

   Ainda é possível filtrar os posicionamentos de acordo com o canal e/ou tipo de conteúdo. Escolha um posicionamento e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/browse-placements.png)

1. Adicione conteúdo à sua representação. Saiba mais em [nesta seção](#content).

1. Ao adicionar conteúdo, como uma imagem ou URL, você pode especificar um **[!UICONTROL Link de destino]**: os usuários que clicarem na oferta serão direcionados para a página correspondente.

   ![](../assets/offer-destination-link.png)

1. Por fim, selecione o idioma de sua escolha para ajudar a identificar e gerenciar o que exibir para os usuários.

1. Para adicionar outra representação, use o **[!UICONTROL Adicionar representação]** e adicione quantas representações forem necessárias.

   ![](../assets/offer-add-representation.png)

1. Depois de adicionar todas as representações, selecione **[!UICONTROL Próxima]**.

## Definir o conteúdo para suas representações {#content}

É possível adicionar diferentes tipos de conteúdo a uma representação.

>[!NOTE]
>
>Somente o conteúdo correspondente ao tipo de conteúdo da disposição está disponível para uso.

### Adicionar imagens {#images}

Se a disposição selecionada for do tipo imagem, é possível adicionar conteúdo proveniente da **Ativo do Adobe Experience Cloud** biblioteca, um repositório centralizado de ativos fornecidos pelo [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Para trabalhar com [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html?lang=pt-BR){target="_blank"}.

1. Escolha o **[!UICONTROL Biblioteca de ativos]** opção.

1. Selecionar **[!UICONTROL Procurar]**.

   ![](../assets/offer-browse-asset-library.png)

1. Navegue pelos ativos para selecionar a imagem de sua escolha

1. Clique em **[!UICONTROL Selecionar]**.

   ![](../assets/offer-select-asset.png)

### Adicionar arquivos HTML ou JSON {#html-json}

Se a disposição selecionada for do tipo HTML, você também poderá adicionar conteúdo HTML ou JSON proveniente da [Biblioteca de ativos do Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Por exemplo, você criou um template de email de HTML no [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} e quiser usar esse arquivo para o conteúdo da oferta. Em vez de criar um novo arquivo, você pode simplesmente fazer upload do modelo na **Biblioteca de ativos** para poder reutilizá-lo nas representações da oferta.

Para reutilizar o conteúdo em uma representação, navegue pelo **Biblioteca de ativos** conforme descrito em [nesta seção](#images) e selecione o arquivo HTML ou JSON de sua escolha.

![](../assets/offer-browse-asset-library-json.png)

### Adicionar URLs {#urls}

Para adicionar conteúdo de um local público externo, selecione **[!UICONTROL URL]**, em seguida, digite o endereço do URL do conteúdo a ser adicionado.

Você pode personalizar URLs usando o editor de expressão. Saiba mais sobre [personalização](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

Por exemplo, você deseja personalizar a imagem mostrada como uma oferta. Você quer que os usuários que favorecem as férias da cidade vejam o horizonte de Nova York e os usuários que favorecem as férias da praia para ver o Havaí costa norte.

Use o Editor de expressão para recuperar atributos de perfil armazenados no Adobe Experience Platform usando esquemas de união. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Se você especificar um **[!UICONTROL Link de destino]**, você também pode personalizar o URL para o qual os usuários que clicam na oferta serão direcionados.

### Adicionar texto personalizado {#custom-text}

Você também pode inserir conteúdo do tipo texto ao selecionar um posicionamento compatível.

1. Selecione o **[!UICONTROL Personalizado]** e clique em **[!UICONTROL Adicionar conteúdo]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Essa opção não está disponível para inserções do tipo imagem.

1. Digite o texto que será exibido na oferta.

   ![](../assets/offer-text-content.png)

   Você pode personalizar o conteúdo usando o Editor de expressão. Saiba mais sobre [personalização](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Somente o **[!UICONTROL Atributos do perfil]**, **[!UICONTROL Públicos-alvo]** e **[!UICONTROL Funções auxiliares]** As fontes de estão disponíveis para a Gestão de decisões.

