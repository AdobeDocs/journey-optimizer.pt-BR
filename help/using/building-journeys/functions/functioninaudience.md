---
product: journey optimizer
title: inAudience
description: Saiba mais sobre a função no Audience
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, função, expressão, jornada
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inAudience {#inAudience}

Verifica se um indivíduo pertence a um determinado público-alvo.

>[!NOTE]
>
>Você pode recuperar até 100 públicos-alvo.

O nome do público-alvo deve ser uma constante de sequência. Não pode ser uma referência de campo nem uma expressão.

Os públicos-alvo são definidos na [Adobe Experience Platform](https://platform.adobe.com/audience/overview). O editor de expressão fornece uma lista de públicos preenchida automaticamente.

Os públicos-alvo podem ter três status:

* existente: a entidade continua no público-alvo.
* percebido: a entidade está entrando no público-alvo.
* encerrado: a entidade está saindo do público-alvo.

Somente os indivíduos com o status de participação de público **Realizado** e **Existente** serão considerados membros do público. Para obter mais informações sobre como avaliar um público, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inAudience('audienceName') == true` significa que você tem um segmentMembership com o status inserido/existente.

`inAudience('audienceName') == false` significa que você tem um segmentMembership com status encerrado.

## Categoria

Adobe Experience Platform

## Sintaxe da função

`inAudience(<parameter>)`

## Parâmetros

| Parâmetro | Descrição | Tipo |
|--- |--- |--- |
| Público-alvo | O nome do público | `<string>` |

## Assinatura e tipo retornado

`inAudience(<string>)`

Retorna um valor booleano.

## Exemplo

`inAudience("men over 50")`

Explicação:

A função retornará **[!UICONTROL true]** se o indivíduo na instância do jornada fizer parte do público-alvo da Adobe Experience Platform chamado &quot;homens acima de 50&quot;, caso contrário **[!UICONTROL false]**.
