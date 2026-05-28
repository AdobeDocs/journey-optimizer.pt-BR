---
title: Atribuir pontuações de prioridade a jornadas e campanhas
description: Saiba como atribuir pontuações de prioridade a jornadas e campanhas.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
TQID: https://experienceleague.adobe.com/An8xmTbO8yWDFizK1B8uvSFkr0t6e9a59ntUoLqhosw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fd59660e-de8a-4bfb-85dc-7fa546030c49
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
subfeature_v2:
  - id: f3fe4813-f254-4f8f-99cc-24bd67f119e1
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 615
ht-degree: 35%

---

# Atribuir pontuações de prioridade {#priority}

O Journey Optimizer permite atribuir uma pontuação de prioridade a uma jornada, campanha ou ação de canal de entrada na atividade de jornada **[!UICONTROL Ação]**.

A prioridade é essencial para priorizar uma jornada, campanha ou ação quando há uma restrição imposta (como um limite de frequência).

Em situações em que um cliente se qualifica para muitas jornadas, campanhas ou comunicações e você deseja ser seletivo quanto ao que ele deve informar e receber, você deve utilizar esse campo.

## Atribuir pontuações de prioridade a jornadas e campanhas {#priority-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à campanha. A prioridade é essencial para priorizar uma campanha quando há uma restrição imposta, como um limite de frequência.</br>Insira um valor numérico (de 0 a 100). Observe que, quanto maior o número, maior a prioridade. Para situações em que duas campanhas têm a mesma pontuação de prioridade, a campanha que foi ativada primeiro será exibida."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à jornada. A prioridade é essencial para priorizar uma jornada quando há uma restrição imposta, como um limite de frequência.</br>Insira um valor numérico (de 0 a 100). Observe que, quanto maior o número, maior a prioridade. Para situações em que duas jornadas têm a mesma pontuação de prioridade, a jornada que foi ativada primeiro será exibida."

➡️ [Conheça este recurso no vídeo](#video)

Atribuir uma pontuação de prioridade é fundamental para a comunicação de entrada, como Web, Dispositivo móvel e No aplicativo. Se você tiver várias campanhas usando a mesma configuração de canal (por exemplo, um banner na parte superior da página da Web), isso pode ser problemático, pois somente o conteúdo de uma campanha pode ser exibido. A pontuação de prioridade é onde você insere sua preferência para qual campanha deve ser exibida quando o recipient pode se qualificar para mais de uma campanha.

>[!NOTE]
>
>Em campanhas, a pontuação de prioridade está disponível somente para os canais de entrada da Web, no aplicativo e com base em código.

Para atribuir uma pontuação de prioridade a uma jornada ou campanha, insira um valor numérico (de 0 a 100) no campo **[!UICONTROL Pontuação de prioridade]** localizado nas propriedades da jornada ou campanha. Quanto maior o número, maior a prioridade.

Se você estava criando esta campanha e queria garantir que o conteúdo dela fosse exibido, atribuiria a ela uma pontuação de 100.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Se duas jornadas ou campanhas tiverem a mesma pontuação de prioridade, o sistema não terá um mecanismo de interrupção de vínculo. Certifique-se de que as pontuações de prioridade sejam exclusivas para evitar conflitos.

## Atribuir pontuações de prioridade às ações de canal de entrada {#priority-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à ação da jornada. A prioridade é essencial para priorizar uma ação de entrada quando há várias ações de jornada ou campanhas com a mesma configuração de canais.</br>Insira um valor numérico (de 0 a 100). Observe que, quanto maior o número, maior a prioridade. Por padrão, a pontuação de prioridade da ação é herdada da pontuação de prioridade geral da jornada."

O Journey Optimizer também permite atribuir uma pontuação de prioridade às ações do canal de entrada na atividade [Ação](../building-journeys/journey-action.md).

Isso permite priorizar uma ação de entrada quando há várias ações ou campanhas do jornada usando a mesma configuração de canal.

>[!NOTE]
>
>Na atividade **[!UICONTROL Ação]**, a pontuação de prioridade está disponível somente para os canais de entrada da Web, no aplicativo e baseados em código.

Na seção **[!UICONTROL Gerenciamento de conflitos]**, a opção **[!UICONTROL Usar prioridade de jornada]** é selecionada por padrão, o que significa que a pontuação de prioridade da ação é herdada da pontuação de prioridade geral da jornada.

Para atribuir uma pontuação de prioridade às ações de entrada definidas na atividade **[!UICONTROL Ação]**, desmarque a opção **[!UICONTROL Usar prioridade de jornada]** e insira um valor numérico (de 0 a 100) no campo **[!UICONTROL Prioridade]**. Quanto maior o número, maior a prioridade.

![](assets/action-journey-priority-score.png){width=70%}

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
