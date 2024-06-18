---
title: Aproveitar dados de contexto no Experience Decisioning
description: Saiba como aproveitar dados de contexto no Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidade limitada"
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: 2349145fcf698769d16326a19a48a413a3c1dd95
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Aproveitar dados de contexto no Experience Decisioning {#context}

Com o Experience Decisioning, você pode aproveitar todas as informações disponíveis no Adobe Experience Platform para executar várias ações, como criar [regras de decisão](rules.md) ou [fórmulas de classificação](ranking.md). Por exemplo, você pode projetar uma regra de decisão que exija que o tempo atual seja ≥ 80 graus no momento em que a solicitação de decisão é feita.

>[!NOTE]
>
>Os dados de contexto são definidos no Adobe Experience Platform e enviados no momento de uma solicitação de decisão. Ela não inclui dados históricos.

Para usar dados de contexto, primeiro é necessário definir os dados que deseja disponibilizar no Experience Decisioning. Depois de concluídos, esses dados se integram perfeitamente ao Experience Decisioning na **[!UICONTROL Dados de contexto]** guia disponível ao criar uma regra de decisão. Você também pode aproveitar os dados ao editar uma fórmula de classificação.

![](assets/decision-rules-context.png)

As etapas para alimentar o Experience Decisioning com dados do Adobe Experience Platform são as seguintes:

1. Criar um **Esquema do evento de experiência**  no Adobe Experience Platform e em seus componentes **conjunto de dados**. [Saiba como criar esquemas](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Criar um novo fluxo de dados do Adobe Experience Platform:

   1. Navegue até a **[!UICONTROL Datastreams]** e selecione **[!UICONTROL Nova sequência de dados]**.

   1. No **[!UICONTROL Esquema de evento]** selecione o schema de Evento de experiência criado anteriormente e clique em **[!UICONTROL Salvar]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Clique em **[!UICONTROL Adicionar serviço]** e selecione &quot;Adobe Experience Platform&quot; como o serviço. No **[!UICONTROL Conjunto de dados do evento]** selecione o conjunto de dados de evento criado anteriormente e ative a variável **[!UICONTROL Adobe Journey Optimizer]** opção.

      ![](assets/decision-rules-context-datastream-service.png)

Depois que a sequência de dados é salva, as informações do conjunto de dados selecionado são buscadas automaticamente e integradas ao Experience Decisioning, normalmente ficando disponíveis em aproximadamente 24 horas.

Para obter mais orientações sobre como trabalhar com o Adobe Experience Platform, explore os seguintes recursos:

* [Esquemas do Experience Data Model (XDM)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Conjuntos de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Datastreams](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
