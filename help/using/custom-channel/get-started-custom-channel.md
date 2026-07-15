---
title: Introdução a canais personalizados
description: Saiba como usar o  [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer]  e usá-lo em campanhas, jornadas e campanhas orquestradas.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Introdução a canais personalizados {#get-started-custom-channel}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

A capacidade **Canais personalizados** do [!DNL Journey Optimizer] permite que você traga qualquer canal de saída para o [!DNL Journey Optimizer] para que possa usá-lo em campanhas, jornadas e campanhas orquestradas, exatamente como qualquer canal nativo. Usando o **Construtor de Canais**, os administradores podem criar e configurar novos canais sem envolvimento de engenharia, e os profissionais de marketing podem começar imediatamente a usá-los para se comunicar com os clientes.

## Que problema ele resolve? {#why-custom-channels}

O [!DNL Journey Optimizer] oferece suporte nativo a email, SMS, notificações por push, WhatsApp, LINE e outros canais. No entanto, muitas organizações usam plataformas de mensagens que não são integradas nativamente — como WeChat, Kakao Talk, Messenger ou um provedor externo — e desejam usá-las no [!DNL Journey Optimizer] para orquestração e criação de campanha, sem deixar de atender aos seus próprios fornecedores.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

Os canais personalizados preenchem essa lacuna: eles permitem usar qualquer ponto de extremidade HTTP de saída como um canal [!DNL Journey Optimizer] completo, desbloqueando:

* **Recursos completos do canal** - Otimização (experimentação e direcionamento de conteúdo), relatórios e monitoramento OOTB, imposição de consentimento e governança e fragmentos de expressão. <!--Multilingual and business rules are planned for a future release.-->
* **Orquestração unificada** - Gerencie todos os seus canais de mensagens em um único local, independentemente do provedor de entrega subjacente.
* **Configuração sem código** - Os administradores configuram o canal por meio da interface do usuário do Construtor de Canais; não é necessário nenhum esforço de engenharia ou código personalizado.

## Canal personalizado versus ações personalizadas {#custom-channel-vs-custom-action}

Se você já tiver usado [ações personalizadas](../action/action.md) em [!DNL Journey Optimizer] jornadas antes, os canais personalizados abordarão um conjunto diferente de casos de uso.

**Use canais personalizados quando** você precisar enviar mensagens para usuários finais por meio de uma plataforma que não tem suporte nativo no [!DNL Journey Optimizer], como o WeChat, o Kakao Talk ou um gateway de mensagens personalizado. Os canais personalizados estão disponíveis em campanhas, jornadas, campanhas orquestradas e suporte:

* Personalização completa por meio do editor de personalização, semelhante aos canais de saída nativos
* Editor de conteúdo visual/de formulário, visualização e prova
* Experimentação e direcionamento de conteúdo
* Emissão de relatórios e monitoramento OOTB
* Várias credenciais de API e configurações de canal
* RBAC/ABAC

Os canais personalizados oferecem suporte a POST como o único método HTTP.

**Use ações personalizadas quando** precisar recuperar dados ou enviar informações para um sistema externo — como uma central de atendimento, uma plataforma de log ou um banco de dados offline — como uma etapa em uma jornada. As ações personalizadas estão disponíveis somente no jornada e oferecem suporte aos métodos GET, PUT e POST.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>Como recomendação geral, use canais personalizados para casos de uso de canal em que você está enviando mensagens para usuários finais. Para outros casos de uso semelhantes a conectores necessários no jornada, como recuperar dados ou acionar sistemas externos, você pode continuar a usar ações personalizadas.

## Casos de uso {#use-cases}

Os canais personalizados são ideais para:

* **Plataformas de mensagens sem suporte** - Canais como WeChat, Kakao Talk, Messenger, Telegram ou serviços de mensagens regionais que não têm um canal [!DNL Journey Optimizer] nativo.
* **Provedores de entrega personalizados** - Organizações que investiram em um provedor externo que desejam continuar usando para a entrega de mensagens, mas preferem usar o [!DNL Journey Optimizer] para orquestração, personalização e gerenciamento de campanhas.
* **Canais herdados** - Gateways de mensagens proprietários ou herdadas que expõem um ponto de extremidade HTTP.
* **Canais específicos do setor** - Mensagens seguras para serviços de saúde, sistemas de alerta bancário ou serviços de notificação do governo.

## Como funciona {#how-it-works}

A configuração e o uso de um canal personalizado seguem os principais estágios abaixo:

1. **Configurar** (Administrador) - Um administrador cria um canal personalizado no **Construtor de Canais**, definindo o ponto de extremidade, a autenticação, a política de limitação e a estrutura de conteúdo da mensagem. Em seguida, uma configuração de canal é criada e vinculada ao canal personalizado. [Saiba mais](configure-custom-channel.md)
1. **Criar** (Profissional de marketing) - Um profissional de marketing adiciona o canal personalizado a uma campanha, campanha ou campanha orquestrada, seleciona uma configuração de canal e cria a carga da mensagem usando o editor de personalização do [!DNL Journey Optimizer]. [Saiba mais](create-custom-experience.md)
1. **Enviar** - Quando um perfil é qualificado, [!DNL Journey Optimizer] envia a carga personalizada para o ponto de extremidade configurado. O sistema externo processa a chamada e entrega a mensagem.
1. **Monitorar** (Administrador/Profissional de marketing) - Administradores e profissionais de marketing podem monitorar o desempenho e a confiabilidade do canal personalizado por meio dos painéis de monitoramento e relatórios de [!DNL Journey Optimizer]. [Saiba mais](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
