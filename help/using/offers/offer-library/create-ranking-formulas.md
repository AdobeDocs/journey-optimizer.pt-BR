---
title: Criar fórmulas de classificação
description: Saiba como criar fórmulas de classificação no Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# Criar fórmulas de classificação {#create-ranking-formulas}

## Sobre fórmulas de classificação {#about-ranking-formulas}

**As** fórmulas de classificação permitem definir regras que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas.

As fórmulas de classificação são expressas em **Sintaxe PQL** e podem aproveitar atributos de perfil, dados de contexto e atributos de oferta. Para obter mais informações sobre como usar a sintaxe PQL, consulte a [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Depois que uma fórmula de classificação é criada, é possível atribuí-la a uma disposição em uma decisão (anteriormente conhecida como atividade de oferta). Para obter mais informações, consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md).

## Criar uma fórmula de classificação {#create-ranking-formula}

Para criar uma fórmula de classificação, siga as etapas abaixo:

* Acesse o menu **[!UICONTROL Components]** e selecione a guia **[!UICONTROL Rankings]**.

* Clique em **[!UICONTROL Create formula]** para criar uma nova fórmula de classificação.

   ![](../../assets/ranking-create-formula.png)

* Especifique o nome da fórmula de classificação, a descrição e a fórmula.

   Neste exemplo, queremos aumentar a prioridade de todas as ofertas com o atributo &quot;quente&quot; se o tempo real estiver quente. Para fazer isso, o **contextData.weather=hot** foi transmitido na chamada de decisão.

   ![](../../assets/ranking-syntax.png)

* Clique em **[!UICONTROL Save]**. Sua fórmula de classificação é criada, você pode selecioná-la na lista para obter detalhes e editá-la ou excluí-la.

   Agora ele está pronto para ser usado em uma decisão para classificar ofertas elegíveis para uma disposição (consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
