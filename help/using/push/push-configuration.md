---
solution: Journey Optimizer
product: journey optimizer
title: Configuração de notificação por push
description: Saiba como configurar seu ambiente para enviar notificações por push com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1536'
ht-degree: 4%

---

# Configurar canal de notificação por push {#push-notification-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo. Antes de começar a enviar notificações por push com [!DNL Journey Optimizer], é necessário garantir que as configurações e integrações estejam em vigor no aplicativo móvel e para tags no Adobe Experience Platform. Para entender o fluxo de dados das notificações por push em [!DNL Adobe Journey Optimizer] consulte [esta página](push-gs.md).

## Antes de começar {#before-starting}

<!--
### Check provisioning

Your Adobe Experience Platform account must be provisioned to contain following schemas and datasets for push notification data flow to function correctly:

| Schema <br>Dataset                                                                       | Group of fields                                                                                                                                                                         | Operation                                                |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM Push Profile Schema <br>CJM Push Profile Dataset                                     | Push Notification Details<br>Adobe CJM ExperienceEvent - Message Profile Details<br>Adobe CJM ExperienceEvent - Message Execution Details<br>Application Details<br>Environment Details | Register Push Token                                      |
| CJM Push Tracking Experience Event Schema<br>CJM Push Tracking Experience Event Dataset | Push Notification Tracking                                                                                                                                                              | Track interactions and provide data for the reporting UI |
-->

### Configurar permissões {#setup-permissions}

Antes de criar um aplicativo móvel, primeiro verifique se você tem ou atribui as permissões de usuário corretas para tags no Adobe Experience Platform. Saiba mais em [Documentação de tags](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

>[!CAUTION]
>
>A configuração de push deve ser executada por um usuário especialista. Dependendo do modelo de implementação e das pessoas envolvidas nessa implementação, talvez seja necessário atribuir o conjunto completo de permissões a um único perfil de produto ou compartilhar permissões entre o desenvolvedor do aplicativo e a **Adobe Journey Optimizer** administrador. Saiba mais sobre **Tags** permissões em [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

Para atribuir **Propriedade** e **Empresa** , siga as etapas abaixo:

1. Acesse o **[!DNL Admin Console]**.

1. No **[!UICONTROL Produtos]** selecione a guia **[!UICONTROL Coleta de dados do Adobe Experience Platform]** cartão.

   ![](assets/push_product_1.png)

1. Selecione um **[!UICONTROL Perfil de produto]** ou criar um novo com o **[!UICONTROL Novo perfil]** botão. Saiba como criar um novo **[!UICONTROL Novo perfil]** no [Documentação do Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target="_blank"}.

1. No **[!UICONTROL Permissões]** guia , selecione **[!UICONTROL Direitos de propriedade]**.

   ![](assets/push_product_2.png)

1. Clique em **[!UICONTROL Adicionar tudo]**. Isso adicionará o seguinte direito ao perfil de produto:
   * **[!UICONTROL Aprovar]**
   * **[!UICONTROL Desenvolver]**
   * **[!UICONTROL Gerenciar ambientes]**
   * **[!UICONTROL Gerenciar extensões]**
   * **[!UICONTROL Publicar]**

   Essas permissões são necessárias para instalar e publicar a extensão do Adobe Journey Optimizer e publicar a propriedade do aplicativo no Adobe Experience Platform Mobile SDK.

1. Em seguida, selecione **[!UICONTROL Direitos da empresa]** no menu à esquerda.

   ![](assets/push_product_4.png)

1. Adicione os seguintes direitos:

   * **[!UICONTROL Gerenciar configurações do aplicativo]**
   * **[!UICONTROL Gerenciar propriedades]**

   Essas permissões são necessárias para que o desenvolvedor do aplicativo móvel configure credenciais de push em **Coleta de dados do Adobe Experience Platform** e definir as superfícies do canal de Notificação por push (ou seja, predefinições de mensagem) em **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. Clique em **[!UICONTROL Salvar]**.

Para atribuir isso **[!UICONTROL Perfil de produto]** para os usuários, siga as etapas abaixo:

1. Acesse o **[!DNL Admin Console]**.

1. No **[!UICONTROL Produtos]** selecione a guia **[!UICONTROL Coleta de dados do Adobe Experience Platform]** cartão.

1. Selecione a configuração anterior **[!UICONTROL Perfil de produto]**.

1. No **[!UICONTROL Usuários]** clique em **[!UICONTROL Adicionar usuário]**.

   ![](assets/push_product_6.png)

1. Digite o nome do usuário ou endereço de email e selecione o usuário. Em seguida, clique em **[!UICONTROL Salvar]**.

   >[!NOTE]
   >
   >Se o usuário não tiver sido criado anteriormente no Admin Console, consulte [Adicionar documentação de usuários](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)

### Configurar seu aplicativo {#configure-app}

A configuração técnica envolve uma estreita colaboração entre o desenvolvedor do aplicativo e o administrador comercial. Antes de começar a enviar notificações por push com [!DNL Journey Optimizer], é necessário definir as configurações em [!DNL Adobe Experience Platform Data Collection] e integrar seu aplicativo móvel com os SDKs do Adobe Experience Platform Mobile.

Siga as etapas de implementação detalhadas nos links abaixo:

* Para **Apple iOS**: Saiba como registrar seu aplicativo com APNs em [Documentação do Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}
* Para **Google Android**: Saiba como configurar um aplicativo cliente Firebase Cloud Messaging no Android em [Documentação do Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}

### Integrar seu aplicativo móvel ao SDK do Adobe Experience Platform {#integrate-mobile-app}

O Adobe Experience Platform Mobile SDK fornece APIs de integração do lado do cliente para dispositivos móveis por meio de SDKs compatíveis com Android e iOS. Seguir [Documentação do SDK do Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/overview){target="_blank"} para obter a configuração com os SDKs do Adobe Experience Platform Mobile em seu aplicativo.

Ao final disso, você também deve ter criado e configurado uma propriedade móvel no [!DNL Adobe Experience Platform Data Collection]. Normalmente, você cria uma propriedade móvel para cada aplicativo móvel que deseja gerenciar. Saiba como criar e configurar uma propriedade móvel no [Documentação do SDK do Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property){target="_blank"}.


## Etapa 1: Adicionar suas credenciais de push do aplicativo na Coleta de dados do Adobe Experience Platform {#push-credentials-launch}

Após conceder as permissões de usuário corretas, agora é necessário adicionar suas credenciais de push do aplicativo móvel em [!DNL Adobe Experience Platform Data Collection].

O registro de credenciais de push do aplicativo móvel é necessário para autorizar o Adobe a enviar notificações por push em seu nome. Consulte as etapas detalhadas abaixo:

1. De [!DNL Adobe Experience Platform Data Collection], selecione o **[!UICONTROL Superfícies do aplicativo]** no painel esquerdo.

1. Clique em **[!UICONTROL Criar superfície do aplicativo]** para criar uma nova configuração.

   ![](assets/add-app-config.png)

1. Insira um **[!UICONTROL Nome]** para a configuração.

1. De **[!UICONTROL Configuração do aplicativo móvel]**, selecione o Sistema operacional:

   * **Para iOS**

      ![](assets/add-app-config-ios.png)

      1. Insira o aplicativo móvel **ID do pacote** no **[!UICONTROL ID do aplicativo (iOS Bundle ID)]** campo. A ID do pacote de aplicativos pode ser encontrada no **Geral** da meta principal em **XCode**.

      1. Ligado o **[!UICONTROL Credenciais de push]** para adicionar suas credenciais.

      1. Arraste e solte seu arquivo .p8 Chave de autenticação de notificação por push do Apple. Essa chave pode ser adquirida do **Certificados**, **Identificadores** e **Perfis** página.

      1. Forneça a **Key ID**. Esta é uma string de 10 caracteres atribuída durante a criação da chave de autenticação p8. Pode ser encontrado em **Teclas** em **Certificados**, **Identificadores** e **Perfis** página.

      1. Forneça a **ID do grupo**. Este é um valor de string que pode ser encontrado na guia Membership .
   * **Para Android**

      ![](assets/add-app-config-android.png)

      1. Forneça a **[!UICONTROL ID do aplicativo (nome do pacote Android)]**: geralmente, o nome do pacote é a id do aplicativo em seu `build.gradle` arquivo.

      1. Ligado o **[!UICONTROL Credenciais de push]** para adicionar suas credenciais.

      1. Arraste e solte as credenciais de push do FCM. Para obter mais detalhes sobre como obter as credenciais de push, consulte [Documentação do Google](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.



1. Clique em **[!UICONTROL Salvar]** para criar a configuração do seu aplicativo.

<!--
## Step 2: Set up a mobile property in Adobe Experience Platform Launch {#launch-property}

Setting up a mobile property allows the mobile app developer or marketer to configure the mobile SDKs attributes such as Session Timeouts, the [!DNL Adobe Experience Platform] sandbox to be targeted and the **[!UICONTROL Adobe Experience Platform Datasets]** to be used for mobile SDK to send data to.

For further details and procedures on how to set up a **[!UICONTROL Platform Launch property]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).


To get the SDKs needed for push notification to work you will need the following SDK extensions, for both Android and iOS:

* **[!UICONTROL Mobile Core]** (installed automatically)
* **[!UICONTROL Profile]** (installed automatically)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optional but recommended to debug the mobile implementation.

Learn more about [!DNL Adobe Experience Platform Launch] extensions in [Adobe Experience Platform Launch documentation](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).
-->

## Etapa 2: Configurar a extensão Adobe Journey Optimizer na propriedade móvel {#configure-journey-optimizer-extension}

O **Extensão do Adobe Journey Optimizer** para SDKs do Adobe Experience Platform Mobile, o aciona notificações por push para aplicativos móveis e ajuda a coletar tokens por push do usuário e gerencia a medição de interação com os serviços da Adobe Experience Platform.

Saiba como configurar a extensão do Journey Optimizer no [Documentação do SDK do Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target="_blank"}.


<!-- 
**[!UICONTROL Edge configuration]** is used by **[!UICONTROL Edge]** extension to send custom data from mobile device to [!DNL Adobe Experience Platform]. 
To configure [!DNL Adobe Experience Platform], you must provide the **[!UICONTROL Sandbox]** name and **[!UICONTROL Event Dataset]**.

For further details and procedures on how to create **[!UICONTROL Edge configuration]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)



1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

<!--
## Step 4: Publish the Property {#publish-property}

You now need to publish the property to integrate your configuration and to use it in the mobile app. 

To publish your property, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

## Step 5: Configure the ProfileDataSource {#configure-profiledatasource}

To configure the `ProfileDataSource`, use the `ProfileDCInletURL` from [!DNL Adobe Experience Platform] setup and add the following in the mobile app:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

-->

## Etapa 3: Teste seu aplicativo móvel com um evento {#mobile-app-test}

Depois de configurar seu aplicativo móvel no Adobe Experience Platform e no [!DNL Adobe Experience Platform Data Collection], agora você pode testá-lo antes de enviar notificações por push para seus perfis. Nesse caso de uso, criamos uma jornada para direcionar nosso aplicativo móvel e definimos um evento que aciona a notificação por push.

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

Para que essa jornada funcione, é necessário criar um esquema XDM. Para obter mais informações, consulte [Documentação XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target="_blank"}.

1. No menu esquerdo, navegue até **[!UICONTROL Esquemas]**.

1. Clique em **[!UICONTROL Criar esquema]** em seguida, selecione **[!UICONTROL ExperiênciaEvento XDM]**.

   ![](assets/test_push_2.png)

1. Selecionar **[!UICONTROL Criar um novo grupo de campos]**.

1. Insira um **[!UICONTROL Nome de exibição]** e **[!UICONTROL Descrição]**. Clique em **[!UICONTROL Adicionar grupos de campos]** quando concluído. Para obter mais informações sobre como criar grupos de campos, consulte [Documentação do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR){target="_blank"}.


   ![](assets/test_push_4.png)

1. No lado esquerdo, selecione o schema . No painel direito, insira o nome do esquema e a descrição. Habilitar este esquema para **[!UICONTROL Perfil]**.

   ![](assets/test_push_4b.png)


1. No lado esquerdo, selecione o grupo de campos e clique no ícone + para criar um novo campo. No **[!UICONTROL Propriedades de grupos de campos]**, no lado direito, digite uma **[!UICONTROL Nome do campo]**, **[!UICONTROL Nome de exibição]** e selecione **[!UICONTROL String]** as **[!UICONTROL Tipo]**.

   ![](assets/test_push_5.png)

1. Verificar **[!UICONTROL Obrigatório]** e clique em **[!UICONTROL Aplicar]**.

1. Clique em **[!UICONTROL Salvar]**. Seu esquema agora é criado e pode ser usado em um evento.

Em seguida, é necessário configurar um evento .

1. No menu esquerdo da página inicial, em ADMINISTRATION (ADMINISTRAÇÃO), selecione **[!UICONTROL Configurações]**. O clique **[!UICONTROL Gerenciar]** no **[!UICONTROL Eventos]** para criar seu novo evento.

1. Clique em **[!UICONTROL Criar evento]**, o painel de configuração do evento é aberto no lado direito da tela.

   ![](assets/test_push_6.png)

1. Insira o nome do evento. Você também pode adicionar uma descrição.

1. No **[!UICONTROL Tipo de ID de evento]** , selecione **[!UICONTROL Baseado em regras]**.

1. No **[!UICONTROL Parâmetros]**, selecione o esquema criado anteriormente.

   ![](assets/test_push_7.png)

1. Na lista de campos, verifique se o campo criado no grupo de campos do schema está selecionado.

   ![](assets/test_push_7b.png)

1. Clique em **[!UICONTROL Editar]** no **[!UICONTROL Condição de ID de evento]** campo. Arraste e solte o campo adicionado anteriormente para definir a condição que será usada pelo sistema para identificar os eventos que acionam a jornada.

   ![](assets/test_push_8.png)

1. Digite a sintaxe que será necessária para acionar a notificação por push no aplicativo de teste, neste exemplo **confirmação do pedido**.

   ![](assets/test_push_9.png)

1. Selecionar **[!UICONTROL ECID]** como seu **[!UICONTROL Namespace]**.

1. Clique em **[!UICONTROL Ok]** then **[!UICONTROL Salvar]**.

Seu evento foi criado e agora pode ser usado em uma jornada.

1. No menu esquerdo, clique em **[!UICONTROL Jornada]**.

1. Clique em **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite as propriedades da jornada no painel de configuração exibido no lado direito. Saiba mais nesta [seção](../building-journeys/journey-gs.md#change-properties).

1. Comece arrastando e soltando o evento criado nas etapas anteriores do **[!UICONTROL Eventos]** lista suspensa.

   ![](assets/test_push_11.png)

1. No **[!UICONTROL Ações]** , arraste e solte uma **[!UICONTROL Empurrar]** atividade para sua jornada.

1. Configure a notificação por push. Para obter mais informações sobre como criar notificações por push, consulte esta seção [página](create-push.md).

1. Clique no botão **[!UICONTROL Teste]** alterne para começar a testar suas notificações por push e clique em **[!UICONTROL Acionar um evento]**.

   ![](assets/test_push_12.png)

1. Insira sua ECID no **[!UICONTROL Chave]** e digite **confirmação do pedido** no segundo campo.

   ![](assets/test_push_13.png)

1. Clique em **[!UICONTROL Enviar]**.

O evento será acionado e você receberá a notificação por push para o aplicativo móvel.

## Etapa 4: Criar uma superfície de canal para push{#message-preset}

Depois que seu aplicativo móvel é configurado em [!DNL Adobe Experience Platform Data Collection], é necessário criar uma superfície para enviar notificações por push do **[!DNL Journey Optimizer]**.

Saiba como criar e configurar uma superfície de canal no [esta seção](../configuration/channel-surfaces.md).

Agora você está pronto para enviar notificações por push com o Journey Optimizer.

* Saiba como criar uma mensagem de push em [esta página](create-push.md).
* Saiba como adicionar uma mensagem a uma jornada em [esta seção](../building-journeys/journeys-message.md).
