---
solution: Journey Optimizer
product: journey optimizer
title: Otimizar atividade
description: Saiba mais sobre a atividade Otimizar
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: atividade, condição, tela, jornada, otimização
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1094
ht-degree: 6%

---

# Introdução à atividade Otimizar {#journey-path-optimization}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade Otimize para criar vários caminhos de jornada com base em experimentação, direcionamento e condições, substituindo a antiga atividade Condition.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Otimizar atividade"
>abstract="A Atividade **otimizar** permite definir como as pessoas avançam pela jornada ao criar vários caminhos com base em critérios específicos, incluindo experimentação, direcionamento e condições específicas. Observe que a atividade **Otimizar** é o novo veículo para criar caminhos condicionais na jornada. Substitui a antiga atividade **Condições**."

>[!IMPORTANT]
>
>A atividade **Otimizar** é o novo veículo para criar caminhos condicionais no jornada. Substitui a antiga atividade **Condição**, que foi removida da interface. Toda lógica condicional é retida e agora é tratada por meio das [condições](conditions.md) da atividade **Otimizar**.
>
>Se você tiver jornadas existentes que usaram atividades de **[!UICONTROL Condição]**, poderá continuar a usá-las como antes. Agora eles aparecem com um novo ícone como **[!UICONTROL Otimizar]** atividades usando o método **[!UICONTROL Condição]**, mas o comportamento não é alterado. Qualquer rótulo personalizado definido no nó é preservado.

A atividade **Otimizar** permite definir como as pessoas avançam na sua jornada criando vários **caminhos** com base em critérios específicos, incluindo experimentação, direcionamento e condições específicas, garantindo o máximo de envolvimento e sucesso na criação de jornadas altamente personalizadas e eficazes.

![Botão Otimizar da paleta de atividades de jornada](assets/journey-optimize.png)

## O que é um caminho de jornada? {#journey-path}

Um **caminho** de jornada pode consistir em qualquer um dos seguintes: sequenciamento de comunicações, tempo entre elas, número de comunicações ou qualquer combinação dessas três variáveis.

Por exemplo, um caminho pode conter um email, outro pode conter duas mensagens SMS e um terceiro pode conter um email, um nó de espera de duas horas e, em seguida, uma mensagem SMS.

## Três maneiras de otimizar suas jornadas {#optimization-methods}

Através da atividade **Otimizar**, você pode executar as seguintes ações nos seus caminhos de jornada:

* [Executar experimentos de caminho](path-experimentation.md) - Teste caminhos diferentes com base em divisões aleatórias para determinar qual tem o melhor desempenho de acordo com as métricas de sucesso predefinidas (por exemplo: taxa de conversão, receita, envolvimento).

* [Aproveite as regras de direcionamento](path-targeting.md) - Defina regras específicas que devem ser atendidas para que um cliente seja qualificado para inserir um dos caminhos de jornada, com base em segmentos de público-alvo, atributos de perfil ou dados contextuais. Isso garante que o público-alvo correto entre no caminho especificado.

  >[!AVAILABILITY]
  >
  >No momento, esse recurso está com a Disponibilidade limitada. Para solicitar acesso, entre em contato com o representante da Adobe.

* [Aplicar condições](conditions.md) - Crie caminhos condicionais com base em critérios específicos, como fontes de dados, hora, data, divisões de porcentagem ou limites de perfil. É equivalente à antiga atividade de Condição.

## Como funciona {#how-it-works}

Quando a jornada estiver ativa, os perfis serão avaliados de acordo com os critérios definidos e, com base nos critérios de correspondência, serão enviados pelo caminho apropriado da jornada.

## Próximas etapas {#next-steps}

Selecione o método de otimização que melhor se adapta ao seu caso de uso:

* Deseja testar e saber qual caminho tem melhor desempenho? → Ir para [Experimentação de caminho](path-experimentation.md)
* Deseja enviar públicos diferentes por caminhos específicos? → Vá para [Direcionamento de caminho](path-targeting.md)
* Deseja criar uma lógica condicional (cenários if/then)? → Vá para [Condições](conditions.md)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página apresenta a atividade Otimize, a substituição da antiga atividade Condition, que permite aos usuários criar vários caminhos de jornada usando experimentação, regras de direcionamento ou lógica condicional.

**Intenções:**

* Entenda o que a atividade Otimizar faz e como ela substitui a antiga atividade Condição
* Criar vários caminhos de jornada usando a experimentação de caminho (teste A/B)
* Definir regras de direcionamento para rotear segmentos de público-alvo ou atributos de perfil específicos para caminhos separados
* Aplicar lógica condicional (if/then) usando o método Condições na atividade Otimizar
* Migrar jornadas existentes que usaram a atividade Condição para a nova atividade Otimizar

**Glossário:**

* **Atividade Otimizar**: a atividade da tela de jornada que substitui a antiga atividade Condição e permite a criação de vários caminhos por meio de experimentação, direcionamento ou condições. *(específico do produto)*
* **Caminho da Jornada**: uma sequência em uma jornada que pode consistir em comunicações, tempos de espera, número de mensagens ou qualquer combinação; os perfis são roteados para um caminho com base em critérios definidos na atividade Otimize. *(específico do produto)*
* **Experimentação de caminho**: um método Otimize que divide aleatoriamente perfis entre caminhos para determinar qual tem melhor desempenho em relação a métricas de sucesso predefinidas, como taxa de conversão ou receita. *(específico do produto)*
* **Direcionamento de caminho**: um método Otimize (atualmente com Disponibilidade Limitada) que roteia perfis para caminhos com base em segmentos de público-alvo, atributos de perfil ou dados contextuais. *(específico do produto)*
* **Condições**: um método Otimize equivalente à atividade Condition anterior, criando caminhos condicionais com base em fontes de dados, hora, data, divisões de porcentagem ou limites de perfil. *(específico do produto)*

**Medidas de Proteção:**

* No momento, o direcionamento de caminho está em Disponibilidade limitada — entre em contato com o representante da Adobe para solicitar acesso
* A antiga atividade Condição foi removida da interface do usuário; as jornadas existentes que a utilizavam continuam a funcionar e agora são exibidas com um novo ícone como Otimizar atividades usando o método Condições
* Os rótulos personalizados definidos em nós de condição anteriores são preservados após a migração para Otimizar

**Terminologia:**

* Nome canônico: atividade Otimize — Acrônimo: none — variantes: otimização de caminho de jornada, nó Otimize
* Sinônimos: &quot;Atividade de otimização (método de condições)&quot; = &quot;antiga atividade de condição&quot;
* Não confunda: &quot;Path experimentation&quot; ≠ &quot;Path targeting&quot; — A experimentação de caminho usa divisões aleatórias para testar qual caminho tem melhor desempenho; o direcionamento de caminho usa regras definidas para rotear públicos específicos para caminhos específicos

**Perguntas frequentes:**

* **P: O que aconteceu com a atividade de Condição?** — Ela foi substituída pela atividade Otimizar e removida da interface. As jornadas existentes que usavam atividades de Condição continuam a funcionar inalteradas; agora são exibidas com um novo ícone como Otimizar atividades usando o método Condições.
* **P: Quais são os três métodos disponíveis na atividade Otimizar?** — experimentação de caminho (divisões A/B aleatórias para encontrar o caminho com melhor desempenho), direcionamento de caminho (roteamento baseado em regras por público-alvo ou atributos de perfil, atualmente em Disponibilidade limitada) e Condições (lógica condicional if/then equivalente à atividade Condition anterior).
* **P: Qual é a diferença entre a experimentação de caminho e o direcionamento de caminho?** — a experimentação de caminhos divide aleatoriamente os perfis para testar e comparar o desempenho dos caminhos com as métricas de sucesso; o direcionamento de caminhos direciona públicos-alvo específicos ou tipos de perfis para caminhos designados com base em critérios definidos.
* **P: O direcionamento de caminho está disponível?** — Não; está atualmente com disponibilidade limitada. Entre em contato com seu representante da Adobe para solicitar acesso.
* **P: O que é um caminho de jornada?** — Um caminho é uma sequência dentro de uma jornada que pode incluir uma combinação de comunicações, períodos de espera e contagens de mensagens. Os perfis são avaliados e roteados para o caminho apropriado pelos critérios de atividade Otimizar.

+++
