---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global
description: Saiba como usar dados do relatório global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 3%

---

# Introdução ao Relatório global {#global-report}

>[!NOTE]
>
> Se as consultas personalizadas forem feitas por meio de APIs ao usar o Serviço de consulta, espere algum atraso para seus relatórios.

Use o **[!UICONTROL Relatório global]** para medir o impacto das jornadas e deliveries em um período selecionado.

* Se quiser direcionar uma jornada ou deliveries no contexto de uma jornada, no **[!UICONTROL Jornadas]** , acesse sua jornada e clique no botão **[!UICONTROL Exibir relatório]** botão. Você pode encontrar os relatórios globais de Jornada, Email, SMS e Push.

  ![](assets/report_journey.png)

* Se quiser direcionar uma campanha, no **[!UICONTROL Campanhas]** , acesse sua campanha e clique no link **[!UICONTROL Relatórios]** botão.

  ![](assets/report_campaign.png)

* Se você deseja alternar do **[!UICONTROL Relatório ao vivo]** para o **[!UICONTROL Relatório global]** para o seu delivery, clique em **[!UICONTROL O tempo todo]** no alternador de guias.

  ![](assets/report_5.png)

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](#list-of-components-global)

## Personalizar painel {#modify-dashboard}

Cada painel de relatório pode ser modificado alterando o período de tempo e redimensionando ou removendo widgets. Alterar os widgets afeta apenas o painel do usuário atual. Outros usuários verão seus próprios painéis ou os definidos por padrão.

1. No relatório Global, selecione uma hora de Início e Término para direcionar dados específicos.

   ![](assets/report_modify_1.png)

1. Para seus relatórios de Jornada que envolvem várias configurações **[!UICONTROL Ações]**, escolha um específico **[!UICONTROL Ação]** no menu suspenso.

1. Se quiser direcionar apenas uma ou várias mensagens recorrentes, selecione-as no **[!UICONTROL Tempo de execução]** menu suspenso.

   ![](assets/report_modify_12.png)

1. Escolha se deseja excluir eventos de teste de seus relatórios com a barra de alternância. Para obter mais informações sobre eventos de teste, consulte [esta página](../building-journeys/testing-the-journey.md).

   Observe que **[!UICONTROL Excluir eventos de teste]** A opção só está disponível para relatórios de Jornada.

   ![](assets/report_modify_2.png)

1. Clique em **[!UICONTROL Modificar]** para começar a personalizar seu painel.

   ![](assets/report_modify_3.png)

1. Ajuste o tamanho dos widgets arrastando o canto inferior direito.

   ![](assets/report_modify_4.png)

1. Clique em **[!UICONTROL Remover]** para remover qualquer widget desnecessário.

   ![](assets/report_modify_5.png)

1. Quando estiver satisfeito com a ordem de exibição e o tamanho dos widgets, clique em **[!UICONTROL Salvar]**.

1. Para personalizar a forma como seus dados são exibidos, você pode alternar entre diferentes opções de visualização, como gráficos, tabelas e gráficos de rosca.

   ![](assets/report_modify_10.png)

O painel foi salvo. Suas diferentes alterações serão reaplicadas para um uso posterior de seus relatórios ao vivo. Se necessário, use o **[!UICONTROL Redefinir]** opção para restaurar os widgets padrão e a ordem dos widgets.

## Exportar seus relatórios {#export-reports}

É possível exportar facilmente seus diferentes relatórios para formatos PDF ou CSV, o que permite compartilhá-los ou imprimi-los. As etapas para exportar relatórios estão detalhadas nas guias abaixo.

➡️ [Descubra este recurso no vídeo](#video-csv)


>[!BEGINTABS]

>[!TAB Exportar seu relatório como um arquivo CSV]

1. No seu relatório, clique em **[!UICONTROL Exportar]** e selecione **[!UICONTROL Arquivo CSV]** para gerar um arquivo CSV no nível geral do relatório.

   ![](assets/export_1.png)

1. Você também pode optar por exportar dados de um widget específico. Clique em **[!UICONTROL Exportar dados do widget para CSV]** ao lado do widget selecionado.

   ![](assets/export_3.png)

1. O arquivo é baixado automaticamente e pode ser localizado em seus arquivos locais.

   Se você gerou o arquivo no nível do relatório, ele contém informações detalhadas para cada widget, incluindo seu título e dados.

   Se você gerou o arquivo no nível do widget, ele fornece especificamente os dados para o widget selecionado.

>[!TAB Exportar seu relatório como um arquivo PDF]

1. No seu relatório, clique em **[!UICONTROL Exportar]** e selecione **[!UICONTROL arquivo PDF]**.

   ![](assets/export_2.png)

1. Na janela Imprimir, configure o documento conforme necessário. Observe que as opções podem variar dependendo do navegador.

1. Escolha imprimir ou salvar seu relatório como PDF.

1. Localize a pasta onde deseja salvar o arquivo, renomeie-a se necessário e clique em Salvar.

Seu relatório agora está disponível para visualização ou compartilhamento em um arquivo pdf.



>[!ENDTABS]


### Exportar relatórios (vídeo) {#video-csv}

Saiba como baixar um relatório CSV para um relatório e um único widget no vídeo explicativo a seguir.

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)



>[!CONTEXTUALHELP]
>id="ajo_report_campaign_ctr"
>title="CTR"
>abstract="Widget do CTR"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_clicks"
>title="Cliques"
>abstract="Widget de Cliques"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_delivered"
>title="Entregues"
>abstract="Widget entregue"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_overview"
>title="Visão geral da campanha"
>abstract="Widget de visão geral do Campaign"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_funnel"
>title="Resultados do funil de campanha"
>abstract="Widget de resultados do funil da campanha"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_tracking_link"
>title="Rótulos de link rastreado"
>abstract="Widget de rótulos de links rastreados"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_displays"
>title="Exibições"
>abstract="Widget de exibições"

<!--campaign email-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivered_click"
>title="Tendência de cliques e entregas"
>abstract="Widget de tendência de clique e entrega"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivery_status"
>title="Status da entrega"
>abstract="Widget de status de entrega"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_sending_statistics"
>title="Estatísticas de envio"
>abstract="Widget de estatísticas de envio"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracking_statistics"
>title="Estatísticas de rastreamento"
>abstract="Widget de estatísticas de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_domains"
>title="Domínios de email"
>abstract="Widget de domínios de email"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link"
>title="Rótulos de link rastreado"
>abstract="Widget dos rótulos do link de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link_urls"
>title="URLs de link rastreado"
>abstract="Widget de URLs de link rastreado"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_subjects"
>title="Assuntos de email"
>abstract="Widget de assuntos de email"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_bounce_reasons"
>title="Motivos de rejeição"
>abstract="Widget de motivos de rejeição"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_exclude"
>title="Excluir motivos"
>abstract="Excluir widget de motivos"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_error"
>title="Motivos do erro"
>abstract="Widget de motivos de erro"


<!--campaign push-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_sending_statistics"
>title="Estatísticas de envio"
>abstract="Widget de estatísticas de envio"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracking_statistics"
>title="Estatísticas de rastreamento"
>abstract="Widget de estatísticas de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link"
>title="Rótulos de link rastreado"
>abstract="Widget dos rótulos do link de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link_urls"
>title="URLs de link rastreado"
>abstract="Widget de URLs de link rastreado"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_bounce_reasons"
>title="Motivos de rejeição"
>abstract="Widget de motivos de rejeição"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_exclude"
>title="Motivos excluídos"
>abstract="Widget de motivos excluídos"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_email_error"
>title="Motivos do erro"
>abstract="Widget de motivos de erro"

<!--campaign inapp-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_impression"
>title="Tendência de impressão e clique"
>abstract="Widget de tendência de impressão e clique"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_clicks"
>title="Cliques"
>abstract="Widget de Cliques"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_displays"
>title="Exibições"
>abstract="Widget de exibições"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracking_data"
>title="Dados de rastreamento"
>abstract="Widget de dados de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link"
>title="Rótulos de link rastreado"
>abstract="Widget de rótulos de links rastreados"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link_urls"
>title="URLs de link rastreado"
>abstract="Widget de URLs de link rastreado"

<!--campaign sms-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivered_click"
>title="Tendência de cliques e entregas"
>abstract="Widget de tendência de clique e entrega"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivery_status"
>title="Status da entrega"
>abstract="Widget de status de entrega"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link"
>title="Rótulos de link rastreado"
>abstract="Widget dos rótulos do link de rastreamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link_urls"
>title="URLs de link rastreado"
>abstract="Widget de URLs de link rastreado"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_inbound"
>title="Mensagem de entrada de SMS"
>abstract="Widget de mensagem de entrada de SMS"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_message_type"
>title="Tipo de mensagem SMS"
>abstract="Widget de tipo de mensagem SMS"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_providers"
>title="Provedores de SMS"
>abstract="Widget de provedores de SMS"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_bounce"
>title="Motivos de rejeição"
>abstract="Widget de motivos de rejeição"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_exclude"
>title="Excluir motivos"
>abstract="Excluir widget de motivos"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_error"
>title="Motivos do erro"
>abstract="Widget de motivos de erro"
