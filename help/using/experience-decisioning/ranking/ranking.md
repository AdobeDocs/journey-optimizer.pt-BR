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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
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


