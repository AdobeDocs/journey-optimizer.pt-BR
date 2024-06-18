---
title: Biblioteca de funções de Data e hora
description: Biblioteca de funções de Data e hora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 7%

---

# Funções de data e hora{#date-time}

As funções de data e hora são usadas para executar operações de data e hora em valores dentro do Journey Optimizer.

## Idade{#age}

A variável `age` é usada para recuperar a idade de uma determinada data.

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

## Hora atual em milissegundos{#current-time}

A variável `currentTimeInMillis` esta função é usada para recuperar a hora atual em milissegundos da época.

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

A variável `dateDiff` é usada para recuperar a diferença entre duas datas em número de dias.

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


## Dia da semana{#day-week}

A variável `dayOfWeek` é usada para recuperar o dia da semana.

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

A variável `dayOfYear` é usada para recuperar o dia do ano.

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

## Formatar data{#format-date}

A variável `formatDate` é usada para formatar um valor de data e hora. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format) %}
```

Onde a primeira string é o atributo de data e o segundo valor é como você gostaria que a data fosse convertida e exibida.

>[!NOTE]
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido em [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemplo**

A operação a seguir retornará a data no seguinte formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Formatar data com suporte local{#format-date-locale}

A variável `formatDate` A função é usada para formatar um valor de data e hora em sua representação sensível a idioma correspondente, ou seja, em um local desejado. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format, locale) %}
```

Onde a primeira string é o atributo de data, o segundo valor é como você gostaria que a data fosse convertida e exibida, e o terceiro valor representa o local no formato de string.

>[!NOTE]
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido em [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Você pode usar formatação e códigos de idiomas válidos, conforme resumido em [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Localidades suportadas](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Exemplo**

A operação a seguir retornará a data no seguinte formato: MM/DD/AA e local FRANÇA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Definir dias{#set-days}

A variável `setDays` é usada para definir o dia do mês para a data-hora especificada.

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

A variável `setHours` é usada para definir a hora da data-hora.

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


## Para UTC{#to-utc}

A variável `toUTC` é usada para converter um datetime em UTC.


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


## Semana do ano UTC{#week-of-year}

A variável `weekOfYear` é usada para recuperar a semana do ano.

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