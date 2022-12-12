---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma campanha
description: Saiba como criar campanhas no [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 10%

---

# Criar uma campanha {#create-campaign}

>[!NOTE]
>
>Antes de criar uma nova campanha, verifique se você tem um canal de superfície (ou seja, uma predefinição de mensagem) e um segmento do Adobe Experience Platform pronto para uso. Saiba mais nestas seções:
>
>* [Criar superfícies de canal](../configuration/channel-surfaces.md)
>* [Introdução aos segmentos](../segment/about-segments.md)


## Criar sua primeira campanha {#create}

1. Acesse o **[!UICONTROL Campanhas]** , em seguida, clique em **[!UICONTROL Criar campanha]**.

   >[!NOTE]
   >
   >Você também pode duplicar uma campanha ao vivo existente para criar uma nova. [Saiba mais](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. No **[!UICONTROL Propriedades]** especifique como deseja executar a campanha:

   * **[!UICONTROL Programado]**
   * **[!UICONTROL Acionado por API]**

   Para obter mais informações sobre o tipo de campanha e os envolvimentos associados, consulte esta seção [seção](#campaigntype).

1. No **[!UICONTROL Ações]** escolha o canal e a superfície do canal a serem usados para enviar a mensagem e clique em **[!UICONTROL Criar]**.

   Uma superfície é uma configuração que foi definida por um [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Somente superfícies de canal compatíveis com o tipo de campanha de marketing são listadas na lista suspensa.

1. Especifique um título e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Para atribuir rótulos de uso de dados personalizados ou principais à campanha, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o Controle de acesso no nível do objeto (OLA)](../administration/object-based-access.md)

## Criar a mensagem {#content}

No **[!UICONTROL Ações]** , crie a mensagem a ser enviada com a campanha.

1. Clique no botão **[!UICONTROL Editar conteúdo]** , em seguida, crie e crie o conteúdo da mensagem.

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

1. Depois que o conteúdo for definido, use a variável **[!UICONTROL Simular conteúdo]** para visualizar e testar seu conteúdo com perfis de teste. [Saiba mais](../email/preview.md).

1. Clique na seta para voltar à tela de criação da campanha.

   ![](assets/create-campaign-design.png)

1. No **[!UICONTROL Rastreamento de ações]** , especifique se deseja rastrear como os recipients reagem ao seu delivery: você pode rastrear cliques e/ou aberturas.

   Os resultados do rastreamento serão acessíveis no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report.md)

## Definir a audiência {#audience}

1. Defina o público-alvo como meta. Para fazer isso, clique no botão **[!UICONTROL Seleção do público-alvo]** para exibir a lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais sobre segmentos](../segment/about-segments.md)

   >[!NOTE]
   >
   >Para campanhas acionadas por API, o público-alvo precisa ser definido por meio de uma chamada de API. [Saiba mais](api-triggered-campaigns.md)

   No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Os indivíduos pertencentes a um segmento que não tem a identidade (namespace) selecionada entre suas diferentes identidades não serão direcionados pela campanha.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Agendar a campanha {#schedule}

1. Para executar sua campanha em uma data específica ou em uma frequência recorrente, configure a variável **[!UICONTROL Agendar]** seção. [Saiba como agendar campanhas](#schedule)

1. Para atribuir rótulos de uso de dados personalizados ou principais à campanha, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o Controle de acesso no nível do objeto (OLA)](../administration/object-based-access.md)

Quando a campanha estiver pronta, você poderá revisá-la e publicá-la. [Saiba mais](#review-activate)

## Tipo de campanha {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campanha"
>abstract="Para uma mensagem de marketing ao especificar uma data de envio, a variável **Programado** O tipo é o mais apropriado. No entanto, se você quiser enviar mensagens transacionais, como redefinição de senha ou abandono de cartão, a variável **Acionado por API** é a melhor opção."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoria de campanha"
>abstract="O valor da Categoria é vinculado diretamente ao valor do tipo de campanha. Programe o tipo de campanha para a **Marketing** categoria e tipo acionado por API para a categoria **Transacional**"

Há dois tipos de campanha disponíveis:

* **[!UICONTROL Programado]**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas têm como objetivo enviar **marketing** digite mensagens.

* **[!UICONTROL Acionado por API]**: execute a campanha usando uma chamada de API . As campanhas acionadas por API são destinadas ao envio de **transacional** mensagens, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, abandono de cartão etc. [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)
