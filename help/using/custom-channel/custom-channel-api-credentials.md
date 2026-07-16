---
title: Gerenciar credenciais de API para canais personalizados
description: Saiba como gerenciar credenciais de API para canais personalizados no Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---


# Gerenciar credenciais de API {#api-credentials}

Quando um canal personalizado é criado com um tipo de autenticação diferente de **Nenhum**, um conjunto inicial de credenciais de API é gerado automaticamente quando o canal é ativado.

Você pode exibir, gerenciar e editar credenciais em **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Construtor de canais]** > **[!UICONTROL Credenciais de API]**.

![Credenciais da API](assets/custom_channel_api_credentials.png){width="100%"}

Ter várias credenciais para o mesmo canal permite anexar diferentes valores de autenticação a diferentes configurações de canal, por exemplo, para diferentes marcas ou casos de uso, sem duplicar a definição do canal.

Para editar um conjunto existente de credenciais, clique em um item na lista de inventário. Todos os campos são editáveis.

Para criar credenciais adicionais para o mesmo canal, siga as etapas abaixo.

1. Na lista **[!UICONTROL Credenciais da API]**, clique em **[!UICONTROL Criar credenciais de API]**.

1. Forneça um nome e uma descrição.

   ![Criar credenciais de API](assets/custom_channel_create_api_credentials.png){width="100%"}

1. Selecione o **[!UICONTROL Canal]** para o qual você está criando credenciais.

   >[!NOTE]
   >
   >Somente canais personalizados ativados com um tipo de autenticação diferente de **Nenhum** são exibidos na lista suspensa.

1. Selecione o **[!UICONTROL Tipo de autenticação]** na lista.
1. Preencha os campos específicos de autenticação:
   * **[!UICONTROL Chave de API]** - Forneça o nome da chave, o valor e o local (parâmetro de consulta ou cabeçalho).
   * **[!UICONTROL Autenticação básica]** - Forneça um nome de usuário e senha.
   * **[!UICONTROL OAuth 2.0]** - Configure a carga para a autenticação OAuth 2.0.
1. Clique em **[!UICONTROL Save]**.

## Próximas etapas {#next-steps}

* [Delegar um subdomínio](custom-channel-subdomains.md) (opcional — obrigatório para rastreamento de link)
* [Criar uma configuração de canais](custom-channel-configuration.md)
