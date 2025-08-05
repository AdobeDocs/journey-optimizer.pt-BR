---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal LINE
description: Saiba como configurar seu ambiente para enviar mensagens LINE com o Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
source-git-commit: bc734ed1249b1ec186eb5f479d605bafee8a1d06
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 6%

---

# Configurar canal LINE no Journey Optimizer {#line-configuration}

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/line-config-1.png)

1. Insira um nome e uma descrição (opcional) para a configuração e selecione o canal a ser configurado.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Selecione o canal **LINE**.

   ![](assets/line-config-2.png)

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Selecione o tipo de mensagem para a configuração:

   * **Marketing**: para mensagens promocionais, como promoções semanais para uma loja de varejo. Essas mensagens exigem o consentimento do usuário e devem estar em conformidade com a política do LINE em relação à aceitação de usuários.
   * **Transacional**: para mensagens não comerciais, como confirmações de pedidos, notificações de redefinição de senha ou atualizações de entrega. Essas mensagens podem ser enviadas até mesmo para usuários que cancelaram a assinatura de comunicações de marketing, mas estão estritamente limitados a contextos transacionais específicos.

1. Selecione suas **[!UICONTROL Configurações de canal]**.

   Entre em contato com o representante da Adobe para definir suas **[!UICONTROL Configurações de canal]**.

   ![](assets/line-config-2.png)

1. Selecione a **[!UICONTROL ID de usuário do LINE]** que deseja mapear. Esse é o identificador usado para vincular mensagens a usuários individuais no canal LINE.

1. Digite seu **[!UICONTROL Nome do Remetente]**, como o nome da sua marca.

1. Envie suas alterações.

Agora é possível selecionar sua configuração ao criar a mensagem LINE.

## Definir a API de configurações do canal LINE {#line-api}

Essa API define as configurações de canal que armazenam a autorização e os detalhes de configuração necessários para a conexão com a API de mensagens LINE. Essas configurações permitem que o Adobe Journey Optimizer autentique e envie mensagens por meio do LINE usando as credenciais fornecidas.

**Ponto de extremidade**

```
POST https://platform.adobe.io/journey/imp/config/channel-settings
```

| Nome do cabeçalho | Descrição |
|-|-|
| Autorização | Token de usuário da conta técnica |
| x-api-key | ID do cliente da Adobe Developer Console |
| x-gw-ims-org-id | Seu IMS Organization ID |
| x-sandbox-name | Nome da sandbox, por exemplo, prod |
| Tipo de conteúdo | Deve ser application/json |


**Solicitar corpo**

```json
{
    "name": "your_defined_name",
    "channelRegistryId": "line",
    "channel": "line",
    "channelSettings": {
        "channelId": "your_line_channel_id",
        "channelSecret": "your_line_channel_secret"
    }
}
```

**Resposta das Configurações de Canal**

```json
{
"id": "3603ed66-ae86-42b8-8a90-d4b4e54e7c3b",
"name": "your_defined_name",
"channelRegistryId": "line",
"channel": "line",
"channelSettings": {
    "channelId": "your_line_channel_id",
    "channelSecret": "your_line_channel_secret"
    },
    "channelPublicationId": "v1_line",
    "createdAt": "2025-07-30T12:00:00.000Z",
    "modifiedAt": "2025-07-30T12:00:00.000Z",
    "isFromLatestVersion": true,
    "_etag": "\"eab98d24-18af-48ae-90f9-e59d4f8cfb2b\""
}
```
