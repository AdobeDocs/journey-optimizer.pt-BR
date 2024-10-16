---
solution: Journey Optimizer
product: journey optimizer
title: Verificar e testar suas mensagens de texto
description: Saiba como verificar e enviar suas mensagens de texto no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Verifique e envie sua mensagem de texto (SMS/MMS){#send-sms}

## Pré-visualizar sua mensagem de texto {#preview-sms}

Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste para visualizar seu conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar sua mensagem usando os dados do perfil de teste.

![](assets/sms_preview_2.png)

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Validar seu conteúdo {#sms-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

![](assets/sms-alert-button.png)

* **Os avisos** referem-se às recomendações e práticas recomendadas. Por exemplo, uma mensagem de aviso será exibida se a mensagem de texto estiver vazia.

* **Erros** impedem que você teste ou ative a jornada, ou publique a campanha, desde que não sejam resolvidos. Por exemplo, uma mensagem de erro avisa quando a linha de assunto está ausente.


>[!NOTE]
>
> Para melhorar sua capacidade de delivery, use os números de telefone nos formatos compatíveis com o provedor. Por exemplo, o Twilio e o Sinch suportam apenas números de telefone no formato E.164.

## Envie suas mensagens de texto {#sms-send}

>[!IMPORTANT]
>
>A partir da versão de setembro, uma nova experiência de ativação de campanha e jornada permitirá gerenciar todo o processo de aprovação, garantindo que campanhas e jornadas sejam totalmente revisadas e aprovadas pelas partes interessadas apropriadas antes de serem publicadas. Esse recurso está disponível em Disponibilidade limitada. [Saiba mais](../test-approve/gs-approval.md)

Quando a mensagem de texto estiver pronta, conclua a configuração da [jornada](../building-journeys/journey-gs.md) ou da [campanha](../campaigns/create-campaign.md) para enviá-la.

**Tópicos relacionados**

* [Configuração de canal de SMS](sms-configuration.md)
* [Relatórios SMS/MMS](../reports/journey-global-report-cja-sms.md)
* [Criação de uma mensagem de texto](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
