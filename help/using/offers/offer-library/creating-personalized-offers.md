---
title: Criar ofertas personalizadas
description: Saiba como criar ofertas personalizadas no Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 4%

---

# Criar ofertas personalizadas {#creating-personalized-offers}

Antes de criar uma oferta, verifique se você criou:

* Uma **disposição** na qual a oferta será exibida. Consulte [Criar disposições](../offer-library/creating-placements.md)
* Uma **regra de decisão** que definirá a condição sob a qual a oferta será apresentada. Consulte [Criar regras de decisão](../offer-library/creating-decision-rules.md).
* Uma ou várias **tags** que você deseja associar à oferta. Consulte [Criar tags](../offer-library/creating-tags.md).

![](../../assets/do-not-localize/how-to-video.png) [Descubra este recurso no vídeo](#video)

A lista de ofertas personalizadas pode ser acessada no menu **[!UICONTROL Offers]**.

![](../../assets/offers_list.png)

## Crie a oferta {#create-offer}

Para criar uma **oferta**, siga estas etapas:

1. Clique em **[!UICONTROL Create offer]** e selecione **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Especifique o nome da oferta, bem como sua data e hora de início e término. Também é possível associar uma ou várias tags existentes à oferta, permitindo pesquisar e organizar a Biblioteca de ofertas com mais facilidade.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >A seção **[!UICONTROL Offer attributes]** permite associar pares de valores chave à oferta para fins de relatório e análise.

## Configure as representações da oferta {#representations}

1. Adicione uma ou várias representações para a oferta usando o botão **[!UICONTROL Add representation]**.

   >[!NOTE]
   >
   >Uma oferta pode ser exibida em diferentes locais em uma mensagem: em um banner superior com uma imagem, como texto em um parágrafo, como um bloco html etc. Quanto mais representações uma oferta tiver, mais oportunidades haverá para usar a oferta em diferentes contextos de posicionamento.

1. Para cada representação, especifique o **[!UICONTROL Channel]** e o **[!UICONTROL Placement]** onde a oferta será exibida.

   ![](../../assets/channel-placement.png)

   O botão **[!UICONTROL Browse]** permite filtrar as disposições disponíveis e filtrá-las de acordo com o tipo de canal e/ou conteúdo.

   ![](../../assets/browse-placements.png)

1. Adicione conteúdo a cada representação proveniente da biblioteca do Adobe Experience Cloud Assets ou de um local público externo.

   * Para adicionar conteúdo da biblioteca Adobe Experience Cloud Assets, arraste-o e solte-o do painel esquerdo na área de representação, em seguida, especifique o URL a ser associado ao conteúdo no campo **[!UICONTROL Destination link]**.

      >[!NOTE]
      >
      >O conteúdo só pode ser arrastado e solto no Seletor de ativos no painel esquerdo. Somente o conteúdo correspondente ao tipo de conteúdo da disposição está disponível para uso.

      ![](../../assets/offer_drag_content.png)

   * Para adicionar conteúdo de um local público externo, clique no botão **[!UICONTROL Add content]** e especifique o nome, URL e link de Destino do conteúdo a ser adicionado.

      Certifique-se de que o conteúdo que você está adicionando corresponda ao tipo de conteúdo da disposição selecionada.

      ![](../../assets/offer_add_content.png)

   * Também é possível inserir conteúdo do tipo texto. Para fazer isso, clique no botão **[!UICONTROL Add content]** e selecione a opção **[!UICONTROL Custom text]**. No campo **[!UICONTROL Text]**, digite o texto que será exibido na oferta.

      >[!NOTE]
      >
      >Essa opção não está disponível para disposições do tipo imagem.

      ![](../../assets/offer_text_content.png)

## Adicionar regras e restrições de qualificação {#eligibility}

As regras e restrições de elegibilidade permitem definir as condições em que uma oferta será exibida.

1. Configure o **[!UICONTROL Offer eligibility]**. Por padrão, a opção de regra de decisão **[!UICONTROL All visitors]** é selecionada, o que significa que qualquer perfil será qualificado para ser apresentado à oferta.

   É possível limitar a apresentação da oferta aos membros de um ou vários segmentos do Adobe Experience Platform. Para fazer isso, ative a opção **[!UICONTROL Visitors who fall into one or multiple segments]** e adicione um ou vários segmentos do painel esquerdo e combine-os usando os operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]**.

   Para obter mais informações sobre como trabalhar com segmentos, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../../assets/offer-eligibility-segment.png)

   Se desejar associar uma regra de decisão específica à oferta, selecione **[!UICONTROL By defined decision rule]** e arraste a regra desejada do painel esquerdo para a área **[!UICONTROL Decision rule]**. Para obter mais informações sobre como criar uma regra de decisão, consulte [esta seção](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Defina o **[!UICONTROL Priority]** da oferta em comparação com outros se o usuário se qualificar para mais de uma oferta. Quanto mais alta for a prioridade de uma oferta, mais alta será a sua prioridade comparada com outras ofertas

1. Especifique o **[!UICONTROL Capping]** da oferta, o que significa o número de vezes que a oferta será apresentada no total entre todos os usuários. Se a oferta tiver sido entregue a todos os usuários o número de vezes que você especificou neste campo, a entrega será interrompida.

   >[!NOTE]
   >
   >O número de vezes que uma oferta é proposta é calculado no momento da preparação do email. Por exemplo, se você preparar um email com várias ofertas, esses números serão contados em relação ao limite máximo, independentemente de o email ser enviado ou não.
   >
   >Se um delivery de email for excluído ou se a preparação for feita novamente antes de ser enviada, o valor limite da oferta será atualizado automaticamente.

   ![](../../assets/offer_capping.png)

   No exemplo acima:

   * A prioridade da oferta é definida como &quot;50&quot;, o que significa que a oferta será apresentada antes de ofertas com prioridade entre 1 e 49 e depois das com prioridade de pelo menos 51.
   * A oferta será considerada somente para usuários que correspondam à regra de decisão &quot;Clientes de fidelidade Gold&quot;.
   * A oferta será apresentada somente uma vez por usuário.

## Revise a oferta {#review}

Depois que as regras e restrições de qualificação tiverem sido definidas, um resumo das propriedades da oferta será exibido. Se tudo estiver configurado corretamente e sua oferta estiver pronta para ser apresentada aos usuários, clique em **[!UICONTROL Finish]** e selecione **[!UICONTROL Save and approve]**.

Também é possível salvar a oferta como rascunho, para editá-la e aprová-la posteriormente.

![](../../assets/offer_review.png)

A oferta é exibida na lista com o status **[!UICONTROL Live]** ou **[!UICONTROL Draft]** , dependendo de você ter aprovado ou não na etapa anterior.

Agora ele está pronto para ser entregue aos usuários. Você pode selecioná-lo para exibir suas propriedades e editá-lo ou suprimi-lo.

![](../../assets/offer_created.png)

Depois que uma oferta é criada, você pode clicar no nome na lista para acessar informações detalhadas, bem como monitorar todas as alterações feitas nela usando a guia **[!UICONTROL Change log]** (consulte [Monitoramento de alterações em ofertas e decisões](../get-started/user-interface.md#monitoring-changes)).

## Tutoriais em vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica ao serviço de aplicativo do Offer Decisioning criado no Adobe Experience Platform. No entanto, fornece orientação genérica para usar a Oferta no contexto do Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
