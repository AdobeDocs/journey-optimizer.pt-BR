---
solution: Journey Optimizer
product: journey optimizer
title: Visualizar sua mensagem SMS
description: Saiba como visualizar e testar sua mensagem SMS no Journey Otimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Enviar sua mensagem SMS {#send-sms}

## Visualizar sua mensagem SMS {#preview-sms}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, aproveitando os dados do perfil de teste.

1. Clique em **[!UICONTROL Simulate content]**.

1. Clique em **[!UICONTROL Manage test profiles]** para adicionar um perfil de teste.

1. Encontre seu perfil de teste com a **[!UICONTROL Identity namespace]** e **[!UICONTROL Identity value]** campos. Em seguida, clique em **[!UICONTROL Add profile]**.

   ![](assets/sms_preview_3.png)

1. Depois de selecionar seu perfil de teste, você pode fechar o **[!UICONTROL Add test profile]** janela.

   ![](assets/sms_preview_1.png)

1. Na janela Preview &amp; test , os dados do perfil de teste são aproveitados no conteúdo da mensagem.

   Por exemplo, para essa mensagem SMS, o conteúdo da mensagem é personalizado:

   ![](assets/sms_preview_2.png)

## Validar o SMS{#sms-preview}

>[!NOTE]
>
> Para melhorar o deliverability, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, Twilio e Sinch suportam apenas números de telefone no formato E.164.

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. Dois tipos de alertas podem acontecer:

* **Avisos** consulte recomendações e práticas recomendadas. Por exemplo, uma mensagem será exibida se a mensagem SMS estiver vazia.

* **Erros** impedir que você teste ou ative a jornada, desde que elas não sejam resolvidas. Por exemplo, uma mensagem avisará que a linha de assunto está ausente.

![](assets/sms-alert-button.png)

Quando a mensagem SMS estiver pronta, conclua a configuração de seu [jornada](../building-journeys/journey-gs.md) ou [campanha](../campaigns/create-campaign.md) para enviá-lo.

**Tópicos relacionados**

* [Configurar canal SMS](sms-configuration.md)
* [Relatório SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma mensagem SMS](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
