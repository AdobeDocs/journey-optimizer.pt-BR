---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Saiba como usar dados do relatório global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: c487bb38-49ce-4238-8e94-8364f994cedd
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 4%

---

# Lista de componentes {#list-of-components-global}

>[!AVAILABILITY]
>
>A experiência atual de relatórios será removida a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição tranquila. [Introdução à nova interface de Relatórios do Journey Optimizer.](report-gs-cja.md)

As tabelas abaixo fornecem a lista de métricas usadas em relatórios e suas definições, dependendo do tipo de delivery.

## Jornada métricas {#journey-metrics}

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
   <td> Número total de Ações executadas com êxito para uma jornada.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfis inseridos<br/> </td> 
   <td> Número total de indivíduos que atingiram o evento de entrada da jornada.<br/> </td> 
</tr>
  <tr> 
   <td> Erro na ação<br/> </td> 
   <td>Número total de erros que ocorreram para Ações.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfis encerrados<br/> </td> 
   <td> Número total de indivíduos que saíram da jornada.<br/> </td> 
</tr> 
  <tr> 
   <td> Falha na jornada individual<br/> </td> 
   <td> Número total de jornadas individuais que não foram executadas com êxito.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Dimensões e métricas de email e SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Devoluções<br/> </td> 
   <td> Total de erros acumulados durante o processo de envio e o processamento de retorno automático em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de rejeição<br/> </td> 
   <td> Porcentagem de emails que foram rejeitados em comparação aos emails enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Cliques<br/> </td> 
   <td> Número de vezes que um conteúdo foi clicado em um email.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregue <br/> </td> 
   <td> Número de mensagens enviadas com êxito em relação ao número total de mensagens enviadas.<br/></td> 
</tr> 
  <tr> 
   <td> Taxa de Entrega<br/> </td> 
   <td> Porcentagem de mensagens enviadas com êxito.<br/> </td> 
</tr>
  <tr> 
   <td> Erros<br/> </td> 
   <td> Número total de erros ocorridos durante o processo de envio que impediram o envio para perfis.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de Erro<br/> </td> 
   <td> Porcentagem de erros ocorridos durante o processo de envio que impediram seu envio em comparação aos emails enviados.<br/> </td> 
</tr>
</tr> 
  <tr> 
   <td> Motivo do Erro<br/> </td> 
   <td> Nome da causa original específica do erro. <a href="exclusion-list.md">Saiba mais sobre os motivos de erro</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Excluído<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Rejeição permanente<br/> </td> 
   <td> O número total de erros permanentes, como um endereço de email incorreto. Isso envolve uma mensagem de erro que declara explicitamente que o endereço é inválido, como Usuário desconhecido.<br/> </td>
</tr>
  <tr> 
   <td> Ignorado<br/> </td> 
   <td> O número total de mensagens temporárias, como Ausência Temporária, ou um erro técnico, por exemplo, se o tipo de remetente for postmaster.<br/> </td> 
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
   <td> Nome da oferta adicionada na entrega. Para obter mais informações sobre posicionamento, consulte esta <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
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
   <td> Taxa de Abertura<br/> </td> 
   <td> Número total de emails abertos em comparação ao número de emails entregues.<br/> </td> 
</tr>
  <tr> 
   <td>Nome do posicionamento<br/> </td> 
   <td> Nome do posicionamento usado para exibir a oferta. Para obter mais informações sobre posicionamento, consulte esta <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
</tr> 
  <tr> 
   <td> Tentativas<br/> </td> 
   <td> Número de emails na fila para tentativas.<br/> </td> 
</tr> 
  <tr> 
   <td> Sent<br/> </td> 
   <td> Número total de envios para a entrega.<br/> </td> 
</tr>
  <tr> 
   <td> Rejeição leve<br/> </td> 
   <td> Número total de erros temporários, como uma caixa de entrada cheia.<br/> </td> 
</tr>
  <tr> 
   <td> Reclamações de spam<br/> </td> 
   <td> Número de vezes que uma mensagem foi declarada como spam ou lixo eletrônico.<br/> </td> 
</tr>
  <tr> 
   <td> Direcionado<br/> </td> 
   <td> Número total de mensagens processadas durante a análise de entrega.<br/> </td> 
</tr> 
  <tr> 
   <td> Cliques únicos<br/> </td> 
   <td> Número de recipients que clicaram em um conteúdo em um email.<br> Observe que ao calcular cliques únicos, os últimos 10 dias são considerados. Se um perfil registrar vários cliques no período de 10 dias, eles serão contados como cliques únicos. No entanto, se um perfil tiver 2 cliques com mais de 10 dias de intervalo, eles não serão considerados cliques exclusivos.<br/> </td> 
</tr> 
  <tr> 
   <td>Taxa de cliques únicos<br/> </td> 
   <td> Porcentagem de usuários que interagiram com a entrega.<br/> </td> 
</tr>
  <tr> 
   <td> Aberturas únicas<br/> </td> 
   <td>Número de destinatários que abriram o delivery. <br> Observe que ao calcular aberturas únicas, os últimos 10 dias são considerados. Se um perfil registrar várias aberturas no período de 10 dias, elas serão contadas como aberturas exclusivas. No entanto, se um perfil tiver duas aberturas com mais de 10 dias de intervalo, elas não serão consideradas aberturas exclusivas.<br/> </td> 
</tr> 
  <tr> 
   <td> Cancelamentos de assinatura<br/> </td> 
   <td> Número de cliques no link de cancelamento de assinatura.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
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
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../content-management/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../content-management/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../content-management/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
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
   <td>Number of recipients who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of recipients who clicked on the unsubscription link.<br/> </td>
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

## Métricas no aplicativo {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Cliques<br/> </td> 
   <td>Número total de destinatários que interagiram com os botões incluídos na mensagem no aplicativo.<br/> </td> 
</tr>
  <tr> 
   <td>Taxa de cliques<br/> </td> 
   <td>Porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que viram a mensagem.<br/> </td> 
</tr> 
  <tr> 
   <td>Taxa de descarte<br/> </td> 
   <td> Porcentagem de mensagens no aplicativo que os destinatários rejeitaram.<br/> </td> 
</tr> 
  <tr> 
   <td>Impressões<br/> </td> 
   <td> Número total de mensagens no aplicativo entregues a todos os usuários.<br/> </td>
</tr>
  <tr> 
   <td>Impressões exclusivas<br/> </td> 
   <td>Número de usuários exclusivos para os quais a mensagem no aplicativo foi entregue.<br/> </td>
</tr>
 </tbody> 
</table>

## Métricas de notificação por push

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
   <td> Número total de ações na notificação por push entregue, por exemplo, clique ou descarte de botões.<br/> </td> 
</tr>
  <tr> 
   <td>Devoluções<br/> </td> 
   <td> Total de erros acumulados durante o processamento de entrega e retorno automático em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de rejeição<br/> </td> 
   <td> Porcentagem de notificações por push que foram rejeitadas em comparação às notificações por push enviadas.<br/> </td>
</tr>
  <tr> 
   <td> Entregue<br/> </td> 
   <td> Número de mensagens enviadas com êxito, em relação ao número total de mensagens enviadas.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de entrega<br/> </td> 
   <td> Porcentagem de notificações por push enviadas com êxito.<br/> </td> 
</tr>
  <tr> 
   <td>Compromissos<br/> </td> 
   <td> Número total de aberturas e ações para esta notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de Participação<br/> </td> 
   <td> Porcentagem de aberturas e ações para esta notificação por push, ou seja, se o perfil abriu o push ou se um botão foi clicado.<br/> </td> 
</tr>
  <tr> 
   <td> Erros<br/> </td> 
   <td> Número total de erros que ocorreram durante uma entrega, impedindo que ela fosse enviada aos perfis.<br/> </td> 
</tr>
  <tr> 
   <td> Taxa de Erro<br/> </td> 
   <td> Porcentagem de erros ocorridos durante uma entrega que impedem seu envio em comparação às notificações por push enviadas.<br/> </td> 
</tr>
  <tr> 
   <td> Motivo do Erro<br/> </td> 
   <td> Nome da causa original específica do erro. <a href="exclusion-list.md">Saiba mais sobre os motivos de erro</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Excluído<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Aberturas<br/> </td> 
   <td> Número total de notificações por push entregues ao dispositivo e clicadas pelos usuários, abrindo o aplicativo. Isso é semelhante ao Clique por Push, exceto que uma Abertura por Push não será acionada se a notificação for descartada.<br/> </td> 
</tr> 
  <tr> 
   <td> Taxa de aberturas<br/> </td> 
   <td> Porcentagem de notificações por push abertas.<br/> </td> 
</tr> 
  <tr> 
   <td> Sent<br/> </td> 
   <td> Número total de envios para a entrega.<br/> </td> 
</tr> 
  <tr> 
   <td> Direcionado<br/> </td> 
   <td> Número total de mensagens de push processadas durante a análise de entrega.<br/> </td> 
</tr>  
 </tbody> 
</table>

## Métricas de landing page {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Devoluções<br/> </td> 
   <td>Número de pessoas que não interagiram com a página de aterrissagem e não concluíram a ação de assinatura.<br/> </td> 
</tr>
 <tr> 
   <td>Taxa de rejeição<br/> </td> 
   <td>Número de pessoas que não interagiram com a página de aterrissagem e não concluíram a ação de assinatura em relação ao número total de visitas.<br/> </td> 
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
   <td>Número de pessoas que interagiram com a página de aterrissagem, por exemplo, inscritas em um formulário.<br/> </td> 
</tr>
<tr>
   <td>Taxa de conversão<br/> </td> 
   <td>Número de pessoas que interagiram com a página de aterrissagem, por exemplo, inscritas em um formulário, em relação ao número total de visitas.<br/> </td> 
</tr>
 <tr> 
   <td>Jornada(s)<br/> </td> 
   <td>Número de visitas à sua página de aterrissagem vindas de uma jornada.<br/> </td> 
</tr>
 <tr> 
   <td>Outras fontes<br/> </td> 
   <td>Número de visitas à sua página de aterrissagem vindas de uma fonte externa em vez de uma jornada.<br/> </td> 
</tr>
 <tr> 
   <td>Total de visitas<br/> </td> 
   <td> Número total de visitas à sua página de aterrissagem provenientes de jornadas e fontes externas, incluindo várias visitas de um destinatário.<br/> </td> 
</tr>
 <tr> 
   <td>Visitantes únicos<br/> </td> 
   <td>Número de pessoas que visitaram sua página de aterrissagem; várias visitas de um destinatário não são consideradas.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas<br/> </td> 
   <td>Número de visitas à página de aterrissagem, incluindo várias visitas de um destinatário.<br/> </td> 
</tr>
 </tbody> 
</table>
