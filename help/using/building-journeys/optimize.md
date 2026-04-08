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
source-git-commit: 8aeb3e3769e28419982c28620e5b141778d2fa67
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 7%

---

# Introdução à atividade Otimizar {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Otimizar atividade"
>abstract="A Atividade **otimizar** permite definir como as pessoas avançam pela jornada ao criar vários caminhos com base em critérios específicos, incluindo experimentação, direcionamento e condições específicas. Observe que a atividade **Otimizar** é o novo veículo para criar caminhos condicionais no jornada. Substitui a antiga atividade **Condition**."

>[!IMPORTANT]
>
>A atividade **Otimizar** é o novo veículo para criar caminhos condicionais no jornada. Substitui a antiga atividade **Condição**, que foi removida da interface do usuário. Toda lógica condicional é retida e agora é tratada por meio das **condições** da atividade [Otimizar](conditions.md).
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
