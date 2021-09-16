---
title: Níveis de permissão
description: Saiba mais sobre permissões de alto e baixo nível
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
source-git-commit: b32306f9561946a6c289e5e9c7cc3243349141bc
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Níveis de permissão {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Cada perfil de produto é composto de permissões que permitem aos usuários acessar os diferentes recursos.
Eles podem ser divididos em dois tipos:

* **Permissão** de alto nível: representa as diferentes permissões que podem ser atribuídas  **[!UICONTROL Product profile]** no  [!DNL Admin console], como  **[!UICONTROL Publish journeys]** e  **[!UICONTROL Manage subdomains delegation]**. As permissões de alto nível abrangem permissões de baixo nível.

* **Permissão** de baixo nível: representa as diferentes permissões que vêm da permissão de alto nível.

Por exemplo, o perfil de produto **[!UICONTROL Journey administrator]** recebe a permissão **[!UICONTROL Manage journeys]**. Dessa permissão resulta as permissões de baixo nível que permitirão ao administrador do Jornada gravar, ler e excluir jornadas.

## Recurso de jornada {#journey-capability}

### Permissão Gerenciar jornadas {#manage-journeys}

A permissão de alto nível **[!UICONTROL Manage journeys]** permite que os usuários criem Jornadas novas e editem/excluam as existentes, bem como o acesso aos objetos que são usados na tela de jornada para criar o fluxo de jornada.

Ele inclui as seguintes permissões de baixo nível:

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

### Permissão Publicar jornadas {#publish-journeys}

A permissão de alto nível **[!UICONTROL Publish journeys]** permite que os usuários publiquem jornadas.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * journeys.publish
   * journeys.read

### Exibir permissão de jornadas {#view-journeys}

A permissão de alto nível **[!UICONTROL View journeys]** permite que os usuários naveguem e visualizem jornadas.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * journeys.read

* Específico do Adobe Experience Platform:
   * segments.read
   * profiles.read

### Gerenciar eventos do jornada, fontes de dados e permissões de ações {#manage-journeys-events}

A permissão de alto nível **[!UICONTROL Manage journeys events, data sources and actions]** permite que os usuários configurem configurações de evento e dados.

Ele inclui as seguintes permissões de baixo nível:

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

### Exibir eventos do jornada, fontes de dados e permissões de ações {#view-journeys-event}

A permissão de alto nível **[!UICONTROL View journeys events, data sources and actions]** permite que os usuários usem eventos e dados no fluxo de jornada.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * jornada_events.read
   * jornada_data_sources.read
   * jornada_actions.read

* Específico do Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Exibir permissão de relatório de jornadas {#view-journeys-report}

A permissão de alto nível **[!UICONTROL View journeys report]** permite que os usuários leiam o relatório de jornada somente leitura.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * jornada_report.read
   * messages_report.read

* Específico do Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Capacidade de mensagem {#message-capability}

### Permissão Gerenciar mensagens {#manage-messages}

A permissão de alto nível **[!UICONTROL Manage messages]** permite que os usuários criem e editem/excluam mensagens.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Específico do Adobe Experience Platform:
   * segments.read
   * schemas.read

### Gerenciar visualização de mensagens e permissão de teste {#mange-messages-preview}

A permissão de alto nível **[!UICONTROL Manage messages preview and test]** permite que os usuários visualizem mensagens personalizadas.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Específico do Adobe Experience Platform:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### Permissão Publicar mensagens {#publish-messages}

A permissão de alto nível **[!UICONTROL Publish messages]** permite que os usuários publiquem mensagens.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages.publish

* Específico do Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Exibir permissão de mensagens {#view-messages}

A permissão de alto nível **[!UICONTROL View messages]** permite que os usuários leiam somente mensagens.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages.read
   * messages_presets.read

* Específico do Adobe Experience Platform:
   * schemas.read
   * segments.read

### Exibir permissão de relatório de mensagens {#view-message-reports}

A permissão de alto nível **[!UICONTROL View messages report]** permite que os usuários criem relatórios de email e de push somente leitura.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Capacidade de gestão de decisões {#decisions-permissions}

### Permissão Gerenciar decisões {#manage-decisioning}

A permissão de alto nível **[!UICONTROL Manage decisions]** permite que os usuários criem e editem/excluam **[!UICONTROL Activity entities]** existentes, bem como gerenciem os objetos usados nessas atividades para tomar as decisões.

Ele inclui as seguintes permissões de baixo nível:

* Gestão específica da decisão:
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

### Exibir permissão de decisões {#view-decisions}

A permissão de alto nível **[!UICONTROL View decisions]** permite que os usuários usem uma Atividade existente e objetos comerciais relacionados para tomar as decisões.

Ele inclui as seguintes permissões de baixo nível:

* Gestão específica da decisão:
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

### Permissão para publicar ofertas de decisão {#publish-decisions}

A permissão de alto nível **[!UICONTROL Publish offers decisioning]** permite que os usuários acessem aprovar/cancelar a aprovação de atividades de Oferta.

Ele inclui as seguintes permissões de baixo nível:

* Gestão específica da decisão:
   * offers_activity.read
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

### Permissão Gerenciar estratégias de classificação {#manage-decisions}

A permissão de alto nível **[!UICONTROL Manage ranking strategies]** permite que os usuários leiam, criem, editem e excluam o relatório de mensagens personalizadas e usem recursos de ação.

Ele inclui as seguintes permissões de baixo nível:

* Gestão específica da decisão:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Capacidade de administração {#administration-permissions}

### Gerenciar permissão de delegação de subdomínios {#manage-subdomain}

A permissão de alto nível **[!UICONTROL Manage subdomains delegation]** permite que os usuários criem, editem e excluam delegações de subdomínio (incluindo pool de IP).

Ele inclui as seguintes permissões de baixo nível:

* subdomains_delegation.read
* subdomínios_delegation.write
* subdomains_delegation.delete

### Exibir permissão de registros PTR {#view-ptr}

A permissão de alto nível **[!UICONTROL View PTR records]** permite que os usuários visualizem registros PTR que foram configurados com base no subdomínio.

Ele inclui as seguintes permissões de baixo nível:

* PTR_records.read
* subdomains_delegation.read

### Gerenciar permissões de pools de IP {#manage-ip-pools}

A permissão de alto nível **[!UICONTROL Manage IP pools]** permite que os usuários criem, editem e excluam a definição de afinidade.

Ele inclui as seguintes permissões de baixo nível:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Permissão Gerenciar configurações gerais de mensagens {#manage-message-settings}

A permissão de alto nível **[!UICONTROL Manage messages general settings]** permite que os usuários criem, editem e excluam configurações globais no nível da sandbox.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Específico do Adobe Experience Platform:
   * schemas.read

### Exibir permissões gerais de configurações de mensagens {#view-message-settings}

A permissão de alto nível **[!UICONTROL View messages general settings]** permite que os usuários visualizem as configurações gerais das mensagens, como o endereço de execução.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages_general_settings.read
* Específico do Adobe Experience Platform:
   * schemas.read

### Permissão Gerenciar predefinições de mensagens {#manage-message-presets}

A permissão de alto nível **[!UICONTROL Manage messages presets]** permite que os usuários criem, editem e excluam predefinições de mensagens em canais no nível da sandbox.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (do Adobe Experience Platform Launch)

### Permissão Exibir predefinições de mensagens {#view-message-presets}

A permissão de alto nível **[!UICONTROL View messages presets]** permite que os usuários visualizem predefinições de mensagens para saber quais predefinições de mensagens usar ao criar uma mensagem.

Ele inclui as seguintes permissões de baixo nível:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (do Adobe Experience Platform Launch)

### Gerenciar permissão de supressão {#manage-suppression}

A permissão de alto nível **[!UICONTROL Manage suppression]** permite que os usuários definam o número de rejeições antes de um endereço de email ser adicionado à lista de supressão, bem como adicionar e excluir entradas de/para a lista de supressão.

Ele inclui as seguintes permissões de baixo nível:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Exibir permissão da lista de supressão {#view-suppresion-list}

A permissão de alto nível **[!UICONTROL View suppression list]** permite que os usuários visualizem o conteúdo e as configurações da lista de supressão.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * suppression_list.view
* Específico do Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Permissão Exportar lista de supressão {#export-suppression-list}

A permissão de alto nível **[!UICONTROL Export suppression list]** permite que os usuários baixem a lista de supressão como um arquivo CSV.

Ele inclui as seguintes permissões de baixo nível:

* Específico do Journey Optimizer:
   * suppression_list.export
* Específico do Adobe Experience Platform:
   * profiles.read
   * datasets.read
