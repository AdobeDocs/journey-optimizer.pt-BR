---
title: Atribuir pontuações de prioridade a jornadas e campanhas
description: Saiba como atribuir pontuações de prioridade a jornadas e campanhas.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 35%

---

# Atribuir pontuações de prioridade a jornadas e campanhas {#priority}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à jornada. A prioridade é essencial para priorizar uma jornada quando há uma restrição imposta, como um limite de frequência. Insira um valor numérico (de 0 a 100). Observe que, quanto maior o número, maior a prioridade. Para situações em que duas jornadas têm a mesma pontuação de prioridade, a jornada que foi ativada primeiro será exibida."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à jornada. A prioridade é essencial para priorizar uma jornada quando há uma restrição imposta, como um limite de frequência. Insira um valor numérico (de 0 a 100). Observe que, quanto maior for o número, maior será a prioridade."

O Journey Optimizer permite atribuir uma pontuação de prioridade a uma jornada ou campanha. A prioridade é essencial para priorizar uma jornada, campanha ou ação quando há uma restrição imposta (como um limite de frequência). Em situações em que um cliente se qualifica para muitas jornadas, campanhas ou comunicações e você deseja ser seletivo quanto ao que ele deve informar e receber, você deve utilizar esse campo.

>[!NOTE]
>
>Em campanhas, a pontuação de prioridade está disponível somente para os canais de entrada da Web, no aplicativo e com base em código.

➡️ [Conheça este recurso no vídeo](#video)

Atribuir uma pontuação de prioridade é fundamental para a comunicação de entrada, como Web, Dispositivo móvel e No aplicativo. Se você tiver várias campanhas usando a mesma configuração de canal (por exemplo, um banner na parte superior da página da Web), isso pode ser problemático, pois somente o conteúdo de uma campanha pode ser exibido. A pontuação de prioridade é onde você insere sua preferência para qual campanha deve ser exibida quando o recipient pode se qualificar para mais de uma campanha.

Para atribuir uma pontuação de prioridade a uma jornada ou campanha, insira um valor numérico (de 0 a 100) no campo **[!UICONTROL Pontuação de prioridade]** localizado nas propriedades da jornada ou campanha. Observe que, quanto maior o número, maior a prioridade. Se você estava criando esta campanha e queria garantir que o conteúdo dela fosse exibido, atribuiria a ela uma pontuação de 100.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Se duas jornadas ou campanhas tiverem a mesma pontuação de prioridade, o sistema não terá um mecanismo de interrupção de vínculo. Certifique-se de que as pontuações de prioridade sejam exclusivas para evitar conflitos.

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
