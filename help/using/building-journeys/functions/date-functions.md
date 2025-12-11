---
product: journey optimizer
title: Funções de data
description: Saiba mais sobre funções de data
feature: Journeys
role: Developer
level: Experienced
keywords: data, funções, expressão, jornada, hora
version: Journey Orchestration
source-git-commit: 8ca1c995bc38b110fa07573f922906c775fd5e6f
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 11%

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

Retorna amanhã às 20h00, sendo XY os minutos no momento da avaliação de hora atual. :XY Se a avaliação ocorrer às 2:45 AM, a hora retornada será 20:45 PM.

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

