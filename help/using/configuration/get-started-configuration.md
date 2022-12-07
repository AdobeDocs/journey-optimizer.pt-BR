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
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# Introdução a [!DNL Journey Optimizer] configuração {#start-optimizer-configuration}

Ao acessar [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e aloca um determinado número de IPs dependendo do seu contrato.

Para criar suas jornadas e enviar mensagens, você precisa seguir as etapas de configuração abaixo.

## Configurar mensagens e canais

Defina as superfícies do canal, adapte e personalize as mensagens.

* [Delegar para Adobe dos subdomínios](about-subdomain-delegation.md) deseja usar para enviar emails e [criar pools de IP](ip-pools.md) para agrupar endereços IP provisionados com sua instância.

* Gerencie o número de dias durante os quais são executadas tentativas antes do envio de endereços de email para a lista de supressão. [Saiba mais](manage-suppression-list.md)

* Definir configurações de notificações por push em ambos [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Saiba mais](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Configure sua instância para enviar SMS (atualmente disponível apenas para um conjunto de organizações - Disponibilidade limitada). [Saiba mais](../sms/sms-configuration.md)

* Crie superfícies de canal para configurar todos os parâmetros técnicos necessários para enviar mensagens. [Saiba mais](channel-surfaces.md)

* Determine qual endereço de email e/ou número de telefone deve ser usado com prioridade para seus recipients quando vários endereços/números estiverem disponíveis no Adobe Experience Platform. [Saiba mais](primary-email-addresses.md)

## Configurar jornadas

Para criar jornadas, é necessário configurar **[!UICONTROL Fontes de dados]**, **[!UICONTROL Eventos]** e **[!UICONTROL Ações]**. [Saiba mais](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* O **fonte de dados** A configuração do permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../datasource/about-data-sources.md)

* Os **Eventos** permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada. Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de streaming para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). [Saiba mais](../event/about-events.md)

* [!DNL Journey Optimizer] O vem com recursos de mensagem integrados que permitem projetar e enviar o conteúdo. Se você estiver usando um sistema de terceiros para enviar mensagens, crie um **ação personalizada**. [Saiba mais](../action/action.md)