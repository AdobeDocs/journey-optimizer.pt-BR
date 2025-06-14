---
title: Gerenciamento de conflitos e priorização
description: Saiba como aproveitar as ferramentas de conflito e priorização do Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 9d84a319497e833aa77416479dd019bab59aab55
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 28%

---

# Gerenciamento de conflitos e priorização {#conflict-prioritization}

## Ferramentas de gerenciamento de conflitos e priorizações {#tools}

No Journey Optimizer, gerenciar o volume e o momento de início das campanhas e jornadas é essencial para não sobrecarregar clientes com muitas interações. O Journey Optimizer oferece várias ferramentas para gerenciamento de conflitos e priorização.

Essas ferramentas estão disponíveis para campanhas e jornadas unitárias, de qualificação de público-alvo e de público-alvo de leitura.

Ao usar essas ferramentas, é possível garantir ações de marketing mais simples e direcionadas, fornecendo a mensagem certa no momento certo e evitando conflitos e sobrecarga.

### Ferramenta de detecção de conflitos

Com a **ferramenta de detecção de conflitos**, é possível identificar possíveis sobreposições em jornadas e campanhas. Isso é essencial, pois muitas comunicações simultâneas podem cansar os clientes. O Journey Optimizer permite monitorar elementos como linhas do tempo, sobreposição de público-alvo e configurações de canal. Ao identificar conflitos antecipadamente, você pode refinar suas campanhas para evitar bombardear clientes com várias mensagens ao mesmo tempo.

➡️ [Saiba como detectar possíveis conflitos em jornadas e campanhas](conflicts.md)

### Pontuações de prioridade

As **pontuações de prioridade** ajudam você a controlar quais campanhas ou jornadas têm prioridade quando um cliente se qualifica para várias comunicações. Isso é especialmente útil para canais de entrada, como web e dispositivos móveis, onde é possível exibir apenas uma campanha por vez. Ao atribuir uma pontuação de prioridade a cada jornada ou campanha, é possível garantir que a mensagem mais importante seja entregue primeiro.

➡️ [Saiba como atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)

### Conjuntos de regras

Os conjuntos de regras permitem **agrupar várias regras em conjuntos de regras** e aplicá-las às jornadas e campanhas de sua escolha. Isso oferece maior granularidade para limitar a frequência e a quantidade de jornadas que um cliente pode inserir em um determinado período de tempo ou controlar a frequência com que os usuários receberão uma mensagem, dependendo do tipo de comunicação.

* **limite e arbitragem de Jornada**

  Os conjuntos de regras permitem limitar a frequência e a quantidade de jornadas que um cliente pode inserir em um determinado período. Você também pode configurar regras para limitar o número de entradas de jornada para um perfil ou limitar o número de jornadas nas quais um cliente pode ser inscrito ao mesmo tempo.

  Além disso, você pode usar configurações de arbitragem para decidir qual jornada um cliente deve inserir se se qualificar para várias jornadas, usando pontuações de prioridade para determinar o melhor ajuste.

  ➡️ [Saiba como trabalhar com limite e arbitragem de jornada](journey-capping.md)

* **Limite de frequência por canal e tipo de comunicação**

  Você também pode usar conjuntos de regras para definir o limite de frequência por tipo de comunicação (por exemplo, Vendas, Promocional) para evitar sobrecarga de clientes com mensagens semelhantes. Você pode controlar a frequência de vários canais, excluindo automaticamente perfis solicitados em excesso para garantir uma melhor experiência do cliente.

  ➡️ [Saiba como definir o limite de frequência por canal e tipo de comunicação](../conflict-prioritization/channel-capping.md)

## Medidas de proteção e limitações

* **Campanhas e pontuações de prioridade** - Em campanhas, a pontuação de prioridade está disponível somente para os canais de entrada **web**, **no aplicativo** e **baseados em código**.

* **Latência de atualização do contador de perfil**

  Pode levar até 20 minutos depois que um cliente inserir uma jornada para que o valor do contador de perfil seja atualizado.

  Se um perfil inserir duas jornadas em uma janela curta, a segunda jornada pode não reconhecer corretamente que o limite de frequência já foi atingido, possivelmente permitindo que o perfil insira ambas as jornadas.

* **Prioridade de namespace para limite de entrada de jornada**

  O limite de entrada só será suportado se o namespace selecionado na jornada for o namespace de prioridade mais alta definido na sandbox. Se a prioridade do namespace não tiver sido configurada explicitamente, a prioridade mais alta padrão será email.

* **Ativações simultâneas em jornadas de qualificação de público-alvo**

  Quando várias jornadas de qualificação de público-alvo são ativadas pelo mesmo evento de qualificação de público-alvo, as contagens de limite de entrada não são precisas. Se as contagens estiverem abaixo do limite, o jornada continuará a arbitrar, mas não poderá obter as contagens mais atualizadas com ativações simultâneas.
