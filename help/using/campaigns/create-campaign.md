---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma campanha
description: Saiba como criar campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: criar, otimizador, campanha, superfície, mensagens
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 72bda999c9e866398375422d8419516e5fea97b5
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 27%

---

# Criar uma campanha {#create-campaign}

>[!NOTE]
>
>Antes de criar uma nova campanha, verifique se você tem uma configuração de canal (ou seja, uma superfície de mensagem) e um público-alvo da Adobe Experience Platform pronto para uso. Saiba mais nestas seções:
>
>* [Criar configurações de canal](../configuration/channel-surfaces.md)
>* [Introdução aos públicos-alvo](../audience/about-audiences.md)

Para criar uma nova campanha, acesse o menu **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**. Você também pode duplicar uma campanha ao vivo existente para criar uma nova. [Saiba mais](modify-stop-campaign.md#duplicate)

## Escolha o tipo de campanha {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campanha"
>abstract="**Campanhas programadas** são executadas imediatamente ou em uma data especificada e devem enviar mensagens de marketing. Campanhas **acionadas por API** são executadas usando uma chamada de API. O objetivo é enviar mensagens de marketing (mensagens promocionais que exigem o consentimento da pessoa) ou mensagens transacionais (mensagens não comerciais, que também podem ser enviadas a perfis não assinantes em contextos específicos)."

1. Selecione o tipo de campanha que deseja executar

   * **[!UICONTROL Agendado - Marketing]**: execute a campanha imediatamente ou em uma data especificada. As campanhas agendadas têm como objetivo enviar mensagens de **marketing**. Eles são configurados e executados na interface do usuário do.

   * **[!UICONTROL Acionado por API - Marketing/Transacional]**: execute a campanha usando uma chamada de API. As campanhas acionadas por API têm como objetivo enviar **mensagens de marketing** ou **mensagens transacionais**, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc. [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. Clique em **[!UICONTROL Criar]** para criar a campanha.

## Definir as propriedades da campanha {#create}

1. Na seção **[!UICONTROL Properties]**, especifique um nome e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. O campo **Tags** permite atribuir Tags unificadas do Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais à campanha, clique no botão **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLA (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md)

## Definir o público da campanha {#audience}

Para definir a população direcionada pela campanha, siga estas etapas:

>[!IMPORTANT]
>
>O uso de públicos-alvo e atributos da [composição de público-alvo](../audience/get-started-audience-orchestration.md) não está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.
>
>Para campanhas acionadas por API, o público-alvo precisa ser definido por meio de uma chamada de API.

1. Na seção **Público-alvo**, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo do Adobe Experience Platform disponíveis. [Saiba mais sobre públicos-alvo](../audience/about-audiences.md)

1. No campo **[!UICONTROL Namespace de identidade]**, escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

   Os indivíduos pertencentes a um segmento que não tem a identidade selecionada (namespace) entre suas diferentes identidades não serão direcionados pela campanha. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Criar a mensagem e configurar o rastreamento {#content}

1. Na seção **[!UICONTROL Actions]**, selecione ou crie uma nova configuração.

   Uma configuração foi definida por um [Administrador do Sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   Somente as configurações de canal compatíveis com o tipo de campanha de marketing são listadas na lista suspensa.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se estiver criando uma campanha de notificação por push, você poderá habilitar o **[!UICONTROL Modo de entrega rápida]**, que é um complemento do Journey Optimizer que permite o envio muito rápido de mensagens por push em grandes volumes. [Saiba mais](../push/create-push.md#rapid-delivery)

1. Clique no botão **[!UICONTROL Editar conteúdo]** para criar e criar sua mensagem. Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lead" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Criar emails</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Pouco frequente" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Criar notificações por push</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validação" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>Criar mensagens SMS</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Depois que o conteúdo for definido, use o botão **[!UICONTROL Simular conteúdo]** para visualizar e testar o conteúdo com perfis de teste. [Saiba mais](../content-management/preview-test.md).

1. Clique na seta para voltar para a tela de criação da campanha.

   ![](assets/create-campaign-design.png)

1. Na seção **[!UICONTROL Rastreamento de ações]**, especifique se deseja acompanhar como seus destinatários reagem à sua entrega: é possível rastrear cliques e/ou aberturas.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report.md)

## Programar a campanha {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programação de campanha"
>abstract="Por padrão, as campanhas começam com uma ativação manual e terminam imediatamente após a mensagem ser enviada uma vez. No entanto, você tem a flexibilidade de definir a data e hora específicas para o envio da mensagem. Além disso, é possível especificar uma data de término para campanhas recorrentes ou acionadas por API. Nos acionadores de ação, você também pode configurar a frequência de envio de mensagens de acordo com suas preferências."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Início da campanha"
>abstract="Especifique a data e a hora em que a mensagem deve ser enviada."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fim da campanha"
>abstract="Especifique quando uma campanha recorrente deve parar de ser executada."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Acionadores de ação da campanha"
>abstract="Defina uma frequência na qual a mensagem da campanha deve ser enviada."

Por padrão, as campanhas começam depois de serem ativadas manualmente e terminam assim que a mensagem é enviada uma vez.

Você pode definir uma frequência na qual a mensagem da campanha deve ser enviada. Para fazer isso, use as opções **[!UICONTROL Action triggers]** na tela de criação da campanha para especificar se a campanha deve ser executada diariamente, semanalmente ou mensalmente.

Se você não quiser executar sua campanha logo após a ativação, poderá especificar uma data e hora em que a mensagem deverá ser enviada usando a opção **[!UICONTROL Início da campanha]**. A opção **[!UICONTROL Campaign end]** permite especificar quando uma campanha recorrente deve parar de ser executada.

![](assets/create-campaign-schedule.png)

Quando a campanha estiver pronta, você poderá revisá-la e publicá-la. [Saiba mais](review-activate-campaign.md)
