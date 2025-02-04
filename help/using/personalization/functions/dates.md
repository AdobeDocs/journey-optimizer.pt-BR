---
title: Biblioteca de funções de Data e hora
description: Biblioteca de funções de Data e hora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 11%

---

# Funções de data e hora{#date-time}

As funções de data e hora são usadas para executar operações de data e hora em valores dentro do Journey Optimizer.

## Adicionar dias {#add-days}

A função `addDays` ajusta uma determinada data por um número especificado de dias, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addDays(date, number) %}
```

+++Exemplo

* Entrada: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-11T17:19:51Z`

+++

## Adicionar horas {#add-hours}

A função `addHours` ajusta uma determinada data por um número especificado de horas, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addHours(date, number) %}
```

+++Exemplo

* Entrada: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Saída: `2024-11-01T18:19:51Z`

+++

## Adicionar minutos {#add-minutes}

A função `addMinutes` ajusta uma determinada data por um número especificado de minutos, usando valores positivos para incrementar e valores negativos para decrementar

**Sintaxe**

```sql
{%= addMinutes(date, number) %}
```

+++Exemplo

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Saída: `2024-11-01T18:09:51Z`

+++

## Adicionar meses {#add-months}

A função `addMonths` ajusta uma determinada data por um número especificado de meses, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addMonths(date, number) %}
```

+++Exemplo

* Entrada: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2025-01-01T17:19:51Z`

+++

## Adicionar segundos {#add-seconds}

O `addSeconds` ajusta uma determinada data por um número especificado de segundos, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addSeconds(date, number) %}
```

+++Exemplo

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-01T17:20:01Z`

+++

## Adicionar anos {#add-years}

O `addYears` ajusta uma determinada data por um número especificado de anos, usando valores positivos para incrementar e valores negativos para diminuir.

**Sintaxe**

```sql
{%= addYears(date, number) %}
```

+++Exemplo

* Entrada: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2026-11-01T17:19:51Z`

+++

## Idade{#age}

A função `age` é usada para recuperar a idade de uma determinada data.

**Sintaxe**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Idade em dias {#age-days}

A função `ageInDays` calcula a idade de uma determinada data em dias, ou seja, o número de dias decorridos entre a determinada data e a data atual, negativo para datas futuras e positivo para datas passadas.

**Sintaxe**

```sql
{%= ageInDays(date) %}
```

+++Exemplo

currentDate = 2025-01-07T12:17:10.720122+05:30 (Ásia/Calcutá)

* Entrada: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Saída: `5`

+++

## Idade em meses {#age-months}

A função `ageInMonths` calcula a idade de uma determinada data em meses, ou seja, o número de meses decorridos entre a determinada data e a data atual , negativo para datas futuras e positivo para datas passadas.

**Sintaxe**

```sql
{%= ageInMonths(date) %}
```

+++Exemplo

currentDate = 2025-01-07T12:22:46.993748+05:30(Ásia/Calcutá)

* Entrada: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Saída: `12`

+++

## Comparar datas {#compare-dates}

A função `compareDates` compara a primeira data de entrada com a outra. Retorna 0 se data1 for igual a data2, -1 se data1 for anterior a data2 e 1 se data1 for posterior a data2.

**Sintaxe**

```sql
{%= compareDates(date1, date2) %}
```

+++Exemplo

* Entrada: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Saída: `-1`

+++

## Converter ZonedDateTime {#convert-zoned-date-time}

A função `convertZonedDateTime` converte uma data-hora em um determinado fuso horário.

**Sintaxe**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Exemplo

* Entrada: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Saída: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Hora atual em milissegundos{#current-time}

A função `currentTimeInMillis` é usada para recuperar a hora atual em milissegundos da época.

**Sintaxe**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Diferença de data{#date-diff}

A função `dateDiff` é usada para recuperar a diferença entre duas datas em número de dias.

**Sintaxe**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Dia do mês {#day-month}

`dayOfWeek` retorna o número que representa o dia do mês.

**Sintaxe**

```sql
{%= dayOfMonth(datetime) %}
```

+++Exemplo

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Saída: `5`

+++


## Dia da semana {#day-week}

A função `dayOfWeek` é usada para recuperar o dia da semana.

**Sintaxe**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Dia do ano{#day-year}

A função `dayOfYear` é usada para recuperar o dia do ano.

**Sintaxe**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Diferença em segundos {#diff-seconds}

A função `diffInSeconds` retorna a diferença entre duas datas em termos de segundos.

**Sintaxe**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Saída: `50`

+++

## Extrair horas {#extract-hours}

A função `extractHours` extrai o componente de hora de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractHours(date) %}
```

+++Exemplo

* Entrada: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `17`

+++

## Extrair minutos {#extract-minutes}

A função `extractMinutes` extrai o componente de minuto de um carimbo de data/hora especificado.

**Sintaxe**

```sql
{%= extractMinutes(date) %}
```

+++Exemplo

* Entrada: `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `19`

+++

## Extrair meses {#extract-months}

A função `extractMonth` extrai o componente de mês de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractMonths(date) %}
```

+++Exemplo

* Entrada: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `11`

+++

## Extrair segundos {#extract-seconds}

A função `extractSeconds` extrai o segundo componente de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractSeconds(date) %}
```

+++Exemplo

* Entrada: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `51`

+++

## Formatar data{#format-date}

A função `formatDate` é usada para formatar um valor de data e hora. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format) %}
```

Onde a primeira string é o atributo de data e o segundo valor é como você gostaria que a data fosse convertida e exibida.

>[!NOTE]
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemplo**

A operação a seguir retornará a data no seguinte formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Formatar data com suporte local{#format-date-locale}

A função `formatDate` é usada para formatar um valor de data e hora em sua representação sensível a idioma correspondente, ou seja, em um local desejado. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format, locale) %}
```

Onde a primeira string é o atributo de data, o segundo valor é como você gostaria que a data fosse convertida e exibida, e o terceiro valor representa o local no formato de string.

>[!NOTE]
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Você pode usar formatação e localidades válidas conforme resumido em [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Localidades com suporte](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exemplo**

A operação a seguir retornará a data no seguinte formato: MM/DD/AA e local FRANÇA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Obter CurrentZonedDateTime {#get-current-zoned-date-time}

A função `getCurrentZonedDateTime` retorna a data e a hora atuais com informações de fuso horário.

**Sintaxe**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Exemplo

* Entrada: `{%= getCurrentZonedDateTime() %}`
* Saída: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Diferença em horas {#hours-difference}

A função `diffInHours` retorna a diferença entre duas datas em termos de horas.

**Sintaxe**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Saída: `10`

+++

## Diferença em minutos{#diff-minutes}

A função `diffInMinutes` é usada para retornar a diferença entre duas datas em termos de minutos.

**Sintaxe**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Saída: `60`

+++

## Diferença em meses {#months-difference}

A função `diffInMonths` retorna a diferença entre duas datas em termos de meses.

**Sintaxe**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Saída: `3`

+++

## Definir dias{#set-days}

A função `setDays` é usada para definir o dia do mês para a data-hora especificada.

**Sintaxe**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Definir horas{#set-hours}

A função `setHours` é usada para definir a hora da data-hora.

**Sintaxe**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Para data hora {#to-date-time}

A função `ToDateTime` converte a cadeia de caracteres em data. Retorna a data da época como saída para entrada inválida.

**Sintaxe**

```sql
{%= toDateTime(string, string) %}
```

+++Exemplo

* Entrada: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Saída: `2024-11-01T17:19:51Z`

+++

## Para UTC{#to-utc}

A função `toUTC` é usada para converter um datetime em UTC.

**Sintaxe**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Vincular ao início do dia {#truncate-day}

A função `truncateToStartOfDay` é usada para modificar uma determinada data-hora, definindo-a para o início do dia com a hora definida como 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Exemplo

* Entrada: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Saída: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

A função `truncateToStartOfQuarter` é usada para truncar uma data e hora no primeiro dia de seu trimestre (por exemplo, 1° de janeiro, 1° de abril, 1° de julho, 1° de outubro) às 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Exemplo

* Entrada: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

A função `truncateToStartOfWeek` modifica uma determinada data-hora definindo-a para o início da semana (segunda-feira às 00:00).

**Sintaxe**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Exemplo

* Entrada: `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Saída: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

A função `truncateToStartOfYear` é usada para modificar uma determinada data-hora, truncando-a para o primeiro dia do ano (1º de janeiro) às 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Exemplo

* Entrada: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-01-01T00:00Z`

+++

## Semana do ano {#week-of-year}

A função `weekOfYear` é usada para recuperar a semana do ano.

**Sintaxe**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Diferença em anos {#diff-years}

A função `diffInYears` é usada para retornar a diferença entre duas datas em termos de anos.

**Sintaxe**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Exemplo

* Entrada: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Saída: `5`

+++
