---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização
feature: Personalização
topic: Personalização
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 52%

---

# Introdução à personalização{#add-personalization}

![](../assets/do-not-localize/badge.png)

Descubra os recursos de personalização do Jornada Optimier para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre ele. Pode ser seu primeiro nome, seus interesses, onde ele vive, o que ele comprou e muito mais.

O Journey Optimizer usa uma sintaxe de personalização simples **em linha** com base em Handlebars que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Para obter mais informações, consulte a documentação do [Modelo de dados (XDM) da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).

>[!CAUTION]
>O schema **Perfil individual XDM** é o único schema que você pode usar para personalizar o conteúdo no Journey Optimizer.

**Exemplos:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados da Experience Cloud Platform.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
