---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a [!DNL Journey Optimizer] configuração
description: Saiba mais sobre [!DNL Journey Optimizer] configuração
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# Introdução a [!DNL Journey Optimizer] configuração {#start-optimizer-configuration}

Ao acessar [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e recebe um determinado número de IPs dependendo do seu contrato.

Para criar suas jornadas e enviar mensagens, você precisa seguir as etapas de configuração abaixo.

## Configurar mensagens e canais

1. Para criar e enviar mensagens, é necessário executar configurações específicas, dependendo do canal.

   * Para o **Email** , é necessário delegar subdomínios à Adobe e criar pools de IP para agrupar endereços IP. [Saiba mais](../email/get-started-email-config.md)

   * Para o **Empurrar** , é necessário definir as configurações de notificações por push em ambas as [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Saiba mais](../push/push-configuration.md)

   * Para o **SMS** , é necessário configurar sua instância para enviar SMS, incluindo a integração das configurações do provedor com o [!DNL Journey Optimizer]. [Saiba mais](../sms/sms-configuration.md)

1. Depois de concluído, você deve criar **superfícies dos canais** para configurar todos os parâmetros técnicos necessários para enviar mensagens. [Saiba mais](channel-surfaces.md)

1. Você também pode:

   * Gerencie o número de dias durante os quais as tentativas são executadas antes de enviar endereços de email para a lista de supressão. [Saiba mais](manage-suppression-list.md)

   * Ative o **Opção de email BBC** para manter uma cópia das mensagens enviadas aos indivíduos. [Saiba mais](archiving-support.md#enable-bcc)

   * Configurar **regras de frequência** para evitar o excesso de solicitações dos recipients. [Saiba mais](frequency-rules.md)

   * Determine qual endereço de email e/ou número de telefone deve ser usado com prioridade para seus recipients quando vários endereços/números estiverem disponíveis na Adobe Experience Platform. [Saiba mais](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Essas etapas devem ser executadas por um [Administrador de sistema do Adobe Journey Otimizer](../start/path/administrator.md).

## Configurar jornadas

Para criar jornadas, é necessário configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**. [Saiba mais](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* O **fonte de dados** A configuração do permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../datasource/about-data-sources.md)

* **Eventos** permitem acionar suas jornadas de forma unitária para enviar mensagens, em tempo real, para o indivíduo que flui para a jornada. Na configuração do evento, você configura os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de fluxo para eventos autenticados e não autenticados (como eventos do SDK do Adobe Mobile). [Saiba mais](../event/about-events.md)

* [!DNL Journey Optimizer] O vem com recursos de mensagem integrados que permitem projetar e enviar o conteúdo. Se você estiver usando um sistema de terceiros para enviar mensagens, crie um **ação personalizada**. [Saiba mais](../action/action.md)