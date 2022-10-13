---
title: Criar uma mensagem de SMS.
description: Saiba como criar uma mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 32c69ef268c78ba834612d16b2ac1c721fb5df56
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 7%

---

# Criar uma mensagem de SMS. {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Criação de SMS"
>abstract="Adicione a mensagem de texto e comece a personalizá-la com o editor de expressão."

Use [!DNL Journey Optimizer] para enviar mensagens de texto aos clientes em seus dispositivos móveis. Você pode criar, personalizar e visualizar mensagens em formato de texto no editor de SMS.

>[!NOTE]
>
>De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a assinatura. Para fazer isso, os recipients do SMS podem responder com palavras-chave de aceitação e recusa. [Saiba como gerenciar a recusa](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

Deliveries de SMS podem ser criados:

* Em um **Jornada**: Depois de adicionar uma atividade de SMS na jornada e definir as configurações básicas, use a **[!UICONTROL Ações: SMS]** painel direito para criar o conteúdo da mensagem SMS.

   Para obter mais informações sobre como configurar a jornada, consulte esta seção [página](../building-journeys/journey-gs.md).

* Em um **Campanha**: Depois de criar uma campanha, selecione SMS como ação e defina configurações básicas.

   Para obter mais informações sobre como configurar sua campanha, consulte esta seção [página](../campaigns/create-campaign.md#configure).

Se esta for a primeira vez que você cria uma mensagem SMS, verifique se o canal SMS foi configurado. [Saiba mais](../configuration/sms-configuration.md).

## Definir o conteúdo do SMS{#sms-content}

Para começar a personalizar a mensagem SMS, siga estas etapas:

1. Clique no botão **[!UICONTROL Mensagem]** para abrir o editor de expressão.

   ![](assets/sms-content.png)

1. Use o editor de expressão para definir o conteúdo e adicionar conteúdo dinâmico. Você pode usar qualquer atributo, como o nome do perfil ou a cidade. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no Editor de expressão.

1. Clique em **[!UICONTROL Salvar]** e verifique a mensagem na visualização.

   ![](assets/sms-content-preview.png)

## Validar o SMS{#sms-preview}

>[!NOTE]
>
> Para melhorar o deliverability, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, Twilio e Sinch suportam apenas números de telefone no formato E.164.

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu [conteúdo personalizado](../personalization/personalize.md), é possível verificar como esse conteúdo é exibido na mensagem, aproveitando os dados do perfil de teste.

Para visualizar como sua mensagem SMS é exibida em dispositivos móveis, clique no botão **[!UICONTROL Simular conteúdo]** guia . Saiba mais sobre a simulação de conteúdo em [esta seção](../design/preview.md).

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. Saiba mais [nesta seção](alerts.md).

![](assets/sms-alert-button.png)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Tópicos relacionados**

* [Configurar canal de SMS](../configuration/sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma nova mensagem](get-started-content.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
