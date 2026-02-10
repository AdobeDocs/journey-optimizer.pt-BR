---
title: Introdução ao serviço de decisão
description: Saiba mais sobre decisão
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
source-git-commit: 741b39a7588ae4e1161891226d95609508b00031
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 21%

---

# Introdução ao serviço de decisão {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="O que é o serviço de decisão?"
>abstract="O serviço de decisão é um novo conjunto de ferramentas semelhante à gestão de decisões que seleciona os melhores itens do mecanismo de decisão para entregar a cada pessoa. Ele exige configuração adicional para ser usado."

## O que é a decisão {#about}

O serviço de decisão simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.

Estes itens de decisão são perfeitamente integrados em mensagens e experiências em [!DNL Adobe Journey Optimizer] canais: [experiência baseada em código](../code-based/get-started-code-based.md), email, SMS e notificações por push.

>[!IMPORTANT]
>
>As políticas de decisão estão disponíveis a todos os clientes para os canais **Experiência baseada em código**, **Notificação por push** e **SMS**. A decisão do canal **Email** está disponível somente em Disponibilidade Limitada. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

➡️ [Conheça este recurso no vídeo](#video)

➡️ Um caso de uso completo que mostra como criar decisões e usá-las em experimentos de conteúdo com o canal de experiência baseado em código é apresentado em [esta seção](experience-decisioning-uc.md).

## Principais etapas da decisão {#steps}

As principais etapas para trabalhar com a Decisão são as seguintes:

1. **Atribuir permissões apropriadas**. A decisão está disponível somente para usuários com acesso a uma **[!UICONTROL função]** relacionada à decisão, como Gerentes de decisão. Se não conseguir acessar o Decisioning, suas permissões deverão ser estendidas.

   +++Saiba como atribuir a função Gerentes de decisão

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

   ➡️ [Saiba como criar itens de decisão](items.md) na interface do usuário (e na [documentação sobre APIs](api-reference/decisions-items/create.md))

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções nas estratégias de seleção para determinar qual coleção de itens de decisão deve ser considerada.

   ➡️ [Saiba como gerenciar coleções de itens](collections.md) na interface do usuário (e na [documentação da API](api-reference/items-collections/create.md))

1. **Criar regras de decisão**: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser mostrado.

   ➡️ [Saiba como criar regras de decisão](rules.md)

1. **Implementar métodos de classificação**: crie métodos de classificação e aplique-os nas estratégias de seleção para determinar a ordem de prioridade para selecionar itens de decisão.

   ➡️ [Saiba como criar métodos de classificação](ranking/ranking.md)

1. **Criar estratégias de seleção**: crie estratégias de seleção que aproveitem coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis.

   ➡️ [Saiba como criar estratégias de seleção na interface do usuário](selection-strategies.md) na interface do usuário (e na [documentação da API](api-reference/selection-strategies/create.md))

1. **Crie uma política de decisão e incorpore-a à sua jornada ou campanha** (experiência baseada em código, email, SMS ou push): as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão qualificados a serem exibidos para o público-alvo desejado.

   ➡️ [Saiba como trabalhar com políticas de decisão](create-decision.md)
➡️ Para entregar com êxito a oferta por meio do canal de experiência baseado em código, siga as etapas de implementação em [esta seção](../code-based/code-based-implementation-samples.md).

## Recursos adicionais

* **[Criar itens de decisão](items.md)** - Saiba como criar e gerenciar itens de decisão, incluindo ofertas, variações de conteúdo e experiências.
* **[Configurar catálogos de decisão](catalogs.md)** - Entenda como organizar itens de decisão em catálogos para melhorar o gerenciamento.
* **[Definir estratégias de seleção](selection-strategies.md)** - Descubra como criar estratégias de seleção com regras de qualificação e métodos de classificação.
* **[Criar políticas de decisão](create-decision-policy.md)** - Saiba como criar políticas de decisão que combinam estratégias e restrições.
* **[Modelos de classificação e IA](ranking/ranking.md)** - Fórmulas de classificação mestre e modelos de IA para decisões personalizadas.
* **[Migrar da Gestão de decisões](migrate-to-decisioning.md)** - Entenda os benefícios da migração para o Decisioning e use APIs de ferramentas de migração.
* **[Medidas de proteção de decisão](decisioning-guardrails.md)** - Revise limitações importantes e práticas recomendadas para a implementação da decisão.
* **[Tutoriais de decisão](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}** - Explore tutoriais em vídeo passo a passo sobre recursos de decisão e práticas recomendadas.

## Vídeo tutorial {#video}

Saiba mais sobre os recursos de decisão no Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3451101?quality=12)
