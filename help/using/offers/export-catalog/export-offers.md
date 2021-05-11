---
title: Conjunto de dados de ofertas personalizadas
description: Esta seção lista todos os campos usados no conjunto de dados exportado para ofertas.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1789'
ht-degree: 3%

---

# Conjunto de dados de ofertas personalizadas {#offers-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para ofertas de conteúdo personalizadas é atualizado.

![](../assets/dataset-offers.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [this section](../export-catalog/access-dataset.md).

As ofertas personalizadas formam o conjunto de opções para uma decisão. O objetivo da decisão é fazer um grande inventário de itens e aplicar inúmeras regras de restrição a esse inventário para reduzi-lo e classificar as opções de qualificação de acordo com um critério. As apresentações resultantes reúnem e personalizam a experiência para indivíduos específicos.

Esta é a lista de todos os campos que podem ser usados no conjunto de dados **[!UICONTROL Decision Object Repository - Personalized Offers]**.

## Identificador

Um identificador exclusivo para o registro.
Tipo: sequência de caracteres

## _experiência

### decisão

#### calendarConstraints

**Detalhes da restrição do calendário**. As restrições do calendário decidem se uma opção de decisão é válida, considerando um intervalo de datas. Fora desse intervalo de datas, a opção não pode ser proposta.
Tipo: objeto

* **Data e hora finais**

   A data final de uma validade de opções de decisão. As opções que ultrapassaram sua data final não podem mais ser propostas no processo de decisão.

   Tipo: sequência de caracteres

* **Data e hora de início**

   A data de início de uma validade de opções de decisão. As opções que não atingiram a data de início ainda não podem ser propostas no processo de decisão.

   Tipo: sequência de caracteres

#### características

**Características da opção de decisão**. Propriedades ou atributos adicionais pertencentes a esta opção de decisão específica. Instâncias diferentes podem ter características diferentes (chaves no mapa). As características são pares de nome/valor usados para distinguir uma opção de decisão de outras. As características são usadas como valores no conteúdo que representa essa opção de decisão e como recursos para analisar e otimizar o desempenho de uma opção. Quando cada instância tem o mesmo atributo ou propriedade, esse aspecto deve ser modelado como um schema de extensão que deriva dos detalhes da opção de decisão.

Tipo: objeto

#### conteúdo

**Detalhes do conteúdo**. Itens de conteúdo para renderizar o item de decisão em contextos diferentes. Uma única opção de decisão pode ter várias variantes de conteúdo. Conteúdo são informações direcionadas a um público-alvo para consumo em uma experiência (digital). O conteúdo é entregue por canais em uma disposição específica.

Tipo: array

* ****
componentesOs componentes do conteúdo que representam a opção de decisão, incluindo todas as variantes de idioma. Componentes específicos são encontrados por &#39;dx:format&#39;, &#39;dc:subject&#39; e &#39;dc:language&#39; ou uma combinação deles. Esses metadados são usados para localizar ou representar o conteúdo associado a uma oferta e integrá-lo de acordo com o contrato de colocação.

   * **Tipo de componente de conteúdo**
Um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
Tipo: sequência de caracteres

   * **_dc**

      * ****
FormatoA manifestação física ou digital do recurso. Normalmente, Formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. A prática recomendada é selecionar um valor de um vocabulário controlado (por exemplo, a lista de [Tipos de Mídia da Internet](http://www.iana.org/ atribuições/media-types/) que define formatos de mídia de computador).

         Tipo: sequência de caracteres

         Exemplo: &quot;application/vnd.adobe.photoshop&quot;

      * ****
IdiomaO idioma ou os idiomas do recurso.\nOs idiomas são especificados no código de idioma, conforme definido em [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que faz parte do BCP 47, que é usado em outro lugar no XDM.

         Tipo: sequência de caracteres

         Exemplos: &quot;/n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      * **id**

         Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.

         Tipo: sequência de caracteres

      * **name**

         Algumas dicas sobre onde localizar o repositório que armazena o ativo externo pelo \&quot;repo:id\&quot;.

         Tipo: sequência de caracteres

      * **repositoryID**

         Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.

         Tipo: sequência de caracteres

         Exemplo: &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         Um localizador de recurso exclusivo opcional para ler o ativo em um repositório de conteúdo. Isso facilitará a obtenção do ativo, sem que o cliente saiba onde o ativo é gerenciado e quais APIs chamar. Isso é semelhante a um link HAL, mas a semântica é mais simples e útil.

         Tipo: sequência de caracteres

         Exemplo: &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&amp;quot&quot;
   * **conteúdo**

      Um campo opcional para armazenar conteúdo diretamente. Em vez de fazer referência ao conteúdo em um repositório de ativos, o componente pode armazenar conteúdo simples diretamente. Este campo não é usado para ativos de conteúdo composto, complexo e binário.

      Tipo: sequência de caracteres

   * **deliveryURL**

      Um endereço de recurso exclusivo opcional para obter o ativo de uma rede de entrega de conteúdo ou de um terminal de serviço. Esse URL é usado para acessar o ativo publicamente por um agente do usuário.

      Tipo: sequência de caracteres

      Exemplo: &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      Um localizador de recurso exclusivo opcional para interações de usuário. Esse URL é usado para fazer referência ao usuário final em um agente do usuário e pode ser rastreado.

      Tipo: sequência de caracteres

      Exemplo: &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg



* **Disposição**

   Posicionamento para estar em conformidade. O valor é o URI (@id) da disposição da oferta referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.

#### Status do ciclo de vida

O status do ciclo de vida permite que os fluxos de trabalho sejam conduzidos com um objeto . O status pode afetar quando um objeto é visível ou considerado relevante. As alterações de status são orientadas pelos clientes ou serviços que usam os objetos.
Tipo: string
Valores possíveis: Rascunho, Aprovado, Em Tempo Real, Concluído, Arquivado

#### Nome da opção de decisão

Nome da opção. O nome é exibido em várias interfaces do usuário.
Tipo: sequência de caracteres

#### Detalhes da restrição de perfil

As restrições de perfil decidem se uma opção está qualificada para essa identidade de perfil, neste momento, neste contexto. Se a restrição de perfil não precisar considerar valores de cada opção, ou seja, se for invariável das opções da seleção de opção, a restrição de perfil que resulta em &quot;falso&quot; cancelará toda a seleção de opção. Por outro lado, uma regra de restrição de perfil que utiliza uma opção como parâmetro é avaliada para cada opção de qualificação da seleção de opção.
Tipo: objeto

* **Descrição**

   Descrição de restrição de perfil. É usado para transmitir intenções legíveis humanas sobre como ou por que essa restrição de perfil foi construída e/ou qual opção será incluída ou excluída por ela.
Tipo: sequência de caracteres

* **Regra de elegibilidade**

   Uma referência a uma regra de decisão que avalia como true ou false para um determinado perfil e/ou outros objetos XDM contextuais específicos. A regra é usada para decidir se a opção se qualifica para um determinado perfil. O valor é o URI (@id) da regra de decisão referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/rule.

   Tipo: sequência de caracteres

* **Tipo de restrição do perfil**

   Determina se alguma restrição está definida no momento e como as restrições são expressas. Pode ser por meio de uma regra ou por meio de uma ou mais associações de segmento.
Tipo: string
Valores possíveis:

   * None

   * &quot;eligentRule&quot;: &quot;A restrição de perfil é expressa como uma única regra que deve ser avaliada como true antes que a ação restrita seja permitida&quot;,

   * &quot;Qualquer segmento&quot;: &quot;A restrição de perfil é expressa como um ou mais segmentos e o perfil deve ser membro de pelo menos um deles antes que a ação restrita seja permitida&quot;,

   * &quot;Todos os segmentos&quot;: &quot;A restrição de perfil é expressa como um ou mais segmentos e o perfil deve ser um membro de todos eles antes que a ação restrita seja permitida&quot;,

   * &quot;rules&quot;: &quot;A restrição de perfil é expressa como um número de regras diferentes, por exemplo, qualificação, aplicabilidade, adequação, que devem ser avaliadas como true antes que a ação restrita seja permitida.&quot;

* **Identificadores de segmento**

   Identificadores dos segmentos

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


#### Detalhes da classificação

Classificação (prioridade). Define o que é considerado a \&quot;melhor ação\&quot;, dado o contexto do critério de decisão. Entre todas as opções selecionadas que atendem à restrição de qualificação, a ordem de classificação decidirá a(s) opção(ões) principal(s) (ou N superior) a ser proposta.

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

      Valores possíveis: &quot;estático&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot; <!--(TBC)-->

   * **Estratégia de classificação**

      Uma referência a uma estratégia que classifica uma lista de opções de decisão. As opções de decisão serão retornadas em uma lista ordenada. O valor dessa propriedade é o URI (@id) da função a ser chamada com a opção on de cada vez. Consulte esquema https://ns.adobe.com/experience/decisioning/rankingStrategy.

      Tipo: sequência de caracteres

* **Priority**

   A prioridade de uma única opção de decisão em relação a todas as outras opções. As opções para as quais nenhuma função de pedido é fornecida são priorizadas usando essa propriedade. As opções com valores de prioridade mais alta são selecionadas antes de qualquer opção de prioridade mais baixa. Se duas ou mais opções qualificadas compartilharem o valor de prioridade mais alto, uma é escolhida aleatoriamente e usada para a proposta de decisão.

   Tipo: integer

   Valor mínimo: 0

   Valor padrão: 0

#### Tags

O conjunto de tags associado a esta entidade. As tags são usadas em expressões de filtro para restringir o inventário geral a um subconjunto (categoria).

* **items**

   Um identificador de um objeto de tag. O valor é o @id da tag referenciada. Consulte esquema de tag: https://ns.adobe.com/experience/decisioning/tag.

## _repo

### Opção de decisão ETag

A revisão de que o objeto da opção de decisão estava no momento em que o instantâneo foi tirado.

Tipo: sequência de caracteres



