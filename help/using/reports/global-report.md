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
source-git-commit: 7c7faa5e672d5ed6d7a083db50b206d11ecc4184
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 5%

---

# Introdução ao Relatório global {#global-report}

>[!NOTE]
>
> Se consultas personalizadas forem realizadas por meio de APIs ao usar o serviço Query, espere algum atraso para seus relatórios.

Use o **[!UICONTROL Relatório global]** para medir o impacto das jornadas e dos deliveries em um período selecionado.

* Se desejar direcionar uma jornada ou deliveries no contexto de uma jornada, da **[!UICONTROL Jornada]** acesse a jornada e clique no menu **[!UICONTROL Exibir relatório]** botão. Em seguida, você pode encontrar os relatórios globais Jornada, Email, SMS e Push .

   ![](assets/report_journey.png)

* Se você deseja direcionar uma campanha, da **[!UICONTROL Campanhas]** acesse sua campanha e clique no menu **[!UICONTROL Relatórios]** botão.

   ![](assets/report_campaign.png)

* Se você quiser mudar do **[!UICONTROL Relatório ao vivo]** para **[!UICONTROL Relatório global]** para o delivery, clique em **[!UICONTROL Todo o tempo]** no alternador de guias.

   ![](assets/report_5.png)

Para obter uma lista detalhada de todas as métricas disponíveis no Adobe Journey Optimizer, consulte [esta página](#list-of-components-global)

## Personalizar painel {#modify-dashboard}

Cada painel de relatórios pode ser modificado alterando o período de tempo e redimensionando ou removendo widgets. Alterar os widgets só afeta o painel do usuário atual. Outros usuários verão seus próprios painéis ou os definidos por padrão.

1. Em seu relatório Global , selecione uma hora de início e fim para direcionar dados específicos.

   ![](assets/report_modify_1.png)

1. Escolha se deseja excluir eventos de teste de seus relatórios com a barra de alternância. Para obter mais informações sobre eventos de teste, consulte [esta página](../building-journeys/testing-the-journey.md).

   Observe que a variável **[!UICONTROL Excluir eventos de teste]** só está disponível para relatórios de Jornada.

   ![](assets/report_modify_2.png)

1. Clique em **[!UICONTROL Modificar]** para começar a personalizar seu painel.

   ![](assets/report_modify_3.png)

1. Ajuste o tamanho dos widgets arrastando o canto inferior direito.

   ![](assets/report_modify_4.png)

1. Clique em **[!UICONTROL Remover]** para remover qualquer widget que você não precise.

   ![](assets/report_modify_5.png)

1. Quando estiver satisfeito com a ordem de exibição e o tamanho dos widgets, clique em **[!UICONTROL Salvar]**.

Seu painel agora é salvo. Suas diferentes alterações serão reaplicadas para um uso posterior dos seus relatórios ao vivo. Se necessário, use a **[!UICONTROL Redefinir]** para restaurar a ordem dos widgets e widgets padrão.

## Lista de componentes {#list-of-components-global}

As tabelas abaixo fornecem a lista de métricas usadas nos relatórios e suas definições, dependendo do tipo de delivery.

### Jornada métricas {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Ações executadas com êxito<br/> </td> 
   <td> Número total de ações executadas com êxito para uma jornada.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfis inseridos<br/> </td> 
   <td> Número total de indivíduos que chegaram ao evento de entrada da jornada.<br/> </td> 
</tr>
  <tr> 
   <td> Erro em ação<br/> </td> 
   <td>Número total de erros que ocorreram para Ações.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfis exportados<br/> </td> 
   <td> Número total de indivíduos que saíram da jornada.<br/> </td> 
</tr> 
  <tr> 
   <td> Falha na jornada individual<br/> </td> 
   <td> Número total de jornadas individuais que não foram executadas com êxito.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Métricas de email e SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Rejeições<br/> </td> 
   <td> Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de rejeição <br/> </td> 
   <td> Porcentagem de emails que retornaram em comparação aos emails enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Cliques<br/> </td> 
   <td> Número de vezes que um conteúdo foi clicado em um email.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregues <br/> </td> 
   <td> Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.<br/></td> 
</tr> 
  <tr> 
   <td> Taxa de entrega<br/> </td> 
   <td> Porcentagem de mensagens enviadas com êxito.<br/> </td> 
</tr>
  <tr> 
   <td> Erros<br/> </td> 
   <td> Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de erro<br/> </td> 
   <td> Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação aos emails enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Excluído<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Rejeição permanente<br/> </td> 
   <td> O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Unknown user.<br/> </td>
</tr>
  <tr> 
   <td> Ignorado<br/> </td> 
   <td> O número total de temporários, como Ausência temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Taxa de cliques da oferta<br/> </td> 
   <td>Porcentagem de usuários que interagiram com a oferta.<br/> </td> 
</tr>
   <tr> 
   <td>Taxa de impressões da oferta<br/> </td> 
   <td>Porcentagem de ofertas abertas em comparação ao número de ofertas enviadas.<br/> </td> 
</tr>
   <tr> 
   <td>Nome da oferta<br/> </td> 
   <td> Nome da oferta adicionada ao delivery. Para obter mais informações sobre posicionamento, consulte esta seção <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Oferta enviada<br/> </td> 
   <td>Número total de envios para a oferta.<br/> </td> 
</tr> 
  <tr>
   <td>Aberturas<br/> </td> 
   <td> Número de vezes que a mensagem foi aberta.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de abertura<br/> </td> 
   <td> Número total de emails abertos em comparação ao número de emails entregues.<br/> </td> 
</tr>
  <tr> 
   <td>Nome da disposição<br/> </td> 
   <td> Nome da disposição usada para exibir sua oferta. Para obter mais informações sobre posicionamento, consulte esta seção <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
</tr> 
  <tr> 
   <td> Tentativas<br/> </td> 
   <td> Número de emails na fila para novas tentativas.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envios para o delivery.<br/> </td> 
</tr>
  <tr> 
   <td> Rejeição suave<br/> </td> 
   <td> Número total de erros temporários, como uma caixa de entrada completa.<br/> </td> 
</tr>
  <tr> 
   <td> Reclamações de spam<br/> </td> 
   <td> Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.<br/> </td> 
</tr>
  <tr> 
   <td> Direcionado<br/> </td> 
   <td> Número total de mensagens processadas durante a análise de delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Cliques únicos<br/> </td> 
   <td> Número de recipients que clicaram em um conteúdo em um email.<br/> </td> 
</tr> 
  <tr> 
   <td>Taxa de cliques exclusiva<br/> </td> 
   <td> Porcentagem de usuários que interagiram com o delivery.<br/> </td> 
</tr>
  <tr> 
   <td> Aberturas únicas<br/> </td> 
   <td>Número de recipients que abriram o delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Cancelamentos de assinatura<br/> </td> 
   <td> Número de cliques no link unsubscription.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
### Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

### Métricas de notificação por push

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Ações<br/> </td> 
   <td> Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.<br/> </td> 
</tr>
  <tr> 
   <td>Rejeições<br/> </td> 
   <td> Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de rejeição <br/> </td> 
   <td> Porcentagem de notificações por push que rejeição em comparação às notificações por push enviadas.<br/> </td>
</tr>
  <tr> 
   <td> Entregues<br/> </td> 
   <td> Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de delivery<br/> </td> 
   <td> Porcentagem de notificações por push enviadas com êxito.<br/> </td> 
</tr>
  <tr> 
   <td>Envolvimentos<br/> </td> 
   <td> Número total de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de participação<br/> </td> 
   <td> Porcentagem de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr>
  <tr> 
   <td> Erros<br/> </td> 
   <td> Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.<br/> </td> 
</tr>
  <tr> 
   <td> Taxa de erro<br/> </td> 
   <td> Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação ao envio de notificações por push.<br/> </td> 
</tr> 
  <tr> 
   <td> Excluído<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Aberturas<br/> </td> 
   <td> Número total de notificações por push enviadas ao dispositivo e clicadas pelos usuários, abrindo o aplicativo. Isso é semelhante ao Clique de push, exceto que a opção Abrir por push não será acionada se a notificação for descartada.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de abertura<br/> </td> 
   <td> Porcentagem de notificações por push abertas.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envios para o delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Direcionado<br/> </td> 
   <td> Número total de mensagens de push processadas durante a análise de delivery.<br/> </td> 
</tr>  
 </tbody> 
</table>

### Métricas de página de aterrissagem {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Rejeições<br/> </td> 
   <td>Número de pessoas que não interagiram com a landing page e não concluíram a ação de assinatura.<br/> </td> 
</tr>
 <tr> 
   <td>Taxa de rejeição<br/> </td> 
   <td>Número de pessoas que não interagiram com a landing page e não concluíram a ação de assinatura em relação ao número total de visitas.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Cliques<br/> </td> 
   <td>Número de vezes que um conteúdo foi clicado na página de aterrissagem.<br/> </td> 
</tr>
 <tr> 
   <td>Taxa de cliques<br/> </td> 
   <td>Porcentagem de cliques na página de aterrissagem.<br/> </td>
</tr>
<tr>
<td>Conversão<br/> </td> 
   <td>Número de pessoas que interagiram com a landing page, por exemplo, assinaram um formulário.<br/> </td> 
</tr>
<tr>
   <td>Índice de conversão<br/> </td> 
   <td>Número de pessoas que interagiram com a landing page, por exemplo, assinaram um formulário em relação ao número total de visitas.<br/> </td> 
</tr>
 <tr> 
   <td>Jornada(s)<br/> </td> 
   <td>Número de visitas à sua página de aterrissagem provenientes de uma jornada.<br/> </td> 
</tr>
 <tr> 
   <td>Outras fontes<br/> </td> 
   <td>Número de visitas à sua página inicial provenientes de uma fonte externa em vez de uma jornada.<br/> </td> 
</tr>
 <tr> 
   <td>Total de visitas<br/> </td> 
   <td> Número total de visitas à sua página inicial provenientes de jornadas e fontes externas, incluindo várias visitas de um recipient.<br/> </td> 
</tr>
 <tr> 
   <td>Visitantes únicos<br/> </td> 
   <td>Número de pessoas que visitaram sua landing page, várias visitas de um recipient não são consideradas.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas<br/> </td> 
   <td>Número de visitas à sua página inicial, incluindo várias visitas de um recipient.<br/> </td> 
</tr>
 </tbody> 
</table>

### Métricas de notificação por push

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Ações<br/> </td> 
   <td> Número total de ações na notificação por push entregue, por exemplo, clique no botão ou descarta.<br/> </td> 
</tr>
  <tr> 
   <td>Rejeições<br/> </td> 
   <td> Total de erros acumulados durante o delivery e o processamento automático de retorno em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de rejeição <br/> </td> 
   <td> Porcentagem de notificações por push que rejeição em comparação às notificações por push enviadas.<br/> </td>
</tr>
  <tr> 
   <td> Entregues<br/> </td> 
   <td> Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de delivery<br/> </td> 
   <td> Porcentagem de notificações por push enviadas com êxito.<br/> </td> 
</tr>
  <tr> 
   <td>Envolvimentos<br/> </td> 
   <td> Número total de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de participação<br/> </td> 
   <td> Porcentagem de aberturas e ações para essa notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr>
  <tr> 
   <td> Erros<br/> </td> 
   <td> Número total de erros que ocorreram durante um delivery, impedindo que ele fosse enviado a perfis.<br/> </td> 
</tr>
  <tr> 
   <td> Taxa de erro<br/> </td> 
   <td> Porcentagem de erros que ocorreram durante um delivery e impediram seu envio em comparação ao envio de notificações por push.<br/> </td> 
</tr> 
  <tr> 
   <td> Excluído<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Aberturas<br/> </td> 
   <td> Número total de notificações por push enviadas ao dispositivo e clicadas pelos usuários, abrindo o aplicativo. Isso é semelhante ao Clique de push, exceto que a opção Abrir por push não será acionada se a notificação for descartada.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de abertura<br/> </td> 
   <td> Porcentagem de notificações por push abertas.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envios para o delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Direcionado<br/> </td> 
   <td> Número total de mensagens de push processadas durante a análise de delivery.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
### In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
</tr> 
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
