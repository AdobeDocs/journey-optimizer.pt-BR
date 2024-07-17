---
solution: Journey Optimizer
product: journey optimizer
title: Geração de push com o Assistente de IA
description: Comece a gerar conteúdo de push com o Assistente de IA
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: a9f9d8af-c762-4038-8bbc-bbd519e0ef3a
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 7%

---

# Geração de push com o Assistente de IA {#generative-push}

>[!BEGINSHADEBOX]

**Índice**

* [Introdução ao Assistente de IA](gs-generative.md)
* [Geração de email com o Assistente de IA](generative-email.md)
* [Geração de SMS com o Assistente de IA](generative-sms.md)
* Geração de push com o Assistente de IA
* [Experimento de conteúdo com o Assistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Antes de começar a usar esse recurso, leia as [Medidas de Proteção e Limitações](gs-generative.md#generative-guardrails) relacionadas.

Depois de criar e personalizar suas mensagens, coloque seu conteúdo de notificação por push em um novo patamar com o Assistente de IA no Adobe Journey Optimizer.

Explore as guias abaixo para saber como usar o Assistente de IA no Journey Optimizer.

>[!BEGINTABS]

>[!TAB Geração de push completa]

Neste exemplo específico, saiba como enviar uma notificação por push envolvente usando o Assistente de IA.

Siga estas etapas:

1. Depois de criar e configurar sua campanha de notificação por push, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha de notificação por push, consulte [esta página](../push/create-push.md).

1. Preencha os **[!UICONTROL detalhes Básicos]** da sua campanha. Depois de concluído, clique em **[!UICONTROL Editar conteúdo]**.

1. Personalize sua notificação por push conforme necessário. [Saiba mais](../push/design-push.md)

1. Acesse o menu **[!UICONTROL Mostrar assistente de IA]**.

   ![](assets/push-genai-full-1.png){zoomable="yes"}

1. Habilite a opção **[!UICONTROL Usar conteúdo original]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo da campanha, nome e público selecionado.

   Seu prompt deve estar sempre vinculado a um contexto específico.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![](assets/push-genai-full-2.png){zoomable="yes"}

1. Selecione **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer contexto adicional ao Assistente de IA.

1. Escolha qual campo você deseja gerar: **[!UICONTROL Título]** e/ou **[!UICONTROL Mensagem]**.

1. Personalize seu prompt com as diferentes opções:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idioma]**: selecione o idioma em que deseja que o conteúdo seja gerado.
   * **[!UICONTROL Tom]**: o tom do seu email deve repercutir na sua audiência. Se você quiser soar informativo, divertido ou persuasivo, o Assistente de IA poderá adaptar a mensagem de acordo.

   ![](assets/push-genai-full-3.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

1. Navegue pelas **[!UICONTROL Variações]** geradas e clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Refrase]**: o Assistente de IA pode reformular sua mensagem de diferentes maneiras, mantendo sua escrita atualizada e engajando públicos diversos.

   * **[!UICONTROL Usar idioma simples]**: use o Assistente de IA para simplificar seu idioma, garantindo clareza e acessibilidade para um público-alvo maior.

   ![](assets/push-genai-full-4.png){zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo de email com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de push. [Saiba mais](../campaigns/review-activate-campaign.md)

>[!TAB Geração de texto]

Neste exemplo específico, saiba como usar o Assistente de IA para conteúdo específico. Siga estas etapas:

1. Depois de criar e configurar sua campanha de notificação por push, clique em **[!UICONTROL Editar conteúdo]**.

   Para obter mais informações sobre como configurar sua campanha por push, consulte [esta página](../push/create-push.md).

1. Preencha os **[!UICONTROL detalhes Básicos]** da sua campanha. Depois de concluído, clique em **[!UICONTROL Editar conteúdo]**.

1. Personalize sua notificação por push conforme necessário. [Saiba mais](../push/design-push.md)

1. Acesse o menu **[!UICONTROL Mostrar assistente de IA]** ao lado dos campos **[!UICONTROL Título]** ou **[!UICONTROL Mensagem]**.

   ![](assets/push-genai-1.png){zoomable="yes"}

1. Habilite a opção **[!UICONTROL Usar conteúdo de referência]** para que o Assistente de IA personalize o novo conteúdo com base no conteúdo da campanha, nome e público selecionado.

   Seu prompt deve estar sempre vinculado a um contexto específico.

1. Ajuste o conteúdo descrevendo o que você deseja gerar no campo **[!UICONTROL Prompt]**.

   Se você estiver procurando ajuda para criar seu prompt, acesse a **[!UICONTROL Biblioteca de Prompts]**, que fornece diversas ideias de prompt para melhorar suas campanhas.

   ![](assets/push-genai-2.png){zoomable="yes"}

1. Selecione **[!UICONTROL Carregar ativo de marca]** para adicionar qualquer ativo de marca que contenha conteúdo que possa fornecer contexto adicional ao Assistente de IA.

   ![](assets/push-genai-3.png){zoomable="yes"}

1. Personalize seu prompt com as diferentes opções:

   * **[!UICONTROL Estratégia de comunicação]**: escolha o estilo de comunicação mais adequado para o texto gerado.
   * **[!UICONTROL Idioma]**: selecione o idioma em que deseja que o conteúdo seja gerado.
   * **[!UICONTROL Tom]**: o tom do seu email deve repercutir na sua audiência. Se você quiser soar informativo, divertido ou persuasivo, o Assistente de IA poderá adaptar a mensagem de acordo.
   * **[!UICONTROL Comprimento]**: selecione o comprimento do conteúdo usando o controle deslizante de intervalo.

   ![](assets/push-genai-4.png){zoomable="yes"}

1. Quando o prompt estiver pronto, clique em **[!UICONTROL Gerar]**.

1. Navegue pelas **[!UICONTROL Variações]** geradas e clique em **[!UICONTROL Visualizar]** para exibir uma versão em tela inteira da variação selecionada.

1. Navegue até a opção **[!UICONTROL Refinar]** na janela **[!UICONTROL Visualizar]** para acessar recursos de personalização adicionais:

   * **[!UICONTROL Usar como conteúdo de referência]**: a variante escolhida servirá como conteúdo de referência para gerar outros resultados.

   * **[!UICONTROL Elaborar]**: o Assistente de IA pode ajudá-lo a expandir tópicos específicos, fornecendo detalhes adicionais para melhor compreensão e engajamento.

   * **[!UICONTROL Resumir]**: informações extensas podem sobrecarregar destinatários de email. Use o Assistente de IA para condensar os pontos principais em resumos claros e concisos que chamem a atenção e os incentivem a ler mais.

   * **[!UICONTROL Refrase]**:O Assistente de IA pode reformular sua mensagem de diferentes maneiras, mantendo sua escrita atualizada e engajando públicos diversos.

   * **[!UICONTROL Usar linguagem mais simples]**: use o Assistente de IA para simplificar sua linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

   ![](assets/push-genai-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]** depois de encontrar o conteúdo apropriado.

   Você também pode ativar o experimento para o seu conteúdo. [Saiba mais](generative-experimentation.md)

1. Insira campos de personalização para personalizar seu conteúdo de email com base nos dados de perfis. Em seguida, clique no botão **[!UICONTROL Simular conteúdo]** para controlar a renderização e verificar as configurações de personalização com perfis de teste. [Saiba mais](../personalization/personalize.md)

Depois de definir seu conteúdo, público-alvo e programação, você estará pronto para preparar sua campanha de push. [Saiba mais](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
