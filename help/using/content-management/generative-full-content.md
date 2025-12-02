---
solution: Journey Optimizer
product: journey optimizer
title: Gerar conteúdo completo com o Assistente de IA
description: Saiba como gerar experiências completas de conteúdo com o Assistente de IA no Journey Optimizer.
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
source-git-commit: de418dc4feefd99231155c550ad3a51e4850ee66
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 2%

---

# Gerar conteúdo completo com o Assistente de IA {#generative-full-content}

>[!IMPORTANT]
>
>Antes de começar a usar esse recurso, consulte as [Medidas de proteção e limitações](gs-generative.md#generative-guardrails) relacionadas.
></br>
>
>Você deve concordar com um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html?lang=pt-BR) antes de usar o Assistente de IA no Journey Optimizer. Para obter mais informações, entre em contato com o representante da Adobe.

Use o Assistente de IA no Journey Optimizer para gerar experiências completas de conteúdo em seus canais de email, Web, landing pages e notificação por push. O Assistente de IA ajuda você a otimizar o impacto de seus deliveries, criando conteúdo abrangente que repercuta com seu público-alvo.

## Para Email e Canais da Web {#email-web-channels}

O AI Assistant pode produzir experiências completas de conteúdo para suas campanhas de email, páginas da Web e páginas de aterrissagem, gerando texto e imagens. Essa funcionalidade robusta ajuda você a criar conteúdo atraente na marca que se conecta com seu público-alvo em todos os pontos de contato digitais.

### Acessar e configurar {#access-configure}

Antes de começar a criar conteúdo com o AI Assistant, você precisará configurar sua campanha ou jornada e abrir o editor de conteúdo. Use as etapas abaixo para preparar seu espaço de trabalho e acessar o painel Assistente de IA.

1. Crie e configure sua campanha ou jornada:
   * **Email**: depois de criar e configurar sua campanha de email, clique em **[!UICONTROL Editar conteúdo]**. [Saiba mais](../campaigns/create-campaign.md)
   * **Web**: depois de criar e configurar sua página da Web, clique em **[!UICONTROL Editar página da Web]**. [Saiba mais](../web/create-web.md)
   * **Página de aterrissagem**: depois de criar e configurar sua página de aterrissagem, clique em **[!UICONTROL Editar conteúdo]**. [Saiba mais](../landing-pages/create-lp.md)

1. Personalize seu layout conforme necessário e acesse o menu do **[!UICONTROL Assistente de IA]**.

   ![Painel do Assistente de IA mostrando a seleção da marca e o campo de prompt](assets/full-email-1.png){zoomable="yes"}

### Gerar conteúdo {#generate-content}

Com o AI Assistant aberto, agora é possível definir as configurações de geração para criar conteúdo que corresponda às suas metas de marca e campanha. Personalize parâmetros de texto e imagem, adicione ativos de marca e forneça prompts para orientar a IA na geração de variações relevantes para seu público.

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo selecionado.

1. Selecione sua **[!UICONTROL Marca]** para garantir que o conteúdo gerado por IA esteja alinhado às especificações da sua marca. [Saiba mais](brands.md) sobre marcas.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas. [Saiba mais sobre as práticas recomendadas do prompt](ai-assistant-prompting-guide.md)

   ![Avisar campo com o botão Avisar Biblioteca](assets/full-email-2.png){zoomable="yes"}

1. **Para Emails**, você pode alternar as opções **[!UICONTROL Linha de assunto]** e **[!UICONTROL Pré-cabeçalho]** para incluí-los na geração de variantes.

1. Personalize seu prompt com a opção **[!UICONTROL Configurações de texto]**:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idiomas]**: escolha o idioma do conteúdo gerado.
   * **[!UICONTROL Tone]**: o tom deve repercutir na audiência. Se você deseja parecer informativo, divertido ou persuasivo, o Assistente de IA pode adaptar a mensagem de acordo.

   ![Painel de configurações de texto mostrando opções de Estratégia de comunicação, Idiomas e Tom](assets/full-email-4.png){zoomable="yes"}

1. Escolha suas **[!UICONTROL configurações de imagem]**:

   * **[!UICONTROL Tipo de conteúdo]**: categoriza a natureza do elemento visual, distinguindo entre diferentes formas de representação visual, como fotos, gráficos ou arte.
   * **[!UICONTROL Intensidade visual]**: você pode controlar o impacto da imagem ajustando sua intensidade. Uma configuração mais baixa (2) criará uma aparência mais suave e mais restrita, enquanto uma configuração mais alta (10) tornará a imagem mais vibrante e visualmente poderosa.
   * **[!UICONTROL Cor e tom]**: a aparência geral das cores em uma imagem e o humor ou atmosfera que ela transmite.
   * **[!UICONTROL Iluminação]**: refere-se ao relâmpago presente em uma imagem, que molda sua atmosfera e realça elementos específicos.
   * **[!UICONTROL Composição]**: refere-se à disposição dos elementos dentro do quadro de uma imagem

   ![Painel de configurações de imagem exibindo as opções Tipo de conteúdo, Intensidade visual, Cor e Tom, Iluminação e Composição](assets/full-email-6.png){zoomable="yes"}

1. No menu **[!UICONTROL Ativos de marca]**, clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer o Assistente de IA de contexto adicional ou selecione um ativo carregado anteriormente.

   Os arquivos carregados anteriormente estão disponíveis no menu suspenso **[!UICONTROL Ativos de marca carregados]**. Basta alternar os ativos que deseja incluir na geração.

   ![Seção de ativos da marca com o botão Carregar ativo da marca](assets/full-email-3.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

### Refinar e finalizar {#refine-finalize}

Depois de gerar variações de conteúdo, você pode ajustar os resultados para garantir que eles atendam aos seus requisitos exatos. Revise o alinhamento da marca, ajuste o tom e o idioma e prepare o conteúdo para ativação em sua campanha ou jornada.

1. Após a geração, navegue pelas **[!UICONTROL Variações]** e clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada ou **[!UICONTROL Aplicar]** para substituir o conteúdo atual.

1. Clique no ícone de porcentagem para exibir sua **[!UICONTROL Pontuação de alinhamento da marca]** e identificar quaisquer desalinhamentos com sua marca.

   Saiba mais sobre [Pontuação de alinhamento da marca](brands-score.md).

   ![Painel Pontuação de alinhamento da marca mostrando a pontuação percentual](assets/full-email-7.png){zoomable="yes"}

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Refrase]**: reescreva a mensagem preservando seu significado. Essa opção ajuda a gerar texto alternativo, melhorar o fluxo ou ajustar o estilo sem alterar a mensagem principal.

   * **[!UICONTROL Usar linguagem mais simples]**: use o AI Assistant para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   * **[!UICONTROL Alterar tom]**: ajuste o tom da mensagem para corresponder melhor ao seu estilo de comunicação, ou seja, tornando-a mais amigável, profissional, urgente ou inspiradora.

   * **[!UICONTROL Alterar estratégia de comunicação]**: modifique a abordagem de mensagens com base em seus objetivos, como criar urgência ou enfatizar o apelo interessante.

   ![Refinar opções de exibição de menu](assets/full-email-5.png){zoomable="yes"}

1. Abra a guia **[!UICONTROL Alinhamento da marca]** para ver como o seu conteúdo se alinha às suas [diretrizes da marca](brands.md).

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

1. Revise e ative o conteúdo:
   * **Email**: quando tiver definido seu conteúdo, público-alvo e agendamento, você estará pronto para preparar sua campanha de email. [Saiba mais](../campaigns/review-activate-campaign.md)
   * **Web**: depois de definir suas configurações de campanha da Web e editar seu conteúdo conforme desejado, você pode revisar e ativar sua campanha da Web. [Saiba mais](../web/create-web.md#activate-web-campaign)
   * **Página de aterrissagem**: quando a página de aterrissagem estiver pronta, você poderá publicá-la para disponibilizá-la para uso em uma mensagem. [Saiba mais](../landing-pages/create-lp.md#publish-landing-page)

## Para canais móveis {#mobile-channels}

O Assistente de IA também oferece suporte à geração de conteúdo para notificações por push em dispositivos móveis, permitindo que você crie títulos, mensagens e imagens envolventes para seus aplicativos móveis. Isso ajuda a manter uma comunicação consistente e de alta qualidade em todos os pontos de contato do cliente, incluindo dispositivos móveis.


### Acessar e configurar {#mobile-access-configure}

Para usar o Assistente de IA para notificações por push, primeiro configure sua campanha por push e abra o editor de conteúdo. As etapas abaixo guiarão você pela preparação da campanha e pelo acesso às ferramentas do Assistente de IA.

1. Depois de criar e configurar sua campanha de notificação por push, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha de notificação por push, consulte [esta página](../push/create-push.md).

1. Preencha os **[!UICONTROL detalhes Básicos]** da sua campanha. Depois de concluído, clique em **[!UICONTROL Editar conteúdo]**.

1. Personalize sua notificação por push conforme necessário. [Saiba mais](../push/design-push.md)

1. Acesse o menu **[!UICONTROL Mostrar assistente de IA]**.

   ![Editor de notificação por push com o painel do Assistente de IA aberto](assets/push-genai-full-1.png){zoomable="yes"}

### Gerar conteúdo {#mobile-generate-content}

Depois de acessar o Assistente de IA para notificações por push, você pode definir as configurações de geração para criar conteúdo móvel atraente. Defina suas preferências de texto e imagem, selecione ativos da marca e use prompts para gerar variações de notificação por push que envolvam seus usuários móveis.

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo selecionado.

1. Selecione sua **[!UICONTROL Marca]** para garantir que o conteúdo gerado por IA esteja alinhado às especificações da sua marca. [Saiba mais](brands.md) sobre marcas.

   Observe que o recurso Marcas é lançado como um beta privado e estará progressivamente disponível para todos os clientes em versões futuras.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![Assistente de IA com campo de prompt e opções](assets/push-genai-full-2.png){zoomable="yes"}

1. Escolha qual campo você deseja gerar: **[!UICONTROL Título]**, **[!UICONTROL Mensagem]** e/ou **[!UICONTROL Imagem]**.

1. Personalize seu prompt com a opção **[!UICONTROL Configurações de texto]**:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idiomas]**: escolha o idioma do conteúdo gerado.
   * **[!UICONTROL Tom]**: o tom das suas notificações por push deve repercutir no seu público-alvo. Se você deseja parecer informativo, divertido ou persuasivo, o Assistente de IA pode adaptar a mensagem de acordo.

   ![Painel de configurações de texto para notificações por push](assets/push-genai-full-3.png){zoomable="yes"}

1. Escolha suas **[!UICONTROL configurações de imagem]**:

   * **[!UICONTROL Tipo de conteúdo]**: categoriza a natureza do elemento visual, distinguindo entre diferentes formas de representação visual, como fotos, gráficos ou arte.
   * **[!UICONTROL Intensidade visual]**: você pode controlar o impacto da imagem ajustando sua intensidade. Uma configuração mais baixa (2) criará uma aparência mais suave e mais restrita, enquanto uma configuração mais alta (10) tornará a imagem mais vibrante e visualmente poderosa.
   * **[!UICONTROL Cor e tom]**: a aparência geral das cores em uma imagem e o humor ou atmosfera que ela transmite.
   * **[!UICONTROL Iluminação]**: refere-se ao relâmpago presente em uma imagem, que molda sua atmosfera e realça elementos específicos.
   * **[!UICONTROL Composição]**: refere-se à disposição dos elementos dentro do quadro de uma imagem

   ![Configurações de imagem para notificações por push](assets/push-genai-full-5.png){zoomable="yes"}

1. No menu **[!UICONTROL Ativos de marca]**, clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer o Assistente de IA de contexto adicional ou selecione um ativo carregado anteriormente.

   Os arquivos carregados anteriormente estão disponíveis no menu suspenso **[!UICONTROL Ativos de marca carregados]**. Basta alternar os ativos que deseja incluir na geração.

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

### Refinar e finalizar {#mobile-refine-finalize}

Depois de revisar as variações de notificação por push geradas, você pode aprimorar o conteúdo. Use as ferramentas de refinamento para ajustar o idioma e o tom, verificar o alinhamento da marca e personalizar o conteúdo antes de ativar a campanha de push.

1. Navegue pelas **[!UICONTROL Variações]** geradas.

1. Clique no ícone de porcentagem para exibir sua **[!UICONTROL Pontuação de alinhamento da marca]** e identificar quaisquer desalinhamentos com sua marca.

   Saiba mais sobre [Pontuação de alinhamento da marca](brands-score.md).

   ![Variações de notificação por push geradas com a Pontuação de alinhamento de marca](assets/push-genai-full-4.png){zoomable="yes"}

1. Clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada ou clique em **[!UICONTROL Aplicar]** para substituir o conteúdo atual.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Refrase]**: reescreva a mensagem preservando seu significado. Essa opção ajuda a gerar texto alternativo, melhorar o fluxo ou ajustar o estilo sem alterar a mensagem principal.

   * **[!UICONTROL Usar linguagem mais simples]**: use o AI Assistant para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   * **[!UICONTROL Alterar tom]**: ajuste o tom da mensagem para corresponder melhor ao seu estilo de comunicação, ou seja, tornando-a mais amigável, profissional, urgente ou inspiradora.

   * **[!UICONTROL Alterar estratégia de comunicação]**: modifique a abordagem de mensagens com base em seus objetivos, como criar urgência ou enfatizar o apelo interessante.

   ![Refinar opções para notificações por push](assets/push-genai-full-6.png){zoomable="yes"}

1. Abra a guia **[!UICONTROL Alinhamento da marca]** para ver como o seu conteúdo se alinha às suas [diretrizes da marca](brands.md).

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar o conteúdo da notificação por push com base nos dados dos perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de push. [Saiba mais](../campaigns/review-activate-campaign.md)

## Vídeo explicativo {#video}

Saiba como usar o Assistente de IA no Journey Optimizer para gerar experiências completas de conteúdo.

>[!VIDEO](https://video.tv.adobe.com/v/3433552)
