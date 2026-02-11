---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a canais de comunicação no [!DNL Adobe Journey Optimizer]
description: Saiba como trabalhar com canais de comunicação do  [!DNL Adobe Journey Optimizer] .
role: User
level: Beginner
exl-id: 5779bcee-49c0-4ffa-9b17-329ef458c96a
source-git-commit: 6a32a60f153ff4880ce974e77bc11eed1e20a7c7
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 100%

---


# Introdução aos canais do [!DNL Adobe Journey Optimizer] {#get-started-email}

No cenário de marketing dinâmico de hoje, alcançar efetivamente seu público-alvo em várias plataformas é essencial para criar relacionamentos duradouros e impulsionar o engajamento. Esta seção fornece uma visão abrangente dos canais de comunicação disponíveis no [!DNL Adobe Journey Optimizer], ajudando a entender como utilizar cada canal de forma eficaz em suas estratégias de marketing.

O Adobe Journey Optimizer oferece uma variedade de canais nativos para interagir com seu público-alvo de maneira eficaz. Você pode combinar entregas de mensagens de saída e experiências de entrada.

## Canais de saída para entrega de mensagens {#outbound-channels}

Os canais de saída para entrega de mensagens envolvem o envio de mensagens para clientes sem interação prévia. Os exemplos incluem campanhas de email e notificações por push, nos quais você entra em contato de forma proativa com seu público-alvo. No [!DNL Adobe Journey Optimizer], os canais de saída com suporte são:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Canal de email

Descubra como criar, configurar e otimizar campanhas de email, incluindo personalização, capacidade de entrega e práticas recomendadas de conformidade.

[Saiba mais sobre o canal de email](../../rp_landing_pages/email-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Canal de notificação por push

Saiba como criar, configurar e enviar notificações por push para iOS e Android, incluindo opções avançadas, como notificações silenciosas e modo de entrega rápida.

[Saiba mais sobre notificações por push](../../rp_landing_pages/push-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/comment-dots.svg)

Mensagens por SMS/MMS/RCS

Entenda como criar, gerenciar e configurar mensagens por SMS, MMS e RCS para fins de marketing e transacionais, incluindo conformidade e personalização.

[Saiba mais sobre mensagens por SMS/MMS/RCS](../../rp_landing_pages/sms-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/mail-bulk.svg)

Campanhas de correspondência direta

Descubra como criar e gerenciar campanhas de correspondência direta, incluindo a exportação de arquivos de extração para provedores externos e a garantia de conformidade com o consentimento do usuário.

[Saiba mais sobre campanhas de correspondência direta](../../rp_landing_pages/direct-mail-landing-page.md)
:::

::::

## Experiências do aplicativo móvel e da Web {#inbound-channels}

Com experiências de entrada de aplicativos móveis e da Web, os clientes iniciam interações. Os exemplos incluem mensagens no aplicativo e experiências baseadas na web, as quais permitem que os usuários interajam com o conteúdo do seu jeito. No [!DNL Adobe Journey Optimizer], os canais de entrada com suporte são:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/mobile.svg)

Mensagens no aplicativo

Aprenda a configurar, projetar e personalizar notificações no aplicativo para plataformas móveis e da web, a fim de engajar os públicos-alvo dentro de aplicativos.

[Saiba mais sobre mensagens no aplicativo](../../rp_landing_pages/in-app-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/globe.svg)

Web

Saiba como criar, configurar e personalizar experiências na web e integrar canais da web a estratégias de marketing de saída.

[Saiba mais sobre o canal da web](../../rp_landing_pages/web-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Experiência baseada em código

Utilize as experiências baseadas em código para fornecer conteúdo personalizado em plataformas digitais, usando SDKs e APIs.

[Saiba mais sobre a experiência baseada em código](../../rp_landing_pages/code-based-experience-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/id-card.svg)

Cartões de conteúdo

Descubra como configurar, criar e projetar cartões de conteúdo para mensagens envolventes e personalizadas em aplicativos móveis e sites.

[Saiba mais sobre a experiência baseada em código](../../rp_landing_pages/content-card-landing-page.md)
:::

::::


## Recursos adicionais

- **[Mensagens do WhatsApp](../../rp_landing_pages/whatsapp-landing-page.md)**: saiba como integrar e usar mensagens do WhatsApp por meio da API da nuvem do Meta para campanhas de comunicação personalizadas e compatíveis.
- **[Mensagens do LINE](../../rp_landing_pages/line-landing-page.md)**: descubra como configurar, criar e personalizar mensagens do LINE para uma comunicação eficaz em campanhas e jornadas.

## Canais em jornadas e campanhas {#channels}

No Adobe Journey Optimizer, é possível usar os canais de comunicação em dois contextos principais:

- **Jornadas**: crie experiências do cliente ininterruptas em vários pontos de contato. Automatize interações com base no comportamento e nas preferências do usuário, garantindo comunicações oportunas e relevantes que orientam os usuários pela jornada com a sua marca. [Saiba como criar e executar uma jornada](../building-journeys/journey-gs.md).

- **Campanhas**: implemente campanhas de marketing específicas que utilizem um determinado canal para atingir objetivos específicos. Tanto na promoção de um novo produto quanto no impulsionamento de vendas sazonais, as campanhas permitem que você crie estratégias de mensagens focadas e adequadas ao seu público-alvo. [Saiba como criar e executar uma campanha](../campaigns/get-started-with-campaigns.md).

A tabela abaixo mostra a disponibilidade de cada canal em diferentes jornadas e campanhas, indicando onde eles são compatíveis.

| Canal | Jornadas | Campanhas de ação (Marketing) | Campanhas de ação (Transacional) | Campanhas acionadas por API | Campanhas orquestradas |
|----------------------|----------|------------------------------|----------------------------------|-------------------------|------------------------|
| Email | ✅ | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ | ✅ |
| Notificações por push | ✅ | ✅ | ✅ | ✅ | ✅ |
| No aplicativo | ✅ | ✅ | — | — | — |
| Correspondência direta | ✅ | ✅ | — | — | ✅ |
| Web | ✅ | ✅ | — | — | — |
| Experiência baseada em código | ✅ | ✅ | — | — | — |
| Cartões de conteúdo | ✅ | ✅ | — | — | — |
| WhatsApp | ✅ | ✅ | — | — | — |
| Linha | ✅ | ✅ | — | — | — |
