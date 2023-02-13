---
solution: Journey Optimizer
product: journey optimizer
title: Visualizar e testar sua mensagem SMS
description: Saiba como visualizar e testar sua mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 6%

---

# Visualizar e testar sua mensagem SMS {#send-sms}

## Visualizar seu SMS {#preview-sms}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando dados de perfil de teste.

1. Clique em **[!UICONTROL Simular conteúdo]**.

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para adicionar um perfil de teste.

1. Encontre seu perfil de teste com a **[!UICONTROL Namespace de identidade]** e **[!UICONTROL Valor de identidade]** campos. Em seguida, clique em **[!UICONTROL Adicionar perfil]**.

   ![](assets/sms_preview_3.png)

1. Depois de selecionar seu perfil de teste, você pode fechar o **[!UICONTROL Adicionar perfil de teste]** janela.

1. No **Visualizar e testar** , os dados do perfil de teste são adicionados ao conteúdo da mensagem.

   ![](assets/sms_preview_2.png)


## Validar o SMS{#sms-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem acontecer: avisos e erros.

* **Avisos** consulte recomendações e práticas recomendadas. Por exemplo, uma mensagem de aviso será exibida se a mensagem SMS estiver vazia.

* **Erros** impedir que você teste ou ative a jornada ou publique a campanha, desde que elas não sejam resolvidas. Por exemplo, uma mensagem de erro avisa quando a linha de assunto está ausente.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Para melhorar o deliverability, use os números de telefone nos formatos compatíveis com o provedor. Por exemplo, Twilio e Sinch suportam apenas números de telefone no formato E.164.

## Enviar seu SMS{#sms-send}

Quando a mensagem SMS estiver pronta, conclua a configuração de seu [jornada](../building-journeys/journey-gs.md) ou [campanha](../campaigns/create-campaign.md) para enviá-lo.

**Tópicos relacionados**

* [Configurar canal de SMS](sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma mensagem de SMS.](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
