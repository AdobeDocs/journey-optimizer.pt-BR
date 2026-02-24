---
title: Gerenciamento de conflitos e priorização
description: Saiba como aproveitar as ferramentas de conflito e priorização do Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 30%

---

# Gerenciamento de conflitos e priorização {#conflict-prioritization}

No Journey Optimizer, gerenciar o volume e o momento de início das campanhas e jornadas é essencial para não sobrecarregar clientes com muitas interações. As ferramentas de gerenciamento de conflitos e priorização ajudam a fornecer comunicações relevantes e oportunas, evitando a fadiga do cliente e garantindo que as mensagens certas cheguem ao seu público-alvo. Usando a detecção de conflitos, as pontuações de prioridade e os conjuntos de regras, você pode simplificar campanhas e jornadas para evitar sobreposições e equilibrar a frequência entre canais.

Essas ferramentas estão disponíveis para campanhas e para jornadas unitárias, de qualificação de público-alvo e de leitura de público. Quer você esteja definindo limites na frequência com que as mensagens são enviadas ou decidindo quais campanhas têm prioridade, esses recursos trabalham juntos para simplificar a tomada de decisões e otimizar sua estratégia de marketing.

## Por onde começar {#where-to-start}

| Sua meta | Ferramenta | Ação |
|-----------|------|--------|
| Veja se as jornadas ou campanhas se sobrepõem (linha do tempo, público-alvo, canal) | **Detecção de conflitos** | [Identificar possíveis conflitos](conflicts.md) |
| Decidir qual mensagem ganha quando um perfil se qualifica para vários | **Pontuações de prioridade** | [Atribuir pontuações de prioridade](priority-scores.md) |
| Limitar a frequência ou o número de mensagens que um perfil recebe | **Conjuntos de regras** (limite de frequência, limite de jornada, horas de silêncio) | [Definir regras de limite de mensagens e jornadas](../../rp_landing_pages/capping-rules-landing-page.md) |

**Fluxo típico:** use a detecção de conflitos para detectar sobreposições, aplicar pontuações de prioridade e conjuntos de regras para controlar quais mensagens são enviadas e com que frequência.

## Gerenciamento de conflitos e ferramentas de priorização {#tools}

### Ferramenta de detecção de conflitos

Com a **ferramenta de detecção de conflitos**, é possível identificar possíveis sobreposições em jornadas e campanhas. Isso é essencial, pois muitas comunicações simultâneas podem cansar os clientes. O Journey Optimizer permite monitorar elementos como linhas do tempo, sobreposição de público-alvo e configurações de canal. Ao identificar conflitos antecipadamente, é possível refinar as campanhas para evitar bombardear clientes com várias mensagens ao mesmo tempo. 

[Saiba como detectar possíveis conflitos em jornadas e campanhas](conflicts.md)

### Pontuações de prioridade

As **Pontuações de prioridade** ajudam a controlar quais campanhas ou jornadas têm prioridade quando um cliente se qualifica para várias comunicações. Isso é especialmente útil para canais de entrada, como web e dispositivos móveis, onde é possível exibir apenas uma campanha por vez. Ao atribuir uma pontuação de prioridade a cada jornada ou campanha, você pode garantir que a mensagem mais importante seja entregue primeiro.

[Saiba como atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)

### Conjuntos de regras

Os conjuntos de regras permitem **agrupar várias regras** e aplicá-las às jornadas e campanhas de sua escolha. Isso oferece maior granularidade para limitar a frequência e a quantidade de jornadas que um cliente pode inserir em um determinado período de tempo, ou para controlar a frequência com que os usuários recebem mensagens, dependendo do tipo de comunicação.

* **Limite de Jornada e arbitragem** - Limite a frequência e o número de jornadas que um cliente pode inserir em um determinado período. Você pode limitar o número de entradas de jornada para um perfil ou limitar o número de jornadas nas quais um cliente pode ser inscrito ao mesmo tempo. Use configurações de arbitragem para decidir qual jornada um cliente deve inserir se se qualificar para várias jornadas, usando pontuações de prioridade para determinar o melhor ajuste. [Saiba como trabalhar com limitação e arbitragem de jornadas](journey-capping.md)

* **Limite de frequência por canal e tipo de comunicação** - Defina o limite de frequência por tipo de comunicação (por exemplo, Vendas, Promocional) para evitar sobrecarga de clientes com mensagens semelhantes. Frequência de controle em vários canais, excluindo automaticamente perfis excessivamente solicitados. [Saiba como definir o limite de frequência por canal e tipo de comunicação](channel-capping.md)

* **Horas de silêncio** - Defina exclusões com base no tempo para que nenhuma mensagem seja enviada durante períodos específicos (Email, SMS, Push, WhatsApp). [Saiba como definir horários de silêncio](quiet-hours.md)

[Saiba como trabalhar com conjuntos de regras](rule-sets.md)

## Medidas de proteção e limitações {#guardrails}

* **Campanhas e pontuações de prioridade**: em campanhas, a pontuação de prioridade está disponível somente para os canais de entrada **web**, **no aplicativo** e **baseados em código**.

* **Latência de atualização do contador de perfil** - Pode levar até 10 minutos depois que um cliente inserir uma jornada para que o valor do contador de perfil seja atualizado. Se um perfil inserir duas jornadas em uma janela curta, a segunda jornada pode não reconhecer corretamente que o limite de frequência já foi atingido, possivelmente permitindo que o perfil insira ambas as jornadas.

* **Prioridade de namespace para o limite de entrada de jornada** - O limite de entrada só terá suporte se o namespace selecionado na jornada for o namespace de prioridade mais alta definido na sandbox. Se a prioridade do namespace não tiver sido configurada explicitamente, a prioridade mais alta padrão será email.

* **Ativações simultâneas em jornadas de qualificação de público-alvo** - Quando várias jornadas de qualificação de público-alvo são ativadas pelo mesmo evento de qualificação de público-alvo, as contagens de limite de entrada não serão precisas. Se as contagens estiverem abaixo do limite, a jornada continuará arbitrando, mas não será capaz de obter as contagens mais atualizadas com ativações simultâneas.

## Recursos adicionais

* **[Identificar possíveis conflitos](conflicts.md)** - Saiba como detectar e resolver conflitos entre campanhas e jornadas sobrepostas.
* **[Atribuir pontuações de prioridade](priority-scores.md)** - Entenda como atribuir e usar pontuações de prioridade para controlar a precedência de entrega de mensagens.
* **[Trabalhar com conjuntos de regras](rule-sets.md)** - Saiba como criar e aplicar conjuntos de regras para o gerenciamento de conflitos e a governança de mensagens.
* **[limite e arbitragem de Jornada](journey-capping.md)** - Configure regras de limite e arbitragem de nível de jornada.
* **[Limite de frequência por canal](channel-capping.md)** - Defina limites de frequência de nível de canal para evitar mensagens excessivas.
* **[Definir horas de espera](quiet-hours.md)** - Definir exclusões com base no tempo para entrega de mensagens.
* **[Tutoriais sobre gerenciamento de conflitos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - Tutoriais em vídeo passo a passo.
