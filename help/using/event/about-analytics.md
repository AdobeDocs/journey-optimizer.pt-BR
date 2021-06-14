---
title: Sobre dados do Adobe Analytics
description: Saiba como aproveitar os dados do Adobe Analytics
feature: Eventos
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# Como aproveitar os dados do Adobe Analytics{#analytics-data}

![](../assets/do-not-localize/badge.png)

>[!NOTE]
>
>Esta seção se aplica somente a eventos com base em regras e clientes que precisam usar dados do Adobe Analytics.

Você pode aproveitar todos os dados de evento comportamental do Adobe Analytics que já estão sendo capturados e transmitidos na plataforma para acionar jornadas e automatizar experiências para seus clientes.

Para que isso funcione, é necessário ativar, no Adobe Experience Platform, o conjunto de relatórios que deseja aproveitar:

1. No Adobe Experience Platform, selecione **[!UICONTROL Sources]** e **[!UICONTROL Add data]** na seção Adobe Analytics. A lista de conjuntos de relatórios disponíveis do Adobe Analytics é exibida.

1. Escolha o conjunto de relatórios que deseja habilitar, clique em **[!UICONTROL Next]** e clique em **[!UICONTROL Finish]**.

1. Compartilhe a ID de dados de origem com o ponto de contato do programa Beta.

Isso ativa o conector de origem do Analytics para esse conjunto de relatórios. Sempre que os dados entram, eles são transformados em um evento de Experiência e enviados para o Adobe Experience Platform.

![](../assets/jo-event9.png)

Para obter mais informações sobre o conector de origem do Adobe Analytics, consulte a [documentação]https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) e o [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html).
