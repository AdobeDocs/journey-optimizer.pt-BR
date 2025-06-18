---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de SMS
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 33%

---

# Introdução à configuração de SMS/MMS/RCS {#sms-configuration}

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

Antes de enviar SMS, MMS ou RCS, você deve configurar o ambiente do Adobe Journey Optimizer. Para fazer isso:

1. Integre as configurações do provedor com o Journey Optimizer.
As etapas dependem do seu provedor de SMS. Navegue pelos links abaixo para acessar a documentação detalhada:
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Provedor personalizado](sms-configuration-custom.md)
1. [Criar uma configuração de SMS](sms-configuration-surface.md)

Estas etapas devem ser executadas por um [Administrador do Sistema](../start/path/administrator.md) do Adobe Journey Optimizer.

## Pré-requisitos{#sms-prerequisites}

Atualmente, o Adobe Journey Optimizer está integrado a provedores de terceiros que oferecem serviços de mensagens de texto independentes do Adobe Journey Optimizer. Os provedores de mensagens de texto e MMS com suporte são: **Sinch**, **Twilio** e **Infobip**. Observe que você pode configurar provedores de mensagens adicionais usando a [configuração de provedor personalizado](sms-configuration-custom.md).

Antes da configuração do canal SMS, você deve criar uma conta com um desses provedores para obter o **Token de API** e a **ID de Serviço**, que você precisa configurar a conexão entre o Adobe Journey Optimizer e o provedor aplicável.

O uso de mensagens de texto e serviços MMS está sujeito a termos e condições adicionais do provedor aplicável. Como soluções de terceiros, o Sinch, o Twilio e o Infobip estão disponíveis para usuários do Adobe Journey Optimizer por meio de uma integração. A Adobe não controla a e não se responsabiliza por produtos de terceiros. Em caso de problemas ou solicitações de assistência relacionados aos serviços de mensagens de texto (SMS/MMS), entre em contato com seu provedor.

>[!CAUTION]
>
>Para acessar e editar subdomínios SMS, você deve ter a permissão **[!UICONTROL Gerenciar subdomínios SMS]** na sandbox de produção. Saiba mais sobre permissões em [esta página](../administration/high-low-permissions.md#administration-permissions).
>

