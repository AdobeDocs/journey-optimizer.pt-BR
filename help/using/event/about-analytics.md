---
solution: Journey Optimizer
product: journey optimizer
title: Sobre dados do Adobe Analytics
description: Saiba como aproveitar os dados do Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: a6735063ec68b40b1441b379a20cba8953b59447
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Aproveitar os dados do Adobe Analytics{#analytics-data}

Você pode aproveitar todos os dados de evento comportamental do Adobe Analytics que já estão sendo capturados e transmitidos na Adobe Experience Platform para acionar jornadas e automatizar experiências para seus clientes.

>[!NOTE]
>
>Esta seção se aplica somente a eventos com base em regras e clientes que precisam usar os dados do Adobe Analytics.

Para que isso funcione, é necessário ativar, na Adobe Experience Platform, o conjunto de relatórios que deseja usar. Para fazer isso, siga as etapas abaixo:

1. Conecte-se à Adobe Experience Platform e navegue até **[!UICONTROL Sources]**.
1. Na seção Adobe Analytics , selecione **[!UICONTROL Add data]**: a lista de conjuntos de relatórios disponíveis do Adobe Analytics é exibida.

1. Selecione o conjunto de relatórios que será ativado, clique em **[!UICONTROL Next]** e **[!UICONTROL Finish]**.

1. Compartilhe a ID de dados de origem com o ponto de contato do programa Beta.

Isso ativa o conector de origem do Analytics para esse conjunto de relatórios. Sempre que os dados entram, eles são transformados em um evento de Experiência e enviados para a Adobe Experience Platform.

![](assets/jo-event9.png)

Saiba mais sobre o conector de origem do Adobe Analytics em  [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target=&quot;_blank&quot;} e [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target=&quot;_blank&quot;}.
