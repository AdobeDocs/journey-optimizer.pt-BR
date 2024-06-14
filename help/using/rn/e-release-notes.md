---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
source-git-commit: 50b0a2eb8794c79d10f09dd12fd6f996402d72ea
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 27%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de junho de 2024 {#e-2024}

**Data de lançamento**: 18 a 19 de junho de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Fluxo de trabalho de Warmup de IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se você estiver enviando emails em um novo endereço IP, agora é possível executar facilmente workflows de aquecimento de IP diretamente da interface do usuário. O Adobe Journey Optimizer oferece uma maneira padronizada e eficiente de aquecer seus endereços IP que segue as práticas recomendadas para uma entrega ideal.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Assistente de IA no Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA é um recurso da interface do usuário que você pode usar para navegar e entender conceitos de Adobe e obter insights operacionais para seu ambiente específico. Ele está disponível em vários produtos na Adobe Experience Cloud, incluindo o Adobe Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-assistant.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
</td>
</tr>
</tbody>
</table-->



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


**Gestão de decisões**

* **Suporte a várias regras na Gestão de decisões** - Agora você pode adicionar até 10 regras de limitação para uma determinada oferta na Gestão de decisões. Isso permite aumentar o nível de controle sobre como as ofertas são enviadas. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**Jornadas**

* O tempo limite global do jornada foi aumentado de 30 para 91 dias.
* O Adobe Journey Optimizer agora é compatível com solicitações de exclusão/acesso de privacidade, bem como com solicitações de gerenciamento do ciclo de vida dos dados.
* Agora é possível redimensionar as colunas no inventário de jornadas.
* **Editor de expressão avançado na configuração do Evento** Agora é GA - Agora você pode aproveitar o editor de expressão avançado ao configurar um evento, permitindo definir expressões mais complexas ou usar funções na condição de id de evento. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. <!--[Read more](../event/about-creating.md)-->
* **Políticas de mesclagem** Agora estão disponíveis no mercado - As políticas de mesclagem usadas por uma Jornada agora estão visíveis e consistentes em toda a jornada. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**Campanhas**

* Ao criar uma campanha no Adobe Journey Optimizer, agora é possível escolher o tipo de campanha (agendada ou acionada) em um novo modal.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canal SMS**

* Agora é possível adicionar códigos curtos exclusivos para cada sandbox com uma única configuração de API, tornando o processo mais eficiente e simplificado.
  <!--* You can now modify existing SMS configurations.-->

**Canal no aplicativo**

* **Fragmento da expressão** - Os fragmentos de expressão agora estão disponíveis para o **Canal no aplicativo**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* Agora você pode usar o plug-in Edge Delivery para obter as informações necessárias para entender e solucionar problemas de suas implementações de entrada.


