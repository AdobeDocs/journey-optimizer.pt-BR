---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Infobip
description: Saiba como configurar seu ambiente para enviar mensagens de texto e MMS com o Journey Optimizer com Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 3%

---

# Configurar provedor Infobip {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Se as palavras-chave de aceitação ou recusa não forem fornecidas, as mensagens de consentimento padrão serão usadas para honrar a privacidade do usuário. A adição de palavras-chave personalizadas substitui automaticamente os padrões.

**Palavras-chave padrão:**

* **Aceitar**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR
* **Recusar**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR INSCRIÇÃO, NÃO
* **Ajuda**: AJUDA

>[!ENDSHADEBOX]

Para configurar o Infobip com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais de API, conforme detalhado abaixo.

   * **[!UICONTROL Fornecedor de SMS]**: Infobip.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL URL de base da API]** e **[!UICONTROL chave de API]**: acesse a página inicial da interface da Web ou a página de gerenciamento de chaves de API para encontrar suas credenciais. Saiba mais em [Documentação do Infobip](https://www.infobip.com/docs/api){target="_blank"}.

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

   * **[!UICONTROL Palavras-chave de entrada personalizadas]**: defina palavras-chave exclusivas para ações específicas, por exemplo, DISCOUNT, OFFERS, ENROLL. Essas palavras-chave são capturadas e armazenadas como atributos no perfil, permitindo acionar uma qualificação de segmento de transmissão na jornada e fornecer uma resposta ou ação personalizada.

   * **[!UICONTROL Mensagem de Resposta de Entrada Padrão]**: digite a resposta padrão que é enviada quando um usuário final envia um SMS de entrada que não corresponde a nenhuma das palavras-chave definidas.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)
