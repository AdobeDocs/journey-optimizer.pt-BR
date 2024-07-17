---
solution: Journey Optimizer
product: journey optimizer
title: Geração de email com o Assistente de IA
description: Comece a gerar conteúdo e ativo de email com o Assistente de IA
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 1b3930ff-f7b0-43f0-bcf2-5c3de0a88b25
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 4%

---

# Geração de email com o Assistente de IA {#generative-email}

>[!BEGINSHADEBOX]

**Índice**

* [Introdução ao Assistente de IA](gs-generative.md)
* Geração de email com o Assistente de IA
* [Geração de SMS com o Assistente de IA](generative-sms.md)
* [Geração de push com o Assistente de IA](generative-push.md)
* [Experimento de conteúdo com o Assistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Antes de começar a usar esse recurso, leia as [Medidas de Proteção e Limitações](gs-generative.md#generative-guardrails) relacionadas.

Depois de criar e personalizar seus emails, aproveite o potencial do Assistente de IA no Journey Optimizer, alimentado pela IA gerativa, para elevar seu conteúdo.

Use o Assistente de IA para aprimorar a eficácia de suas campanhas, criando emails completos, trechos de texto personalizados e imagens personalizadas que falam diretamente com seu público-alvo, aumentando o engajamento e a interação.

Explore as guias abaixo para saber como usar o Assistente de IA no Journey Optimizer.

>[!BEGINTABS]

>[!TAB Geração de email completa]

No exemplo a seguir, aproveitaremos o assistente de IA para refinar um modelo de email existente.

1. Depois de criar e configurar sua campanha de email, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha de email, consulte [esta página](../campaigns/create-campaign.md).

1. Personalize seu email conforme necessário e acesse o menu do **[!UICONTROL Assistente de IA]**.

   ![](assets/full-email-1.png){zoomable="yes"}

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize novo conteúdo com base no conteúdo da campanha, nome e público selecionado.

   Seu prompt deve estar sempre vinculado ao conteúdo atual.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![](assets/full-email-2.png){zoomable="yes"}

1. Você pode alternar as opções **[!UICONTROL Linha de assunto]** e **[!UICONTROL Pré-cabeçalho]** para incluí-las na geração da variante.

1. Clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer contexto adicional ao Assistente de IA ou selecione um carregado anteriormente.

   ![](assets/full-email-3.png){zoomable="yes"}

1. Personalize seu prompt com as diferentes opções:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idioma]**: selecione o idioma em que deseja que o conteúdo seja gerado.
   * **[!UICONTROL Tom]**: o tom do seu email deve repercutir na sua audiência. Se você quiser soar informativo, divertido ou persuasivo, o Assistente de IA poderá adaptar a mensagem de acordo.

   ![](assets/full-email-4.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

1. Navegue pelas **[!UICONTROL Variações]** geradas e clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Refrase]**: o Assistente de IA pode reformular sua mensagem de diferentes maneiras, mantendo sua escrita atualizada e engajando públicos diversos.

   * **[!UICONTROL Usar linguagem mais simples]**: use o Assistente de IA para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   ![](assets/full-email-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo de email com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de email. [Saiba mais](../campaigns/review-activate-campaign.md)

>[!TAB Geração de texto]

No exemplo a seguir, aproveitaremos o assistente de IA para aprimorar o conteúdo de nosso email.

1. Depois de criar e configurar sua campanha de email, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha de email, consulte [esta página](../email/create-email.md).

1. Selecione um **[!UICONTROL Componente de texto]** para direcionar somente a um conteúdo específico. e acesse o menu do **[!UICONTROL Assistente de IA]**.

   ![](assets/text-genai-1.png){zoomable="yes"}

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize novo conteúdo com base no conteúdo da campanha, nome e público selecionado.

   Seu prompt deve estar sempre vinculado ao conteúdo atual.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![](assets/text-genai-2.png){zoomable="yes"}

1. Clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer contexto adicional ao Assistente de IA.

   ![](assets/text-genai-3.png){zoomable="yes"}

1. Personalize seu prompt com as diferentes opções:

   * **[!UICONTROL Estratégia de comunicação]**: selecione a abordagem de comunicação desejada para o texto gerado.
   * **[!UICONTROL Idioma]**: escolha o idioma para o conteúdo da variante.
   * **[!UICONTROL Tone]**: certifique-se de que o texto é apropriado para seu público-alvo e sua finalidade.
   * **[!UICONTROL Comprimento]**: selecione o comprimento do conteúdo usando o controle deslizante de intervalo.

   ![](assets/text-genai-4.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

1. Navegue pelas **[!UICONTROL Variações]** geradas e clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Elaborar]**: o Assistente de IA pode ajudá-lo a expandir tópicos específicos, fornecendo detalhes adicionais para melhor compreensão e engajamento.

   * **[!UICONTROL Resumir]**: informações extensas podem sobrecarregar destinatários de email. Use o Assistente de IA para condensar os pontos principais em resumos claros e concisos que chamem a atenção e os incentivem a ler mais.

   * **[!UICONTROL Refrase]**:O Assistente de IA pode reformular sua mensagem de diferentes maneiras, mantendo sua escrita atualizada e engajando públicos diversos.

   * **[!UICONTROL Usar linguagem mais simples]**: use o Assistente de IA para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   ![](assets/text-genai-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo de email com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de email. [Saiba mais](../campaigns/review-activate-campaign.md)

>[!TAB Geração de imagem]

No exemplo abaixo, aprenda a usar o Assistente de IA para otimizar e melhorar seus ativos, garantindo uma experiência mais amigável.

1. Depois de criar e configurar sua campanha de email, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha de email, consulte [esta página](../email/create-email.md).

1. Preencha os **[!UICONTROL detalhes Básicos]** da sua campanha. Depois de concluído, clique em **[!UICONTROL Editar conteúdo de email]**.

1. Selecione o ativo que deseja alterar com o Assistente de IA.

1. No menu à direita, selecione **[!UICONTROL Assistente do AI]**.

   ![](assets/image-genai-1.png){zoomable="yes"}

1. Habilite a opção **[!UICONTROL Estilo de referência]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo de referência. Você também pode carregar uma imagem para adicionar contexto à sua variação.

   Seu prompt deve estar sempre vinculado ao conteúdo atual.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![](assets/image-genai-2.png){zoomable="yes"}

1. Clique em **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer contexto adicional ao Assistente de IA.

1. Personalize seu prompt com as diferentes opções:

   * **[!UICONTROL Taxa de proporção]**: determina a largura e a altura do ativo. Você tem a opção de escolher entre taxas comuns, como 16:9, 4:3, 3:2 ou 1:1, ou pode inserir um tamanho personalizado.
   * **[!UICONTROL Cor e tom]**: a aparência geral das cores em uma imagem e o humor ou atmosfera que ela transmite.
   * **[!UICONTROL Tipo de conteúdo]**: categoriza a natureza do elemento visual, distinguindo entre diferentes formas de representação visual, como fotos, gráficos ou arte.
   * **[!UICONTROL Iluminação]**: refere-se ao relâmpago presente em uma imagem, que molda sua atmosfera e realça elementos específicos.
   * **[!UICONTROL Composição]**: refere-se à disposição dos elementos dentro do quadro de uma imagem

   ![](assets/image-genai-4.png){zoomable="yes"}

1. Quando estiver satisfeito com a configuração do prompt, clique em **[!UICONTROL Gerar]**.

1. Navegue pelas **[!UICONTROL sugestões de variação]** para encontrar o ativo desejado.

   Clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada.

   ![](assets/image-genai-5.png){zoomable="yes"}

1. Escolha **[!UICONTROL Mostrar Semelhante]** se desejar exibir imagens relacionadas a esta variante.

   ![](assets/image-genai-6.png){zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Após definir o conteúdo da mensagem, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

1. Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de email. [Saiba mais](../campaigns/review-activate-campaign.md)

>[!ENDTABS]

## Vídeo explicativo {#video}

Saiba como usar o assistente de IA para gerar email, texto ou imagens completos.

>[!VIDEO](https://video.tv.adobe.com/v/3428341)
