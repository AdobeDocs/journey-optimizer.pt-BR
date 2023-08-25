---
solution: Journey Optimizer
product: journey optimizer
title: Suporte para arquivamento no Journey Optimizer
description: Saiba como arquivar mensagens
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: arquivamento, mensagens, HIPAA, CCO, e-mails
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 315309fdede3aa095fc59266acf765dc4b782dd9
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 7%

---

# Suporte para arquivamento {#archiving-support}

## Como arquivar mensagens {#about-archiving}

Regulamentos como a HIPAA exigem que [!DNL Journey Optimizer] O deve fornecer uma maneira de arquivar mensagens enviadas a indivíduos. Na verdade, se os clientes fizerem uma reclamação, eles deverão ter a capacidade de obter uma cópia da mensagem enviada para fins de verificação.

* Para o canal de email, [!DNL Journey Optimizer] O fornece um recurso de email com CCO integrado. [Saiba mais](#bcc-email)

* Além disso, para todos os canais, é possível usar o campo &quot;Modelo&quot; na **Conjunto de dados da entidade**, que contém os detalhes dos modelos de mensagem não personalizados. Exporte o conjunto de dados com este campo para salvar metadados como: quem enviou a mensagem, para quem e quando. Observe que os dados personalizados não são exportados - somente o template (formato e estrutura da mensagem) é levado em consideração. [Saiba mais](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] O não é compatível com o requisito de arquivamento de SMS. Para obter suporte dedicado ao arquivamento, trabalhe com seu fornecedor de SMS (Synch ou Twilio).

## Como usar o CCO para emails {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definir um endereço de email CCO"
>abstract="Você pode manter uma cópia dos emails enviados enviando-os para uma caixa de entrada CCO. Digite o endereço de email de sua escolha para que cada email enviado seja copiado para o CCO. Observe que o domínio do endereço CCo deve ser diferente de qualquer subdomínio delegado ao Adobe. Esse recurso é opcional."

Você pode enviar uma cópia oculta (Cco) de um email enviado por [!DNL Journey Optimizer] para um endereço CCO dedicado. Esse recurso opcional permite reter cópias das comunicações por e-mail enviadas aos usuários para fins de conformidade e/ou arquivamento. O endereço CCO não está visível para outros destinatários da mensagem.

### Habilitar email com CCO {#enable-bcc}

Para ativar o **[!UICONTROL Email com CCO]** opção, insira o endereço de email de sua escolha no campo dedicado da [superfície de canal](channel-surfaces.md) (ou seja, predefinição de mensagem). Você pode especificar qualquer endereço externo no formato correto, exceto um endereço de email definido em um subdomínio delegado ao Adobe. Por exemplo, se você delegou o *marketing.luma.com* subdomínio para Adobe, qualquer endereço como *abc@marketing.luma.com* é proibida.

>[!CAUTION]
>
>Você só pode definir um endereço de email de CCO. Verifique se o endereço CCo tem capacidade de recepção suficiente para armazenar todos os emails enviados usando a superfície de canal atual.
>
>Mais recomendações estão listadas em [nesta seção](#bcc-recommendations-limitations).

>[!NOTE]
>
>Se você adquiriu a oferta complementar Healthcare Shield, deve garantir que o ISP de seus endereços BCC ofereça suporte ao protocolo TLS 1.2.

![](assets/preset-bcc.png)

Quando a configuração for concluída, todas as mensagens de email baseadas nessa superfície serão copiadas de forma oculta para o endereço de email CCO inserido. A partir daí, as mensagens podem ser processadas e arquivadas usando um sistema externo.

>[!CAUTION]
>
>O uso do recurso CCO é contabilizado em relação ao número de mensagens para as quais você está licenciado. Portanto, ative-o somente nas superfícies usadas para comunicações críticas que você deseja arquivar. Verifique se há volumes licenciados em seu contrato.

A configuração de endereço de email com CCO é imediatamente salva e processada no nível da superfície. Ao criar uma nova mensagem usando essa superfície, o endereço de email de CCO é exibido automaticamente.

![](assets/preset-bcc-in-msg.png)

No entanto, o endereço CCo é selecionado para envio de comunicações seguindo a lógica descrita [aqui](../email/email-settings.md).

### Recommendations e limitações {#bcc-recommendations-limitations}

* Para garantir sua conformidade com a privacidade, os emails com CCO devem ser processados por um sistema de arquivamento capaz de armazenar com segurança informações de identificação pessoal (PII).

* Como as mensagens podem conter dados confidenciais ou privados, como informações de identificação pessoal (PII), verifique se o endereço CCO está correto e proteja o acesso às mensagens.

* Sua caixa de entrada usada para Cco deve ser gerenciada corretamente para espaço e entrega. Se a caixa de entrada retornar rejeições, alguns emails poderão não ser recebidos e, portanto, não serão arquivados.

* As mensagens podem ser entregues no endereço de email de CCO antes dos recipients do público-alvo. As mensagens com CCO também podem ser enviadas mesmo que as mensagens originais [rejeitado](../reports/suppression-list.md#delivery-failures).

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Não abra ou clique nos emails enviados para o endereço CCo, pois ele é considerado no total de aberturas e cliques da análise de envio, o que pode causar alguns erros de cálculo no [relatórios](../reports/global-report.md).

* Não marque mensagens como spam na caixa de entrada CCO, pois isso afetará todos os outros emails enviados para esse endereço.

>[!CAUTION]
>
>Não clique no link de cancelamento de inscrição nos emails enviados para o endereço CCo, pois você cancelará imediatamente a inscrição dos recipients correspondentes.

### Conformidade com o GDPR {#gdpr-compliance}

Regulamentos como o GDPR afirmam que os titulares de dados devem poder modificar seu consentimento a qualquer momento. Como os emails com CCO que você está enviando com o Journey Optimizer incluem informações pessoalmente identificáveis com segurança (PII), você deve editar o **[!UICONTROL Esquema do evento de feedback CCO do email do CJM]** ser capaz de gerenciar essas PII em conformidade com o GDPR e regulamentos semelhantes.

Para fazer isso, siga as etapas abaixo.

1. Ir para **[!UICONTROL Gestão de dados]** > **[!UICONTROL Esquemas]** > **[!UICONTROL Procurar]** e selecione **[!UICONTROL Esquema do evento de feedback CCO do email do CJM]**.

   ![](assets/preset-bcc-schema.png)

1. Clique para expandir **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** depois **[!UICONTROL secondaryRecipientDetail]**.

1. Selecionar **[!UICONTROL endereçoDestinatárioOriginal]**.

1. No **[!UICONTROL Propriedades do campo]** à direita, role para baixo até a **[!UICONTROL Identidade]** caixa de seleção

1. Selecione e também selecione **[!UICONTROL Identidade principal]**.

1. Selecione um namespace na lista suspensa.

   ![](assets/preset-bcc-schema-identity.png)

1. Clique em **[!UICONTROL Aplicar]**.

>[!NOTE]
>
>Saiba mais sobre como gerenciar a privacidade e os regulamentos aplicáveis na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target="_blank"}.

### Dados de relatório CCO {#bcc-reporting}

Criar relatórios como tal no Cco não está disponível nos relatórios de jornada e mensagem. No entanto, as informações são armazenadas em um conjunto de dados do sistema chamado **[!UICONTROL Conjunto de dados do evento de feedback CCO do AJO]**. Você pode executar consultas nesse conjunto de dados para encontrar informações úteis para fins de depuração, por exemplo.

Você pode acessar esse conjunto de dados por meio da interface do usuário. Selecionar **[!UICONTROL Gestão de dados]** > **[!UICONTROL Conjuntos de dados]** > **[!UICONTROL Procurar]** e habilite o **[!UICONTROL Mostrar conjuntos de dados do sistema]** alterne do filtro para exibir os conjuntos de dados gerados pelo sistema. Saiba mais sobre como acessar conjuntos de dados no [nesta seção](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Para executar consultas nesse conjunto de dados, você pode usar o Editor de consultas fornecido pelo [Serviço de consulta Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. Para acessá-lo, selecione **[!UICONTROL Gestão de dados]** > **[!UICONTROL Consultas]** e clique em **[!UICONTROL Criar consulta]**. [Saiba mais](../data/get-started-queries.md)

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
   >Para obter a `<journey version id>`, selecione o parâmetro correspondente [Versão do jornada](../building-journeys/journey.md#journey-versions) do **[!UICONTROL Gerenciamento de jornadas]** > **[!UICONTROL Jornadas]** menu. O ID da versão do jornada é exibido no final do URL exibido no navegador da Web.
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
   >Para obter a `<journey action id>` , execute a primeira consulta descrita acima usando a id de versão do jornada. A variável `<recipient email address>` é o endereço de email do recipient direcionado ou real.

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
