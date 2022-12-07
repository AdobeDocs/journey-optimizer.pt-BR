---
solution: Journey Optimizer
product: journey optimizer
title: Visualizar sua mensagem SMS
description: Saiba como visualizar e testar sua mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# Enviar sua mensagem SMS {#send-sms}

## Visualizar sua mensagem SMS {#preview-sms}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, aproveitando os dados do perfil de teste.

1. Clique em **[!UICONTROL Simular conteúdo]**.

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para adicionar um perfil de teste.

1. Encontre seu perfil de teste com a **[!UICONTROL Namespace de identidade]** e **[!UICONTROL Valor de identidade]** campos. Em seguida, clique em **[!UICONTROL Adicionar perfil]**.

   ![](assets/sms_preview_3.png)

1. Depois de selecionar seu perfil de teste, você pode fechar o **[!UICONTROL Adicionar perfil de teste]** janela.

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

* [Configurar canal de SMS](sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma mensagem de SMS.](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
