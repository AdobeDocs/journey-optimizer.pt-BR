---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar personalização em campanhas orquestradas
description: Saiba como personalizar mensagens do Orchestrated campaign usando atributos de perfil, atributos de público-alvo da tabela de trabalho e matrizes de coleção de enriquecimento.
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# Adicionar personalização em campanhas orquestradas {#add-personalization}

Depois de [orquestrar atividades](orchestrate-activities.md) na tela e adicionar uma atividade de canal, você personaliza o conteúdo da mensagem no email, SMS ou outro editor de canal.

O Personalization em campanhas orquestradas funciona de forma semelhante a outras [!DNL Journey Optimizer] campanhas ou jornadas, com diferenças vinculadas à **tabela de trabalho**: atributos calculados por atividades de direcionamento e enriquecimento na tela, não apenas dados do armazenamento de perfil.

## Acessar o editor de personalização {#access}

1. Abra a campanha Orquestrada e adicione uma atividade de canal. [Saiba como adicionar uma atividade de canal](activities/channels.md#add)

1. Configure a atividade do canal, abra a guia **[!UICONTROL Conteúdo]** e edite a mensagem.

1. No editor de mensagens, use o editor de personalização para inserir atributos no conteúdo.

Para visualizar e testar o conteúdo personalizado da atividade do canal, consulte [Verificar e testar seu conteúdo](activities/channels.md#simulate-content-test-profiles).

## Atributos de perfil e de destino {#attributes}

Quando você abre o editor de personalização, duas pastas principais contêm atributos disponíveis para personalização:

* **[!UICONTROL Atributos do perfil]**

  Dados relacionados ao perfil de [!DNL Adobe Experience Platform]: nome, endereço de email, local e outras características capturadas no perfil do usuário.

* **[!UICONTROL Atributos do público-alvo]** (somente campanhas orquestradas)

  Atributos calculados na tela da campanha da tabela de trabalho. Esta pasta tem duas subpastas:

   * **`<Targeting dimension>`** (por exemplo, Destinatários ou Compras) — Atributos relacionados à dimensão que você direciona na campanha.

   * **`Enrichment`** — Dados adicionados através de atividades de **[!UICONTROL Enriquecimento]** (links relacionais, linhas coletadas, agregações). Após um enriquecimento de 1:N **[!UICONTROL Coletar dados]**, você obtém as linhas numeradas e uma matriz de coleção. [Saiba como trabalhar com dados de coleção de enriquecimento](#enrichment-collections)

Para obter uma visão geral detalhada do editor de personalização no [!DNL Journey Optimizer], consulte [Introdução à personalização](../personalization/personalize.md).

## Trabalhar com dados de coleção de enriquecimento {#enrichment-collections}

Quando você configura uma atividade **[!UICONTROL Enriquecimento]** com um link 1:N e **[!UICONTROL Coletar dados]**, os atributos de enriquecimento estão disponíveis em **[!UICONTROL Atributos de destino] > [!UICONTROL Enriquecimento]** de duas formas:

* **Linhas niveladas** — Um campo por linha recuperada (por exemplo, **Compra 1**, **Compra 2**, **Compra 3**), cada uma com os atributos selecionados no link (como preço ou produto). Use-os quando precisar de slots separados e fixos, como por exemplo `target.enrichment.purchase1.price`.

* **Matriz da coleção** — Uma matriz para todas as linhas coletadas, chamada a partir do rótulo do link (por exemplo, **compras**). Use isso quando precisar trabalhar no conjunto completo de registros, com [funções de matriz](#array-functions).

![](assets/enrichment-target-attributes-picker.png)

Para identificar as linhas planas da matriz da coleção, insira o atributo no editor de expressão e leia o caminho gerado. A matriz da coleção é a entrada cujo caminho é **plural** (por exemplo `purchases`) e não tem **nenhum número de linha** (`purchase1`, `purchase2` e assim por diante).

| O que você precisa | Caminho no editor de expressão |
| --- | --- |
| **Uma linha coletada** | **Numerado** — por exemplo `target.enrichment.purchase1.price` |
| **A coleção completa** | **Plural e sem número** — por exemplo `target.enrichment.purchases.price` |

Você pode aplicar as mesmas [funções de matriz e lista](../personalization/functions/arrays-list.md) usadas em outro lugar em [!DNL Journey Optimizer] a uma coleção de enriquecimento, fazendo referência a `target.enrichment.<label>`.

Por exemplo, em uma linha de assunto, você pode mostrar quantas compras coletadas existem e o preço do primeiro item:

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [Saiba como configurar o enriquecimento da coleção na tela](activities/enrichment.md#collection-personalization)
