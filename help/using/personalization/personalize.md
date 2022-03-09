---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 27%

---

# Introdução à personalização{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] recursos de personalização para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre eles. Pode ser seu primeiro nome, interesses, onde vivem, o que compraram e muito mais.

➡️ [Saiba como personalizar uma mensagem nesses vídeos](#video-perso)
➡️ [Casos de uso do Discover que usam a personalização](personalization-use-case.md)

## Criar expressões de personalização usando uma sintaxe dedicada {#syntax}

[!DNL Journey Optimizer] usa uma **inline** sintaxe de personalização simples com base em Handlebars, que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados do Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se &quot;Olá, John Doe&quot;.

## Aproveite os dados do perfil para personalizar suas mensagens {#data}

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

>[!CAUTION]
>O **Perfil individual XDM** schema é o único schema que pode ser usado para personalizar o conteúdo em [!DNL Journey Optimizer].

## Adicionar personalização em diferentes contextos {#contexts}

[!DNL Journey Optimizer] O permite personalizar o conteúdo e a exibição de mensagens de várias maneiras diferentes. Saiba mais sobre os contextos nos quais você pode realizar a personalização em [esta seção](personalization-contexts.md).

## Trabalhar com o editor de expressão {#editor}

[!DNL Journey Optimizer] O fornece um editor de expressão, onde você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

Várias ferramentas estão disponíveis para ajudar a criar o conteúdo de personalização (funções auxiliares, biblioteca de expressões predefinidas, favoritos de atributos...)

Saiba mais sobre [!DNL Journey Optimizer] editor de expressão em [esta seção](personalization-build-expressions.md)

## Vídeos tutoriais{#video-perso}

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
