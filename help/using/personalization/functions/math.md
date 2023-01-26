---
title: Biblioteca de funções matemáticas
description: Biblioteca de funções matemáticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# Funções matemáticas {#math}

Saiba como usar funções de Matemática no Editor de expressão.

## Absoluto    {#absolute}

O `absolute` é usada para converter um número, seu valor absoluto.

**Sintaxe**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

O `formatNumber` é usada para formatar qualquer número em sua representação sensível ao idioma.

Ele aceita um número e uma string que representa a localidade e retorna uma string formatada do número na localidade desejada.

**Sintaxe**

```sql
{%= formatNumber(number/double,string) %}: string
```

Você pode usar a formatação e as localidades válidas, conforme resumido em [Documentação do oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Localidades suportadas](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Exemplo**

Esse query retorna uma string formatada em árabe correspondente a 123456.789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

O `random` é usada para retornar um valor aleatório entre 0 e 1.

**Sintaxe**

```sql
{%= random() %}: double
```

## Arredondar para baixo {#round-down}

O `roundDown` é usada para arredondar um número.

**Sintaxe**

```sql
{%= roundDown(double) %}: double
```

## Arredondar para cima {#round-up}

O `Count only null` é usada para arredondar um número.

**Sintaxe**

```sql
{%= roundUp(double) %}: double
```

## Sequência de caracteres hexadecimal {#to-hex-string}

O `toHexString` converte qualquer número em sua string hexadecimal.

**Sintaxe**

```sql
{%= toHexString(number) %}: string
```

**Exemplo**

Esse query retorna o valor hexadecimal de 158, ou seja, 9e.

```sql
{%= toHexString(158) %}
```

## Porcentagem para {#to-percentage}

O `toPercentage` é usada para converter um número em porcentagem.

**Sintaxe**

```sql
{%= toPercentage(double) %}: string
```

## Para precisão {#to-precision}

O `toPrecision` é usada para converter um número para a precisão necessária.

**Sintaxe**

```sql
{%= toPrecision(double,int) %}: string
```

## Para string {#to-string}

O **toString** converte qualquer número em sua representação da string.

**Sintaxe**

```sql
{%= toString(string) %}: string
```

**Exemplo**

Essa query retorna &quot;12&quot;.

```sql
{%= toString(12) %} 
```
