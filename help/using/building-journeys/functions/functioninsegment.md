---
product: journey optimizer
title: inSegment
description: Saiba mais sobre a função no segmento
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, função, expressão, jornada
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: b1b736eb723f3eb586dd33a4b8551e46b01b7789
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 6%

---

# inSegment {#inSegment}

Verifica se um indivíduo pertence a um determinado público-alvo.

>[!NOTE]
>
>Você pode recuperar até 100 públicos-alvo.

O nome do público-alvo deve ser uma constante de sequência. Não pode ser uma referência de campo nem uma expressão.

Os públicos-alvo são definidos na [Adobe Experience Platform](https://platform.adobe.com/audience/overview). O editor de expressão fornece uma lista de públicos preenchida automaticamente.

Os públicos-alvo podem ter dois status:

* realizado: a entidade se qualifica para a definição do segmento.
* encerrado: a entidade está saindo da definição do segmento.

Somente os indivíduos com o status de participação de público **Realizado** serão considerados membros do público. Para obter mais informações sobre como avaliar um público, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inSegment('segmentName') == true` significa que você tem um segmentMembership com o status inserido/existente.

`inSegment('segmentName') == false` significa que você tem um segmentMembership com status encerrado.

## Categoria

Adobe Experience Platform

## Sintaxe da função

`inSegment(<parameter>)`

## Parâmetros

| Parâmetro | Descrição | Tipo |
|--- |--- |--- |
| Segmento | O nome do público | `<string>` |

## Assinatura e tipo retornado

`inSegment(<string>)`

Retorna um valor booleano.

## Exemplo

`inSegment("men over 50")`

Explicação:

A função retornará **[!UICONTROL true]** se o indivíduo na instância do jornada fizer parte do público-alvo da Adobe Experience Platform chamado &quot;homens acima de 50&quot;, caso contrário **[!UICONTROL false]**.

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-functions-functioninsegment.md}}
