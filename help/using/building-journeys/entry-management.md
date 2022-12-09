---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Gerenciamento de entrada de perfil {#entry-management}

Por padrão, novas jornadas permitem reentrada. Você pode desmarcar a opção para jornadas de &quot;uma só vez&quot;, por exemplo, se quiser oferecer um presente único quando uma pessoa entrar em uma loja. Nesse caso, você não deseja que o cliente possa entrar novamente na jornada e receber a oferta novamente.

![](assets/journey-re-entrance.png)

Quando uma jornada termina, seu status é **[!UICONTROL Closed]**. Novos indivíduos não podem mais entrar na jornada. As pessoas que já se encontram na viagem terminam normalmente a viagem.

Após o tempo limite global padrão de 30 dias, a jornada muda para a **Concluído** status.  [Saiba mais](journey-gs.md#global_timeout).


## Jornadas unitárias{#entry-unitary}

As jornadas unitárias (começando com um evento ou uma qualificação de segmento) incluem uma garantia que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (se for o mesmo evento ou um evento diferente que aciona a mesma jornada), essa jornada não será iniciada novamente para esse perfil.

Além disso:

* Se a reentrada estiver ativada, um perfil poderá entrar em uma jornada várias vezes, mas não poderá fazê-lo até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá inserir várias vezes na mesma jornada

## Ler jornadas de segmento{#entry-read-segment}

Em uma jornada de segmento de leitura:

* Para jornadas não recorrentes: o perfil entra uma vez e somente uma vez na jornada.

* Para jornadas recorrentes: o perfil entra na jornada em cada recorrência, se ele estiver no segmento/status esperado. Se ele ainda estava na jornada de uma recorrência anterior, ele a reiniciará do início.

Em jornadas de eventos comerciais que começam com uma **Ler segmento** atividade : sabendo que essa jornada se baseia na recepção de um evento de negócios, se o perfil estiver qualificado no segmento esperado, ele entrará na jornada de cada evento de negócios recebido, o que significa que esse perfil pode ser várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de eventos de negócios diferentes.
