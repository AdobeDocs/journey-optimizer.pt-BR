---
title: Métodos de classificação
description: Saiba como trabalhar com métodos de classificação
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1qUj05fLaRqqJGfaoL-y5uwtknp7HDkWKocHMde-8lc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 16%

---

# Métodos de classificação {#rankings}

Os métodos de classificação permitem classificar itens para exibição em um determinado perfil. Depois que um método de classificação é criado, será possível atribuí-lo a uma estratégia de seleção para definir quais itens devem ser selecionados primeiro.

Dois tipos de métodos de classificação estão disponíveis:

* **As fórmulas** permitem definir regras que determinarão qual item deve ser apresentado primeiro, em vez de considerar as pontuações de prioridade do item.

* Os **modelos de IA** permitem usar sistemas de modelo treinados que aproveitarão vários pontos de dados para determinar qual item deve ser apresentado primeiro.

## Criar métodos de classificação {#create}

Para criar um método de classificação, siga estas etapas:

1. Navegue até o menu **[!UICONTROL Configuração de estratégia]** e selecione o menu **[!UICONTROL Fórmulas]** ou **[!UICONTROL Modelos de IA]**, dependendo do tipo de classificação que deseja usar.

   ![](../assets/ranking-create.png)

1. Clique no botão **[!UICONTROL Criar fórmula]** ou **[!UICONTROL Criar modelo de IA]** no canto superior direito da tela.

   Informações detalhadas sobre como criar fórmulas de classificação e modelos de IA estão disponíveis nas seguintes seções:

   * [Fórmulas de classificação](ranking-formulas.md)
   * [Modelos de IA](ai-models.md)

1. Configure a fórmula ou o modelo de IA para atender às suas necessidades e, em seguida, salve.

Seu método de classificação agora está pronto para ser usado em uma [estratégia de seleção](../selection-strategies.md) para classificar itens de decisão qualificados.


