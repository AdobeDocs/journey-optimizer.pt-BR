---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 52%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de agosto de 2024 {#e-2024}

**Data de lançamento**: 20-21 de agosto de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Ação personalizada do Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode integrar o Adobe Journey Optimizer com o Adobe Marketo Engage para criar seus casos de uso B2B. Em uma jornada, uma nova ação personalizada permite assimilar dados no Marketo.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configurações de canal aprimoradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos atuais da superfície de canal foram aprimorados para oferecer uma abordagem consistente em todos os canais. Agora você pode definir, gerenciar e reutilizar essas configurações para qualquer um dos seus canais.</p>
<p><ul>
<li>Superfícies de canal agora são renomeadas para <strong>Configurações de canal</strong></li>
<li>No inventário Configurações de canal, agora é possível criar configurações de canal reutilizáveis para todos os canais, incluindo agora Web, Mensagens no aplicativo ou Experiência baseada em código</li>
<li>O OLAC (Object Level Access Control) agora está disponível para cada configuração de canal, permitindo que você decida quais dos seus usuários têm permissão para criar ou usar configurações específicas</li>
<li>Para alguns canais, você pode criar configurações de canal que direcionem várias plataformas. Um exemplo seria uma configuração de canal de mensagens no aplicativo que pode direcionar uma página da Web, um aplicativo do iOS e um aplicativo do Android.</li>
</ul></p>
<p>Para obter mais informações, consulte a <a href="../configuration/ip-warmup-gs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Jornadas**

* Na atividade **Condição**, por padrão, a condição Tempo agora é definida por hora, das 00:00 às 12:00. [Leia mais](../building-journeys/condition-activity.md#time_condition)

**Públicos-alvo**

* O uso de públicos-alvo a partir de uploads personalizados (arquivo CSV) agora está disponível para uso com o Privacy and Security Shield.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
