---
solution: Journey Optimizer
product: journey optimizer
title: Princípios-chave da criação de campanhas em várias etapas
description: Saiba mais sobre os princípios-chave das campanhas em várias etapas com o Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 36%

---


# Princípios-chave da criação de campanhas em várias etapas {#ms-campaign-creation}

Com o Adobe Journey Optimizer, você pode criar campanhas em várias etapas em uma tela visual para projetar processos entre canais, como segmentação, execução de campanha e processamento de arquivos.

## O que há dentro de uma campanha em várias etapas? {#gs-ms-campaign-inside}

O diagrama de campanha em várias etapas é uma representação do que deveria acontecer. Ele descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Cada campanha em várias etapas contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As várias atividades são representadas no diagrama por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  Em um diagrama de campanha de várias etapas, uma determinada atividade pode produzir várias tarefas, principalmente quando há um loop ou ações recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha em várias etapas usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante o ciclo de vida da campanha de várias etapas.

## Etapas principais para criar uma campanha em várias etapas {#gs-ms-campaign-steps}

As principais etapas para criar uma campanha em várias etapas são as seguintes:

![](assets/workflow-creation-process.png){zoomable="yes"}

