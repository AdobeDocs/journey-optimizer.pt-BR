---
title: Biblioteca de funções matemáticas
description: Biblioteca de funções matemáticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Funções matemáticas {#math}

Saiba como usar funções de Matemática no Editor de expressão.

## Absoluto    {#absolute}

O `absolute` é usada para converter um número, seu valor absoluto.

**Formato**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

O `random` é usada para retornar um valor aleatório entre 0 e 1.

**Formato**

```sql
{%= random() %}: double
```

## Arredondar para baixo {#round-down}

O `roundDown` é usada para arredondar um número.

**Formato**

```sql
{%= roundDown(double) %}: double
```

## Arredondar para cima {#round-up}

O `Count only null` é usada para arredondar um número.

**Formato**

```sql
{%= roundUp(double) %}: double
```

## Porcentagem para {#to-percentage}

O `toPercentage` é usada para converter um número em porcentagem.

**Formato**

```sql
{%= toPercentage(double) %}: string
```

## Para precisão {#to-precision}

O `toPrecision` é usada para converter um número para a precisão necessária.

**Formato**

```sql
{%= toPrecision(double,int) %}: string
```
