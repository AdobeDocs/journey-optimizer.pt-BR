---
title: Biblioteca de funções de Data e Hora
description: Biblioteca de funções de Data e Hora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# Funções de Data/Hora{#date-time}

As funções de data e hora são usadas para executar operações de data e hora em valores no Journey Optimizer.

## Idade{#age}

O `age` é usada para recuperar a idade de uma determinada data.

**Formato**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## Hora atual em milissegundos{#current-time}

O `currentTimeInMillis` é usada para recuperar o tempo atual em milissegundos de época.

**Formato**

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

O `dateDiff` é usada para recuperar a diferença entre duas datas em número de dias.

**Formato**

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

O `dayOfWeek` é usada para recuperar o dia da semana.

**Formato**

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

O `dayOfYear` é usada para recuperar o dia do ano.

**Formato**

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

## Data de formato{#format-date}

O `formatDate` é usada para formatar um valor de data e hora. O formato deve ser um padrão Java DateTimeFormat válido.

**Formato**

```sql
{%= formatDate(date, format) %}
```

Onde a primeira string é o atributo date e o segundo valor é como você gostaria que a data fosse convertida e exibida.

>[!NOTE]
>
> Se um padrão de data for inválido, a data retornará para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java como resumidas [na documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemplo**

A seguinte operação retornará a data no seguinte formato: DD/MM/YY

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Definir dias{#set-days}

O `setDays` é usada para definir o dia do mês para determinada data-hora.

**Formato**

```sql
{%= setDays(date, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Definir horas{#set-hours}

O `setHours` é usada para definir a hora da data-hora.

**Formato**

```sql
{%= setHours(date, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Para UTC{#to-utc}

O `toUTC` é usada para converter um datetime em UTC.


**Formato**

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

O `weekOfYear` é usada para recuperar a semana do ano.

**Formato**

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
