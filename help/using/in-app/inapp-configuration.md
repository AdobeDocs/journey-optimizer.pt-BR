---
title: Configuração no aplicativo
description: Saiba como configurar seu ambiente para enviar mensagens no aplicativo com o Journey Optimizer
role: Admin
level: Intermediate
keywords: no aplicativo, mensagem, configuração, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 11%

---

# Configuração do canal no aplicativo {#inapp-configuration}

Antes de enviar mensagens no aplicativo, é necessário configurar o canal no aplicativo no [!DNL Adobe Experience Platform Data Collection].

1. Do seu [!DNL Adobe Experience Platform Data Collection] , acesse o **[!UICONTROL Sequência de dados]** e clique em **[!UICONTROL Nova sequência de dados]**. Para obter mais informações sobre a criação de sequências de dados, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=pt-BR).

1. Selecione o [!DNL Adobe Experience Platform] serviço.

   [!DNL Edge Segmentation] e [!DNL Adobe Journey Optimizer] deve ser selecionado.

   ![](assets/inapp_config_6.png)

1. Em seguida, acesse o **[!UICONTROL Superfícies do aplicativo]** e clique em **[!UICONTROL Criar superfície do aplicativo]**.

   >[!NOTE]
   >
   > Você precisa do **Gerenciar configuração do aplicativo** permissão para ter acesso à **[!UICONTROL Superfícies do aplicativo]** menu. Para obter mais informações, consulte [este vídeo](#video).

   ![](assets/inapp_config_1.png)

1. Adicione um nome ao seu **[!UICONTROL Superfície do aplicativo]**.


1. No menu suspenso Apple iOS, digite seu **ID do pacote do iOS**. Consulte [Documentação do Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obter mais informações sobre **ID do pacote**.

   ![](assets/inapp_config_2.png)

1. No menu suspenso do Android, digite seu **Nome do pacote Android**. Consulte [Documentação do Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obter mais informações sobre **Nome do pacote**.

1. Clique em **[!UICONTROL Salvar]** quando terminar a configuração do seu **[!UICONTROL Superfície do aplicativo]**.

   ![](assets/inapp_config_3.png)

   Seu **[!UICONTROL Superfície do aplicativo]** Agora estarão disponíveis ao criar uma nova campanha com uma mensagem no aplicativo. [Saiba mais](create-in-app.md)

1. Depois de criar sua superfície de aplicativo, agora é necessário criar uma propriedade móvel.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para o procedimento detalhado.

   ![](assets/inapp_config_4.png)

1. No menu Extensões da propriedade recém-criada, instale as seguintes extensões:

   * Rede de borda da Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimento
   * Identidade
   * Núcleo móvel
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) para o procedimento detalhado.

   ![](assets/inapp_config_5.png)

O canal no aplicativo agora está configurado. Você pode começar a enviar mensagens no aplicativo para seus usuários.

**Tópicos relacionados:**

* [Criação de uma mensagem no aplicativo](create-in-app.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)


## Vídeos tutoriais{#video}

* O vídeo abaixo mostra como atribuir a variável **Gerenciar configuração do aplicativo** permissão para acessar o menu Superfícies do aplicativo.

  +++Ver vídeo
  >[!VIDEO](https://video.tv.adobe.com/v/3421607)
+++
