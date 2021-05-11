---
title: Configuração de notificação por push
description: Saiba como configurar seu ambiente para enviar notificações por push com o Journey Optimizer
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 2%

---

# Configuração de notificação por push {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## Introdução à configuração de push {#gs-push}

Antes de começar a enviar notificações por push com [!DNL Journey Optimizer], é necessário definir as configurações em [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch].

## Configurações do Adobe Experience Platform {#platform-settings}

Para configurar seu aplicativo móvel em [!DNL Adobe Experience Platform Launch], siga estas etapas:

1. [Atribuir direitos de propriedade e de empresa](#push-rights)
1. [Adicione as credenciais de push do aplicativo móvel no Platform launch](#push-credentials-launch).
1. [Criar ](#edge-configuration) configuração de borda a ser usada pela  **[!UICONTROL Edge]** extensão para enviar dados personalizados de dispositivo móvel para  [!DNL Adobe Experience Platform].
1. [Configurar uma propriedade](#launch-property) Platform launch.
1. [Publique a propriedade](#publish-property).
1. [Configure ProfileDataSource](#configure-profiledatasource).

### Etapa 1: Atribuir direitos de propriedade e empresa {#push-rights}

Antes de criar um aplicativo móvel, primeiro verifique se você tem ou atribui as permissões de usuário corretas.

Para obter mais informações sobre o gerenciamento de usuários com [!DNL Adobe Experience Platform Launch], consulte [documentação do Platform launch](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions).

Para atribuir direitos de Propriedade e Empresa:

1. Acesse o [!DNL Admin Console].

1. Na guia **[!UICONTROL Products]**, selecione o cartão **[!UICONTROL Adobe Experience Platform Launch]**.

   ![](assets/push_product_1.png)

1. Selecione um **[!UICONTROL Product Profile]** existente ou crie um novo com o botão **[!UICONTROL New profile]**. Para obter mais informações sobre como criar um novo **[!UICONTROL New profile]**, consulte a [documentação do Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui).

1. Na guia **[!UICONTROL Permissions]**, selecione **[!UICONTROL Property rights]**.

   ![](assets/push_product_2.png)

1. Clique em **[!UICONTROL Add all]**. Isso adicionará os seguintes direitos ao perfil de produto:
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. Em seguida, selecione **[!UICONTROL Company rights]** no menu à esquerda.

   ![](assets/push_product_4.png)

1. Adicione os seguintes direitos:

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. Clique em **[!UICONTROL Save]**.

Para atribuir esse **[!UICONTROL Product profile]** aos usuários:

1. Na guia [!DNL Admin Console], na guia **[!UICONTROL Products]**, selecione o cartão **[!UICONTROL Adobe Experience Platform Launch]**.

1. Selecione o **[!UICONTROL Product profile]** configurado anteriormente.

1. Na guia **[!UICONTROL Users]**, clique em **[!UICONTROL Add user]**.

   ![](assets/push_product_6.png)

1. Digite o nome do usuário ou endereço de email e selecione o usuário. Em seguida, clique em **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Se o usuário não tiver sido criado anteriormente no Admin Console, consulte a [Documentação Adicionar usuários](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


Agora você tem as permissões de usuário corretas para criar e configurar um aplicativo móvel em [!DNL Adobe Experience Platform Launch].

### Etapa 2: Adicionar suas credenciais de push do aplicativo móvel no Platform launch {#push-credentials-launch}

>[!NOTE]
>
> Para adicionar credenciais de push em [!DNL Adobe Experience Platform Launch], o proprietário do aplicativo móvel deve buscá-las no APNs/FCM.

1. Em [!DNL Adobe Experience Platform Launch], verifique se **[!UICONTROL Client Side]** está selecionado no menu suspenso.

1. Selecione a guia **[!UICONTROL App Configurations]** no painel esquerdo e clique em **[!UICONTROL App Configuration]** para criar uma nova configuração.

1. Insira um **[!UICONTROL Name]** para a configuração.

1. No menu suspenso **[!UICONTROL Messaging Service Type]**, selecione o **[!UICONTROL Messaging service type]** a ser usado para essas credenciais. Aqui, selecionamos **[!UICONTROL Apple Push Notification Service]** já que estamos trabalhando com o iOS.

1. Insira o aplicativo móvel **[!UICONTROL Bundle Id]** no campo **[!UICONTROL App ID (iOS Bundle ID)]** se estiver usando o serviço de notificação por push da Apple ou no campo **[!UICONTROL App ID (Android package name)]** se estiver usando o Firebase Cloud Messaging.

   ![](assets/push_launch_app_configuration.png)

1. Arraste e solte o arquivo de chave .p8 ou o arquivo de chave privada .json para o campo **[!UICONTROL Push Credentials]**.

1. Insira **[!UICONTROL Key Id]** e **[!UICONTROL Team Id]** se estiver usando o serviço de notificação por push da Apple.

1. Clique em **[!UICONTROL Save]** para criar a configuração do aplicativo.

### Etapa 3: Criar configuração de borda {#edge-configuration}

**[!UICONTROL Edge configuration]** é usada por  **[!UICONTROL Edge]** extensão para enviar dados personalizados de dispositivo móvel para  [!DNL Adobe Experience Platform].
Para configurar [!DNL Adobe Experience Platform], você deve fornecer o nome **[!UICONTROL Sandbox]** e **[!UICONTROL Event Dataset]**.

1. Em [!DNL Adobe Experience Platform Launch], selecione a guia **[!UICONTROL Edge Configurations]** e clique em **[!UICONTROL Edge Configurations]**.

1. Selecione **[!UICONTROL New Edge Configuration]** para adicionar um novo **[!UICONTROL Edge Configuration]**.
1. Insira um **[!UICONTROL Name]** e clique em **[!UICONTROL Save]**

1. Clique no botão **[!UICONTROL Adobe Experience Platform]** para ativá-lo.

1. Preencha os campos **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** e **[!UICONTROL Profile Dataset]**. Em seguida, clique em **[!UICONTROL Save]**.

   ![](assets/push-config-4.png)

### Etapa 4: Configurar uma propriedade de Platform launch {#launch-property}

A configuração de uma propriedade [!DNL Adobe Experience Platform Launch] permite que o desenvolvedor de aplicativos ou profissional de marketing móvel configure os atributos de SDKs móveis, como Tempo limite da sessão, a sandbox [!DNL Adobe Experience Platform] a ser direcionada e o **[!UICONTROL Adobe Experience Platform Datasets]** a ser usado para o SDK móvel enviar dados.

1. Em [!DNL Adobe Experience Platform Launch], verifique se **[!UICONTROL Client Side]** está selecionado no menu suspenso.

1. selecione a guia **[!UICONTROL Properties]** e clique em **[!UICONTROL New Property]**.

   ![](assets/push-config-6.png)

1. Insira um **[!UICONTROL Name]** para sua nova propriedade.

1. Selecione **[!UICONTROL Mobile]** como **[!UICONTROL Platform]**.

   ![](assets/push-config-7.png)

1. Clique em **[!UICONTROL Save]** para criar sua nova propriedade.

Para obter os SDKs necessários para que a notificação por push funcione, você precisará das seguintes extensões do SDK, tanto para Android quanto para iOS:

* **[!UICONTROL Mobile Core]** (instalado automaticamente)
* **[!UICONTROL Profile]** (instalado automaticamente)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, opcional, mas recomendado para depurar a implementação móvel.

Para saber mais sobre as extensões [!DNL Adobe Experience Platform Launch], consulte a [documentação do Platform launch](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).

Para configurar **[!UICONTROL Adobe Experience Platform Edge Extension]** para enviar dados personalizados de dispositivos móveis para [!DNL Adobe Experience Platform].

1. Selecione a propriedade criada anteriormente e selecione a guia **[!UICONTROL Extensions]** para exibir as extensões dessa propriedade.

   ![](assets/push-config-8.png)

1. Clique em **[!UICONTROL Configure]** na extensão **[!UICONTROL Adobe Experience Platform Edge]** Rede&#39;.

1. Na lista suspensa **[!UICONTROL Edge Configuration]**, selecione o **[!UICONTROL Edge Configuration]** criado nas etapas anteriores. Para obter mais informações sobre **[!UICONTROL Edge Configuration]**, consulte esta [seção](#edge-configuration).

1. Clique em **[!UICONTROL Save]**.

Para configurar a extensão **[!UICONTROL Adobe Experience Platform Messaging]** para enviar interações por push e perfil para os conjuntos de dados corretos, siga as mesmas etapas descritas acima. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** e **[!UICONTROL  Profile Dataset]** criadas no [Adobe Experience Platform setup](#edge-configuration).

### Etapa 5: Publicar a propriedade {#publish-property}

Agora, é necessário publicar a propriedade para integrar sua configuração e usá-la no aplicativo móvel.
Para publicar sua propriedade, consulte as etapas detalhadas em [Documentação do SDK do Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

### Etapa 6: Configurar o ProfileDataSource {#configure-profiledatasource}

Para configurar o `ProfileDataSource`, use o `ProfileDCInletURL` da configuração [!DNL Adobe Experience Platform] e adicione o seguinte no aplicativo móvel:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->
