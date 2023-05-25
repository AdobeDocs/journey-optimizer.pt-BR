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
source-git-commit: 7ac2ae714f2d11d2559b6195af37e2dece35b17c
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Níveis de permissão {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Cada função é composta de permissões que permitem aos usuários acessar os diferentes recursos.
Eles podem ser divididos em dois tipos:

* **Permissão de alto nível**: representa as diferentes permissões que podem ser atribuídas a **[!UICONTROL Função]** no [!DNL Admin console], como **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Permissões de alto nível abrangem permissões de baixo nível.

* **Permissão de baixo nível**: representa as diferentes permissões provenientes da permissão de alto nível.

Por exemplo, a variável **[!DNL Journey administrator]** é atribuída a função **[!DNL Manage journeys]** permissão. Dessa permissão resultam as permissões de baixo nível que permitirão ao administrador do Jornada gravar, ler e excluir jornadas.

## Jornada recurso {#journey-capability}

* **[!DNL Manage journeys]** a permissão de alto nível permite que os usuários criem Jornadas novas e editem/excluam  existentes, bem como acesso aos objetos usados na tela de jornada para criar o fluxo de jornada.

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

* **[!DNL Publish journeys]** a permissão de alto nível permite que os usuários publiquem jornadas.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** a permissão de alto nível permite que os usuários naveguem e visualizem jornadas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * journeys.read
   * Específico do Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** a permissão de alto nível permite que os usuários definam configurações de eventos e dados.

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

* **[!DNL View journeys events, data sources and actions]** a permissão de alto nível permite que os usuários usem eventos e dados no fluxo de jornada.

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

* **[!DNL View journeys report]** a permissão de alto nível permite que os usuários leiam o relatório de jornada.

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

* **[!DNL Manage frequency rules]** a permissão de alto nível permite que os usuários leiam, criem, editem, excluam e ativem/desativem regras de frequência.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** a permissão de alto nível permite que os usuários visualizem regras de frequência.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * frequency_rules.read

+++

## Recurso de campanha {#campaign-capability}

* **[!DNL Manage campaigns]** a permissão de alto nível permite que os usuários criem campanhas novas e editem/excluam campanhas

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete

      <!--* experiments.read
      * experiments.write
      * experiments.delete-->
+++

* **[!DNL Publish campaigns]** a permissão de alto nível permite que os usuários publiquem campanhas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * campaign-read
      * campaign-publish
         <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** a permissão de alto nível permite que os usuários leiam e editem o relatório campanhas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * campaign.read
      * campaign-report.read

      <!--* experiments.read
      * experiments_report.read-->
+++

## Recurso de gestão de decisão {#decisions-permissions}

* **[!DNL Manage decisions]** a permissão de alto nível permite que os usuários criem novos e editem/excluam arquivos existentes **[!DNL Activity entities]**, bem como gerenciar os objetos usados nessas atividades para tomar as decisões.

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

* **[!DNL View decisions]** a permissão de alto nível permite que os usuários usem uma Atividade existente e objetos comerciais relacionados para tomar as decisões.

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
      * datasets.write
      * datasets.delete

+++

* **[!DNL Manage offers]** a permissão de alto nível permite que os usuários criem, editem e excluam todas as ofertas, componentes, decisões de leitura e coleções.

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

* **[!DNL Manage ranking strategies]** a permissão de alto nível permite que os usuários leiam, criem, editem e excluam estratégias de classificação.

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

* **[!DNL Manage subdomains delegation]** a permissão de alto nível permite que os usuários criem, editem e excluam delegações de subdomínio (incluindo o pool de IP).

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage PTR records]** a permissão de alto nível permite que os usuários leiam e editem registros PTR que foram configurados com base no subdomínio.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL View PTR records]** a permissão de alto nível permite que os usuários visualizem registros PTR que foram configurados com base no subdomínio.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL Manage IP pools]** a permissão de alto nível permite que os usuários criem, editem e excluam a definição de afinidade.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage messages general settings]** a permissão de alto nível permite que os usuários criem, editem e excluam configurações globais no nível da sandbox.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete
   * Específico do Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL View messages general settings]** a permissão de alto nível permite que os usuários visualizem configurações gerais de mensagens, como o endereço de execução.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_general_settings.read
   * Específico do Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL Manage channel surface]** a permissão de alto nível permite que os usuários criem, editem e excluam superfícies de canal em canais no nível da sandbox.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (do Adobe Experience Platform Launch)

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->

* **[!DNL Manage suppression]** a permissão de alto nível permite que os usuários definam o número de rejeições antes que um endereço de email seja adicionado à lista de supressão, bem como adicionar e excluir entradas da/para a lista de supressão.

+++ Inclui as seguintes permissões de baixo nível:
   * Específico do Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View suppression list]** a permissão de alto nível permite que os usuários visualizem o conteúdo e as configurações da lista de supressão.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * suppression_list.view
   * Específico do Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Export suppression list]** a permissão de alto nível permite que os usuários baixem a lista de supressão como um arquivo CSV.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * suppression_list.export
   * Específico do Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage landing page settings]** a permissão de alto nível permite que os usuários leiam, criem e editem subdomínios de página de aterrissagem e configurações predefinidas.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

* **[!DNL Manage messages presets]** a permissão de alto nível permite que os usuários leiam, criem, editem e excluam marcas de conteúdo.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
   * Específico da Coleção de dados:
      * Mobile_setting.read

+++

* **[!DNL View messages presets]** a permissão de alto nível permite que os usuários visualizem predefinições de mensagens.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read
   * Específico da Coleção de dados:
      * Mobile_setting.read

+++

* **[!DNL Manage SMS subdomains]** a permissão de alto nível permite que os usuários leiam, criem, editem e excluam subdomínios de SMS.

+++ Inclui as seguintes permissões de baixo nível:

   * Específico do Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete
+++
