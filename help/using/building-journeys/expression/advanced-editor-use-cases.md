---
solution: Journey Optimizer
product: journey optimizer
title: Uso do editor de expressão avançado
description: Saiba como criar expressões avançadas
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: expressão, condição, casos de uso, eventos
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 2%

---

# Exemplos de expressão avançada{#advanced-expression-examples}

O editor de expressão avançado pode ser usado para criar condições que permitem filtrar usuários em suas jornadas. Essas condições permitem direcionar os usuários no prazo, data, local, duração para que eles possam ser redirecionados na jornada.

>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../exp-event-lookup.md)


## Criação de condições em Eventos de experiência


>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../exp-event-lookup.md)
>



O editor de expressão avançado é obrigatório para executar consultas em séries de tempo, como uma lista de compras ou cliques anteriores em mensagens. Essas consultas não podem ser executadas usando o editor simples.

>[!NOTE]
>
>Eventos começam com @, fontes de dados com #.

Os eventos de experiência são recuperados do Adobe Experience Platform como uma coleção em ordem cronológica inversa, portanto:

* a primeira função retornará o evento mais recente
* a última função retornará a mais antiga.

Por exemplo, digamos que você queira direcionar os clientes com um abandono de carrinho nos últimos 7 dias para enviar uma mensagem quando o cliente estiver chegando perto de uma loja, com uma oferta nos itens desejados que estão na loja.

**Você precisa criar as seguintes condições:**

Primeiro de tudo, clientes-alvo que navegaram na loja online, mas não finalizaram o pedido nos últimos sete dias.

**Esta expressão procura um valor especificado em um valor de cadeia de caracteres:**

`In ("addToCart", #{field reference from experience event})`

**Esta expressão procura todos os eventos para este usuário especificado nos últimos 7 dias:**

Em seguida, ele seleciona todos os eventos de adição ao carrinho que não se transformaram em uma compra completa.

>[!NOTE]
>
>Para inserir campos na expressão rapidamente, clique duas vezes no campo no painel esquerdo do editor.

O carimbo de data e hora especificado está agindo como o valor de data e hora, o segundo é o número de dias.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Essa expressão retorna um valor booleano.

**Agora vamos criar uma expressão verificando se o produto está em estoque**

* No Inventário, essa expressão procura o campo de quantidade de um produto e especifica que ele deve ser maior que 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* À direita, os valores necessários são especificados, aqui, precisamos recuperar o local do armazenamento, que é mapeado do local do evento &quot;ArriveLumaStudio&quot;:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* E especifique SKU, usando a função `first` para recuperar a interação &quot;addToCart&quot; mais recente:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

A partir daí, você pode adicionar outro caminho na jornada para quando o produto não estiver na loja e enviar uma notificação com oferta de engajamento. Configure as mensagens de acordo e use dados de personalização para aprimorar o público-alvo da mensagem.

## Filtragem de carimbo de data e hora em expressões

Ao referenciar vários eventos de atividade do carrinho, especifique uma janela de carimbo de data e hora de início e de término para evitar a coleta de dados históricos. Por exemplo:

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

## Exemplos de manipulações de cadeias de caracteres com o editor de expressão avançado

**Em condições**

Essa condição recupera apenas os eventos de geofence acionados em &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explicação: Esta é uma comparação de sequência estrita (diferencia maiúsculas de minúsculas), equivalente a uma consulta no modo simples que usa `equal to` com `Is sensitive` marcado.

A mesma consulta com `Is sensitive` desmarcado gerará a seguinte expressão no modo avançado:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**Em ações**

A seguinte expressão permite definir a ID do CRM em um campo de personalização de ação:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Explicação: Este exemplo usa as funções `substr` e `lastIndexOf` para remover chaves que delimitam a ID do CRM transmitida com um evento de inicialização de aplicativo móvel.


Para obter mais informações sobre como usar o editor de expressão avançado, assista a [este vídeo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=pt-BR).

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página fornece exemplos práticos do uso do editor de expressão avançado para criar condições de jornada que filtram os usuários por atividade do carrinho, status do inventário, eventos de geofence, manipulações de cadeias de caracteres e janelas de carimbo de data/hora.

**Intenções:**

* Criar uma condição de abandono de carrinho usando `in()` e `inLastDays()` para direcionar usuários que adicionaram itens, mas não concluíram a compra em 7 dias
* Filtrar coleções de eventos de experiência por janela de carimbo de data e hora para evitar a captura de dados históricos
* Aplicar comparações de cadeias de caracteres que diferenciam maiúsculas de minúsculas e que não diferenciam maiúsculas de minúsculas a campos de eventos de geofence
* Extrair e manipular IDs de CRM de eventos de inicialização de aplicativo móvel usando `substr` e `lastIndexOf`
* Verificar a disponibilidade do estoque de produtos comparando um campo de quantidade com um limite
* Combinar várias expressões booleanas usando a lógica `and` / `not` em condições de jornada

**Glossário:**

* **Editor de expressão avançado**: a interface do Journey Optimizer para gravar expressões complexas de nível de código usando funções, operadores e referências de campo *(específico do produto)*
* **currentDataPackField**: Uma variável de loop usada ao iterar em coleções de fonte de dados dentro de `all()`, `first()` ou `last()` funções *(específico do produto)*
* **inLastDays(timestamp, N)**: uma função de data que retorna verdadeiro se o carimbo de data/hora fornecido estiver nos últimos N dias *(específico do produto)*
* **Eventos de experiência**: registros de dados comportamentais de série temporal armazenados no Adobe Experience Platform, recuperados em ordem cronológica inversa *(específico do produto)*

**Medidas de Proteção:**

* Não há suporte para o uso de eventos de experiência diretamente em expressões/condições de jornada; métodos alternativos, como atributos computados ou segmentos de público-alvo, devem ser usados
* O editor de expressão avançado deve ser usado (não o editor simples) para consultas em dados de série temporal, como coleções de compras ou cliques
* Clicar duas vezes em um campo no painel esquerdo o insere rapidamente na expressão; evite digitar caminhos de campo manualmente para reduzir erros
* Os eventos de experiência de consulta de expressões retornam um booleano; verifique se a lógica downstream espera um tipo booleano

**Terminologia:**

* Nome canônico: Editor de expressão avançado — Acrônimo: none — variantes: editor de expressão, editor avançado
* Sinônimos: &quot;addToCart&quot; = &quot;adicionar à interação do carrinho&quot;; &quot;completePurchase&quot; = &quot;evento de conclusão de compra&quot;
* Não confundir: eventos (com prefixo `@`) ≠ fontes de dados (com prefixo `#`)

**Perguntas frequentes:**

* **P: Por que devo usar o editor avançado em vez do editor simples para consultas de abandono de carrinho?** — O editor simples não pode executar consultas em coleções de série temporal; o editor avançado é necessário para as funções de coleção `all()`, `first()` e `last()`.
* **P: Como faço referência ao evento &quot;addToCart&quot; mais recente em uma expressão?** — Use a função `first()` na coleção de eventos de experiência filtrada por `productInteraction == "addToCart"`, já que os eventos são retornados em ordem cronológica inversa.
* **P: Como faço para que uma comparação de cadeias de caracteres não diferencie maiúsculas de minúsculas no editor avançado?** — Use a função `equalIgnoreCase()` em vez do operador `==`.
* **P: Qual é a finalidade de adicionar uma janela de carimbo de data/hora ao consultar eventos do carrinho?** — A especificação de um carimbo de data e hora de início e término impede a coleta de dados históricos que estejam fora da janela de atividade desejada.
* **P: Como remover chaves de uma cadeia de caracteres da ID do CRM transmitida em um evento?** — Use `substr()` combinado com `lastIndexOf()` para extrair o conteúdo entre as chaves.

+++
