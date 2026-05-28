---
solution: Journey Optimizer
product: journey optimizer
title: Usar variáveis em campanhas orquestradas
description: Saiba como usar variáveis de evento em campanhas orquestradas para criar condições e regras de direcionamento.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
feature_v2:
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 1%

---


# Usar variáveis em campanhas orquestradas {#variables-oc}

## Como definir variáveis {#set}

Em uma campanha Orquestrada, você pode trabalhar com variáveis, ou seja, valores que direcionam o direcionamento, condições de **[!UICONTROL Teste]** e outra lógica de tela. Esses valores podem vir de dois lugares:

* **Um sinal** — Se o agendamento da campanha for **[!UICONTROL Acionado por um sinal]**, você poderá passar parâmetros ao acionar a campanha. Esses parâmetros se tornam disponíveis como variáveis na campanha Orquestrada acionada para essa execução. [Saiba como acionar uma campanha Orquestrada usando um sinal](trigger-orchestrated-campaign.md)

* **Variáveis globais** — Você pode definir pares de nomes/valores diretamente na campanha usando o menu **[!UICONTROL Editar variáveis]**, sem a necessidade de API ou sinal. [Saiba como definir variáveis globais em campanhas orquestradas](global-variables.md)

>[!NOTE]
>
>Por enquanto, as variáveis suportam somente valores de **texto**.
>
>As variáveis direcionam a **lógica da tela** (regras, condições) e não podem ser usadas para personalização de mensagens.

## Usar variáveis na tela {#use}

As variáveis estão disponíveis nos seguintes locais na tela:

* **Construtor de regras** — Abra o editor de expressões para uma regra e use o seletor de **variáveis de eventos** para selecionar uma variável e inserir sua referência na expressão. [Saiba como editar expressões](edit-expressions.md)

  No exemplo abaixo, uma variável chamada `brand` foi passada e a regra a usa como uma condição de filtro.

  ![Construtor de regras usando uma variável de marca das variáveis de evento](assets/variables-rule.png){zoomable="yes"}

* Atividade **[!UICONTROL Test]** — Quando você define uma condição, o menu suspenso **[!UICONTROL Tipo de condição]** lista todas as variáveis no escopo junto com **[!UICONTROL Contagem de população]**. Selecione uma variável para usá-la como a base para uma ramificação de teste. [Saiba como configurar a atividade **[!UICONTROL Testar]**](activities/test.md)

  No exemplo abaixo, a variável `channel` é usada para rotear o fluxo para transições diferentes dependendo de seu valor.

  ![Lista suspensa de tipo de condição de atividade de teste listando a variável de canal](assets/variables-test.png){zoomable="yes"}
