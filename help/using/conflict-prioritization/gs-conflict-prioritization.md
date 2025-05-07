---
title: Gerenciamento de conflitos e priorização
description: Saiba como aproveitar as ferramentas de conflito e priorização do Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilidade limitada"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: ht
source-wordcount: '637'
ht-degree: 100%

---

# Gerenciamento de conflitos e priorização {#conflict-prioritization}

>[!AVAILABILITY]
>
>Os recursos de conflito e priorização estão atualmente em disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desses recursos.

No Journey Optimizer, gerenciar o volume e o momento certo para uso de campanhas e jornadas é essencial para não sobrecarregar clientes com muitas interações. O Journey Optimizer oferece várias ferramentas para gerenciamento de conflitos e priorização.

## Ferramentas de gerenciamento de conflitos e priorizações {#tools}

Com a **ferramenta de detecção de conflitos**, é possível identificar possíveis sobreposições em jornadas e campanhas. Isso é essencial, pois muitas comunicações simultâneas podem cansar os clientes. O Journey Optimizer permite monitorar elementos como linhas do tempo, sobreposição de público-alvo e configurações de canal. Ao identificar conflitos antecipadamente, é possível refinar as campanhas para evitar bombardear clientes com várias mensagens ao mesmo tempo. [Saiba como detectar possíveis conflitos em jornadas e campanhas](conflicts.md)

Além disso, as **pontuações de prioridade** ajudam a controlar quais campanhas ou jornadas têm prioridade quando um cliente se qualifica para várias comunicações. Isso é especialmente útil para canais de entrada, como web e dispositivos móveis, onde é possível exibir apenas uma campanha por vez. Por atribuir uma pontuação de prioridade a cada jornada ou campanha, é possível garantir que a mensagem mais importante seja entregue primeiro. [Saiba como atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)

A **limitação e arbitragem de jornada** permite limitar a frequência e o número de jornadas em que um cliente pode ser inserido em um determinado intervalo de tempo. É possível definir regras para limitar o número de entradas de jornada de um perfil ou limitar o número de jornadas nas quais um cliente pode ser inscrito ao mesmo tempo. Além disso, é possível usar as configurações de arbitragem para decidir em qual jornada um cliente deve ser inserido caso se qualifique para várias jornadas, usando pontuações de prioridade para determinar a melhor opção. [Saiba como trabalhar com limitação e arbitragem de jornadas](journey-capping.md)

Por fim, também é possível usar conjuntos de regras para definir o **limite de frequência por tipo de comunicação** (por exemplo, vendas ou promocional) para não sobrecarregar clientes com mensagens semelhantes.  É possível controlar a frequência de vários canais excluindo automaticamente perfis solicitados em excesso para garantir uma melhor experiência do cliente. [Saiba como trabalhar com conjuntos de regras](../configuration/rule-sets.md)</li></ul>

Por aproveitar esses recursos, é possível garantir ações de marketing mais simples e direcionadas, fornecendo a mensagem certa no momento certo e evitando conflitos e sobrecarga.

## Medidas de proteção e limitações

**Limite de frequência e públicos-alvo em lote**

Para limitar a frequência no canal ou jornada, caso esteja usando um público-alvo em lote, o valor do contador de perfil referenciado no momento da entrada na jornada ou o tempo de execução da mensagem para uma comunicação de canal será baseado no instantâneo diário tirado.

Isso pode ser problemático, pois os clientes podem exceder o limite de frequência se tiverem entrado em outra jornada ou recebido outra comunicação entre o momento do instantâneo diário e o momento da jornada em que estão entrando (ou da mensagem que está sendo entregue).

**Limite de frequência e públicos-alvo de streaming**

Com públicos-alvo de transmissão, pode levar até 2 horas para que o sistema reconheça um valor de contador atualizado. Dessa forma, recomendamos um espaço entre as comunicações e jornadas de pelo menos duas horas, se possível, para atenuar esse risco.

**Hora de início das jornadas**

Para garantir que os recursos de gerenciamento de conflitos e priorização funcionem corretamente, recomendamos definir o momento de início da jornada em pelo menos 10 minutos no futuro, para permitir que o sistema atualize o contador adequadamente.

Se os clientes já tiverem atingido seus limites ao entrar em uma jornada, ainda não será permitida a entrada, mas se não tiverem atingido, o contador de entradas não será incrementado.

**Arbitragem da jornada**

Por enquanto, somente as jornadas de público-alvo de leitura são compatíveis com a arbitragem de jornada. As configurações de arbitragem não podem ser usadas para jornadas de qualificação unitárias ou de público-alvo.
