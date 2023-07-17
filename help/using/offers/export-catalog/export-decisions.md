---
title: Conjunto de dados de decisões
description: Esta seção lista todos os campos usados no conjunto de dados exportado para decisões
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 3%

---

# Conjunto de dados de decisões {#decisions-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para decisões é atualizado.

![](../assets/dataset-activities.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A visualização hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas no [nesta seção](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados na variável **[!UICONTROL Repositório de objetos de decisão - Decisões]** (anteriormente conhecido como Repositório de objetos de decisão - Atividades).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ Identificador

**Campo:** _id
**Título:** Identificador
**Descrição:** Um identificador exclusivo do registro.
**Tipo:** sequência de caracteres

+++

+++ _experiência

**Campo:** _experience
**Tipo:** objeto

+++

+++ _experience > decisioning

**Campo:** decisão
**Tipo:** objeto

+++

+++ _experience > decisioning > criteria

**Campo:** critérios
**Título:** Critérios
**Descrição:** Define um conjunto de critérios de decisão em que cada um contém um conjunto de restrições.
**Tipo:** matriz

+++

+++ _experience > decisioning > criteria > description

**Campo:** descrição
**Título:** Descrição
**Descrição:** Descrição do critério. É usado para transmitir intenções legíveis por humanos sobre como ou por que esse critério foi construído e como ele está afetando a decisão.
**Tipo:** sequência de caracteres

+++

+++_experience > decisão > critérios > optionSelection

**Campo:** optionSelection
**Título:** Seleção de opção
**Descrição:** A seleção de opções define a validade/aplicabilidade das opções neste contexto.
**Tipo:** objeto

* Descrição

  **Campo:** descrição
  **Título:** Descrição
  **Descrição:** Descrição da seleção de opção. É usado para transmitir intenções legíveis por humanos sobre como ou por que essa seleção de opção foi construída e/ou qual opção corresponderá.
  **Tipo:** sequência de caracteres

* Filtro de opção

  **Campo:** filtro
  **Título:** Filtro de opção
  **Descrição:** A referência a um filtro baseado em qualificador de coleção (anteriormente conhecido como &quot;etiqueta&quot;) que corresponde às opções de um estoque usando seus qualificadores de coleção anexados. O valor é o URI (@id) da regra de decisão referenciada. Consulte schema https://ns.adobe.com/experience/decisioning/filter.
  **Tipo:** sequência de caracteres

* Tipo de Restrição de Perfil

  **Campo:** optionSelectionType
  **Título:** Tipo de Restrição de Perfil
  **Descrição:** Determina se alguma restrição está definida no momento e como as restrições são expressas. Pode ser por meio de uma consulta de filtro ou por meio de uma ou mais associações de público-alvo.
  **Tipo:** sequência de caracteres
  **Valores possíveis:** &quot;none&quot; (padrão), &quot;directList&quot;, &quot;filter&quot;

* Lista de opções

  **Campo:** opções
  **Título:** Lista de opções
  **Descrição:** Uma lista que especifica diretamente as opções sem avaliar uma consulta de filtro. É possível especificar uma lista de opções ou uma regra de filtro de opções.
  **Tipo:** matriz

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_experience > decisão > critérios > inserções

**Campo:** disposições
**Título:** Restrições de posicionamento
**Descrição:** A restrição de posicionamento declara que esse critério só é aplicável para os posicionamentos listados. Somente quando o posicionamento direcionado estiver na `xdm:placements` list é a seleção de opção considerada. Caso contrário, todo o critério de decisão será ignorado. Quando a lista &quot;xdm:placements&quot; é omitida ou está vazia, o critério é considerado para qualquer posicionamento direcionado. As disposições listadas aqui impõem critérios implícitos para a seleção de opções. Uma opção a ser considerada deve ter uma representação para a inserção direcionada.
**Tipo:** matriz

* Identificador de posicionamento

  **Título:** Identificador de posicionamento
  **Descrição:** Uma referência a uma entidade de posicionamento. O valor é o URI (@id) do posicionamento referenciado. Consulte schema https://ns.adobe.com/experience/decisioning/placement.
  **Tipo:** sequência de caracteres

+++

+++_experience > decisão > critérios > profileConstraints

**Campo:** profileConstraints
**Título:** Restrição de perfil
**Descrição:** A restrição de perfil decide se uma seleção de opção é elegível para essa identidade de perfil neste momento, neste contexto. Se a restrição de perfil não precisar considerar valores de cada opção, ou seja, se for invariável das opções da seleção da opção, a restrição de perfil avaliada como &#39;falsa&#39; cancelará toda a seleção da opção. Por outro lado, uma regra de restrição de perfil que usa uma opção como parâmetro é avaliada para cada opção de qualificação da seleção da opção.
**Tipo:** objeto

+++

+++_experience > decisão > critérios > profileConstraints > Descrição

**Campo:** descrição
**Título:** Descrição
**Descrição:** Descrição de restrição de perfil. É usado para transmitir intenções legíveis por humanos sobre como ou por que essa restrição de perfil foi construída e/ou qual opção será incluída ou excluída por ela.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisão > critérios > profileConstraints > Regra de elegibilidade

**Campo:** eligibilityRule
**Título:** Regra de elegibilidade
**Descrição:** Uma referência a uma regra de decisão que é avaliada como verdadeira ou falsa para um determinado perfil e/ou outros objetos XDM contextuais fornecidos. A regra é usada para decidir se a opção se qualifica para um determinado perfil. O valor é o URI (@id) da regra de decisão referenciada. Consulte schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisão > critérios > profileConstraints > Tipo de restrição do perfil

**Campo:** profileConstraintType
**Título:** Tipo de Restrição de Perfil
**Descrição:** Determina se alguma restrição está definida no momento e como as restrições são expressas. Pode ser por meio de uma regra ou de uma ou mais associações de público-alvo.
**Tipo:** string
**Valores possíveis:**
* &quot;none&quot; (padrão)
* &quot;eligibilityRule&quot;: &quot;A restrição de perfil é expressa como uma única regra que deve ser avaliada como verdadeira antes que a ação restrita seja permitida.&quot;
* &quot;anySegments&quot;: &quot;A restrição de perfil é expressa como um ou mais públicos-alvo e o perfil deve ser um membro de pelo menos um deles antes que a ação restrita seja permitida.&quot;
* &quot;allSegments&quot;: &quot;a restrição de perfil é expressa como um ou mais públicos-alvo e o perfil deve ser um membro de todos eles antes que a ação restrita seja permitida.&quot;
* &quot;regras&quot;: &quot;A restrição de perfil é expressa como um número de regras diferentes, por exemplo, elegibilidade, aplicabilidade, adequação, que devem ser avaliadas como verdadeiras antes que a ação restrita seja permitida.&quot;

+++

+++ _experience > decisão > critérios > profileConstraints > segmentIdentities

**Campo:** segmentIdentities
**Título:** Identificadores de segmento
**Descrição:** Identificadores do público-alvo.
**Tipo:** matriz

* Identificador

  **Campo:** _id
  **Título:** Identificador
  **Descrição:** Identidade do público no namespace relacionado.
  **Tipo:** sequência de caracteres

* namespace

  **Campo:** namespace
  **Título:** Namespace
  **Descrição:** O namespace associado à variável `xid` atributo.
  **Tipo:** objeto
  **Obrigatório:** &quot;code&quot;

   * Código

     **Campo:** código
     **Título:** Código
     **Descrição:** O código é um identificador legível por humanos para o namespace e pode ser usado para solicitar a id técnica do namespace que é usada para o processamento do gráfico de identidade.
     **Tipo:** sequência de caracteres

* Identificador de experiência

  **Campo:** xid
  **Título:** Identificador de experiência
  **Descrição:** Quando presente, esse valor representa um identificador de namespace cruzado que é exclusivo em todos os identificadores de escopo de namespace em todos os namespaces.
  **Tipo:** sequência de caracteres

+++

+++_experience > decisão > critérios > classificação

**Campo:** classificação
**Título:** Detalhes da classificação
**Descrição:** Classificação (prioridade). Define como a \&quot;melhor opção\&quot; é determinada dado o contexto do critério de decisão. Entre todas as opções selecionadas que atendem às restrições de perfil, a classificação decidirá as opções principais (ou N principais) a serem propostas.
**Tipo:** objeto

+++

+++_experience > decisão > critérios > classificação > ordem

**Campo:** pedido
**Título:** Avaliação do pedido
**Descrição:** Avaliação de uma ordem relativa de uma ou mais opções de decisão. As opções com valores ordinais mais altos são selecionadas sobre qualquer opção com valores ordinais mais baixos. Os valores determinados por este método podem ser ordenados, mas as distâncias entre eles não podem ser medidas e nem somas nem produtos podem ser calculados. A mediana e o modo são as únicas medidas de tendência central que podem ser usadas para dados ordinais.
**Tipo:** objeto

* Função de pontuação

  **Campo:** função
  **Título:** Função de pontuação
  **Descrição:** Uma referência a uma função que calcula uma pontuação numérica para essa opção de decisão. As opções de decisão serão classificadas por essa pontuação. O valor dessa propriedade é o URI (@id) da função a ser chamada com uma opção de cada vez. Consulte schema https://ns.adobe.com/experience/decisioning/function.
  **Tipo:** sequência de caracteres

* Tipo de avaliação do pedido**

  **Campo:** orderEvaluationType
  **Título:** Tipo de avaliação do pedido
  **Descrição:** Especifica qual mecanismo de avaliação de pedido é usado, prioridade estática das opções de decisão, uma função de pontuação que calcula um valor numérico para cada opção ou um modelo de IA que recebe uma lista para ordená-lo.
  **Tipo:** sequência de caracteres
  **Valores possíveis:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* Estratégia de classificação

  **Campo:** rankingStrategy
  **Título:** Estratégia de classificação
  **Descrição:** Uma referência a uma estratégia que classifica uma lista de opções de decisão. As opções de decisão serão retornadas em uma lista ordenada. O valor dessa propriedade é o URI (@id) da função a ser chamada com uma opção de cada vez. Consulte schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Tipo:** sequência de caracteres

+++

+++ _experiência > decisão > critérios > classificação > Prioridade

**Campo:** prioridade
**Título:** Prioridade
**Descrição:** A prioridade de uma única opção de decisão em relação a todas as outras opções. As opções para as quais nenhuma função de ordem é fornecida são priorizadas usando essa propriedade. As opções com valores de prioridade mais altos são selecionadas antes de qualquer opção de prioridade mais baixa. Se duas ou mais opções qualificadas compartilharem o valor de prioridade mais alto, uma será escolhida aleatoriamente e usada para a apresentação de decisão.
**Tipo:** inteiro
**Valor mínimo:** 0
**Valor padrão:** 0

+++

+++ _experience > decisão > Data e hora de término da atividade

**Campo:** endTime
**Título:** Data e hora de término da atividade
**Descrição:** Data e hora de término da decisão (anteriormente conhecida como atividade). A propriedade tem a semântica da propriedade &#39;endTime&#39; de schema.org definida em https://schema.org/Action.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisão > Opção de Fallback

**Campo:** fallback
**Título:** Opção de Fallback
**Descrição:** A referência a uma opção de fallback usada ao tomar decisões no contexto desta decisão não qualifica nenhuma das opções regulares (isso normalmente acontece quando restrições rígidas são aplicadas). O valor é o URI (@id) da opção de fallback referenciada.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisioning > Nome da atividade

**Campo:** name
**Título:** Nome da atividade
**Descrição:** Nome da decisão (anteriormente conhecida como atividade) que é exibido em várias interfaces do usuário.
**Tipo:** sequência de caracteres

+++

+++_experience > decisioning > Data e hora de início da atividade

**Campo:** startTime
**Título:** Data e hora de início da atividade
**Descrição:** Data de início e hora de término da decisão (anteriormente conhecida como atividade). A propriedade tem a semântica da propriedade &#39;startTime&#39; de schema.org definida em https://schema.org/Action.
**Tipo:** sequência de caracteres

+++

+++ _repo

**Campo:** _repo
**Tipo:** objeto

+++

+++ _repo > ETag Atividade

**Campo:** etag
**Título:** ETag de atividade
**Descrição:** A revisão na qual o objeto de decisão (anteriormente conhecido como atividade) estava quando o instantâneo foi tirado.
**Tipo:** sequência de caracteres

+++
