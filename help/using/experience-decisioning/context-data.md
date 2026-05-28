---
title: Aproveitar dados de contexto no Decisioning
description: Saiba como aproveitar os dados de contexto no Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/tL3mwS9sDtSkSVljry1EeqPnYn4U34TvXCg5jX2ej3M
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# Aproveitar dados de contexto no Decisioning {#context}

Com o Decisioning, você pode aproveitar todas as informações disponíveis no Adobe Experience Platform para executar várias ações, como criar [regras de decisão](rules.md) ou [fórmulas de classificação](ranking/ranking.md).

Por exemplo, você pode projetar uma regra de decisão que exija que o tempo atual seja ≥ 80 graus no momento em que a solicitação de decisão é feita.

>[!NOTE]
>
>Os dados de contexto são definidos no Adobe Experience Platform e enviados no momento de uma solicitação de decisão. Ela não inclui dados históricos.

Para usar dados de contexto, primeiro é necessário definir os dados que deseja disponibilizar no Decisioning. Depois de concluídos, esses dados se integram perfeitamente à Decisão na guia **[!UICONTROL Dados de contexto]** disponível ao criar uma regra de decisão. Você também pode aproveitar os dados ao editar uma fórmula de classificação.

![](assets/decision-rules-context.png)

As etapas para alimentar a Decisão com dados do Adobe Experience Platform são as seguintes:

1. Crie um **esquema de Evento de Experiência** no Adobe Experience Platform e seu **conjunto de dados** associado. [Saiba como criar esquemas](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Criar um novo fluxo de dados do Adobe Experience Platform:

   1. Navegue até o menu **[!UICONTROL Datastreams]** e selecione **[!UICONTROL Novo Datastream]**.

   1. Na lista suspensa **[!UICONTROL Esquema de evento]**, selecione o esquema de Evento de experiência criado anteriormente e clique em **[!UICONTROL Salvar]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Clique em **[!UICONTROL Adicionar serviço]** e selecione &quot;Adobe Experience Platform&quot; como o serviço. Na lista suspensa **[!UICONTROL Conjunto de Dados do Evento]**, selecione o conjunto de dados do evento criado anteriormente e habilite a opção **[!UICONTROL Adobe Journey Optimizer]**.

      ![](assets/decision-rules-context-datastream-service.png)

Depois que a sequência de dados é salva, as informações do conjunto de dados selecionado são buscadas automaticamente e integradas ao Decisioning, normalmente ficando disponíveis em aproximadamente 24 horas.

Para obter mais orientações sobre como trabalhar com o Adobe Experience Platform, explore os seguintes recursos:

* [Esquemas do Experience Data Model (XDM)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Conjuntos de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Sequências de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
