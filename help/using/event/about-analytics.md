---
title: Sobre dados do Adobe Analytics
description: Saiba como aproveitar os dados do Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 587ac4a17db71790ed4d9ee07214293a2882180c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 8%

---

# Aproveite os dados do Adobe Analytics{#analytics-data}

Você pode aproveitar todos os dados de evento comportamental do Adobe Analytics que já estão sendo capturados e transmitidos na plataforma para acionar jornadas e automatizar experiências para seus clientes.

>[!NOTE]
>
>Esta seção se aplica somente a eventos com base em regras e clientes que precisam usar dados do Adobe Analytics.

Para que isso funcione, é necessário ativar, no Adobe Experience Platform, o conjunto de relatórios que deseja aproveitar:

1. No Adobe Experience Platform, selecione **[!UICONTROL Sources]** then **[!UICONTROL Add data]** na seção Adobe Analytics . A lista de conjuntos de relatórios disponíveis do Adobe Analytics é exibida.

1. Escolha o conjunto de relatórios que deseja ativar, clique em **[!UICONTROL Next]** e clique em **[!UICONTROL Finish]**.

1. Compartilhe a ID de dados de origem com o ponto de contato do programa Beta.

Isso ativa o conector de origem do Analytics para esse conjunto de relatórios. Sempre que os dados entram, eles são transformados em um evento de Experiência e enviados para o Adobe Experience Platform.

![](assets/jo-event9.png)

Saiba mais sobre o conector de origem do Adobe Analytics em  [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=pt-BR){target=&quot;_blank&quot;} e [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=pt-BR){target=&quot;_blank&quot;}.
