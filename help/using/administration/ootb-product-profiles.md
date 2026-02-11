---
solution: Journey Optimizer
product: journey optimizer
title: Funções integradas do Journey Optimizer
description: Saiba mais sobre as funções integradas
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: permissões, criação, mensagens
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: a91d5c6a22f81411d7a9acbe2bbc8e86c1a4da13
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 7%

---

# Funções integradas {#ootb-product-profiles}

As funções integradas são um conjunto de direitos unitários que permitem aos usuários acessar determinadas funcionalidades ou objetos na interface. Consulte [esta página](ootb-permissions.md) para obter a lista de permissões disponíveis para criar sua função.


## [!DNL Campaign Administrator] {#campaign-administrator}

A função **[!DNL Campaign Administrator]** permite que os menus de administração com a possibilidade de gerenciar e publicar Campanhas e Gestão de decisões.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acesso a sandboxes.</li> </ul> |
| Campanhas | <ul><li> **[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publicar campanhas.</li><li>**[!DNL View campaigns report]**: leia e edite o relatório de campanhas.</li></ul> |
| Configurações de canal | <ul> <li>**[!DNL Export suppression list]**: acesso à lista de supressão de exportação como arquivo CSV.</li> <li>**[!DNL Manage alerts]**: habilitar/desabilitar alertas para campanhas, mensagens e direitos.</li> <li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir pool de IPs.</li> <li>**[!DNL Manage landing page settings]**: ler, criar, editar e excluir configurações da página de aterrissagem.</li> <li>**[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li> <li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir a identidade visual do conteúdo.</li> <li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: ler, criar, editar e excluir configurações de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir a delegação de subdomínio.</li> <li>**[!DNL Manage suppression rules]**: acessar as regras de supressão de leitura, criação, edição e exclusão.</li> <li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li> <li>**[!DNL View suppression list]**: ler e exportar a lista de supressão local.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

A função **[!DNL Campaign Approver]** permite que os usuários aprovem entregas e as publiquem. Mais tarde, eles poderão verificar o sucesso de suas entregas com os relatórios **[!DNL Campaigns]**.

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Campanhas | <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publicar campanhas.</li><li>**[!DNL View campaigns report]**: ler, editar relatórios de campanha.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

A função **[!DNL Campaign Manager]** permite que os usuários criem e editem **[!UICONTROL Campanhas]** e todos os recursos vinculados a **[!UICONTROL Campanhas]**, mas não poderão publicá-las.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Campanhas | <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL View campaigns report]**: ler, editar relatório de jornada.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

A função **[!DNL Campaign Viewer]** permite acesso somente leitura aos recursos **[!UICONTROL Campanhas]** e **[!UICONTROL Gerenciamento de decisão]**.

Os usuários atribuídos a esta função não poderão editar nem publicar.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Campanhas | <ul><li>**[!DNL View campaigns]**: acesso somente leitura a campanhas.</li><li>**[!DNL View campaigns report]**: acesso somente leitura aos relatórios de campanhas.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisões.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

A função **[!DNL Content Library Manager]** permite acesso apenas ao menu **[!UICONTROL Modelos de conteúdo]**. Os usuários atribuídos a essa função só poderão acessar a biblioteca de modelos para criar conteúdo sem acessar as jornadas ou campanhas.

Essa permissão inclui as seguintes permissões:

| Recurso | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Biblioteca da Journey Optimizer | <ul><li>**[!DNL Manage library items]**: ler, criar, editar e excluir itens da Biblioteca Journey Optimizer, incluindo modelos de conteúdo e fragmentos.</li><li>**[!DNL Manage simulate content]**: acesso à opção **[!UICONTROL Simular conteúdo]** para visualização e prova.</li><li>**[!DNL Publish Fragment]**: publicar fragmentos de conteúdo.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

A função **[!DNL Decisioning manager]** permite acesso apenas ao menu **[!UICONTROL Gerenciamento de decisão]**. Os usuários atribuídos a essa função só poderão gerenciar, exibir e publicar decisões.

Essa permissão inclui as seguintes permissões:

| Recurso | Permissões |
|-|-|
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisão.</li><li>**[!DNL Publish decisions]**: ativar ou desativar atividades de decisão.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

A função **[!DNL Journey Administrator]** permite que os menus de administração com a possibilidade de gerenciar e publicar Jornadas e Gestão de decisões.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acesso a sandboxes.</li> </ul> |
| Configurações de canal | <ul> <li>**[!DNL Manage alerts]**: habilitar/desabilitar alertas para jornadas e direitos.</li> <li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir pool de IPs.</li> <li>**[!DNL Manage Landing page settings]**: criar, editar e excluir subdomínios e predefinições de página de aterrissagem.</li> <li>**[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li> <li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir a identidade visual do conteúdo.</li> <li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: criar, editar e excluir credenciais de API e configurações de canal de SMS necessárias para habilitar o canal de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir a delegação de subdomínio.</li> <li>**[!DNL Manage suppression rules]**: acessar as regras de supressão de leitura, criação, edição e exclusão.</li> <li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li> <li>**[!DNL View suppression list]**: ler e exportar a lista de supressão local.</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL Manage data usage policies]**: ler, criar, editar e excluir políticas de uso de dados.</li> <li>**[!DNL Manage usage label]**: ler, criar e excluir rótulos de uso.</li> <li>**[!DNL View data usage policies]**: acesso somente leitura a políticas de uso de dados.</li> <li>**[!DNL View user activity log]**: acesso somente leitura para visualizar logs de auditoria registrados de atividades do Experience Platform.</li> </ul> |
| Gestão de decisões | <ul> <li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li> <li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li> </ul> |
| Jornadas | <ul> <li>**[!DNL Manage journeys]**: ler, criar, editar, parar (ao vivo, modo de teste e simulação) e excluir jornadas. </li> <li>**[!DNL Manage journeys events, data sources and actions]**: ler, criar, editar e excluir eventos, fontes ou ações.</li> <li>**[!DNL Publish journeys]**: publicar, iniciar modo de teste, iniciar simulação, pausar e retomar jornadas. </li> <li>**[!DNL View journeys report]**: ler e editar o relatório de jornadas.</li> </ul> |
| Biblioteca da Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]**: adicionar e excluir expressões salvas na Biblioteca [!DNL Journey Optimizer].</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

A função **[!DNL Journey Approver]** permite que os usuários aprovem entregas e as publiquem. Mais tarde, eles poderão verificar o sucesso de suas entregas com os relatórios **[!DNL Journey]**.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View channel configurations]**: acesso somente leitura às configurações de canal.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Jornadas | <ul><li>**[!DNL Manage journeys]**: ler, criar, editar, parar (ao vivo, modo de teste e simulação) e excluir jornadas. </li><li>**[!DNL Publish journey]**: publicar, iniciar modo de teste, iniciar simulação, pausar e retomar jornadas. </li><li>**[!DNL View journeys events, data sources and actions]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatórios de jornada.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

A função **[!DNL Journey Manager]** permite que os usuários criem e editem **[!UICONTROL Jornadas]** e todos os recursos vinculados a **[!UICONTROL Jornadas]**, mas não poderão publicá-los.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View channel configurations]**: acesso somente leitura às configurações de canal.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Jornadas | <ul><li>**[!DNL Manage journeys]**: ler, criar, editar, parar (ao vivo, modo de teste e simulação) e excluir jornadas.</li><li>**[!DNL View journeys events]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatório de jornada.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

A função **[!DNL Journey viewer]** permite acesso somente leitura aos recursos do **[!UICONTROL Jornada]** e do **[!UICONTROL Gerenciamento de decisão]**.

Os usuários atribuídos a esta função não poderão editar nem publicar.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Gestão de decisões | <ul><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisões.</li></ul> |
| Jornadas | <ul><li>**[!DNL View journeys]**: acesso somente leitura a jornadas.</li><li>**[!DNL View journeys event, data sources, actions]**: acesso somente leitura a eventos e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: acesso somente leitura a relatórios do jornada.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

A função **[!DNL Orchestrated Campaign Administrator]** permite que os menus de administração com a possibilidade de gerenciar e publicar campanhas Orquestradas.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**: habilitar ou acessar recursos de campanha e público alimentados por IA.</li> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acesso a sandboxes.</li> <li>**[!DNL View operational insights]**: acesso somente leitura a insights e painéis de monitoramento no nível do sistema.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL Export suppression list]**: acesso à lista de supressão de exportação como arquivo CSV.</li> <li>**[!DNL Manage alerts]**: habilitar/desabilitar alertas para campanhas, mensagens e direitos.</li> <li>**[!DNL Manage custom dashboards]**: ler, criar, editar e excluir painéis personalizados.</li><li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir pool de IPs.</li> <li>**[!DNL Manage landing page settings]**: ler, criar, editar e excluir configurações da página de aterrissagem.</li> <li>**[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li> <li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir a identidade visual do conteúdo.</li><li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: ler, criar, editar e excluir configurações de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir a delegação de subdomínio.</li> <li>**[!DNL Manage suppression rules]**: acessar as regras de supressão de leitura, criação, edição e exclusão.</li> <li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li> <li>**[!DNL View suppression list]**: ler e exportar a lista de supressão local.</li> </ul> |
| Painel | <ul> <li>**[!DNL Manage standard dashboard]**: ler, criar, editar e excluir widgets e esquemas de widget personalizados por meio da Biblioteca de widgets.</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL View user activity log]**: acesso somente leitura para visualizar logs de auditoria registrados de atividades do Experience Platform. </li> </ul> |
| Ingestão de dados | <ul> <li>**[!DNL Manage sources]**: ler, criar, editar e desabilitar fontes.</li> </ul> |
| Gerenciamento de dados | <ul> <li>**[!DNL Manage datasets]**: ler, criar, editar e excluir conjuntos de dados.</li> </ul> |
| Modelagem de dados | <ul> <li>**[!DNL Manage schemas]**: ler, criar, editar e excluir esquemas e recursos relacionados.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li></ul> |
| Regras do Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: acesso somente leitura a regras de frequência.</li><li>**[!DNL Manage frequency rules]**: ler, criar, editar ou excluir regras de frequência.</li> </ul> |
| Mensagens | <ul><li> **[!DNL Manage Messages]**: ler, criar, editar e excluir mensagens. </li> **[!DNL Manage Messages Preview and Test]**: aprovar e publicar mensagens quando uma política for aplicada.</li><li>**[!DNL Publish Messages]**: publicar mensagens. </li><li>**[!DNL View Messages Report]**: ler e editar relatórios de mensagens. <li></ul> |
| Campanhas orquestradas | <ul><li> **[!DNL Manage orchestrated campaigns]**: ler, criar, editar e excluir campanhas orquestradas.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: ler, criar, editar e excluir links e reconciliações entre Perfis do Adobe Experience Platform e entidades de armazenamento relacional.</li><li>**[!DNL Publish orchestrated campaigns]**: publicar campanhas orquestradas.</li><li>**[!DNL View orchestrated campaigns report]**: ler e editar o relatório Campanhas orquestradas.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

A função **[!DNL Orchestrated Campaign Approver]** permite que os usuários publiquem campanhas orquestradas.

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Enable AI Assistant]**: habilitar ou acessar recursos de campanha e público alimentados por IA.</li>  <li>**[!DNL View operational insights]**: acesso somente leitura a insights e painéis de monitoramento no nível do sistema.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li> <li>**[!DNL Manage custom dashboards]**: criar, editar e excluir painéis personalizados.</li></ul> |
| Painel | <ul> <li>**[!DNL Manage standard dashboard]**: ler, criar, editar e excluir widgets e esquemas de widget personalizados por meio da Biblioteca de widgets.</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL View user activity log]**: acesso somente leitura para visualizar logs de auditoria registrados de atividades do Experience Platform.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |
| Regras do Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: acesso somente leitura a regras de frequência.</li></ul> |
| Mensagens | <ul><li> **[!DNL Manage Messages]**: ler, criar, editar e excluir mensagens. </li> **[!DNL Manage Messages Preview and Test]**: aprovar e publicar mensagens quando uma política for aplicada.</li><li>**[!DNL Publish Messages]**: publicar mensagens. </li><li>**[!DNL View Messages Report]**: ler e editar relatórios de mensagens. <li></ul> |
| Campanhas orquestradas | <ul><li>**[!DNL Manage orchestrated campaigns]**: ler, criar, editar e excluir campanhas orquestradas.</li><li>**[!DNL Publish orchestrated campaigns]**: publicar campanhas orquestradas.</li><li>**[!DNL View orchestrated campaigns admin]**: acesso somente leitura a links e reconciliações entre Perfis Adobe Experience Platform e entidades de armazenamento relacional.</li><li>**[!DNL View orchestrated campaigns report]**: ler, editar relatórios de campanhas orquestradas.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

A função **[!DNL Orchestrated Campaign Manager]** permite que os usuários criem e editem **[!UICONTROL campanhas orquestradas]** e todos os recursos vinculados a **[!UICONTROL campanhas orquestradas]**, mas não poderão publicá-las.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: habilitar ou acessar recursos de campanha e público alimentados por IA.</li> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li>  <li>**[!DNL View operational insights]**: acesso somente leitura a insights e painéis de monitoramento no nível do sistema.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL Manage custom dashboards]**: criar, editar e excluir painéis personalizados.</li><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li></ul> |
| Painel | <ul> <li>**[!DNL Manage standard dashboard]**: ler, criar, editar e excluir widgets e esquemas de widget personalizados por meio da Biblioteca de widgets.</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL View user activity log]**: acesso somente leitura para visualizar logs de auditoria registrados de atividades do Experience Platform.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |
| Regras do Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: acesso somente leitura a regras de frequência. </li></ul> |
| Mensagens | <ul><li> **[!DNL Manage Messages]**: ler, criar, editar e excluir mensagens. </li> **[!DNL Manage Messages Preview and Test]**: aprovar e publicar mensagens quando uma política for aplicada.</li><li>**[!DNL View Messages Report]**: ler e editar relatórios de mensagens. </li></ul> |
| Campanhas orquestradas | <ul><li>**[!DNL Manage orchestrated campaigns]**: ler, criar, editar e excluir campanhas orquestradas.</li><li>**[!DNL View orchestrated campaigns report]**: ler, editar campanhas orquestradas.</li><li>**[!DNL View orchestrated campaigns admin]**: acesso somente leitura a links e reconciliações entre Perfis Adobe Experience Platform e entidades de armazenamento relacional.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

A função **[!DNL Campaign Viewer]** permite acesso somente leitura aos recursos **[!UICONTROL Campanhas orquestradas]**.

Os usuários atribuídos a esta função não poderão editar nem publicar.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: habilitar ou acessar recursos de campanha e público alimentados por IA.</li> <li>**[!DNL View operational insights]**: acesso somente leitura a insights e painéis de monitoramento no nível do sistema.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL Manage custom dashboards]**: criar, editar e excluir painéis personalizados.</li></ul> |
| Painel | <ul> <li>**[!DNL Manage standard dashboard]**: ler, criar, editar e excluir widgets e esquemas de widget personalizados por meio da Biblioteca de widgets.</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL View user activity log]**: acesso somente leitura para visualizar logs de auditoria registrados de atividades do Experience Platform.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisões.</li></ul> |
| Regras do Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: acesso somente leitura a regras de frequência.</li></ul> |
| Campanhas orquestradas | <ul><li>**[!DNL View orchestrated campaigns]**: acesso somente leitura a campanhas orquestradas.</li><li>**[!DNL View orchestrated campaigns report]**: acesso somente leitura a relatórios de campanhas orquestradas.</li></ul> |




