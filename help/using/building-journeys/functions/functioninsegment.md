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
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta a função herdada `inSegment`, que verifica se um perfil de jornada pertence a um público-alvo nomeado do Adobe Experience Platform e retorna um valor booleano.

**Intenções:**
* Verificar se um perfil é um membro ativo de um público nomeado usando `inSegment`
* Usar `inSegment('name') == true` para confirmar a associação de público realizada (ativa) em uma condição de jornada
* Use `inSegment('name') == false` para confirmar a associação de público-alvo (inativo) encerrada

**Glossário:**
* **Realizado**: o status de participação de público-alvo significa que a entidade está qualificada atualmente para a definição de segmento *(específico do produto)*
* **Saída**: Status de participação de público-alvo significando que a entidade está saindo ou saiu da definição de segmento *(específico do produto)*

**Medidas de Proteção:**
* É possível recuperar até 100 públicos-alvo em uma única jornada
* O nome do público-alvo deve ser uma constante de cadeia de caracteres; referências de campo e expressões não são compatíveis como parâmetros

**Terminologia:**
* Nome canônico: inSegment — Acrônimo: none — variantes: inAudience (função preferida atual)
* Sinônimos: &quot;inSegment&quot; = &quot;verificação de associação de público-alvo&quot; (herdado)
* Não confunda: &quot;inSegment&quot; (função herdada/obsoleta) ≠ &quot;inAudience&quot; (função recomendada atual)
* Não confundir: &quot;realizado&quot; (membro ativo) ≠ &quot;encerrado&quot; (já não é um membro)

**Perguntas frequentes:**
* **P: Qual é a diferença entre `inSegment` e `inAudience`?** — `inSegment` é o nome da função herdada; `inAudience` é a função recomendada no momento. Ambos verificam a associação de público-alvo, mas `inAudience` tem uma documentação mais completa, incluindo medidas de proteção e detalhes de tempo de propagação.
* **P: O que `inSegment('name') == true` significa?** — Significa que o perfil tem um status &quot;realizado&quot; segmentMembership, ou seja, o indivíduo é um membro ativo do público-alvo.
* **P: Posso passar uma expressão dinâmica como o nome do público-alvo?** — Não, o nome do público-alvo deve ser uma constante de sequência; referências de campo e expressões não são compatíveis.
* **P: Quantos públicos-alvo posso avaliar em uma jornada?** — É possível recuperar até 100 públicos-alvo em uma única jornada.

+++
