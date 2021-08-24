---
title: Introdução à configuração de push
description: Entender o fluxo de dados e os componentes da notificação por push
feature: Configurações do aplicativo, Encaminhar
role: Admin
level: Intermediate
source-git-commit: 1b11ff3848434a4cac1ca17318950481f20537c8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Introdução à configuração de push {#get-started-push}

As notificações por push ajudam você a acessar os usuários do aplicativo móvel a qualquer momento, especialmente quando não estiverem usando ativamente seu aplicativo. As notificações por push podem ajudar você a obter vários casos de uso, como fornecer atualizações sobre seu serviço, solicitar que um usuário tome medidas, alertar o usuário para um novo negócio etc. As plataformas de dispositivos exigem o opt-in antes que os usuários finais possam receber ou exibir suas notificações. O opt-in do usuário pode ser recebido assim que o aplicativo for iniciado pela primeira vez após a instalação ou em uma sessão ou fluxo de trabalho subsequente, conforme apropriado. [!DNL Journey Optimizer] O suporta notificações por push e ajuda a enviar notificações altamente relevantes a taxas de transferência líderes do setor. As notificações por push podem incluir personalização e contexto baseado em Jornadas para aproveitar os insights de dados que sua marca tem com o Adobe Experience Cloud.

Esta página ajudará você a configurar e compreender os principais serviços e fluxos de trabalho envolvidos com notificações por push em [!DNL Journey Optimizer].

As etapas para configurar o canal de push em [!DNL Adobe Journey Optimizer] são detalhadas em [nesta página](push-configuration.md).

## Notificações por push e [!DNL Adobe Journey Optimizer]

O gráfico a seguir mostra os sistemas e serviços envolvidos com fluxos de dados associados, destacando como as notificações por push são fornecidas de um ponto de vista de serviço completo.

![](assets/push-flow.png)

1. Registro do aplicativo para dispositivos móveis com marca (Android ou iOS) com APNs da Apple e serviços de mensagens por push do Google FCM
1. Os serviços de mensagens geram um token de push, que é um identificador que [!DNL Adobe Journey Optimizer] usará para direcionar o dispositivo específico com uma notificação por push.
1. O token de push gerado anteriormente é transmitido à Adobe Experience Platform e sincronizado com o Perfil do cliente em tempo real; isso é feito no OOTB com um SDK de cliente fácil de integrar
1. As mensagens de push são criadas em [!DNL Adobe Journey Optimizer], as mensagens de push são criadas em relação a uma predefinição de mensagem
1. As mensagens de push podem ser incluídas na tela de orquestração no Jornada
1. Após a publicação do Jornada, os perfis do cliente com base nas condições do Jornada são qualificados para receber notificações por push, as cargas de mensagens por push são personalizadas nesta etapa
1. As cargas de push personalizadas são encaminhadas para um serviço interno de delivery de mensagens de push
1. Esse serviço interno valida as credenciais do aplicativo associado à mensagem e
1. Envia a mensagem para os serviços de mensagens da Apple e do Google para entrega final
1. Os comentários dos serviços de mensagens são anotados, erros e sucessos são registrados para relatórios em relatórios Live &amp; Global do Jornada
1. As notificações por push são entregues aos dispositivos do usuário final
1. As interações de notificação por push do usuário final são enviadas como Eventos de experiência do cliente do usuário final por meio da integração com o SDK

## Funções dos principais serviços em notificações por push

* **Os** provedores de serviços de notificação por push são os principais serviços da Web de componentes que fornecem notificações de servidores remotos para aplicativos móveis.

   [!DNL Adobe Journey Optimizer]  O suporta plataformas Android e iOS e, consequentemente, integra-se ao seguinte:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)  - para enviar notificações para aplicativos móveis Android
   * [Apple Push Notification Service (APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  - para enviar notificações para aplicativos móveis iOS

* **Adobe Experience Platform Mobile** SDK, que fornece APIs de integração do lado do cliente para dispositivos móveis por meio de SDKs compatíveis com Android e iOS. O SDK fornece uma extensão [!DNL Adobe Journey Optimizer] que expõe uma variedade de APIs específicas para mensagens de push e permite o fluxo de dados como registrar o token de push ou enviar eventos de rastreamento de push ou qualquer outro evento de experiência personalizada para o Adobe Experience Platform. O SDK também fornece uma variedade de outras extensões que permitem outros recursos do Adobe Experience Cloud e de parceiros de terceiros.

   A integração do SDK também requer a configuração de serviços de [Coleta de dados](https://experienceleague.adobe.com/docs/launch/using/home.html?lang=pt-BR){target=&quot;_blank&quot;} do Adobe Experience Platform, como:

   * Criação de um armazenamento de dados para configurar o perfil e os conjuntos de dados do evento de experiência com base nos quais os dados fluem para o Adobe Experience Platform
   * Criação de propriedades móveis do lado do cliente e adição de extensões. O SDK integra-se estreitamente a essas extensões para fornecer uma experiência de coleta de dados contínua.
   * Registrando o identificador do pacote de aplicativos para dispositivos móveis e as credenciais do aplicativo

* **O**  Perfil do cliente em tempo real da Adobe Experience Platform mantém uma visão holística de cada cliente individual ao combinar dados de vários canais, incluindo Web, dispositivos móveis, CRM e de terceiros. O Perfil permite consolidar os dados do cliente em uma visualização unificada, oferecendo uma conta acionável com carimbo de data e hora de cada interação com o cliente. O token de push de um determinado usuário do aplicativo é armazenado em relação ao perfil do usuário como dados de registro, enquanto as interações que o usuário faz com as notificações de push são rastreadas como dados de eventos da série de tempo. [Saiba mais sobre o Perfil do cliente em tempo real do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : depois que as integrações do aplicativo móvel com os componentes acima mencionados estiverem em vigor e os perfis do cliente estiverem no Adobe Experience Platform, você poderá criar e orquestrar notificações por push no  [!DNL Adobe Journey Optimizer] para interagir com os usuários.

## Instalação técnica por push e fluxos de trabalho do profissional

O gráfico a seguir mostra as várias etapas, completas, envolvidas na configuração dos componentes que formam o esqueleto do fluxo de dados por push. Os itens de ação foram categorizados com base na função que executa a configuração e no componente que está sendo configurado.

![](assets/user-flow.png)
