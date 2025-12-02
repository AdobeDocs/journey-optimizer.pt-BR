---
solution: Journey Optimizer
product: journey optimizer
title: Gerar texto com o Assistente de IA
description: Saiba como gerar conteúdo de texto com o Assistente de IA no Journey Optimizer.
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
source-git-commit: b70911f1f1fa00154729b5b88517233b67a377cb
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 2%

---

# Gerar texto com o Assistente de IA {#generative-text}

>[!IMPORTANT]
>
>Antes de começar a usar esse recurso, consulte as [Medidas de proteção e limitações](gs-generative.md#generative-guardrails) relacionadas.
></br>
>
>Você deve concordar com um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html?lang=pt-BR) antes de usar o Assistente de IA no Journey Optimizer. Para obter mais informações, entre em contato com o representante da Adobe.

Use o Assistente de IA no Journey Optimizer para gerar conteúdo de texto envolvente que repercuta com seu público-alvo. Não importa se você precisa aprimorar a cópia de email, criar conteúdo atraente na Web, criar texto de página de aterrissagem persuasivo, escrever mensagens de notificação por push ou redigir mensagens SMS: o Assistente de IA ajuda a fornecer texto impactante.

## Para Email e Canais da Web {#email-web-channels}

O Assistente de IA pode gerar conteúdo de texto de alta qualidade para suas campanhas de email, experiências da Web e páginas de aterrissagem. Esse recurso permite criar mensagens atraentes na marca que se conectam com seu público-alvo em pontos de contato digitais.

### Acessar e configurar {#access-configure}

Antes de começar a gerar conteúdo de texto com o AI Assistant, será necessário configurar a campanha ou jornada e acessar o editor de conteúdo. Siga estas etapas para preparar seu espaço de trabalho e abrir o painel Assistente de IA.

1. Crie e configure sua campanha ou jornada:

   * **Email**: depois de criar e configurar sua campanha de email, clique em **[!UICONTROL Editar conteúdo]**. [Saiba mais](../email/create-email.md)
   * **Web**: depois de criar e configurar sua página da Web, clique em **[!UICONTROL Editar página da Web]**. [Saiba mais](../web/create-web.md)
   * **Página de aterrissagem**: depois de criar e configurar sua página de aterrissagem, clique em **[!UICONTROL Abrir designer]**. [Saiba mais](../landing-pages/create-lp.md)

1. Selecione um **[!UICONTROL Componente de texto]** para segmentar apenas um conteúdo específico e acessar o menu do **[!UICONTROL Assistente de IA]** (ou **[!UICONTROL Mostrar Assistente de IA]** para Web).

   ![Componente de texto selecionado com o menu do Assistente de IA aberto](assets/text-genai-1.png){zoomable="yes"}

### Gerar conteúdo {#generate-content}

Saiba como criar solicitações claras, configurações de ajuste e gerar texto personalizado usando o Assistente de IA, garantindo que suas mensagens se alinhem às suas metas de marca e comunicação.

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo selecionado.

1. Selecione sua **[!UICONTROL Marca]** para garantir que o conteúdo gerado por IA esteja alinhado às especificações da sua marca. [Saiba mais](brands.md) sobre marcas.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![Painel de geração de texto do Assistente de IA com campo Prompt e seletor de Marca](assets/text-genai-2.png){zoomable="yes"}

1. Personalize seu prompt com a opção **[!UICONTROL Configurações de texto]**:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idiomas]**: escolha o idioma do conteúdo gerado.
   * **[!UICONTROL Tone]**: o tom deve repercutir na audiência. Se você deseja parecer informativo, divertido ou persuasivo, o Assistente de IA pode adaptar a mensagem de acordo.
   * **Comprimento do texto**: use o controle deslizante para selecionar o comprimento desejado do texto.

   ![Configurações de texto expandidas mostrando opções](assets/text-genai-4.png){zoomable="yes"}

1. No menu **[!UICONTROL Ativos de marca]**, clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer o Assistente de IA de contexto adicional ou selecione um ativo carregado anteriormente.

   Os arquivos carregados anteriormente estão disponíveis no menu suspenso **[!UICONTROL Ativos de marca carregados]**. Basta alternar os ativos que deseja incluir na geração.

   ![Menu suspenso de ativos da marca](assets/text-genai-3.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

### Refinar e finalizar {#refine-finalize}

Saiba como revisar o texto gerado, fazer refinamentos e aplicar personalização para finalizar seu conteúdo, criando mensagens sofisticadas e envolventes prontas para entrega.

1. Navegue pelas **[!UICONTROL Variações]** geradas.

   Clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada ou clique em **[!UICONTROL Aplicar]** para substituir o conteúdo atual.

1. Clique no ícone de porcentagem para exibir sua **[!UICONTROL Pontuação de alinhamento da marca]** e identificar quaisquer desalinhamentos com sua marca.

   Saiba mais sobre [Pontuação de alinhamento da marca](brands-score.md).

   ![Variações de texto geradas com a Pontuação de alinhamento da marca](assets/text-genai-6.png){zoomable="yes"}

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Refrase]**: reescreva a mensagem preservando seu significado. Essa opção ajuda a gerar texto alternativo, melhorar o fluxo ou ajustar o estilo sem alterar a mensagem principal.

   * **[!UICONTROL Usar linguagem mais simples]**: use o AI Assistant para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   * **[!UICONTROL Alterar tom]**: ajuste o tom da mensagem para corresponder melhor ao seu estilo de comunicação, ou seja, tornando-a mais amigável, profissional, urgente ou inspiradora.

   * **[!UICONTROL Alterar estratégia de comunicação]**: modifique a abordagem de mensagens com base em seus objetivos, como criar urgência ou enfatizar o apelo interessante.

   ![Refinar menu de opções](assets/text-genai-5.png){zoomable="yes"}

1. Abra a guia **[!UICONTROL Alinhamento da marca]** para ver como o seu conteúdo se alinha às suas [diretrizes da marca](brands.md).

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

1. Revise e ative o conteúdo:
   * **Email**: quando tiver definido seu conteúdo, público-alvo e agendamento, você estará pronto para preparar sua campanha de email. [Saiba mais](../campaigns/review-activate-campaign.md)
   * **Web**: depois de definir suas configurações de campanha da Web e editar seu conteúdo conforme desejado, você pode revisar e ativar sua campanha da Web. [Saiba mais](../web/create-web.md#activate-web-campaign)
   * **Página de aterrissagem**: quando a página de aterrissagem estiver pronta, você poderá publicá-la para disponibilizá-la para uso em uma mensagem. [Saiba mais](../landing-pages/create-lp.md#publish-landing-page)

## Para canais móveis {#mobile-channels}

O Assistente de IA pode gerar conteúdo de texto atraente para suas notificações por push e mensagens SMS, ajudando você a criar comunicações móveis envolventes que repercutem com seu público-alvo em todos os pontos de contato móveis.

### Acessar e configurar {#mobile-access-configure}

Antes de começar a gerar texto com o Assistente de IA para canais móveis, você deve configurar sua campanha e acessar o Assistente de IA. O método de acesso varia um pouco entre as notificações por push e as mensagens SMS.

1. Crie e configure sua campanha via celular:
   * **Notificações por push**: depois de criar e configurar sua campanha de notificação por push, clique em **[!UICONTROL Editar conteúdo]**. [Saiba mais](../push/create-push.md)
   * **SMS**: depois de criar e configurar sua campanha de SMS, clique em **[!UICONTROL Editar conteúdo]**. [Saiba mais](../sms/create-sms.md)

1. Preencha os **[!UICONTROL detalhes Básicos]** da sua campanha. Depois de concluído, clique em **[!UICONTROL Editar conteúdo]**.

1. Personalize a mensagem conforme necessário:
   * **Notificações por push**: [Saiba mais](../push/design-push.md)
   * **SMS**: [Saiba mais](../sms/create-sms.md)

1. Acessar o assistente de IA:
   * **Para notificações por push**: clique no menu **[!UICONTROL Editar texto com o Assistente de IA]** ao lado dos campos **[!UICONTROL Título]** ou **[!UICONTROL Mensagem]**. Você também pode acessar diretamente o menu **Assistente de IA**.

     ![Tela de composição de notificação por push com o botão Editar texto com o Assistente de IA](assets/push-text-1.png){zoomable="yes"}

   * **Para SMS**: clique no menu **[!UICONTROL Editar texto com o Assistente de IA]** ao lado da **[!UICONTROL Mensagem]** ou acesse o menu **[!UICONTROL Mostrar Assistente de IA]**.

     ![Editor de mensagens SMS com o painel Assistente de IA aberto](assets/sms-genai-1.png){zoomable="yes"}

### Gerar conteúdo {#mobile-generate-content}

Depois de acessar o Assistente de IA, você pode definir as configurações de geração para criar conteúdo móvel que corresponda às suas metas de marca e campanha. Personalize parâmetros de texto, adicione ativos de marca e forneça prompts para orientar a IA na geração de variações relevantes.

1. Selecione sua **[!UICONTROL Marca]** para garantir que o conteúdo gerado por IA esteja alinhado às especificações da sua marca. [Saiba mais](brands.md) sobre marcas.

   Observe que o recurso Marcas é lançado como um beta privado e estará progressivamente disponível para todos os clientes em versões futuras.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas. [Saiba mais sobre as práticas recomendadas do prompt](ai-assistant-prompting-guide.md)

   ![Assistente de IA com campo de prompt e opções](assets/push-genai-2.png){zoomable="yes"}

1. **Para notificação por push**, escolha qual campo você deseja gerar: Título e/ou Mensagem.

1. Personalize seu prompt com a opção **[!UICONTROL Configurações de texto]**:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idiomas]**: escolha o idioma do conteúdo gerado.
   * **[!UICONTROL Tone]**: o tom deve repercutir na audiência. Se você deseja parecer informativo, divertido ou persuasivo, o Assistente de IA pode adaptar a mensagem de acordo.

     ![Painel de configurações de texto](assets/push-genai-4.png){zoomable="yes"}

1. No menu **[!UICONTROL Conteúdo de referência]**, clique em **[!UICONTROL Carregar arquivo]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer o Assistente de IA de contexto adicional ou selecione um que tenha sido carregado anteriormente.

   Os arquivos carregados anteriormente estão disponíveis no menu suspenso **[!UICONTROL Conteúdo de referência carregado]**. Basta alternar os ativos que deseja incluir na geração.

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

### Refinar e finalizar {#mobile-refine-finalize}

Depois de gerar variações de texto para suas mensagens móveis, você pode ajustar os resultados para garantir que eles atendam aos seus requisitos exatos. Revise o alinhamento da marca, ajuste o tom e o idioma e prepare o conteúdo para ativação.

1. Após a geração, navegue pelas **[!UICONTROL Variações]**.

1. Clique no ícone de porcentagem para exibir sua **[!UICONTROL Pontuação de alinhamento da marca]** e identificar quaisquer desalinhamentos com sua marca.

   Saiba mais sobre [Pontuação de alinhamento da marca](brands-score.md).

   ![Variações de texto geradas com a Pontuação de alinhamento da marca](assets/push-genai-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada ou clique em **[!UICONTROL Aplicar]** para substituir o conteúdo atual.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Refrase]**: reescreva a mensagem preservando seu significado. Essa opção ajuda a gerar texto alternativo, melhorar o fluxo ou ajustar o estilo sem alterar a mensagem principal.

   * **[!UICONTROL Usar linguagem mais simples]**: use o AI Assistant para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   * **[!UICONTROL Traduzir]**: simplifique seu idioma para garantir clareza e acessibilidade para um público-alvo maior.

   * **[!UICONTROL Alterar tom]**: ajuste o tom da mensagem para corresponder melhor ao seu estilo de comunicação, ou seja, tornando-a mais amigável, profissional, urgente ou inspiradora.

   * **[!UICONTROL Alterar estratégia de comunicação]**: modifique a abordagem de mensagens com base em seus objetivos, como criar urgência ou enfatizar o apelo interessante.

     ![Refinar menu](assets/push-genai-6.png){zoomable="yes"}

1. Abra a guia **[!UICONTROL Alinhamento da marca]** para ver como o seu conteúdo se alinha às suas [diretrizes da marca](brands.md).

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha via celular. [Saiba mais](../campaigns/review-activate-campaign.md)

