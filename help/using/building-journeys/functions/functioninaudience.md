---
product: journey optimizer
title: função inAudience
description: Saiba mais sobre a função Adobe Experience Platform no Audience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, função, expressão, jornada, público-alvo, segmentação
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# função inAudience {#inAudience}

A função `inAudience` é uma função Adobe Experience Platform que permite verificar se um indivíduo em sua jornada pertence a um público-alvo específico. Essa função avançada permite criar caminhos de jornada personalizados com base na associação ao público, permitindo segmentação e direcionamento sofisticados nas experiências do cliente.

Use a função `inAudience` quando precisar:

* Caminhos de jornada de ramificação com base na associação do público-alvo. [Saiba mais](../condition-activity.md#using-a-segment)
* Aplicar lógica condicional que depende de um perfil pertencer a um segmento específico
* Direcione grupos específicos de clientes com experiências personalizadas
* Avaliar a participação do público-alvo em tempo real nas condições de jornada
* Combinar várias verificações de público-alvo para criar regras complexas de direcionamento

A função avalia a associação de público-alvo em tempo real e retorna um valor booleano, tornando-a ideal para nós de decisão e expressões condicionais. Os públicos são definidos e gerenciados no [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (saiba mais sobre o [trabalho com públicos](../../audience/about-audiences.md) no Journey Optimizer), e o editor de expressão fornece sugestões de preenchimento automático para ajudar você a referenciá-los com precisão.

**Status do público-alvo:**

Os públicos-alvo podem ter dois status de participação:

* **Realizado**: o indivíduo se qualifica para a definição de público-alvo e é um membro ativo
* **Encerrado**: o indivíduo saiu do público-alvo e não se qualifica mais

Apenas indivíduos com o status **Realizado** serão considerados membros ativos do público-alvo. Quando a função retorna `true`, ela confirma que o indivíduo tem o status realizado; quando retorna `false`, ela indica o status encerrado. Para obter mais informações sobre a avaliação de público, consulte a [documentação do Serviço de Segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

+++Sintaxe

`inAudience(<parameter>)`

+++

+++Parâmetros

| Parâmetro | Descrição | Tipo |
|--- |--- |--- |
| Público-alvo | O nome do público | `<string>` |

**Restrições importantes:**

* O nome do público-alvo deve ser uma constante de sequência
* Ele não pode ser uma referência de campo ou uma expressão
* Você pode recuperar até 100 públicos-alvo em uma única jornada

+++

+++Assinatura e tipo retornado

`inAudience(<string>)`

Retorna um valor booleano:
* `true`: O indivíduo é um membro da audiência (status realizado)

* `false`: O indivíduo não é membro da audiência (status de saída)

+++

+++Exemplos

`inAudience("men over 50")`

Retorna **true** se o indivíduo na instância do jornada fizer parte do público-alvo da Adobe Experience Platform chamado &quot;homens acima de 50&quot;, caso contrário **false**.

**Casos de uso prático:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Medidas de proteção e limitações {#guardrails}

Ao usar a função `inAudience` em suas jornadas, esteja ciente das seguintes medidas de proteção e limitações:

**Limite de recuperação de público-alvo:**
* Você pode recuperar até 100 públicos-alvo em uma única jornada
* O editor de expressão fornece uma lista de públicos-alvo disponíveis preenchida automaticamente para ajudar você a referenciá-los corretamente

**Restrições de parâmetro:**
* O nome do público-alvo deve ser uma constante de sequência
* Não há suporte para referências e expressões de campo como parâmetros

**Alterações no nome do público-alvo:**
* Alterar o nome de um público-alvo existente no Adobe Experience Platform não atualiza automaticamente nenhuma referência a esse público-alvo nas expressões de jornada
* Se o nó de condição usar `inAudience('oldAudienceName')`, você deverá editar manualmente a expressão para usar o novo nome
* Se o nome do público-alvo não for atualizado, a condição de jornada será interrompida e poderá resultar em um comportamento de jornada incorreto

**Considerações sobre a política de mesclagem:**
* Ao usar vários públicos com a função `inAudience`, inconsistências com políticas de mesclagem podem causar erros ou alertas
* Consulte [Propriedades da Jornada](../journey-properties.md) para obter mais informações sobre o comportamento da política de mesclagem

## Tópicos relacionados

Saiba mais sobre como usar públicos-alvo na Adobe Journey Optimizer:

* **[Sobre públicos-alvo](../../audience/about-audiences.md)** - Entenda como os públicos-alvo funcionam no Adobe Experience Platform e no Journey Optimizer, inclusive como criá-los e gerenciá-los
* **[Atividade Ler público-alvo](../read-audience.md)** - Use públicos-alvo para acionar a entrada de jornada e fazer com que todos os membros do público-alvo insiram uma jornada
* **[Eventos de qualificação de público-alvo](../audience-qualification-events.md)** - Ouça as entradas e saídas do perfil dos públicos-alvo para acionar ações de jornada em tempo real
* **[Uso de públicos-alvo em condições](../condition-activity.md#using-a-segment)** - Crie caminhos de jornada condicionais com base na associação de público-alvo usando a atividade de Condição
* **[Propriedades da Jornada - Políticas de mesclagem](../journey-properties.md)** - Entenda como as políticas de mesclagem funcionam ao usar vários públicos com a função inAudience

