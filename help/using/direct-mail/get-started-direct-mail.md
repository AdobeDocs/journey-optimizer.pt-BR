---
title: Introdução à correspondência direta
description: Saiba como criar e enviar uma mensagem de correspondência direta no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: correspondência direta, mensagem, campanha
source-git-commit: a445e418dc11f577c609c16894ce119359f2a261
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Introdução à correspondência direta {#create-direct}

>[!AVAILABILITY]
>
>Por enquanto, o Canal de mala direta não está disponível para organizações que compraram a oferta complementar do Adobe Healthcare Shield.
>

A correspondência direta é um canal offline que permite personalizar e gerar os arquivos de extração necessários para os provedores de correspondência direta enviarem emails para seus clientes.

Ao criar uma campanha de correspondência direta, o Journey Optimizer gera automaticamente um arquivo contendo todos os perfis direcionados e dados selecionados, como endereços postais e atributos de perfil. Esse arquivo é enviado ao servidor de sua escolha para que seja acessível ao seu provedor de correspondência direta escolhido, que lidará com o processo de correspondência real para você.

As principais etapas para enviar mensagens de correspondência direta são as seguintes:

![](assets/dm-creation-process.png)

Mensagens de correspondência direta só podem ser criadas no contexto de campanhas programadas. Eles não estão disponíveis para uso em campanhas acionadas por API ou em jornadas.

>[!IMPORTANT]
>
>Antes de enviar uma mensagem de mala direta, verifique se você configurou:
>
>1. A [configuração de roteamento de arquivos](../direct-mail/direct-mail-configuration.md#file-routing-configuration) que especifica o servidor onde o arquivo de extração deve ser carregado e armazenado,
>1. A [superfície de mensagem de correspondência direta](../direct-mail/direct-mail-configuration.md#direct-mail-surface) que referenciará a configuração de roteamento de arquivos.
