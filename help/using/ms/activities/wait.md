---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Wait em campanhas com várias etapas
description: Saiba como usar a atividade de espera em campanhas com várias etapas
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 77%

---

# Aguardar {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Atividade Aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."

A atividade **Aguardar** é uma atividade de **Controle de fluxo**. Ela é usada para permitir que um determinado período transcorra entre duas atividades que estão sendo executadas. Por exemplo, a espera de vários dias após uma atividade de entrega de email para depois analisar as aberturas e os cliques gerados durante esse período antes de executar qualquer operação de acompanhamento (email de lembrete, criação de público-alvo, etc.).

## Configuração{#wait-configuration}

Siga estas etapas para configurar a atividade **Aguardar**:

1. Adicione uma atividade **Wait** à campanha em várias etapas.

1. Especifique a **Duração** da espera entre as transições de entrada e saída.

1. Selecione a unidade de tempo no campo **Períodos**: segundos, minutos, horas, dias.

## Exemplo{#wait-example}

O exemplo a seguir ilustra a atividade **Aguardar** em um caso de uso comum. Um convite é enviado por email para um evento. 24 horas após o envio, é feita uma entrega de SMS para a mesma população.

![](../assets/workflow-wait-example.png)
