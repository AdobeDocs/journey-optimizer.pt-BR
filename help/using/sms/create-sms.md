---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma mensagem de SMS.
description: Saiba como criar uma mensagem SMS no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 17%

---

# Criar uma mensagem de SMS. {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Criar uma mensagem de SMS."
>abstract="Adicione sua mensagem SMS e comece a personalizá-la com o editor de expressão."

## Adicionar uma mensagem SMS {#create-sms-journey-campaign}

Navegue pelas guias abaixo para saber como adicionar uma mensagem SMS em uma campanha ou jornada.

>[!BEGINTABS]

>[!TAB Adicionar uma mensagem SMS a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de SMS da **Ações** seção da paleta.

   ![](assets/sms_create_1.png)

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície de mensagem a ser usada.

   ![](assets/sms_create_2.png)

   Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md)

   A variável **[!UICONTROL Superficial]** é pré-preenchido, por padrão, com a última superfície usada para esse canal pelo usuário.

Agora é possível começar a projetar o conteúdo da sua mensagem SMS usando o **[!UICONTROL Editar conteúdo]** botão. [Definir o conteúdo do SMS](#sms-content)

>[!TAB Adicionar uma mensagem SMS a uma campanha]

1. Crie uma nova campanha programada ou acionada por API, selecione **[!UICONTROL SMS]** como sua ação e escolha a opção **[!UICONTROL Superfície do aplicativo]** para usar. [Saiba mais sobre a configuração de SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o da sua campanha **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

   ![](assets/sms_create_4.png)

1. Clique em **[!UICONTROL Selecionar público]** botão para definir o público-alvo a ser direcionado na lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais](../audience/about-audiences.md).

1. No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do público-alvo selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../campaigns/content-experiment.md)

1. No **[!UICONTROL Rastreamento de ações]** especifique se deseja rastrear cliques nos links da mensagem SMS.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

1. No **[!UICONTROL Acionadores de ação]** selecione o **[!UICONTROL Frequência]** de sua mensagem SMS:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mês

Agora é possível começar a projetar o conteúdo da sua mensagem SMS usando o **[!UICONTROL Editar conteúdo]** botão. [Projetar o conteúdo de SMS](#sms-content)

>[!ENDTABS]

## Definir o conteúdo do SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definir o conteúdo do SMS"
>abstract="Personalize as mensagens SMS usando o editor de expressão para definir o conteúdo e incorporar elementos dinâmicos."

1. Na tela de configuração do jornada ou da campanha, clique no link **[!UICONTROL Editar conteúdo]** botão para configurar o conteúdo do SMS.

1. Clique em **[!UICONTROL Mensagem]** para abrir o editor de expressão.

   ![](assets/sms-content.png)

1. Use o editor de expressão para definir o conteúdo e adicionar conteúdo dinâmico. Você pode usar qualquer atributo, como o nome do perfil ou a cidade. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no Editor de expressão.

1. Depois de definir o conteúdo, você pode adicionar os URLs de rastreamento à mensagem. Para fazer isso, acesse o **[!UICONTROL Funções auxiliares]** e selecione **[!UICONTROL Auxiliares]**.

   Observe que para usar a função de redução de URL, primeiro você deve configurar um subdomínio que será vinculado à sua superfície. [Saiba mais](sms-subdomains.md)

   >[!CAUTION]
   >
   > Para acessar e editar subdomínios SMS, você deve ter a **[!UICONTROL Gerenciar subdomínios de SMS]** permissão na sandbox de produção.

   ![](assets/sms_tracking_1.png)

1. No prazo de **[!UICONTROL Funções auxiliares]** clique em **[!UICONTROL Função de URL]** e selecione **[!UICONTROL Adicionar URL]**.

   ![](assets/sms_tracking_2.png)

1. No `originalUrl` cole o URL que deseja encurtar e clique em **[!UICONTROL Salvar]**.

1. Ative a opção MMS para adicionar mídia ao conteúdo de SMS.

   O MMS vem com algumas limitações listadas na [esta página](../start/guardrails.md#sms-guardrails).

   >[!NOTE]
   >
   > A opção MMS só está disponível com Sinch. É necessário criar uma credencial de API específica para criar o MMS. [Saiba mais](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. Adicionar um **[!UICONTROL Título]** à sua mídia.

1. Insira o URL da mídia na caixa **[!UICONTROL Mídia]** campo.

   ![](assets/sms_create_7.png)

1. Clique em **[!UICONTROL Salvar]** e verifique sua mensagem na visualização. Você pode usar **[!UICONTROL Simular conteúdo]** para visualizar seus URLs encurtados ou conteúdo personalizado.

   ![](assets/sms-content-preview.png)

Agora você pode testar e enviar sua mensagem SMS para o público-alvo. [Saiba mais](send-sms.md)
Depois de enviado, você pode medir o impacto do SMS nos relatórios do Campaign ou do Jornada. Para obter mais informações sobre relatórios, consulte [esta seção](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. Para fazer isso, os destinatários de SMS podem responder com palavras-chave de aceitação e recusa. [Saiba como gerenciar a recusa](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Tópicos relacionados**

* [Pré-visualizar, testar e enviar sua mensagem SMS](send-sms.md)
* [Configurar canal de SMS](sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)
