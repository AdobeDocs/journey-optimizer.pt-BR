---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: bd4a66d4d0c280c83b37241ccba53843b9442509
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 40%

---

# Introdução à personalização{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] recursos de personalização para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre eles. Pode ser seu primeiro nome, interesses, onde vivem, o que compraram e muito mais.

➡️ [Saiba como personalizar uma mensagem nesses vídeos](#video-perso)

[!DNL Journey Optimizer] usa uma **inline** sintaxe de personalização simples com base em Handlebars, que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

>[!CAUTION]
>O **Perfil individual XDM** schema é o único schema que pode ser usado para personalizar o conteúdo em [!DNL Journey Optimizer].

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados da Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se &quot;Olá, John Doe&quot;.

## Vídeos tutoriais{#video-perso}

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
