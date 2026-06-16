---
title: Criar uma caixa de entrada
description: Comece a usar a Caixa de entrada no Adobe Journey Optimizer para fornecer mensagens persistentes e não intrusivas aos usuários.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# Introdução à caixa de entrada {#inbox-gs}

>[!BEGINSHADEBOX]

**Nesta página:** Entenda como o canal da Caixa de Entrada mantém as mensagens de marketing em um local persistente dentro do seu aplicativo ou site, para que os usuários possam voltar a lê-las e interagir com elas da maneira que desejarem.

>[!ENDSHADEBOX]

A caixa de entrada fornece mensagens persistentes de baixo atrito em um local dentro do aplicativo móvel ou site. As mensagens no aplicativo e push podem desaparecer após um deslizamento ou toque; a Caixa de entrada mantém as mensagens disponíveis para que as pessoas possam abrir, ler e agir quando quiserem.

A Caixa de entrada se baseia no canal Cartões de conteúdo e adiciona:

* **Mensagens persistentes**: o conteúdo permanece na caixa de entrada até que você o remova ou expire, para que os usuários possam retornar a ele depois de fechar uma notificação ou sair do aplicativo.
* **Local centralizado**: uma única caixa de correio no seu aplicativo ou site para mensagens de marketing relevantes.
* **Implementação flexível**: use o container pronto da caixa de entrada ou personalize a experiência em sua própria interface.
* **Status de leitura**: as mensagens podem ser marcadas como lidas ou não lidas no dispositivo em que estão abertas.

## Guia de início rápido

Siga estas etapas para configurar e usar a Caixa de entrada:

1. [Configurar o Adobe Journey Optimizer](inbox-configuration.md)

   Adicione uma configuração de canal da **Caixa de entrada** em **Configurações de canais** para que o Journey Optimizer saiba onde e como a caixa de entrada é executada (página da Web, regra ou superfície de aplicativo móvel).

1. [Criar sua Caixa de entrada no Journey Optimizer](inbox-create.md)

   Crie uma campanha que use a ação **Cartão de conteúdo** e escolha **Caixa de entrada** como o local de entrega — agendado na interface ou acionado por API.

1. [Criar uma Caixa de entrada](inbox-design.md)

   Escolha modelos de caixa de entrada e layouts expandidos ou em lista para que as mensagens correspondam à sua marca e à sua UX.

1. [Crie seu Cartão de conteúdo e vincule-o à sua Caixa de entrada](../content-card/create-content-card.md)

   Crie cartão de conteúdo no designer, finalize as opções específicas da Caixa de entrada e ative a campanha para que as mensagens cheguem à caixa de entrada.

## Recursos adicionais

* [Interface da Caixa de entrada (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS): requisitos, superfície da API pública, configurações da caixa de entrada e links para tutoriais para implementar a Caixa de entrada do Journey Optimizer em um aplicativo iOS com o Adobe Experience Platform Mobile SDK (iOS 15 ou mais recente, Xcode 15 ou mais recente, Swift 5.1 ou mais recente).

* [Buscar e exibir caixa de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox): carregue mensagens da caixa de entrada do Journey Optimizer e renderize a interface da Caixa de entrada no Android (documentação do Adobe Developer).

* [Personalização da Caixa de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox): ajuste o layout, o estilo e o comportamento de interação da caixa de entrada para seu aplicativo Android (documentação do Adobe Developer).

* [Acompanhamento de eventos da Caixa de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events): assine retornos de chamada da caixa de entrada para ações do usuário e atualizações do ciclo de vida no Android (documentação do Adobe Developer).
