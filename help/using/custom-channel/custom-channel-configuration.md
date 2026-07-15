---
title: Criar uma configuração de canal para um canal personalizado
description: Saiba como criar uma configuração de canal para um canal personalizado no Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 2%

---


# Criar uma configuração de canais {#create-channel-config}

Uma configuração de canal vincula seu canal personalizado a uma predefinição nomeada e reutilizável que os profissionais de marketing selecionam ao criar campanhas e jornadas.

Para criar uma configuração de canal para um canal personalizado, siga as etapas abaixo.

1. Vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**. Saiba mais sobre [criação de uma configuração de canal](../configuration/channel-surfaces.md).

1. Na lista suspensa **[!UICONTROL Selecionar canal]**, selecione um dos canais personalizados ativados.

   ![Selecionar canal](assets/custom_channel_select_channel.png){width="100%"}

1. Se o canal selecionado usar autenticação (o tipo não é **Nenhum**), o campo **[!UICONTROL Credenciais de API]** será exibido. Selecione as credenciais a serem usadas para esta configuração. [Saiba mais sobre credenciais de API](custom-channel-api-credentials.md)

   ![Selecionar credenciais de API](assets/custom_channel_config_api_credentials.png){width="100%"}

1. Se você tiver configurado subdomínios para canais personalizados no [!DNL Journey Optimizer], poderá selecionar um subdomínio delegado para usar no rastreamento de links presentes na carga para essa configuração. [Saiba como delegar um subdomínio](custom-channel-subdomains.md)

1. Se o canal selecionado tiver cabeçalhos ou parâmetros de consulta [definidos como variáveis](create-custom-channel.md#endpoint-configuration) para a URL do ponto de extremidade, a seção **[!UICONTROL Parâmetros dinâmicos]** será exibida.

   Insira o valor para cada parâmetro. Você pode usar o editor de personalização para inserir valores dinâmicos (por exemplo, um identificador de usuário resolvido no perfil). Isso permite personalizar a solicitação do para cada recipient com base nos dados de perfil.

   ![Parâmetros dinâmicos](assets/custom_channel_config_dynamic_parameters.png){width="100%"}

1. Se o canal personalizado tiver campos de conteúdo com a caixa de seleção **[!UICONTROL Configuração de canal]** habilitada, esses campos aparecerão na seção **[!UICONTROL Configuração de carga]**. [Saiba mais](create-custom-channel.md#payload-configuration)

   ![Campos de carga](assets/custom_channel_config_payload.png){width="100%"}

   Configure um valor para cada campo, conforme apropriado para essa configuração. Isso é útil para campos que podem variar com base no contexto da campanha ou jornada, como informações do remetente ou modelos de mensagem.

1. Para campanhas orquestradas, conclua a seção **[!UICONTROL Detalhes da execução]** para mapear dimensões de perfil e especificar o endereço de execução.

   ![Detalhes da execução em campanhas orquestradas](assets/custom_channel_oc_execution_details.png){width="80%"}

1. Clique em **[!UICONTROL Enviar]** para salvar e ativar a configuração do canal.

<!--
>[!CAUTION]
>
>If your organization uses approval policies, you may need to request approval before activating journeys or campaigns that use this channel configuration. [Learn more](../test-approve/gs-approval.md)
-->

## Próximas etapas {#next-steps}

O canal personalizado está totalmente configurado. Os profissionais de marketing podem começar a usá-lo para criar experiências para os clientes:

* [Criar experiências de canal personalizadas](create-custom-experience.md)
* [Testar seu canal personalizado](test-custom-channel.md)
* [Monitorar canais personalizados](configure-custom-channel.md)
