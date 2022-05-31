---
title: Definir configurações de email
description: Saiba como definir configurações de email no nível predefinido de mensagens
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 65c2ba7e0931f449a29d1e7ff01d6d68fccca448
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---

# Definir configurações de email {#email-settings}

Defina as configurações de email na seção dedicada da configuração predefinida de mensagem. Saiba como criar predefinições de mensagem em [esta seção](message-presets.md).

![](assets/preset-email.png)

## Tipo de email {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir a categoria de email"
>abstract="Selecione o tipo de mensagem que será enviada ao usar esta predefinição: Marketing para mensagens promocionais, que exigem consentimento do usuário, ou Transacional para mensagens não comerciais, que também podem ser enviadas para perfis sem assinatura em contextos específicos."

No **TIPO DE EMAIL** selecione o tipo de mensagem que será enviada com a predefinição: **Marketing** ou **Transacional**.

* Choose **Marketing** para mensagens promocionais: essas mensagens exigem o consentimento do usuário.

* Choose **Transacional** para mensagens não comerciais, como confirmação de pedido, notificações de redefinição de senha ou informações de delivery, por exemplo.

>[!CAUTION]
>
>**Transacional** as mensagens podem ser enviadas aos perfis que cancelaram a assinatura das comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

When [criação de uma mensagem](../messages/get-started-content.md#create-new-message), você deve escolher uma predefinição de mensagem válida que corresponda à categoria selecionada para a mensagem.

## Subdomínio e pool IP {#subdomains-and-ip-pools}

No **DETALHES DO SUBDOMÍNIO E DO POOL IP** na seção , você deve:

1. Selecione o subdomínio a ser usado para enviar os emails. [Saiba mais](about-subdomain-delegation.md)

1. Selecione o pool de IP a ser associado à predefinição. [Saiba mais](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Não é possível continuar com a criação predefinida enquanto o pool de IP selecionado estiver em [edição](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** e nunca foi associado ao subdomínio selecionado. Caso contrário, a versão mais antiga da associação do pool de IP/subdomínio ainda será usada. Se esse for o caso, salve a predefinição como rascunho e tente novamente depois que o pool de IP tiver a variável **[!UICONTROL Success]** status.

>[!NOTE]
>
>Para ambientes não relacionados à produção, o Adobe não cria subdomínios de teste prontos para uso nem concede acesso a um pool IP de envio compartilhado. Você precisa [delegar seus próprios subdomínios](delegate-subdomain.md) e usar os IPs do pool atribuído à sua organização.

## List-Unsubscribe {#list-unsubscribe}

Em [selecionar um subdomínio](#subdomains-and-ip-pools) na lista, a variável **[!UICONTROL Enable List-Unsubscribe]** será exibida.

![](assets/preset-list-unsubscribe.png)

Essa opção está ativada por padrão.

Se você deixá-lo ativado, um link de cancelamento de subscrição será incluído automaticamente no cabeçalho do email, como:

![](assets/preset-list-unsubscribe-header.png)

Se você desativar esta opção, nenhum link de cancelamento de subscrição será exibido no cabeçalho do email.

O link de cancelamento de subscrição consiste em dois elementos:

* Um **cancelar inscrição do endereço de email**, para a qual todas as solicitações de cancelamento de subscrição são enviadas.

   Em [!DNL Journey Optimizer], o endereço de email de cancelamento de inscrição é o padrão **[!UICONTROL Mailto (unsubscribe)]** endereço exibido na predefinição de mensagem, com base no [subdomínio selecionado](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* O **cancelar inscrição do URL**, que é o URL da landing page onde o usuário será redirecionado depois de cancelado a assinatura.

   Se você adicionar um [link para opção de não participação com um clique](../messages/consent.md#one-click-opt-out) para uma mensagem criada usando essa predefinição, o URL de cancelamento de subscrição será o URL definido para o link de recusa de um clique.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Se você não adicionar um link para opção de não participação com um clique no conteúdo da mensagem, nenhuma landing page será exibida para o usuário.

Saiba mais sobre como adicionar um link de cancelamento de subscrição de cabeçalho às suas mensagens em [esta seção](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parâmetros de cabeçalho{#email-header}

No **[!UICONTROL HEADER PARAMETERS]** , insira os nomes do remetente e os endereços de email associados ao tipo de mensagens enviadas usando essa predefinição.

>[!CAUTION]
>
>Os endereços de email devem usar o [subdomínio delegado](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: O nome do remetente, como o nome da sua marca.

* **[!UICONTROL Sender email]**: O endereço de email que deseja usar para suas comunicações. Por exemplo, se o subdomínio delegado for *marketing.luma.com*, você pode usar *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: O nome que será usado quando o recipient clicar no **Responder** no software cliente de email.

* **[!UICONTROL Reply to (email)]**: O endereço de email que será usado quando o recipient clicar no link **Responder** no software cliente de email. Você deve usar um endereço definido no subdomínio delegado (por exemplo, *reply@marketing.luma.com*), caso contrário, os emails serão descartados.

* **[!UICONTROL Error email]**: Todos os erros gerados pelos ISPs após alguns dias de envio de email (rejeições assíncronas) são recebidos neste endereço.

![](assets/preset-header.png)

>[!NOTE]
>
>Os endereços devem começar com uma letra (A-Z) e só podem conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

### Encaminhar email {#forward-email}

Se quiser encaminhar para um endereço de email específico todos os emails recebidos por [!DNL Journey Optimizer] para o subdomínio delegado, entre em contato com o Atendimento ao Cliente do Adobe. Você precisará fornecer:

* O endereço de email de encaminhamento de sua escolha. Observe que o domínio de endereço de email de encaminhamento não pode corresponder a qualquer subdomínio delegado ao Adobe.
* O nome da sua caixa de proteção.
* O nome predefinido para o qual o endereço de email de encaminhamento será usado.
* O atual **[!UICONTROL Reply to (email)]** endereço definido no nível predefinido.

>[!NOTE]
>
>Só pode haver um endereço de email de encaminhamento por subdomínio. Consequentemente, se várias predefinições usarem o mesmo subdomínio, o mesmo endereço de email de encaminhamento deverá ser usado para todas elas.

O endereço de email de encaminhamento será configurado pelo Adobe. Isso pode levar de 3 a 4 dias.

<!--
## BCC email {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Define a BCC email address"
>abstract="You can keep a copy of sent emails by sending them to a BCC inbox. Enter the email address of your choice so that every email sent is blind-copied to this BCC address. This feature is optional."

You can send an identical copy (or blind carbon copy) of an email sent by [!DNL Journey Optimizer] to a BCC inbox. This optional feature allows you to retain copies of email communications you send to your users for compliance and/or archival purposes. This will be invisible to the delivery recipients.

>[!CAUTION]
>
>This capability will be available starting **May, 31**.

### Enable BCC email {#enable-bcc}

To enable the **[!UICONTROL BCC email]** option, enter the email address of your choice in the dedicated field. You can specify any external address in correct format, except an email address defined on the delegated subdomain. For example, if the delegated subdomain is *marketing.luma.com*, any address like *abc@marketing.luma.com* is prohibited.

>[!NOTE]
>
>You can only define one BCC email address. Make sure the BCC address has enough reception capacity to store all the emails that are sent using the current preset.
>
>More recommendations are listed in [this section](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

All email messages using this preset will be blind-copied to the BCC email address you entered. From there, they can be processed and archived using an external system.

>[!CAUTION]
>
>Your BCC feature usage will be counted against the number of messages you are licensed for. Hence, only enable it in the presets used for critical communications that you wish to archive. Check your contract for licensed volumes.

The BCC email address setting is immediately saved and processed at the preset level. When you [create a new message](../messages/get-started-content.md#create-new-message) using this preset, the BCC email address is automatically displayed.

![](assets/preset-bcc-in-msg.png)

However, the BCC address gets picked up for sending communications following the logic below:

* For batch and burst journeys, it does not apply to batch or burst execution that had already started before the BCC setting is made. The change will be picked up at the next recurrence or new execution.

* For transactional messages, the change is picked up immediately for the next communication (up to one minute delay).

>[!NOTE]
>
>You do not need to republish a message or journey for the BCC setting to be picked up.

### Recommendations and limitations {#bcc-recommendations-limitations}

* To ensure your privacy compliance, BCC emails must be processed by an archiving system capable of storing securely personally identifiable information (PII).

* As messages can contain sensitive or private data, such as personally identifiable information (PII), make sure the BCC address is correct, and secure the access to messages.

* Your inbox used for BCC should be properly managed for space and delivery. If the inbox returns bounces, some emails may not be received and therefore will fail to get archived.

* Messages may be delivered to the BCC email address before the target recipients. BCC messages can also been sent even though the original messages may have [bounced](../reports/suppression-list.md#delivery-failures).

    //////OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK /////////

* Do not open or click through the emails sent to the BCC address as it is taken into account in the total opens and clicks from the send analysis, which could cause some miscalculations in [reports](../reports/message-monitoring.md). 

* Do not mark messages as spam in the BCC inbox, as it will impact all the other emails sent to this address.


>[!CAUTION]
>
>Do not click the unsubscribe link in the emails sent to the BCC address as you will immediately unsubscribe the corresponding recipients.

### GDPR compliance {#gdpr-compliance}

Regulations such as GDPR state that Data Subjects should be able to modify their consent at any time. Because the BCC emails you are sending with Journey Optimizer include securely personally identifiable information (PII), you must edit the **[!UICONTROL CJM Email BCC Feedback Event Schema]** to be able to manage these PII in compliance with GDPR and similar regulations.

To do this, follow the steps below.

1. Go to **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** and select **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

    ![](assets/preset-bcc-schema.png)

1. Click to expand **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]**.

1. Select **[!UICONTROL originalRecipientAddress]**.

1. In the **[!UICONTROL Field properties]** on the right, scroll down to the **[!UICONTROL Identity]** checkbox.

1. Select it and also select **[!UICONTROL Primary identity]**.

1. Select a namespace from the drop-down list.

    ![](assets/preset-bcc-schema-identity.png)

1. Click **[!UICONTROL Apply]**.

>[!NOTE]
>
>Learn more on managing Privacy and the applicable regulations in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target="_blank"}.

### BCC reporting data {#bcc-reporting}

Reporting as such on BCC is not available in the journey and message reports. However, information is stored on a system dataset called **[!UICONTROL AJO BCC Feedback Event Dataset]**. You can run queries against this dataset to find useful information for debugging purpose for example.

You can access this dataset through the user interface. Select **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** and enable the **[!UICONTROL Show system datasets]** toggle from the filter to display the system-generated datasets. Learn more on how to access datasets in [this section](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

To run queries against this dataset, you can use the Query Editor provided by the [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. To access it, select **[!UICONTROL Data management]** > **[!UICONTROL Queries]** and click **[!UICONTROL Create query]**. [Learn more](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Depending on what information you are looking for, you can run the following queries.

1. For all the other queries below, you will need the journey action ID. Run this query to fetch all action IDs associated with a particular journey version ID within the last 2 days:

        ```
        SELECT
        DISTINCT
        CAST(TIMESTAMP AS DATE) AS EventTime,
        _experience.journeyOrchestration.stepEvents.journeyVersionID,
        _experience.journeyOrchestration.stepEvents.actionName, 
        _experience.journeyOrchestration.stepEvents.actionID 
        FROM journey_step_events 
        WHERE 
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
        _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
        TIMESTAMP > NOW() - INTERVAL '2' DAY 
        ORDER BY EventTime DESC;
        ```

    >[!NOTE]
    >
    >To get the `<journey version id>`parameter, select the corresponding [journey version](../building-journeys/journey-versions.md) from the **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** menu. The journey version ID is displayed at the end of the URL displayed in your web browser.
    >
    >![](assets/preset-bcc-action-id.png)

1. Run this query to fetch all message feedback events (especially feedback status) generated for a particular message targeted to a specific user within the last 2 days:

        ```
        SELECT  
        _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
        _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
        timestamp AS EventTime, 
        _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
        _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
        CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
            WHEN 'sent' THEN 'Sent'
            WHEN 'delay' THEN 'Retry'
            WHEN 'out_of_band' THEN 'Bounce' 
            WHEN 'bounce' THEN 'Bounce'
        END AS FeedbackStatusCategory
        FROM cjm_message_feedback_event_dataset 
        WHERE  
            timestamp > now() - INTERVAL '2' day  AND
            _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
            _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
            _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
            ORDER BY EventTime DESC;
        ```

    >[!NOTE]
    >
    >To get the `<journey action id>` parameter, run the first query described above using the journey version id. The `<recipient email address>` parameter is the targeted or actual recipient's email address.

1. Run this query to fetch all BCC message feedback events generated for a particular message targeted to a specific user within the last 2 days:

    ```
    SELECT   
    _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
    _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
    _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
    timestamp AS EventTime, 
    _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
    CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
                WHEN 'sent' THEN 'Sent'
                WHEN 'delay' THEN 'Retry'
                WHEN 'out_of_band' THEN 'Bounce' 
                WHEN 'bounce' THEN 'Bounce'
            END AS FeedbackStatusCategory 
    FROM ajo_bcc_feedback_event_dataset  
    WHERE  
    timestamp > now() - INTERVAL '2' day  AND
    _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
    _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
    _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
    ORDER BY EventTime DESC;
    ```

1. Run this query to fetch all recipient addresses who have not received the message whereas its BCC entry exists within the last 30 days:

    ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
    ```
-->

## Parâmetros de nova tentativa de email {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar o período de tempo de nova tentativa"
>abstract="As tentativas são executadas por 3,5 dias (84 horas) quando uma mensagem de email falha devido a um erro temporário de devolução temporária. Você pode ajustar esse período de tentativas padrão para atender melhor às suas necessidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Sobre tentativas"

Você pode configurar o **Parâmetros de nova tentativa de email**.

![](assets/preset-retry-parameters.png)

Por padrão, a variável [período de tempo de nova tentativa](retries.md#retry-duration) está definida para 84 horas, mas você pode ajustar essa configuração para melhor atender às suas necessidades.

Você deve inserir um valor inteiro (em horas ou minutos) dentro do seguinte intervalo:

* Para emails de marketing, o período mínimo de nova tentativa é de 6 horas.
* Para emails transacionais, o período mínimo de nova tentativa é de 10 minutos.
* Para ambos os tipos de email, o período máximo de tentativas é de 84 horas (ou 5040 minutos).

Saiba mais sobre tentativas em [esta seção](retries.md).

## Rastreamento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parâmetros de rastreamento de URL"
>abstract="Use esta seção para anexar parâmetros de rastreamento automaticamente aos URLs da campanha presentes no seu conteúdo de email."

Você pode usar **[!UICONTROL URL Tracking Parameters]** para medir a eficácia de seus esforços de marketing em todos os canais. Este recurso é opcional.

Os parâmetros definidos nesta seção serão anexados ao final dos URLs incluídos no conteúdo da mensagem de email. Em seguida, você pode capturar esses parâmetros em ferramentas de análise da Web, como Adobe Analytics ou Google Analytics, e criar vários relatórios de desempenho.

![](assets/preset-url-tracking.png)

Três parâmetros de rastreamento de URL são preenchidos automaticamente como um exemplo ao criar uma predefinição de mensagem. Você pode editá-los e adicionar até 10 parâmetros de rastreamento usando o **[!UICONTROL Add new parameter]** botão.

Para configurar um parâmetro de rastreamento de URL, você pode inserir diretamente os valores desejados no **[!UICONTROL Name]** e **[!UICONTROL Value]** ou escolha em uma lista de valores predefinidos navegando até os seguintes objetos:

* Atributos de jornada: **ID de origem**, **Nome da origem**, **ID da versão de origem**
* Atributos de ação: **ID da ação**, **Nome da ação**
* Atributos do offer decisioning: **ID da oferta**, **Nome da oferta**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Não selecione uma pasta: navegue até a pasta necessária e selecione um atributo de perfil para usar como valor de parâmetro de rastreamento.

Abaixo estão exemplos de URLs compatíveis com Adobe Analytics e Google Analytics.

* URL compatível com Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatível com Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>É possível combinar a digitação de valores de texto e a seleção de valores predefinidos. Cada **[!UICONTROL Value]** pode conter até 255 caracteres no total.
