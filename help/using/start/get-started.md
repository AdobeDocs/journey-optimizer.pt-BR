---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: Descubra os principais recursos e casos de uso do Adobe Journey Optimizer
feature: Get Started
topic: Content Management
role: User
level: Beginner
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: db3c87d10469550eb30224c932344ff1e3ae1767
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 86%

---

# Introdução ao Journey Optimizer {#cjm-gs}

## O que é o [!DNL Adobe Journey Optimizer]?{#about-cjm}

O [!DNL Adobe Journey Optimizer] ajuda as empresas a fornecer experiências conectadas, contextuais e personalizadas aos clientes. A jornada do cliente é todo o processo de interação de clientes com a marca, desde o primeiro contato até a sua saída. Ela começa com a fase de percepção, onde o cliente aprende sobre a marca e começa a se envolver. O cliente interagirá ainda mais com a marca, visitará sites online e locais físicos e fará compras, enviará mensagens ou fará resenhas.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e combina um perfil do cliente em tempo real unificado, uma estrutura aberta de priorização de API, um Offer Decisioning centralizado, além de inteligência artificial (IA) e aprendizado de máquina (ML) para personalização e otimização. O Journey Optimizer permite que as marcas determinem de forma inteligente a próxima melhor interação com escala, velocidade e flexibilidade durante toda a jornada do cliente. Com o [!DNL Adobe Journey Optimizer], as empresas podem criar e entregar campanhas de marketing agendadas (como promoções semanais para uma loja de varejo) e comunicações individuais personalizadas (como uma notificação por push sobre um item que um cliente de aplicativo de fidelidade tenha visto e que estava anteriormente indisponível), tudo no mesmo aplicativo.

➡️ [Descobrir Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=pt-BR){target="_blank"} (vídeo)


<!-- Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.-->


## Casos de uso {#use-cases}

* Os profissionais de marketing podem usar o [!DNL Adobe Journey Optimizer] para enviar comunicações individualizadas, bem como comunicações em lote baseadas em públicos-alvo. Por exemplo, uma loja de roupas normalmente envia pesquisas pós-compra para todos os clientes que compraram produtos na última semana. Devido às intempéries, alguns carregamentos sofreram atrasos. Ao ver quais clientes não receberam suas remessas, a loja de roupas pode excluir essas pessoas do envio agendado da pesquisa de satisfação do cliente e, em vez disso, enviar um email personalizado pedindo desculpas pelo atraso e oferecendo um código de desconto com recomendações de produto baseadas em suas compras anteriores.

  Os profissionais de marketing também podem usar o aplicativo para enviar comunicações em tempo real baseadas em comportamento. Por exemplo, o mesmo varejista poderia engajar em tempo real um(a) cliente fiel que entra no estacionamento da loja, enviando uma notificação por push sobre um suéter do seu tamanho que está de volta ao estoque.

* Os não profissionais de marketing, como as equipes de operações e suporte ao cliente envolvidas na experiência do cliente, podem usar o [!DNL Adobe Journey Optimizer] para gerenciar várias tarefas, como notificações operacionais ou até mesmo para monitorar o processo de integração de clientes. Pense por exemplo, um parque de diversões onde os visitantes baixam um aplicativo móvel como parte de sua experiência no parque. A equipe de manutenção pode usar o [!DNL Adobe Journey Optimizer] para notificar os visitantes sobre as atrações que estão fechadas atualmente devido à manutenção.

## Principais recursos {#key-capabilities}

O [!DNL Adobe Journey Optimizer] é um aplicativo ágil e escalonável para a criação e o fornecimento de experiências personalizadas, conectadas e oportunas ao cliente por meio de qualquer aplicativo, dispositivo ou canal.

![](assets/ajo-capabilities.png)

Os principais recursos incluem:

* **Insights e envolvimentos do cliente em tempo real** — um perfil integrado usa dados ao vivo de todas as fontes nos pontos de contato do cliente, incluindo dados comportamentais, transacionais, financeiros e operacionais para otimizar experiências pessoais e contextuais para os clientes em seu tempo.

* **Orquestração e execução modernas do Omnichannel** — uma tela única na qual se pode harmonizar e otimizar a jornada do cliente para um equilíbrio entre o engajamento do cliente e o alcance de marketing, ajudando as marcas a agregar mais valor ao longo do ciclo de vida do cliente. As jornadas do cliente criadas no [!DNL Adobe Journey Optimizer] podem ser dinâmicas e baseadas em eventos para ajudar as marcas a reagir a sinais em tempo real, bem como conectar essas interações com campanhas programadas, para que sejam tomadas as decisões corretas com respeito a quais comunicações devem ser enviadas a um cliente, quando e por quais canais.

* **Decisão e personalização inteligentes** – as marcas podem aplicar decisões centralizadas e incorporar inteligência artificial e aprendizado de máquina para configurar insights preditivos pela experiência do cliente, facilitando a automação das decisões e a otimização da experiência em escala. O serviço de decisão possibilita ofertas centralizadas em canais em escala por meio do [!DNL Adobe Journey Optimizer].


>[!NOTE]
>
>* Os componentes e recursos disponíveis no ambiente dependem das [permissões](../administration/permissions.md) e do [pacote de licenciamento](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Em caso de dúvida, entre em contato com o(a) gerente de sucesso do cliente da Adobe ou com o(a) representante da Adobe.
>
>* As diretrizes e procedimentos gerais de privacidade da Adobe Experience Cloud se aplicam ao [!DNL Journey Optimizer]. [Saiba mais sobre a privacidade da Adobe Experience Cloud](https://www.adobe.com/br/privacy/experience-cloud.html){target="_blank"}.




## Arquitetura {#architecture}

Entenda a arquitetura básica do [!DNL Adobe Journey Optimizer], os pontos de integração e a relação entre [!DNL Journey Optimizer] e [!DNL Experience Platform] no diagrama abaixo.

O Adobe Experience Platform é uma base de dados poderosa, flexível, aberta e centralizada que coleta, padroniza, governa, aplica insights de IA e unifica dados para oferecer clientes digitais relevantes e relevantes
experiências.

![](assets/ajo-aep-architecture-diagram.png){width="70%" zoomable="yes"}

Quatro aplicativos são criados nativamente no Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics e Adobe Mix Modeler.

A funcionalidade e os serviços principais da Journey Optimizer operam a partir dos componentes essenciais da Adobe Experience Platform, que incluem o Perfil do cliente em tempo real. Embora o Journey Optimizer funcione perfeitamente e seja interoperável com a Real-Time CDP e o Customer Journey Analytics, ele pode
também funcionam de forma independente como um aplicativo independente.

![](assets/ajo-architecture-diagram.png){width="70%" zoomable="yes"}



>[!MORELIKETHIS]
>
>* [Etapas principais para iniciar](quick-start.md)
>* [Criar jornadas e enviar mensagens](../building-journeys/journey-gs.md)
>* [Relatórios em tempo real](../reports/live-report.md)
>* [Visão geral sobre a segurança do Journey Optimizer](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF)
