---
product: journey optimizer
title: toDuration
description: Saiba mais sobre a função toDuration
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDuration, função, expressão, jornada
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 3%

---

# toDuration {#toDuration}

Converte um valor de argumento em uma duração. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## Categoria

Conversão

## Sintaxe da função

`toDuration(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| string | formatos baseados no formato de duração ISO-8601 PnDTnHnMn.nS com dias considerados exatamente 24 horas |
| inteiro | número de milissegundos |

Se expressão de string: os formatos aceitos são baseados no formato de duração ISO-8601 PnDTnHnMn.nS com dias considerados como sendo exatamente 24 horas.

A string começa com um sinal opcional, indicado pelo símbolo ASCII negativo ou positivo. Se negativo, todo o período é negado. A letra ASCII &quot;P&quot; é a próxima em maiúsculas ou minúsculas. Há então quatro seções, cada uma consistindo de um número e um sufixo. As seções têm sufixos em ASCII de &quot;D&quot;, &quot;H&quot;, &quot;M&quot; e &quot;S&quot; para dias, horas, minutos e segundos, aceitos em maiúsculas ou minúsculas. Os sufixos devem ocorrer em ordem. A letra ASCII &quot;T&quot; deve ocorrer antes da primeira ocorrência, se houver, de uma hora, minuto ou segunda seção. Pelo menos uma das quatro seções deve estar presente, e se &quot;T&quot; estiver presente, deve haver pelo menos uma seção após o &quot;T&quot;. A parte do número de cada seção deve consistir em um ou mais dígitos ASCII. O número pode ser prefixado pelo símbolo ASCII negativo ou positivo. O número de dias, horas e minutos que devem ser analisados. O número de segundos deve ser analisado juntamente com a fração opcional. O ponto decimal pode ser um ponto ou uma vírgula. A parte fracional pode ter de zero a nove dígitos.

## Assinaturas e tipo retornado

`toDuration(<string>)`

`toDuration(<integer>)`

Retorna uma duração.

## Exemplos

`toDuration("PT10H")`

Retorna a duração de 10 horas.

`toDuration("PT4S")`

Retorna a duração de 4s.

`toDuration(4000)`

Retorna a duração de 4s.
