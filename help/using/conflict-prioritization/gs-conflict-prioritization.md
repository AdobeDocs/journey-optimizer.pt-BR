---
title: Gerenciamento de conflitos e priorização
description: Saiba como aproveitar as ferramentas de conflito e priorização do Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
TQID: https://experienceleague.adobe.com/vx-CmsYwj7QyN2sVMrpJ9VUNDgnXq8qt1nT9lHOFV3s
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fd59660e-de8a-4bfb-85dc-7fa546030c49
subfeature_v2:
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: f3fe4813-f254-4f8f-99cc-24bd67f119e1
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 49542ca70e8899061bc79772cf96069ab2587ab2
workflow-type: ht
source-wordcount: 896
ht-degree: 100%

---

# Gerenciamento de conflitos e priorização {#conflict-prioritization}

>[!BEGINSHADEBOX]

**Nesta página:** descubra como a detecção de conflitos, as pontuações de prioridade e os conjuntos de regras funcionam juntos para que você possa evitar comunicações sobrepostas e controlar a frequência com que os clientes recebem mensagens.

>[!ENDSHADEBOX]

No Journey Optimizer, gerenciar o volume e o momento das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. Ferramentas de gestão de conflitos e priorização ajudam você a fornecer comunicações ponderadas e oportunas, evitando a fadiga do cliente e garantindo que as mensagens certas cheguem ao seu público-alvo. Ao usar detecção de conflitos, pontuações de prioridade e conjuntos de regras, você pode otimizar campanhas e jornadas para evitar sobreposições e equilibrar a frequência entre os canais.

Essas ferramentas estão disponíveis para campanhas e jornadas unitárias, de qualificação de público-alvo e de público-alvo de leitura. Quer você esteja definindo limites para a frequência de envio das mensagens ou decidindo quais campanhas têm prioridade, esses recursos trabalham juntos para simplificar a tomada de decisão e otimizar a sua estratégia de marketing.

## Por onde começar {#where-to-start}

| Sua meta | Ferramenta | Ação |
|-----------|------|--------|
| Veja se as jornadas ou campanhas se sobrepõem (linha do tempo, público-alvo, canal) | **Detecção de conflito** | [Identificar possíveis conflitos](conflicts.md) |
| Decidir qual mensagem ganha quando um perfil se qualifica para vários | **Pontuações de prioridade** | [Atribuir pontuações de prioridade](priority-scores.md) |
| Limitar a frequência ou o número de mensagens que um perfil recebe | **Conjuntos de regras** (limite de frequência, limite de jornada, horário de silêncio) | [Definir regras de limitação de mensagens e jornadas](../../rp_landing_pages/capping-rules-landing-page.md) |

**Fluxo típico:** use a detecção de conflitos para identificar sobreposições, aplicar pontuações de prioridade e conjuntos de regras para controlar quais mensagens são enviadas e com que frequência.

## Ferramentas de gestão de conflitos e priorização {#tools}

### Ferramenta de detecção de conflitos

Com a **ferramenta de detecção de conflitos**, é possível identificar possíveis sobreposições em jornadas e campanhas. Isso é essencial, pois muitas comunicações simultâneas podem cansar os clientes. O Journey Optimizer permite monitorar elementos como linhas do tempo, sobreposição de público-alvo e configurações de canal. Ao identificar conflitos antecipadamente, é possível refinar as campanhas para evitar bombardear clientes com várias mensagens ao mesmo tempo.

[Aprenda a detectar possíveis conflitos em jornadas e campanhas](conflicts.md)

### Pontuações de prioridade

As **Pontuações de prioridade** ajudam a controlar quais campanhas ou jornadas têm prioridade quando um cliente se qualifica para várias comunicações. Isso é especialmente útil para canais de entrada, como web e dispositivos móveis, onde é possível exibir apenas uma campanha por vez. Ao atribuir uma pontuação de prioridade a cada jornada ou campanha, você pode garantir que a mensagem mais importante seja entregue primeiro.

[Aprenda a atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)

### Conjuntos de regras

Os conjuntos de regras permitem que você **agrupe várias regras** e as aplique às jornadas e campanhas de sua escolha. Assim, você conta com mais granularidade para limitar a frequência e a quantidade de jornadas que um cliente pode inserir em um determinado intervalo de tempo, ou controlar a frequência com que os usuários recebem uma mensagem, dependendo do tipo de comunicação.

* **Limitação e arbitragem de jornadas**: limitar a frequência e a quantidade de jornadas em que um cliente pode entrar em um determinado intervalo de tempo. Você pode limitar o número de entradas de jornadas para um perfil ou restringir o número de jornadas nas quais um cliente pode estar inscrito simultaneamente. Use as configurações de arbitragem para decidir qual jornada um cliente deve seguir caso se qualifique para várias jornadas, usando pontuações de prioridade para determinar a melhor opção. [Saiba como trabalhar com limitação de jornada e arbitragem](journey-capping.md)

* **Limitação de frequência por canal e tipo de comunicação**: defina a limitação de frequência por tipo de comunicação (por exemplo, Vendas, Promocional) para evitar sobrecarregar os clientes com mensagens semelhantes. Controle a frequência em vários canais, excluindo automaticamente perfis com solicitações excessivas. [Saiba como configurar o limite de frequência por canal e tipo de comunicação](channel-capping.md)

* **Horário de silêncio**: defina exclusões com base no tempo para que nenhuma mensagem seja enviada durante períodos específicos (Email, SMS, Push, WhatsApp). [Saiba como definir horários de silêncio](quiet-hours.md)

[Saiba como trabalhar com conjuntos de regras](rule-sets.md)

## Medidas de proteção e limitações {#guardrails}

* **Campanhas e pontuações de prioridade**: em campanhas, a pontuação de prioridade está disponível somente para os canais de entrada **web**, **no aplicativo** e **baseados em código**.

* **Latência de atualização do contador de perfil**: pode levar até 10 minutos após um cliente entrar em uma jornada para que o valor do contador de perfil seja atualizado. Se um perfil entrar em duas jornadas em uma curta janela de tempo, a segunda jornada pode não reconhecer corretamente que o limite de frequência já foi atingido, possivelmente permitindo que o perfil entre em ambas as jornadas.

* **Prioridade de namespace para limitação de entrada de jornada**: a limitação de entrada só é aceita se o namespace selecionado na jornada for o namespace de maior prioridade definido na sandbox. Se a prioridade do namespace não tiver sido configurada explicitamente, a prioridade mais alta padrão será email.

* **Ativações simultâneas em jornadas de qualificação de público-alvo**: quando várias jornadas de qualificação de público-alvo são ativadas pelo mesmo evento de qualificação de público-alvo, as contagens para limitação de entrada não são precisas. Se as contagens estiverem abaixo do limite, a jornada continuará a arbitrar, mas não poderá obter as contagens mais atualizadas com ativações simultâneas.

## Recursos adicionais

* **[Identificar possíveis conflitos](conflicts.md)**: aprenda a detectar e resolver conflitos entre campanhas e jornadas sobrepostas.
* **[Atribuir pontuações de prioridade](priority-scores.md)**: compreenda como atribuir e usar pontuações de prioridade para controlar a precedência de entrega de mensagens.
* **[Trabalhar com conjuntos de regras](rule-sets.md)**: aprenda a criar e aplicar conjuntos de regras para gestão de conflitos e governança de mensagens.
* **[Limite de jornada e arbitragem](journey-capping.md)**: configure regras de limite e arbitragem em nível de jornada.
* **[Limitação de frequência por canal](channel-capping.md)**: defina limites de frequência no nível do canal para evitar o excesso de mensagens.
* **[Definir horário de silêncio](quiet-hours.md)**: defina exclusões baseadas em tempo para entrega de mensagens.
* **[Tutoriais de gestão de conflitos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: tutoriais em vídeo passo a passo.
* **[Casos de uso do Journey Optimizer](../building-journeys/jo-use-cases.md)**: procure padrões práticos, incluindo limite de frequência e lógica de supressão de jornada.
