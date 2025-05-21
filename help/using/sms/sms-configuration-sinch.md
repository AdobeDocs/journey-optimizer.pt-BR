---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Sinch
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 3%

---

# Configurar provedor Sinch {#sms-configuration-sinch}

Ao usar o provedor Sinch com o Journey Optimizer, você pode encontrar duas opções distintas:

* **Configuração de SMS**: configure suas credenciais da API Sinch para enviar mensagens SMS facilmente.

* **Configuração do MMS**: para mensagens multimídia (MMS), configure suas credenciais da API do Sinch MMS. Observe que o rastreamento e a resposta às mensagens de entrada são manipulados pela configuração do SMS. A configuração do MMS é somente para entrega de saída da mensagem MMS.

## Credenciais da API Sinch{#create-api}

>[!BEGINSHADEBOX]

Se as palavras-chave de aceitação ou recusa não forem fornecidas, as mensagens de consentimento padrão serão usadas para honrar a privacidade do usuário. A adição de palavras-chave personalizadas substitui automaticamente os padrões.

**Palavras-chave padrão:**

* **Aceitar**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR
* **Recusar**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR INSCRIÇÃO, NÃO
* **Ajuda**: AJUDA

>[!ENDSHADEBOX]

Para configurar seu provedor Sinch para enviar mensagens SMS e MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

+++ Lista de credenciais SMS para configuração

   | Campos de configuração | Descrição |
   |---|---|    
   | Fornecedor de SMS | Sinch |
   | Nome | Escolha um nome para a credencial da API. |
   | ID de serviço e token de API | Para acessar a página APIs, você pode encontrar suas credenciais na guia SMS. Saiba mais em [Documentação da Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Palavras-chave de Opt-in | Insira as palavras-chave padrão ou personalizadas que acionarão automaticamente sua Mensagem de aceitação. Para várias palavras-chave, use valores separados por vírgulas. |
   | Mensagem de Opt-in | Insira a resposta personalizada que é enviada automaticamente como sua mensagem de aceitação. |
   | Palavras-chave de recusa | Insira as palavras-chave padrão ou personalizadas que acionarão automaticamente sua mensagem de recusa. Para várias palavras-chave, use valores separados por vírgulas. |
   | Mensagem de recusa | Insira a resposta personalizada que é enviada automaticamente como sua mensagem de recusa. |
   | Palavras-chave da Ajuda | Insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **Mensagem de Ajuda**. Para várias palavras-chave, use valores separados por vírgulas. |
   | Mensagem de ajuda | Digite a resposta personalizada que é enviada automaticamente como sua **Mensagem de Ajuda**. |
   | Palavras-chave de aceitação dupla | Insira as palavras-chave que acionam o processo de aceitação dupla. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. Para várias palavras-chave, use valores separados por vírgulas. [Saiba mais sobre a Aceitação Dupla de SMS](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Mensagem de aceitação dupla | Insira a resposta personalizada que é enviada automaticamente em resposta à confirmação de aceitação dupla. |
   | Número de entrada | Adicione seu número de entrada exclusivo ou código curto. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada ou código curto. |
   | Palavras-chave de entrada personalizadas | Defina palavras-chave exclusivas para ações específicas, por exemplo, DESCONTO, OFERTAS, INSCRIÇÃO. Essas palavras-chave são capturadas e armazenadas como atributos no perfil, permitindo acionar uma qualificação de segmento de transmissão na jornada e fornecer uma resposta ou ação personalizada. |
   | Mensagem de resposta de entrada padrão | Insira a resposta padrão que é enviada quando um usuário final envia um SMS de entrada que não corresponde a nenhuma das palavras-chave definidas. |
   | Substituir URL | Insira seu URL personalizado para substituir os endpoints padrão para relatórios do delivery de SMS, dados de feedback, mensagens de entrada ou notificações de eventos. A Sinch enviará todas as atualizações relevantes para esse URL em vez das predefinidas. |

+++

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens SMS. [Saiba mais](sms-configuration-surface.md)

## Credenciais da API do MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Juntamente com a configuração do MMS, também é necessário criar credenciais da API Sinch especificamente para rastrear mensagens de entrada e gerenciar solicitações de consentimento.

Para configurar o Sinch MMS para enviar o MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API do MMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL ID do Projeto]**, **[!UICONTROL ID do Aplicativo]** e **[!UICONTROL Token da API]**: siga as etapas abaixo para coletar suas credenciais de API do MMS.

      * Para **[!UICONTROL ID do Projeto]** e **[!UICONTROL ID do Aplicativo]**: Acesse a página [Visão Geral da API de Conversa](https://dashboard.sinch.com/convapi/overview) do seu projeto Sinch no Painel Sinch.
      * Para **[!UICONTROL Token de API]**: obtenha as [Chaves de acesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para o seu Projeto Sinch e gere um **Token de API Base64** do seu Projeto Sinch **Chaves de acesso**.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens MMS. [Saiba mais](sms-configuration-surface.md)
