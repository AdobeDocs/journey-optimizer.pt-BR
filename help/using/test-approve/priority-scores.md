---
title: Atribuir pontuações de prioridade a jornadas e campanhas
description: Saiba como atribuir pontuações de prioridade a jornadas e campanhas.
role: User
level: Beginner
badge: label="Disponibilidade limitada"
hide: true
hidefromtoc: true
source-git-commit: 0eedadee1e8c1d4642d8602d48bcc9a49a0a2e53
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 9%

---


# Atribuir pontuações de prioridade a jornadas e campanhas {#priority}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao gerenciamento de conflitos e priorização](gs-conflict-prioritization.md)
* [Detectar possíveis conflitos em jornadas e campanhas](conflicts.md)
* **[Atribuir pontuações de prioridade a jornadas e campanhas](priority-scores.md)**
* [Limite e arbitragem de jornada](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>As ferramentas de gerenciamento e priorização de conflitos estão disponíveis atualmente como uma Disponibilidade limitada somente para usuários selecionados.

O Journey Optimizer permite atribuir uma pontuação de prioridade a uma jornada ou campanha. A prioridade é essencial para priorizar uma jornada, campanha ou ação quando há uma restrição imposta (como um limite de frequência). Em situações em que um cliente se qualifica para muitas jornadas, campanhas ou comunicações e você deseja ser seletivo quanto ao que ele deve informar e receber, você deve utilizar esse campo.

>[!NOTE]
>
>A pontuação de prioridade está disponível para canais de entrada: canais da Web, no aplicativo e baseados em código. No jornada, a pontuação de prioridade está disponível somente para os canais **no aplicativo** e **baseados em código**.

➡️ [Descubra este recurso no vídeo](#video)

Atribuir uma pontuação de prioridade é fundamental para a comunicação de entrada, como Web, Dispositivo móvel e No aplicativo. Se você tiver várias campanhas usando a mesma configuração de canal (por exemplo, um banner na parte superior da página da Web), isso pode ser problemático, pois somente o conteúdo de uma campanha pode ser exibido. A pontuação de prioridade é onde você insere sua preferência para qual campanha deve ser exibida quando o recipient pode se qualificar para mais de uma campanha.

Para atribuir uma pontuação de prioridade a uma jornada ou campanha, insira um valor numérico (de 0 a 100) no campo **[!UICONTROL Pontuação de prioridade]** localizado nas propriedades da jornada ou campanha. Observe que quanto maior o número, maior a prioridade. Se você estava criando esta campanha e queria garantir que o conteúdo dela fosse exibido, atribuiria a ela uma pontuação de 100.

![](assets/priority-score.png)

Para situações em que duas campanhas têm a mesma pontuação de prioridade, a campanha que foi ativada primeiro será exibida.

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
