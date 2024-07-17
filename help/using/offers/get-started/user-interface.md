---
title: Interface do usuário da biblioteca de ofertas
description: Saiba mais sobre a interface do usuário da Biblioteca de ofertas
feature: Decision Management
topic: Integrations
role: User
level: Beginner, Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 33%

---

# Interface do usuário da biblioteca de ofertas {#user-interface}

A seção **[!UICONTROL Gestão de decisões]** no painel esquerdo fornece dois menus que dão acesso aos recursos de gestão de decisões:

Use o menu **[!UICONTROL Ofertas]** para gerenciar e entregar suas ofertas:


![](../assets/offers_menu.png)

* **[!UICONTROL Visão geral]**: novo em [!DNL decision management]? Siga as etapas na tela para começar a configurar disposições, ofertas e coleções. Quando já estiver familiarizado com o [!DNL decision management], obtenha uma visão geral sobre suas ofertas, coleções e decisões mais recentes. [Saiba mais](#overview)
* **[!UICONTROL Ofertas]**: crie e acesse suas ofertas personalizadas e substitutas. Saiba como criar [ofertas](../offer-library/creating-personalized-offers.md) e [ofertas substitutas](../offer-library/creating-fallback-offers.md)
* **[!UICONTROL Coleções]**: organize suas ofertas em coleções estáticas e dinâmicas. [Saiba mais](../offer-library/creating-collections.md)
* **[!UICONTROL Decisões]**: crie e gerencie decisões para entregar suas ofertas. [Saiba mais](../offer-activities/create-offer-activities.md)
* **[!UICONTROL Decisão em lote]**: entregar decisões de oferta a todos os perfis em um determinado público-alvo da Adobe Experience Platform. [Saiba mais](../batch-delivery.md)
* **[!UICONTROL Simulação]**: valide sua lógica de decisão simulando quais ofertas serão entregues a um perfil de teste para um determinado posicionamento. [Saiba mais](../offer-activities/simulation.md)

Use o menu **[!UICONTROL Componentes]** para criar e gerenciar componentes necessários para criar ofertas e decisões:

![](../assets/offer_activities.png)

* **[!UICONTROL Posicionamentos]**: crie e gerencie posicionamentos onde suas ofertas serão exibidas. [Saiba mais](../offer-library/creating-placements.md)
* **[!UICONTROL Qualificadores de coleção]**: crie e gerencie qualificadores de coleção (anteriormente conhecidos como &quot;marcas&quot;) para organizar e filtrar suas ofertas. [Saiba mais](../offer-library/creating-tags.md)
* **[!UICONTROL Regras]**: gerencie as condições em que suas ofertas são apresentadas. [Saiba mais](../offer-library/creating-decision-rules.md)
* **[!UICONTROL Classificação]**: crie e gerencie fórmulas de classificação para determinar qual oferta deve ser apresentada primeiro para um determinado posicionamento. [Saiba mais](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>Se tiver problemas ao acessar a gestão de decisões ou alguns de seus recursos, verifique com um usuário Administrador se você recebeu os direitos necessários. Consulte [Conceder acesso à Gestão de Decisões](starting-offer-decisioning.md#granting-acess-to-decision-management).

## Visão geral {#overview}

Quando você é novo no [!DNL decision management], a guia **[!UICONTROL Visão geral]** o orienta pelas etapas principais necessárias para começar a criar sua primeira decisão de oferta. Siga as etapas na tela para começar a criar inserções, ofertas e coleções. Quando terminar com essas primeiras etapas, você será solicitado a criar decisões de oferta.

>[!NOTE]
>
>As principais etapas para criar ofertas e usá-las em uma decisão são apresentadas em [esta seção](../offer-library/key-steps.md).

Quando você estiver mais familiarizado com o [!DNL decision management] e já tiver criado pelo menos uma decisão de oferta, a guia **[!UICONTROL Visão geral]** exibirá as ofertas, as coleções e as decisões mais recentes.

Clique em uma oferta ou em uma decisão para acessar diretamente os detalhes do item selecionado.

Clique no botão **[!UICONTROL Exibir todos]** para acessar as listas de oferta, coleção ou decisão.

![](../assets/overview_view-all.png)

## Pesquisar e filtrar informações {#search-and-filter-information}

Use a **barra de pesquisa** para localizar um item específico.

**Filtros** também podem ser acessados clicando no ícone de filtro no canto superior esquerdo da lista. Eles permitem filtrar os elementos exibidos de acordo com diferentes critérios. Você pode, por exemplo, filtrar as inserções que foram criadas para o canal de comunicação por email e o conteúdo do tipo imagem.

![](../assets/filters.png)

## Personalizar informações exibidas {#customize-displayed-information}

As listas dos menus do Gerenciamento de decisão podem ser personalizadas usando o botão de configuração na parte superior direita das listas.

Essa personalização permite escolher as informações que serão exibidas de acordo com suas necessidades.

Observe que a personalização de colunas é salva para cada usuário.

![](../assets/columns.png)

## Painel de informações {#information-pane}

Nas diferentes listas, selecione um elemento para exibir um painel de informações que permitirá recuperar informações e executar ações básicas no elemento.

![](../assets/information-pane.png)

As listas de ofertas e decisões agora permitem executar ações em massa em vários elementos. Para fazer isso, selecione as ofertas ou decisões desejadas e selecione a ação que deseja executar no painel de informações.

Observe que você também pode duplicar uma oferta existente ou decisões para criar uma cópia com o status **[!UICONTROL Rascunho]**. Isso pode ser executado no painel de informações ou em uma oferta ou na visualização detalhada de uma decisão.

## Registros de alteração de ofertas e decisões {#changes-logs}

[!DNL Journey Optimizer] permite visualizar todas as alterações feitas em uma oferta ou em uma decisão. Para fazer isso, acesse o menu **[!UICONTROL Auditorias]** no menu esquerdo. [Saiba como auditar ações em recursos](../../privacy/audit-logs.md)
