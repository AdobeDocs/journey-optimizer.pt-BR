---
title: Interface do usuário
description: Saiba mais sobre a interface do usuário da Biblioteca de ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 37%

---

# Interface do usuário {#user-interface}

O **[!UICONTROL Gestão de decisões]** no painel esquerdo fornece dois menus que fornecem acesso aos recursos de gerenciamento de decisões:

Use o **[!UICONTROL Ofertas]** para gerenciar e entregar suas ofertas:


![](../assets/offers_menu.png)

* **[!UICONTROL Visão geral]**: Novo em [!DNL decision management]? Siga as etapas na tela para começar a configurar disposições, ofertas e coleções. Quando já estiver familiarizado com [!DNL decision management], obtenha uma visão geral sobre as ofertas, coleções e decisões mais recentes. [Saiba mais](#overview)
* **[!UICONTROL Ofertas]**: Crie e acesse suas ofertas personalizadas e de fallback. Saiba como criar [ofertas](../offer-library/creating-personalized-offers.md) e [ofertas de fallback](../offer-library/creating-fallback-offers.md)
* **[!UICONTROL Coleções]**: Organize suas ofertas em coleções estáticas e dinâmicas. [Saiba mais](../offer-library/creating-collections.md)
* **[!UICONTROL Decisões]**: Crie e gerencie decisões para fornecer suas ofertas. [Saiba mais](../offer-activities/create-offer-activities.md)
* **[!UICONTROL Decisão em lote]**: Entregar decisões de oferta a todos os perfis em um determinado segmento do Adobe Experience Platform. [Saiba mais](../batch-delivery.md)
* **[!UICONTROL Simulação]**: Valide a lógica de decisão simulando quais ofertas serão entregues a um perfil de teste para uma determinada disposição. [Saiba mais](../offer-activities/simulation.md)

Use o **[!UICONTROL Componentes]** para criar e gerenciar os componentes necessários para criar ofertas e decisões:

![](../assets/offer_activities.png)

* **[!UICONTROL Posicionamentos]**: Crie e gerencie disposições onde suas ofertas serão exibidas. [Saiba mais](../offer-library/creating-placements.md)
* **[!UICONTROL Qualificadores de coleção]**: Crie e gerencie os qualificadores de coleta (anteriormente conhecidos como &quot;tags&quot;) para organizar e filtrar suas ofertas. [Saiba mais](../offer-library/creating-tags.md)
* **[!UICONTROL Regras]**: Gerencie as condições em que suas ofertas são apresentadas. [Saiba mais](../offer-library/creating-decision-rules.md)
* **[!UICONTROL Classificação]**: Crie e gerencie fórmulas de classificação para determinar qual oferta deve ser apresentada primeiro para uma determinada disposição. [Saiba mais](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>Se tiver problemas ao acessar o gerenciamento de decisões ou alguns de seus recursos, verifique com um usuário administrador se você recebeu os direitos necessários. Consulte [Conceder acesso ao gerenciamento de decisões](starting-offer-decisioning.md#granting-acess-to-decision-management).

## Visão geral {#overview}

Quando você é novo no [!DNL decision management], o **[!UICONTROL Visão geral]** guia você pelas principais etapas necessárias para começar a criar sua primeira decisão de oferta. Siga as etapas na tela para começar a criar disposições, ofertas e coleções. Depois de concluir essas primeiras etapas, você será solicitado a criar decisões de oferta.

>[!NOTE]
>
>As principais etapas para criar ofertas e usá-las em uma decisão são apresentadas em [esta seção](../offer-library/key-steps.md).

Quando você estiver mais familiarizado com o [!DNL decision management] e você já criou pelo menos uma decisão de oferta, a **[!UICONTROL Visão geral]** exibe suas ofertas, coleções e decisões mais recentes.

Clique em uma oferta ou em uma decisão para acessar diretamente os detalhes do item selecionado.

Clique no botão **[!UICONTROL Exibir tudo]** para acessar as listas de oferta, coleção ou decisão.

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

Observe que você também pode duplicar uma oferta existente ou decisões para criar uma cópia com a **[!UICONTROL Rascunho]** status. Isso pode ser executado no painel de informações ou em uma oferta ou na visualização detalhada de uma decisão.

## Registros de alteração de ofertas e decisões {#changes-logs}

A Biblioteca de ofertas permite visualizar todas as alterações feitas em uma oferta ou decisão. Para fazer isso, abra a oferta ou a decisão clicando no nome na lista e selecione o **[!UICONTROL Log de alterações]** guia .

Todas as alterações feitas são exibidas nessa tela, bem como no nome do usuário que executou as alterações.

![](../assets/change-logs.png)
