---
title: Introdução a [!DNL Journey Optimizer] configuração
description: Saiba mais sobre [!DNL Journey Optimizer] configuração
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 9%

---


# Introdução a [!DNL Journey Optimizer] configuração {#start-optimizer-configuration}

Ao acessar [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e recebe um determinado número de IPs dependendo do seu contrato.

Para criar suas jornadas e enviar mensagens, você precisa seguir estas etapas de configuração:

1. **Configurar mensagens e canais**: definir predefinições, adaptar e personalizar mensagens de email e de push

   * Defina as configurações de notificações por push em [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Saiba mais](../messages/push-gs.md)

   * Crie predefinições de mensagens para configurar todos os parâmetros técnicos necessários para mensagens de email e de notificação por push. [Saiba mais](message-presets.md)

   * Determine qual endereço de email deve ser usado com prioridade para seus recipients quando vários endereços estiverem disponíveis no Adobe Experience Platform. [Saiba mais](primary-email-addresses.md)

   * Gerencie o número de dias durante os quais as tentativas são executadas antes de enviar endereços de email para a lista de supressão. [Saiba mais](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../messages/push-gs.md)
    -->

1. **Delegar subdomínios**: para qualquer novo subdomínio ser usado no Journey Optimizer, a primeira etapa será delegá-lo. [Saiba mais](about-subdomain-delegation.md)

   ![](assets/subdomain.png)

1. **Criar pools de IP**: melhore a capacidade de delivery de email e a reputação, agrupando os endereços IP provisionados com sua instância. [Saiba mais](ip-pools.md)

   ![](assets/ip-pool.png)

1. **Configurar jornadas**: para criar o jornada, é necessário configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**. [Saiba mais](about-data-sources-events-actions.md)

   ![](assets/admin-menu.png)

   * O **Fonte de dados** A configuração do permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. Saiba mais sobre Fontes de dados neste [seção](../datasource/about-data-sources.md)

   * **Eventos** permite acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada. Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de streaming para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). Saiba mais sobre eventos neste [seção](../event/about-events.md)

   * [!DNL Journey Optimizer] O vem com recursos de mensagem incorporados: você pode criar o conteúdo e publicar a mensagem. Se você estiver usando um sistema de terceiros para enviar mensagens, crie um **ação personalizada**. Saiba mais sobre ações neste [seção](../action/action.md)