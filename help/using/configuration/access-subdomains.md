---
solution: Journey Optimizer
product: journey optimizer
title: Acessar subdomínios delegados
description: Saiba como acessar subdomínios delegados.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---

# Acessar subdomínios delegados {#access-delegated-subdomains}

Todos os subdomínios delegados são exibidos na variável **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Subdomínios]** menu. Os filtros estão disponíveis para ajudar você a refinar a lista (data de delegação, usuário ou status).

![](assets/subdomain-list.png)

O **[!UICONTROL Status]** fornece informações sobre o processo de delegação de subdomínio:

* **[!UICONTROL Rascunho]**: A delegação de subdomínio foi salva como rascunho. Clique no nome do subdomínio para retomar o processo de delegação,
* **[!UICONTROL Processamento]**: O subdomínio está passando por várias verificações de configuração antes de poder ser usado,
* **[!UICONTROL Sucesso]**: O subdomínio passou pelas verificações com êxito e pode ser usado para enviar mensagens,
* **[!UICONTROL Falha]**: Uma ou várias verificações falharam após o envio da delegação de subdomínio.

Para acessar informações detalhadas sobre um subdomínio, abra-o na lista. É possível:

* Recupere o nome do subdomínio (somente leitura) configurado durante o processo de delegação, bem como os URLs gerados (recursos, mirror pages, URLs de rastreamento),

* Adicione um registro TXT de verificação do site do Google ao seu subdomínio para garantir que ele seja verificado (consulte [Adicionar um registro TXT do Google a um subdomínio](google-txt.md)).

![](assets/subdomain-delegated.png)
