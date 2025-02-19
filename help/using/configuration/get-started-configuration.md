---
solution: Journey Optimizer
product: journey optimizer
title: 'Introdução à configuração do [!DNL Journey Optimizer]  '
description: 'Saiba mais sobre a configuração do [!DNL Journey Optimizer] '
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuração, configurar, mensagens, canal, sandbox, otimizador
source-git-commit: 40bef9a05fef1433773a73d546752e84f81b7366
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 93%

---


# Introdução à configuração do [!DNL Journey Optimizer] {#start-optimizer-configuration}

Ao acessar o [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e aloca um determinado número de IPs dependendo do seu contrato.

Para criar suas jornadas e enviar mensagens, você precisa seguir as etapas de configuração abaixo.

## Configurar mensagens e canais

1. Para criar e enviar mensagens, é necessário executar configurações específicas, dependendo do canal.

   * Para o canal **Email** , é necessário delegar subdomínios à Adobe e criar pools de IP para agrupar endereços IP. [Saiba mais](../email/get-started-email-config.md)

   * Para o canal **Push** é necessário definir as configurações de notificações por push na [!DNL Adobe Experience Platform] e no [!DNL Adobe Experience Platform Launch]. [Saiba mais](../push/push-configuration.md)

   * Para o canal **SMS** é necessário configurar sua instância para enviar SMS, incluindo a integração das configurações do provedor com [!DNL Journey Optimizer]. [Saiba mais](../sms/sms-configuration.md)

1. Depois de concluído, você deve criar **configurações de canal** para configurar todos os parâmetros técnicos necessários para entregar mensagens. [Saiba mais](channel-surfaces.md)

1. Você também pode:

   * Gerenciar o número de dias durante os quais são executadas tentativas antes do envio de endereços de email para a lista de supressão. [Saiba mais](manage-suppression-list.md)

   * Ativar a **Opção de email CCO** para manter uma cópia das mensagens enviadas a pessoas físicas. [Saiba mais](archiving-support.md#enable-bcc)

   * Configure as **regras de negócio** para evitar o excesso de solicitações de seus destinatários. [Saiba mais](../configuration/rule-sets.md)

   * Determine qual endereço de email e/ou número de telefone deve ser usado com prioridade para seus destinatários quando vários endereços/números estiverem disponíveis na Adobe Experience Platform. [Saiba mais](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Essas etapas devem ser executadas por um [administrador do sistema do Adobe Journey Optimizer](../start/path/administrator.md).

## Configurar jornadas

Para construir jornadas, é necessário configurar as **[!UICONTROL Fontes de dados]**, **[!UICONTROL Eventos]** e **[!UICONTROL Ações]**. [Saiba mais](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* A configuração da **fonte de dados** permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../datasource/about-data-sources.md)

* Os **Eventos** permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, à pessoa física que flui para a jornada. Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de streaming para eventos autenticados e não autenticados (como eventos do SDK móvel da Adobe). [Saiba mais](../event/about-events.md)

* O [!DNL Journey Optimizer] vem com recursos de mensagem incorporados que permitem projetar e enviar seu conteúdo. Se você estiver usando um sistema de terceiros para enviar mensagens, crie uma **ação personalizada**. [Saiba mais](../action/action.md)