---
product: journey optimizer
title: Função inAudience
description: Saiba mais sobre a função Adobe Experience Platform no Audience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, função, expressão, jornada, público-alvo, segmentação
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 1%

---

# Função inAudience {#inAudience}

A função `inAudience` é uma função Adobe Experience Platform que permite verificar se um indivíduo em sua jornada pertence a um público-alvo específico. Essa função avançada permite criar caminhos de jornada personalizados com base na associação ao público, permitindo segmentação e direcionamento sofisticados nas experiências do cliente.

Use a função `inAudience` quando precisar:

* Caminhos de jornada de ramificação com base na associação do público-alvo. [Saiba mais](../conditions.md#using-a-segment)
* Aplicar lógica condicional que depende de um perfil pertencer a um segmento específico
* Direcione grupos específicos de clientes com experiências personalizadas
* Avaliar a participação do público-alvo em tempo real nas condições de jornada
* Combinar várias verificações de público-alvo para criar regras complexas de direcionamento

A função avalia a associação de público-alvo em tempo real e retorna um valor booleano, tornando-a ideal para nós de decisão e expressões condicionais. Os públicos são definidos e gerenciados no [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (saiba mais sobre o [trabalho com públicos](../../audience/about-audiences.md) no Journey Optimizer), e o editor de expressão fornece sugestões de preenchimento automático para ajudar você a referenciá-los com precisão.

**Status do público-alvo:**

Os públicos-alvo podem ter dois status de participação:

* **Realizado**: o indivíduo se qualifica para a definição de público-alvo e é um membro ativo
* **Encerrado**: o indivíduo saiu do público-alvo e não se qualifica mais

Apenas indivíduos com o status **Realizado** serão considerados membros ativos do público-alvo. Quando a função retorna `true`, ela confirma que o indivíduo tem o status realizado; quando retorna `false`, ela indica o status encerrado. Para obter mais informações sobre a avaliação de público, consulte a [documentação do Serviço de Segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=pt-BR#interpret-segment-results){target="_blank"}.

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

**Tempo de propagação:** {#propagation-timing}

Ao usar `inAudience()` em um nó de condição, o tempo de avaliação de associação de segmento varia dependendo de onde a condição aparece na jornada:

* **Em uma jornada de Leitura de Público-alvo, antes de uma atividade de Espera:** o Journey Optimizer lê a partir da projeção em lote do perfil. Os dados nesta projeção são atualizados em **2 horas** após a assimilação. Os públicos-alvo que dependem de condições baseadas no dia ou baseadas no tempo podem enfrentar atraso adicional. Adicione uma breve [atividade de espera](../wait-activity.md) no início da jornada ou permita o tempo de buffer para garantir que a associação de segmento mais recente seja refletida.
* **Em uma jornada de evento unitária ou após uma atividade Wait:** a associação de segmento é lida a partir da projeção de streaming (unitária). Normalmente, os dados estão disponíveis em **15 minutos**. Para obter mais detalhes, consulte a [documentação de assimilação de streaming do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/streaming/overview){target="_blank"}.

## Tópicos relacionados

Saiba mais sobre como usar públicos-alvo na Adobe Journey Optimizer:

* **[Sobre públicos-alvo](../../audience/about-audiences.md)** - Entenda como os públicos-alvo funcionam no Adobe Experience Platform e no Journey Optimizer, inclusive como criá-los e gerenciá-los
* **[Atividade Ler público-alvo](../read-audience.md)** - Use públicos-alvo para acionar a entrada de jornada e fazer com que todos os membros do público-alvo insiram uma jornada
* **[Eventos de qualificação de público-alvo](../audience-qualification-events.md)** - Ouça as entradas e saídas do perfil dos públicos-alvo para acionar ações de jornada em tempo real
* **[Uso de públicos-alvo em condições](../conditions.md#using-a-segment)** - Crie caminhos de jornada condicionais com base na associação de público-alvo usando a atividade Otimize
* **[Propriedades da Jornada - Políticas de mesclagem](../journey-properties.md)** - Entenda como as políticas de mesclagem funcionam ao usar vários públicos com a função inAudience

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta a função `inAudience`, que verifica em tempo real se um perfil de jornada pertence a um público-alvo nomeado do Adobe Experience Platform e retorna um valor booleano usado em condições de jornada.

**Intenções:**
* Ramifique um caminho de jornada com base no fato de um perfil ser membro de um público-alvo específico usando `inAudience`
* Combinar várias verificações `inAudience` com a lógica AND/OR para criar condições complexas de direcionamento
* Verificar se um perfil não inseriu um público-alvo específico usando uma verificação de negação (`inAudience("...") == false`)
* Entenda as diferenças de tempo de propagação entre as jornadas Ler público-alvo e as jornadas de eventos unitários
* Identificar e corrigir referências de público corrompidas causadas por renomeações de público no Adobe Experience Platform

**Glossário:**
* **Realizado**: status de participação de público indicando o indivíduo atualmente qualificado para a definição de público-alvo e que é um membro ativo *(específico do produto)*
* **Encerrado**: status de participação de público indicando que o indivíduo deixou o público e não se qualifica mais *(específico do produto)*
* **Política de mesclagem**: uma regra no Adobe Experience Platform que determina como os dados do perfil de vários conjuntos de dados são combinados ao avaliar a associação de público-alvo *(específico do produto)*
* **Projeção de lote**: o armazenamento de dados do perfil foi atualizado de acordo com uma agenda (dentro de 2 horas após a assimilação) usada pela opção Ler jornadas de público-alvo *(específico do produto)*
* **Projeção de streaming**: o armazenamento de dados do perfil em tempo real (normalmente disponível em 15 minutos) usado em jornadas de evento unitárias e após atividades Wait *(específico do produto)*

**Medidas de Proteção:**
* Uma única jornada pode recuperar até 100 públicos-alvo
* O parâmetro de nome de público deve ser uma constante de cadeia de caracteres; não há suporte para referências de campo e expressões dinâmicas
* Renomear um público no Adobe Experience Platform não atualiza automaticamente as referências `inAudience` nas expressões do jornada. São necessárias atualizações manuais
* Políticas de mesclagem inconsistentes em vários públicos usados na mesma jornada podem causar erros ou alertas

**Terminologia:**
* Nome canônico: inAudience — Acrônimo: none — variantes: inSegment (nome herdado)
* Sinônimos: &quot;inAudience&quot; = &quot;função de verificação de associação de público&quot;
* Não confundir: &quot;Realizado&quot; (membro ativo) ≠ &quot;Saindo&quot; (não é mais um membro)
* Não confunda: &quot;inAudience&quot; (função atual) ≠ &quot;inSegment&quot; (função herdada obsoleta)

**Perguntas frequentes:**
* **P: O que `inAudience` retorna quando um perfil sai do público-alvo?** — Retorna `false`; somente perfis com status &quot;Realizado&quot; são considerados membros ativos e retornam `true`.
* **P: quantos públicos-alvo posso verificar em uma única jornada?** — É possível recuperar até 100 públicos-alvo em uma única jornada.
* **P: O que acontece se eu renomear um público no Adobe Experience Platform depois de usá-lo em uma jornada?** — A expressão de jornada não é atualizada automaticamente; você deve editar manualmente a chamada `inAudience` para usar o novo nome de público-alvo, caso contrário, a condição será interrompida.
* **P: Com que rapidez a associação de público-alvo fica disponível após uma atualização de perfil em uma jornada de Leitura de Público-alvo?** — Em uma jornada Read Audience antes de uma atividade Wait, os dados são lidos na projeção de lote atualizada dentro de 2 horas após a assimilação.
* **P: Posso passar um atributo de perfil como o parâmetro de nome de público-alvo?** — Não, o nome do público-alvo deve ser uma constante de sequência; referências de campo e expressões não são compatíveis.

+++
