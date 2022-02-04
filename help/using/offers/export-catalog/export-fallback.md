---
title: Conjunto de dados de ofertas de fallback
description: Esta seção lista todos os campos usados no conjunto de dados exportado para ofertas de fallback
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 3%

---

# Conjunto de dados de ofertas de fallback {#fallback-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para ofertas de fallback é atualizado.

![](../../assets/dataset-fallback.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [esta seção](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados no **[!UICONTROL Decision Object Repository - Fallback Offers]** conjunto de dados.

## Identificador {#identifier}

**Campo:** _id
**Título:** Identificador
**Descrição:** Um identificador exclusivo para o registro.
**Tipo:** sequência de caracteres

## _experiência {#experience}

**Campo:** _experiência
**Tipo:** objeto

### _experience > decisão

**Campo:** decisão
**Tipo:** objeto

#### _experience > decisioning > características

**Campo:** características
**Título:** Características da opção de decisão
**Descrição:** Propriedades ou atributos adicionais pertencentes a esta opção de decisão específica. Instâncias diferentes podem ter características diferentes (chaves no mapa). As características são pares de valores de nome usados para distinguir uma opção de decisão de outras. As características são usadas como valores no conteúdo que representa essa opção de decisão e como recursos para analisar e otimizar o desempenho de uma opção. Quando cada instância tem o mesmo atributo ou propriedade, esse aspecto deve ser modelado como um schema de extensão que deriva dos detalhes da opção de decisão.
**Tipo:** objeto

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### _experience > decisioning > content

**Campo:** conteúdo
**Título:** Detalhes do conteúdo
**Descrição:** Itens de conteúdo para renderizar o item de decisão em contextos diferentes. Uma única opção de decisão pode ter várias variantes de conteúdo. Conteúdo são informações direcionadas a um público-alvo para consumo em uma experiência (digital). O conteúdo é entregue por canais em uma disposição específica.
**Tipo:** array

**_experience > decisão > conteúdo > componentes**

**Campo:** componentes
**Descrição:** Os componentes do conteúdo que representam a opção de decisão, incluindo todas as variantes de idioma. Componentes específicos são encontrados por &#39;dx:format&#39;, &#39;dc:subject&#39; e &#39;dc:language&#39; ou uma combinação deles. Esses metadados são usados para localizar ou representar o conteúdo associado a uma oferta e integrá-lo de acordo com o contrato de colocação.
**Tipo:** array
**Obrigatório:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisão > conteúdo > componentes > Tipo de componente de conteúdo**

   **Campo:** _type
   **Título:** Tipo de componente de conteúdo
   **Descrição:** Um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
   **Tipo:** sequência de caracteres

* **_experience > decisioning > content > components > _dc**

   **Campo:** _dc
   **Tipo:** objeto
   **Obrigatório:** &quot;format&quot;

   * **Formato**

      **Campo:** format
      **Título:** Formato
      **Descrição:** A manifestação física ou digital do recurso. Normalmente, Formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. A prática recomendada é selecionar um valor de um vocabulário controlado (por exemplo, a lista de [Tipos de mídia da Internet](http://www.iana.org/ atribuições/media-types/) definindo formatos de mídia de computador).
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;application/vnd.adobe.photoshop&quot;

   * **Idioma**

      **Campo:** idioma
      **Título:** Idioma
      **Descrição:** O idioma ou os idiomas do recurso. \nOs idiomas são especificados no código do idioma, conforme definido em [RFC IETF 3066](https://www.ietf.org/rfc/rfc3066.txt), que faz parte do BCP 47, utilizado noutros pontos do XDM.
      **Tipo:** array
      **Exemplos:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning > content > components > _repo**

   **Campo:** _repo
   **Tipo:** objeto

   * **id**

      **Campo:** id
      **Descrição:** Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **Campo:** name
      **Descrição:** Algumas dicas sobre onde localizar o repositório que armazena o ativo externo pelo \&quot;repo:id\&quot;.
      **Tipo:** sequência de caracteres

   * **repositoryID**

      **Campo:** repositoryID
      **Descrição:** Um identificador exclusivo opcional para fazer referência ao ativo em um repositório de conteúdo. Quando as APIs da Platform são usadas para recuperar a representação, o cliente pode esperar uma propriedade adicional \&quot;repo:resolveUrl\&quot; para recuperar o ativo.
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Campo:** resolveURL
      **Descrição:** Um localizador de recurso exclusivo opcional para ler o ativo em um repositório de conteúdo. Isso facilitará a obtenção do ativo sem que o cliente saiba onde o ativo é gerenciado e quais APIs chamar. Isso é semelhante a um link HAL, mas a semântica é mais simples e objetiva.
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > decisioning > content > components > content**

   **Campo:** conteúdo
   **Descrição:** Um campo opcional para armazenar conteúdo diretamente. Em vez de fazer referência ao conteúdo em um repositório de ativos, o componente pode armazenar conteúdo simples diretamente. Este campo não é usado para ativos de conteúdo composto, complexo e binário.
   **Tipo:** sequência de caracteres

* **_experience > decisioning > content > components > deliveryURL**

   **Campo:** deliveryURL
   **Descrição:** Um endereço de recurso exclusivo opcional para obter o ativo de uma rede de entrega de conteúdo ou de um terminal de serviço. Esse URL é usado para acessar o ativo publicamente por um agente do usuário.
   **Tipo:** sequência de caracteres
   **Exemplo:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > content > components > linkURL**

   **Campo:** linkURL
   **Descrição:** Um localizador de recurso exclusivo opcional para interações de usuário. Esse URL é usado para fazer referência ao usuário final em um agente do usuário e pode ser rastreado.
   **Tipo:** sequência de caracteres
   **Exemplo:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > content > Placement**

**Campo:** placement
**Título:** Posicionamento
**Descrição:** Posicionamento para estar em conformidade. O valor é o URI (@id) da disposição da oferta referenciada. Consulte esquema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** sequência de caracteres

#### _experience > decisioning > Status do ciclo de vida

**Campo:** lifecycleStatus
**Título:** Status do ciclo de vida
**Descrição:** O status do ciclo de vida permite que os fluxos de trabalho sejam conduzidos com um objeto . O status pode afetar quando um objeto é visível ou considerado relevante. As alterações de status são orientadas pelos clientes ou serviços que usam os objetos.
**Tipo:** string
**Valores possíveis:** &quot;Rascunho&quot; (padrão), &quot;Aprovado&quot;, &quot;Em tempo real&quot;, &quot;Concluído&quot;, &quot;Arquivado&quot;

#### _experience > decisioning > Nome da opção de decisão

**Campo:** name
**Título:** Nome da opção de decisão
**Descrição:** Nome da opção que é exibida em várias interfaces do usuário.
**Tipo:** sequência de caracteres

#### _experience > decisioning > tags

**Campo:** tags
**Título:** Tags
**Descrição:** O conjunto de tags associado a esta entidade. As tags são usadas em expressões de filtro para restringir o inventário geral a um subconjunto (categoria).
**Tipo:** array

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**Campo:** _repo
**Tipo:** objeto

### _repo > ETag da opção de decisão

**Campo:** tag
**Título:** Opção de decisão ETag
**Descrição:** A revisão de que o objeto da opção de decisão estava no momento em que o instantâneo foi tirado.
**Tipo:** sequência de caracteres
