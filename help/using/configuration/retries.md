---
title: Tentativas
description: Saiba como as tentativas são executadas antes de enviar um endereço para a lista de supressão
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
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# Tentativas {#retries}

Quando uma mensagem falha devido a um erro temporário **Suave rejeição** ou **Ignorado**, várias tentativas são executadas. Cada erro incrementa um contador de erros. Quando esse contador atinge o limite, o endereço é adicionado à lista de supressão.

Na configuração padrão<!--so can you edit this setting or not?? contradictory information was given-->, o limite é definido em três erros:

* Para o mesmo delivery, no terceiro erro encontrado, o endereço é suprimido.

* Se houver diferentes deliveries e dois erros ocorrerem pelo menos em 24 horas de intervalo, o contador de erros será incrementado a cada erro e o endereço também será suprimido na terceira tentativa.

Se um delivery for bem-sucedido após uma tentativa, o contador de erros do endereço será reinicializado.

Você pode modificar o limite usando o botão **[!UICONTROL Edit]** do menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Duração da nova tentativa de mensagem {#retry-duration}

As tentativas serão executadas por **3,5 dias** a partir do momento em que a mensagem foi adicionada à fila de email.

O atraso mínimo entre as tentativas e o número máximo de tentativas a serem executadas é <!--managed by the Enhanced MTA,--> baseado no desempenho histórico e atual de um IP em um determinado domínio.

Após 3,5 dias, qualquer mensagem na fila de tentativas será removida e enviada de volta como uma rejeição.<!--???-->