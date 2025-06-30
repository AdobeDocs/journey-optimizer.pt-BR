---
title: Métodos de classificação
description: Saiba como trabalhar com métodos de classificação
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '204'
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


