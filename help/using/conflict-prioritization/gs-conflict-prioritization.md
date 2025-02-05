---
title: Gerenciamento de conflitos e priorização
description: Saiba como aproveitar as ferramentas de conflito e priorização do Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilidade limitada"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 10%

---

# Gerenciamento de conflitos e priorização {#conflict-prioritization}

>[!AVAILABILITY]
>
>Os recursos de conflito e priorização estão atualmente disponíveis em Disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desses recursos.

No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. O Journey Optimizer oferece várias ferramentas para o gerenciamento de conflitos e a priorização.

## Ferramentas de gerenciamento de conflitos e priorizações {#tools}

Com a **ferramenta de detecção de conflitos**, você pode identificar possíveis sobreposições em jornadas e campanhas. Isso é crucial, pois muitas comunicações simultâneas podem causar fadiga do cliente. O Journey Optimizer permite monitorar elementos como linhas do tempo, sobreposição de público-alvo e configurações de canal. Ao identificar conflitos antecipadamente, você pode refinar suas campanhas para evitar bombardear clientes com várias mensagens ao mesmo tempo. [Saiba como detectar possíveis conflitos em jornadas e campanhas](conflicts.md)

Além disso, as **pontuações de prioridade** ajudam você a controlar quais campanhas ou jornadas têm prioridade quando um cliente se qualifica para várias comunicações. Isso é especialmente útil para canais de entrada, como web e dispositivos móveis, em que apenas uma campanha pode ser exibida a qualquer momento. Ao atribuir uma pontuação de prioridade a cada jornada ou campanha, é possível garantir que a mensagem mais importante seja entregue primeiro. [Saiba como atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)

**limite de Jornada e arbitragem** permite limitar a frequência e o número de jornadas que um cliente pode inserir em um determinado período. Você pode configurar regras para limitar o número de entradas de jornada para um perfil ou limitar o número de jornadas nas quais um cliente pode ser inscrito ao mesmo tempo. Além disso, você pode usar configurações de arbitragem para decidir qual jornada um cliente deve inserir se se qualificar para várias jornadas, usando pontuações de prioridade para determinar o melhor ajuste. [Saiba como trabalhar com limitação e arbitragem de jornadas](journey-capping.md)

Finalmente, você também pode usar conjuntos de regras para definir **limite de frequência por tipo de comunicação** (por exemplo, Vendas, Promocional) para evitar sobrecarga de clientes com mensagens semelhantes. Você pode controlar a frequência em vários canais, excluindo automaticamente perfis excessivamente solicitados para garantir uma melhor experiência do cliente. [Saiba como trabalhar com conjuntos de regras](../configuration/rule-sets.md)</li></ul>

Ao aproveitar esses recursos, você pode garantir esforços de marketing mais simples e direcionados, fornecendo a mensagem certa no momento certo e evitando conflitos e sobrecarga.

## Medidas de proteção e limitações

**Limite de frequência e públicos-alvo em lote**

Para limite de frequência, canal ou jornada, se o público-alvo usado for um público em lote, o valor do contador de perfil referenciado no momento da entrada na jornada ou o tempo de execução da mensagem para uma comunicação de canal será do instantâneo diário que é tirado.

Isso pode ser problemático, pois os clientes podem exceder o limite de frequência se tiverem entrado em outra jornada ou recebido outra comunicação entre a hora do instantâneo diário e a hora da jornada que está sendo inserida (ou a mensagem que está sendo entregue).

**Limite de frequência e públicos-alvo de streaming**

Para públicos de transmissão, pode levar até 2 horas para que o sistema reconheça um valor de contador atualizado e, como tal, recomendamos comunicações de espaçamento e jornadas com pelo menos duas horas de intervalo, se possível, para atenuar esse risco.

**hora de início do Jornada**

Para garantir que os recursos de gerenciamento de conflitos e priorização funcionem corretamente, recomendamos definir a hora de início da jornada pelo menos 10 minutos no futuro, para permitir que o sistema atualize o contador adequadamente.

Se os clientes já tiverem atingido seu limite ao inserir uma jornada, ainda não será permitida a entrada, mas se não tiverem atingido seu limite, o contador de entradas não será incrementado.

**Arbitragem de Jornada**

Por enquanto, somente as jornadas de público-alvo de leitura são compatíveis com a arbitragem de jornada. As configurações de arbitragem não podem ser usadas para jornadas de qualificação unitárias ou de público-alvo.
