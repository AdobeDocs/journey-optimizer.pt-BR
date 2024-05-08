---
title: Métodos de classificação
description: Saiba como trabalhar com métodos de classificação
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidade limitada"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 12%

---

# Métodos de classificação {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Criar fórmulas de classificação"
>abstract="As fórmulas permitem definir regras que determinam qual item deve ser apresentado primeiro, ao invés de considerar a pontuação de prioridade do item. Depois que um método de classificação é criado, é possível atribuí-lo a uma estratégia de seleção para definir quais itens devem ser selecionados primeiro."

Os métodos de classificação permitem classificar itens para exibição em um determinado perfil. Depois que um método de classificação é criado, é possível atribuí-lo a uma estratégia de seleção para definir quais itens devem ser selecionados primeiro.

Dois tipos de métodos de classificação estão disponíveis:

* **Fórmulas** O permite definir regras que determinarão qual item deve ser apresentado primeiro, em vez de considerar as pontuações de prioridade do item.

* **Modelos de IA** O permite usar sistemas de modelo treinados que aproveitarão vários pontos de dados para determinar qual item deve ser apresentado primeiro.

## Criar métodos de classificação {#create}

Para criar um método de classificação, siga estas etapas:

1. Navegue até a **[!UICONTROL Configuração da estratégia]** e selecione o **[!UICONTROL Fórmulas]** ou **[!UICONTROL Modelos de IA]** dependendo do tipo de classificação que deseja usar.

1. Clique em **[!UICONTROL Criar fórmula]** ou **[!UICONTROL Criar modelo de IA]** no canto superior direito da tela.

   ![](assets/ranking-create.png)

1. Configure a fórmula ou o modelo de IA para atender às suas necessidades e salve.

   Informações detalhadas sobre como criar fórmulas de classificação e modelos de IA estão disponíveis na documentação da gestão de decisões:

   * [Fórmulas de classificação](../offers/ranking/create-ranking-formulas.md)
   * [Modelos de IA](../offers/ranking/ai-models.md)


## Aproveitar atributos de itens de decisão em fórmulas {#items}

As fórmulas de classificação são expressas em **Sintaxe PQL** e podem aproveitar vários atributos, como atributos de perfil, [dados de contexto](context-data.md) e atributos relacionados aos seus itens de decisão.

Para aproveitar os atributos relacionados aos seus itens de decisão em fórmulas, siga a sintaxe abaixo no código da fórmula de classificação. Expanda cada seção para obter mais informações:

+++Aproveitar atributos padrão de itens de decisão

![](assets/formula-attribute.png)

+++

+++Aproveitar atributos personalizados de itens de decisão

![](assets/formula-attribute-custom.png)

+++
