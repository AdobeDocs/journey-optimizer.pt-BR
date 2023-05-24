---
solution: Journey Optimizer
product: journey optimizer
title: Níveis de permissão
description: Saiba mais sobre permissões de alto e baixo nível que permitem aos usuários acessar os diferentes recursos do.
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: permissão, alto nível, baixo nível, perfil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# Níveis de permissão {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Cada perfil de produto é composto de permissões que permitem aos usuários acessar os diferentes recursos.
Eles podem ser divididos em dois tipos:

* **Permissão de alto nível**: representa as diferentes permissões que podem ser atribuídas a **[!UICONTROL Perfil do produto]** no [!DNL Admin console], como **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Permissões de alto nível abrangem permissões de baixo nível.

* **Permissão de baixo nível**: representa as diferentes permissões provenientes da permissão de alto nível.

Por exemplo, a variável **[!DNL Journey administrator]** perfil de produto é atribuído ao **[!DNL Manage journeys]** permissão. Dessa permissão resultam as permissões de baixo nível que permitirão ao administrador do Jornada gravar, ler e excluir jornadas.

## Recurso de Jornada {#journey-capability}

### [!DNL Manage journeys] permissão {#manage-journeys}

A variável **[!DNL Manage journeys]** a permissão de alto nível permite que os usuários criem Jornadas novas e editem/excluam  existentes, bem como acesso aos objetos usados na tela de jornada para criar o fluxo de jornada.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Específico do Adobe Experience Platform:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] permissão {#publish-journeys}

A variável **[!DNL Publish journeys]** a permissão de alto nível permite que os usuários publiquem jornadas.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] permissão {#view-journeys}

A variável **[!DNL View journeys]** a permissão de alto nível permite que os usuários naveguem e visualizem jornadas.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * journeys.read

* Específico do Adobe Experience Platform:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] permissão {#manage-journeys-events}

A variável **[!DNL Manage journeys events, data sources and actions]** a permissão de alto nível permite que os usuários definam configurações de eventos e dados.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * jornada_events.read
   * jornada_events.write
   * jornada_events.delete
   * jornada_data_sources.read
   * jornada_data_sources.write
   * jornada_data_sources.delete
   * jornada_actions.read
   * jornada_actions.write
   * jornada_actions.delete

* Específico do Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] permissão {#view-journeys-event}

A variável **[!DNL View journeys events, data sources and actions]** a permissão de alto nível permite que os usuários usem eventos e dados no fluxo de jornada.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * jornada_events.read
   * jornada_data_sources.read
   * jornada_actions.read

* Específico do Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] permissão {#view-journeys-report}

A variável **[!DNL View journeys report]** a permissão de alto nível permite que os usuários leiam o relatório de jornada.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * jornada_report.read
   * messages_report.read

* Específico do Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Recurso de gestão de decisão {#decisions-permissions}

### [!DNL Manage decisions] permissão {#manage-decisioning}

A variável **[!DNL Manage decisions]** a permissão de alto nível permite que os usuários criem novos e editem/excluam arquivos existentes **[!DNL Activity entities]**, bem como gerenciar os objetos usados nessas atividades para tomar as decisões.

Inclui as seguintes permissões de baixo nível:

* Específico para a gestão de decisões:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Específico do Adobe Experience Platform:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] permissão {#view-decisions}

A variável **[!DNL View decisions]** a permissão de alto nível permite que os usuários usem uma Atividade existente e objetos comerciais relacionados para tomar as decisões.

Inclui as seguintes permissões de baixo nível:

* Específico para a gestão de decisões:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Específico do Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] permissão {#publish-decisions}

A variável **[!DNL Publish offers decisioning]** a permissão de alto nível permite que os usuários acessem aprovar/não aprovar atividades de Oferta.

Inclui as seguintes permissões de baixo nível:

* Específico para a gestão de decisões:
   * offer_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Específico do Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] permissão {#manage-ranking-strategies}

A variável **[!DNL Manage ranking strategies]** a permissão de alto nível permite que os usuários leiam, criem, editem e excluam estratégias de classificação.

Inclui as seguintes permissões de baixo nível:

* Específico para a gestão de decisões:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Recurso de administração {#administration-permissions}

### [!DNL Manage subdomains delegation] permissão {#manage-subdomain}

A variável **[!DNL Manage subdomains delegation]** a permissão de alto nível permite que os usuários criem, editem e excluam delegações de subdomínio (incluindo o pool de IP).

Inclui as seguintes permissões de baixo nível:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] permissão {#manage-ptr}

A variável **[!DNL Manage PTR records]** a permissão de alto nível permite que os usuários leiam e editem registros PTR que foram configurados com base no subdomínio.

Inclui as seguintes permissões de baixo nível:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] permissão {#view-ptr}

A variável **[!DNL View PTR records]** a permissão de alto nível permite que os usuários visualizem registros PTR que foram configurados com base no subdomínio.

Inclui as seguintes permissões de baixo nível:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] permissão {#manage-ip-pools}

A variável **[!DNL Manage IP pools]** a permissão de alto nível permite que os usuários criem, editem e excluam a definição de afinidade.

Inclui as seguintes permissões de baixo nível:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] permissão {#manage-channel-surface}

A variável **[!DNL Manage channel surface]** a permissão de alto nível permite que os usuários criem, editem e excluam superfícies de canal em canais no nível da sandbox.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (do Adobe Experience Platform Launch)

### [!DNL View channel surface] permissão {#view-channel-surface}

A variável **[!DNL View channel surface]** a permissão de alto nível permite que os usuários visualizem superfícies de canal para saber quais superfícies de canal usar.

Inclui as seguintes permissões de baixo nível:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (da Coleção de dados da Adobe Experience Platform)

### [!DNL Manage suppression] permissão {#manage-suppression}

A variável **[!DNL Manage suppression]** a permissão de alto nível permite que os usuários definam o número de rejeições antes que um endereço de email seja adicionado à lista de supressão, bem como adicionar e excluir entradas da/para a lista de supressão.

Inclui as seguintes permissões de baixo nível:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] permissão {#view-suppression-list}

A variável **[!DNL View suppression list]** a permissão de alto nível permite que os usuários visualizem o conteúdo e as configurações da lista de supressão.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * suppression_list.view

* Específico do Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] permissão {#export-suppression-list}

A variável **[!DNL Export suppression list]** a permissão de alto nível permite que os usuários baixem a lista de supressão como um arquivo CSV.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * suppression_list.export

* Específico do Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] permissão {#manage-landing-page-settings}

A variável **[!DNL Manage landing page settings]** a permissão de alto nível permite que os usuários leiam, criem e editem subdomínios de página de aterrissagem e configurações predefinidas.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] permissão {#manage-frequency-rules}

A variável **[!DNL Manage frequency rules]** a permissão de alto nível permite que os usuários leiam, criem, editem, excluam e ativem/desativem regras de frequência.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] permissão {#view-frequency-rules}

A variável **[!DNL View frequency rules]** a permissão de alto nível permite que os usuários visualizem regras de frequência.

Inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * frequency_rules.read
