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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# Tentativas {#retries}

Quando uma mensagem de email falha devido a um erro temporário **Suave rejeição** ou **Ignorado**, várias tentativas são executadas. Cada erro incrementa um contador de erros. Quando esse contador atinge o limite, o endereço é adicionado à lista de supressão.

>[!NOTE]
>
>Saiba mais sobre os tipos de erros na seção [Delivery failure types](../suppression-list.md#delivery-failures).

Na configuração padrão, o limite é definido em três erros:

* Para o mesmo delivery, no terceiro erro encontrado, o endereço é suprimido.

* Se houver diferentes deliveries e dois erros ocorrerem pelo menos em 24 horas de intervalo, o contador de erros será incrementado a cada erro e o endereço também será suprimido na terceira tentativa.

Se um delivery for bem-sucedido após uma tentativa, o contador de erros do endereço será reinicializado.

Você pode modificar o limite usando o botão **[!UICONTROL Edit]** do menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Período de tempo de repetição {#retry-duration}

O **período de tempo de repetição** é o período em que qualquer mensagem de email do delivery que encontrou um erro temporário ou rejeição temporária será repetida.

Por padrão, as tentativas serão executadas por **3,5 dias** (ou **84 horas**) a partir do momento em que a mensagem foi adicionada à fila de email.

No entanto, para garantir que as tentativas de repetição não sejam mais executadas quando não forem mais necessárias, é possível alterar essa configuração de acordo com suas necessidades ao criar ou editar uma predefinição de mensagem [a1/> aplicada ao canal de email.](message-presets.md)

Por exemplo, você pode definir o período de nova tentativa como 24 horas para um email transacional relacionado à redefinição de senha e contendo um link válido por apenas um dia. Da mesma forma, para uma venda à meia-noite, você pode definir um período de repetição de 6 horas.

>[!NOTE]
>
>O período de repetição não pode exceder 84 horas. O período mínimo de tentativas é de 6 horas para emails de marketing e 10 minutos para emails transacionais.

Saiba como ajustar os parâmetros de repetição de email ao criar uma predefinição de mensagem em [this section](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->