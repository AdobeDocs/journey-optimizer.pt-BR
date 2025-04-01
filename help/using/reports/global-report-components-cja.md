---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Saiba como usar os dados do seu relatório
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: 3de7826ae4a7efc2837288779fb444fa15688d3f
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 2%

---

# Lista de componentes {#list-of-components-global}

As tabelas abaixo fornecem a lista de métricas usadas em relatórios e suas definições, dependendo do tipo de delivery.

## Métricas de jornada {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definição<br/> </th> 
</tr>
 </thead> 
 <tbody> 
<tr> 
<td>Jornada envolvimento</td> 
<td>Número total de indivíduos únicos que receberam mensagens enviadas por meio da jornada, representando perfis distintos que atingiram um ponto de ação designado na jornada.</td> 
</tr> 
<tr> 
<td>Entradas de jornada</td> 
<td>Número total de indivíduos que atingiram o evento de entrada da jornada.</td> 
</tr>
<tr> 
<td>Jornada saídas</td> 
<td>Número total de indivíduos que saíram da jornada.</td> 
</tr>
<tr> 
<td>Falhas de jornada</td> 
<td>Número total de jornadas individuais que não foram executadas com êxito.</td> 
</tr>
<tr> 
<td>Entradas de Jornada únicas</td> 
<td>Número total de indivíduos que atingiram o evento de entrada da jornada, com várias interações do mesmo perfil não consideradas.</td> 
</tr>
<tr> 
<td>Saídas de Jornada únicas</td> 
<td>Número total de indivíduos que saíram da jornada, com várias interações do mesmo perfil não consideradas.</td> 
</tr>
<tr> 
<td>Falhas de Jornada únicas</td> 
<td>Número total de jornadas individuais que não foram executadas com êxito, com várias interações do mesmo perfil não consideradas.</td> 
</tr>
 </tbody> 
</table>

## Métricas de email {#email-metrics}

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
   <td> Taxa de abertura de cliques (CTOR)<br/> </td> 
   <td> Número de vezes que o email foi aberto.<br/> </td> 
  </tr>
  <tr> 
   <td> Taxa de cliques (CTR)<br/> </td> 
   <td> Porcentagem de usuários que interagiram com o email.<br/> </td> 
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
   <td> Motivo do Erro<br/> </td> 
   <td> Nome da causa original específica do erro. <a href="exclusion-list.md">Saiba mais sobre os motivos de erro</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Taxa de cliques da oferta<br/> </td> 
   <td> Porcentagem de usuários que interagiram com a oferta.<br/> </td> 
  </tr>
  <tr> 
   <td> Taxa de impressões da oferta<br/> </td> 
   <td> Porcentagem de ofertas abertas em comparação ao número de ofertas enviadas.<br/> </td> 
  </tr>
  <tr> 
   <td> Nome da oferta<br/> </td> 
   <td> Nome da oferta adicionada na entrega. Para obter mais informações sobre posicionamento, consulte esta <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Oferta enviada<br/> </td> 
   <td> Número total de envios para a oferta.<br/> </td> 
  </tr> 
  <tr> 
   <td> Aberturas<br/> </td> 
   <td> Número de vezes que a mensagem foi aberta.<br/> </td> 
  </tr> 
  <tr> 
   <td> Erros de Saída<br/> </td> 
   <td> Número total de erros ocorridos durante o processo de envio que impediram o envio para perfis.<br/> </td> 
  </tr> 
  <tr> 
   <td> Exclusões de saída<br/> </td> 
   <td> Número de perfis que foram excluídos pelo Adobe Journey Optimizer.<br/> </td> 
  </tr>
  <tr> 
   <td> Nome do posicionamento<br/> </td> 
   <td> Nome do posicionamento usado para exibir a oferta. Para obter mais informações sobre posicionamento, consulte esta <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
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
   <td> Número de perfis que clicaram em um conteúdo em um email.<br> Observe que ao calcular cliques únicos, os últimos 10 dias são considerados. Se um perfil registrar vários cliques no período de 10 dias, eles serão contados como cliques únicos. No entanto, se um perfil tiver 2 cliques com mais de 10 dias de intervalo, eles não serão considerados cliques exclusivos.<br/> </td> 
  </tr>
  <tr> 
   <td> Cancelamentos de Assinatura de Email Exclusivos<br/> </td> 
   <td> Número de perfis que cancelaram a assinatura de seus emails.<br/> </td> 
  </tr>
  <tr> 
   <td> Aberturas únicas<br/> </td> 
   <td> Número de perfis que abriram o delivery. <br> Observe que ao calcular aberturas únicas, os últimos 10 dias são considerados. Se um perfil registrar várias aberturas no período de 10 dias, elas serão contadas como aberturas exclusivas. No entanto, se um perfil tiver duas aberturas com mais de 10 dias de intervalo, elas não serão consideradas aberturas exclusivas.<br/> </td> 
  </tr> 
  <tr> 
   <td> Cancelamentos de assinatura<br/> </td> 
   <td> Número de cliques no link de cancelamento de assinatura.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## Métricas de SMS

<table> 
  <thead> 
    <tr> 
      <th> Métrica de SMS </th> 
      <th> Definição </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>Entregues</td> 
      <td>Número de mensagens SMS enviadas com êxito, em relação ao número total de mensagens SMS.</td> 
    </tr>
    <tr> 
      <td>Cliques</td> 
      <td>Número de vezes que um link em uma mensagem SMS foi clicado.</td> 
    </tr>
    <tr> 
      <td>Rejeições para mensagens SMS de saída</td> 
      <td>Número total de erros acumulados durante o processo de envio e o processamento automático de retorno em relação ao número total de mensagens SMS enviadas.</td> 
    </tr>
    <tr> 
      <td>Erros de SMS de saída</td> 
      <td>Número total de erros que ocorreram, impedindo que a mensagem SMS fosse enviada aos recipients.</td> 
    </tr>
    <tr> 
      <td>Exclusões de SMS de saída</td> 
      <td>Número de perfis excluídos do recebimento de mensagens SMS pelo Adobe Journey Optimizer.</td> 
    </tr>
    <tr> 
      <td>Cliques únicos</td> 
      <td>Número de recipients únicos que clicaram em um link em uma mensagem SMS.</td> 
    </tr>
    <tr> 
      <td>Exibições</td> 
      <td>Número de vezes que uma mensagem SMS foi exibida ou aberta.</td> 
    </tr>
    <tr> 
      <td>Exibições únicas</td> 
      <td>Número de recipients únicos que abriram a mensagem SMS, excluindo várias interações do mesmo usuário.</td> 
    </tr>
    <tr> 
      <td>People</td> 
      <td>Número de perfis de usuário exclusivos que receberam ou interagiram com uma mensagem SMS.</td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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
   <td>Número total de perfis que interagiram com os botões incluídos na mensagem no aplicativo.<br/> </td> 
  </tr>
  <tr> 
   <td>Taxa de cliques<br/> </td> 
   <td>Porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que viram a mensagem.<br/> </td> 
  </tr>
  <tr> 
   <td>Taxa de descarte<br/> </td> 
   <td>Porcentagem de mensagens no aplicativo que os perfis rejeitaram.<br/> </td> 
  </tr>
  <tr> 
   <td>Impressões<br/> </td> 
   <td>Número total de mensagens no aplicativo entregues a todos os usuários.<br/> </td>
  </tr>
  <tr> 
   <td>Impressões exclusivas<br/> </td> 
   <td>Número de usuários exclusivos para os quais a mensagem no aplicativo foi entregue.<br/> </td>
  </tr>
  <tr> 
   <td>Exibições<br/> </td>
   <td>Número de vezes que a mensagem no aplicativo foi aberta.<br/> </td>
  </tr>
  <tr> 
   <td>Exibições únicas<br/> </td>
   <td>Número de vezes que a mensagem no aplicativo foi aberta, excluindo várias interações do mesmo perfil.<br/> </td>
  </tr>
  <tr> 
   <td>Cliques únicos<br/> </td>
   <td>Número de perfis que clicaram no conteúdo em suas mensagens no aplicativo.<br/> </td>
  </tr>
  <tr> 
   <td>Cliques<br/> </td>
   <td>Número de vezes que clicou no conteúdo em suas mensagens no aplicativo.<br/> </td>
  </tr>
  <tr> 
   <td>Taxa de cliques (CTR)<br/> </td>
   <td>Porcentagem de usuários que interagiram com as mensagens no aplicativo.<br/> </td>
  </tr>
  <tr> 
   <td>Taxa de abertura de cliques (CTOR)<br/> </td>
   <td>Número de vezes que a mensagem no aplicativo foi aberta.<br/> </td>
  </tr>
  <tr> 
   <td>Envios<br/> </td>
   <td>Número total de mensagens no aplicativo enviadas.<br/> </td>
  </tr>
  <tr> 
   <td>Entrada disparada<br/> </td>
   <td>Número de vezes que uma mensagem no aplicativo foi disparada por uma interação do usuário ou evento predefinido.<br/> </td>
  </tr>
  <tr> 
   <td>Descartes de entrada<br/> </td>
   <td>Número de vezes que os usuários rejeitaram a mensagem no aplicativo sem interagir com ela.<br/> </td>
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
   <td> Enviar ações personalizadas<br/> </td> 
   <td>Número de ações personalizadas executadas por perfis em resposta às notificações por push.<br/> </td> 
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
   <td> Número total de visitas à sua página de aterrissagem provenientes de jornadas e fontes externas, incluindo várias visitas de um perfil.<br/> </td> 
</tr>
 <tr> 
   <td>Visitantes únicos<br/> </td> 
   <td>Número de pessoas que visitaram sua página de aterrissagem; várias visitas de um perfil não são consideradas.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas<br/> </td> 
   <td>Número de visitas à sua página de aterrissagem, incluindo várias visitas de um perfil.<br/> </td> 
</tr>
 </tbody> 
</table>
