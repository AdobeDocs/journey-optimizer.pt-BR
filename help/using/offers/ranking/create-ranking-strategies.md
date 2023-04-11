---
product: experience platform
solution: Experience Platform
title: Criar modelos de IA
description: Saiba como criar modelos de IA para classificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 6%

---

# Criar modelos de IA {#ai-rankings}

[!DNL Journey Optimizer] permite criar **Modelos de IA** para classificar ofertas com base em suas metas de negócios.

>[!CAUTION]
>
>Para criar, editar ou excluir modelos de IA, você deve ter a variável **Gerenciar estratégias de classificação** permissão. [Saiba mais](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Criar um modelo de IA {#create-ranking-strategy}

Para criar um modelo de IA, siga as etapas abaixo:

1. Crie um conjunto de dados no qual os eventos de conversão serão coletados. [Saiba como](../data-collection/create-dataset.md)

1. No **[!UICONTROL Componentes]** acesse o **[!UICONTROL Classificação]** e selecione **[!UICONTROL Modelos de IA]**.

   ![](../assets/ai-ranking-list.png)

   Todos os modelos de IA criados até agora são listados.

1. Clique no botão **[!UICONTROL Criar modelo de IA]** botão.

1. Especifique um nome exclusivo e uma descrição para o modelo de IA e selecione o tipo de modelo de IA que deseja criar:

   * **[!UICONTROL Otimização automática]** O otimiza as ofertas com base no desempenho da oferta anterior. [Saiba mais](auto-optimization-model.md)
   * **[!UICONTROL Personalizado]** otimiza e personaliza as ofertas com base em segmentos e no desempenho da oferta. [Saiba mais](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >O **[!UICONTROL Métrica de otimização]** A seção fornece informações sobre o evento de conversão usado pelo modelo de IA para calcular a classificação das ofertas.
   >
   >[!DNL Journey Optimizer] Classifique as ofertas com base na **taxa de conversão** (Índice de conversão = Número total de eventos de conversão / Número total de eventos de impressão). A taxa de conversão é calculada usando dois tipos de métricas:
   >* **Eventos de impressão** (ofertas exibidas)
   >* **Eventos de conversão** (ofertas que resultam em cliques por email ou pela Web).

   >
   >Esses eventos são capturados automaticamente usando o SDK da Web ou o SDK móvel fornecido. Saiba mais sobre isso em [Visão geral do SDK da Web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR).

1. Selecione os conjuntos de dados em que os eventos de conversão e impressão são coletados. Saiba como criar esse conjunto de dados em [esta seção](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Somente os conjuntos de dados criados a partir de esquemas associados ao **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos (anteriormente conhecido como mixin) são exibidos na lista suspensa.

1. Se você estiver criando um **[!UICONTROL Personalização]** Modelo de IA, selecione os segmentos a serem usados para treinar o modelo de IA.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >É possível selecionar até 5 segmentos.

1. Salve e ative o modelo de IA.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Agora, cada vez que uma oferta é exibida e/ou clicada, você deseja que o evento correspondente seja capturado automaticamente pela variável **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos que usa a variável [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou Mobile SDK.

Para poder enviar tipos de evento (oferta exibida ou oferta clicada), você deve definir o valor correto para cada tipo de evento em um evento de experiência enviado para o Adobe Experience Platform. [Saiba como](../data-collection/schema-requirement.md)