---
title: Pré-requisitos do canal no aplicativo
description: Saiba como configurar seu ambiente para enviar mensagens no aplicativo com o Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: no aplicativo, mensagem, configuração, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 7e850261f1a82492c5df93c4437b4e3c6859a2d7
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 6%

---

# Pré-requisitos do canal no aplicativo {#inapp-configuration}

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que as mensagens no aplicativo sejam entregues corretamente, as seguintes configurações devem ser definidas:

* No [Coleta de dados do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem um fluxo de dados definido, como na seção **[!UICONTROL Adobe Experience Platform]** serviço que você tem o Adobe Experience Platform Edge e **[!UICONTROL Adobe Journey Optimizer]** opção ativada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=pt-BR){target="_blank"}

  ![](assets/inapp_config_6.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, make sure you have the default merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  >[!NOTE]
  >
  >Ao usar um personalizado **[!UICONTROL Preferência do conjunto de dados]** política de mesclagem, adicione a variável **[!UICONTROL Jornada entrada]** conjunto de dados na política de mesclagem especificada.

  ![](assets/inapp_config_8.png)

## Pré-requisitos de configuração de canal {#channel-prerequisites}

1. Acesse o **[!UICONTROL Superfícies do aplicativo]** e clique em **[!UICONTROL Criar superfície do aplicativo]**.

1. Adicione um nome ao seu **[!UICONTROL Superfície do aplicativo]**.

   ![](assets/inapp_config_2b.png)

1. No **[!UICONTROL Apple iOS]** , configure seu aplicativo para dispositivos móveis para o Apple iOS.

+++ Saiba mais

   1. Digite seu **[!UICONTROL ID do pacote do iOS]**. Consulte [Documentação do Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obter mais informações sobre **ID do pacote**.

   1. (opcional) Escolha a opção **[!UICONTROL Sandbox]** de onde deseja enviar notificações por push. Observe que a escolha de uma sandbox específica requer as permissões de acesso necessárias.

      Para obter mais informações sobre gerenciamento de sandbox, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Ativar o **[!UICONTROL Push credentials]** opção para arrastar e soltar seu arquivo de chave de autenticação .p8, se necessário.

      Você também pode ativar a variável **[!UICONTROL Insira manualmente as credenciais de push]** opção para copiar e colar a chave de autenticação APNs diretamente.

   1. Insira seu **[!UICONTROL ID da chave]** e **[!UICONTROL ID da equipe]**.

      ![](assets/inapp_config_2.png)

+++

1. No **[!UICONTROL Android]** , configure seu aplicativo móvel para Android.

+++ Saiba mais

   1. Digite seu **[!UICONTROL Nome do pacote Android]**. Consulte [Documentação do Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obter mais informações sobre **Nome do pacote**.

   1. (opcional) Escolha a opção **[!UICONTROL Sandbox]** de onde deseja enviar notificações por push. Observe que a escolha de uma sandbox específica requer as permissões de acesso necessárias.

      Para obter mais informações sobre gerenciamento de sandbox, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Ativar o **[!UICONTROL Push credentials]** opção para arrastar e soltar seu arquivo de chave privada .json, se necessário.

      Você também pode ativar a variável **[!UICONTROL Insira manualmente as credenciais de push]** opção para copiar e colar a chave privada do FCM diretamente.

      ![](assets/inapp_config_7.png)

1. Clique em **[!UICONTROL Salvar]** quando terminar a configuração do seu **[!UICONTROL Superfície do aplicativo]**.

   ![](assets/inapp_config_3.png)

   Seu **[!UICONTROL Superfície do aplicativo]** agora estarão disponíveis ao criar uma nova campanha com uma mensagem no aplicativo. [Saiba mais](create-in-app.md)

1. Depois de criar sua superfície de aplicativo, agora é necessário criar uma propriedade móvel.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para o procedimento detalhado.

   ![](assets/inapp_config_4.png)

1. No menu Extensões da propriedade recém-criada, instale as seguintes extensões:

   * Rede de borda Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimento
   * Identidade
   * Núcleo móvel
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) para o procedimento detalhado.

   ![](assets/inapp_config_5.png)

O canal no aplicativo agora está configurado. Você pode começar a enviar mensagens no aplicativo para seus usuários.

## Pré-requisitos do experimento de conteúdo {#experiment-prerequisites}

Para habilitar experimentos de conteúdo para o canal no aplicativo, verifique se [conjunto de dados](../data/get-started-datasets.md) usado na implementação no aplicativo [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios de experimento, se você adicionar um conjunto de dados que não esteja presente no seu fluxo de dados da Web, os dados da Web não serão exibidos nos relatórios de experimento de conteúdo.

Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo no [nesta seção](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo [!DNL Journey Optimizer] sistema de relatórios e não afeta a coleta ou a assimilação de dados.

Se você estiver **não** usando as seguintes opções [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), adicione os seguintes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, e `Web Details`. Estas são necessárias para a [!DNL Journey Optimizer] relatórios de experimento de conteúdo à medida que eles rastream em quais experimentos e tratamentos cada perfil está participando.

>[!NOTE]
>
>A adição desses grupos de campos não afeta a coleta de dados normal. É aditivo apenas para as páginas em que um experimento está sendo executado, deixando todos os outros rastreamentos intactos.

## Vídeos tutoriais{#video}

* O vídeo abaixo mostra como atribuir a variável **Gerenciar configuração do aplicativo** permissão para acessar o menu Superfícies do aplicativo.

  +++Ver vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++

**Tópicos relacionados:**

* [Criação de uma mensagem no aplicativo](create-in-app.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)

