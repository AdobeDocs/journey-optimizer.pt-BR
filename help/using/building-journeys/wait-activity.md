---
solution: Journey Optimizer
product: journey optimizer
title: Atividade aguardar
description: Saiba como configurar a atividade de espera
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: aguardar, atividade, jornada, próximo, tela
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: db3c87d10469550eb30224c932344ff1e3ae1767
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 17%

---

# Atividade aguardar {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Atividade aguardar"
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

### Espera e reentrada {#wait-reentrance}

Uma prática recomendada para não usar as atividades **Aguardar** para bloquear a reentrada. Em vez disso, use a opção **Permitir reentrada** no nível de propriedades da jornada. Saiba mais [nesta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera e teste {#wait-test-mode}

No modo de teste, o parâmetro **[!UICONTROL Tempo de espera em teste]** permite definir o tempo que cada atividade de **Espera** durará. O tempo padrão é de 10 segundos. Isso garantirá que você obtenha os resultados do teste rapidamente. Saiba mais [nesta página](../building-journeys/testing-the-journey.md).

### Canais de espera e móveis {#wait-mobile-channels}

Se você quiser mostrar uma [mensagem no aplicativo](../in-app/create-in-app.md) logo após enviar uma [notificação por push](../push/get-started-push.md), use uma atividade **Aguardar** para permitir que o tempo de carga da mensagem no aplicativo seja propagado. Normalmente, recomenda-se uma espera de 5 a 15 minutos, mas os tempos exatos podem variar dependendo da complexidade da carga útil e das necessidades de personalização.

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

## Nó de espera automático  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Sobre o nó de espera automático"
>abstract="Uma atividade de **Espera** é adicionada automaticamente após esta atividade. Ela é definida para 3 dias. É possível removê-la ou configurá-la conforme necessário."

Cada atividade de experiência de entrada (mensagem no aplicativo, experiência baseada em código ou Cartão) vem com uma atividade de **Aguardar** de 3 dias. Como as mensagens de entrada terminam automaticamente quando um perfil atinge o final da jornada, pressupomos que você deseje que seus usuários a vejam pelo menos por 3 dias. Você pode remover esta atividade **Aguardar** ou alterar sua configuração, se necessário.