---
title: Jornada fórmulas de classificação de arbitragem
description: Saiba como criar fórmulas para classificar jornadas para arbitragem, de modo que a melhor jornada seja selecionada por perfil com base em regras e contexto.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---

# Usar fórmulas para classificar jornadas {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>Este recurso está atualmente com a Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

O [!DNL Adobe Journey Optimizer] ajuda você a controlar quais jornadas um perfil pode inserir quando se qualificar para mais do que o sistema permite. Para fazer isso, você pode usar [conjuntos de regras](rule-sets.md) para definir limites na entrada de jornada ou simultaneidade. Quando um perfil é qualificado para mais jornadas do que o limite permite, a prioridade atribuída a cada jornada determina quais jornadas são selecionadas.

Em vez de usar a prioridade, você também pode usar **fórmulas de classificação** para ajustar dinamicamente a classificação de jornadas com base em atributos de jornada, atributos de perfil ou pontuações de modelo de IA.

As fórmulas oferecem mais flexibilidade do que a prioridade estática. Por exemplo, você pode impulsionar uma jornada para membros de fidelidade Ouro.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## Criar uma fórmula de classificação {#create-journey-ranking-formula}

Para criar uma fórmula de classificação para suas jornadas, siga as etapas abaixo.

1. Acesse a seção **[!UICONTROL Classificação de orquestração]** e selecione a guia **[!UICONTROL Fórmulas de classificação]**. A lista de fórmulas criadas anteriormente é exibida.

1. Clique em **[!UICONTROL Criar fórmula]**.

1. Especifique o nome da fórmula e adicione uma descrição, se desejar.

   ![Painel de detalhes da fórmula com campos de nome e descrição](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >O objeto de classificação é a entidade à qual a fórmula de classificação será aplicada. Por padrão, o objeto de classificação está definido como **[!UICONTROL Jornada]**.

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. Opcionalmente, clique em **[!UICONTROL Selecionar modelo de IA]** para definir o modelo que será usado como referência para criar sua fórmula de classificação.

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. Na seção **[!UICONTROL Critério 1]**, especifique a quais jornadas você deseja aplicar uma pontuação de classificação, fazendo o seguinte:

   * selecionar um [atributo de jornada](../building-journeys/journey-properties.md) (como nome de jornada, marcas, prioridade ou outras propriedades de jornada);
   * selecionar um operador lógico;
   * adicionar uma condição correspondente - você pode digitar/selecionar um valor ou escolher um atributo de perfil.

   ![Seção do critério 1 com atributo de jornada, operador e condição correspondente](assets/journey-formula-criterion-1.png){width="70%"}

1. Como opção, você pode especificar elementos adicionais para refinar as condições de correspondência para seus critérios serem verdadeiros.

   ![Condição adicional para refinar os critérios de correspondência](assets/journey-formula-additional-condition.png){width="70%"}

   Por exemplo, você definiu *Critério 1* como *marcas de Jornada* que contêm *Fidelidade*. Além disso, você pode adicionar outra condição, como se o *Status de fidelidade* fosse *Ouro*, então o *Critério 1* fosse verdadeiro.

1. Crie uma expressão que atribuirá uma pontuação de classificação às jornadas que atenderem à condição definida acima. Você pode referenciar qualquer um dos seguintes:
   * uma variável:
      * a prioridade da jornada, que é um valor manual atribuído à jornada ao [criar uma jornada](../building-journeys/journey-gs.md);
      * a pontuação resultante do modelo de IA que você selecionou opcionalmente acima;
   * um atributo:
      * qualquer atributo que possa existir no perfil, como qualquer pontuação de propensão derivada externamente;
      * um atributo de jornada;
   * um valor estático que pode ser atribuído em um formato livre;
   * uma combinação de todos os itens acima.

   ![Construtor de expressões para atribuir pontuação de classificação usando variáveis, atributos ou valores estáticos](assets/journey-formula-expression.png){width="70%"}

1. Clique em **[!UICONTROL Adicionar critério]** para adicionar um ou mais critérios quantas vezes forem necessárias. A lógica é a seguinte:
   * Se o primeiro critério for verdadeiro para um determinado item de decisão, ele terá precedência sobre os próximos.
   * Se não for verdadeiro, o mecanismo de decisão passará para o segundo critério e assim por diante.

1. Depois de definir todos os critérios, no último campo, é possível criar uma expressão que será atribuída a todas as jornadas que não atenderem aos critérios acima.

   ![Campo de expressão para jornadas que não atendem a nenhum critério](assets/journey-formula-criteria-not-met.png){width="70%"}

1. Clique em **[!UICONTROL Criar]** para concluir a fórmula de classificação.

Agora é possível selecionar essa fórmula na lista para visualizar seus detalhes e editá-la ou excluí-la. Em seguida, ela fica disponível ao configurar um conjunto de regras. [Saiba como](#assign-formula-to-ruleset)

### Exemplos de fórmula de classificação {#journey-ranking-formula-example}

Considere os exemplos abaixo.

+++Exemplo 1: usar a prioridade da jornada ou a pontuação da IA com base nas tags de jornada

![Fórmula de classificação: a marca de marketing usa a prioridade de jornada](assets/journey-formula-ex-1.png){width="60%"}

Se a jornada tiver uma tag &quot;Marketing&quot;, a pontuação da classificação será a prioridade da jornada.

![Fórmula de classificação: a marca promocional usa a pontuação do modelo de IA](assets/journey-formula-ex-2.png){width="60%"}

Se a jornada tiver uma tag &quot;Promocional&quot;, a pontuação da classificação será a pontuação do modelo de IA.

+++

+++Exemplo 2: aumentar jornadas de fidelidade por status de perfil


![Fórmula de classificação: a marca de fidelidade com status Gold usa a prioridade de jornada mais 5](assets/journey-formula-ex-3.png){width="60%"}

Se a jornada tiver uma tag de &quot;Fidelidade&quot; e o status de fidelidade do perfil for Ouro, a pontuação de classificação usada será a prioridade de jornada mais 5.

![Fórmula de classificação: a marca de fidelidade com status Prata usa a prioridade de jornada mais 2](assets/journey-formula-ex-4.png){width="60%"}

Se a jornada tiver uma tag de &quot;Fidelidade&quot; e o status de fidelidade do perfil for Prata, a pontuação de classificação será a prioridade de jornada mais 2.

Se nenhuma das condições acima for atendida, a pontuação de classificação usada será a prioridade da jornada.

+++

### Usar o editor de código {#journey-ranking-formula-code-editor}

Para expressar fórmulas de classificação na **sintaxe do PQL**, alterne para o editor de código usando o botão dedicado na parte superior direita da tela. Para obter mais informações sobre como usar a sintaxe do PQL, consulte a [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=pt-BR).

>[!CAUTION]
>
>Esta ação impedirá a reversão para a exibição padrão do construtor desta fórmula.

Em seguida, você pode aproveitar os atributos de jornada, atributos de perfil e valores estáticos para criar sua fórmula de classificação.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## Atribuir a fórmula a um conjunto de regras {#assign-formula-to-ruleset}

Para usar uma fórmula para classificar suas jornadas, é necessário atribuí-la a um conjunto de regras.

>[!NOTE]
>
>As fórmulas são atribuídas no nível do conjunto de regras, não em jornadas individuais.

1. No menu **[!UICONTROL Regras de negócio]**, crie um conjunto de regras que você deseja usar para arbitragem de jornada. [Saiba como](rule-sets.md#Create)

1. Selecione o domínio **[!UICONTROL Jornada]**.

   ![Propriedades do conjunto de regras com o domínio de Jornada selecionado](assets/journey-formula-rule-set-journey.png){width="60%"}

1. Nas propriedades do conjunto de regras, defina o **[!UICONTROL Método de classificação]** como **[!UICONTROL Fórmula]** (em vez da **[!UICONTROL Prioridade]** padrão).

1. Selecione a fórmula de classificação criada na lista suspensa.

   ![Conjunto de regras com fórmula de classificação selecionada na lista suspensa](assets/journey-rule-set-formula.png){width="60%"}

1. Crie as regras de limite de jornada que deseja adicionar ao conjunto de regras. [Saiba como](journey-capping.md#create-rule)

1. Salve o conjunto de regras.

Agora, a fórmula é atribuída ao conjunto de regras. Você pode aplicar esse conjunto de regras às suas jornadas.

## Aplicar o conjunto de regras a uma jornada {#assign-rule-set-to-journey}

Para atribuir o conjunto de regras a uma jornada, siga as etapas abaixo.

1. Crie ou abra a jornada à qual deseja atribuir o conjunto de regras. [Saiba como criar uma jornada](../building-journeys/journey-gs.md)

1. Nas propriedades da jornada, selecione o conjunto de regras na lista suspensa.  [Saiba como](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Somente um conjunto de regras pode ser aplicado a uma jornada de cada vez.

1. Salve a jornada.

Todas as jornadas que usam esse conjunto de regras serão classificadas com a fórmula selecionada quando o limite for aplicado.

Para monitorar o desempenho de seus conjuntos de regras e fórmulas de classificação, consulte a seção [Limite de Jornada e Conflitos](../reports/channel-report-cja.md#rule-sets) no relatório Visão geral.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

