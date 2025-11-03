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
version: Journey Orchestration
source-git-commit: 5eddbb1f9ab53f1666ccd8518785677018e10f6f
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 3%

---


# Gerenciamento de entrada de perfis {#entry-management}

O gerenciamento de entrada de perfis depende do tipo de jornada.

## Tipos de jornadas {#types-of-journeys}

Com o Adobe Journey Optimizer, você pode criar os seguintes tipos de jornadas:

* **jornadas de evento unitário**: essas jornadas começam com um evento unitário. Quando o evento é recebido, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

* **jornadas de eventos comerciais**: essas jornadas começam com um evento comercial seguido imediatamente por uma atividade **Ler público**. Quando o evento for recebido, os perfis pertencentes ao público-alvo direcionado entram na jornada. Uma instância dessa jornada é criada para cada perfil. [Leia mais](#entry-business)

* jornadas de **Leitura de público-alvo**: essas jornadas começam com uma atividade **Leitura de público-alvo**. Quando a jornada for executada, os perfis que pertencem ao público-alvo de destino entram na jornada. Uma instância dessa jornada é criada para cada perfil. Essas jornadas podem ser recorrentes ou &quot;únicas&quot;. [Leia mais](#entry-read-audience)

* **jornadas de qualificação de público-alvo**: essas jornadas começam com um evento de qualificação de público-alvo. Essas jornadas escutam as entradas e saídas dos perfis nos públicos-alvo. Quando isso acontece, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

Em todos os tipos de jornada, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo, para todas as [versões ativas da jornada](publishing-the-journey.md#journey-versions-journey-versions). Para verificar se uma pessoa está em uma jornada, a identidade do perfil é usada como uma chave. O sistema não permite que a mesma chave, por exemplo, a chave `CRMID=3224`, esteja em locais diferentes na mesma jornada.

## Taxa de processamento de jornada {#journey-processing-rate}

A taxa de processamento da jornada é afetada por vários fatores que determinam como os perfis fluem em uma jornada:

### Taxa de entrada do perfil {#profile-entrance-rate}

A forma como os perfis inserem jornadas e a taxa esperada depende da primeira atividade usada:

* **Ler público-alvo** jornadas (cenário em lote, em que você direciona um público-alvo de perfis e aciona uma jornada para esse público-alvo completo): o máximo é de 20.000 TPS (transações por segundo), que é a cota disponível em um **nível de sandbox**. Se você tiver várias jornadas em execução ao mesmo tempo nessa sandbox, talvez não seja possível atingir 20.000 TPS. Considere esse máximo como o melhor cenário possível.

* **jornadas de qualificação de público-alvo** (cenário unitário, em que você deseja acionar uma jornada quando um perfil é qualificado ou desqualificado para um público-alvo de transmissão): o máximo é de 5.000 TPS. Observe que esse é um limite compartilhado com jornadas que começam com eventos e também é compartilhado entre jornadas em um **nível de organização**.

* **jornadas de evento unitário** (cenário unitário, em que você deseja acionar uma jornada quando um evento é emitido de um perfil): o mesmo acima, ambos compartilhando o mesmo limite de 5.000 TPS. Mais informações sobre a taxa de transferência do evento de jornada estão disponíveis em [esta seção](../event/about-events.md#event-thoughput).

* **jornadas de evento comercial** (que é essencialmente um cenário unitário em lote, pois um evento comercial é sempre seguido por um público de Leitura): os eventos comerciais também contam para a cota de 5.000 TPS, mas a atividade Ler público logo após terá o mesmo limite que as jornadas que começam com um público de Leitura (20.000 TPS).

### Eventos e qualificações de público dentro do jornada {#events-inside-journeys}

Após a entrada, você pode usar as atividades de **Evento unitário** ou **Qualificação de público-alvo** dentro da jornada. Um perfil pode entrar em qualquer um dos quatro tipos de jornadas descritos acima e esperar que um evento seja emitido ou esperar que esse perfil se qualifique para um público-alvo. Esses eventos unitários e qualificações de Público-alvo contarão na cota descrita acima. Por exemplo: se você iniciar uma jornada com um público-alvo de Leitura (com um máximo de 20.000 TPS) e tiver um evento logo após, esse evento terá no máximo 5.000 TPS.

### Impacto das atividades de espera {#wait-activities-impact}

As atividades de **Aguardar** no jornada também podem afetar quantos perfis estão fluindo por uma jornada em um momento específico. Normalmente, uma atividade Wait é baseada em um tempo relativo (por exemplo: sai 2 horas após inserir a espera, portanto, todos os perfis não sairão ao mesmo tempo). No entanto, se um tempo fixo for definido nessa atividade de espera, vários perfis poderão sair dessa jornada exatamente ao mesmo tempo. Esta não é uma prática recomendada. Volumes maciços podem então ser vistos e a TPS a partir deste ponto pode exceder 20.000 TPS.

### Atividades de ação {#action-activities-impact}

Finalmente, as atividades de **ação** (canais nativos como Email, SMS, Push, etc., saída ou entrada, ações personalizadas, saltos ao enviar perfis para outras jornadas, atualização de perfis ao enviar dados para o Unified Profile Service etc.) podem ser afetadas pela carga de perfil proveniente do jornada, mas também podem afetar a taxa de processamento. Por exemplo, uma ação personalizada direcionada a um endpoint externo com um tempo de resposta alto reduzirá a taxa de processamento da jornada.

Para ações personalizadas, o limite padrão é de 300.000 chamadas por minuto, que podem ser alteradas com uma política de limite personalizada. Saiba mais sobre o limite de ação personalizada em [esta seção](../configuration/external-systems.md#capping).

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

Várias opções estão disponíveis para jornadas recorrentes de Leitura de público. Para obter mais informações, consulte a seção [Usar um público em uma jornada](../building-journeys/read-audience.md).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
