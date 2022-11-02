---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Gerenciamento de entrada de perfil {#entry-management}

Em uma jornada unitária:

* Se a reentrada estiver ativada, um perfil poderá inserir uma jornada várias vezes, mas não poderá fazê-lo até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá inserir várias vezes a mesma jornada

Para obter mais informações sobre a reentrada do perfil, consulte esta seção [seção](../building-journeys/journey-gs.md#change-properties).

Em uma jornada de segmento de leitura:

* Para jornadas não recorrentes: o perfil é inserido uma vez e somente uma vez na jornada.
* para jornadas recorrentes: o perfil insere a jornada em cada recorrência, se ele estiver no segmento/status esperado. Se ele ainda estava na jornada de uma recorrência anterior, ele a reiniciará do início.

Em jornadas de eventos comerciais que começam com um segmento de leitura :

Sabendo que essa jornada se baseia na recepção de um evento de negócios, se o perfil estiver qualificado no segmento esperado, ele inserirá a jornada para cada evento de negócios recebido, o que significa que esse perfil pode ser várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de eventos de negócios diferentes.

As jornadas Unitárias (começando com um evento ou uma qualificação de segmento) incluem uma garantia que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.
