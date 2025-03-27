---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal do WhatsApp
description: Saiba como configurar seu ambiente para enviar mensagens do WhatsApp com o Journey Optimizer
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
source-git-commit: 22664437fb1f548f4c1524ea5fa7ac9e7fdc7f59
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 4%

---

# Introdução à configuração do WhatsApp {#whatsapp-config}

>[!BEGINSHADEBOX]

**Índice**

* [Introdução a mensagens do WhatsApp](get-started-whatsapp.md)
* **[Introdução à configuração do WhatsApp](whatsapp-configuration.md)**
* [Criar uma mensagem de WhatsApp](create-whatsapp.md)
* [Verificar e enviar suas mensagens do WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Antes de enviar a mensagem do WhatsApp, você deve configurar o ambiente do Adobe Journey Optimizer e associar-se à conta do WhatsApp. Para fazer isso:

1. [Criar suas credenciais da API do WhatsApp](#WhatsApp-credentials)
1. [Criar sua configuração do WhatsApp](#WhatsApp-configuration)

Estas etapas devem ser executadas por um [Administrador do Sistema](../start/path/administrator.md) do Adobe Journey Optimizer.

## Criar credenciais da API do WhatsApp {#whatsapp-credentials}

1. No painel à esquerda, vá para **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais de API, conforme detalhado abaixo:

   * **Token de API**: https://developers.facebook.com/docs/facebook-login/guides/access-tokens/
   * **ID da Conta Comercial**: insira o número exclusivo relacionado ao seu portfólio comercial. Saiba mais em [Metadocumentação](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Clique em **[!UICONTROL Continuar]**.

1. Escolha a **Conta Comercial** que deseja conectar às credenciais da API do WhatsApp.

   ![](assets/whatsapp-api-2.png)

1. Selecione o **número de telefone** usado para enviar suas mensagens do Whatsapp.

1. As configurações de número de telefone são preenchidas automaticamente:

   * **Classificação de qualidade**: reflete o feedback do cliente sobre as mensagens enviadas nas últimas 24 horas.
      * Verde: alta qualidade
      * Amarelo: qualidade do Medium
      * Vermelho: baixa qualidade

     Saiba mais sobre [Classificação de qualidade](https://www.facebook.com/business/help/766346674749731#)

   * **Taxa de transferência**: indica a taxa à qual seu número de telefone pode enviar mensagens.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens do WhatsApp. [Saiba mais](#whatsapp-configuration)

## Criar configuração do WhatsApp {#whatsapp-configuration}

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]**. Clique no botão **[!UICONTROL Criar configuração de canal]**.

   ![](assets/whatsapp-config-1.png)

1. Digite um nome e uma descrição (opcional) para a configuração e selecione o canal do WhatsApp.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

1. Selecione **[!DNL WhatsApp]** como seu canal.

   ![](assets/whatsapp-config-2.png)

1. Selecione **[!UICONTROL Ação(ões) de marketing]** para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. Saiba mais

1. Selecione a **[!UICONTROL configuração do WhatsApp]** criada anteriormente.

   ![](assets/whatsapp-config-3.png)

1. Digite o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a configuração do canal como rascunho e retomar a configuração posteriormente.

1. Depois que a configuração do canal é criada, ela é exibida na lista com o status **[!UICONTROL Processando]**.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](../configuration/channel-surfaces.md).

1. Depois que as verificações forem bem-sucedidas, a configuração do canal obterá o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado para enviar mensagens.

Agora você está pronto para enviar mensagens do WhatsApp com o Journey Optimizer.
