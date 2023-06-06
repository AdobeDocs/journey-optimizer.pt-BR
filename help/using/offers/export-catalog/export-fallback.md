---
title: Conjunto de dados de ofertas substitutas
description: Esta seção lista todos os campos usados no conjunto de dados exportado para ofertas de fallback
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 118eddf540d1dfb3a30edb0b877189ca908944b1
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 3%

---

# Conjunto de dados de ofertas substitutas {#fallback-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para ofertas de fallback é atualizado.

![](../assets/dataset-fallback.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A visualização hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas no [nesta seção](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados na variável **[!UICONTROL Repositório de objetos de decisão - Ofertas substitutas]** conjunto de dados.

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

+++ _experiência > decisão > características

**Campo:** características
**Título:** Características da opção de decisão
**Descrição:** Propriedades ou atributos adicionais pertencentes a essa opção de decisão específica. Instâncias diferentes podem ter características diferentes (chaves no mapa). As características são pares de valores de nome usados para distinguir uma opção de decisão de outras. As características são usadas como valores no conteúdo que representa essa opção de decisão e como recursos para analisar e otimizar o desempenho de uma opção. Quando cada instância tem o mesmo atributo ou propriedade, esse aspecto deve ser modelado como um schema de extensão que deriva do detalhe da opção de decisão.
**Tipo:** objeto

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ _experience > decisioning > content

**Campo:** conteúdo
**Título:** Detalhes do conteúdo
**Descrição:** Itens de conteúdo para renderizar o item de decisão em contextos diferentes. Uma única opção de decisão pode ter várias variantes de conteúdo. Conteúdo é a informação direcionada a um público-alvo para consumo em uma experiência (digital). O conteúdo é entregue por meio de canais em uma disposição específica.
**Tipo:** matriz

+++

+++_experience > decisão > conteúdo > componentes

**Campo:** componentes
**Descrição:** Os componentes do conteúdo que representa a opção de decisão, incluindo todas as variantes de idioma. Componentes específicos são encontrados por &quot;dx:format&quot;, &quot;dc:subject&quot; e &quot;dc:language&quot; ou uma combinação dos mesmos. Esses metadados são usados para localizar ou representar o conteúdo associado a uma oferta e integrá-lo de acordo com o contrato de posicionamento.
**Tipo:** matriz
**Obrigatório:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisão > conteúdos > componentes > Tipo de componente de conteúdo**

   **Campo:** _type
   **Título:** Tipo de componente de conteúdo
   **Descrição:** Um conjunto enumerado de URIs em que cada valor é mapeado para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
   **Tipo:** sequência de caracteres

* **_experience > decisioning > content > components > _dc**

   **Campo:** _dc
   **Tipo:** objeto
   **Obrigatório:** &quot;format&quot;

   * **Formato**

      **Campo:** formato
      **Título:** Formato
      **Descrição:** A manifestação física ou digital do recurso. Normalmente, o Formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. A prática recomendada é selecionar um valor de um vocabulário controlado (por exemplo, a lista de [Tipos de mídia da Internet](https://www.iana.org/ atribuições/tipos de mídia/) definição de formatos de mídia de computador).
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;application/vnd.adobe.photoshop&quot;

   * **Idioma**

      **Campo:** idioma
      **Título:** Idioma
      **Descrição:** O idioma ou idiomas do recurso. \nOs idiomas são especificados no código de idioma conforme definido em [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), que faz parte do BCP 47, que é usado em outro lugar no XDM.
      **Tipo:** matriz
      **Exemplos:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisão > content > components > _repo**

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
      **Descrição:** Um localizador de recursos exclusivo opcional para ler o ativo em um repositório de conteúdo. Isso facilitará a obtenção do ativo sem que o cliente entenda onde ele é gerenciado e quais APIs chamar. Isso é semelhante a um link HAL, mas a semântica é mais simples e mais funcional.
      **Tipo:** sequência de caracteres
      **Exemplo:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > decisioning > content > components > content**

   **Campo:** conteúdo
   **Descrição:** Um campo opcional para conter o conteúdo diretamente. Em vez de fazer referência ao conteúdo em um repositório de ativos, o componente pode reter o conteúdo simples diretamente. Esse campo não é usado para ativos de conteúdo composto, complexo e binário.
   **Tipo:** sequência de caracteres

* **_experience > decisioning > content > components > deliveryURL**

   **Campo:** deliveryURL
   **Descrição:** Um localizador de recursos exclusivo opcional para obter o ativo de uma rede de entrega de conteúdo ou ponto de extremidade de serviço. Esse URL é usado para acessar o ativo publicamente por um agente do usuário.
   **Tipo:** sequência de caracteres
   **Exemplo:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > content > components > linkURL**

   **Campo:** linkURL
   **Descrição:** Um localizador de recursos exclusivo opcional para interações do usuário. Esse URL é usado para indicar o usuário final a em um agente do usuário e pode ser rastreado.
   **Tipo:** sequência de caracteres
   **Exemplo:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++

+++ _experience > decisioning > contents > Placement

**Campo:** inserção
**Título:** Posicionamento
**Descrição:** Posicionamento a ser cumprido. O valor é o URI (@id) do posicionamento de oferta referenciado. Consulte schema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisão > Status do ciclo de vida

**Campo:** lifecycleStatus
**Título:** Status do ciclo de vida
**Descrição:** O status do ciclo de vida permite que os workflows sejam conduzidos com um objeto. O status pode afetar o local em que um objeto é visível ou considerado relevante. As alterações de status são orientadas pelos clientes ou serviços que usam os objetos.
**Tipo:** string
**Valores possíveis:** &quot;Rascunho&quot; (padrão), &quot;Aprovado&quot;, &quot;Ao vivo&quot;, &quot;Concluído&quot;, &quot;Arquivado&quot;

+++

+++ _experience > decisão > Nome da opção de decisão

**Campo:** name
**Título:** Nome da opção de decisão
**Descrição:** Nome da opção que é exibido em várias interfaces de usuário.
**Tipo:** sequência de caracteres

+++

+++ _experience > decisioning > tags

**Campo:** tags
**Título:** Tags
**Descrição:** O conjunto de qualificadores de coleção (anteriormente conhecidos como &quot;tags&quot;) associados a essa entidade. Os qualificadores da coleção são usados em expressões de filtro para restringir o inventário geral a um subconjunto (categoria).
**Tipo:** matriz

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ _repo

**Campo:** _repo
**Tipo:** objeto

+++

+++ _repo > ETag de Opção de Decisão

**Campo:** etag
**Título:** ETag de opção de decisão
**Descrição:** A revisão na qual o objeto de opção de decisão estava quando o instantâneo foi tirado.
**Tipo:** sequência de caracteres

+++
