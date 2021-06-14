---
title: Delegar subdomínios
description: Saiba como delegar subdomínios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configurações do aplicativo
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---


# Acessar subdomínios delegados

Todos os subdomínios delegados são exibidos no menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**. Os filtros estão disponíveis para ajudar você a refinar a lista (data de delegação, usuário ou status).

![](../assets/subdomain-list.png)

A coluna **[!UICONTROL Status]** fornece informações sobre o processo de delegação de subdomínio:

* **[!UICONTROL Draft]**: A delegação de subdomínio foi salva como rascunho. Clique no nome do subdomínio para retomar o processo de delegação,
* **[!UICONTROL Processing]**: O subdomínio está passando por várias verificações de configuração antes de poder ser usado,
* **[!UICONTROL Success]**: O subdomínio passou pelas verificações com êxito e pode ser usado para enviar mensagens,
* **[!UICONTROL Failed]**: Uma ou várias verificações falharam após o envio da delegação de subdomínio.

Para acessar informações detalhadas sobre um subdomínio, abra-o na lista. É possível:

* Recupere o nome do subdomínio (somente leitura) configurado durante o processo de delegação, bem como os URLs gerados (recursos, mirror page, URLs de rastreamento),

* Adicione um registro TXT de verificação de site do Google ao seu subdomínio para garantir que ele seja verificado (consulte [Adicionar um registro TXT do Google a um subdomínio](google-txt.md)).

![](../assets/subdomain-delegated.png)
