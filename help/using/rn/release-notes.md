---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# Notas de versão {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

As notas de versão anteriores estão disponíveis [nesta página](release-notes-2023.md). Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Notas de versão de outubro de 2023 {#oct-rn-2023}

### Novos recursos{#oct-2023-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Ferramentas de sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As ferramentas de sandbox permitem copiar objetos em várias sandboxes aproveitando a exportação e a importação de pacotes. Um pacote pode consistir em um único objeto ou em vários objetos. Todos os objetos incluídos em um pacote precisam ser da mesma sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>Para obter mais informações, consulte a <a href="../building-journeys/copy-to-sandbox.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Serviço de Mensagens Multimídia (MMS) em SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o canal SMS, agora é possível aprimorar a comunicação enviando mensagens do Serviço de Mensagens Multimídia (MMS), o que permite o compartilhamento de imagens, GIFs ou vídeos com clientes. Observe que esse recurso está disponível somente com o Sinch.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Para obter mais informações, consulte a <a href="../sms/create-sms.md#mms-content">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>

### Melhorias {#oct-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* Agora é possível direcionar públicos-alvo enviados a partir de um arquivo CSV para jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)
* Agora é possível direcionar públicos-alvo criados por meio da composição de público-alvo e aproveitar os atributos de enriquecimento em jornadas. [Saiba mais](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>No momento, esses recursos estão disponíveis como um beta privado.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campanhas**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Quando ocorre um erro em uma das campanhas, um ícone de aviso agora é exibido na lista de campanhas junto com o status da campanha. [Saiba mais](../campaigns/modify-stop-campaign.md#statuses)

**Jornadas**

* A duração máxima que você pode definir em qualquer tempo de espera agora é de 29 dias, em vez de 30. Essa melhoria foi introduzida para evitar que a espera exceda os 30 dias de duração da jornada. Isso se aplica a:

   * o campo **Quantidade de tempo** na [atividade de espera](../building-journeys/wait-activity.md)
   * o **período de espera de reentrada** nas [propriedades da jornada](../building-journeys/journey-gs.md#entrance)
   * o campo **Aguardar por** na definição de tempo limite das [atividades de evento](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Gestão de decisões**

* Vários rótulos relacionados ao limite de ofertas na interface da gestão de decisões foram atualizados. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

