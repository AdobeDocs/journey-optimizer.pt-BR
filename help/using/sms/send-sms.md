---
solution: Journey Optimizer
product: journey optimizer
title: Pré-visualizar e testar a mensagem SMS
description: Saiba como pré-visualizar e testar sua mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# Pré-visualizar e testar a mensagem SMS {#send-sms}

## Pré-visualizar seu SMS {#preview-sms}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para visualizar e testar o conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

1. Clique em **[!UICONTROL Simular conteúdo]**.

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para adicionar um perfil de teste.

1. Encontre seu perfil de teste com o **[!UICONTROL Namespace de identidade]** e **[!UICONTROL Valor de identidade]** campos. Em seguida, clique em **[!UICONTROL Adicionar perfil]**.

   ![](assets/sms_preview_3.png)

1. Depois de selecionar o perfil de teste, você pode fechar o **[!UICONTROL Adicionar perfil de teste]** janela.

1. No **Visualização e teste** , os dados do perfil de teste são adicionados ao conteúdo da mensagem.

   ![](assets/sms_preview_2.png)


## Validar seu SMS{#sms-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

* **Avisos** consulte recomendações e práticas recomendadas. Por exemplo, uma mensagem de aviso será exibida se a mensagem SMS estiver vazia.

* **Erros** impede que você teste ou ative a jornada, ou publique a campanha, desde que não sejam resolvidos. Por exemplo, uma mensagem de erro avisa quando a linha de assunto está ausente.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Para melhorar sua capacidade de delivery, use os números de telefone nos formatos compatíveis com o provedor. Por exemplo, o Twilio e o Sinch suportam apenas números de telefone no formato E.164.

## Envie seu SMS{#sms-send}

Quando a mensagem SMS estiver pronta, conclua a configuração de [jornada](../building-journeys/journey-gs.md) ou [campaign](../campaigns/create-campaign.md) para enviá-lo.

**Tópicos relacionados**

* [Configurar canal de SMS](sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma mensagem de SMS.](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
