---
title: Introdução ao serviço de decisão
description: Saiba mais sobre Decisões
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 4839c3c70dcc524da5f3cc394d5573ce5755ea64
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 23%

---

# Introdução ao serviço de decisão {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="O que é o serviço de decisão?"
>abstract="O serviço de decisão é um novo conjunto de ferramentas semelhante à gestão de decisões que seleciona os melhores itens do mecanismo de decisão para entregar a cada pessoa. Ele exige configuração adicional para ser usado."

## O que é a decisão {#about}

O serviço de Decisão simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de escolha sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.

Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada através do [novo canal de experiência baseado em código](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), agora acessível em campanhas do Journey Optimizer.

>[!IMPORTANT]
>
>As políticas de decisão estão disponíveis para uso em campanhas de experiência baseadas em código somente.

➡️ Um caso de uso completo que mostra como criar decisões e usá-las em experimentos de conteúdo com o canal de experiência baseado em código é apresentado em [esta seção](experience-decisioning-uc.md).

## Principais etapas da decisão {#steps}

As principais etapas para trabalhar com a Decisão são as seguintes:

1. **Atribuir permissões apropriadas**. A decisão está disponível somente para usuários com acesso a uma **[!UICONTROL função]** relacionada à decisão, como Gerentes de decisão. Se não conseguir acessar o Decisioning, suas permissões deverão ser estendidas.

   +++Saiba como atribuir a função de Gerentes de decisão

   1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e selecione Gerenciadores de decisão.

      ![](assets/decision_permission_1.png)

   1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

      ![](assets/decision_permission_2.png)

   1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

      Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   O usuário deve receber um email de redirecionamento para sua instância.

   +++

1. **Configurar atributos personalizados**: adapte o catálogo de itens aos seus requisitos específicos, configurando atributos personalizados no esquema do catálogo.

   ➡️ [Saiba como configurar o catálogo de itens](catalogs.md)

1. **Crie itens de decisão** para mostrar ao seu público-alvo direcionado.

   ➡️ [Saiba como criar itens de decisão](items.md) na interface do usuário (e na [Documentação de API](api-reference/decisions-items/create.md))

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções nas estratégias de seleção para determinar qual coleção de itens de decisão deve ser considerada.

   ➡️ [Saiba como gerenciar coleções de itens](collections.md) na interface do usuário (e na [documentação da API](api-reference/items-collections/create.md))

1. **Criar regras de decisão**: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser mostrado.

   ➡️ [Saiba como criar regras de decisão](rules.md)

1. **Implementar métodos de classificação**: crie métodos de classificação e aplique-os nas estratégias de seleção para determinar a ordem de prioridade para selecionar itens de decisão.

   ➡️ [Saiba como criar métodos de classificação](ranking.md)

1. **Criar estratégias de seleção**: crie estratégias de seleção que aproveitem coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis.

   ➡️ [Saiba como criar estratégias de seleção na interface do usuário](selection-strategies.md) na interface do usuário (e na [Documentação da API](api-reference/selection-strategies/create.md))

1. **Crie uma política de decisão e incorpore-a à sua campanha baseada em código**: as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão qualificados a serem exibidos para o público-alvo desejado.

   ➡️ [Saiba como trabalhar com políticas de decisão](create-decision.md)
➡️ Para fornecer a oferta com êxito por meio do canal de experiência baseado em código, siga as etapas de implementação em [esta seção](../code-based/code-based-implementation-samples.md).

Um caso de uso completo que mostra como usar decisões em uma experiência baseada em código é apresentado em [esta seção](experience-decisioning-uc.md).
