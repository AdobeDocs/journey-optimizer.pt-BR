---
title: Lista de permissões
description: Saiba como usar a lista de permissões.
feature: Capacidade de entrega
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: 2d03285400b86b2c296997537852bb89ae0f6d0a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Lista de permissões {#allow-list}

Agora é possível definir uma lista segura para envio específica no nível [sandbox](administration/sandboxes.md), para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para seus clientes.

A lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos recipients ou domínios autorizados a receber os emails enviados de uma sandbox específica. Isso pode impedir que você envie emails acidentalmente para endereços de clientes reais quando estiver em um ambiente de teste.


>[!CAUTION]
>
>Esse recurso está **não** disponível nas sandboxes de produção. Ela se aplica somente ao canal de email.


## Ative a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões em uma sandbox de não produção, atualize a lista de permissões para que ela não fique mais vazia. Para desativar o recurso, limpe a lista de modo que ela fique vazia novamente.

<!--
you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in [this section](#logic).

-->
>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é honrado ao executar jornadas, mas também ao testar mensagens com [provas](preview.md#send-proofs) e testar jornadas usando o [modo de teste](building-journeys/testing-the-journey.md).

## Adicionar entidades à lista de permissões {#add-entities}

Para adicionar novos endereços de email ou domínios à lista de permissões para uma sandbox específica, você deve chamar a API de supressão com o valor `ALLOWED` para o atributo `listType` . Por exemplo:

![](assets/allow-list-api.png)

Você pode executar as operações **Adicionar**, **Excluir** e **Obter**.

>[!NOTE]
>
>A lista de permissões pode conter até 1.000 entradas.

<!--
Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).
-->


## Lógica da lista de permissões {#logic}

<!-- When the allowed list is [enabled](#enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Quando a lista de permissões é **empty**, a lógica de lista de permissões não é aplicada. Isso significa que você pode enviar emails para qualquer perfil, desde que não estejam na [lista de supressão](suppression-list.md).

Quando a lista de permissões for **not empty**, a lógica de lista de permissões será aplicada:

* Se uma entidade não estiver **na lista de permissões** e não estiver na lista de supressão, o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Not allowed]**.

* Se uma entidade estiver **na lista de permissões**, e não na lista de supressão, o email poderá ser enviado para o recipient correspondente. No entanto, se a entidade também estiver na [lista de supressão](suppression-list.md), o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Suppressed]**.




