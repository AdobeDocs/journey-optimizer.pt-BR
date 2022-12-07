---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à configuração de email
description: Saiba mais sobre a configuração de email no [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 16%

---


# Introdução à configuração de email {#get-starte-email-config}

Para enviar emails por meio de jornadas e campanhas no [!DNL Journey Optimizer], é necessário executar várias etapas de configuração.

1. Para garantir o deliverability ideal e proteger sua reputação, comece delegando ao Adobe os subdomínios que você usará para enviar seus emails com a [!DNL Journey Optimizer]. Esses subdomínios determinarão elementos, como as páginas da Web a serem rastreadas e os URLs da mirror page. [Saiba mais](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Melhore a capacidade de delivery de email e a reputação ao agrupar os endereços IP provisionados com sua instância. [Saiba mais](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Crie as superfícies do canal e selecione o **[!UICONTROL Email]** canal. [Saiba mais](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Em cada superfície de canal de email, configure todos os parâmetros técnicos necessários para enviar emails. [Saiba mais](email-settings.md)

   * É aqui que você seleciona o subdomínio a ser usado para enviar os emails e os pools de IP para associar à superfície. [Saiba mais](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * O **[!UICONTROL Email do remetente]** e **[!UICONTROL Email de erro]** os endereços devem usar o subdomínio delegado selecionado atual. [Saiba mais](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Determine qual endereço de email deve ser usado com prioridade para seus recipients quando vários endereços estiverem disponíveis no Adobe Experience Platform. [Saiba mais](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gerencie o número de dias durante os quais são executadas tentativas antes do envio de endereços de email para a lista de supressão. [Saiba mais](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
