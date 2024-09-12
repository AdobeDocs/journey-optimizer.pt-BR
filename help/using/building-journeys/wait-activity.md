---
solution: Journey Optimizer
product: journey optimizer
title: Atividade Aguardar
description: Saiba como configurar a atividade de espera
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: aguardar, atividade, jornada, próximo, tela
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: f81fde0076fc8689c689fae7a0ee8c7aa9fdbeed
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 13%

---

# Atividade Aguardar {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Atividade Aguardar"
>abstract="Se quiser esperar antes de executar a próxima atividade no caminho, você pode usar uma atividade Esperar. Ela permite definir o momento em que a próxima atividade será executada. Duas opções estão disponíveis: duração e personalizado."

Você pode usar uma atividade **[!UICONTROL Wait]** para definir uma duração antes de executar a próxima atividade.  A duração máxima de espera é de **90 dias**.

Você pode definir dois tipos de atividade **Aguardar**:

* Uma espera com base em uma duração relativa. [Saiba mais](#duration)
* Uma data personalizada, usando funções para calculá-la. [Saiba mais](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Recomendações {#wait-recommendations}

### Várias atividades de espera {#multiple-wait-activities}

Ao usar várias atividades **Wait** em uma jornada, esteja ciente de que o [tempo limite global](journey-properties.md#global_timeout) para jornada é de 91 dias, o que significa que os perfis estão sempre saindo do máximo da jornada 91 dias após terem inserido. Saiba mais [nesta página](journey-properties.md#global_timeout).

Um indivíduo só poderá inserir uma atividade **Aguardar** se tiver tempo suficiente na jornada para concluir a duração da espera antes do tempo limite de jornada de 91 dias.

### Aguardar e reentrar {#wait-re-entrance}

Uma prática recomendada é não usar atividades de **Aguardar** para bloquear a reentrada. Em vez disso, use a opção **Permitir reentrada** no nível de propriedades da jornada. Saiba mais [nesta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera e teste {#wait-test-modd}

No modo de teste, o parâmetro **[!UICONTROL Tempo de espera em teste]** permite definir o tempo que cada atividade de **Espera** durará. O tempo padrão é de 10 segundos. Isso garantirá que você obtenha os resultados do teste rapidamente. Saiba mais [nesta página](../building-journeys/testing-the-journey.md).

## Configuração {#wait-configuration}

### Espera de duração {#duration}

Selecione o tipo **Duration** para definir a duração relativa da espera antes da execução da próxima atividade. A duração máxima é de **90 dias**.

![Definir a duração da espera](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Espera personalizada {#custom}

Selecione o tipo **Personalizado** para definir uma data personalizada, usando uma expressão avançada com base em um campo proveniente de um evento ou uma resposta de ação personalizada. Não é possível definir uma duração relativa diretamente, por exemplo, 7 dias, mas você pode usar funções para calculá-la se necessário (por exemplo: 2 dias após a compra).

![Definir uma espera personalizada com uma expressão](assets/journey57.png)

A expressão no editor deve fornecer um formato `dateTimeOnly`. Consulte [esta página](expression/expressionadvanced.md). Para obter mais informações sobre o formato dateTimeOnly, consulte [esta página](expression/data-types.md).

A prática recomendada é usar datas personalizadas específicas para seus perfis e evitar o uso da mesma data para todos. Por exemplo, não defina `toDateTimeOnly('2024-01-01T01:11:00Z')`, mas sim `toDateTimeOnly(@event{Event.productDeliveryDate})`, que é específico para cada perfil. Esteja ciente de que o uso de datas fixas pode causar problemas na execução da jornada.


>[!NOTE]
>
>Você pode usar uma expressão `dateTimeOnly` ou usar uma função para converter para `dateTimeOnly`. Por exemplo: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, o campo no evento tem o formato 2023-08-12T09:46:06Z.
>
>O **fuso horário** é esperado nas propriedades da jornada. Como resultado, da interface do usuário, não é possível apontar diretamente para um deslocamento de hora e fuso horário completo da combinação de carimbo de data e hora ISO-8601, como 2023-08-12T09:46:06.982-05. [Saiba mais](../building-journeys/timezone-management.md).


Para validar se a atividade de espera funciona como esperado, você pode usar os eventos da etapa. [Saiba mais](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->

## Nó de espera automático  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Sobre o nó de espera automático"
>abstract="Uma atividade **Wait** é adicionada automaticamente após esta atividade. Está definido para 3 dias. Você pode removê-lo ou configurá-lo conforme necessário."

Cada atividade de mensagem de entrada (mensagem no aplicativo, experiência baseada em código ou Cartão) vem com uma atividade **Wait** de 3 dias. Como as mensagens de entrada terminam automaticamente quando um perfil atinge o final da jornada, pressupomos que você deseje que seus usuários a vejam pelo menos por 3 dias. Você pode remover esta atividade **Aguardar** ou alterar sua configuração, se necessário.