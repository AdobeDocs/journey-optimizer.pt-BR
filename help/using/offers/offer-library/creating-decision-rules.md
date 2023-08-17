---
title: Criar regras de decisão
description: Saiba como criar regras de decisão para definir para quem as ofertas podem ser exibidas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 17%

---

# Criar regras de decisão {#create-decision-rules}

É possível criar regras de decisão de oferta com base nos dados disponíveis no Adobe Experience Platform. As regras de decisão determinam para quem uma oferta pode ser exibida.

Por exemplo, você pode especificar que deseja que somente uma &#39;Oferta de roupas de inverno femininas&#39; seja exibida quando (Gênero = &#39;Feminino&#39;) e (Região = &#39;Nordeste&#39;).

➡️ [Descubra este recurso no vídeo](#video)

A lista de regras de decisão criadas pode ser acessada no **[!UICONTROL Componentes]** menu.

![](../assets/decision_rules_list.png)

Para criar uma regra de decisão, siga estas etapas:

1. Vá para a **[!UICONTROL Regras]** e clique em **[!UICONTROL Criar regra]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nomeie a regra, forneça uma descrição e configure-a de acordo com suas necessidades.

   Para fazer isso, o Adobe Experience Platform **Construtor de segmentos** O está disponível para ajudar você a criar as condições da regra. [Saiba como criar definições de segmento](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >O Construtor de segmentos fornecido para criar regras de decisão apresenta algumas especificidades em comparação à usada com o **[!UICONTROL Segmentação]** serviço. No entanto, o processo global descrito no [Construtor de segmentos](../../audience/creating-a-segment-definition.md) a documentação ainda é válida para criar regras de decisões de ofertas. Saiba mais na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=pt-br).

1. À medida que você adiciona e configura novos campos no espaço de trabalho, a variável **[!UICONTROL Propriedades do público]** exibe informações sobre os perfis estimados pertencentes ao público. Clique em **[!UICONTROL Atualizar estimativa]** para atualizar dados.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que exige que o tempo atual seja ≥ 80 graus.

1. Clique em **[!UICONTROL Salvar]** para confirmar.

1. Depois que a regra é criada, ela é exibida no **[!UICONTROL Regras]** lista. Você pode selecioná-la para exibir suas propriedades e editá-la ou excluí-la.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>No momento, as ofertas baseadas em eventos não são compatíveis com o [!DNL Journey Optimizer]. Se você criar uma regra de decisão com base em uma [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}, você não poderá aproveitá-lo em uma oferta.

## Tutorial em vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
