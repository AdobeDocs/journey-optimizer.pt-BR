---
title: Introdução à configuração de push
description: Entender o fluxo de dados e os componentes da notificação por push
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Introdução à configuração de push {#get-started-push}

![](assets/do-not-localize/badge.png)

As notificações por push servem como um canal de comunicação rápida, permitindo que você transmita mensagens, ofertas ou outras informações para os usuários do aplicativo móvel. Normalmente, o usuário final deve aceitar receber notificações por push; o opt-in geralmente ocorre durante o processo de instalação e os usuários finais têm uma maneira de gerenciar notificações se alterarem suas mentes posteriormente. Uma vantagem importante das notificações por push na computação móvel é que a tecnologia não requer que aplicativos específicos em um dispositivo móvel sejam abertos para que uma mensagem seja recebida. Isso permite que um smartphone receba e exiba notificações, mesmo quando a tela do dispositivo estiver bloqueada e o aplicativo móvel estiver em segundo ou fechado.

**[!DNL Adobe Journey Optimizer]**  O permite enviar mensagens de push sensíveis ao tempo, relevantes e personalizadas em uma escala grande. Um segmento de perfis de clientes pode ser direcionado para receber notificações por push avançadas em seus dispositivos móveis iOS e Android. Esses segmentos podem ser criados com base em eventos de experiência do usuário passados ou ao vivo, dados de registro do usuário ou uma combinação de interações e dados do usuário. Quando uma jornada estiver em execução, você poderá exibir relatórios detalhados de quantas mensagens foram enviadas, falharam por qual motivo e também informações de rastreamento de push, como quantos usuários clicaram nelas.

Este documento o guiará por um fluxo de dados completo das notificações por push básicas usando [!DNL Journey Optimizer] e um diagrama de fluxo de usuário para explicar como cada função cumpre suas responsabilidades e colabora para unir o fluxo de dados por push.


## Componentes e serviços envolvidos

* **Os** provedores de mensagens em nuvem são serviços de terceiros que nos permitem enviar notificações de servidores remotos para aplicativos móveis.

   [!DNL Adobe Journey Optimizer]  O suporta plataformas Android e iOS e lida com dois serviços principais de mensagens em nuvem:
   * Firebase Cloud Messaging (FCM) - para enviar notificações para aplicativos móveis Android
   * Apple Push Notification Service (APNs) - para enviar notificações para aplicativos móveis iOS

* **Aplicativo móvel integrado com o Adobe Mobile** SDK, que ajuda a integrar seus aplicativos móveis com as soluções da Adobe Experience Cloud. O SDK móvel é composto por várias extensões de solução Experience Cloud para fornecer recursos específicos ao serviço que representam. Essas extensões expõem várias APIs para ativar o fluxo de dados, como registrar o token de push ou enviar eventos de rastreamento de push ou qualquer outro evento de experiência personalizada para o Adobe Experience Platform.

* **O Adobe Launch**  (ou Data Collection) é a próxima geração de recursos de gerenciamento de SDKs móveis que permite o fluxo de dados do SDK móvel para  [!DNL Adobe Experience Platform]. Ele fornece recursos para registrar extensões, criar regras e elementos de dados para enviar dados do aplicativo móvel para as soluções da Adobe Experience Cloud. Com relação ao fluxo de dados das notificações por push, as principais configurações necessárias no Adobe Launch são:

   * Criação de um armazenamento de dados para configurar os conjuntos de dados do perfil e do evento de experiência com base nos quais os dados fluem para a plataforma de experiência.
   * Criação de uma propriedade móvel do lado do cliente e adição de extensões. O SDK móvel se integra estreitamente a essas extensões para fornecer uma experiência de coleta de dados contínua.
   * Registrar o identificador do pacote de aplicativos para dispositivos móveis e as credenciais do aplicativo que ajudariam a identificar e validar exclusivamente a conformidade do aplicativo no momento do envio da notificação por push.

* **Perfis do cliente em tempo real é o componente no Adobe Experience Platform que permite visualizar uma visualização holística de cada cliente individual ao combinar dados de vários canais, incluindo Web, dispositivos móveis, CRM e de terceiros.** O Perfil permite consolidar os dados do cliente em uma visualização unificada, oferecendo uma conta acionável com carimbo de data e hora de cada interação com o cliente. Os dados estáticos que identificam o usuário do aplicativo móvel, como um token por push, são armazenados em relação ao perfil do usuário como dados de registro, enquanto as interações que o usuário faz com as notificações por push são rastreadas como dados de eventos da série de tempo.

* **[!DNL Adobe Journey Optimizer]** : quando as integrações de aplicativos móveis com os componentes mencionados acima estiverem em vigor e os perfis de clientes estiverem disponíveis como perfis de clientes em tempo real, você poderá aproveitar os poderosos recursos de segmentação de público-alvo no  [!DNL Adobe Journey Optimizer]  para garantir a melhor experiência para cada pessoa.


## Fluxo de dados por push

Este diagrama mostra um fluxo básico de dados de mensagens de push e dá uma espiada nos vários produtos e componentes do Adobe envolvidos no fluxo.

![](assets/push-flow.png)


1. O cliente desenvolve um aplicativo móvel no Android ou iOS que lançaria para seus usuários. Para usar o recurso de push fornecido pelos provedores de push, ou seja, APNS pela Apple e FCM pelo Google, o aplicativo móvel se registra e habilita o recurso de push.
1. Os provedores de push geram e enviam um token de push para o aplicativo móvel. Um token de push é um identificador que os remetentes usam para direcionar dispositivos específicos com uma notificação por push.
1. O aplicativo móvel é integrado ao SDK do Adobe Mobile, que expõe várias extensões e APIs. A extensão Mensagens expõe uma API para registrar o token de push no Adobe Experience Platform no perfil do cliente.
1. Quando o aplicativo móvel estiver pronto, ele será configurado em **[!DNL Journey Launch]** `>` **Configurações do aplicativo** juntamente com as credenciais.
O profissional de marketing agora cria uma notificação por push em **[!DNL Adone Journey Optimizer]** `>` **Mensagens** em relação ao aplicativo móvel registrado.
1. O comerciante orquestra uma jornada do cliente definindo o fluxo de eventos e ações. Para enviar uma notificação por push em um estágio da jornada, o profissional de marketing adiciona uma ação do tipo &quot;Mensagem&quot; e a associa à mensagem criada na etapa anterior.
1. Sempre que um perfil de cliente se qualifica para receber a notificação por push por qualquer motivo, por exemplo, no disparo de um evento ou na qualificação de um segmento, a mensagem é personalizada em relação ao perfil, se aplicável.
1. A mensagem de push personalizada é enviada para processamento adicional no serviço de delivery de push.
1. O serviço de delivery de push valida as credenciais do aplicativo associado à mensagem.
1. A mensagem é enviada aos provedores de push para entrega no aplicativo móvel em relação ao token de push e às credenciais específicas.
1. Os provedores de push enviam um feedback sugerindo se a mensagem foi entregue com êxito ao provedor ou não. Caso contrário, a mensagem de erro relevante faz parte do feedback. Esse feedback é enviado para o relatório do Adobe para que o cliente visualize em sua Jornada [Live](reports/live-report.md) e [Relatórios Globais](reports/global-report.md).
1. Enquanto isso, os provedores de push entregam de forma assíncrona a notificação por push bem-sucedida ao aplicativo móvel.
1. À medida que o cliente interage com a notificação, as impressões, como clicar/abrir, podem ser rastreadas como **Eventos de experiência**. A extensão Mensagens expõe APIs para enviar eventos de rastreamento ao Adobe Experience Platform em relação ao perfil do cliente.

## Fluxo do usuário de push

Este diagrama mostra as várias etapas envolvidas na configuração dos componentes que formam o esqueleto do fluxo de dados por push. Os itens de ação foram categorizados com base na função que executa a configuração e no componente que está sendo configurado. Como você pode ver, antes de começar a enviar notificações por push com **[!DNL Adobe Journey Optimizer]** , é necessário garantir que as configurações e integrações estejam em vigor no aplicativo móvel, **[!DNL Adobe Launch]** e **[!DNL Adobe Experience Platform]**.

![](assets/user-flow.png)

As etapas detalhadas para configurar o canal de push e ativar as notificações por push em [!DNL Journey Optimizer] estão disponíveis em [esta página](push-configuration.md).