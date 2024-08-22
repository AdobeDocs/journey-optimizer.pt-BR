---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Infobip
description: Saiba como configurar seu ambiente para enviar mensagens de texto e MMS com o Journey Optimizer com Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 5%

---

# Configurar provedor Infobip {#sms-configuration-infobip}

Para configurar o Infobip com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais de API, conforme detalhado abaixo.

   * **[!UICONTROL Fornecedor de SMS]**: Infobip.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL URL de base da API]** e **[!UICONTROL chave de API]**: acesse a página inicial da interface da Web ou a página de gerenciamento de chaves de API para encontrar suas credenciais. Saiba mais em [Documentação de Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Palavras-chave de aceitação]**: digite as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **[!UICONTROL Mensagem de aceitação]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de aceitação]**: digite a resposta personalizada que é enviada automaticamente como sua **[!UICONTROL Mensagem de aceitação]**.

   * **[!UICONTROL Palavras-chave de recusa]**: digite as palavras-chave ou padrão que dispararão automaticamente sua **[!UICONTROL Mensagem de recusa]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de recusa]**: digite a resposta personalizada que é enviada automaticamente como sua **[!UICONTROL Mensagem de recusa]**.

   * **[!UICONTROL Palavras-chave da Ajuda]**: digite as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **Mensagem da Ajuda**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de Ajuda]**: digite a resposta personalizada que é enviada automaticamente como sua **Mensagem de Ajuda**.

   * **[!UICONTROL Palavras-chave de Aceitação Dupla]**: digite as palavras-chave que disparam o processo de aceitação dupla. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de aceitação dupla]**: digite a resposta personalizada que é enviada automaticamente em resposta à confirmação da aceitação dupla.

   * **[!UICONTROL ID da Entidade Principal]**: digite sua ID de entidade principal DLT atribuída.

   * **[!UICONTROL ID do Modelo de Conteúdo]**: digite sua ID de modelo de conteúdo DLT registrada.

   * **[!UICONTROL Período de Validade]**: digite o período de validade da mensagem em horas. Caso as mensagens não possam ser entregues dentro desse período, o sistema fará tentativas adicionais para reenviá-las. O período de validade padrão é definido como 48 horas.

   * **[!UICONTROL Dados de Retorno de Chamada]**: insira os dados adicionais do cliente que serão enviados na URL de Notificação.

   * **[!UICONTROL Número de Entrada]**: adicione seu número de entrada exclusivo. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)
