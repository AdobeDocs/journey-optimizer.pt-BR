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
TQID: https://experienceleague.adobe.com/QXJ9G3btsn7ZEwSB2Bm0uGt89gsh8D7SnNZ-Vw2muXM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cf64c7f6-7428-4ae5-b158-8df9771f38f4id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 6%

---

# Verificação e envio da notificação por push {#send-push}

## Pré-visualizar sua notificação por push {#preview-push}

Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente para visualizar seu conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]**. Em seguida, você pode selecionar o tipo de dispositivo para visualizar o conteúdo: **[!UICONTROL iOS]**, **[!UICONTROL Android]** ou **[!UICONTROL Web]**.

![](assets/push_preview_3.png)

Informações detalhadas sobre como visualizar e testar o conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

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
> Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para enviar a notificação por push. [Saiba mais](../test-approve/gs-approval.md)

Quando a mensagem de push estiver pronta, conclua a configuração da [jornada](../building-journeys/journey-gs.md) ou da [campanha](../campaigns/create-campaign.md) para enviá-la.

**Tópicos relacionados**

* [Configurar canal de push para dispositivos móveis](push-configuration.md)
* [Configurar canal de push para Web](push-configuration-web.md)
* [Relatório de notificação por push](../reports/journey-global-report-cja-push.md)
* [Criar uma notificação por push](create-push.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journey-action.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)

