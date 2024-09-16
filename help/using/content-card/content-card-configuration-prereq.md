---
title: Configuração de cartões de conteúdo
description: Pré-requisitos do canal de cartões de conteúdo
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidade limitada" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 7%

---

# Pré-requisitos dos cartões de conteúdo {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**Índice**

* [Introdução a cartões de conteúdo](get-started-content-card.md)
* **Pré-requisitos de cartões de conteúdo**
* [Configurar canal de cartões de conteúdo no Journey Optimizer](content-card-configuration.md)
* [Criar cartões de conteúdo](create-content-card.md)
* [Criar cartões de conteúdo](design-content-card.md)
* [Relatório de cartões de conteúdo](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Atualmente, os cartões de conteúdo estão disponíveis apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.

Para que o Adobe Journey Optimizer exiba corretamente os cartões de conteúdo, você deve definir as seguintes configurações do Adobe Experience Platform:

* **Coleta de dados do Adobe Experience Platform**

  [Criar uma sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) e [adicionar o serviço Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep). Habilite as opções de **[!UICONTROL Segmentação do Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. Isso garante que os eventos do Journey Optimizer sejam manipulados pelo Edge Network Adobe Experience Platform. Consulte a [documentação de sequências de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) para obter mais informações sobre como configurar uma sequência de dados.

* **Adobe Experience Platform**

  Verifique se a política de mesclagem padrão tem a **Política de mesclagem ativa na Edge** habilitada no menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Políticas de mesclagem]**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >Ao usar uma política de mesclagem personalizada de **[!UICONTROL preferência de conjunto de dados]**, adicione o conjunto de dados de **[!UICONTROL Entrada de Jornada]** dentro da política de mesclagem especificada.

* **Adobe Experience Platform Mobile ou Platform Web SDK**

  Para aplicativos móveis e da Web, para adicionar modificações às suas páginas da Web ou aplicativos móveis, é necessário implementar o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/pt-br/docs/platform-learn/implement-web-sdk/overview) no seu site ou o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) nos seus aplicativos móveis.

* **Journey Optimizer**

  Crie uma [Configuração do cartão de conteúdo](#content-card-configuration).

* **Solução de problemas**

  Use a exibição **Edge Delivery** dentro do **Adobe Experience Platform Assurance** para solucionar problemas de experiências móveis. Ele pode inspecionar solicitações, verificar chamadas de borda e examinar dados de perfil. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery)

* **Experimentos de conteúdo**

  Verifique se o conjunto de dados usado na [sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank) do seu aplicativo também está incluído na sua configuração de relatório de experimento de conteúdo. Os dados do aplicativo não serão exibidos nos relatórios se os conjuntos de dados não corresponderem.

  Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo [esta seção](../content-management/reporting-configuration.md).
