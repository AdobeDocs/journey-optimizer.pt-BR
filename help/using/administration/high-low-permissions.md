---
solution: Journey Optimizer
product: journey optimizer
title: Níveis de permissão
description: Saiba mais sobre permissões de alto e baixo nível que permitem aos usuários acessar os diferentes recursos do.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: permissão, alto nível, baixo nível, perfil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 9d87d133bb580ebed94a265beded5895f7fd0301
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Níveis de permissão {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Cada função é composta de permissões que permitem aos usuários acessar os diferentes recursos.
Eles podem ser divididos em dois tipos:

* **Permissão de alto nível**: representa as diferentes permissões que podem ser atribuídas à **[!UICONTROL Função]**, como **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Permissões de alto nível abrangem permissões de baixo nível. Permissões de alto nível são detalhadas em [esta página](ootb-permissions.md).

* **Permissão de baixo nível**: representa as diferentes permissões provenientes da permissão de alto nível.

Por exemplo, a função **[!DNL Journey administrator]** recebe a permissão **[!DNL Manage journeys]**. Dessa permissão resultam as permissões de baixo nível que permitirão ao administrador do Jornada gravar, ler e excluir jornadas.

## Jornada recurso {#journey-capability}

* A permissão de alto nível **[!DNL Manage journeys]** permite que os usuários criem Jornadas novas e editem/excluam  existentes, bem como acesso aos objetos usados na tela de jornada para criar o fluxo de jornada.

+++ Inclui as seguintes permissões de baixo nível:

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

+++

* A permissão de alto nível **[!DNL Publish journeys]** permite que os usuários publiquem jornadas.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* A permissão de alto nível **[!DNL View journeys]** permite que os usuários naveguem e visualizem jornadas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * journeys.read

   * Específico do Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* A permissão de alto nível do **[!DNL Manage journeys events, data sources and actions]** permite que os usuários definam configurações de eventos e dados.

+++ Inclui as seguintes permissões de baixo nível:

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

+++

* A permissão de alto nível **[!DNL View journeys events, data sources and actions]** permite que os usuários usem eventos e dados no fluxo de jornada.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * jornada_events.read
      * jornada_data_sources.read
      * jornada_actions.read

   * Específico do Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* A permissão de alto nível **[!DNL View journeys report]** permite que os usuários façam relatórios de jornada somente leitura.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * jornada_report.read
      * messages_report.read

   * Específico do Adobe Experience Platform:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Recurso de regras do Journey Optimizer {#journey-rules-capability}

* A permissão de alto nível **[!DNL Manage frequency rules]** permite que os usuários leiam, criem, editem, excluam e ativem/desativem regras de frequência.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* A permissão de alto nível **[!DNL View frequency rules]** permite que os usuários exibam regras de frequência.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * frequency_rules.read

+++

## Recurso de campanha {#campaign-capability}

* A permissão de alto nível **[!DNL Export suppression list]** permite que os usuários baixem a lista de supressão como um arquivo CSV.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * suppression_list.export

   * Específico do Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* A permissão de alto nível **[!DNL Manage campaigns]** permite que os usuários criem campanhas novas e editem/excluam campanhas

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* A permissão de alto nível **[!DNL Publish campaigns]** permite que os usuários publiquem campanhas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* A permissão de alto nível **[!DNL View campaigns report]** permite que os usuários leiam e editem o relatório de campanhas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Recurso de gestão de decisão {#decisions-permissions}

* A permissão de alto nível **[!DNL Manage decisions]** permite que os usuários criem novos e editem/excluam **[!DNL Activity entities]** existentes, bem como gerenciem os objetos usados nessas atividades para tomar decisões.

+++ Inclui as seguintes permissões de baixo nível:

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

+++

* A permissão de alto nível **[!DNL View decisions]** permite que os usuários usem uma Atividade existente e objetos comerciais relacionados para tomar as decisões.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico para a gestão de decisões:
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Específico do Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read

+++

* A permissão de alto nível **[!DNL Manage offers]** permite que os usuários criem, editem e excluam todas as ofertas, componentes, decisões de leitura e coleções.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico para a gestão de decisões:
      * offer_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Específico do Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* A permissão de alto nível **[!DNL Manage ranking strategies]** permite que os usuários leiam, criem, editem e excluam estratégias de classificação.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico para a gestão de decisões:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Recurso de configurações de canal {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ It includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* A permissão de alto nível **[!DNL Manage file routing]** permite que os usuários criem, editem e excluam configurações de roteamento de arquivos.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* A permissão de alto nível **[!DNL Manage IP pools]** permite que os usuários criem, editem e excluam a definição de afinidade.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* A permissão de alto nível **[!DNL Manage landing page settings]** permite que os usuários leiam, criem e editem subdomínios e configurações predefinidas da página de aterrissagem.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* A permissão de alto nível **[!DNL Manage messages general settings]** permite que os usuários criem, editem e excluam configurações globais no nível da sandbox.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Específico do Adobe Experience Platform:
      * schemas.read

+++

* A permissão de alto nível **[!DNL Manage messages presets]** permite que os usuários leiam, criem, editem e excluam configurações de canal entre canais no nível da sandbox.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Específico da Coleção de dados:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* A permissão de alto nível **[!DNL Manage PTR records]** permite que os usuários leiam e editem registros PTR que foram configurados com base no subdomínio.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* A permissão de alto nível **[!DNL Manage Seedlist]** permite que os usuários leiam, criem, editem e excluam a Seedlist.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* A permissão de alto nível **[!DNL Manage SMS subdomains]** permite que os usuários leiam, criem, editem e excluam subdomínios de SMS.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* A permissão de alto nível **[!DNL Manage subdomains delegations]** permite que os usuários criem, editem e excluam delegações de subdomínio (incluindo o pool de IP).

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* A permissão de alto nível **[!DNL Manage suppression]** permite que os usuários definam o número de rejeições antes que um endereço de email seja adicionado à lista de supressão, bem como adicionar e excluir entradas da/para a lista de supressão.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* A permissão de alto nível **[!DNL View file routing]** permite que os usuários exibam configurações de roteamento de arquivos.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * file_routing.read

+++

* A permissão de alto nível **[!DNL View messages general settings]** permite que os usuários exibam configurações gerais de mensagens, como o endereço de execução.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_general_settings.read

   * Específico do Adobe Experience Platform:
      * schemas.read

+++

* A permissão de alto nível **[!DNL View messages presets]** permite que os usuários exibam predefinições de mensagens.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Específico da Coleção de dados:
      * Mobile_setting.read

+++

* A permissão de alto nível **[!DNL View PTR records]** permite que os usuários exibam registros PTR que foram configurados com base no subdomínio.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* A permissão de alto nível **[!DNL View suppression list]** permite que os usuários exibam o conteúdo e as configurações da lista de supressão.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * suppression_list.view

   * Específico do Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

## Recurso de assistência de IA {#ai-permissions}

* A permissão de alto nível **[!DNL Generate content]** permite que os usuários acessem o Assistente de IA na Journey Optimizer.

+++ Inclui a seguinte permissão de baixo nível:

   * Específico do Journey Optimizer:
      * ai-assistant-generated-content.generate

+++
