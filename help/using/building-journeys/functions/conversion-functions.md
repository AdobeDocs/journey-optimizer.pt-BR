---
product: journey optimizer
title: Funções de conversão
description: Saiba mais sobre funções de conversão
feature: Journeys
role: Developer
level: Experienced
keywords: conversão, funções, expressão, jornada, tipo, conversão
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 6%

---

# Funções de conversão {#conversion-functions}

As funções de conversão permitem transformar dados de um tipo para outro nas expressões de jornada. Essas funções são essenciais para garantir a compatibilidade de dados e o manuseio adequado de tipos ao trabalhar com diferentes fontes de dados e operações.

Use as funções de conversão quando precisar:

* Converter valores de cadeia de caracteres em tipos numéricos, booleanos ou de data ([toInteger](#toInteger), [toDecimal](#toDecimal), [toBool](#toBool))
* Transforme datas e horas entre diferentes formatos e representações ([toDateTime](#toDateTime), [toDateTimeOnly](#toDateTimeOnly), [toDateOnly](#toDateOnly))
* Conversão de valores numéricos entre tipos inteiros e decimais ([toInteger](#toInteger), [toDecimal](#toDecimal))
* Converter valores para formato de cadeia de caracteres ([toString](#toString)) ou duração ([toDuration](#toDuration))
* Garantir compatibilidade de tipo para comparações e operações
* Processar dados de fontes externas que podem ter diferentes formatos de tipo

Cada função de conversão lida automaticamente com regras específicas de tipo e casos de borda, tornando a transformação de dados mais confiável e previsível em suas expressões de jornada.

## toBool {#toBool}

Converte um valor de argumento em um valor booleano, dependendo de seu tipo.

* Da string: tente converter o valor da string como booleano, de &quot;true&quot; se o valor da string for &quot;true&quot;, caso contrário, false
* Do numérico: verdadeiro se o valor numérico não for igual a 0, caso contrário, falso

+++Sintaxe

`toBool(<parameter>)`

+++

+++Parâmetros

* decimal
* booleano
* sequência de caracteres
* inteiro

+++

+++Assinaturas e tipos retornados

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Retornar um booleano.

+++

+++Exemplos

`toBool("true")`

`toBool(1)`

Retorna verdadeiro.

`toBool("this is not a boolean")`

Retorna falso.

+++

## toDateOnly {#toDateOnly}

Converte um argumento em um valor de tipo dateOnly. Para saber mais sobre tipos de dados, consulte esta [seção](../expression/data-types.md).

+++Sintaxe

`toDateOnly(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Representação em sequência de caracteres de uma data como &quot;AAAA-MM-DD&quot; (formato XDM). Também é compatível com o formato ISO-8601: apenas a parte **full-date** é considerada (Consulte [RFC 3339, seção 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | sequência de caracteres |
| data e hora | dateTime |
| data hora sem fuso horário | dateTimeOnly |
| valor inteiro de uma época em milissegundos | inteiro |

+++

+++Assinaturas e tipos retornados

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Retorna um valor de tipo dateOnly.

+++

+++Exemplos

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

todos retornam um objeto dateOnly representando 2023-08-18.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Retorna um dateOnly.

+++

## toDateTime {#toDateTime}

Converte parâmetros em um valor de data e hora, dependendo de seus tipos.

+++Sintaxe

`toDateTime(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora no formato ISO-8601 | sequência de caracteres |
| id do fuso horário | sequência de caracteres |
| data hora sem fuso horário | dateTimeOnly |
| valor inteiro de uma época em milissegundos | inteiro |

+++

+++Assinaturas e tipos retornados

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Retornar um **dateTime**.

+++

+++Exemplos

`toDateTime ("2023-08-18T23:17:59.123Z")`

Retorna 2023-08-18T23:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

Retorna 2023-08-18T23:17:59.123Z

`toDateTime(1560762190189)`

Retorna 17T09:03:10.189Z de 2023

+++

>[!NOTE]
>
>A ID do fuso horário deve ser uma constante de sequência. Não pode ser uma referência de campo nem uma expressão. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Converte um valor de argumento em um valor somente de data e hora.

+++Sintaxe

`toDateTimeOnly(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora no formato ISO-8601 ou &quot;AAAA-MM-DD&quot; (formato de data XDM) | sequência de caracteres |
| data e hora | dateTime |

+++

+++Assinaturas e tipos retornados

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Retorna um datetime sem considerar o fuso horário.

+++

+++Exemplos

`toDateTimeOnly ("2023-08-18")`

retorna um dateTime representando 2023-08-18T00:00:00.000

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Converte um valor de argumento em um valor decimal, dependendo de seu tipo.

+++Sintaxe

`toDecimal(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres | converte o valor da string em um decimal |
| dateTime | converte a data no número de milissegundos (milissegundos da época) |
| booleano | converte o valor booleano como 1 se verdadeiro, 0 se falso |
| inteiro | converte para um decimal (exemplo.: 1 torna-se 1.0) |

+++

+++Assinaturas e tipos retornados

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Retorna um decimal.

+++

+++Exemplos

`toDecimal("4.0")`

Retorna 4.0.

+++

## toDuration {#toDuration}

Converte um valor de argumento em uma duração. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

+++Sintaxe

`toDuration(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres | formatos baseados no formato de duração ISO-8601 PnDTnHnMn.nS com dias considerados exatamente 24 horas |
| inteiro | número de milissegundos |

Se expressão de string: os formatos aceitos são baseados no formato de duração ISO-8601 PnDTnHnMn.nS com dias considerados como sendo exatamente 24 horas.

A string começa com um sinal opcional, indicado pelo símbolo ASCII negativo ou positivo. Se negativo, todo o período é negado. A letra ASCII &quot;P&quot; é a próxima em maiúsculas ou minúsculas. Há então quatro seções, cada uma consistindo de um número e um sufixo. As seções têm sufixos em ASCII de &quot;D&quot;, &quot;H&quot;, &quot;M&quot; e &quot;S&quot; para dias, horas, minutos e segundos, aceitos em maiúsculas ou minúsculas. Os sufixos devem ocorrer em ordem. A letra ASCII &quot;T&quot; deve ocorrer antes da primeira ocorrência, se houver, de uma hora, minuto ou segunda seção. Pelo menos uma das quatro seções deve estar presente, e se &quot;T&quot; estiver presente, deve haver pelo menos uma seção após o &quot;T&quot;. A parte do número de cada seção deve consistir em um ou mais dígitos ASCII. O número pode ser prefixado pelo símbolo ASCII negativo ou positivo. O número de dias, horas e minutos que devem ser analisados. O número de segundos deve ser analisado juntamente com a fração opcional. O ponto decimal pode ser um ponto ou uma vírgula. A parte fracional pode ter de zero a nove dígitos.

+++

+++Assinaturas e tipo retornado

`toDuration(<string>)`

`toDuration(<integer>)`

Retorna uma duração.

+++

+++Exemplos

`toDuration("PT10H")`

Retorna a duração de 10 horas.

`toDuration("PT4S")`

Retorna a duração de 4s.

`toDuration(4000)`

Retorna a duração de 4s.

+++

## toInteger {#toInteger}

Converte um valor de argumento em um inteiro.

+++Sintaxe

`toInteger(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres | converte o valor da string em um inteiro |
| dateTime | converte a data no número de milissegundos (milissegundos da época) |
| decimal | converte em um inteiro removendo a parte decimal (exemplo: 1,5 torna-se 1) |
| booleano | converte o valor booleano como 1 se verdadeiro, 0 se falso |

+++

+++Assinaturas e tipo retornado

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Retorna um número inteiro.

+++

+++Exemplos

`toInteger("4")`

Retorna 4.

+++

## toString {#toString}

Converte um valor de argumento em um valor de string, dependendo de seu tipo. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

+++Sintaxe

`toString(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| dateTime | converte a data no formato de data UTC |
| dateTimeOnly | converte a data no formato de data UTC |
| duração | converta para o número correspondente de milissegundos como uma string |
| inteiro | converte para representação em string do valor (1 torna-se &quot;1&quot;) |
| decimal | converte para representação em string do valor (1,5 torna-se &quot;1,5&quot;) |
| booleano | converta o valor booleano como &#39;true&#39; se verdadeiro, &#39;false&#39; se falso |

+++

+++Assinaturas e tipo retornado

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retorna uma string.

+++

+++Exemplos

`toString(4)`

Retorna &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Retorna a representação da string do campo dateOnly fornecido (campo XDM Date), por exemplo &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Retorna &quot;PT1.52S&quot;.

+++

