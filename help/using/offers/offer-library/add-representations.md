---
title: Adicionar representações a uma oferta
description: Saiba como adicionar representações às suas ofertas
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 8%

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
   >Somente as disposições disponíveis para o canal selecionado são exibidas na lista suspensa **[!UICONTROL Disposição]**.

1. Selecione uma disposição na lista.

   Você também pode usar o botão ao lado da lista suspensa **[!UICONTROL Posicionamento]** para procurar todos os posicionamentos.

   ![](../assets/browse-button-placements.png)

   Ainda é possível filtrar os posicionamentos de acordo com o canal e/ou tipo de conteúdo. Escolha um posicionamento e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/browse-placements.png)

1. Adicione conteúdo à sua representação. Saiba mais em [esta seção](#content).

1. Ao adicionar conteúdo, como uma imagem ou URL, você pode especificar um **[!UICONTROL Link de destino]**: os usuários que clicarem na oferta serão direcionados para a página correspondente.

   ![](../assets/offer-destination-link.png)

1. Por fim, selecione o idioma de sua escolha para ajudar a identificar e gerenciar o que exibir para os usuários.

1. Para adicionar outra representação, use o botão **[!UICONTROL Adicionar representação]** e adicione quantas representações forem necessárias.

   ![](../assets/offer-add-representation.png)

1. Depois de adicionar todas as representações, selecione **[!UICONTROL Avançar]**.

## Definir o conteúdo para suas representações {#content}

É possível adicionar diferentes tipos de conteúdo a uma representação.

>[!NOTE]
>
>Somente o conteúdo correspondente ao tipo de conteúdo da disposição está disponível para uso.

### Adicionar imagens {#images}

Se o posicionamento selecionado for do tipo imagem, você poderá adicionar conteúdo proveniente da biblioteca do **Adobe Experience Cloud Asset**, um repositório centralizado de ativos fornecidos pelo [!DNL Adobe Experience Manager Assets].

>[!NOTE]
>
> Para trabalhar com o [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, é necessário implantar o [!DNL Assets Essentials] para sua organização e verificar se os usuários fazem parte dos **Usuários consumidores do Assets Essentials** e/ou dos **Perfis de produto dos Usuários do Assets Essentials**. Saiba mais sobre [esta página](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. Escolha a opção **[!UICONTROL Biblioteca de ativos]**.

1. Selecione **[!UICONTROL Procurar]**.

   ![](../assets/offer-browse-asset-library.png)

1. Navegue pelos ativos para selecionar a imagem de sua escolha

1. Clique em **[!UICONTROL Selecionar]**.

   ![](../assets/offer-select-asset.png)

### Adicionar arquivos HTML ou JSON {#html-json}

Se o posicionamento selecionado for do tipo HTML, você também poderá adicionar conteúdo HTML ou JSON provenientes da [biblioteca de Ativos da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Por exemplo, você criou um modelo de email do HTML no [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} e deseja usar esse arquivo para o conteúdo da oferta. Em vez de criar um novo arquivo, basta carregar o modelo na **Biblioteca de Ativos** para poder reutilizá-lo nas representações de oferta.

Para reutilizar o conteúdo em uma representação, navegue pela **Biblioteca de Ativos** conforme descrito em [esta seção](#images) e selecione o arquivo HTML ou JSON de sua escolha.

![](../assets/offer-browse-asset-library-json.png)

### Adicionar URLs {#urls}

Para adicionar conteúdo de um local público externo, selecione **[!UICONTROL URL]** e insira o endereço da URL do conteúdo a ser adicionado.

Você pode personalizar URLs usando o editor de personalização. Saiba mais sobre [personalização](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

Por exemplo, você deseja personalizar a imagem mostrada como uma oferta. Você quer que os usuários que favorecem as férias da cidade vejam o horizonte de Nova York e os usuários que favorecem as férias da praia para ver o Havaí costa norte.

Use o editor de personalização para recuperar atributos de Perfil armazenados no Adobe Experience Platform usando esquemas de união. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Se você especificar um **[!UICONTROL Link de destino]**, também poderá personalizar a URL para a qual os usuários que clicarem na oferta serão direcionados.

### Adicionar texto personalizado {#custom-text}

Você também pode inserir conteúdo do tipo texto ao selecionar um posicionamento compatível.

1. Selecione a opção **[!UICONTROL Personalizado]** e clique em **[!UICONTROL Adicionar conteúdo]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Essa opção não está disponível para inserções do tipo imagem.

1. Digite o texto que será exibido na oferta.

   ![](../assets/offer-text-content.png)

   Você pode personalizar o conteúdo usando o editor de personalização. Saiba mais sobre [personalização](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Somente os **[!UICONTROL Atributos do perfil]**, **[!UICONTROL Públicos-alvo]** e **[!UICONTROL Funções auxiliares]** fontes estão disponíveis para a Gestão de Decisões.

## Personalizar representações com base nos dados de contexto{#context-data}

Quando dados de contexto são passados na chamada [Edge decisioning](../api-reference/offer-delivery-api/edge-decisioning-api.md), você pode aproveitar esses dados para personalizar representações dinamicamente. Por exemplo, você pode adaptar a representação de uma oferta com base em fatores em tempo real, como as condições meteorológicas atuais no momento em que a decisão é tomada.

Para usar dados de contexto em representações de oferta, incorpore a variável de dados de contexto diretamente no conteúdo de representação usando o namespace `profile.timeSeriesEvents.`.

Este é um exemplo de sintaxe usado para personalizar a representação de uma oferta com base nos sistemas operacionais dos usuários:

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

A solicitação de decisão correspondente do Edge, incluindo os dados de contexto, é a seguinte:

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
