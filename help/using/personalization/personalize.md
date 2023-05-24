---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: expressão, editor, início, personalização
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 28%

---

# Introdução à personalização{#add-personalization}

Descobrir [!DNL Adobe Journey Optimizer] recursos de personalização para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre eles. Pode ser seu nome, interesses, onde vivem, o que compraram e muito mais.

➡️ [Saiba como personalizar uma mensagem nesses vídeos](#video-perso)
➡️ [Descubra casos de uso que usam a personalização](personalization-use-case.md)

## Criar expressões de personalização usando uma sintaxe dedicada {#syntax}

[!DNL Journey Optimizer] usa um **em linha** sintaxe de personalização simples baseada em Handlebars que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se torna &quot;Olá, John Doe&quot;.

## Aproveite os dados do perfil para personalizar suas mensagens {#data}

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

>[!CAUTION]
>A variável **Perfil individual XDM** O esquema é o único esquema que você pode usar para personalizar o conteúdo no [!DNL Journey Optimizer].

## Adicionar personalização em contextos diferentes {#contexts}

[!DNL Journey Optimizer] O permite personalizar o conteúdo e a exibição de mensagens de várias maneiras diferentes. Saiba mais sobre os contextos em que você pode realizar a personalização no [nesta seção](personalization-contexts.md).

## Trabalhar com o editor de expressão {#editor}

[!DNL Journey Optimizer] O fornece um editor de expressão, no qual você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

Várias ferramentas estão disponíveis para ajudar a criar seu conteúdo de personalização (funções auxiliares, biblioteca de expressões predefinidas, atributos que favorecem...)

Saiba mais sobre [!DNL Journey Optimizer] editor de expressão em [nesta seção](personalization-build-expressions.md)

## Vídeos tutoriais{#video-perso}

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Saiba como adicionar uma personalização baseada em perfil a uma mensagem e como usar o segmento de afiliação como uma pré-condição para um bloco de personalização.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
