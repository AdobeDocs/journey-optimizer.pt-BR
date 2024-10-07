---
title: Pré-requisitos e configuração do canal no aplicativo
description: Saiba como configurar seu ambiente para enviar mensagens no aplicativo com o Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: no aplicativo, mensagem, configuração, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 9%

---

# Pré-requisitos e configuração {#inapp-configuration}

## Etapas de configuração {#inapp-steps}

Para enviar mensagens no aplicativo em suas jornadas e campanhas com o [!DNL Journey Optimizer], você precisa seguir as etapas de configuração a seguir.

1. Certifique-se de ter as permissões corretas nas campanhas do Journey Optimizer antes de iniciar, mesmo que planeje usar nas jornadas apenas mensagens no aplicativo. As permissões de campanha ainda são necessárias. [Saiba mais](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
1. Habilite o Adobe Journey Optimizer na sequência de dados da Coleção de dados da Adobe Experience Platform e verifique sua política de mesclagem padrão no Adobe Experience Platform, conforme detalhado nos [Pré-requisitos de entrega](#delivery-prerequisites) abaixo.
1. Crie uma configuração de canal de mensagens no aplicativo em Administration > Channels > Channel configurations, conforme detalhado em [esta seção](#channel-prerequisites).
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

## Criar uma configuração no aplicativo {#channel-prerequisites}

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/inapp_config_1.png)

1. Insira um nome e uma descrição (opcional) para a configuração e selecione o canal a ser configurado.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Selecione o canal **Mensagens no aplicativo**.

   ![](assets/inapp_config_9.png)

1. Selecione a plataforma à qual a mensagem no aplicativo será aplicada.

   ![](assets/inapp_config_10.png)

1. Para a Web:

   * Você pode inserir uma **[!UICONTROL URL da página]** para aplicar alterações a uma página específica.

   * É possível criar uma regra para direcionar vários URLs que seguem o mesmo padrão.

+++ Como criar uma regra de correspondência de Páginas.

      1. Selecione **[!UICONTROL Regra de correspondência de páginas]** como configuração de aplicativo e insira sua **[!UICONTROL URL da página]**.

      1. Na janela **[!UICONTROL Editar regra de configuração]**, defina seus critérios para os campos **[!UICONTROL Domínio]** e **[!UICONTROL Página]**.
      1. Nos menus suspensos de condição, personalize ainda mais seus critérios.

         Aqui, por exemplo, para editar elementos exibidos em todas as páginas de produtos de vendas do site Luma, selecione Domínio > Começa com > Luma e Página > Contém > vendas.

         ![](assets/in_app_web_surface_4.png)

      1. Clique em **[!UICONTROL Adicionar outra regra de página]** para criar outra regra, se necessário.

      1. Selecione a **[!UICONTROL URL padrão de criação e visualização]**.

      1. Salve as alterações. A regra é exibida na tela **[!UICONTROL Criar campanha]**.

+++

1. Para iOS e Android:

   * Insira sua **[!UICONTROL ID do aplicativo]**.

1. Envie suas alterações.

Agora é possível selecionar sua configuração ao criar a mensagem no aplicativo.

## Pré-requisitos de relatórios {#experiment-prerequisites}

>[!NOTE]
>
>O conjunto de dados é usado como somente leitura pelo sistema de relatórios [!DNL Journey Optimizer] e não afeta a coleta ou a assimilação de dados.

Para habilitar relatórios para o canal no aplicativo, você precisa verificar se o [conjunto de dados](../data/get-started-datasets.md) usado na sua implementação no aplicativo [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} também está incluído na sua configuração de relatórios.

Em outras palavras, ao configurar os relatórios, se você adicionar um conjunto de dados que não esteja presente no fluxo de dados do aplicativo, os dados do aplicativo não serão exibidos nos relatórios.

Saiba como adicionar conjuntos de dados para relatórios em [esta seção](../reports/reporting-configuration.md#add-datasets).

Se você estiver **não** usando os [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} predefinidos a seguir para o esquema do conjunto de dados: `AEP Web SDK ExperienceEvent` e `Consumer Experience Event` (conforme definido em [esta página](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), adicione os seguintes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` e `Web Details`. Eles são necessários para os relatórios de experimento de conteúdo [!DNL Journey Optimizer], pois estão rastreando em quais experimentos e tratamentos cada perfil está participando.

[Saiba mais sobre a configuração de relatórios](../reports/reporting-configuration.md)

>[!NOTE]
>
>A adição desses grupos de campos não afeta a coleta de dados normal. É aditivo apenas para as páginas em que um experimento está sendo executado, deixando todos os outros rastreamentos intactos.

**Tópicos relacionados:**

* [Criação de uma mensagem no aplicativo](create-in-app.md)
* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)

