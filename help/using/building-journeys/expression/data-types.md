---
solution: Journey Optimizer
product: journey optimizer
title: Tipos de dados
description: Saiba mais sobre os tipos de dados em expressões avançadas
feature: Journeys
role: Developer
level: Experienced
keywords: expressão, dados, tipo de dados, jornada
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 3%

---

# Tipos de dados {#data-types}

Tecnicamente, uma constante sempre contém um tipo de dados. Na expressão literal, especificamos apenas o valor. O tipo de dados pode ser inferido a partir do valor (por exemplo, string, inteiro, decimal etc.). Para casos específicos, como data e hora, usamos funções dedicadas para a representação.

As seções abaixo fornecem informações sobre as diferentes expressões de tipos de dados e como elas são representadas.

## sequência de caracteres {#string}

**Descrição**

Sequência comum de caracteres. Ele não tem um tamanho específico, exceto o implícito que vem do ambiente, como a quantidade de memória disponível.

Formato JSON: string

Formato de serialização: UTF-8

**Representação literal**

```json
"<value>"
```

```json
'<value>'
```

**Exemplo**

```json
"hello world"
```

```json
'hello world'
```

## inteiro {#integer}

**Descrição**

Valor inteiro de -2^63 a 2^63-1.

Formato JSON: número

**Representação literal**

```json
<integer value>
```

**Exemplo**

```json
42
```

## decimal {#decimal}

**Descrição**

Número decimal. Ele representa um valor flutuante:

* maior valor finito positivo do tipo double, (2-2^-52)x2^1023
* menor valor normal positivo do tipo double, 2-1022
* menor valor positivo diferente de zero do tipo double, 2 p-1074

Formato JSON: número

Formato de serialização: usando &#39;.&#39; como separador decimal.

**Representação literal**

```json
<integer value>.<integer value>
```

**Exemplo**

```json
3.14
```

## booleano {#boolean}

**Descrição**

Valor booleano gravado em minúsculas: verdadeiro ou falso

Formato JSON: booleano

**Representação literal**

```json
true
```

```json
false
```

**Exemplo**

```json
true
```

## dateOnly {#date-only}

**Descrição**

Representa uma data somente sem um fuso horário, visualizado como um dia-mês-ano.

É uma descrição da data, como usada para aniversários.

Formato JSON: cadeia de caracteres.

O formato é: AAAA-MM-DD (ISO-8601), por exemplo: &quot;2021-03-11&quot;.

Ele pode ser encapsulado em uma função toDateOnly.

Ele usa DateTimeFormatter ISO_LOCAL_DATE_TIME para desserializar e serializar o valor. [Saiba mais](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Representação literal**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Exemplo**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Descrição**

Representa uma data e hora sem um fuso horário, visualizado como ano-mês-dia-hora-minuto-segundo-milissegundo.

Formato JSON: cadeia de caracteres.

Ele não armazena ou representa um fuso horário. Em vez disso, é uma descrição da data, como usada para aniversários, combinada com a hora local, como visto em um relógio de parede.

Ele não pode representar um instante na linha do tempo sem informações adicionais, como um deslocamento ou fuso horário.

Ele pode ser encapsulado em uma função toDateTimeOnly.

Formato de serialização: formato de data-hora de deslocamento estendido ISO-8601.

Ele usa DateTimeFormatter ISO_LOCAL_DATE_TIME para desserializar e serializar o valor. [Saiba mais](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME"){_blank}.

**Representação literal**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Exemplos**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**Descrição**

Constante de data e hora que também considera o fuso horário. Ele representa uma data e hora com um deslocamento de UTC.

Ele pode ser visto como um instante de tempo com as informações adicionais do deslocamento. É uma forma de representar um &quot;momento&quot; específico em um determinado lugar do mundo.

Formato JSON: cadeia de caracteres.

Ele pode ser encapsulado em uma função toDateTime.

Formato de serialização: formato de data-hora de deslocamento estendido ISO-8601.

Ele usa DateTimeFormatter ISO_OFFSET_DATE_TIME para desserializar e serializar o valor. [Saiba mais](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}.

Você também pode passar um número inteiro passando um valor de época. [Leia mais](https://www.epochconverter.com){_blank}.

O fuso horário pode ser especificado por um deslocamento ou um código de fuso horário (por exemplo: Europa/Paris, Z - significando UTC).

**Representação literal**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**Exemplos**

```json
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## duração {#duration}

**Descrição**

Ela representa uma quantidade de tempo baseada no tempo, como &quot;34,5 segundos&quot;. Ele modela uma quantidade ou quantidade de tempo em termos de milissegundos.

As unidades temporais suportadas são: milissegundos, segundos, minutos, horas, dias onde um dia equivale a 24 horas. Não há suporte para anos e meses, pois eles não são uma quantidade fixa de tempo.

Formato JSON: cadeia de caracteres.

Ele deve ser encapsulado em uma função toDuration.

Formato de serialização: para desserializar uma ID de fuso horário, ele usa a função java java.time.

Duration.parse: os formatos aceitos são baseados no formato de duração ISO-8601 PnDTnHnMn.nS com dias considerados exatamente 24 horas. [Saiba mais](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}.

**Representação literal**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**Exemplo**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## list {#list}

**Descrição**

Lista separada por vírgulas de expressões usando colchetes como delimitadores.

Não há suporte para polimorfismo, portanto, todas as expressões contidas na lista devem ter o mesmo tipo.

**Representação literal**

```json
[<expression>, <expression>, ... ]
```

**Exemplo**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página descreve cada tipo de dados com suporte no editor de expressão avançado de Jornada — cadeia de caracteres, inteiro, decimal, booleano, dateOnly, dateTimeOnly, dateTime, duration e list — com seus formatos JSON, regras de serialização e sintaxe de representação literal.

**Intenções:**

* Identificar a sintaxe literal correta para cada tipo de dados ao gravar expressões de jornada
* Entenda a diferença entre os tipos `dateOnly`, `dateTimeOnly` e `dateTime` e quando usar cada um
* Representa um valor de duração usando o formato ISO-8601 ou milissegundos com a função `toDuration()`
* Construir uma expressão de lista com sintaxe de colchetes para uso em operações de coleta
* Usar funções de conversão (`toDateTime`, `toDateTimeOnly`, `toDuration`, `toDateOnly`) para criar constantes digitadas

**Glossário:**

* **dateOnly**: uma data sem hora ou fuso horário, formatada como AAAA-MM-DD; adequada para aniversários ou datas do calendário *(específica do produto)*
* **dateTimeOnly**: uma data e hora sem informações de fuso horário; não pode representar um instante específico sem um deslocamento *(específico do produto)*
* **dateTime**: uma constante de data-hora que inclui um deslocamento UTC, representando um instante específico; também pode ser criada a partir de um inteiro da época *(específico do produto)*
* **duração**: uma quantidade baseada em tempo modelada em milissegundos; usa o formato ISO-8601 `PnDTnHnMn.nS`; anos e meses não são suportados *(específico do produto)*
* **lista**: uma coleção separada por vírgulas de expressões do mesmo tipo, delimitada por colchetes *(específico do produto)*

**Medidas de Proteção:**

* A duração é compatível somente com milissegundos, segundos, minutos, horas e dias — anos e meses não são compatíveis, pois não são períodos fixos
* Um valor `duration` deve ser ajustado em `toDuration()` — ele não pode ser expresso como um literal simples
* Todas as expressões em um `list` devem ter o mesmo tipo — não há suporte para polimorfismo
* `dateTimeOnly` não pode representar um instante de tempo sem um deslocamento ou fuso horário adicional

**Terminologia:**

* Nome canônico: Tipos de dados — Acrônimo: none — variantes: tipos de dados de expressão, tipos de dados de jornada
* Sinônimos: &quot;dateTime&quot; = &quot;date-time com fuso horário&quot;; &quot;dateTimeOnly&quot; = &quot;date-time local&quot;
* Não confundir: `dateOnly` (sem hora) ≠ `dateTimeOnly` (data + hora, sem fuso horário) ≠ `dateTime` (data + hora + fuso horário/deslocamento)

**Perguntas frequentes:**

* **P: Qual é a diferença entre `dateTimeOnly` e `dateTime`?** — `dateTimeOnly` não tem fuso horário ou deslocamento e não pode representar um instante preciso; `dateTime` inclui um deslocamento UTC e representa um momento específico.
* **P: Como posso expressar uma duração de 2 dias e 3 horas?** — Use `toDuration("P2DT3H")`.
* **P: Posso misturar inteiros e cadeias de caracteres em uma expressão de lista?** — Não; todas as expressões em uma lista devem ser do mesmo tipo.
* **P: Como faço para criar um `dateTime` a partir de um carimbo de data e hora de época em milissegundos?** — Use `toDateTime(<epoch in milliseconds>)`, por exemplo `toDateTime(1560762190189)`.
* **P: `true` ou `True` é o literal booleano correto?** — Use minúsculas `true` ou `false`; variantes em maiúsculas não são válidas.

+++
