---
title: Pré-requisitos e configuração do canal no aplicativo
description: Saiba como configurar seu ambiente para enviar mensagens no aplicativo com o Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: no aplicativo, mensagem, configuração, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 9%

---

# Pré-requisitos e configuração {#inapp-configuration}

## Etapas de configuração {#inapp-steps}

Para enviar mensagens no aplicativo em suas jornadas e campanhas com o [!DNL Journey Optimizer], você precisa seguir as etapas de configuração a seguir.

1. Certifique-se de ter as permissões corretas nas campanhas do Journey Optimizer antes de iniciar, mesmo que planeje usar nas jornadas apenas mensagens no aplicativo. As permissões de campanha ainda são necessárias. [Saiba mais](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
Uma permissão específica deve ser concedida para acessar o menu **Superfícies do Aplicativo** na Coleção de Dados da Adobe Experience Platform. Saiba mais em [este vídeo](#video).
1. Habilite o Adobe Journey Optimizer na sequência de dados da Coleção de dados da Adobe Experience Platform e verifique sua política de mesclagem padrão no Adobe Experience Platform, conforme detalhado nos [Pré-requisitos de entrega](#delivery-prerequisites) abaixo.
1. Crie e configure uma superfície de aplicativo na Coleção de dados da Adobe Experience Platform, conforme detalhado em [esta seção](#channel-prerequisites).
1. Se você estiver usando experimentos de conteúdo, siga os requisitos listados em [esta seção](#experiment-prerequisite).

Depois de concluída, você pode criar, configurar e enviar sua primeira mensagem no aplicativo. Saiba como fazer isso [nesta seção](create-in-app.md).

## Pré-requisitos de entrega {#delivery-prerequisites}

Para que as mensagens no aplicativo sejam entregues corretamente, as seguintes configurações devem ser definidas:

* Na [Coleção de Dados da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}, verifique se você tem uma sequência de dados definida, como no serviço **[!UICONTROL Adobe Experience Platform]**, se você tem a opção Adobe Experience Platform Edge e **[!UICONTROL Adobe Journey Optimizer]** habilitada.

  Isso garante que os eventos de entrada do Journey Optimizer sejam manipulados corretamente pelo Adobe Experience Platform Edge. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* Em [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}, verifique se você tem a política de mesclagem padrão com a opção **[!UICONTROL Política de mesclagem Ative-On-Edge]** habilitada. Para fazer isso, selecione uma política no menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Mesclar Políticas]**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Essa política de mesclagem é usada por [!DNL Journey Optimizer] canais de entrada para ativar e publicar corretamente campanhas de entrada na borda. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}

  >[!NOTE]
  >
  >Ao usar uma política de mesclagem personalizada de **[!UICONTROL preferência de conjunto de dados]**, adicione o conjunto de dados de **[!UICONTROL Entrada de Jornada]** dentro da política de mesclagem especificada.

  ![](assets/inapp_config_8.png)

* Para solucionar problemas de entrega de experiências móveis do Journey Optimizer, você pode usar a exibição **Edge Delivery** no **Adobe Experience Platform Assurance**. Este plug-in permite que você inspecione chamadas de solicitação em detalhes, verifique se as chamadas de borda esperadas ocorrem conforme previsto e examine dados de perfil, incluindo mapas de identidade, associações de segmento e configurações de consentimento. Além disso, você pode revisar as atividades para as quais a solicitação se qualificou e identificar aquelas que não foram qualificadas.

  O uso do plug-in **Edge Delivery** ajuda a obter os insights necessários para entender e solucionar problemas de implementações de entrada de maneira eficaz.

  [Saiba mais sobre a exibição do Edge Delivery](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery)

## Pré-requisitos de configuração de canal {#channel-prerequisites}

1. Acesse o menu **[!UICONTROL Superfícies do aplicativo]** e clique em **[!UICONTROL Criar superfície do aplicativo]**.

1. Adicione um nome à sua **[!UICONTROL superfície do aplicativo]**.

   ![](assets/inapp_config_2b.png)

1. No menu suspenso **[!UICONTROL Apple iOS]**, configure seu aplicativo para dispositivos móveis para Apple iOS.

+++ Saiba mais

   1. Digite sua **[!UICONTROL ID do Pacote do iOS]**. Consulte a [documentação do Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obter mais informações sobre a **ID do Pacote**.

   1. (opcional) Escolha a **[!UICONTROL Sandbox]** de onde deseja enviar notificações por push. Observe que a escolha de uma sandbox específica requer as permissões de acesso necessárias.

      Para obter mais informações sobre gerenciamento de sandbox, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite a opção **[!UICONTROL Push credentials]** para arrastar e soltar seu arquivo de chave de autenticação .p8, se necessário.

      Você também pode habilitar a opção **[!UICONTROL Inserir credenciais de push manualmente]** para copiar e colar a chave de autenticação APNs diretamente.

   1. Insira sua **[!UICONTROL ID de Chave]** e a **[!UICONTROL ID de Equipe]**.

      ![](assets/inapp_config_2.png)

+++

1. No menu suspenso **[!UICONTROL Android]**, configure seu aplicativo móvel para Android.

+++ Saiba mais

   1. Digite o **[!UICONTROL nome do pacote do Android]**. Consulte a [documentação do Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obter mais informações sobre **Nome do pacote**.

   1. (opcional) Escolha a **[!UICONTROL Sandbox]** de onde deseja enviar notificações por push. Observe que a escolha de uma sandbox específica requer as permissões de acesso necessárias.

      Para obter mais informações sobre gerenciamento de sandbox, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite a opção **[!UICONTROL Push credentials]** para arrastar e soltar seu arquivo de chave privada .json, se necessário.

      Você também pode habilitar a opção **[!UICONTROL Inserir credenciais de push manualmente]** para copiar e colar a chave privada do FCM diretamente.

      ![](assets/inapp_config_7.png)

1. Clique em **[!UICONTROL Salvar]** quando terminar a configuração da sua **[!UICONTROL superfície de aplicativo]**.

   ![](assets/inapp_config_3.png)

   Sua **[!UICONTROL superfície de aplicativo]** agora estará disponível ao criar uma nova campanha com uma mensagem no aplicativo. [Saiba mais](create-in-app.md)

1. Depois de criar sua superfície de aplicativo, agora é necessário criar uma propriedade móvel.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para obter o procedimento detalhado.

   ![](assets/inapp_config_4.png)

1. No menu Extensões da propriedade recém-criada, instale as seguintes extensões:

   * Edge Network Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimento
   * Identidade
   * Núcleo móvel
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) para obter o procedimento detalhado.

   ![](assets/inapp_config_5.png)

O canal no aplicativo agora está configurado. Você pode começar a enviar mensagens no aplicativo para seus usuários.

## Pré-requisitos do experimento de conteúdo {#experiment-prerequisites}

Para habilitar experimentos de conteúdo para o canal no aplicativo, você precisa verificar se o [conjunto de dados](../data/get-started-datasets.md) usado na sua implementação no aplicativo [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios de experimento, se você adicionar um conjunto de dados que não esteja presente no seu fluxo de dados da Web, os dados da Web não serão exibidos nos relatórios de experimento de conteúdo.

Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo [esta seção](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo sistema de relatórios [!DNL Journey Optimizer] e não afeta a coleta ou a assimilação de dados.

Se você estiver **não** usando os [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} predefinidos a seguir para o esquema do conjunto de dados: `AEP Web SDK ExperienceEvent` e `Consumer Experience Event` (conforme definido em [esta página](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), adicione os seguintes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` e `Web Details`. Eles são necessários para os relatórios de experimento de conteúdo [!DNL Journey Optimizer], pois estão rastreando em quais experimentos e tratamentos cada perfil está participando.

>[!NOTE]
>
>A adição desses grupos de campos não afeta a coleta de dados normal. É aditivo apenas para as páginas em que um experimento está sendo executado, deixando todos os outros rastreamentos intactos.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como atribuir a permissão **Gerenciar configuração de aplicativo** para acessar o menu de superfícies do aplicativo.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**Tópicos relacionados:**

* [Criação de uma mensagem no aplicativo](create-in-app.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)

