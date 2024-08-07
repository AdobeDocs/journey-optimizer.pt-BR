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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# Introdução à personalização{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalizar experiências"
>abstract="Use o **Adobe Journey Optimizer** para adaptar as mensagens a cada destinatário, aproveitando seus dados e informações. Esses dados podem ser: nome, interesses, onde vivem, o que compraram etc."

Descubra os recursos de personalização do [!DNL Adobe Journey Optimizer] para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre eles. Esses dados podem ser: nome, interesses, onde vivem, o que compraram etc.

➡️ [Saiba como personalizar uma mensagem nestes vídeos](#video-perso)
➡️ [Descobrir casos de uso aproveitando a personalização](personalization-use-case.md)

## Criar expressões de personalização usando uma sintaxe dedicada {#syntax}

[!DNL Journey Optimizer] usa uma sintaxe de personalização simples **embutida** com base em Handlebars que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. [Saiba mais sobre a sintaxe de personalização](personalization-syntax.md).

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados Experience Platform: `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se &quot;Olá, John Doe&quot;.

## Aproveite os dados do perfil para personalizar suas mensagens {#data}

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

>[!CAUTION]
>O esquema **Perfil Individual XDM** é o único esquema que você pode usar para personalizar conteúdo em [!DNL Journey Optimizer].

Além disso, você também pode aproveitar os **atributos computados** para personalizar seu conteúdo. Os atributos computados são baseados em conjuntos de dados de Evento de experiência habilitados para perfil assimilados na Adobe Experience Platform e servem como pontos de dados agregados armazenados em perfis de clientes que resumem eventos comportamentais individuais [Saiba como trabalhar com atributos computados](../audience/computed-attributes.md)

## Trabalhar com o editor de personalização {#editor}

O [!DNL Journey Optimizer] fornece um editor de personalização onde você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo. Várias ferramentas estão disponíveis para ajudar a criar o conteúdo de personalização, como: funções auxiliares, biblioteca de expressões predefinidas, atributos que favorecem e muito mais.

* [Saiba como trabalhar com o editor de personalização](personalization-build-expressions.md)
* [Saiba onde você pode realizar a personalização](personalization-contexts.md).

## Vídeos tutoriais{#video-perso}

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Saiba como adicionar personalização baseada em perfil a uma mensagem e como usar a associação de público-alvo como pré-condição para um bloco de personalização.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

