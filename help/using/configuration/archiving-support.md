---
solution: Journey Optimizer
product: journey optimizer
title: Suporte para arquivamento no Journey Optimizer
description: Saiba como arquivar mensagens
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: arquivamento, mensagens, HIPAA, CCO, e-mails
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: de90083d67787495a28ee45f5912d2cbb0c0ff0c
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 6%

---

# Suporte para arquivamento {#archiving-support}

## Como arquivar mensagens {#about-archiving}

Regulamentos como o HIPAA exigem que [!DNL Journey Optimizer] forneça uma maneira de arquivar mensagens enviadas a indivíduos. Na verdade, se os clientes fizerem uma reclamação, eles deverão ter a capacidade de obter uma cópia da mensagem enviada para fins de verificação.

* Para o canal de email, [!DNL Journey Optimizer] fornece um recurso interno de email com CCO. [Saiba mais](#bcc-email)

* Além disso, para todos os canais, você pode usar o campo &quot;Modelo&quot; no **Conjunto de Dados da Entidade**, que contém os detalhes dos modelos de mensagem não personalizados. Exporte o conjunto de dados com este campo para salvar metadados como: quem enviou a mensagem, para quem e quando. Observe que os dados personalizados não são exportados - somente o template (formato e estrutura da mensagem) é levado em consideração. [Saiba mais](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] não tem suporte para o requisito de arquivamento de SMS. Para obter suporte dedicado ao arquivamento, trabalhe com seu fornecedor de SMS (Sinch, Infobip ou Twilio).

## Como usar o campo CCO para emails {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definir um endereço de email CCO"
>abstract="Você pode manter uma cópia dos emails enviados enviando-os para uma caixa de entrada CCO. Digite o endereço de email de sua escolha para que cada email enviado seja copiado para o CCO. Observe que o domínio de endereço CCO deve ser distinto de qualquer subdomínio delegado à Adobe. Esse recurso é opcional."

Você pode enviar uma cópia oculta (Cco) de um email enviado por [!DNL Journey Optimizer] a um endereço CCO dedicado. Esse recurso opcional permite reter cópias das comunicações por e-mail enviadas aos usuários para fins de conformidade e/ou arquivamento. O endereço CCO não está visível para outros destinatários da mensagem.

### Habilitar email com CCO {#enable-bcc}

Para habilitar a opção **[!UICONTROL Email com CCO]**, digite o endereço de email de sua escolha no campo dedicado da [configuração de canal](channel-surfaces.md) (ou seja, predefinição de mensagem). Você pode especificar qualquer endereço externo no formato correto, exceto um endereço de email definido em um subdomínio delegado ao Adobe. Por exemplo, se você delegou o subdomínio *marketing.luma.com* ao Adobe, qualquer endereço como *abc@marketing.luma.com* será proibido.

>[!CAUTION]
>
>Você só pode definir um endereço de email de CCO. Verifique se o endereço CCo tem capacidade de recepção suficiente para armazenar todos os emails enviados usando a configuração de canal atual.
>
>Mais recomendações estão listadas em [esta seção](#bcc-recommendations-limitations).

>[!NOTE]
>
>Se você adquiriu a oferta complementar Healthcare Shield, deve garantir que o ISP de seus endereços BCC ofereça suporte ao protocolo TLS 1.2.

![](assets/preset-bcc.png)

Quando a configuração estiver concluída, todas as mensagens de email baseadas nessa configuração serão copiadas de forma oculta para o endereço de email CCO inserido. A partir daí, as mensagens podem ser processadas e arquivadas usando um sistema externo.

>[!CAUTION]
>
>O uso do recurso CCO é contabilizado em relação ao número de mensagens para as quais você está licenciado. Portanto, ative-o somente nas configurações usadas para comunicações críticas que você deseja arquivar. Verifique se há volumes licenciados em seu contrato.

A configuração de endereço de email CCO é imediatamente salva e processada no nível de configuração. Ao criar uma nova mensagem usando essa configuração, o endereço de email de CCO é exibido automaticamente.

![](assets/preset-bcc-in-msg.png)

No entanto, o endereço CCO é selecionado para o envio de comunicações seguindo a lógica descrita [aqui](../email/email-settings.md).

### Recommendations e limitações {#bcc-recommendations-limitations}

* Para garantir sua conformidade com a privacidade, os emails com CCO devem ser processados por um sistema de arquivamento capaz de armazenar com segurança informações de identificação pessoal (PII).

* Como as mensagens podem conter dados confidenciais ou privados, como informações de identificação pessoal (PII), verifique se o endereço CCO está correto e proteja o acesso às mensagens.

* Sua caixa de entrada usada para Cco deve ser gerenciada corretamente para espaço e entrega. Se a caixa de entrada retornar rejeições, alguns emails poderão não ser recebidos e, portanto, não serão arquivados.

* As mensagens podem ser entregues no endereço de email de CCO antes dos recipients do público-alvo. As mensagens com CCO também podem ser enviadas mesmo que as mensagens originais tenham [devolvido](../reports/suppression-list.md#delivery-failures).

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Não abra ou clique nos emails enviados para o endereço CCo, pois ele é considerado no total de aberturas e cliques da análise de envio, o que pode causar alguns erros de cálculo em [relatórios](../reports/global-report.md).

* Não marque mensagens como spam na caixa de entrada CCO, pois isso afetará todos os outros emails enviados para esse endereço.

>[!CAUTION]
>
>Não clique no link de cancelamento de inscrição nos emails enviados para o endereço CCo, pois você cancelará imediatamente a inscrição dos recipients correspondentes.

### Conformidade com o GDPR {#gdpr-compliance}

Regulamentos como o GDPR afirmam que os titulares de dados devem poder modificar seu consentimento a qualquer momento. Como os emails com CCO que você está enviando com o Journey Optimizer incluem informações pessoalmente identificáveis com segurança (PII), você deve editar o **[!UICONTROL Esquema de evento de feedback CCO de email do CJM]** para gerenciar essas PII em conformidade com o GDPR e regulamentos semelhantes.

Para fazer isso, siga as etapas abaixo.

1. Vá para **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Esquemas]** > **[!UICONTROL Procurar]** e selecione **[!UICONTROL Esquema de Evento de Comentários CCO de Email CJM]**.

   ![](assets/preset-bcc-schema.png)

1. Clique para expandir a **[!UICONTROL _experiência]**, **[!UICONTROL customerJourneyManagment]** e depois **[!UICONTROL secondaryRecipientDetail]**.

1. Selecione **[!UICONTROL originalRecipientAddress]**.

1. Nas **[!UICONTROL Propriedades do campo]** à direita, role até a caixa de seleção **[!UICONTROL Identidade]**.

1. Selecione e também selecione **[!UICONTROL Identidade principal]**.

1. Selecione um namespace na lista suspensa.

   ![](assets/preset-bcc-schema-identity.png)

1. Clique em **[!UICONTROL Aplicar]**.

>[!NOTE]
>
>Saiba mais sobre como gerenciar a privacidade e os regulamentos aplicáveis na [documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target="_blank"}.

### Dados de relatório CCO {#bcc-reporting}

Criar relatórios como tal no Cco não está disponível nos relatórios de jornada e mensagem. No entanto, as informações são armazenadas em um conjunto de dados do sistema chamado **[!UICONTROL Conjunto de Dados de Eventos de Comentários Cco do AJO]**. Você pode executar consultas nesse conjunto de dados para encontrar informações úteis para fins de depuração, por exemplo.

Para acessar este conjunto de dados por meio da interface, selecione **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Conjuntos de dados]** > **[!UICONTROL Procurar]**. Saiba mais sobre como acessar conjuntos de dados em [esta seção](../data/get-started-datasets.md#access-datasets).

<!--![](assets/preset-bcc-dataset.png)-->

Para executar consultas neste conjunto de dados, você pode usar o Editor de consultas fornecido pelo [Serviço de consulta do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. Para acessá-lo, selecione **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Consultas]** e clique em **[!UICONTROL Criar consulta]**. [Saiba mais](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Dependendo das informações que você está procurando, é possível executar as seguintes consultas.

1. Para todas as outras consultas abaixo, você precisará da ID de ação de jornada. Execute esta consulta para buscar todas as IDs de ação associadas a uma ID de versão de jornada específica nos últimos 2 dias:

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
   >Para obter o parâmetro `<journey version id>`selecione a [versão do jornada](../building-journeys/journey.md#journey-versions) correspondente no menu **[!UICONTROL gerenciamento de Jornadas]** > **[!UICONTROL Jornada]**. O ID da versão do jornada é exibido no final do URL exibido no navegador da Web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Execute esta consulta para buscar todos os eventos de feedback de mensagem (especialmente o status de feedback) gerados para uma mensagem específica direcionada a um usuário específico nos últimos dois dias:

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
   >Para obter o parâmetro `<journey action id>`, execute a primeira consulta descrita acima usando a ID da versão do jornada. O parâmetro `<recipient email address>` é o endereço de email do destinatário real ou direcionado.

1. Execute esta consulta para buscar todos os eventos de feedback de mensagem CCO gerados para uma mensagem específica direcionada a um usuário específico nos últimos dois dias:

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

1. Execute esta consulta para buscar todos os endereços de destinatários que não receberam a mensagem enquanto sua entrada CCO existe nos últimos 30 dias:

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

### Usar cabeçalho de mensagem para reconciliar informações de cópia CCO e email enviado {#bcc-header}

Quando as cópias Cco de email são arquivadas em um sistema externo, por exemplo, você pode recuperar as informações nos emails enviados correspondentes usando um cabeçalho incluído na mensagem.

Cada mensagem de email agora contém um cabeçalho chamado `x-message-profile-id`. O valor desse cabeçalho é diferente para cada perfil: ele é exclusivo para cada email enviado e para sua cópia de email CCO correspondente.

O cabeçalho `x-message-profile-id` também é armazenado nos seguintes conjuntos de dados do sistema: [Conjunto de Dados do Evento de Feedback de Mensagens do AJO](../data/datasets-query-examples.md#message-feedback-event-dataset) (emails enviados) e [Conjunto de Dados do Evento de Feedback de Cco de AJO](#bcc-reporting) (cópias Cco). Você pode consultar esses conjuntos de dados para reconciliar a cópia CCO e o email real correspondente.

* Para acessar esses conjuntos de dados por meio da interface, selecione **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Conjuntos de dados]** > **[!UICONTROL Procurar]**. Saiba mais sobre como acessar conjuntos de dados em [esta seção](../data/get-started-datasets.md#access-datasets).

* Use o Editor de Consultas fornecido pelo [Serviço de Consulta Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. Para acessá-lo, selecione **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Consultas]** e clique em **[!UICONTROL Criar consulta]**. [Saiba mais](../data/get-started-queries.md)

Abaixo estão alguns exemplos de consultas que você pode executar para recuperar informações correspondentes às suas cópias CCO.

**Consulta 1**

Para obter o evento CCO compilado com o evento de feedback correspondente para o email real com os detalhes da ação da campanha:

```
SELECT
  mfe.timestamp AS OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  bcc._experience.customerJourneyManagement.emailChannelContext.address AS BCCEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.campaignID AS CampaignID,
  mfe._experience.customerJourneyManagement.messageExecution.campaignActionID AS CampaignActionID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN ajo_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = '<x-message-profile-id>'
ORDER BY mfe.timestamp DESC;
```

**Consulta 2**

Para anexar o evento de CCO ao evento de feedback correspondente do email real com os detalhes da ação de jornada:

```
SELECT
  mfe.timestamp AS OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  bcc._experience.customerJourneyManagement.emailChannelContext.address AS BCCEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AS journeyActionID,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionInstanceID AS JourneyVersionInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN ajo_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = '<x-message-profile-id>'
ORDER BY mfe.timestamp DESC;
```
