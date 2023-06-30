---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma campanha
description: Saiba como criar campanhas no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: criar, otimizador, campanha, superfície, mensagens
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 11c1945f8e7f7ca74a2c9ca33ff85fea77bcf5db
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 28%

---

# Criar uma campanha {#create-campaign}

>[!NOTE]
>
>Antes de criar uma nova campanha, verifique se você tem um canal de superfície (ou seja, predefinição de mensagem) e um segmento do Adobe Experience Platform pronto para uso. Saiba mais nestas seções:
>
>* [Criar superfícies de canal](../configuration/channel-surfaces.md)
>* [Introdução aos segmentos](../segment/about-segments.md)

Para criar uma nova campanha, acesse o **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**. Você também pode duplicar uma campanha ao vivo existente para criar uma nova. [Saiba mais](modify-stop-campaign.md#duplicate)

## Escolha o tipo de campanha e o canal {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campanha"
>abstract="**Campanhas programadas** são executadas imediatamente ou em uma data especificada e devem enviar mensagens de marketing. Campanhas **acionadas por API** são executadas usando uma chamada de API. O objetivo é enviar mensagens de marketing ou mensagens transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, abandono de carrinho etc."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoria da campanha"
>abstract="Se você estiver criando uma campanha programada, a campanha de **marketing** é selecionada automaticamente. Para campanhas acionadas por API, escolha se deseja enviar uma mensagem de **marketing** ou **transacional**, ou seja, uma mensagem enviada após uma ação executada por um indivíduo: redefinição de senha, abandono de carrinho etc."

1. No **[!UICONTROL Propriedades]** especifique como deseja executar a campanha. Há dois tipos de campanha disponíveis:

   * **[!UICONTROL Agendado]**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas são destinadas ao envio **marketing** mensagens. Eles são configurados e executados na interface do usuário do.

   * **[!UICONTROL Acionado pela API]**: execute a campanha usando uma chamada de API. As campanhas acionadas por API têm como objetivo enviar **marketing** ou **transacional** mensagens, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc. [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)

1. Se você estiver criando uma campanha programada, a campanha de **marketing** é selecionada automaticamente. Para campanhas acionadas por API, escolha se deseja enviar uma **marketing** ou **transacional** mensagem.&quot;

1. No **[!UICONTROL Ações]** escolha o canal e a superfície de canal a serem usados para enviar a mensagem.

   Uma superfície é uma configuração que foi definida por um [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   Somente as superfícies do canal compatíveis com o tipo de campanha de marketing são listadas na lista suspensa.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se estiver criando uma campanha de notificação por push, você poderá ativar a **[!UICONTROL Modo de entrega rápida]**, que é um complemento do Journey Optimizer que permite o envio muito rápido de mensagens por push em grandes volumes. [Saiba mais](../push/create-push.md#rapid-delivery)

1. Clique em **[!UICONTROL Criar]** para criar a campanha.

## Definir as propriedades da campanha {#create}

1. No **[!UICONTROL Propriedades]** especifique um nome e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. A variável **Tags** permite atribuir Tags unificadas do Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais à campanha, clique no link **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o OLA (Object Level Access Control, controle de acesso em nível de objeto)](../administration/object-based-access.md)

## Criar a mensagem e configurar o rastreamento {#content}

No **[!UICONTROL Ações]** crie a mensagem a ser enviada com a campanha.

1. Clique em **[!UICONTROL Editar conteúdo]** e, em seguida, criar e projetar o conteúdo da mensagem.

   Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Cliente potencial" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Criar emails</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Pouco frequentes" src="../assets/do-not-localize/push.jpg">
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

1. Depois que o conteúdo for definido, use o **[!UICONTROL Simular conteúdo]** botão para visualizar e testar seu conteúdo com perfis de teste. [Saiba mais](../email/preview.md).

1. Clique na seta para voltar para a tela de criação da campanha.

   ![](assets/create-campaign-design.png)

1. No **[!UICONTROL Rastreamento de ações]** especifique se deseja rastrear como seus recipients reagem ao seu delivery: é possível rastrear cliques e/ou aberturas.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report.md)

## Definir o público {#audience}

Clique em **[!UICONTROL Selecionar público]** botão para exibir a lista de segmentos do Adobe Experience Platform disponíveis. [Saiba mais sobre segmentos](../segment/about-segments.md)

>[!NOTE]
>
>Para campanhas acionadas por API, o público-alvo precisa ser definido por meio de uma chamada de API. [Saiba mais](api-triggered-campaigns.md)

No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

    >[!NOTE]
    >
    >Indivíduos pertencentes a um segmento que não tem a identidade selecionada (namespace) entre suas diferentes identidades não serão direcionados pela campanha.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Programar a campanha {#schedule}

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

Você pode definir uma frequência na qual a mensagem da campanha deve ser enviada. Para fazer isso, use o **[!UICONTROL Acionadores de ação]** opções na tela de criação da campanha para especificar se a campanha deve ser executada diariamente, semanalmente ou mensalmente.

Se não quiser executar sua campanha logo após a ativação, você poderá especificar uma data e hora em que a mensagem deverá ser enviada usando o **[!UICONTROL Início da campanha]** opção. A variável **[!UICONTROL Fim da campanha]** permite especificar quando uma campanha recorrente deve parar de ser executada.

![](assets/create-campaign-schedule.png)

Quando a campanha estiver pronta, você poderá revisá-la e publicá-la. [Saiba mais](review-activate-campaign.md)
