---
product: journey optimizer
title: Funções de data
description: Saiba mais sobre funções de data
feature: Journeys
role: Developer
level: Experienced
keywords: data, funções, expressão, jornada, hora
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 15cd7992e3263d7d2b94cf2efe50850d16e04a5d
workflow-type: tm+mt
source-wordcount: 1384
ht-degree: 7%

---

# Funções de data {#date-functions}

As funções de data permitem manipular e trabalhar com valores de data e hora nas expressões de jornada. Essas funções são essenciais para condições baseadas em tempo, programação e cálculos temporais nas jornadas do cliente.

Use funções de data quando precisar:

* Obtenha a hora ou data atual com a manipulação de fuso horário específica ([now](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Verifique se uma data está em um intervalo de tempo específico ([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears))
* Modificar componentes de data e hora ([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone))
* Realizar cálculos e comparações com base no tempo
* Converter entre diferentes formatos de hora e representações

As funções de data fornecem controle preciso sobre a lógica temporal, permitindo que você crie caminhos de jornadas com detecção de hora e condições que respondam a cronogramas e cronogramas específicos.

>[!NOTE]
>
>As funções nesta página estão disponíveis em expressões de jornada. Algumas funções como `now()` não estão disponíveis no editor de personalização para conteúdo de email. [Saiba mais](../../personalization/functions/dates.md)

## currentTimeInMillis {#currentTimeInMillis}

Retorna a hora atual em milissegundos da época.

+++Sintaxe

`currentTimeInMillis()`

+++

+++Parâmetros

Esta função não usa parâmetros.

+++

+++Assinaturas e tipo retornado

`currentTimeInMillis()`

Retorna um inteiro.

+++

+++Exemplos

`currentTimeInMillis()`

Retorna &quot;1544712617131&quot;.

+++

## inLastDays {#inLastDays}

Retorna verdadeiro se um determinado dateTime estiver entre agora e agora - dias delta.

+++Sintaxe

`inLastDays(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inLastDays(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inLastHours {#inLastHours}

Retorna verdadeiro se a data e hora especificadas estiverem entre agora e agora - delta horas.

+++Sintaxe

`inLastHours(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inLastHours(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Retorna verdadeiro.

+++

## inLastMonths {#inLastMonths}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora - meses delta.

+++Sintaxe

`inLastMonths(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inLastMonths(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inLastYears {#inLastYears}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora - anos delta.

+++Sintaxe

`inLastYears(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inLastYears(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inNextDays {#inNextDays}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + dias delta.

+++Sintaxe

`inNextDays(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inNextDays(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inNextHours {#inNextHours}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + horas delta.

+++Sintaxe

`inNextHours(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inNextHours(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inNextMonths {#inNextMonths}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + meses delta.

+++Sintaxe

`inNextMonths(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inNextMonths(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## inNextYears {#inNextYears}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + anos delta.

+++Sintaxe

`inNextYears(<dateTime>,<delta>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

+++

+++Assinaturas e tipo retornado

`inNextYears(<dateTime>,<integer>)`

Retorna um valor booleano.

+++

+++Exemplos

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

+++

## now {#now}

Retorna a data atual no formato de data e hora. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

>[!NOTE]
>
>Esta função só está disponível em expressões de jornada. Para personalização de email e outro conteúdo, use `getCurrentZonedDateTime()`. [Saiba mais](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++Sintaxe

`now(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres | Identificador de fuso horário (opcional) |

+++

+++Assinaturas e tipo retornado

`now()`

`now("<timeZone id>")`

Retorna dateTime.

+++

+++Exemplos

`now()`

Retorna 2023-06-03T06:30Z.

`toString(now())`

Retorna &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Retorna 2023-06-03T08:30+02:00.

+++

## nowWithDelta {#nowWithDelta}

Retorna o datetime atual incluindo um deslocamento. Se uma ID de fuso horário for especificada, o deslocamento de fuso horário será aplicado. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

+++Sintaxe

`nowWithDelta(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| delta | valor inteiro positivo ou negativo |
| parte de data | anos, meses, dias, horas, minutos ou segundos como uma string |
| id do fuso horário | representação da string do valor do fuso horário. Para obter mais informações, consulte [Tipos de dados](../expression/data-types.md). A ID do fuso horário deve ser uma constante de sequência. Não pode ser uma referência de campo nem uma expressão. |

+++

+++Assinaturas e tipo retornado

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Retorna dateTime.

+++

+++Exemplos

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Retorna dateTime exatamente 2 horas atrás.

`nowWithDelta(1, "months", "Asia/Tokyo")`

Quando avaliado em 31/01/2026, retorna 28/02/2026; quando avaliado em 31/05/2026, retorna 30/06/2026...

`nowWithDelta()` usa aritmética de mês de calendário. Se o mês de destino tiver menos dias que o dia do mês atual, o resultado será normalizado para o último dia válido desse mês. A função não se estende para o mês seguinte.

+++

## setHours {#setHours}

Define apenas as horas de uma data e hora ou data e hora. Por exemplo, se você quiser aguardar até uma determinada hora amanhã, poderá forçar a hora.

+++Sintaxe

`setHours(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data hora sem considerar o fuso horário | dateTimeOnly |
| horas | inteiro |

+++

+++Assinaturas e tipo retornado

`setHours(<dateTime>,<hours>)`

Retorna um datetime.

`setHours(<dateTimeOnly>,<hours>)`

Retorna uma data e hora sem considerar o fuso horário.

+++

+++Exemplos

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Retorna amanhã às 20h00, sendo XY os minutos no momento da avaliação de hora atual. :XYSe a avaliação ocorrer às 2:45 AM, a hora retornada será 20:45 PM.

+++

## setDays {#setDays}

Define apenas o dia de uma data e hora ou data e hora. Por exemplo, se você quiser aguardar até um determinado dia do mês, poderá forçar o dia.

+++Sintaxe

`setDays(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data hora sem considerar o fuso horário | dateTimeOnly |
| dias | inteiro |

+++

+++Assinaturas e tipo retornado

`setDays(<dateTime>,<days>)`

Retorna um datetime.

`setDays(<dateTimeOnly>,<days>)`

Retorna uma data e hora sem considerar o fuso horário.

+++

+++Exemplos

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Retorna 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Retorna uma nova data e hora, com um novo fuso horário no mesmo instante.

+++Sintaxe

`updateTimeZone(<parameters>)`

+++

+++Parâmetros

* id do fuso horário: string
* dateTime

+++

+++Assinatura e tipo retornado

`updateTimeZone(<dateTime>,<timeZone id>)`

Retorna um datetime.

+++

+++Exemplos

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Retorna 28/08/2023:15:30.123+02:00.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Se o valor do campo de carimbo de data/hora for `2021-11-16T16:55:12.939318+01:00`, a função retornará `2021-11-17T02:55:12.942115+11:00`.

+++

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta todas as funções de data e hora disponíveis nas expressões do AJO jornada, abordando como obter a hora atual, verificar se uma data se enquadra em uma janela de tempo relativa e modificar componentes de data/hora.

**Intenções:**
* Obter o datetime atual (com fuso horário opcional) usando `now` ou `nowWithDelta`
* Recuperar a hora atual como um inteiro da época usando `currentTimeInMillis`
* Verifique se um datetime está nos últimos N dias, horas, meses ou anos usando `inLastDays`, `inLastHours`, `inLastMonths`, `inLastYears`
* Verifique se um datetime está nos próximos N dias, horas, meses ou anos usando `inNextDays`, `inNextHours`, `inNextMonths`, `inNextYears`
* Forçar uma hora ou dia específico do mês em um valor datetime usando `setHours` ou `setDays`
* Converta um datetime em um fuso horário diferente, preservando o mesmo instante usando `updateTimeZone`

**Glossário:**
* **dateTime**: um valor date-time que inclui informações de deslocamento de fuso horário *(específico do produto)*
* **dateTimeOnly**: um valor date-time sem informações de fuso horário *(específico do produto)*
* **milissegundos da época**: um número inteiro que representa o número de milissegundos decorridos desde 1970-01-01T00:00:00Z
* **delta**: um deslocamento inteiro (positivo ou negativo) usado com `nowWithDelta` para deslocar a hora atual por um número de anos, meses, dias, horas, minutos ou segundos

**Medidas de Proteção:**
* `now()` está disponível somente em expressões jornada; para personalização de email, use `getCurrentZonedDateTime()`
* A ID do fuso horário em `nowWithDelta` deve ser uma constante de cadeia de caracteres — não há suporte para referências de campo e expressões dinâmicas
* A ID do fuso horário em `updateTimeZone` deve ser uma constante de cadeia de caracteres

**Terminologia:**
* Nome canônico: Funções de data — Acrônimo: none — variantes: funções de data e hora, funções temporais
* Sinônimos: &quot;now()&quot; = &quot;current datetime&quot;; &quot;currentTimeInMillis()&quot; = &quot;current epoch miliseconds&quot;
* Não confunda: &quot;inLastDays&quot; (retroage no tempo) ≠ &quot;inNextDays&quot; (retroage no tempo)
* Não confunda: &quot;setHours&quot; (substitui o componente de hora) ≠ &quot;nowWithDelta&quot; (desloca a hora atual)
* Não confunda: &quot;updateTimeZone&quot; (mesmo instante, representação de fuso horário diferente) ≠ &quot;setHours&quot; (altera o valor de tempo em si)

**Perguntas frequentes:**
* **P: Posso usar `now()` no conteúdo de personalização de email?** — Não, `now()` está disponível somente em expressões de jornada. Use `getCurrentZonedDateTime()` para personalização de email.
* **P: Como verificar se um evento aconteceu nas últimas 24 horas?** — Use `inLastHours(@event{MyEvent.timestamp}, 24)`.
* **P: Como faço para obter a diferença de tempo atual de 2 horas no passado?** — Use `nowWithDelta(-2, "hours")`.
* **P: O que `updateTimeZone` faz de diferente de `setHours`?** — `updateTimeZone` mantém o mesmo instante de tempo, mas o expressa em um fuso horário diferente, enquanto `setHours` altera o componente de hora do valor datetime.
* **P: O parâmetro de fuso horário em `nowWithDelta` pode ser um campo de perfil?** — Não, a ID do fuso horário deve ser uma constante de cadeia de caracteres; não há suporte para referências de campo.
* **P: O que acontece quando `nowWithDelta()` é usado com meses e a data atual é uma data de fim de mês?** — A função usa aritmética de mês-calendário e normaliza o resultado para o último dia válido do mês de destino. Por exemplo, adicionar 1 mês a 31 de janeiro retorna 28 de fevereiro (não 3 de março).

+++
