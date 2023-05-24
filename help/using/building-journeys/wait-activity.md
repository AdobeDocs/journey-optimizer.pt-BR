---
solution: Journey Optimizer
product: journey optimizer
title: Atividade de espera
description: Saiba mais sobre a atividade de espera
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: aguardar, atividade, jornada, próximo, tela
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 23%

---

# Atividade de espera{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Atividade de espera"
>abstract="Se quiser esperar antes de executar a próxima atividade no caminho, você pode usar uma atividade Esperar. Ela permite definir o momento em que a próxima atividade será executada. Duas opções estão disponíveis: duração e personalizado."

Se quiser aguardar antes de executar a próxima atividade no caminho, você poderá usar um **[!UICONTROL Aguardar]** atividade. Ela permite definir o momento em que a próxima atividade será executada. Três opções estão disponíveis:

* [Duração](#duration)
* [Personalizado](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Sobre a atividade Wait{#about_wait}

A duração máxima de espera é de 30 dias. No modo de teste, a variável **[!UICONTROL Tempo de espera no teste]** permite definir o tempo que cada atividade de espera durará. O tempo padrão é de 10 segundos. Isso garantirá que você obtenha os resultados do teste rapidamente. Consulte [esta página](../building-journeys/testing-the-journey.md)

Tenha cuidado ao usar várias atividades de espera em uma jornada, pois o tempo limite da jornada global é de 30 dias, o que significa que um perfil sempre desaparecerá do máximo da jornada 30 dias após ter entrado.

## Espera de duração{#duration}

Selecione a duração da espera antes da execução da próxima atividade.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Espera personalizada{#custom}

Essa opção permite definir uma data personalizada, por exemplo, 12 de julho de 2020 às 17h, usando uma expressão avançada com base em um campo proveniente de um evento ou de uma fonte de dados. Isso não permite definir uma duração personalizada, por exemplo, 7 dias. A expressão no editor de expressão deve fornecer um formato dateTimeOnly. Consulte esta [página](expression/expressionadvanced.md). Para obter mais informações sobre o formato dateTimeOnly, consulte esta [página](expression/data-types.md).

>[!NOTE]
>
>Você pode usar uma expressão dateTimeOnly ou usar uma função para converter em dateTimeOnly. Por exemplo: toDateTimeOnly(@{Event.offerOpened.activity.endTime}), o campo no evento será do formulário 2016-08-12T09:46:06Z
>
>A variável **fuso horário** é esperado nas propriedades da jornada. Como resultado, não é possível, hoje, a partir da interface apontar diretamente para um carimbo de data e hora ISO-8601 completo misturando deslocamento de tempo e fuso horário como 2016-08-12T09:46:06.982-05 Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey57.png)

Para validar se a atividade de espera funciona como esperado, você pode usar os eventos da etapa. Consulte [esta página](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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


