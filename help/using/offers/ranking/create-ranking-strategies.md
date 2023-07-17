---
product: experience platform
solution: Experience Platform
title: Criar modelos de IA
description: Saiba como criar modelos de IA para classificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 7%

---

# Criar modelos de IA {#ai-rankings}

[!DNL Journey Optimizer] permite criar **Modelos de IA** para classificar ofertas com base em suas metas comerciais.

>[!CAUTION]
>
>Para criar, editar ou excluir modelos de IA, você deve ter a **Gerenciar estratégias de classificação** permissão. [Saiba mais](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Criar um modelo de IA {#create-ranking-strategy}

Para criar um modelo de IA, siga as etapas abaixo:

1. Crie um conjunto de dados em que os eventos de conversão serão coletados. [Saiba como](../data-collection/create-dataset.md)

1. No **[!UICONTROL Componentes]** , acesse o **[!UICONTROL Classificação]** e selecione **[!UICONTROL Modelos de IA]**.

   ![](../assets/ai-ranking-list.png)

   Todos os modelos de IA criados até o momento estão listados.

1. Clique em **[!UICONTROL Criar modelo de IA]** botão.

1. Especifique um nome exclusivo e uma descrição para o modelo de IA e selecione o tipo de modelo de IA que deseja criar:

   * **[!UICONTROL Otimização automática]** otimiza ofertas com base no desempenho de ofertas anteriores. [Saiba mais](auto-optimization-model.md)
   * **[!UICONTROL Otimização personalizada]** O otimiza e personaliza ofertas com base em públicos-alvo e desempenho da oferta. [Saiba mais](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >A variável **[!UICONTROL Métrica de otimização]** A seção fornece informações sobre o evento de conversão usado pelo modelo de IA para calcular a classificação das ofertas.
   >
   >[!DNL Journey Optimizer] classificar ofertas com base na **taxa de conversão** (Taxa de conversão = Número total de eventos de conversão / Número total de eventos de impressão). A taxa de conversão é calculada usando dois tipos de métricas:
   >* **Eventos de impressão** (ofertas exibidas)
   >* **Eventos de conversão** (ofertas que resultam em cliques por email ou pela Web).
   >
   >Esses eventos são capturados automaticamente usando o SDK da Web ou o SDK móvel fornecido. Saiba mais sobre isso em [Visão geral do SDK da Web do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR).

1. Selecione os conjuntos de dados nos quais os eventos de conversão e impressão são coletados. Saiba como criar esse conjunto de dados no [nesta seção](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Somente os conjuntos de dados criados a partir de esquemas associados à **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos (anteriormente conhecido como mixin) são exibidos na lista suspensa.

1. Se você estiver criando uma **[!UICONTROL Otimização personalizada]** Modelo de IA, selecione os segmentos a serem usados para treinar o modelo de IA.

   ➡️ [Descubra este recurso no vídeo](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Você pode selecionar até 5 públicos-alvo.

1. Salve e ative o modelo de IA.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Agora, sempre que uma oferta for exibida e/ou clicada, você desejará que o evento correspondente seja capturado automaticamente pelo **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos usando o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou Mobile SDK.

Para enviar tipos de evento (oferta exibida ou oferta clicada), você deve definir o valor correto para cada tipo de evento em um evento de experiência enviado para o Adobe Experience Platform. [Saiba como](../data-collection/schema-requirement.md)

## Vídeo explicativo {#video}

Saiba como criar um modelo de otimização personalizado e como aplicá-lo a uma decisão.

>[!VIDEO](https://video.tv.adobe.com/v/3419954?quality=12)
