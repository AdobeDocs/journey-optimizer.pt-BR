---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Scheduler
description: Saiba como usar a atividade Scheduler em uma campanha de várias etapas
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 21%

---

# Scheduler {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Atividade Scheduler"
>abstract="A atividade **Scheduler** permite agendar quando a campanha de várias etapas será iniciada. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade da campanha em várias etapas."


A atividade **Scheduler** é uma atividade de **Controle de fluxo**. Ele permite programar quando a campanha em várias etapas será iniciada. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade da campanha em várias etapas.

## Práticas recomendadas{#scheduler-best-practices}

* Não agende uma campanha em várias etapas para execução por mais de 15 minutos, pois pode atrapalhar o desempenho geral do sistema e criar bloqueios no banco de dados.
* Se quiser enviar uma entrega instantânea em sua campanha de várias etapas, adicione uma atividade de agendador e configure-a para ser executada **Uma vez**. Você também pode definir o **Cronograma** nas configurações de entrega.
* Para enviar uma entrega recorrente em sua campanha de várias etapas, é necessário usar uma atividade **Scheduler** e definir a frequência de execução. A atividade recorrente de delivery não permite definir um agendamento.

## Configuração de atividade do scheduler {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validade do Scheduler"
>abstract="É possível definir um período de validade para o Scheduler. Pode ser permanente (padrão) ou pode ser válido até uma data específica."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opções do Scheduler"
>abstract="Defina a frequência do scheduler. Pode ser executado em um momento específico, uma ou várias vezes por dia, semana ou mês."

Siga estas etapas para configurar a atividade **Scheduler**:

![](../assets/workflow-scheduler.png)

1. Adicione uma atividade **Scheduler** à sua campanha de várias etapas.

1. Configure a **Frequência de execução**:

   * **Uma vez**: a campanha em várias etapas é executada uma única vez.

   * **Diariamente**: a campanha em várias etapas é executada em um horário específico, uma vez por dia.

   * **Várias vezes por dia:** a campanha em várias etapas é executada regularmente várias vezes por dia. Você pode configurar as execuções em horários específicos ou periodicamente.

   * **Semanalmente**: a campanha em várias etapas é executada em um horário especificado, uma ou várias vezes por semana.

   * **Monthly**: a campanha em várias etapas é executada em um momento especificado, uma ou várias vezes por mês. Você pode selecionar meses quando precisar que a campanha em várias etapas seja executada. Você também pode configurar as execuções em dias da semana especificados do mês, como a segunda terça-feira do mês.

1. Defina os detalhes da execução de acordo com a frequência selecionada. Os campos de detalhes podem variar dependendo da frequência usada (tempo, frequência de repetição, dias especificados etc.).

1. Clique em **Visualizar horários de inicialização** para verificar o agendamento das próximas dez execuções da sua campanha em várias etapas.

1. Defina o período de validade do scheduler:

   * **Permanente (nunca expira)**: a campanha em várias etapas é executada, de acordo com a frequência especificada, sem limites para o intervalo de tempo ou o número de iterações.

   * **Período de validade**: a campanha em várias etapas é executada de acordo com a frequência especificada, até uma data específica. É necessário especificar datas de início e término.

>[!NOTE]
>
>Se quiser iniciar a campanha em várias etapas imediatamente, clique em **Executar tarefa pendente** na barra de ações superior do agendador. Esse botão só estará disponível quando você tiver iniciado a campanha em várias etapas.

## Exemplo{#scheduler-example}

No exemplo a seguir, a atividade é configurada para que a campanha em várias etapas seja executada várias vezes por dia às 9h e às 12h, todos os dias da semana de 1º de outubro de 2025 a 1º de janeiro de 2026.

![](../assets/workflow-scheduler2.png)
