---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à configuração de  [!DNL Journey Optimizer]  canais
description: Saiba mais sobre a configuração de  [!DNL Journey Optimizer]  canais
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuração, configurar, mensagens, canal, sandbox, otimizador
source-git-commit: 21e2ea3e6a72d2a0eb0338df5665282d814501ac
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 48%

---


# Introdução à configuração de canais {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Controles de taxas dos canais"
>abstract="Controles de taxas dos canais"

Ao acessar o [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e aloca um determinado número de IPs dependendo do seu contrato.

Para enviar mensagens, você precisa seguir as etapas de configuração listadas abaixo:

1. Como um [administrador de sistema do Adobe Journey Optimizer](../start/path/administrator.md), defina as configurações específicas do seu canal. Saiba como definir essas configurações nas seguintes páginas:

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>Email</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>Notificação por push</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="Correspondência direta" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Correspondência direta</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="No aplicativo" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>No aplicativo</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="Experiência baseada em código" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>Experiência baseada em código</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="Cartões de conteúdo" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Cartões de conteúdo</strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >Para canais móveis, a [Configuração de canal guiada](set-mobile-config.md) facilita a configuração rápida de canais de marketing, garantindo que todos os recursos necessários estejam prontamente disponíveis no Experience Platform, no Journey Optimizer e na Coleção de dados. Isso permite que sua equipe de marketing comece a criar campanhas e jornadas.

1. Depois de concluído, você deve configurar todos os parâmetros técnicos necessários para entregar mensagens criando **configurações de canal**. [Saiba mais sobre as configurações de canal](channel-surfaces.md)

1. Dependendo dos canais que você está usando, seus ambientes e suas necessidades, também é necessário executar as seguintes etapas:

   * Configuração de subdomínio e delegação para seus canais, como [emails](about-subdomain-delegation.md), [SMS](../sms/sms-subdomains.md), [páginas de aterrissagem](../landing-pages/lp-subdomains.md) e [experiências da Web](../web/web-delegated-subdomains.md).

   * Configurar planos de aquecimento de IP para a capacidade de entrega ideal. [Saiba mais](ip-warmup-gs.md)

   * Defina uma lista de permissões para envio de email. [Saiba mais](allow-list.md)

   * Gerenciar o número de dias durante os quais são executadas tentativas antes do envio de endereços de email para a lista de supressão. [Saiba mais](manage-suppression-list.md)

   * Ativar a **Opção de email CCO** para manter uma cópia das mensagens enviadas a pessoas físicas. [Saiba mais](archiving-support.md#enable-bcc)

   * Configure as **regras de negócio** para evitar o excesso de solicitações de seus destinatários. [Saiba mais](../conflict-prioritization/rule-sets.md)

   * Determine qual endereço de email e/ou número de telefone deve ser usado com prioridade para seus destinatários quando vários endereços/números estiverem disponíveis na Adobe Experience Platform. [Saiba mais](primary-email-addresses.md)
