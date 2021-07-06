---
title: Criar regras de decisão
description: Saiba como criar regras de decisão no Adobe Experience Platform.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: 0e5cc9101ff382ce9fde442da38eb46aa28e9c77
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 15%

---

# Criar regras de decisão {#creating-decision-rules}

Você pode criar regras de decisão de oferta com base nos dados disponíveis no Adobe Experience Platform. As regras de decisão determinam para quem uma oferta pode ser exibida.

Por exemplo, você pode especificar que deseja que somente uma &#39;Oferta de roupas de inverno femininas&#39; seja exibida quando (Gênero = &#39;Feminino&#39;) e (Região = &#39;Nordeste&#39;).

➡️ [Descubra este recurso no vídeo](#video)

A lista de regras de decisão criadas pode ser acessada no menu **[!UICONTROL Components]**.

![](../../assets/decision_rules_list.png)

Para criar uma regra de decisão, siga estas etapas:

1. Vá para a guia **[!UICONTROL Rules]** e clique em **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Nomeie a regra, forneça uma descrição e configure-a de acordo com suas necessidades.

   Para fazer isso, o **Construtor de segmentos** do Adobe Experience Platform está disponível para ajudar você a criar as condições da regra. Para obter mais informações sobre como usá-lo, consulte a [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

   Neste exemplo, a regra direcionará os clientes que têm o nível de fidelidade &quot;Gold&quot;.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >O Construtor de segmentos fornecido para criar regras de decisão apresenta algumas especificidades em comparação com a usada com o serviço **[!UICONTROL Audience Destinations]**. Por exemplo, a guia **[!UICONTROL Segments]** não está disponível para uso. No entanto, o processo global descrito na documentação do Construtor de segmentos ainda é válido para criar regras de decisão de ofertas.

1. Clique em **[!UICONTROL Save]** para confirmar.

1. Depois que a regra é criada, ela é exibida na lista de regras. Você pode selecioná-lo para exibir suas propriedades e editá-lo ou excluí-lo.

   ![](../../assets/rule_created.png)

## Tutorial em vídeo {#video}

>[!NOTE]
>
>Este vídeo se aplica ao serviço de aplicativo do Offer Decisioning criado no Adobe Experience Platform. No entanto, fornece orientação genérica para usar a Oferta no contexto do Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
