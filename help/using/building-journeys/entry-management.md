---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: reentrada, jornada, perfil, recorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 6023f1004c74cedc7567fd142be767b12d85ba6d
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 5%

---


# Gerenciamento de entrada de perfis {#entry-management}

O gerenciamento de entrada de perfis depende do tipo de jornada.

## Tipos de jornadas {#types-of-journeys}

Com o Adobe Journey Optimizer, você pode criar os seguintes tipos de jornadas:

* **jornadas de evento unitário**: essas jornadas começam com um evento unitário. Quando o evento é recebido, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

* **jornadas de eventos comerciais**: essas jornadas começam com um evento comercial seguido imediatamente por uma atividade **Ler público**. Quando o evento for recebido, os perfis pertencentes ao público-alvo direcionado entram na jornada. Uma instância dessa jornada é criada para cada perfil. [Leia mais](#entry-business)

* jornadas de **Leitura de público-alvo**: essas jornadas começam com uma atividade **Leitura de público-alvo**. Quando a jornada for executada, os perfis que pertencem ao público-alvo de destino entram na jornada. Uma instância dessa jornada é criada para cada perfil. Essas jornadas podem ser recorrentes ou &quot;únicas&quot;. [Leia mais](#entry-read-audience)

* **jornadas de qualificação de público-alvo**: essas jornadas começam com um evento de qualificação de público-alvo. Essas jornadas escutam as entradas e saídas dos perfis nos públicos-alvo. Quando isso acontece, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

Em todos os tipos de jornada, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Para verificar se uma pessoa está em uma jornada, a identidade do perfil é usada como uma chave. O sistema não permite que a mesma chave, por exemplo, a chave `CRMID=3224`, esteja em locais diferentes na mesma jornada.

## Jornadas unitárias de qualificação de evento e público-alvo{#entry-unitary}

Nas jornadas **Evento unitário** e **Qualificação de público-alvo**, você pode habilitar ou desabilitar a reentrada:

* Se a reentrada estiver ativada, um perfil poderá inserir uma jornada várias vezes, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá entrar várias vezes na mesma jornada dentro do tempo limite global da jornada. Consulte esta [seção](../building-journeys/journey-properties.md#global_timeout).

Por padrão, as jornadas permitem a reentrada. Quando a opção **Permitir reentrada** está ativada, o campo **Período de espera de reentrada** é exibido. Isso permite definir o tempo de espera antes de permitir que um perfil entre na jornada novamente. Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. A duração máxima é de 91 dias ([tempo limite global](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Após o período de reentrada, os perfis podem entrar na jornada novamente. Para evitar isso e desativar totalmente a reentrada desses perfis, você pode adicionar uma condição para testar se o perfil entrou já ou não, usando dados de perfil ou público-alvo.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Jornadas comerciais {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

Em **jornadas comerciais**, para permitir várias execuções de eventos comerciais, ative a opção correspondente na seção **[!UICONTROL Execução]** das propriedades de jornada.

![](assets/business-entry.png)

No caso de eventos comerciais, para determinada jornada, os dados do público-alvo recuperados na primeira execução são reutilizados durante uma janela de tempo de 1 hora.

Um perfil pode estar presente várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de diferentes eventos comerciais.

Para obter mais informações, consulte esta [seção](../event/about-creating-business.md)

## Ler jornadas de público {#entry-read-audience}

**Ler público-alvo** As jornadas podem ser recorrentes ou &quot;únicas&quot;:

* Para jornadas não recorrentes/únicas: o perfil insere uma vez e apenas uma vez na jornada.

* Para jornadas recorrentes: por padrão, todos os perfis pertencentes ao público-alvo inserem a jornada em cada recorrência. Eles devem concluir a jornada antes de entrar novamente em outra ocorrência.

Duas opções estão disponíveis para jornadas recorrentes de Leitura de público:

* Opção **Leitura incremental**: quando uma jornada com uma **Leitura de público** recorrente é executada pela primeira vez, todos os perfis da audiência entram na jornada. Essa opção permite direcionar, após a primeira ocorrência, somente os indivíduos que entraram no público-alvo desde a última execução da jornada.

  >[!NOTE]
  >
  >Se você estiver direcionando um [público-alvo de carregamento personalizado](../audience/about-audiences.md#segments-in-journey-optimizer) na sua jornada, os perfis só serão recuperados na primeira recorrência se essa opção estiver habilitada em uma jornada recorrente, já que esses públicos-alvo são corrigidos.

* **Forçar reentrada na recorrência**: essa opção permite fazer com que todos os perfis ainda presentes na jornada saiam automaticamente na próxima execução. Se a duração dos perfis nesta jornada for maior que a frequência de recorrência (por exemplo, se você usar atividades de espera), não ative essa opção para garantir que os perfis possam concluir a jornada.

![](assets/read-audience-options.png)

Para obter mais informações, consulte esta [seção](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
