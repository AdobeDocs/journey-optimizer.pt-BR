---
solution: Journey Optimizer
product: journey optimizer
title: Definir o público da campanha de ação
description: Saiba como definir o público-alvo da campanha de ação.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: criar, otimizador, campanha, superfície, mensagens
exl-id: 5635ef04-c69d-4397-9762-7a6f1265d453
TQID: https://experienceleague.adobe.com/3lWwW0Lru2D5D83QqHl48Gsxv7JVKjX8ZBmZAiMFiB0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 6%

---

# Definir o público da campanha de ação {#action-campaign-audience}

Use a guia **[!UICONTROL Público-alvo]** para definir o público da campanha.

![](assets/campaign-audience.png)

1. **Selecionar o público-alvo**

   Para campanhas de marketing, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais sobre públicos](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >O uso de públicos-alvo e atributos da [composição de público-alvo](../audience/get-started-audience-orchestration.md) não está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

1. **Selecione o tipo de identidade**

   No campo **[!UICONTROL Tipo de identidade]**, escolha o tipo de chave a ser usado para identificar os indivíduos do público-alvo selecionado. Você pode usar um tipo de identidade existente ou criar um novo usando o Serviço de identidade da Adobe Experience Platform. Os namespaces de Identidade Padrão estão listados em [esta página](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Somente um tipo de identidade é permitido por campanha. Indivíduos pertencentes a um segmento que não tem o tipo de identidade selecionado entre suas diferentes identidades não podem ser alvos da campanha. Saiba mais sobre tipos de identidade e namespaces na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

## Próximas etapas {#next}

Quando o público-alvo da sua campanha de ação estiver pronto, você poderá agendar a campanha. [Saiba mais](campaign-schedule.md)
