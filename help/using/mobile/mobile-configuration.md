---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de SMS
description: Saiba como configurar seu ambiente para enviar mensagens móveis com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b519bcd5489c441e7f22cb47783d8b99a58c2442
workflow-type: tm+mt
source-wordcount: 480
ht-degree: 40%

---

# Começar a configurar o dispositivo móvel {#sms-configuration}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como configurar o ambiente do Adobe Journey Optimizer para enviar mensagens SMS, MMS e RCS integrando um provedor, como Sinch, Twilio ou Infobip, criando um webhook e definindo uma configuração móvel.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurar o provedor de SMS com o Journey Optimizer"
>abstract="O Adobe Journey Optimizer envia mensagens de dispositivos móveis por meio de provedores de serviços de SMS. Selecione o provedor e preencha as credenciais da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurar o provedor de MMS com o Journey Optimizer"
>abstract="O Adobe Journey Optimizer envia conteúdo de mídia por meio de provedores de serviços MMS. Selecione o provedor e preencha as credenciais da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configure o provedor de SMS/RCS/MMS com o Journey Optimizer"
>abstract="Antes de enviar mensagens de dispositivos móveis (SMS/RCS/MMS), é necessário integrar as configurações do provedor com o Journey Optimizer. Depois de concluído, você precisará criar uma configuração de SMS/RCS/MMS. Essas etapas precisam ser executadas por um(a) administrador(a) de sistema do Adobe Journey Optimizer."
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
1. [Criar uma configuração para dispositivos móveis](mobile-configuration-surface.md)

Se você comprar SMS por meio do Adobe Journey Optimizer, também poderá [exibir métricas de uso de SMS](sms-usage-report.md) para reconciliar volumes MO e MT com a cobrança do fornecedor.

Estas etapas devem ser executadas por um [Administrador do Sistema](../start/path/administrator.md) do Adobe Journey Optimizer.

## Pré-requisitos{#sms-prerequisites}

Atualmente, o Adobe Journey Optimizer está integrado a provedores de terceiros que oferecem serviços de mensagens móveis independentes do Adobe Journey Optimizer. Os provedores de mensagens móveis e MMS com suporte são: **Sinch**, **Twilio** e **Infobip**. Observe que você pode configurar provedores de mensagens adicionais usando a [configuração de provedor personalizado](mobile-configuration-custom.md).

Antes de configurar o Canal móvel, você deve criar uma conta com um desses provedores para obter o **Token de API** e a **ID de serviço**, que você precisa configurar a conexão entre o Adobe Journey Optimizer e o provedor aplicável.

Seu uso de mensagens móveis e serviços MMS está sujeito a termos e condições adicionais do provedor aplicável. Como soluções de terceiros, o Sinch, o Twilio e o Infobip estão disponíveis para usuários do Adobe Journey Optimizer por meio de uma integração. A Adobe não controla a e não se responsabiliza por produtos de terceiros. Se tiver problemas ou solicitações de assistência relacionados aos serviços de mensagens móveis, entre em contato com seu provedor.

>[!CAUTION]
>
>Para acessar e editar subdomínios SMS, você deve ter a permissão **[!UICONTROL Gerenciar subdomínios SMS]** na sandbox de produção. Saiba mais sobre permissões em [esta página](../administration/high-low-permissions.md#administration-permissions).
>

