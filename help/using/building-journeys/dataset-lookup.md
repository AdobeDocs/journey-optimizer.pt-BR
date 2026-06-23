---
solution: Journey Optimizer
product: journey optimizer
title: Usar  [!DNL Adobe Experience Platform] dados no jornada
description: Saiba como usar a Atividade de Pesquisa de Conjunto de Dados no [!DNL Adobe Journey Optimizer] para enriquecer as jornadas do cliente com dados externos do [!DNL Adobe Experience Platform].
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidade limitada" type="Informative"
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
TQID: https://experienceleague.adobe.com/4sQ3A15j47fQ6hI1G9oS6T6ne9nbxIaeqc-95zSUIq4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1500
ht-degree: 6%

---

# Usar dados da [!DNL Adobe Experience Platform] em jornadas {#datalookup}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade de pesquisa de conjunto de dados para recuperar dinamicamente dados de conjuntos de dados de registros do Adobe Experience Platform em tempo de execução e enriquecer suas jornadas com dados externos para personalização e tomada de decisão.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Atividade de pesquisa do conjunto de dados"
>abstract="A atividade **[!UICONTROL Pesquisa de conjunto de dados]** permite recuperar dados de [!DNL Adobe Experience Platform]conjuntos de dados de registros durante o tempo de execução. Ao aproveitar esse recurso, é possível acessar dados que podem não estar no perfil ou no conteúdo do evento, garantindo que as interações com o cliente sejam relevantes e oportunas."

A atividade **[!UICONTROL Pesquisa de conjunto de dados]** permite recuperar dados de [!DNL Adobe Experience Platform]conjuntos de dados de registros durante o tempo de execução. Ao aproveitar esse recurso, é possível acessar dados que podem não estar no perfil ou no conteúdo do evento, garantindo que as interações com o cliente sejam relevantes e oportunas.

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível para todos os clientes como uma versão de disponibilidade limitada.

Principais benefícios:

* **Personalização em tempo real**: personalize as experiências do cliente usando dados enriquecidos.
* **Tomada de decisão dinâmica**: use dados externos para orientar lógica e ações de jornada.
* **Acesso a dados aprimorado**: recupere metadados do produto, tabelas de preços ou dados relacionais vinculados a chaves específicas.

## Leitura obrigatória {#must-read}

Revise esses requisitos antes de configurar pesquisas de conjunto de dados.

### Ativação do conjunto de dados

O conjunto de dados deve ser habilitado para pesquisa em [!DNL Adobe Experience Platform]. Informações detalhadas estão disponíveis nesta seção: [Use [!DNL Adobe Experience Platform] data](../data/lookup-aep-data.md).

### Limites e restrições

* Máximo de 10 atividades de Pesquisa de conjunto de dados por jornada.
* Máximo de 20 campos selecionados.
* Máximo de 50 chaves na matriz de chaves de pesquisa.
* O tamanho de dados enriquecido é limitado a 10 KB.

### Considerações adicionais sobre desempenho

As recomendações abaixo são orientações para evitar atrasos no delivery:

| Consideração | Limite recomendado | Descrição |
| ------- | ------- | ------- |
| Atributos por pesquisa | Até 20 | Número de campos de dados recuperados por registro em uma única atividade de pesquisa. |
| Atividades de pesquisa | Até 5 por jornada | Cada jornada pode conter até 5 atividades de pesquisa separadas. Cada pesquisa pode direcionar a um conjunto de dados diferente. |

## Configurar a atividade de pesquisa do conjunto de dados {#configure}

Para configurar a atividade **[!UICONTROL Pesquisa de conjunto de dados]**, siga estas etapas:

1. Expanda a categoria **[!UICONTROL Orquestração]** e solte uma atividade de **[!UICONTROL Pesquisa de conjunto de dados]** na tela.

   Atividade de pesquisa do conjunto de dados ![[!DNL Adobe Experience Platform] na jornada &#x200B;](assets/aep-data-activity.png)

1. Adicione um rótulo e uma descrição.

1. No campo **[!UICONTROL Conjunto de Dados]**, selecione o conjunto de dados com os atributos necessários.

   >[!NOTE]
   >
   >Se o conjunto de dados que você está procurando não for exibido na lista, verifique se você o ativou para pesquisa. Para obter mais detalhes, consulte a seção [Deve ler](#must-read).

1. Selecione os campos específicos que deseja buscar no conjunto de dados.

   * Você só pode selecionar nós de folha (campos no nível mais baixo do esquema). O campo deve ser um valor primitivo (sequência, número, booleano, data etc.).

   * Listas (matrizes) e mapas (objetos de valor-chave) não podem ser selecionados.

   +++Exemplo

   ![Seleção de campo de conjunto de dados mostrando tipos de dados primitivos e estrutura](assets/aep-data-leaf-primitive.png)

   +++

1. No campo **[!UICONTROL Chave(s) de pesquisa]**, escolha uma chave de associação que exista nos atributos de item de decisão e no conjunto de dados. Essa chave é usada pelo sistema para pesquisar no conjunto de dados selecionado.

   * As chaves podem ser expressões derivadas do contexto da jornada, como SKUs, IDs de email ou outros identificadores. Exemplo: `@profile.email` ou `list(@event{purchase_event.products.sku})`.

   * Somente **cadeias de caracteres** ou **listas de cadeias de caracteres** têm suporte.

   >[!IMPORTANT]
   >
   >Você deve definir a chave de pesquisa usando o **modo avançado**. Se você usar o modo simples para definir a chave, a saída da atividade de pesquisa do conjunto de dados não estará disponível como um atributo de contexto em atividades downstream, e a sintaxe `@datasetLookup{}` falhará com um erro &quot;Pesquisa de conjunto de dados não encontrada&quot; nas atividades de condição.

   +++Exemplo

   ![Editor de expressão com pesquisa de campo de conjunto de dados e funções de cadeia de caracteres](assets/aep-data-strings.png)

   +++

## Usar dados enriquecidos na jornada

Os dados recuperados pela atividade **[!UICONTROL Pesquisa de conjunto de dados]** são armazenados no contexto de Jornada como uma matriz de objetos. Está disponível no editor de expressão de jornada e no editor de personalização, permitindo lógica condicional e mensagens personalizadas com base em dados enriquecidos.

* **Editor de Expressão de Jornada**:

  Acesse o editor do **[!UICONTROL Modo avançado]** e use a sintaxe: `@datasetLookup{MyDatasetLookUpActivity1.entities}`. [Saiba como trabalhar com o editor de expressão avançado](../building-journeys/expression/expressionadvanced.md)

* **Editor Personalization**:

  Use a sintaxe: `{{context.journey.datasetLookup.1482319411.entities}}`.

>[!NOTE]
>
>Os dados enriquecidos são transitórios e estão disponíveis apenas durante o tempo de execução da jornada e na personalização de atividades de saída (email, push, SMS etc.)

## Exemplos de casos de uso

+++Filtragem com base na categoria do produto

**Cenário**:Send um cupom para usuários que gastam mais de US$ 40 em produtos domésticos.

**Fluxo de Jornadas**:

1. **Evento de compra**: capturar SKUs do carrinho do usuário.

1. **Atividade de pesquisa do conjunto de dados**:

   * Conjunto de dados: `products-dataset` (SKU como chave primária).
   * Chaves de Pesquisa: `list(@event{purchase_event.products.sku})`.
   * Campos a Retornar: `["SKU", "category", "price"]`.

1. **Atividade de condição**:

   * Filtrar SKUs em que a categoria é &quot;residência&quot;.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )} 
     ```

   OR

   * Agregar o total gasto em produtos domésticos e compará-lo ao limite de US$ 40.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )}.price}, ',', true ) > 40
     ```

1. **Editor Personalization**:

   Use os dados enriquecidos para personalizar o conteúdo do email:

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++Personalization usando dados de fidelidade externos

**Cenário**: identifique qual conta de email de um perfil tem um Status de Fidelidade Platinum. Nesse cenário, a conta de fidelidade é associada a uma ID de email e os dados de fidelidade não estão disponíveis na loja de pesquisa de perfil padrão.

**Fluxo de Jornadas**:

1. **Acionador do Evento de Perfil**: Capturar IDs de email do perfil ou do contexto do evento.

1. **Atividade de Pesquisa de Conjunto de Dados**:
   * Conjunto de dados: `loyalty-member-dataset` (email como chave primária).
   * Chaves de Pesquisa: `@profile.email`.
   * Campos a Retornar: `["email", "loyaltyTier"]`.

1. **Atividade de condição**:

   Ramifique a jornada com base no nível de fidelidade:

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Editor Personalization**:

   Use os dados da camada de fidelidade enriquecida para personalizar a comunicação de saída:

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```

+++

## Solução de problemas {#troubleshooting}

### Erro &quot;Pesquisa de conjunto de dados não encontrada&quot; na atividade de condição {#troubleshooting-not-found}

**Sintoma:** A sintaxe `@datasetLookup{}` no editor de expressão avançado de uma atividade de condição retorna um erro &quot;Pesquisa de conjunto de dados não encontrada&quot;, mesmo que a atividade de pesquisa de conjunto de dados esteja configurada corretamente na jornada.

**Causa:** a chave de pesquisa na atividade de pesquisa do conjunto de dados foi definida usando o modo simples. Quando a chave não está definida no modo avançado, a saída da atividade não é exposta como um atributo de contexto em atividades downstream.

**Correção:** Abra a atividade de pesquisa do conjunto de dados, localize o campo **[!UICONTROL Chave(s) de pesquisa]** e alterne para o **modo avançado** para redefinir a expressão de chave. Salve a atividade e publique novamente a jornada.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como configurar a atividade de pesquisa do Conjunto de dados para recuperar dinamicamente os dados do conjunto de dados de registros do AEP no tempo de execução do jornada para personalização em tempo real e lógica condicional.

**Intenções:**

* Adicione uma atividade de pesquisa do conjunto de dados a uma jornada para buscar dados de registros externos do AEP no tempo de execução
* Selecionar campos de conjunto de dados específicos (nós de folha/valores primitivos) para recuperar durante a pesquisa
* Definir uma chave de pesquisa no modo avançado para unir o contexto de jornada com registros de conjunto de dados
* Usar dados enriquecidos do conjunto de dados no editor de expressão de jornada ou no editor de personalização
* Solução de problemas de erros &quot;Pesquisa de conjunto de dados não encontrada&quot; causados pelo uso do modo simples para a chave de pesquisa

**Glossário:**

* **Atividade de pesquisa do conjunto de dados**: uma atividade de orquestração de jornada que recupera dados de conjuntos de dados de registros AEP em tempo de execução usando uma chave de junção *(específico do produto)*
* **Nó de folha**: um campo no nível mais baixo de uma hierarquia de esquema que contém um valor primitivo (sequência, número, booleano, data) *(específico do produto)*
* **Chave de pesquisa**: a expressão de associação (cadeia de caracteres ou lista de cadeias de caracteres) usada para corresponder dados de contexto de jornada com registros no conjunto de dados selecionado *(específico do produto)*
* **Dados enriquecidos**: dados recuperados por uma atividade de pesquisa do Conjunto de Dados e armazenados transitoriamente no contexto de jornada para uso em atividades downstream *(específico do produto)*

**Medidas de Proteção:**

* Máximo de 10 atividades de pesquisa do conjunto de dados por jornada.
* Máximo de 20 campos selecionados por atividade de pesquisa.
* Máximo de 50 chaves na matriz de chaves de pesquisa.
* O tamanho de dados enriquecido é limitado a 10 KB.
* O conjunto de dados deve ser ativado para pesquisa no Adobe Experience Platform antes de aparecer na configuração da atividade.
* Somente nós de folha (valores primitivos) podem ser selecionados; matrizes e mapas não podem ser selecionados.
* Somente cadeias de caracteres ou listas de cadeias de caracteres têm suporte como chaves de pesquisa.
* A chave de pesquisa deve ser definida no modo avançado; o uso do modo simples faz com que a saída da atividade fique indisponível como um atributo de contexto downstream.
* Os dados enriquecidos são transitórios e estão disponíveis apenas durante o tempo de execução do jornada e na personalização da atividade de saída.
* Para desempenho, são recomendados até 5 atividades de pesquisa por jornada e até 20 atributos por pesquisa.

**Terminologia:**

* Nome canônico: Atividade de pesquisa do conjunto de dados — Acrônimo: n/a — variantes: pesquisa de dados do AEP, atividade de enriquecimento de dados
* Sinônimos: &quot;chave de pesquisa&quot; = &quot;chave de associação&quot;
* Não confunda: &quot;Atividade de pesquisa do conjunto de dados&quot; ≠ &quot;Pesquisa de evento de experiência&quot; — a pesquisa do conjunto de dados recupera dados do conjunto de dados de registro, não eventos de experiência de série de tempo

**Perguntas frequentes:**

* **P: Por que meu conjunto de dados não aparece na lista suspensa de campos Conjunto de dados?** — O conjunto de dados deve estar habilitado para pesquisa no Adobe Experience Platform. Siga as instruções na seção Must-read para ativá-la.
* **P: Por que `@datasetLookup{}` retorna um erro &quot;Pesquisa de conjunto de dados não encontrada&quot; em uma condição?** — A chave de pesquisa foi definida usando o modo simples em vez do modo avançado. Redefina-a no modo avançado e republique a jornada.
* **P: Posso recuperar matrizes ou mapear campos do conjunto de dados?** — Não, somente campos de nó de folha primitivos (sequência, número, booleano, data) podem ser selecionados.
* **P: Como faço para acessar dados enriquecidos em um email?** — Use o editor de personalização com a sintaxe `{{context.journey.datasetLookup.<activityId>.entities}}`.
* **P: Os dados enriquecidos persistem após o término da jornada?** — Não, os dados enriquecidos são transitórios e só ficam disponíveis durante a sessão de tempo de execução do jornada.

+++
