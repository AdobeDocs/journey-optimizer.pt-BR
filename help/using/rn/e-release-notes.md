---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: ae9a315f6c9d2c2408788a7e4b32cdbd516f41d6
workflow-type: ht
source-wordcount: '656'
ht-degree: 100%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de maio de 2024 {#e-2024}

**Data de lançamento**: 21 a 22 de maio de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.


<table>
<thead>
<tr>
<th><strong>Escolha de experiências - Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Escolha de experiências simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.</p>
<p>Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer. As políticas de decisão da Escolha de experiências estão disponíveis para uso somente em campanhas de experiência baseadas em código.</p>
<p>No momento, a Escolha de experiências está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/gs-experience-decisioning.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
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

**Escolha de experiências** (disponibilidade limitada)

As seguintes melhorias foram adicionadas desde a versão beta até a versão atual:

* **Escolha de experiências + Experiências baseadas em código**: agora é possível aproveitar o recurso Escolha de experiências para usar itens de decisão em campanhas baseadas em código. Observação: o canal Experiência baseada em código e a Escolha de experiências não estão disponíveis para organizações que compraram as ofertas complementares do Adobe Healthcare Shield e Privacy and Security Shield. [Leia mais](../code-based/get-started-code-based.md)
* **Dados de contexto**: agora é possível aproveitar os dados de contexto da Adobe Experience Platform em suas regras de decisão e nas fórmulas de classificação. [Leia mais](../experience-decisioning/context-data.md)
* **Nova permissão**: a permissão “Gerenciar escolhas de experiência” agora está disponível para o recurso Gestão de decisões. Isso permite gerenciar direitos relacionados à Escolha de experiências. [Leia mais](../experience-decisioning/gs-experience-decisioning.md)
* **Regras de limite**: agora é possível adicionar várias regras de limite para um determinado item de decisão na Escolha de experiências. Isso permite aumentar o nível de controle sobre como as ofertas são enviadas. [Leia mais](../experience-decisioning/items.md#capping)
* **Relatórios**: agora é possível criar painéis de relatórios personalizados para campanhas da Escolha de experiências usando o [!DNL Customer Journey Analytics]. [Leia mais](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canal de email**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Pontuação de spam** (Beta): agora é possível verificar sua pontuação de spam de conteúdo em um relatório dedicado. Com o SpamAssassin, o Adobe Journey Optimizer testa seu conteúdo de email e atribui uma pontuação para indicar se os ISPs ou provedores de caixa de correio o consideram como spam ou não. [Leia mais](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >No momento, esse recurso está na versão beta, disponível apenas para clientes beta. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Jornadas**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Suporte a mTLS**: a autenticação mTLS agora é compatível com ações personalizadas. Não é necessária uma configuração adicional da ação personalizada ou jornada para ativar o mTLS; isso ocorre automaticamente ao detectar um ponto de acesso habilitado para mTLS. [Leia mais](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabelas de pesquisa em eventos**: agora é possível aproveitar os dados de um conjunto de dados de pesquisa após definir uma relação usando um atributo de uma matriz de objetos. Os valores de pesquisa estarão disponíveis em jornadas (condições, ações personalizadas etc.) e na personalização de mensagens. [Leia mais](../event/experience-event-schema.md#relationships_limitations)
* **Editor de expressão avançado na configuração de evento** (disponibilidade limitada): agora é possível utilizar o editor de expressão avançado ao configurar um evento, o que permite definir expressões mais complexas ou usar funções na condição de ID de evento. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. [Leia mais](../event/about-creating.md)
* **Políticas de mesclagem** (disponibilidade limitada): as políticas de mesclagem usadas por uma jornada agora estão visíveis e são consistentes em toda a jornada. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. [Leia mais](../building-journeys/journey-gs.md#merge-policies)

**Globalização**

Como parte do nosso esforço contínuo em fornecer uma experiência de usuário unificada, harmonizamos a terminologia usada nos produtos e aplicativos da Adobe Experience Cloud. Isso afeta o termo alemão “Titel”, que é alterado para “Label” quando se refere ao nome de um objeto. As alterações serão progressivamente implementadas na interface e na documentação.



