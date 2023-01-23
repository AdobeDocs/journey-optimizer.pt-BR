---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys
role: User
level: Intermediate
keywords: reentrada, jornada, perfil, recorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---

# Gerenciamento de entrada de perfil {#entry-management}

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção por jornadas de &quot;uma ocorrência&quot;, por exemplo, se quiser oferecer um presente único quando uma pessoa entrar em uma loja. Nesse caso, você não deseja que o cliente possa entrar novamente na jornada e receber a oferta novamente.

![](assets/journey-re-entrance.png)

Quando uma jornada termina, seu status é **[!UICONTROL Fechado]**. Novos indivíduos não podem mais entrar na jornada. Pessoas que já estão na jornada terminam a jornada normalmente.

Após o tempo limite global padrão de 30 dias, a jornada muda para a **Concluído** status.  [Saiba mais](journey-gs.md#global_timeout).


## Jornadas Unitárias{#entry-unitary}

As jornadas unitárias (começando com um evento ou uma qualificação de segmento) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

Além disso:

* Se a reentrada estiver ativada, um perfil poderá inserir uma jornada várias vezes, mas não poderá fazê-lo até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá inserir várias vezes a mesma jornada

## Ler jornadas de segmento{#entry-read-segment}

Em uma jornada de segmento de leitura:

* Para jornadas não recorrentes: o perfil é inserido uma vez e somente uma vez na jornada.

* Para jornadas recorrentes: o perfil insere a jornada em cada recorrência, se ele estiver no segmento/status esperado. Se ele ainda estava na jornada de uma recorrência anterior, ele a reiniciará do início.

Em jornadas de evento comercial que começam com um **Ler segmento** atividade : sabendo que essa jornada se baseia na recepção de um evento de negócios, se o perfil estiver qualificado no segmento esperado, ele inserirá a jornada para cada evento de negócios recebido, o que significa que esse perfil pode ser várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de eventos de negócios diferentes.
