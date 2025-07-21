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
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---


# Definir o público da campanha de ação {#action-campaign-audience}

Use a guia **[!UICONTROL Público-alvo]** para definir o público da campanha.

![](assets/campaign-audience.png)

1. **Selecionar a audiência**

   Para campanhas de marketing, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais sobre públicos](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >O uso de públicos-alvo e atributos da [composição de público-alvo](../audience/get-started-audience-orchestration.md) não está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

1. **Selecione o tipo de identidade**

   No campo **[!UICONTROL Tipo de identidade]**, escolha o tipo de chave a ser usado para identificar os indivíduos do público-alvo selecionado. Você pode usar um tipo de identidade existente ou criar um novo usando o Serviço de identidade da Adobe Experience Platform. Os namespaces de Identidade Padrão estão listados em [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Somente um tipo de identidade é permitido por campanha. Indivíduos pertencentes a um segmento que não tem o tipo de identidade selecionado entre suas diferentes identidades não podem ser alvos da campanha. Saiba mais sobre tipos de identidade e namespaces na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

## Próximas etapas {#next}

Quando o público-alvo da sua campanha de ação estiver pronto, você poderá agendar a campanha. [Saiba mais](campaign-schedule.md)
