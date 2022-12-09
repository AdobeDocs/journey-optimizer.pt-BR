---
title: Configuração no aplicativo
description: Saiba como configurar seu ambiente para enviar mensagens no aplicativo com o Journey Otimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Configurar canal no aplicativo {#inapp-configuration}

Antes de enviar mensagens no aplicativo, é necessário configurar o canal no aplicativo em [!DNL Adobe Experience Platform Data Collection].

1. Em seu [!DNL Adobe Experience Platform Data Collection] , acesse a **[!UICONTROL Datastream]** e clique em **[!UICONTROL New datastream]**. Para obter mais informações sobre a criação de conjunto de dados, consulte [esta página](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Selecione o [!DNL Adobe Experience Platform] serviço.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] e [!DNL Adobe Journey Optimizer] deve ser selecionado.

   ![](assets/inapp_config_6.png)

1. Em seguida, acesse o **[!UICONTROL App surfaces]** , em seguida, clique em **[!UICONTROL Create App surface]**.

   ![](assets/inapp_config_1.png)

1. Adicione um nome a **[!UICONTROL App surface]**.

1. No menu suspenso Apple iOS , digite seu **ID do pacote do iOS**. Consulte [Documentação da Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obter mais informações sobre **ID do pacote**.

   ![](assets/inapp_config_2.png)

1. No menu suspenso Android , digite o **Nome do pacote do Android**. Consulte [Documentação do Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obter mais informações sobre **Nome do pacote**.

1. Clique em **[!UICONTROL Save]** ao concluir a configuração do **[!UICONTROL App surface]**.

   ![](assets/inapp_config_3.png)

   Seu **[!UICONTROL App surface]** O agora estará disponível ao criar uma nova campanha com uma mensagem no aplicativo. [Saiba mais](create-in-app.md)

1. Depois de criar a superfície do aplicativo, agora é necessário criar uma propriedade móvel.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para o procedimento pormenorizado.

   ![](assets/inapp_config_4.png)

1. No menu Extensões da propriedade recém-criada, instale as seguintes extensões:

   * Rede de borda da Adobe Experience Platform
   * Adobe Journey Otimizer
   * Garantia da AEP
   * Consentimento
   * Identificar
   * Mobile Core
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) para o procedimento pormenorizado.

   ![](assets/inapp_config_5.png)

O canal no aplicativo agora está configurado. Você pode começar a enviar mensagens no aplicativo para seus usuários.

**Tópicos relacionados:**

* [Criar uma mensagem no aplicativo](create-in-app.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](inapp-report.md)
