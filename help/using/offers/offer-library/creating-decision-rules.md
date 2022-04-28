---
title: Criar regras de decisão
description: Saiba como criar regras de decisão para definir para quem as ofertas podem ser exibidas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 15%

---

# Criar regras de decisão {#create-decision-rules}

Você pode criar regras de decisão de oferta com base nos dados disponíveis no Adobe Experience Platform. As regras de decisão determinam para quem uma oferta pode ser exibida.

Por exemplo, você pode especificar que deseja que somente uma &#39;Oferta de roupas de inverno femininas&#39; seja exibida quando (Gênero = &#39;Feminino&#39;) e (Região = &#39;Nordeste&#39;).

➡️ [Descubra este recurso no vídeo](#video)

A lista de regras de decisão criadas pode ser acessada na variável **[!UICONTROL Components]** menu.

![](../assets/decision_rules_list.png)

Para criar uma regra de decisão, siga estas etapas:

1. Vá para o **[!UICONTROL Rules]** e, em seguida, clique em **[!UICONTROL Create rule]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nomeie a regra, forneça uma descrição e configure-a de acordo com suas necessidades.

   Para fazer isso, o **Construtor de segmentos** O está disponível para ajudar a criar as condições da regra. [Saiba mais](../../segment/about-segments.md)

   Neste exemplo, a regra direcionará os clientes que têm o nível de fidelidade &quot;Gold&quot;.

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >O Construtor de segmentos fornecido para criar regras de decisão apresenta algumas especificidades em comparação com a usada com a variável **[!UICONTROL Audience Destinations]** serviço. Por exemplo, a variável **[!UICONTROL Segments]** não está disponível para uso. No entanto, o processo global descrito na documentação do Construtor de segmentos ainda é válido para criar regras de decisão de ofertas.

1. Clique em **[!UICONTROL Save]** para confirmar.

1. Depois que a regra é criada, ela é exibida na lista de regras. Você pode selecioná-lo para exibir suas propriedades e editá-lo ou excluí-lo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>No momento, as ofertas baseadas em eventos não são compatíveis com o [!DNL Journey Optimizer]. Se você criar uma regra de decisão com base em um [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, você não poderá aproveitá-lo em uma oferta.

## Tutorial em vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
