---
solution: Journey Optimizer
product: journey optimizer
title: Perfis de produto incorporados
description: Saiba mais sobre os perfis de produto integrados
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: permissões, criação, mensagens
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 10%

---

# Perfis de produto incorporados {#ootb-product-profiles}

## [!DNL Campaign Administrator] {#campaign-administrator}

O **[!DNL Campaign Administrator]** O perfil de produto permite que os menus de administração tenham a possibilidade de gerenciar e publicar campanhas e o gerenciamento de decisões.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Campanhas| <ul><li> **[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publique campanhas.</li><li>**[!DNL View campaigns report]**: ler e editar relatório de campanhas.</li></ul>|
|Administração|<ul><li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir delegação de subdomínio.</li><li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir o pool ip.</li><li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li><li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li><li> **[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li><li>**[!DNL Manage messages presets]**: ler, criar, editar e excluir marcas de conteúdo.</li><li>**[!DNL Manage suppression rules]**: acesse ler, criar, editar e excluir regras de supressão.</li><li>**[!DNL Export suppression list]**: acesso à lista de supressão de exportação como um arquivo CSV.</li><li>**[!DNL View suppression list]**: ler e exportar lista de supressão local.</li><li>**[!DNL Manage alerts]**: ativar/desativar alertas para campanhas, mensagens e direitos.</li><li>**[!DNL Manage landing page settings]**: ler, criar, editar e excluir configurações de página de aterrissagem.</li><li>**[!DNL Manage SMS settings]**: ler, criar, editar e excluir configurações de SMS.</li></ul>|
|Gerenciamento de decisão|<ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: conceda acesso a sandboxes.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

O **[!DNL Campaign Approver]** o perfil de produto permite que os usuários aprovem os deliveries e os publiquem. Eles podem verificar posteriormente o sucesso de seus deliveries com a variável **[!DNL Campaigns]** relatórios.

| Capacidade | Permissões| |-|-| |Campanhas| <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL Publish campaigns]**: publique campanhas.</li><li>**[!DNL View Campaigns report]**: ler, editar relatórios de jornada.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizados e usar recursos de ação.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>|
|Administração| <ul><li>**[!DNL View messages presets]**: acesso somente leitura às predefinições de mensagens.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

O **[!DNL Campaign Manager]** o perfil de produto permite que os usuários criem e editem **[!UICONTROL Campanhas]** e todos os recursos vinculados a **[!UICONTROL Campanhas]** mas não poderá publicá-las.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Campanhas| <ul><li>**[!DNL Manage campaigns]**: ler, criar, editar e excluir campanhas.</li><li>**[!DNL View campaigns report]**: ler, editar relatório de jornada.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios de mensagens personalizados e usar recursos de ação.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>|
|Administração| <ul><li>**[!DNL View messages presets]**: acesso somente leitura às predefinições de mensagens.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

O **[!DNL Campaign Viewer]** o perfil do produto permite acesso somente leitura ao **[!UICONTROL Campanhas]** e **[!UICONTROL Gestão de decisões]** recursos.

Os usuários atribuídos a este perfil de produto não poderão editar ou publicar.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Campanhas| <ul><li>**[!DNL View campaigns]**: acesso somente leitura a campanhas.</li><li>**[!DNL View campaigns report]**: acesso somente leitura aos relatórios de campanhas.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL View decisions]**: acesso somente leitura às entidades de decisão.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

O **[!DNL Journey Administrator]** O perfil de produto permite que os menus de administração tenham a possibilidade de gerenciar e publicar Jornadas e o gerenciamento de decisões.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Jornadas| <ul><li> **[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li><li>**[!DNL Publish journeys]**: publicar jornadas.</li><li>**[!DNL Manage journeys events, data sources and actions]**: ler, criar, editar e excluir eventos, fontes ou ações.</li><li>**[!DNL View journeys report]**: leia e edite o relatório do jornada.</li></ul>|
|Administração|<ul><li>**[!DNL Manage subdomains delegation]**: ler, criar, editar e excluir delegação de subdomínio.</li><li>**[!DNL Manage IP pools]**: ler, criar, editar e excluir o pool ip.</li><li>**[!DNL Manage PTR records]**: ler e editar registros PTR.</li><li>**[!DNL View PTR records]**: acesso somente leitura a registros PTR.</li><li>**[!DNL Manage channel surfaces]**: ler, criar, editar e excluir marcas de conteúdo.</li><li>**[!DNL Manage Landing page settings]**: crie, edite e exclua subdomínios de página de aterrissagem e predefinições de página de aterrissagem.</li><li> **[!DNL Manage messages general settings]**: ler, criar, editar e excluir configurações gerais de mensagens.</li><li>**[!DNL Manage SMS settings]**: crie, edite e exclua as credenciais da API e as superfícies do canal SMS necessárias para habilitar o canal SMS.</li><li>**[!DNL Manage suppression rules]**: acesse ler, criar, editar e excluir regras de supressão.</li><li>**[!DNL View suppression list]**: ler e exportar lista de supressão local.</li><li>**[!DNL Manage alerts]**: ativar/desativar alertas para jornadas e direitos.</li></ul>|
|Gerenciamento de decisão|<ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir decisões.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir estratégias de classificação.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: conceda acesso a sandboxes.</li><li>**[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Read Identity namespace]**: acesso somente leitura ao namespace de identidade.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>| |Biblioteca da Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: adicionar e excluir expressões salvas na [!DNL Journey Optimizer] Biblioteca.</li></ul>|
|Governança de dados|<ul><li>**[!DNL Manage usage label]**: ler, criar e excluir rótulos de uso.</li><li>**[!DNL Manage data usage policies]**: ler, criar, editar e excluir políticas de uso de dados.</li><li>**[!DNL View data usage policies]**: acesso somente leitura às políticas de uso de dados.</li><li>**[!DNL View user activity log]**: ler e exportar logs de auditoria.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

O **[!DNL Journey Approver]** o perfil de produto permite que os usuários aprovem os deliveries e os publiquem. Eles podem verificar posteriormente o sucesso de seus deliveries com a variável **[!DNL Journey]** relatórios.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Jornadas| <ul><li>**[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li><li>**[!DNL Publish journey]**: publicar jornadas.</li><li>**[!DNL View journeys events, data sources and actions]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatórios de jornada.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>|
|Administração| <ul><li>**[!DNL View channel surfaces]**: acesso somente leitura às superfícies do canal.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

O **[!DNL Journey Manager]** o perfil de produto permite que os usuários criem e editem **[!UICONTROL Jornada]** e todos os recursos vinculados a **[!UICONTROL Jornada]** mas não poderá publicá-las.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Jornadas| <ul><li>**[!DNL Manage journeys]**: ler, criar, editar e excluir jornadas.</li><li>**[!DNL View journeys events]**: acesso somente leitura a eventos do jornada, ações personalizadas do jornada e fontes de dados do jornada.</li><li>**[!DNL View journeys report]**: ler, editar relatório de jornada.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: ler, criar, editar e excluir segmentos.</li><li>**[!DNL Manage profiles]**: ler, criar, editar e excluir perfis.</li><li>**[!DNL Read datasets]**: acesso somente leitura a conjuntos de dados.</li><li>**[!DNL Read schemas]**: acesso somente leitura a schemas.</li><li>**[!DNL Manage merge policies]**: ler, criar, editar e excluir políticas de mesclagem.</li></ul>|
|Administração| <ul><li>**[!DNL View channel surfaces]**: acesso somente leitura às superfícies do canal.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

O **[!DNL Journey viewer]** o perfil do produto permite acesso somente leitura ao **[!UICONTROL Jornada]** e **[!UICONTROL Gestão de decisões]** recursos.

Os usuários atribuídos a este perfil de produto não poderão editar ou publicar.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Jornadas| <ul><li>**[!DNL View journeys]**: acesso somente leitura ao jornada.</li><li>**[!DNL View journeys event, data sources, actions]**: acesso somente leitura a eventos do jornada e fontes de dados.</li><li>**[!DNL View journeys report]**: acesso somente leitura aos relatórios do jornada.</li></ul>|
|Gerenciamento de decisão| <ul><li>**[!DNL View decisions]**: acesso somente leitura às entidades de decisão.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

O **[!DNL Decisioning manager]** o perfil de produto permite somente a **[!UICONTROL Gestão de decisões]** menu. Os usuários atribuídos a este perfil de produto só poderão gerenciar, visualizar e publicar decisões.

Este perfil de produto conta com as seguintes permissões:

| Capacidade | Permissões| |-|-| |Gestão das decisões| <ul><li>**[!DNL Manage decisions]**: ler, criar, editar e excluir entidades de decisão.</li><li>**[!DNL View decisions]**: acesso somente leitura às entidades de decisão.</li><li>**[!DNL Manage ranking strategies]**: ler, criar, editar e excluir relatórios personalizados e usar recursos de ação.</li><li>**[!DNL Publish decisions]**: ativar ou desativar atividades de decisão.</li></ul>|
