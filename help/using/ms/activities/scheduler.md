---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Scheduler
description: Saiba como usar a atividade Scheduler em uma campanha orquestrada
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 21%

---

# Scheduler {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Atividade Scheduler"
>abstract="A atividade **Scheduler** permite agendar quando a campanha orquestrada será iniciada. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade da campanha orquestrada."


A atividade **Scheduler** é uma atividade de **Controle de fluxo**. Ele permite programar quando a campanha orquestrada será iniciada. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade da campanha orquestrada.

## Práticas recomendadas{#scheduler-best-practices}

* Não programe uma campanha orquestrada para execução por mais de 15 minutos, pois isso pode atrapalhar o desempenho geral do sistema e criar bloqueios no banco de dados.
* Se quiser enviar uma entrega instantânea em sua campanha orquestrada, adicione uma atividade de agendador e configure-a para ser executada **Uma vez**. Você também pode definir o **Cronograma** nas configurações de entrega.
* Para enviar uma entrega recorrente em sua campanha orquestrada, é necessário usar uma atividade **Scheduler** e definir a frequência de execução. A atividade recorrente de delivery não permite definir um agendamento.

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

1. Adicione uma atividade **Scheduler** à sua campanha orquestrada.

1. Configure a **Frequência de execução**:

   * **Uma vez**: a campanha orquestrada é executada uma única vez.

   * **Diariamente**: a campanha orquestrada é executada em um horário específico, uma vez por dia.

   * **Várias vezes ao dia:** a campanha orquestrada é executada regularmente várias vezes ao dia. Você pode configurar as execuções em horários específicos ou periodicamente.

   * **Semanalmente**: a campanha orquestrada é executada em um momento especificado, uma ou várias vezes por semana.

   * **Monthly**: a campanha orquestrada é executada em um momento especificado, uma ou várias vezes por mês. Você pode selecionar meses quando precisar que a campanha orquestrada seja executada. Você também pode configurar as execuções em dias da semana especificados do mês, como a segunda terça-feira do mês.

1. Defina os detalhes da execução de acordo com a frequência selecionada. Os campos de detalhes podem variar dependendo da frequência usada (tempo, frequência de repetição, dias especificados etc.).

1. Clique em **Visualizar horas de inicialização** para verificar a programação das próximas dez execuções da sua campanha orquestrada.

1. Defina o período de validade do scheduler:

   * **Permanente (nunca expira)**: a campanha orquestrada é executada, de acordo com a frequência especificada, sem limites para o intervalo de tempo ou o número de iterações.

   * **Período de validade**: a campanha orquestrada é executada de acordo com a frequência especificada, até uma data específica. É necessário especificar datas de início e término.

>[!NOTE]
>
>Se quiser iniciar a campanha orquestrada imediatamente, clique em **Executar tarefa pendente** na barra de ação superior do agendador. Esse botão só estará disponível quando você tiver iniciado a campanha orquestrada.

## Exemplo{#scheduler-example}

No exemplo a seguir, a atividade é configurada para que a campanha orquestrada seja executada várias vezes por dia, às 9h e às 12h, todos os dias da semana, de 1º de outubro de 2025 a 1º de janeiro de 2026.

![](../assets/workflow-scheduler2.png)
