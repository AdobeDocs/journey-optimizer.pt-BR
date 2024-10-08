---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à configuração de email
description: Saiba mais sobre a configuração de email no [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: email, configuração, superfície, subdomínios
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 100%

---

# Introdução à configuração de email {#get-starte-email-config}

Para poder enviar emails por meio de jornadas e campanhas no [!DNL Journey Optimizer] é necessário executar várias etapas de configuração.

1. Para garantir a entrega ideal e proteger sua reputação, comece delegando à Adobe os subdomínios que você usará para enviar seus emails com [!DNL Journey Optimizer]. Esses subdomínios determinarão elementos como as páginas da Web a serem rastreadas e os URLs da mirror page. [Saiba mais](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Melhore a capacidade de entrega de email e a reputação, agrupando os endereços IP provisionados com sua instância. [Saiba mais](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Defina as configurações de canal e selecione o canal **[!UICONTROL Email]**. [Saiba mais](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Em cada configuração de canal de email, configure todos os parâmetros técnicos necessários para entregar os emails. [Saiba mais](email-settings.md)

   * É aqui que você seleciona o subdomínio a ser usado para enviar os emails e os pools de IP para associar à configuração. [Saiba mais](email-settings.md#subdomains-and-ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Os endereços do **[!UICONTROL Email do remetente]** e do **[!UICONTROL Email de erro]** devem usar o subdomínio delegado selecionado atual. [Saiba mais](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Determine qual endereço de email deve ser usado com prioridade para seus destinatários quando vários endereços estiverem disponíveis na Adobe Experience Platform. [Saiba mais](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gerenciar o número de dias durante os quais são executadas tentativas antes do envio de endereços de email para a lista de supressão. [Saiba mais](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
