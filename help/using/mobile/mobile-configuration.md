---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de SMS
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9a68782b0ca1a9a65db621209cf4f39ea5ce911d
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 41%

---

# Introdução à configuração móvel {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurar o provedor de SMS com o Journey Optimizer"
>abstract="O Adobe Journey Optimizer envia mensagens de texto por meio de provedores de serviços de SMS. Selecione o provedor e preencha as credenciais da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurar o provedor de MMS com o Journey Optimizer"
>abstract="O Adobe Journey Optimizer envia conteúdo de mídia por meio de provedores de serviços MMS. Selecione o provedor e preencha as credenciais da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configuração do provedor de SMS/MMS com o Journey Optimizer"
>abstract="Antes de enviar mensagens de texto (SMS/MMS), é necessário integrar as configurações do provedor com o Journey Optimizer. Depois de concluído, você precisará criar uma configuração de SMS/MMS. Essas etapas precisam ser executadas por um(a) administrador(a) de sistema do Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Criar uma configuração de canais SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecionar a configuração do fornecedor de SMS"
>abstract="Selecione as credenciais da API configuradas para seu fornecedor de SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Recusa difusa"
>abstract="Quando habilitada, a opção de Recusa difusa detecta mensagens de entrada que se aproximam às palavras-chave de recusa definidas (por exemplo, CANCILAR) e envia automaticamente uma resposta de confirmação para verificar a intenção de cancelamento de inscrição do usuário. Se o usuário confirmar por meio do prompt definido, sua inscrição será cancelada."

Antes de enviar SMS, MMS ou RCS, você deve configurar o ambiente do Adobe Journey Optimizer. Para fazer isso:

1. Integre as configurações do provedor com o Journey Optimizer.
As etapas dependem do seu provedor de SMS. Navegue pelos links abaixo para acessar a documentação detalhada:
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [Provedor personalizado](mobile-configuration-custom.md)
1. [Criar webhook](mobile-webhook.md)
1. [Criar uma configuração móvel](mobile-configuration-surface.md)

Estas etapas devem ser executadas por um [Administrador do Sistema](../start/path/administrator.md) do Adobe Journey Optimizer.

## Pré-requisitos{#sms-prerequisites}

Atualmente, o Adobe Journey Optimizer está integrado a provedores de terceiros que oferecem serviços de mensagens de texto independentes do Adobe Journey Optimizer. Os provedores de mensagens de texto e MMS com suporte são: **Sinch**, **Twilio** e **Infobip**. Observe que você pode configurar provedores de mensagens adicionais usando a [configuração de provedor personalizado](mobile-configuration-custom.md).

Antes de configurar o Canal móvel, você deve criar uma conta com um desses provedores para obter o **Token de API** e a **ID de serviço**, que você precisa configurar a conexão entre o Adobe Journey Optimizer e o provedor aplicável.

O uso de mensagens de texto e serviços MMS está sujeito a termos e condições adicionais do provedor aplicável. Como soluções de terceiros, o Sinch, o Twilio e o Infobip estão disponíveis para usuários do Adobe Journey Optimizer por meio de uma integração. A Adobe não controla a e não se responsabiliza por produtos de terceiros. Se tiver problemas ou solicitações de assistência relacionados aos serviços de mensagens móveis, entre em contato com seu provedor.

>[!CAUTION]
>
>Para acessar e editar subdomínios SMS, você deve ter a permissão **[!UICONTROL Gerenciar subdomínios SMS]** na sandbox de produção. Saiba mais sobre permissões em [esta página](../administration/high-low-permissions.md#administration-permissions).
>

