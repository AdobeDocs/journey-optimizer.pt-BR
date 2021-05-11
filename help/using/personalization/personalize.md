---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# Comece já {#add-personalization}

![](../assets/do-not-localize/badge.png)

A personalização, no contexto do Journey Optimizer, é a ação de direcionar uma mensagem a um assinante específico, aproveitando os dados e informações que você tem sobre ele. Pode ser seu primeiro nome, seus interesses, onde ele vive, e muito mais.

O Journey Optimizer usa uma sintaxe de personalização simples **inline** com base em Handlebars que permite criar expressões com conteúdo delimitado por chaves duplas **{{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Consulte [Sintaxe de personalização](personalization-syntax.md).

A personalização é baseada nos dados de perfil gerenciados pelo schema **Perfil individual XDM** definido no Adobe Experience Platform. Para obter mais informações, consulte a documentação do [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).

>[!CAUTION]
>O esquema **Perfil individual XDM** é o único que você pode usar para personalizar o conteúdo no Journey Optimizer.

**Exemplos:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Durante o **processamento de mensagens** (email e push), a expressão é substituída pelos dados contidos nos bancos de dados da plataforma Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
