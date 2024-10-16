---
solution: Journey Optimizer
product: journey optimizer
title: Verificação e envio da notificação por push
description: Saiba como verificar e enviar sua notificação por push no Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Verificação e envio da notificação por push {#send-push}

## Pré-visualizar sua notificação por push {#preview-push}

Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste para visualizar seu conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste. Você pode selecionar o tipo de dispositivo para visualizar o conteúdo: **[!UICONTROL iOS]** ou **[!UICONTROL Android]**.

![](assets/push_preview_3.png)

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Validar sua notificação por push {#push-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

* **Os avisos** referem-se às recomendações e práticas recomendadas.

* **Erros** impedem que você teste ou ative a jornada enquanto não forem resolvidos, como:

   * **[!UICONTROL A versão da mensagem por push está vazia]**: esse erro é exibido quando o corpo ou título da notificação por push está ausente. Saiba como definir o conteúdo de notificação por push em [esta seção](create-push.md).

   * **[!UICONTROL a configuração não existe]**: você não poderá usar sua mensagem se a configuração selecionada for excluída após a criação da mensagem. Se este erro ocorrer, selecione outra configuração na mensagem **[!UICONTROL Propriedades]**. Saiba mais sobre configurações de canal em [esta seção](../configuration/channel-surfaces.md).

   * **[!UICONTROL A carga do Push iOS/Android excedeu o limite de 4 KB]**: o tamanho da notificação por push não pode exceder 4 KB. Para respeitar esse limite, tente reduzir o uso de imagens ou emojis. Saiba como gerenciar o conteúdo de notificação por push nesta [seção](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Para melhorar a capacidade de delivery, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, o Twilio e o Sinch suportam apenas números de telefone no formato E.164.

## Enviar a notificação por push{#push-send}

>[!IMPORTANT]
>
>A partir da versão de setembro, uma nova experiência de ativação de campanha e jornada permitirá gerenciar todo o processo de aprovação, garantindo que campanhas e jornadas sejam totalmente revisadas e aprovadas pelas partes interessadas apropriadas antes de serem publicadas. Esse recurso está disponível em Disponibilidade limitada. [Saiba mais](../test-approve/gs-approval.md)

Quando a mensagem de push estiver pronta, conclua a configuração da [jornada](../building-journeys/journey-gs.md) ou da [campanha](../campaigns/create-campaign.md) para enviá-la.

**Tópicos relacionados**

* [Configurar canal por push](push-configuration.md)
* [Relatório de notificação por push](../reports/journey-global-report-cja-push.md)
* [Criar uma notificação por push](create-push.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)

