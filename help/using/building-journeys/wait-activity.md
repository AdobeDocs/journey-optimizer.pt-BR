---
title: Atividade de espera
description: Saiba mais sobre a atividade de espera
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 8a68d1e6d498ef3055c703d4e73471ab6d7bff40
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 7%

---

# Atividade de espera{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Atividade de espera"
>abstract="Se desejar esperar antes de executar a próxima atividade no caminho, você pode usar uma atividade Wait . Ela permite definir o momento em que a próxima atividade será executada. Três opções estão disponíveis: duração, data fixa e personalizado."

Se quiser esperar antes de executar a próxima atividade no caminho, use um **[!UICONTROL Wait]** atividade . Ela permite definir o momento em que a próxima atividade será executada. Três opções estão disponíveis:

* [Duração](#duration)
* [Data fixa](#fixed_date)
* [Personalizado](#custom)

<!--* [Email send time optimization](#email_send_time_optimization)-->

## Sobre a atividade Wait{#about_wait}

A duração máxima da espera é de 30 dias. No modo de teste, a variável **[!UICONTROL Wait time in test]** permite definir o tempo que cada atividade de espera durará. O tempo padrão é de 10 segundos. Isso garantirá que os resultados do teste sejam obtidos rapidamente. Consulte [esta página](../building-journeys/testing-the-journey.md)

Tenha cuidado ao usar várias atividades de Espera em uma jornada, pois o tempo limite da jornada global é de 30 dias, o que significa que um perfil sempre deixará de participar da jornada no máximo 30 dias após ter entrado nela.

## Duração da espera{#duration}

Selecione a duração da espera antes da execução da próxima atividade.

![](assets/journey55.png)

## Data de espera fixa{#fixed_date}

Selecione a data para a execução da próxima atividade.

![](assets/journey56.png)

## Aguardar personalizado{#custom}

Essa opção permite definir uma data personalizada, por exemplo, 12 de julho de 2020 às 17h, usando uma expressão avançada com base em um campo proveniente de um evento ou uma fonte de dados. Ela não permite definir uma duração personalizada, por exemplo, 7 dias. A expressão no editor de expressão deve fornecer um formato dateTimeOnly . Consulte esta [página](expression/expressionadvanced.md). Para obter mais informações sobre o formato dateTimeOnly , consulte [página](expression/data-types.md).

>[!NOTE]
>
>Você pode utilizar uma expressão dateTimeOnly ou usar uma função para converter em dateTimeOnly. Por exemplo: toDateTimeOnly(@{Event.offerOpened.activity.endTime}), sendo o campo do evento o formulário 2016-08-12T09:46:06Z.
>
>O **fuso horário** é esperado nas propriedades da sua jornada. Como resultado, hoje não é possível da interface apontar diretamente para um carimbo de data e hora ISO-8601 completo, tempo de combinação e deslocamento de fuso horário como 2016-08-12T09:46:06.982-05. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey57.png)

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
