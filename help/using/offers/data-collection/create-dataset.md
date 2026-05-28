---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Criar um conjunto de dados para coletar eventos
description: Saiba como criar um conjunto de dados para coletar eventos
badge: label="Legado" type="Informative"
feature: Ranking, Decision Management, Datasets
role: Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SnbdXcSaDXxO1OapmRL3YYwRmCbBFqcuPlxFt-NEZCc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 15%

---

# Criar um conjunto de dados para coletar eventos {#create-dataset}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

Para coletar eventos de experiência, primeiro é necessário criar um conjunto de dados para onde esses eventos serão enviados.

Comece criando o esquema que será usado no seu conjunto de dados:

1. No menu **[!UICONTROL Data Management]**, selecione **[!UICONTROL Schema]**.

1. Clique em **[!UICONTROL Criar esquema]**, na parte superior direita, selecione **[!UICONTROL Evento de experiência]** e clique em **Avançar**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. Insira um nome e uma descrição para o esquema e clique em **Concluir**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Na seção **[!UICONTROL Grupos de campos]** à esquerda, selecione **[!UICONTROL Adicionar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. No campo **[!UICONTROL Pesquisa]**, digite &quot;interação de proposta&quot;.

1. Selecione o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** e clique em **[!UICONTROL Adicionar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >O esquema que será usado no seu conjunto de dados deve ter o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** associado a ele. Caso contrário, você não poderá usá-lo no modelo de IA.

1. Salve o esquema.

>[!NOTE]
>
>Saiba mais sobre a criação de esquemas em [Noções básicas sobre a composição de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

agora você está pronto para criar um conjunto de dados usando esse esquema. Para fazer isso, siga as etapas abaixo:

1. No menu **[!UICONTROL Data Management]**, selecione **[!UICONTROL Datasets]** e vá para a guia **[!UICONTROL Browse]**.

1. Clique em **[!UICONTROL Criar conjunto de dados]** e selecione **[!UICONTROL Criar conjunto de dados do esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecione o esquema que acabou de criar na lista e clique em **[!UICONTROL Avançar]**.

1. Forneça um nome exclusivo para o conjunto de dados no campo **[!UICONTROL Nome]** e clique em **[!UICONTROL Concluir]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Este conjunto de dados agora pode ser selecionado para coletar dados do evento ao [criar um modelo de IA](../ranking/create-ranking-strategies.md).
