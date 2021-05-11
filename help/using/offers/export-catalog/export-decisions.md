---
title: Introdução à exportação de catálogo de ofertas
description: Esta seção lista todos os campos usados no conjunto de dados exportado para decisões.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 4%

---

# Conjunto de dados Decisões {#decisions-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para decisões é atualizado.

![](../assets/dataset-activities.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [this section](../export-catalog/access-dataset.md).

Uma decisão (anteriormente conhecida como decisão de oferta) é usada para controlar o processo de decisão. Especifica o filtro aplicado ao inventário total para restringir as ofertas por tópico/categoria, a disposição para restringir o inventário às ofertas que se encaixam tecnicamente no espaço reservado para a oferta e especifica uma opção de fallback se as restrições combinadas desqualificarem todas as ofertas de personalização disponíveis.

Esta é a lista de todos os campos que podem ser usados no conjunto de dados **[!UICONTROL Decision Object Repository - Decisions]** (anteriormente conhecido como Repositório de Objeto de Decisão - Atividades).

## Identificador

Um identificador exclusivo para o registro.

Tipo: sequência de caracteres

## _experiência

### decisão

#### critérios

Define um conjunto de critérios de decisão, onde cada um contém um conjunto de restrições.

Tipo: array

* **Descrição**

   Descrição do critério. É utilizado para transmitir intenções legíveis ao ser humano sobre a forma como este critério foi construído e como está a afetar a decisão.

   Tipo: sequência de caracteres

* **Seleção de opção**

   A seleção de opção define a validade/aplicabilidade das opções neste contexto.

   Tipo: objeto

   * **Descrição**

      Descrição da seleção da opção. Ele é usado para transmitir intenções legíveis humanas sobre como ou por que essa seleção de opção foi construída e/ou qual opção corresponderá.

      Tipo: sequência de caracteres

   * **Filtro de opções**

      A referência a um filtro baseado em tag que corresponde às opções de um inventário usando suas tags anexadas. O valor é o URI (@id) da regra de decisão referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/filter.

      Tipo: sequência de caracteres

   * **Tipo de restrição do perfil**

      Determina se alguma restrição está definida no momento e como as restrições são expressas. Pode ser por meio de uma consulta de filtro ou por meio de uma ou mais associações de segmento.

      Tipo: sequência de caracteres

   * **Lista de opções**

      Uma lista que especifica diretamente as opções sem avaliar uma consulta de filtro. É possível especificar uma lista de opções ou uma regra de filtro de opções.

      Tipo: array

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option.-->

* **disposições**

   A restrição de posicionamento declara que esse critério só é aplicável para as disposições listadas. Somente quando a disposição direcionada está na lista `xdm:placements` é a seleção de opção considerada. Caso contrário, todos os critérios de decisão serão ignorados. Quando a lista &quot;xdm:disposições&quot; é omitida ou está vazia, o critério é considerado para qualquer disposição direcionada. As disposições listadas aqui impõem critérios implícitos para a seleção da opção. Uma opção a ser considerada deve ter uma representação para a disposição direcionada.

   Tipo: array

   * **Identificador de disposição**

   Uma referência a uma entidade de disposição. O valor é o URI (@id) da disposição referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.

   Tipo: sequência de caracteres

* **Restrição de perfil**

   A restrição de perfil decide se uma seleção de opção está qualificada para essa identidade de perfil no momento, neste contexto. Se a restrição de perfil não precisar considerar valores de cada opção, ou seja, se for invariável das opções da seleção de opção, a restrição de perfil que resulta em &quot;falso&quot; cancelará toda a seleção de opção. Por outro lado, uma regra de restrição de perfil que utiliza uma opção como parâmetro é avaliada para cada opção de qualificação da seleção de opção.

   Tipo: objeto

   * **Descrição**

      Descrição de restrição de perfil. É usado para transmitir intenções legíveis humanas sobre como ou por que essa restrição de perfil foi construída e/ou qual opção será incluída ou excluída por ela.

      Tipo: sequência de caracteres

   * **Regra de elegibilidade**

      Uma referência a uma regra de decisão que avalia como true ou false para um determinado perfil e/ou outros objetos XDM contextuais específicos. A regra é usada para decidir se a opção se qualifica para um determinado perfil. O valor é o URI (@id) da regra de decisão referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/rule.

      Tipo: sequência de caracteres

   * **Tipo de restrição do perfil**

      Determina se alguma restrição está definida no momento e como as restrições são expressas. Pode ser por meio de uma regra ou por meio de uma ou mais associações de segmento.

      Tipo: sequência de caracteres

      Valores possíveis: &quot;none&quot;, &quot;eligentRule&quot;, &quot;anySegments&quot;, &quot;allSegments&quot;, &quot;rules&quot;

      Valor padrão: &quot;nenhum&quot;

   * **Identificadores de segmento**

      Identificadores dos segmentos

      Sequência de caracteres: array

      * **Identificador**

         Identidade do segmento no namespace relacionado.

         Tipo: sequência de caracteres

      * **Namespace**

         O namespace associado ao atributo `xid`.

         Tipo: objeto

         * **Código**

            O código é um identificador legível para o namespace e pode ser usado para solicitar a id de namespace técnico, que é usada para o processamento de gráficos de identidade.

            Tipo: sequência de caracteres
      * **Identificador da experiência**

         Quando presente, esse valor representa um identificador de namespace cruzado que é exclusivo em todos os identificadores de escopo de namespace em todos os namespaces.

         Tipo: sequência de caracteres


* **Detalhes da classificação**

   Classificação (prioridade). Define como o \&quot;melhor opção\&quot; é determinado no contexto do critério de decisão. Entre todas as opções selecionadas que atendem às restrições de perfil, a classificação decidirá as opções principais (ou N principais) a serem propostas.

   Tipo: objeto

   * **Avaliação de pedidos**

      Avaliação de uma ordem relativa de uma ou mais opções de decisão. Opções com valores ordinais mais altos são selecionadas em qualquer opção com valores ordinais mais baixos. Os valores determinados por este método podem ser ordenados, mas as distâncias entre eles não podem ser medidas, nem os montantes nem os produtos podem ser calculados. A mediana e o modo são as únicas medidas de tendência central que podem ser usadas para dados ordinais.

      Tipo: objeto

      * **Função de pontuação**

         Uma referência a uma função que calcula uma pontuação numérica para essa opção de decisão. As opções de decisão serão ordenadas (classificadas) de acordo com essa pontuação. O valor dessa propriedade é o URI (@id) da função a ser chamada com a opção on de cada vez. Consulte esquema https://ns.adobe.com/experience/decisioning/function.

         Tipo: sequência de caracteres

      * **Tipo de Avaliação de Pedido**

         Especifica qual mecanismo de avaliação de ordem é usado, prioridade estática das opções de decisão, uma função de pontuação que calcula um valor numérico para cada opção ou uma estratégia de classificação que recebe uma lista para solicitá-la.

         Tipo: sequência de caracteres

      * **Estratégia de classificação**

         Uma referência a uma estratégia que classifica uma lista de opções de decisão. As opções de decisão serão retornadas em uma lista ordenada. O valor dessa propriedade é o URI (@id) da função a ser chamada com a opção on de cada vez. Consulte esquema https://ns.adobe.com/experience/decisioning/rankingStrategy.

         Tipo: sequência de caracteres
   * **Priority**

      A prioridade de uma única opção de decisão em relação a todas as outras opções. As opções para as quais nenhuma função de pedido é fornecida são priorizadas usando essa propriedade. As opções com valores de prioridade mais alta são selecionadas antes de qualquer opção de prioridade mais baixa. Se duas ou mais opções qualificadas compartilharem o valor de prioridade mais alto, uma é escolhida aleatoriamente e usada para a proposta de decisão.

      Tipo: integer

      Valor mínimo: 0

      Valor padrão: 0


#### Data e hora de término da atividade

Data de término e hora de término da decisão. A propriedade tem a semântica da propriedade &#39;endTime&#39; de schema.org definida em http://schema.org/Action.

Tipo: sequência de caracteres

#### Opção de fallback

A referência a uma opção de fallback que é usada ao tomar decisões no contexto desta decisão não qualifica nenhuma das opções regulares (isso normalmente acontece quando as restrições rígidas são aplicadas). O valor é o URI (@id) da opção de fallback referenciada.

Tipo: sequência de caracteres

#### Nome da atividade

Nome da decisão que é exibido em várias interfaces do usuário.

Tipo: sequência de caracteres

#### Data e hora de início da atividade

Data de início e hora de término da decisão. A propriedade tem a semântica da propriedade &#39;startTime&#39; de schema.org definida em http://schema.org/Action.

Tipo: sequência de caracteres

## _repo

### ETag da atividade

A revisão de que o objeto da decisão estava no momento em que o instantâneo foi tirado.

Tipo: sequência de caracteres
