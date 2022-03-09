---
title: Introdução à configuração de push
description: Entender o fluxo de dados e os componentes da notificação por push
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 5%

---

# Introdução à configuração de push {#get-started-push}

Esta página ajudará você a configurar e compreender os principais serviços e fluxos de trabalho envolvidos com as notificações por push em [!DNL Journey Optimizer]. Saiba como criar notificações por push no [esta página](create-push.md).

Etapas para configurar o canal de push em [!DNL Adobe Journey Optimizer] são detalhadas em [esta página](push-configuration.md).

## Notificações por push e [!DNL Adobe Journey Optimizer] {#push-notifications-and-journey-optimizer}

O gráfico a seguir mostra os sistemas e serviços envolvidos com fluxos de dados associados, destacando como as notificações por push são fornecidas de um ponto de vista de serviço completo.

![](assets/push-flow.png)

1. Registro do aplicativo para dispositivos móveis com marca (Android ou iOS) com APNs Apple e serviços de mensagens por push FCM do Google
1. Os serviços de mensagens geram um token de push, que é um identificador que [!DNL Adobe Journey Optimizer] será usado para direcionar o dispositivo específico com uma notificação por push.
1. O token de push gerado anteriormente é transmitido à Adobe Experience Platform e sincronizado com o Perfil do cliente em tempo real; isso é feito no OOTB com um SDK de cliente fácil de integrar
1. As mensagens de push são criadas em [!DNL Adobe Journey Optimizer], mensagens de push são criadas em relação a uma predefinição de mensagem
1. As mensagens de push podem ser incluídas na tela de orquestração no Jornada
1. Após a publicação do Jornada, os perfis do cliente com base nas condições do Jornada são qualificados para receber notificações por push, as cargas de mensagens por push são personalizadas nesta etapa
1. As cargas de push personalizadas são encaminhadas para um serviço interno de delivery de mensagens de push
1. Esse serviço interno valida as credenciais do aplicativo associado à mensagem e
1. Envia a mensagem para os serviços de mensagens da Apple e Google para entrega final
1. Os comentários dos serviços de mensagens são anotados, erros e sucessos são registrados para relatórios em relatórios Live &amp; Global do Jornada
1. As notificações por push são entregues aos dispositivos do usuário final
1. As interações de notificação por push do usuário final são enviadas como Eventos de experiência do cliente do usuário final por meio da integração com o SDK

## Funções dos principais serviços em notificações por push {#roles-of-key-services}

* **Provedores de serviços de notificação por push** são os principais serviços da Web de componentes que fornecem notificações de servidores remotos para aplicativos móveis.

   [!DNL Adobe Journey Optimizer]  O suporta plataformas Android e iOS e, consequentemente, integra-se ao seguinte:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - para enviar notificações para o aplicativo móvel Android
   * [Serviço de notificação por push (APNs) do Apple](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - para enviar notificações para o aplicativo móvel iOS

* **Adobe Experience Platform Mobile SDK** que fornece APIs de integração do lado do cliente para dispositivos móveis por meio de SDKs compatíveis com Android e iOS. O SDK fornece um [!DNL Adobe Journey Optimizer] Exposição de uma variedade de APIs específicas para mensagens de push e habilitação do fluxo de dados, como registrar o token de push ou enviar eventos de rastreamento de push ou qualquer outro evento de experiência personalizada para o Adobe Experience Platform. O SDK também fornece uma variedade de outras extensões que permitem outros recursos do Adobe Experience Cloud e de parceiros de terceiros.

   A integração do SDK também requer a configuração do Adobe Experience Platform [Coleta de dados](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=pt-BR){target=&quot;_blank&quot;} serviços como:

   * Criação de um armazenamento de dados para configurar o perfil e os conjuntos de dados do evento de experiência com base nos quais os dados fluem para o Adobe Experience Platform
   * Criação de propriedades móveis do lado do cliente e adição de extensões. O SDK integra-se estreitamente a essas extensões para fornecer uma experiência de coleta de dados contínua.
   * Registrando o identificador do pacote de aplicativos para dispositivos móveis e as credenciais do aplicativo

* **Perfil do cliente em tempo real da Adobe Experience Platform**  O mantém uma visualização holística de cada cliente individual ao combinar dados de vários canais, incluindo Web, dispositivos móveis, CRM e de terceiros. O Perfil permite consolidar os dados do cliente em uma visualização unificada, oferecendo uma conta acionável com carimbo de data e hora de cada interação com o cliente. O token de push de um determinado usuário do aplicativo é armazenado em relação ao perfil do usuário como dados de registro, enquanto as interações que o usuário faz com as notificações de push são rastreadas como dados de eventos da série de tempo. [Saiba mais sobre o Perfil do cliente em tempo real da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : depois que as integrações do aplicativo móvel com os componentes mencionados acima estiverem em vigor e os perfis do cliente estiverem em vigor no Adobe Experience Platform, você poderá criar e orquestrar notificações por push em [!DNL Adobe Journey Optimizer] para interagir com seus usuários.

## Instalação técnica por push e fluxos de trabalho do profissional {#push-technical-setup}

O gráfico a seguir mostra as várias etapas, completas, envolvidas na configuração dos componentes que formam o esqueleto do fluxo de dados por push. Os itens de ação foram categorizados com base na função que executa a configuração e no componente que está sendo configurado.

![](assets/user-flow.png)
