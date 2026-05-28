---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Trabalhar com eventos de gestão de decisões
description: Saiba como criar relatórios de gestão de decisões na Adobe Experience Platform.
badge: label="Legado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# Introdução aos eventos de Gestão de decisões {#monitor-offer-events}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

Cada vez que a Gestão de decisões toma uma decisão para determinado perfil, as informações relacionadas a esses eventos são automaticamente enviadas para a Adobe Experience Platform.

Isso permite obter insights sobre suas decisões, por exemplo, para saber qual oferta foi apresentada a um determinado perfil. É possível exportar esses dados para analisá-los em seu próprio sistema de relatórios ou aproveitar o [serviço de consultas](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=pt-BR) da Adobe Experience Platform em combinação com outras ferramentas para aprimorar a análise e os relatórios.

## Informações importantes disponíveis em conjuntos de dados {#key-information}

Cada evento enviado quando uma decisão é tomada contém quatro pontos de dados principais que podem ser aproveitados para fins de análise e relatórios:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Substituta]**: nome e ID da oferta substituta, se nenhuma oferta personalizada foi selecionada,
* **[!UICONTROL Posicionamento]**: nome, ID e canal do posicionamento usado para entregar a oferta,
* **[!UICONTROL Seleções]**: nome e ID da oferta selecionada para o perfil,
* **[!UICONTROL Atividade]**: nome e ID da decisão.

Além disso, também é possível aproveitar os campos **[!UICONTROL identityMap]** e **[!UICONTROL Carimbo de data e hora]** para recuperar informações sobre o perfil e a hora na qual a oferta foi entregue.

Para obter mais informações sobre todos os campos XDM enviados com cada decisão, consulte [esta seção](xdm-fields.md).

## Acessar conjuntos de dados {#access-datasets}

Os conjuntos de dados contendo eventos da Gestão de decisões podem ser acessados no menu **[!UICONTROL Conjuntos de dados]** da Adobe Experience Platform. Um conjunto de dados é criado automaticamente no provisionamento para cada uma de suas instâncias.

![](../assets/events-datasets-list.png)

Esses conjuntos de dados são baseados no esquema **[!UICONTROL ODE DecisionEvents]** que contém todos os campos XDM necessários para enviar informações da Gestão de decisões para a Adobe Experience Platform.

>[!NOTE]
>
>Observe que os conjuntos de dados do ODE DecisionEvents são **conjuntos de dados que não são de perfil**, o que significa que eles não podem ser assimilados na Experience Platform para serem usados pelo perfil do cliente em tempo real.
