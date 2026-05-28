---
title: Biblioteca de funções matemáticas
description: Biblioteca de funções matemáticas
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 6%

---

# Funções matemáticas {#math}

Saiba como usar funções matemáticas no editor de personalização.

## Absoluto {#absolute}

A função `absolute` é usada para converter um número em seu valor absoluto.

**Sintaxe**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

A função `formatNumber` é usada para formatar qualquer número em sua representação sensível a linguagem.

Ele aceita um número e uma string representando o local e retorna uma string formatada do número no local desejado.

**Sintaxe**

```sql
{%= formatNumber(number/double,string) %}: string
```

Você pode usar formatação e localidades válidas conforme resumido na [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e nas [Localidades com suporte](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Exemplo**

Esta consulta retorna uma string formatada em árabe correspondente a 123456.789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Aleatória {#random}

A função `random` é usada para retornar um valor aleatório entre 0 e 1.

**Sintaxe**

```sql
{%= random() %}: double
```

## Arredondar para baixo {#round-down}

A função `roundDown` é usada para arredondar para baixo um número.

**Sintaxe**

```sql
{%= roundDown(double) %}: double
```

## Arredondar para cima {#round-up}

A função `roundUp` é usada para arredondar um número para cima.

**Sintaxe**

```sql
{%= roundUp(double) %}: double
```

## Para hex string {#to-hex-string}

A função `toHexString` converte qualquer número em sua cadeia de caracteres hexadecimal.

**Sintaxe**

```sql
{%= toHexString(number) %}: string
```

**Exemplo**

Este query retorna o valor hexadecimal de 158, ou seja, 9e.

```sql
{%= toHexString(158) %}
```

## Para Int {#to-int}

A função `toInt` é usada para converter qualquer um desses tipos (número, duplo, int, longo, flutuante, curto, byte, booleano, string) em um inteiro.

**Sintaxe**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Exemplo**

Esta consulta retorna o valor inteiro de 42,6, ou seja, 42.

```sql
{%= toInt(42.6) %}: integer
```

## Para porcentagem {#to-percentage}

A função `toPercentage` é usada para converter um número em porcentagem.

**Sintaxe**

```sql
{%= toPercentage(double) %}: string
```

## Para precisão {#to-precision}

A função `toPrecision` é usada para converter um número para a precisão necessária.

**Sintaxe**

```sql
{%= toPrecision(double,int) %}: string
```

## Para string {#to-string}

A função **toString** converte qualquer número em sua representação de cadeia de caracteres.

**Sintaxe**

```sql
{%= toString(string) %}: string
```

**Exemplo**

Essa consulta retorna &quot;12&quot;.

```sql
{%= toString(12) %} 
```
