---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Infobip
description: Saiba como configurar seu ambiente para enviar mensagens de texto e MMS com o Journey Optimizer com Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 5beaf2b7dc339cb94352cd7503dd86a97a6db6bd
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 1%

---

# Configurar provedor Infobip {#sms-configuration-infobip}

Ao integrar o Infobip ao Adobe Journey Optimizer, você pode enviar mensagens de texto aos seus perfis como parte de suas jornadas e campanhas.

Para configurar o Infobip como seu provedor de SMS, siga as etapas abaixo:

1. [Criar credencial de API](#api-credential)
1. [Criar webhook](sms-webhook.md)
1. [Criar configuração de canal](sms-configuration-surface.md)
1. [Criar Jornada ou Campanha com ação de canal SMS](create-sms.md)

## Configurar credenciais de API para SMS {#api-credential}

Para configurar o Infobip com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   +++ Lista de credenciais SMS para configuração

   | Campos de configuração | Descrição |
   |---|---|
   | Fornecedor de SMS | Infobip |
   | Nome | Escolha um nome para a credencial da API. |
   | URL básico da API e chave da API | Acesse a página inicial da interface da Web ou a página de gerenciamento de chaves da API para encontrar suas credenciais. Para pontos de extremidade de domínio regionais ou alternativos, por exemplo, `api-ny2.infobip.com`, especifique a URL de base completa e verifique seu token de autorização com suporte para Infobip. </br>Saiba mais em [Documentação da Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | ID da entidade principal | Informe a ID da entidade principal DLT atribuída. |
   | ID do modelo de conteúdo | Insira a ID do modelo de conteúdo DLT registrado. |
   | Período de validade | Insira o período de validade da mensagem em horas. Caso as mensagens não possam ser entregues dentro desse período, o sistema fará tentativas adicionais para reenviá-las. O período de validade padrão é definido como 48 horas. |
   | Dados de Retorno | Insira os dados adicionais do cliente que serão enviados no URL de notificação. |
   | Número de entrada | Adicione seu número de entrada exclusivo. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada. |

   +++

1. Habilite a opção **[!UICONTROL Recusa difusa]** para detectar mensagens que se assemelham a palavras-chave de recusa (por exemplo, &#39;CANCIL&#39;) e personalize a resposta de confirmação no campo **[!UICONTROL Resposta automática difusa]**.

   **[!UICONTROL A opção de recusa difusa]** identifica mensagens SMS que indicam que um usuário deseja cancelar a inscrição, mesmo que a mensagem não corresponda exatamente a uma palavra-chave de recusa definida. Ele pode detectar frases comuns de recusa e determinados termos ofensivos, ajudando a garantir que suas campanhas respeitem as preferências do usuário e permaneçam em conformidade.

1. Selecione **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para rotear o SMS de entrada desta credencial para um conjunto de dados pré-criado que você escolher na lista suspensa. [Saiba mais sobre como criar conjuntos de dados](../experience-decisioning/data-collection/create-dataset.md)

   >[!NOTE]
   >
   >O esquema do conjunto de dados deve ser **[!UICONTROL XDM ExperienceEvent]** e incluir pelo menos estes grupos de campos:
   >* Adobe CJM ExperienceEvent - Detalhes de interação da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes da execução da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes do perfil da mensagem
   >
   >O esquema e o conjunto de dados devem ser habilitados para o Perfil.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

1. Clique em **[!UICONTROL Verificar conexão de SMS]**, a partir de suas credenciais de API existentes, para testar e verificar suas credenciais de API de SMS enviando uma mensagem de exemplo para um dispositivo designado.

1. Preencha os campos **Número** e **Mensagem** e clique em **[!UICONTROL Verificar conexão]**.

   >[!IMPORTANT]
   >
   >A mensagem deve ser estruturada para se alinhar ao formato de carga do provedor.

   ![](assets/verify-connection.png)

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)

## Configurar credencial de API para RCS

O Adobe Journey Optimizer oferece suporte a mensagens RCS por meio de Infobip usando o recurso [Provedor de SMS personalizado](sms-configuration-custom.md). Isso permite a entrega de mensagens avançadas e interativas por meio de perfis empresariais verificados, incorporando elementos como carrosséis, botões e conteúdo multimídia.

➡️ [Saiba como o Infobip oferece suporte ao RCS na documentação do Infobip](https://www.infobip.com/docs/api/channels/rcs)

Para habilitar mensagens RCS com Infobip, novas credenciais de API devem ser configuradas por meio de um Provedor de SMS Personalizado. As credenciais de SMS Infobip existentes não são compatíveis, pois o RCS requer um formato de carga distinto.

Para configurar o RCS com Infobip:

1. **Registre sua empresa para o RCS via Infobip**

   Comece concluindo o processo de integração e registro do RCS na plataforma Infobip. Isso envolve configurar o perfil do remetente do RCS e garantir que sua conta esteja habilitada para RCS. Saiba mais em [Documentação de Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Criar um Webhook de SMS**

   [Configure um webhook de SMS personalizado](sms-configuration-custom.md#webhook) no Journey Optimizer. Este webhook será responsável por lidar com recibos de entrega, mensagens RCS de entrada e atualizações de status da plataforma da Infobip.

1. **Criar credencial de API usando Personalizado como fornecedor de SMS**

   [Crie uma nova credencial de API](sms-configuration-custom.md#api-credential) no Journey Optimizer, selecionando &quot;Personalizado&quot; como provedor de SMS. Use o método de autenticação de ponto de extremidade RCS, o URL base e os cabeçalhos apropriados.

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](sms-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](sms-configuration-surface.md)
