---
title: Conjunto de dados de ofertas personalizadas
description: Esta seção lista todos os campos usados no conjunto de dados exportado para ofertas
badge: label="Herdados" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '1963'
ht-degree: 0%

---

# Conjunto de dados de ofertas personalizadas {#offers-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para ofertas de conteúdo personalizado é atualizado.

![](../assets/dataset-offers.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A visualização hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [esta seção](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados no conjunto de dados **[!UICONTROL Repositório de Objetos de Decisão - Ofertas Personalizadas]**.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ Identificador

**Campo:** _id
**Título:** Identificador
**Descrição:** Um identificador exclusivo para o registro.
**Tipo:** cadeia de caracteres

+++

+++ _experiência {#experience}

**Campo:** _experiência
**Tipo:** objeto

+++

+++ _experience > decisioning

**Campo:** decisão
**Tipo:** objeto

+++

+++ _experience > decisão > calendarConstraints

**Campo:** calendarConstraints
**Título:** Detalhes de Restrição de Calendário
**Descrição:** as restrições de calendário decidem se uma opção de decisão é válida considerando um intervalo de datas. Fora desse intervalo de datas, a opção não pode ser proposta.
**Tipo:** objeto

* **Data e hora de término**

  **Campo:** endDate
  **Título:** Data e hora de término
  **Descrição:** A data final de uma validade de opções de decisão. As opções que passaram da data de término não podem mais ser propostas no processo de decisão.
  **Tipo:** cadeia de caracteres

* **Data e hora de início**

  **Campo:** startDate
  **Título:** Data e hora de início
  **Descrição:** A data inicial de uma validade de opções de decisão. As opções que não atingiram a data de início não podem ser propostas ainda no processo de decisão.
  **Tipo:** cadeia de caracteres

+++

+++ _experiência > decisão > características

**Campo:** características
**Título:** Características da Opção de Decisão
**Descrição:** propriedades ou atributos adicionais pertencentes a esta opção de decisão específica. Instâncias diferentes podem ter características diferentes (chaves no mapa). As características são pares de valores de nome usados para distinguir uma opção de decisão de outras. As características são usadas como valores no conteúdo que representa essa opção de decisão e como recursos para analisar e otimizar o desempenho de uma opção. Quando cada instância tem o mesmo atributo ou propriedade, esse aspecto deve ser modelado como um schema de extensão que deriva do detalhe da opção de decisão.
**Tipo:** objeto

+++

+++ _experience > decisioning > content

**Campo:** conteúdo
**Título:** Detalhes do Conteúdo
**Descrição:** itens de conteúdo para renderizar o item de decisão em contextos diferentes. Uma única opção de decisão pode ter várias variantes de conteúdo. Conteúdo é a informação direcionada a um público-alvo para consumo em uma experiência (digital). O conteúdo é entregue por meio de canais em uma disposição específica.
**Tipo:** matriz

+++

+++_experience > decisão > conteúdo > componentes

**Campo:** componentes
**Descrição:** Os componentes do conteúdo que representam a opção de decisão, incluindo todas as suas variantes de idioma. Componentes específicos são encontrados por &quot;dx:format&quot;, &quot;dc:subject&quot; e &quot;dc:language&quot; ou uma combinação dos mesmos. Esses metadados são usados para localizar ou representar o conteúdo associado a uma oferta e integrá-lo de acordo com o contrato de posicionamento.
**Tipo:** matriz
**Obrigatório:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experiência > decisão > conteúdo > componentes > Tipo de componente de conteúdo**

  **Campo:** _tipo
  **Título:** Tipo de Componente de Conteúdo
  **Descrição:** Um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
  **Tipo:** cadeia de caracteres

* **_experiência > decisão > conteúdo > componentes > _dc**

  **Campo:** _dc
  **Tipo:** objeto
  **Obrigatório:** &quot;formato&quot;

   * **Formato**

     **Campo: formato**
     **Título:** Formato
     **Descrição:** A manifestação física ou digital do recurso. Normalmente, o Formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. A prática recomendada é selecionar um valor de um vocabulário controlado (por exemplo, a lista de [Tipos de mídia da Internet](https://www.iana.org/assignments/media-types/) definindo formatos de mídia de computador).
     **Tipo:** cadeia de caracteres
     **Exemplo:** &quot;application/vnd.adobe.photoshop&quot;

   * **Idioma**

     **Campo:** idioma
     **Título:** Idioma
     **Descrição:** O idioma ou idiomas do recurso. \nOs idiomas são especificados no código de idioma conforme definido em [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que faz parte do BCP 47, que é usado em outro lugar no XDM.
     **Tipo:** matriz
     **Exemplos:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experiência > decisão > conteúdo > componentes > _repo**

  **Campo:** _repo
  **Tipo:** objeto

   * **id**

     **Campo:** id
     **Descrição:** Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.
     **Tipo:** cadeia de caracteres
     **Exemplo:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **Campo:** nome
     **Descrição:** Alguma dica sobre onde localizar o repositório que armazena o ativo externo pelo \&quot;repo:id\&quot;.
     **Tipo:** cadeia de caracteres

   * **IDdoRepositório**

     **Campo:** repositoryID
     **Descrição:** Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.
     **Tipo:** cadeia de caracteres
     **Exemplo:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolverURL**

     **Campo:** resolveURL
     **Descrição:** Um localizador de recursos exclusivo opcional para ler o ativo em um repositório de conteúdo. Isso facilitará a obtenção do ativo sem que o cliente entenda onde ele é gerenciado e quais APIs chamar. Isso é semelhante a um link HAL, mas a semântica é mais simples e mais funcional.
     **Tipo:** cadeia de caracteres
     **Exemplo:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experiência > decisão > conteúdo > componentes > conteúdo**

  **Campo:** conteúdo
  **Descrição:** Um campo opcional para conter o conteúdo diretamente. Em vez de fazer referência ao conteúdo em um repositório de ativos, o componente pode reter o conteúdo simples diretamente. Esse campo não é usado para ativos de conteúdo composto, complexo e binário.
  **Tipo:** cadeia de caracteres

* **_experiência > decisão > conteúdo > componentes > deliveryURL**

  **Campo:** deliveryURL
  **Descrição:** Um localizador de recursos exclusivo opcional para obter o ativo de uma rede de entrega de conteúdo ou ponto de extremidade de serviço. Esse URL é usado para acessar o ativo publicamente por um agente do usuário.
  **Tipo:** cadeia de caracteres
  **Exemplo:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experiência > decisão > conteúdo > componentes > linkURL**

  **Campo:** linkURL
  **Descrição:** Um localizador de recursos exclusivo opcional para interações do usuário. Esse URL é usado para indicar o usuário final a em um agente do usuário e pode ser rastreado.
  **Tipo:** cadeia de caracteres
  **Exemplo:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_experience > decisão > conteúdo > Posicionamento

**Campo:** posicionamento
**Título:** Posicionamento
**Descrição:** Posicionamento a ser seguido. O valor é o URI (@id) do posicionamento de oferta referenciado. Consulte schema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** cadeia de caracteres

+++

+++ _experience > decisão > Status do ciclo de vida

**Campo:** lifecycleStatus
**Título:** Status do Ciclo de Vida
**Descrição:** o status do ciclo de vida permite que os fluxos de trabalho sejam conduzidos com um objeto. O status pode afetar o local em que um objeto é visível ou considerado relevante. As alterações de status são orientadas pelos clientes ou serviços que usam os objetos.
**Tipo:** cadeia de caracteres
**Valores possíveis:** &quot;Rascunho&quot; (padrão), &quot;Aprovado&quot;, &quot;Ao Vivo&quot;, &quot;Concluído&quot;, &quot;Arquivado&quot;

+++

+++ _experience > decisão > Nome da opção de decisão

**Campo:** nome
**Título:** Nome da Opção de Decisão
**Descrição:** Nome da opção que é exibido em várias interfaces de usuário.
**Tipo:** cadeia de caracteres

+++

+++ _experience > decisão > profileConstraints

**Campo:** profileConstraints
**Título:** Detalhes de Restrição de Perfil
**Descrição:** As restrições de perfil decidem se uma opção está qualificada para esta identidade de perfil, neste momento, neste contexto. Se a restrição de perfil não precisar considerar valores de cada opção, ou seja, se for invariável das opções da seleção da opção, a restrição de perfil avaliada como &#39;falsa&#39; cancelará toda a seleção da opção. Por outro lado, uma regra de restrição de perfil que usa uma opção como parâmetro é avaliada para cada opção de qualificação da seleção da opção.
**Tipo:** objeto

+++

+++_experience > decisão > profileConstraints > Descrição

**Campo:** descrição
**Título:** Descrição
**Descrição:** Descrição da restrição do perfil. É usado para transmitir intenções legíveis por humanos sobre como ou por que essa restrição de perfil foi construída e/ou qual opção será incluída ou excluída por ela.
**Tipo:** cadeia de caracteres

+++

+++_experience > decisão > profileConstraints > Regra de elegibilidade

**Campo:** eligibilityRule
**Título:** Regra de Qualificação
**Descrição:** Uma referência a uma regra de decisão que é avaliada como verdadeira ou falsa para um determinado perfil e/ou outros objetos XDM contextuais fornecidos. A regra é usada para decidir se a opção se qualifica para um determinado perfil. O valor é o URI (@id) da regra de decisão referenciada. Consulte schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** cadeia de caracteres

+++

+++_experience > decisão > profileConstraints > Tipo de restrição de perfil

**Campo:** profileConstraintType
**Título:** Tipo de Restrição de Perfil
**Descrição:** determina se há restrições definidas no momento e como elas são expressas. Pode ser por meio de uma regra ou de uma ou mais associações de público-alvo.
**Tipo:** cadeia de caracteres
**Valores possíveis:**
* &quot;none&quot; (padrão)
* &quot;eligibilityRule&quot;: &quot;A restrição de perfil é expressa como uma única regra que deve ser avaliada como verdadeira antes que a ação restrita seja permitida.&quot;
* &quot;anySegments&quot;: &quot;A restrição de perfil é expressa como um ou mais públicos-alvo e o perfil deve ser um membro de pelo menos um deles antes que a ação restrita seja permitida.&quot;
* &quot;allSegments&quot;: &quot;a restrição de perfil é expressa como um ou mais públicos-alvo e o perfil deve ser um membro de todos eles antes que a ação restrita seja permitida.&quot;
* &quot;regras&quot;: &quot;A restrição de perfil é expressa como um número de regras diferentes, por exemplo, elegibilidade, aplicabilidade, adequação, que devem ser avaliadas como verdadeiras antes que a ação restrita seja permitida.&quot;

+++

+++_experience > decisão > profileConstraints > Identificadores de segmento

**Campo:** segmentIdentities
**Título:** Identificadores de Segmento
**Descrição:** Identificadores dos públicos-alvo
**Tipo:** matriz

* **Identificador**

  **Campo:** _id
  **Título:** Identificador
  **Descrição:** Identidade dos públicos-alvo no namespace relacionado.
  **Tipo:** cadeia de caracteres

* **Namespace**

  **Campo:** namespace
  **Título:** Namespace
  **Descrição:** O namespace associado ao atributo `xid`.
  **Tipo:** objeto
  **Obrigatório:** &quot;código&quot;

   * **Código**

     **Campo:** código
     **Título:** Código
     **Descrição:** O código é um identificador legível por humanos para o namespace e pode ser usado para solicitar a identificação técnica do namespace que é usada para o processamento do gráfico de identidade.
     **Tipo:** cadeia de caracteres

* **Identificador de experiência**

  **Campo:** xid
  **Título:** Identificador de experiência
  **Descrição:** Quando presente, esse valor representa um identificador de namespace cruzado que é exclusivo em todos os identificadores de escopo de namespace em todos os namespaces.
  **Tipo:** cadeia de caracteres

+++

+++ _experience > decisão > classificação

**Campo:** classificação
**Título:** Detalhes da Classificação
**Descrição:** Classificação (prioridade). Define o que é considerado a \&quot;melhor ação\&quot;, dado o contexto do critério de decisão. Entre todas as opções selecionadas que atendem à restrição de qualificação, a ordem de classificação decidirá as opções principais (ou N principais) a serem propostas.
**Tipo:** objeto

+++

+++_experience > decisão > classificação > Avaliação de pedido

**Campo:** ordem
**Título:** Avaliação da Ordem
**Descrição:** Avaliação de uma ordem relativa de uma ou mais opções de decisão. As opções com valores ordinais mais altos são selecionadas sobre qualquer opção com valores ordinais mais baixos. Os valores determinados por este método podem ser ordenados, mas as distâncias entre eles não podem ser medidas e nem somas nem produtos podem ser calculados. A mediana e o modo são as únicas medidas de tendência central que podem ser usadas para dados ordinais.
**Tipo:** objeto

* **Função de pontuação**

  Função **Campo:**
  **Título:** Função de pontuação
  **Descrição:** Uma referência a uma função que calcula uma pontuação numérica para essa opção de decisão. As opções de decisão serão classificadas por essa pontuação. O valor dessa propriedade é o URI (@id) da função a ser chamada com uma opção de cada vez. Consulte schema https://ns.adobe.com/experience/decisioning/function.
  **Tipo:** cadeia de caracteres

* **Tipo de Avaliação do Pedido**

  **Campo:** orderEvaluationType
  **Título:** Tipo de Avaliação da Ordem
  **Descrição:** Especifica qual mecanismo de avaliação de ordem é usado, a prioridade estática das opções de decisão, uma função de pontuação que calcula um valor numérico para cada opção ou um modelo de IA que recebe uma lista para ordená-la.
  **Tipo:** cadeia de caracteres
  **Valores possíveis:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* **Estratégia de classificação**

  **Campo:** rankingStrategy
  **Título:** Estratégia de classificação
  **Descrição:** Uma referência a uma estratégia que classifica uma lista de opções de decisão. As opções de decisão serão retornadas em uma lista ordenada. O valor dessa propriedade é o URI (@id) da função a ser chamada com uma opção de cada vez. Consulte schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Tipo:** cadeia de caracteres

+++

+++_experience > decisão > classificação > Prioridade

**Campo:** prioridade
**Título:** Prioridade
**Descrição:** A prioridade de uma única opção de decisão em relação a todas as outras opções. As opções para as quais nenhuma função de ordem é fornecida são priorizadas usando essa propriedade. As opções com valores de prioridade mais altos são selecionadas antes de qualquer opção de prioridade mais baixa. Se duas ou mais opções qualificadas compartilharem o valor de prioridade mais alto, uma será escolhida aleatoriamente e usada para a apresentação de decisão.
**Tipo:** inteiro
**Valor mínimo:** 0
**Valor padrão:** 0

+++

+++ _experience > decisioning > tags

**Campo:** marcas
**Título:** Marcas
**Descrição:** O conjunto de qualificadores de coleção (anteriormente conhecidos como &quot;marcas&quot;) associado a esta entidade. Os qualificadores da coleção são usados em expressões de filtro para restringir o inventário geral a um subconjunto (categoria).
**Tipo:** matriz

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**Campo:** _repo
**Tipo:** objeto

+++

+++ _repo > ETag de Opção de Decisão

**Campo:** etag
**Título:** ETag de Opções de Decisão
**Descrição:** A revisão na qual o objeto de opção de decisão estava quando o instantâneo foi tirado.
**Tipo:** cadeia de caracteres

+++
