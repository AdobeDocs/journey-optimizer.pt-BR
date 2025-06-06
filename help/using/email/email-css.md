---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar CSS personalizado ao seu conteúdo de email
description: Saiba como adicionar CSS personalizado ao seu conteúdo de email diretamente no Designer de email no Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, resumo, email
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# Adicionar metadados ao conteúdo do email {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Adicionar CSS personalizado"
>abstract="xxx"

Ao criar seus emails, você pode adicionar seu próprio CSS personalizado diretamente no [!DNL Journey Optimizer] [Designer de email](get-started-email-design.md).

O que é esperado na área de texto Adicionar CSS personalizado é uma cadeia de caracteres CSS válida.

![](assets/email-body-css.png)

Condições de disponibilidade

O recurso Adicionar CSS personalizado está disponível somente quando há um conteúdo definido no editor. Para ver a seção Adicionar CSS personalizado, o usuário precisa adicionar conteúdo no editor. Se o usuário remover todo o conteúdo, a seção desaparecerá e o css personalizado não será aplicado. Se o usuário adicionar o conteúdo de volta, a seção estará disponível e o css personalizado será aplicado.

**Exemplos de entradas CSS inválidas**

CSS inválido não pode ser salvo e, se o CSS for inválido, uma notificação em vermelho aparecerá para indicar que o CSS não pôde ser salvo.

`<style>` não é aceito


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


chave ausente inválida

```
body {
 background: red; 
```
