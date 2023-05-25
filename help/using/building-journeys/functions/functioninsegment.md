---
product: journey optimizer
title: inSegment
description: Saiba mais sobre a função no segmento
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, função, expressão, jornada
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 6%

---

# inSegment {#inSegment}

Verifica se um indivíduo pertence a um determinado segmento.

>[!NOTE]
>
>Você pode recuperar até 100 segmentos.

O nome do segmento deve ser uma constante de sequência. Não pode ser uma referência de campo nem uma expressão.

Os segmentos são definidos na variável [Adobe Experience Platform](https://platform.adobe.com/segment/overview). O editor de expressão fornece uma lista de segmentos preenchida automaticamente.

Os segmentos podem ter três status:

* existente: a entidade continua a estar no segmento.
* realizado: a entidade está informando o segmento.
* encerrado: a entidade está saindo do segmento.

Somente os indivíduos com o **Realizado** e **Existente** os status de participação do segmento serão considerados membros do segmento. Para obter mais informações sobre como avaliar um segmento, consulte [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`IF inSegment('segmentName') == true` significa que você tem um segmentMembership com o status inserido/existente.

`ELSE inSegment('segmentName') == false` significa que você tem um segmentMembership com o status encerrado.

## Categoria

Adobe Experience Platform

## Sintaxe da função

`inSegment(<parameter>)`

## Parâmetros

| Parâmetro | Descrição | Tipo |
|--- |--- |--- |
| Segmento | O nome do segmento | `<string>` |

## Assinatura e tipo retornado

`inSegment(<string>)`

Retorna um valor booleano.

## Exemplo

`inSegment("men over 50")`

Explicação:

A função retornará **[!UICONTROL true]** se o indivíduo na instância do jornada fizer parte do segmento do Adobe Experience Platform chamado &quot;homens acima de 50&quot;, **[!UICONTROL false]** caso contrário.
