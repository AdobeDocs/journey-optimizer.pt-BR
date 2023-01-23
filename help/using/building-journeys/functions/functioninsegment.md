---
product: journey optimizer
title: inSegment
description: Saiba mais sobre a função noSegment
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, função, expressão, jornada
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 6%

---

# inSegment {#inSegment}

Verifica se um indivíduo pertence a um determinado segmento.

>[!NOTE]
>
>Você pode recuperar até 100 segmentos.

O nome do segmento deve ser uma constante de string. Não pode ser uma referência de campo nem uma expressão.

Os segmentos são definidos na variável [Adobe Experience Platform](https://platform.adobe.com/segment/overview). O editor de expressão fornece uma lista de segmentos preenchida automaticamente.

Os segmentos podem ter três status:

* existente: continua a estar no segmento.
* realizado: está inserindo o segmento.
* encerrado: está saindo do segmento.

Somente os indivíduos com a variável **Realizado** e **Existente** os status de participação do segmento serão considerados membros do segmento. Para obter mais informações sobre como avaliar um segmento, consulte [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` significa que você tem uma segmentMembership com o status inserido/existente.

`ELSE inSegment('segmentName') == false` significa que você tem uma segmentMembership do status de saída.

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

Retorna um booleano.

## Exemplo

`inSegment("men over 50")`

Explicação:

A função retornará **[!UICONTROL true]** se o indivíduo na instância do jornada fizer parte do segmento do Adobe Experience Platform chamado &quot;homens acima de 50&quot;, **[!UICONTROL false]** caso contrário.
