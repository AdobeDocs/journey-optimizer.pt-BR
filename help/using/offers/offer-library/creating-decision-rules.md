---
title: Criar regras de decisão
description: Saiba como criar regras de decisão para definir para quem as ofertas podem ser exibidas
badge: label="Herdados" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 7%

---

# Criar regras de decisão {#create-decision-rules}

## Sobre as regras de decisão {#about}

É possível criar regras de decisão de oferta com base nos dados disponíveis no Adobe Experience Platform. As regras de decisão determinam para quem uma oferta pode ser exibida.

Por exemplo, você pode especificar que deseja que somente uma &#39;Oferta de roupas de inverno femininas&#39; seja exibida quando (Gênero = &#39;Feminino&#39;) e (Região = &#39;Nordeste&#39;).

➡️ [Conheça este recurso no vídeo](#video)

Esta é uma lista de limitações que devem ser observadas ao trabalhar com regras de decisão:

* A decisão do Edge usa o perfil de borda que não armazena eventos, portanto, qualquer regra usada em uma decisão de borda será inválida.
* Ao criar uma regra de decisão, a retrospectiva de um período anterior não é compatível. Por exemplo, se você especificar um evento de experiência que ocorreu no último mês como um componente da regra. Qualquer tentativa de incluir um período de lookback durante a criação da regra acionará um erro ao salvá-la.
  <!--* Decision requests that use the hub profile will look at the last 100 experience events on the profile to evaluate rules that reference historical experience events.-->

## Criar uma regra de decisão {#create}

A lista de regras de decisão criadas está acessível no menu **[!UICONTROL Componentes]**.

![](../assets/decision_rules_list.png)

Para criar uma regra de decisão, siga estas etapas:

1. Vá para a guia **[!UICONTROL Regras]** e clique em **[!UICONTROL Criar regra]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nomeie a regra, forneça uma descrição e configure-a de acordo com suas necessidades.

   Para fazer isso, o **Construtor de segmentos** da Adobe Experience Platform está disponível para ajudar você a criar as condições da regra. [Saiba como criar definições de segmento](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >O Construtor de segmentos fornecido para criar regras de decisão apresenta algumas especificidades em comparação à usada com o serviço **[!UICONTROL Segmentação]**. No entanto, o processo global descrito na documentação do [Construtor de segmentos](../../audience/creating-a-segment-definition.md) ainda é válido para criar regras de decisões de ofertas. Saiba mais na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=pt-br).

1. À medida que você adiciona e configura novos campos no espaço de trabalho, o painel **[!UICONTROL Propriedades de público-alvo]** exibe informações sobre os perfis estimados pertencentes ao público-alvo. Clique em **[!UICONTROL Atualizar estimativa]** para atualizar os dados.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que exige que o tempo atual seja ≥ 80 graus.

1. Clique em **[!UICONTROL Salvar]** para confirmar.

1. Depois que a regra for criada, ela será exibida na lista **[!UICONTROL Regras]**. Você pode selecioná-la para exibir suas propriedades e editá-la ou excluí-la.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>No momento, não há suporte no [!DNL Journey Optimizer] para ofertas baseadas em eventos. Se você criar uma regra de decisão baseada em um [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=pt-BR#events){target="_blank"}, não poderá aproveitá-la em uma oferta.

## Tutorial em vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
