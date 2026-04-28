---
solution: Journey Optimizer
product: journey optimizer
title: Definir o público da campanha acionada pela API
description: Saiba como definir o público-alvo de campanha acionada por API.
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: 6dda5687-3742-4e88-be7c-c4969b183161
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 3%

---

# Definir o público da campanha acionada pela API {#api-audience}

Use a guia **[!UICONTROL Público-alvo]** para definir o público da campanha.

![](assets/campaign-audience.png)

## Selecionar o público-alvo

**Para campanhas acionadas pela API de marketing**, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo disponíveis da Adobe Experience Platform. [Saiba mais sobre públicos](../audience/about-audiences.md).

>[!IMPORTANT]
>
>O uso de públicos-alvo e atributos da [composição de público-alvo](../audience/get-started-audience-orchestration.md) não está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Para campanhas acionadas por API transacional**, os perfis direcionados precisam ser definidos na chamada de API. Uma única chamada de API suporta até 20 recipients únicos. Cada recipient deve ter uma ID de usuário exclusiva. IDs de usuário duplicadas não são permitidas. Saiba mais na [Documentação da API de execução de mensagem interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMUnitaryMessageExecution){target="_blank"}

## Selecione o tipo de identidade

No campo **[!UICONTROL Tipo de identidade]**, escolha o tipo de chave a ser usado para identificar os indivíduos do público-alvo selecionado. Você pode usar um tipo de identidade existente ou criar um novo usando o Serviço de identidade da Adobe Experience Platform. Os namespaces de Identidade Padrão estão listados em [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

Somente um tipo de identidade é permitido por campanha. Indivíduos pertencentes a um segmento que não tem o tipo de identidade selecionado entre suas diferentes identidades não podem ser alvos da campanha. Saiba mais sobre tipos de identidade e namespaces na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

## Ativar criação de perfil na execução da campanha

Em alguns casos, pode ser necessário enviar mensagens transacionais para perfis que não existem no sistema. Por exemplo, se um usuário desconhecido tentar redefinir a senha no seu site. Quando um perfil não existe no banco de dados, o Journey Optimizer permite que você o crie automaticamente ao executar a campanha para permitir o envio da mensagem para esse perfil.

Para ativar a criação de perfil na execução da campanha, alterne a opção **[!UICONTROL Criar novos perfis]** para ativada. If this option is disabled, unknown profiles will be rejected for any sending and the API call will fail.

![](assets/api-triggered-create-profile.png)

>[!IMPORTANT]
>
>This option is provided for **very small volume profile creation** in a large volume transactional sending use case, with bulk of profiles already existing in platform.
>
>Unknown profiles are created in the **AJO Interactive Messaging Profile Dataset** dataset, in three default namespace (email, phone and ECID) respectively for each outbound channels (Email, SMS and Push). However, if you are using a custom namespace, the identity is created with the same custom namespace.
>
>Profile creation at execution is not available for [High Throughput campaigns](../campaigns/api-triggered-high-throughput.md), as this mode does not rely on Adobe profiles. The system will not check whether the profiles exist or not.

## Habilitar webhooks {#webhook}

For Transactional API triggered campaigns, you can enable webhooks to receive real-time feedback on the execution status of your messages. To do this, toggle the **[!UICONTROL Enable webhooks]** option to send delivery status events to a configured webhook.

![](assets/api-triggered-webhook.png)

Webhook configurations are managed centrally in the **[!UICONTROL Administration]** / **[!UICONTROL Channels]** / **[!UICONTROL Feedback Webhook]** menu. From there, administrators can create and edit webhook endpoints. [Learn how to create Feedback Webhooks](../configuration/feedback-webhooks.md)

## Próximas etapas {#next}

Once your campaign configuration and content are ready, you can schedule its execution. [Saiba mais](api-triggered-campaign-schedule.md)
