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
source-git-commit: ee2e07353762a81aadd3d63580c528f617599623
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# Funções integradas {#ootb-product-profiles}

As funções integradas são um conjunto de direitos unitários que permitem aos usuários acessar determinadas funcionalidades ou objetos na interface. Consulte [esta página](ootb-permissions.md) para obter a lista de permissões disponíveis para criar sua função.

## [!DNL Content Library Manager] {#content-library-manager}

A função **[!DNL Content Library Manager]** permite acesso apenas ao menu **[!UICONTROL Modelos de conteúdo]**. Os usuários atribuídos a essa função só poderão acessar a biblioteca de modelos para criar conteúdo sem acessar as jornadas ou campanhas.

Essa função inclui as seguintes permissões:

| Recurso | Permissões |
|-|-|
| Biblioteca da Journey Optimizer | <ul><li>**[!DNL Manage library items]**: ler, criar, editar e excluir itens da Biblioteca Journey Optimizer, incluindo modelos de conteúdo e fragmentos.</li><li>**[!DNL Manage simulate content]**: acesso à opção **[!UICONTROL Simular conteúdo]** para visualização e prova.</li><li>**[!DNL Publish Fragment]**: publicar fragmentos de conteúdo.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

A função **[!DNL Decisioning manager]** permite acesso apenas ao menu **[!UICONTROL Gerenciamento de decisão]**. Os usuários atribuídos a essa função só poderão gerenciar, exibir e publicar decisões.

Essa função inclui as seguintes permissões:

| Recurso | Permissões |
|-|-|
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisão.</li><li>**[!DNL Publish decisions]**: ativar ou desativar atividades de decisão.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

A função **[!DNL Campaign Administrator]** permite que os menus de administração com a possibilidade de gerenciar e publicar Campanhas e Gestão de decisões.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Campanhas | <ul><li> **[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publicar campanhas.</li><li>**[!DNL View campaigns report]**: leia e edite o relatório de campanhas.</li></ul> |
| Configurações de canal | <ul> <li>**[!DNL Export suppression list]**: acesso à lista de supressão de exportação como arquivo CSV.</li> <li>**[!DNL Manage alerts]**: habilitar/desabilitar alertas para campanhas, mensagens e direitos.</li> <li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir pool de IPs.</li> <li>**[!DNL Manage landing page settings]**: ler, criar, editar e excluir configurações da página de aterrissagem.</li> <li>**[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li> <li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir a identidade visual do conteúdo.</li> <li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: ler, criar, editar e excluir configurações de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir a delegação de subdomínio.</li> <li>**[!DNL Manage suppression rules]**: acessar as regras de supressão de leitura, criação, edição e exclusão.</li> <li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li> <li>**[!DNL View suppression list]**: ler e exportar a lista de supressão local.</li> </ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acesso a sandboxes.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

A função **[!DNL Campaign Approver]** permite que os usuários aprovem entregas e as publiquem. Mais tarde, eles poderão verificar o sucesso de suas entregas com os relatórios **[!DNL Campaigns]**.

| Recursos | Permissões |
|-|-|
| Campanhas | <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publicar campanhas.</li><li>**[!DNL View campaigns report]**: ler, editar relatórios de campanha.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

A função **[!DNL Campaign Manager]** permite que os usuários criem e editem **[!UICONTROL Campanhas]** e todos os recursos vinculados a **[!UICONTROL Campanhas]**, mas não poderão publicá-las.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Campanhas | <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL View campaigns report]**: ler, editar relatório de jornada.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizadas e usar recursos de ação.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View messages presets]**: acesso somente leitura a predefinições de mensagens.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

A função **[!DNL Campaign Viewer]** permite acesso somente leitura aos recursos **[!UICONTROL Campanhas]** e **[!UICONTROL Gerenciamento de decisão]**.

Os usuários atribuídos a esta função não poderão editar nem publicar.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Campanhas | <ul><li>**[!DNL View campaigns]**: acesso somente leitura a campanhas.</li><li>**[!DNL View campaigns report]**: acesso somente leitura aos relatórios de campanhas.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisões.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

A função **[!DNL Journey Administrator]** permite que os menus de administração com a possibilidade de gerenciar e publicar Jornadas e Gestão de decisões.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Jornadas | <ul> <li>**[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li> <li>**[!DNL Manage journeys events, data sources and actions]**: ler, criar, editar e excluir eventos, fontes ou ações.</li> <li>**[!DNL Publish journeys]**: publicar jornadas.</li> <li>**[!DNL View journeys report]**: ler e editar o relatório de jornadas.</li> </ul> |
| Configurações de canal | <ul> <li>**[!DNL Manage alerts]**: habilitar/desabilitar alertas para jornadas e direitos.</li> <li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir pool de IPs.</li> <li>**[!DNL Manage Landing page settings]**: criar, editar e excluir subdomínios e predefinições de página de aterrissagem.</li> <li>**[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li> <li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir a identidade visual do conteúdo.</li> <li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: criar, editar e excluir credenciais de API e configurações de canal de SMS necessárias para habilitar o canal de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir a delegação de subdomínio.</li> <li>**[!DNL Manage suppression rules]**: acessar as regras de supressão de leitura, criação, edição e exclusão.</li> <li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li> <li>**[!DNL View suppression list]**: ler e exportar a lista de supressão local.</li> </ul> |
| Gestão de decisões | <ul> <li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li> <li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li> <li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li> <li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li> <li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li> <li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li> <li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acesso a sandboxes.</li> </ul> |
| Biblioteca da Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]**: adicionar e excluir expressões salvas na Biblioteca [!DNL Journey Optimizer].</li> </ul> |
| Governança de dados | <ul> <li>**[!DNL Manage data usage policies]**: ler, criar, editar e excluir políticas de uso de dados.</li> <li>**[!DNL Manage usage label]**: ler, criar e excluir rótulos de uso.</li> <li>**[!DNL View data usage policies]**: acesso somente leitura a políticas de uso de dados.</li> <li>**[!DNL View user activity log]**: ler e exportar logs de auditoria.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

A função **[!DNL Journey Approver]** permite que os usuários aprovem entregas e as publiquem. Mais tarde, eles poderão verificar o sucesso de suas entregas com os relatórios **[!DNL Journey]**.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Jornadas | <ul><li>**[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li><li>**[!DNL Publish journey]**: publicar jornadas.</li><li>**[!DNL View journeys events, data sources and actions]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatórios de jornada.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View channel configurations]**: acesso somente leitura às configurações de canal.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

A função **[!DNL Journey Manager]** permite que os usuários criem e editem **[!UICONTROL Jornadas]** e todos os recursos vinculados a **[!UICONTROL Jornadas]**, mas não poderão publicá-los.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Jornadas | <ul><li>**[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li><li>**[!DNL View journeys events]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatório de jornada.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li> **[!DNL Manage segments]**: ler, criar, editar e excluir definições de segmento.</li><li>**[!DNL View datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL View schemas]**: acesso somente leitura a esquemas.</li></ul> |
| Configurações de canal | <ul><li>**[!DNL View channel configurations]**: acesso somente leitura às configurações de canal.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

A função **[!DNL Journey viewer]** permite acesso somente leitura aos recursos do **[!UICONTROL Jornada]** e do **[!UICONTROL Gerenciamento de decisão]**.

Os usuários atribuídos a esta função não poderão editar nem publicar.

Essa função inclui as seguintes permissões:

| Recursos | Permissões |
|-|-|
| Jornadas | <ul><li>**[!DNL View journeys]**: acesso somente leitura a jornadas.</li><li>**[!DNL View journeys event, data sources, actions]**: acesso somente leitura a eventos e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: acesso somente leitura a relatórios do jornada.</li></ul> |
| Gestão de decisões | <ul><li>**[!DNL View decisions]**: acesso somente leitura a entidades de decisões.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Orchestrated Campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: read, create, edit, and delete custom dashboards.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: Read, create, edit and delete links and reconciliations between Adobe Experience Platform Profiles and Relational store entities.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL View sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to publish Orchestrated campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaign reports.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li> </ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Orchestrated campaigns]** and every capability linked to **[!UICONTROL Orchestrated campaigns]** but will not be able to publish them.

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Orchestrated campaigns]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Messages|<ul><li>**[!DNL View messages]**: view messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

-->