---
title: Configuração de cartões de conteúdo
description: Pré-requisitos do canal de cartões de conteúdo
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# Pré-requisitos dos cartões de conteúdo {#content-card-configuration-prereq}

Para que o Adobe Journey Optimizer exiba corretamente os cartões de conteúdo, você deve definir as seguintes configurações do Adobe Experience Platform:

* **Coleta de dados do Adobe Experience Platform**

  [Criar uma sequência de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure){target="_blank"} e [adicionar o serviço Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Habilite as opções de **[!UICONTROL Segmentação do Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. Isso garante que os eventos do Journey Optimizer sejam manipulados pelo Adobe Experience Platform Edge Network.
Adicione o grupo de campos **Evento de experiência - Interação de apresentação** ao conjunto de dados para incluir esses dados em seus relatórios. [Saiba mais sobre sequências de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Verifique se a política de mesclagem padrão tem a **Política de mesclagem ativa na Edge** habilitada no menu **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** > **[!UICONTROL Políticas de mesclagem]** do Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR#configure){target="_blank"}

  >[!NOTE]
  >
  >Ao usar uma política de mesclagem personalizada de **[!UICONTROL preferência de conjunto de dados]**, adicione o conjunto de dados de **[!UICONTROL Entrada de Jornada]** dentro da política de mesclagem especificada.

* **Adobe Experience Platform Mobile ou Platform Web SDK**

  Para aplicativos móveis e da Web, para adicionar modificações às suas páginas da Web ou aplicativos móveis, é necessário implementar a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/pt-br/docs/platform-learn/implement-web-sdk/overview){target="_blank"} no seu site ou a [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"} nos seus aplicativos móveis.

* **Journey Optimizer**

  Crie uma [Configuração do cartão de conteúdo](#content-card-configuration).

* **Solução de problemas**

  Use o modo de exibição **Edge Delivery** em **Adobe Experience Platform Assurance** para solucionar problemas de experiências móveis. Ele pode inspecionar solicitações, verificar chamadas de borda e examinar dados de perfil. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Experimentos de conteúdo**

  Verifique se o conjunto de dados usado na [sequência de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/overview#_blank){target="_blank"} do seu aplicativo também está incluído na sua configuração de relatório de experimento de conteúdo. Os dados do aplicativo não serão exibidos nos relatórios se os conjuntos de dados não corresponderem.

  Saiba como adicionar conjuntos de dados para relatórios de experimento de conteúdo [esta seção](../reports/reporting-configuration.md).

## Proteção de gerenciamento de perfil {#profile-management-guardrail}

[!DNL Journey Optimizer] cartões de conteúdo podem direcionar perfis com pseudônimos, ou seja, perfis que ainda não foram autenticados ou conhecidos por não terem sido engajados anteriormente em outros canais. Esse é o caso, por exemplo, ao direcionar todos os visitantes ou públicos com base em IDs temporárias, como ECID.

Isso aumenta a contagem total de perfis que podem ser ativados, o que pode ter implicações de custo se o número contratual de perfis que você adquiriu for excedido. As métricas de licença para cada pacote estão listadas na página [Descrição do Produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Você pode verificar o número de perfis ativáveis no [painel de uso de licença](../audience/license-usage.md).

Para manter seus perfis ativáveis dentro de limites razoáveis, a Adobe recomenda configurar um TTL (Time-To-Live) para excluir automaticamente perfis com pseudônimos do Perfil do cliente em tempo real se eles não tiverem sido vistos ou envolvidos em uma janela de tempo específica.

>[!NOTE]
>
>Saiba como configurar a expiração de dados para perfis com pseudônimo na [documentação do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

A Adobe recomenda definir o valor de TTL como 14 dias para corresponder ao TTL do perfil do Edge atual.