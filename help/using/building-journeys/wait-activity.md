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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qWxnLiuHh-sJQyUOuRB6CgRIpZ6ud6eO-WNoWcv9JeU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 932
ht-degree: 7%

---

# Atividade aguardar {#wait-activity}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como configurar a atividade de espera para pausar um caminho por uma duração relativa ou até uma data calculada personalizada antes da execução da próxima atividade.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Atividade aguardar"
>abstract="A atividade Wait permite aguardar antes de executar a próxima atividade no caminho. Ela permite definir o momento em que a próxima atividade será executada. Duas opções estão disponíveis: duração e personalizado."

Você pode usar uma atividade **[!UICONTROL Wait]** para definir uma duração antes de executar a próxima atividade.  A duração máxima de espera é de **90 dias**.

Você pode definir dois tipos de atividade **Aguardar**:

* Uma espera com base em uma duração relativa. [Saiba mais](#duration)
* Uma data personalizada, usando funções para calculá-la. [Saiba mais](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Recomendações {#wait-recommendations}

Use essas recomendações para manter as esperas previsíveis e seguras.

### Várias atividades de espera {#multiple-wait-activities}

Ao usar várias atividades **Wait** em uma jornada, esteja ciente de que o [tempo limite global](journey-properties.md#global_timeout) para jornada é de 91 dias, o que significa que os perfis estão sempre saindo do máximo da jornada 91 dias após terem inserido. Saiba mais [nesta página](journey-properties.md#global_timeout).

Um indivíduo só poderá inserir uma atividade **Aguardar** se tiver tempo suficiente na jornada para concluir a duração da espera antes do tempo limite de jornada de 91 dias.

### Espera e reentrada {#wait-reentrance}

Uma prática recomendada para não usar as atividades **Aguardar** para bloquear a reentrada. Em vez disso, use a opção **Permitir reentrada** no nível de propriedades da jornada. Saiba mais [nesta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera e teste {#wait-test-mode}

No modo de teste, o parâmetro **[!UICONTROL Tempo de espera em teste]** permite definir o tempo que cada atividade de **Espera** durará. O tempo padrão é de 10 segundos. Isso garantirá que você obtenha os resultados do teste rapidamente. Saiba mais [nesta página](../building-journeys/testing-the-journey.md).

### Canais de espera e móveis {#wait-mobile-channels}

Se você quiser mostrar uma [mensagem no aplicativo](../in-app/create-in-app.md) logo após enviar uma [notificação por push](../../rp_landing_pages/push-landing-page.md), use uma atividade **Aguardar** para permitir que o tempo de carga da mensagem no aplicativo seja propagado. Normalmente, recomenda-se uma espera de 5 a 15 minutos, mas os tempos exatos podem variar dependendo da complexidade da carga útil e das necessidades de personalização.

## Configuração {#wait-configuration}

Configure a duração e o tempo de espera aqui.

### Espera de duração {#duration}

Selecione o tipo **Duration** para definir a duração relativa da espera antes da execução da próxima atividade. A duração máxima é de **90 dias**.

![Definir a duração da espera](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)
-->

### Espera personalizada {#custom}

Selecione o tipo **Personalizado** para definir uma data personalizada, usando uma expressão avançada com base em um campo proveniente de um evento ou uma resposta de ação personalizada. Não é possível definir uma duração relativa diretamente, por exemplo, 7 dias, mas você pode usar funções para calculá-la se necessário (por exemplo: 2 dias após a compra).

![Definir uma espera personalizada com uma expressão](assets/journey57.png)

A expressão no editor deve fornecer um formato `dateTimeOnly`. Consulte [esta página](expression/expressionadvanced.md). Para obter mais informações sobre o formato dateTimeOnly, consulte [esta página](expression/data-types.md).

A prática recomendada é usar datas personalizadas específicas para seus perfis e evitar o uso da mesma data para todos. Por exemplo, não defina `toDateTimeOnly('2024-01-01T01:11:00Z')`, mas sim `toDateTimeOnly(@event{Event.productDeliveryDate})`, que é específico para cada perfil. Esteja ciente de que o uso de datas fixas pode causar problemas na execução da jornada. Saiba mais sobre o impacto das atividades de espera na taxa de processamento da jornada em [esta seção](entry-management.md#wait-activities-impact).


>[!CAUTION]
>
>Ao trabalhar com expressões `dateTimeOnly`, lembre-se do seguinte:
>
>* Você pode usar uma expressão `dateTimeOnly` diretamente ou convertê-la usando uma função — por exemplo: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})` onde o valor do campo está no formato `2023-08-12T09:46:06Z`.
>* O **fuso horário** está definido nas propriedades da jornada. Como resultado, não é possível que a interface aponte para um carimbo de data e hora ISO-8601 completo que mescla deslocamento de hora e fuso horário, como `2023-08-12T09:46:06.982-05`. [Saiba mais](../building-journeys/timezone-management.md)
>* Ao criar uma expressão de espera personalizada com `toDateTimeOnly()`, **não** anexe `Z` ou um deslocamento de fuso horário (por exemplo, `-05:00`). A expressão deve fazer referência ao fuso horário configurado pela jornada sem designadores de fuso horário explícitos; caso contrário, os perfis podem ficar presos na atividade de espera.
>
>| | Exemplo |
>|---|---|
>| **Correto** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))` |
>| **Incorreto** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ (contém `Z`) |

Para validar se a atividade de espera funciona como esperado, você pode usar os eventos da etapa. [Saiba mais](../reports/query-examples.md#common-queries).

## Atualização de perfil após espera {#profile-refresh}

Quando um perfil é estacionado em uma atividade **Wait** em uma jornada que começa com uma atividade **Read Audience**, a jornada atualiza automaticamente os atributos do perfil no UPS (Serviço de Perfil Unificado) para buscar os dados mais recentes disponíveis.

* **Na entrada da jornada**: os perfis usam valores de atributo do instantâneo de público-alvo que foi avaliado quando a jornada foi iniciada.
* **Após um nó de espera**: a jornada executa uma pesquisa para recuperar os dados de perfil mais recentes do UPS, não os dados de instantâneo mais antigos. Isso significa que os atributos de perfil podem ter sido alterados desde o início da jornada.

Esse comportamento garante que as atividades downstream usem informações atuais do perfil após um período de espera. No entanto, poderá produzir resultados inesperados se você esperar que a jornada use apenas os dados do instantâneo original durante toda a execução.

Exemplo: se um perfil se qualificar para um público-alvo de &quot;cliente Silver&quot; no início da jornada, mas atualizar para &quot;cliente Gold&quot; durante uma espera de 3 dias, as atividades após a espera verão o status atualizado de &quot;cliente Gold&quot;.

## Nó de espera automático  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node"
>title="Sobre o nó de espera automático"
>abstract="Um nó **Wait** é inserido automaticamente após esta ação de entrada. É definido como 3 dias por padrão, garantindo que os perfis permaneçam na jornada por tempo suficiente para exibir a mensagem ou a experiência. A duração da espera pode ser atualizada ou o nó removido, se o caso de uso exigir."

Cada atividade de experiência de entrada (mensagem no aplicativo, experiência baseada em código ou Cartão) vem com uma atividade de **Aguardar** de 3 dias. Como as mensagens de entrada terminam automaticamente quando um perfil atinge o final da jornada, pressupomos que você deseje que seus usuários a vejam pelo menos por 3 dias. Você pode remover esta atividade **Aguardar** ou alterar sua configuração, se necessário.
