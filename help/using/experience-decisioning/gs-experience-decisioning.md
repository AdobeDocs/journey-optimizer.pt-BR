---
title: Introdução ao serviço de Decisão
description: Saiba mais sobre Decisões
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: cb6b73db76c710dd8e736e710f5eb758337be696
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 16%

---

# Introdução ao serviço de Decisão {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="O que é a tomada de decisão?"
>abstract="A decisão é uma nova ferramenta, além da Gestão de decisões, para escolher os melhores itens do mecanismo de decisão e entregá-los a cada indivíduo. Ela requer configuração adicional para ser usada."

## O que é a decisão {#about}

O serviço de Decisão simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de escolha sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.

Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada através do [novo canal de experiência baseado em código](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), agora acessível em campanhas do Journey Optimizer. As políticas de decisão estão disponíveis para uso em campanhas de experiência baseadas em código somente.

## Medidas de proteção e limitações {#guardrails}

Para garantir o uso ideal do Decisioning, lembre-se das seguintes medidas de proteção e limitações:

### Medidas de proteção gerais {#general}

* **Itens de oferta**: cada coleção de itens pode conter até 500 itens de oferta.
* **Atributos personalizados**: um item de decisão pode incluir no máximo 100 atributos personalizados.
* **Estratégias de seleção e itens de decisão por política**: uma política de decisão suporta até 10 estratégias de seleção e itens de decisão combinados.

### Regras de elegibilidade {#eligibility}

* **Níveis de aninhamento**: a profundidade do aninhamento é limitada a 30 níveis. Isso é medido pela contagem dos parênteses de fechamento `)` na cadeia de caracteres do PQL.
* **Tamanho da cadeia de caracteres de regra**: uma cadeia de caracteres de regra pode ter até 15 KB de tamanho para caracteres codificados em UTF-8. É equivalente a 15.000 caracteres ASCII (1 byte cada) ou 3.750-7.500 caracteres não ASCII (2-4 bytes cada).

### Fórmulas de classificação {#ranking}

* **Níveis de aninhamento**: a profundidade do aninhamento é limitada a 30 níveis. Isso é medido pela contagem dos parênteses de fechamento `)` na cadeia de caracteres do PQL.
* **Tamanho da cadeia de caracteres de fórmula**: uma cadeia de caracteres de regra pode ter até 8 KB de tamanho para caracteres codificados em UTF-8. É equivalente a 8.000 caracteres ASCII (1 byte cada) ou 2.000-4.000 caracteres não ASCII (2-4 bytes cada).

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

   ➡️ [Saiba como criar itens de decisão](items.md) ([Documentação de API](api-reference/decisions-items/create.md))

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções nas estratégias de seleção para determinar qual coleção de itens de decisão deve ser considerada.

   ➡️ [Saiba como gerenciar coleções de itens](collections.md) ([Documentação de API](api-reference/items-collections/create.md))

1. **Criar regras de decisão**: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser mostrado.

   ➡️ [Saiba como criar regras de decisão](rules.md)

1. **Implementar métodos de classificação**: crie métodos de classificação e aplique-os nas estratégias de decisão para determinar a ordem de prioridade para selecionar itens de decisão.

   ➡️ [Saiba como criar métodos de classificação](ranking.md)

1. **Criar estratégias de seleção**: crie estratégias de seleção que aproveitem coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis.

   ➡️ [Saiba como criar estratégias de seleção](selection-strategies.md) ([Documentação da API](api-reference/selection-strategies/create.md))

1. **Crie uma política de decisão e incorpore-a à sua campanha baseada em código**: as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão qualificados a serem exibidos para o público-alvo desejado.

   ➡️ [Saiba como trabalhar com políticas de decisão](create-decision.md)
