---
solution: Journey Optimizer
product: journey optimizer
title: Suporte ao arquivamento no Journey Optimizer
description: Saiba como arquivar mensagens
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 3%

---

# Suporte para arquivamento {#archiving-support}

## Como arquivar mensagens {#about-archiving}

Regulamentos como o HIPAA exigem que [!DNL Journey Optimizer] O deve fornecer uma maneira de arquivar mensagens enviadas a indivíduos. Na verdade, se seus clientes gerarem uma solicitação, eles deverão ter a capacidade de obter uma cópia da mensagem enviada para fins de verificação.

* Para o canal de email, [!DNL Journey Optimizer] O fornece um recurso de email CCO integrado. [Saiba mais](#bcc-email)

* Além disso, para todos os canais, você pode usar o campo &quot;Template&quot; no **Conjunto de dados da entidade**, que contém os detalhes dos templates de mensagem não personalizados. Exporte o conjunto de dados com este campo para salvar metadados como: quem enviou a mensagem, para quem e quando. Observe que os dados personalizados não são exportados - somente o modelo (formato e estrutura da mensagem) é levado em conta. [Saiba mais](../start/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] não é o proprietário do suporte para o requisito de arquivamento de SMS. Para obter suporte de arquivamento dedicado, trabalhe com seu fornecedor de SMS (Synch ou Twilio).

## Como usar o CCO para emails {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definir um endereço de email CCO"
>abstract="Você pode manter uma cópia dos emails enviados enviando-os para uma caixa de entrada CCO. Digite o endereço de email de sua escolha para que cada email enviado seja copiado para o CCO. Observe que o domínio de endereço CCO não deve ser o mesmo que qualquer subdomínio delegado ao Adobe. Este recurso é opcional."

Você pode enviar uma cópia idêntica (ou cópia oculta de carbono) de um email enviado por [!DNL Journey Optimizer] para uma caixa de entrada CCO. Esse recurso opcional permite reter cópias das comunicações por email enviadas aos usuários para fins de conformidade e/ou arquivamento. Isso será invisível para os recipients do delivery.

### Habilitar email CCO {#enable-bcc}

Para ativar o **[!UICONTROL Email CCO]** , insira o endereço de email de sua escolha no campo dedicado da variável [superfície do canal](channel-surfaces.md) (ou seja, predefinição de mensagem). Você pode especificar qualquer endereço externo no formato correto, exceto um endereço de email definido em um subdomínio delegado ao Adobe. Por exemplo, se você delegou o *marketing.luma.com* subdomínio para Adobe, qualquer endereço como *abc@marketing.luma.com* é proibida.

>[!CAUTION]
>
>Você só pode definir um endereço de email CCO. Verifique se o endereço CCO tem capacidade de recepção suficiente para armazenar todos os emails enviados usando a superfície do canal atual.
>
>Mais recomendações estão listadas em [esta seção](#bcc-recommendations-limitations).

>[!NOTE]
>
>Se você adquiriu a oferta complementar do Healthcare Shield, é necessário garantir que o ISP do seu endereço CCO seja compatível com o protocolo TLS 1.2.

![](assets/preset-bcc.png)

Todas as mensagens de email que usam essa superfície serão copiadas para o CCO para o endereço de email inserido. A partir daí, eles podem ser processados e arquivados usando um sistema externo.

>[!CAUTION]
>
>O uso do recurso CCO será contado em relação ao número de mensagens para as quais você está licenciado. Assim, ative-o apenas nas superfícies usadas para comunicações críticas que você deseja arquivar. Verifique se há volumes licenciados em seu contrato.

A configuração de endereço de email CCO é imediatamente salva e processada no nível da superfície. Quando você [criar uma nova mensagem](../messages/get-started-content.md) usando essa superfície, o endereço de email CCO é exibido automaticamente.

![](assets/preset-bcc-in-msg.png)

No entanto, o endereço CCO é selecionado para enviar comunicações seguindo a lógica abaixo:

* Para jornadas em lote e em burst, não se aplica à execução em lote ou em burst que já havia sido iniciada antes da definição de Cco ser feita. A alteração será selecionada na próxima recorrência ou nova execução.

* Para mensagens transacionais, a alteração é selecionada imediatamente para a próxima comunicação (atraso de até um minuto).

>[!NOTE]
>
>Não é necessário republicar sua jornada para que a configuração Cco seja selecionada.

### Recommendations e limitações {#bcc-recommendations-limitations}

* Para garantir sua conformidade com a privacidade, os emails do CCO devem ser processados por um sistema de arquivamento capaz de armazenar informações de identificação pessoal (PII) seguras.

* Como as mensagens podem conter dados confidenciais ou privados, como informações de identificação pessoal (PII), verifique se o endereço CCO está correto e proteja o acesso às mensagens.

* Sua caixa de entrada usada para Cco deve ser gerenciada adequadamente para espaço e entrega. Se a caixa de entrada retornar rejeições, alguns emails poderão não ser recebidos e, portanto, não serão arquivados.

* As mensagens podem ser entregues ao endereço de email CCo antes dos recipients do target. As mensagens Cco também podem ser enviadas mesmo que as mensagens originais tenham [devolvido](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Não abra ou clique nos emails enviados para o endereço CCO, pois são considerados no total de aberturas e cliques da análise de envio, o que pode causar alguns erros de cálculo no [relatórios](../reports/global-report.md).

* Não marque mensagens como spam na caixa de entrada CCO, pois isso afetará todos os outros emails enviados para esse endereço.


>[!CAUTION]
>
>Não clique no link de cancelamento de subscrição nos emails enviados para o endereço CCo, pois você cancelará imediatamente a assinatura dos recipients correspondentes.

### Conformidade com o RGPD {#gdpr-compliance}

Regulamentos como o GDPR afirmam que os titulares de dados devem poder modificar o consentimento a qualquer momento. Como os emails CCO que você está enviando com o Journey Optimizer incluem informações de identificação pessoal (PII) seguras, você deve editar a variável **[!UICONTROL Esquema de evento de feedback CCO de email CJM]** para gerenciar essas PII de acordo com o GDPR e regulamentos semelhantes.

Para fazer isso, siga as etapas abaixo.

1. Ir para **[!UICONTROL Gestão de dados]** > **[!UICONTROL Esquemas]** > **[!UICONTROL Procurar]** e selecione **[!UICONTROL Esquema de evento de feedback CCO de email CJM]**.

   ![](assets/preset-bcc-schema.png)

1. Clique para expandir **[!UICONTROL _experiência]**, **[!UICONTROL customerJourneyManagement]** then **[!UICONTROL secondaryRecipientDetail]**.

1. Selecionar **[!UICONTROL originalRecipientAddress]**.

1. No **[!UICONTROL Propriedades do campo]** à direita, role para baixo até o **[!UICONTROL Identidade]** caixa de seleção.

1. Selecione-o e também selecione **[!UICONTROL Identidade primária]**.

1. Selecione um namespace na lista suspensa.

   ![](assets/preset-bcc-schema-identity.png)

1. Clique em **[!UICONTROL Aplicar]**.

>[!NOTE]
>
>Saiba mais sobre como gerenciar a privacidade e os regulamentos aplicáveis na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

### Dados de relatórios CCO {#bcc-reporting}

Os relatórios como tal no CCO não estão disponíveis na jornada e nos relatórios de mensagem. No entanto, as informações são armazenadas em um conjunto de dados do sistema chamado **[!UICONTROL Conjunto de dados do evento de feedback CCO AJO]**. Você pode executar consultas em relação a esse conjunto de dados para encontrar informações úteis para fins de depuração, por exemplo.

Você pode acessar esse conjunto de dados por meio da interface do usuário do . Selecionar **[!UICONTROL Gestão de dados]** > **[!UICONTROL Conjuntos de dados]** > **[!UICONTROL Procurar]** e ativar **[!UICONTROL Mostrar conjuntos de dados do sistema]** alterne do filtro para exibir os conjuntos de dados gerados pelo sistema. Saiba mais sobre como acessar conjuntos de dados no [esta seção](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Para executar consultas em relação a esse conjunto de dados, você pode usar o Editor de consultas fornecido pelo [Serviço de query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. Para acessá-lo, selecione **[!UICONTROL Gestão de dados]** > **[!UICONTROL Queries]** e clique em **[!UICONTROL Criar query]**. [Saiba mais](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Dependendo de quais informações você estiver procurando, é possível executar as seguintes consultas.

1. Para todas as outras consultas abaixo, será necessário a ID de ação do jornada. Execute esta consulta para buscar todas as IDs de ação associadas a uma ID de versão do jornada específica nos últimos 2 dias:

       &quot;
       SELECIONAR
       DISTINTO
       CAST(CARIMBO DE DATA E HORA COMO DATA) COMO EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM jornada_step_events
       ONDE
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.journeyOrchestration.stepEvents.actionID não é NULL AND
       CARIMBO DE DATA E HORA > NOW() - INTERVALO &#39;2&#39; DIA
       ORDEM POR EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Para obter o `<journey version id>`selecione o [Versão do jornada](../building-journeys/journey-versions.md) do **[!UICONTROL Gerenciamento de jornadas]** > **[!UICONTROL Jornada]** menu. A ID da versão do jornada é exibida no final do URL exibido no navegador da Web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Execute esta consulta para buscar todos os eventos de feedback de mensagem (especialmente o status de feedback) gerados para uma mensagem específica direcionada a um usuário específico nos últimos 2 dias:

       &quot;
       SELECIONAR
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjorneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE _experience.customerjorneymanagement.messagedeliveryfeedback.feedbackStatus
       QUANDO &#39;enviado&#39; ENTÃO &#39;ENVIADO&#39;
       QUANDO &#39;atraso&#39; E DEPOIS &#39;Repetir&#39;
       QUANDO &#39;out_of_band&#39; ENTÃO &#39;Bounce&#39;
       QUANDO &#39;saltar&#39; E DEPOIS &#39;Rejeitar&#39;
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       ONDE
       timestamp > now() - INTERVAL &#39;2&#39; day E
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       ORDEM POR EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Para obter o `<journey action id>` execute a primeira consulta descrita acima usando a id da versão do jornada. O `<recipient email address>` é o endereço de email do recipient real ou direcionado.

1. Execute esta consulta para buscar todos os eventos de feedback de mensagem CCO gerados para uma mensagem específica direcionada a um usuário específico nos últimos 2 dias:

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

1. Execute esta query para buscar todos os endereços de recipient que não receberam a mensagem, enquanto sua entrada CCO existe nos últimos 30 dias:

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
