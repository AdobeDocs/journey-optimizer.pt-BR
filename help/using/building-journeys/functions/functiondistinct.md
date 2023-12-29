---
product: journey optimizer
title: distinct
description: Saiba mais sobre a distinção de função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct, função, expressão, jornada
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 5%

---

# distinct {#distinct}

Retorna os valores ou objetos distintos de uma determinada lista. Entradas nulas são ignoradas.

>[!NOTE]
>
>Se a lista de destino for um listObject, essa função só poderá ser usada em expressões de ação personalizadas.

## Categoria

Lista

## Sintaxe da função

`distinct(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | string | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

## Assinaturas e tipos retornados

`distinct(<listInteger>)`

Retorna uma lista de inteiros.

`distinct(<listDecimal>)`

Retorna uma lista de decimais.

`distinct(<listString>)`

Retorna uma lista de strings.

`distinct(<listDateTimeOnly>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`distinct(<listDateTime>)`

Retorna uma lista de datetimes.

`distinct(<listDateOnly>)`

Retorna uma lista de datas.

`distinct(<listBoolean>)`

Retorna uma lista de booleanos.

`distinct(<listDuration>)`

Retorna uma lista de durações.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Retorna uma lista de objetos.


## Exemplos

`distinct([10,2,10,null])`

Devoluções `[10, 2]`.
