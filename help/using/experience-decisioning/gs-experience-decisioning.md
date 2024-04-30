---
title: Introdução ao Experience Decisioning
description: Saiba mais sobre o Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: f71795c99157ce43f5250aaf10eb0b97f235b454
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 23%

---

# Introdução ao Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX &quot;O que você encontrará neste guia de documentação&quot;]

* **[Introdução ao Experience Decisioning](gs-experience-decisioning.md)**
* Gerencie seus itens de decisão: [Configurar o catálogo de itens](catalogs.md) - [Criar itens de decisão](items.md) - [Gerenciar coleções de itens](collections.md)
* Configurar a seleção dos itens: [Criar regras de decisão](rules.md) - [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

## O que é o Experience Decisioning {#about}

>[!AVAILABILITY]
>
>O recurso de decisão de experiência está disponível atualmente como um beta apenas para usuários selecionados. Para participar do programa beta, entre em contato com o atendimento ao cliente da Adobe.
>
>As políticas de decisão estão disponíveis para uso somente em campanhas de experiência baseadas em código.

A Escolha de experiências simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.

Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer.

## Principais etapas do Experience Decisioning {#steps}

As principais etapas para trabalhar com o Experience Decisioning são as seguintes:

1. **Atribuir permissões apropriadas**. As decisões só estão disponíveis para usuários com acesso a uma experiência relacionada ao Experience Decisioning **[!UICONTROL função]** como os Gerentes de decisão. Se não conseguir acessar as decisões, suas permissões deverão ser estendidas.

   +++Saiba como atribuir a função de Gerentes de decisão

   1. Para atribuir uma função a um usuário na [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e selecione Gerenciadores de decisão.

      ![](assets/decision_permission_1.png)

   1. No **[!UICONTROL Usuários]** clique em **[!UICONTROL Adicionar usuário]**.

      ![](assets/decision_permission_2.png)

   1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

      Se o usuário não tiver sido criado anteriormente, consulte a [Adicionar documentação de usuários](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   O usuário deve receber um email de redirecionamento para sua instância.

+++

1. **Configurar atributos personalizados**: personalize o catálogo dos itens de decisão de acordo com suas necessidades específicas, configurando atributos personalizados no esquema do catálogo.

1. **Criar itens de decisão** para mostrar ao público-alvo direcionado.

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções nas estratégias de seleção para determinar qual coleção de itens de decisão deve ser considerada.

1. **Criar regras de decisão**: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser mostrado.

1. **Implementar métodos de classificação**: crie métodos de classificação e aplique-os nas estratégias de decisão para determinar a ordem de prioridade para selecionar itens de decisão.

1. **Criar estratégias de seleção**: crie estratégias de seleção que aproveitam coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis.

1. **Incorpore uma política de decisão à sua campanha baseada em código**: as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão qualificados a serem exibidos para o público-alvo desejado.
