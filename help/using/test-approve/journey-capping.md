---
title: Limite e arbitragem de jornada
description: Saiba como criar regras de limitação para suas jornadas e como arbitrar a entrada de jornada
role: User
level: Beginner
badge: label="Disponibilidade limitada"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# Limite e arbitragem de jornada {#journey-capping}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao gerenciamento de conflitos e priorização](gs-conflict-prioritization.md)
* [Detectar possíveis conflitos em jornadas e campanhas](conflicts.md)
* [Atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)
* **[limite e arbitragem de Jornada](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>As ferramentas de gerenciamento e priorização de conflitos estão disponíveis atualmente como uma Disponibilidade limitada somente para usuários selecionados.

O limite de jornada ajuda a limitar o número de jornadas nas quais um perfil pode ser inscrito, evitando a sobrecarga de comunicação. No Journey Optimizer, você pode definir dois tipos de regras de limitação:

* **Limite de entrada** limita o número de entradas em uma jornada em um determinado período para um perfil.
* **Limite de simultaneidade** limita quantas jornadas um perfil pode ser inscrito simultaneamente. Esse tipo de limite aproveita as pontuações de prioridade das jornadas para arbitrar entradas se os perfis estiverem qualificados para várias jornadas ao mesmo tempo em um determinado período.

## Criar uma regra de limite de jornada {#create-rule}

Para criar uma regra de limite de jornada, siga estas etapas:

1. Navegue até o menu **[!UICONTROL Regras de negócio (Beta)]** para acessar o inventário de conjuntos de regras.

1. Selecione o conjunto de regras ao qual deseja adicionar a regra de limitação ou crie um novo conjunto de regras:

   * Para usar um conjunto de regras existente, selecione-o na lista. As regras de limitação de jornada só podem ser adicionadas a conjuntos de regras com o domínio &quot;jornada&quot;. Você pode verificar essas informações nas listas de conjuntos de regras, na coluna **[!UICONTROL Domínio]**.

     ![](assets/journey-capping-list.png)

   * Para criar a regra de limitação dentro de um novo conjunto de regras, clique em **[!UICONTROL Criar conjunto de regras]**, especifique um nome exclusivo para o conjunto de regras e selecione &quot;Jornada&quot; no menu suspenso **[!UICONTROL Domínio do Conjunto de Regras]** e clique em **[!UICONTROL Salvar]**.

     ![](assets/journey-capping-rule-set.png)

1. Na tela do conjunto de regras, clique no botão **[!UICONTROL Adicionar regra]** e configure a regra para atender às suas necessidades:

   ![](assets/journey-capping-concurrency.png)

   * Forneça um nome exclusivo para a regra.

   * Na lista suspensa **[!UICONTROL Tipo de Regra]**, especifique o tipo de limite para a regra.

      * **[!UICONTROL Limite de Entrada de Jornada]**: Limita o número de entradas na jornada em um determinado período para um perfil.
      * **[!UICONTROL Limite de Simultaneidade de Jornada]**: Limita quantas jornadas um perfil pode ser inscrito simultaneamente.

   * Expanda as seções abaixo para saber como configurar cada tipo de limite:

     +++Configurar uma regra de limite de entrada de jornada

      1. No campo **[!UICONTROL Limite]**, defina o número máximo de vezes que um perfil pode entrar na jornada.
      1. No campo **[!UICONTROL Duration]**, defina o período a ser considerado.

     Neste exemplo, queremos impedir que perfis entrem nesta jornada mais de &quot;5&quot; vezes em um mês.

     ![](assets/journey-capping-entry-example.png)

+++

     +++Configurar uma regra de limite de simultaneidade de jornada

      1. No campo **[!UICONTROL Limite]**, defina o número máximo de jornadas nas quais um perfil pode ser inscrito simultaneamente.
      1. Use o campo **[!UICONTROL Priorização antecipada]** para arbitrar as entradas de jornada com base nas pontuações de prioridade em um período escolhido (por exemplo, 1 dia, 7 dias, 30 dias). Isso ajuda a priorizar a entrada em jornadas de valor mais alto se um perfil estiver qualificado para várias jornadas.

     Neste exemplo, queremos impedir que perfis entrem na jornada se já estiverem inscritos em outra jornada. Se outra jornada nos próximos 7 dias tiver uma pontuação de prioridade mais alta, o perfil inserirá essa jornada.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Quando a regra de limitação estiver pronta para ser aplicada às jornadas, ative-a clicando no botão de reticências ao lado do nome.

   ![](assets/journey-capping-activate-rule.png)

1. Ative todo o conjunto de regras clicando no botão de reticências ao lado do botão Adicionar regra no canto superior direito da tela.

   ![](assets/journey-capping-activate-rule-set.png){width="50%" zommable="yes"}

## Aplicar regras de limitação a jornadas {#apply-capping}

Para aplicar uma regra de limitação a uma jornada, acesse a jornada e abra suas propriedades. No menu suspenso **[!UICONTROL Regras de limitação]**, selecione o conjunto de regras relevante.
Quando a jornada for ativada, as regras de limitação definidas no conjunto de regras entrarão em vigor.

![](assets/journey-capping-apply.png)
