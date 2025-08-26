---
title: Configuração de cartões de conteúdo
description: Pré-requisitos do canal de cartões de conteúdo
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# Pré-requisitos dos cartões de conteúdo {#content-card-configuration-prereq}

Para que o Adobe Journey Optimizer exiba corretamente os cartões de conteúdo, você deve definir as seguintes configurações do Adobe Experience Platform:

* **Coleta de dados do Adobe Experience Platform**

  [Criar uma sequência de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure) e [adicionar o serviço Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure#aep). Habilite as opções de **[!UICONTROL Segmentação do Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. Isso garante que os eventos do Journey Optimizer sejam manipulados pelo Adobe Experience Platform Edge Network.
Adicione o grupo de campos **Evento de experiência - Interação de apresentação** ao conjunto de dados para incluir esses dados em seus relatórios. [Saiba mais sobre sequências de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure)

* **Adobe Experience Platform**

  Verifique se a política de mesclagem padrão tem a **Política de mesclagem ativa na Edge** habilitada no menu **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Políticas de mesclagem]** do Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR#configure){target="_blank"}

  >[!NOTE]
  >
  >Ao usar uma política de mesclagem personalizada de **[!UICONTROL preferência de conjunto de dados]**, adicione o conjunto de dados de **[!UICONTROL Entrada de Jornada]** dentro da política de mesclagem especificada.

* **Adobe Experience Platform Mobile ou Platform Web SDK**

  Para aplicativos móveis e da Web, para adicionar modificações às suas páginas da Web ou aplicativos móveis, é necessário implementar a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/pt-br/docs/platform-learn/implement-web-sdk/overview) no seu site ou a [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) nos seus aplicativos móveis.

* **Journey Optimizer**

  Crie uma [Configuração do cartão de conteúdo](#content-card-configuration).

* **Solução de problemas**

  Use o modo de exibição **Edge Delivery** em **Adobe Experience Platform Assurance** para solucionar problemas de experiências móveis. Ele pode inspecionar solicitações, verificar chamadas de borda e examinar dados de perfil. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery)

* **Experimentos de conteúdo**

  Verifique se o conjunto de dados usado na [sequência de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/overview#_blank) do seu aplicativo também está incluído na sua configuração de relatório de experimento de conteúdo. Os dados do aplicativo não serão exibidos nos relatórios se os conjuntos de dados não corresponderem.

  Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo [esta seção](../reports/reporting-configuration.md).
