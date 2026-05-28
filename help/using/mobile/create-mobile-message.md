---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma mensagem para dispositivo móvel
description: Saiba como criar uma mensagem móvel no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
TQID: https://experienceleague.adobe.com/xgPlWorA3lsIF8ZBPHdg2UAK8cLKUsJO-2ONc7ZG8AU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 748
ht-degree: 2%

---

# Criar uma mensagem para dispositivo móvel {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Criar uma mensagem para dispositivo móvel"
>abstract="Para criar uma mensagem móvel, adicione uma ação SMS em uma jornada ou campanha e comece a personalizá-la com o editor de personalização."

>[!AVAILABILITY]
>
>O RCS não é um serviço pronto para HIPAA e não deve ser usado para coletar, armazenar ou processar dados pessoais confidenciais, incluindo dados de saúde permitidos, por exemplo, informações pessoais de saúde, que sua organização pode ter permissão para processar no Journey Optimizer.

Você pode criar e enviar mensagens de texto (SMS), comunicação avançada (RCS) e multimídia (MMS) com o Adobe Journey Optimizer. Primeiro, é necessário adicionar uma ação de Mensagem móvel em uma jornada ou campanha e, em seguida, definir o conteúdo da Mensagem móvel, conforme detalhado abaixo. O Adobe Journey Optimizer também oferece recursos para testar suas mensagens móveis antes do envio, para que você possa verificar a renderização, os atributos de personalização e todas as outras configurações.

De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing SMS/RCS/MMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. Para fazer isso, os destinatários de SMS podem responder com palavras-chave de aceitação e recusa. [Saiba como gerenciar a opção de não participação](../privacy/opt-out.md#opt-out-decision-management)

## Adicionar uma mensagem móvel {#create-sms-journey-campaign}

Navegue pelas guias abaixo para saber como adicionar uma mensagem móvel em uma campanha ou jornada.

>[!BEGINTABS]

>[!TAB Adicionar uma mensagem móvel a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade **[!UICONTROL Ação]** da seção **[!UICONTROL Ações]** da paleta. Saiba mais sobre a [Atividade de ação](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >As atividades de canal nativas herdadas (Email, Push, SMS, No aplicativo, Web, Experiência baseada em código e Cartão de conteúdo) serão descontinuadas a partir da versão de março de 2026. As jornadas existentes que usam essas atividades continuam a funcionar sem alterações — nenhuma migração é necessária.

1. Selecione **[!UICONTROL Mensagem móvel]** como o tipo de ação e clique em **[!UICONTROL Adicionar]**.

   ![](assets/sms_create_1.png)

1. Insira um **[!UICONTROL Rótulo]** para identificar sua ação na tela de jornada.

1. Clique no botão **[!UICONTROL Configurar ação]**.

1. Você é direcionado para a guia **[!UICONTROL Ações]**. Nesse local, selecione ou crie a configuração de mensagem móvel que será usada. [Saiba mais](mobile-configuration.md)

   ![](assets/sms_create_2.png)

1. Além disso, você pode aplicar regras de limitação à sua ação de mensagem móvel selecionando um conjunto de regras na lista suspensa **[!UICONTROL Regras de negócio]**. [Saiba mais](../conflict-prioritization/channel-capping.md)

1. Selecione o botão **[!UICONTROL Editar conteúdo]** e crie o conteúdo conforme desejado. [Saiba mais](design-mobile.md)

1. Volte para a tela de jornada. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

Para obter mais informações sobre como criar, configurar e publicar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Adicionar uma mensagem móvel a uma campanha]

1. Acesse o menu **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**.

1. Selecione o tipo de campanha que deseja executar

   * **Agendado - Marketing**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas são destinadas ao envio de mensagens de marketing. Eles são configurados e executados na interface do usuário do.

   * **Acionado por API - Marketing/Transacional**: execute a campanha usando uma chamada de API. As campanhas acionadas por API destinam-se ao envio de mensagens de marketing ou transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc.

1. Na seção **[!UICONTROL Propriedades]**, edite o **[!UICONTROL Título]** e a **[!UICONTROL Descrição]** da sua campanha.

1. Na guia **[!UICONTROL Ação]**, clique em **[!UICONTROL Adicionar ação]** e escolha **[!UICONTROL Mensagem móvel]**. Em seguida, selecione ou crie uma nova configuração.

   Saiba mais sobre a configuração de mensagem móvel em [esta página](mobile-configuration.md).

   ![](assets/sms_create_3.png)

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../content-management/content-experiment.md)

1. Na seção **[!UICONTROL Rastreamento de ações]**, especifique se deseja rastrear cliques nos links da mensagem móvel.

1. Na guia **[!UICONTROL Público-alvo]**, clique no botão **[!UICONTROL Selecionar público-alvo]** para definir o público-alvo a ser direcionado na lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais](../audience/about-audiences.md).

1. No campo **[!UICONTROL Namespace de identidade]**, escolha o namespace a ser usado para identificar os indivíduos do público selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

1. Na guia **[!UICONTROL Agendar]**, você pode projetar suas Campanhas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Cronograma]** da sua campanha no [nesta seção](../campaigns/campaign-schedule.md#action-campaign-schedule).

1. No menu **[!UICONTROL Acionadores de ação]**, escolha a **[!UICONTROL Frequência]** da mensagem móvel:

   * Uma vez
   * Diariamente
   * Semanal
   * Month

Agora você pode começar a projetar o conteúdo da sua Mensagem móvel a partir do botão **[!UICONTROL Editar conteúdo]**, conforme detalhado abaixo. [Saiba mais](design-mobile.md)

Para obter mais informações sobre como criar, configurar e ativar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

**Tópicos relacionados**

* [Criar uma mensagem para dispositivo móvel](design-mobile.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)
* [Pré-visualizar, testar e enviar a mensagem móvel](send-mobile-message.md)
* [Configurar canal de mensagem móvel](mobile-configuration.md)
* [Relatórios de mensagem móvel](../reports/journey-global-report-cja-sms.md)

