---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar metadados ao conteúdo do email
description: Saiba como melhorar a legibilidade e a acessibilidade do seu conteúdo de email com metadados no Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: pré-cabeçalho, editor, resumo, email
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
source-git-commit: 0f3191a3d7c5c78e1d8fac2e587e26522f02f8f5
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 26%

---

# Adicionar metadados ao conteúdo do email {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Definir um pré-cabeçalho"
>abstract="Pré-cabeçalho é um texto resumido e curto que sucede ao assunto quando visualizamos o email no cliente de email. Em muitos casos, fornece um breve resumo do email e, normalmente, tem apenas uma frase."

Ao criar seus emails, para melhorar a legibilidade e a acessibilidade, você pode definir metaatributos adicionais para o seu conteúdo. O [!DNL Journey Optimizer] [Designer de email](get-started-email-design.md) permite que você especifique os seguintes elementos:

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Pré-cabeçalho]**: um pré-cabeçalho é um texto curto de resumo que segue a linha de assunto ao visualizar um email do seu cliente de email. Em muitos casos, fornece um breve resumo do email e, normalmente, tem apenas uma frase.

  >[!NOTE]
  >
  >Os pré-cabeçalhos não são compatíveis com todos os clientes de email. Quando não é compatível, o pré-cabeçalho não é exibido.

* **[!UICONTROL Título do documento]**: este campo, que corresponde ao elemento `<title>`, fornece informações descritivas sobre o seu conteúdo de email, geralmente exibido como uma dica de ferramenta ao passar o mouse. Ele pode ajudar os usuários com deficiência fornecendo contexto adicional e pode contribuir para uma melhor compreensão do seu conteúdo por mecanismos de pesquisa.

* **[!UICONTROL Idioma do documento]**: para garantir a acessibilidade, você pode especificar o idioma que os leitores de tela usarão para converter texto e imagens em fala ou braille - para pessoas com deficiências visuais ou dificuldades de aprendizagem. Esta configuração corresponde ao atributo `lang` no elemento `<html>`.

Para definir essas configurações, siga as etapas abaixo.

1. No [Designer de email](content-from-scratch.md), adicione pelo menos um **[!UICONTROL componente de Estrutura]** para começar a criar seu email.

1. Clique em **[!UICONTROL Corpo]**, na **[!UICONTROL Árvore de navegação]** à esquerda ou na parte superior do painel direito.

   ![](assets/email_body.png)

1. Na guia **[!UICONTROL Configurações]**, digite algum texto dentro dos campos **[!UICONTROL Pré-cabeçalho]**, **[!UICONTROL Título do documento]** e/ou **[!UICONTROL Idioma do documento]**.

1. Você também pode clicar no ícone de personalização ao lado de cada campo para personalizar o conteúdo de atributos de perfil, públicos, atributos contextuais e muito mais. [Saiba mais sobre a personalização](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Clique em **[!UICONTROL Salvar]** para confirmar as alterações.