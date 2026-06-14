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
TQID: https://experienceleague.adobe.com/apen1-tlKZ3bnGV9X1RacDk1LXt7sJBQNfTQiaFAyYA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 24%

---

# Adicionar metadados ao conteúdo do email {#email-metadata}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como definir metadados de email no Designer de email, incluindo o pré-cabeçalho, o título do documento e o idioma do documento, para melhorar a legibilidade e a acessibilidade do seu conteúdo de email.

>[!ENDSHADEBOX]

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