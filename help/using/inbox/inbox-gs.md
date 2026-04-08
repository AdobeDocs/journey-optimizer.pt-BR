---
title: Criar uma caixa de entrada
description: Comece a usar a Caixa de entrada no Adobe Journey Optimizer para fornecer mensagens persistentes e não intrusivas aos usuários.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: 2eb2e99e654516fc13a7f98125f48e7e8f672ee3
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Introdução à Caixa de entrada {#inbox-gs}

A caixa de entrada fornece mensagens persistentes de baixo atrito em um local dentro do aplicativo móvel ou site. O aplicativo e o push podem desaparecer após um deslizamento ou toque; a Caixa de entrada mantém as mensagens disponíveis para que as pessoas possam abrir, ler e agir de acordo com elas quando for adequado.

A caixa de entrada é criada no canal Cartões de conteúdo e adiciona:

* **Mensagens persistentes**: o conteúdo permanece na caixa de entrada até que você o remova ou expire, para que os usuários possam retornar a ele depois de fechar uma notificação ou sair do aplicativo.
* **Local centralizado**: uma única caixa de correio no seu aplicativo ou site para mensagens de marketing relevantes.
* **Implementação flexível**: use o contêiner pronto da caixa de entrada ou personalize a experiência em sua própria interface do usuário.
* **Status de Leitura**: as mensagens podem ser marcadas como lidas ou não lidas no dispositivo em que estão abertas.

## Guia de início rápido

Siga estas etapas para configurar e usar a Caixa de entrada:

1. [Configurar Adobe Journey Optimizer](inbox-configuration.md)

   Adicione uma configuração de canal da **Caixa de entrada** em **Configurações de canal** para que a Journey Optimizer saiba onde e como a caixa de entrada é executada (página da Web, regra ou superfície de aplicativo móvel).

1. [Criar sua Caixa de entrada no Journey Optimizer](inbox-create.md)

   Crie uma campanha que use a ação **Cartão de conteúdo** e escolha **Caixa de entrada** como o local de entrega — agendado na interface ou acionado pela API.

1. [Projetar a Caixa de entrada](inbox-design.md)

   Escolha modelos de caixa de entrada e liste ou layouts expandidos para que as mensagens correspondam à sua marca e UX.

1. [Crie seu cartão Conteúdo e vincule-o à sua Caixa de entrada](../content-card/create-content-card.md)

   Crie o conteúdo do cartão no designer, finalize as opções específicas da Caixa de entrada e ative a campanha para que as mensagens cheguem à caixa de entrada.

## Recursos adicionais

* [Buscar e exibir caixa de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/): carregue mensagens da caixa de entrada do Journey Optimizer e renderize a interface do usuário da Caixa de Entrada no Android (documentação do Adobe Developer).
* [Personalização da Caixa de Entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/): ajuste o layout, o estilo e o comportamento de interação da caixa de entrada para seu aplicativo Android (documentação do Adobe Developer).
* [Acompanhamento de Eventos da Caixa de Entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/): assine retornos de chamada da caixa de entrada para ações do usuário e atualizações do ciclo de vida no Android (documentação do Adobe Developer).
