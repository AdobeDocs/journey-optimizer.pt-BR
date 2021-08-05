---
title: Lista de permissões
description: Saiba como usar a lista de permissões.
feature: Capacidade de entrega
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 2%

---

# Lista de permissões {#allow-list}

Agora é possível definir uma lista segura para envio específica no nível [sandbox](administration/sandboxes.md), para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para seus clientes.

>[!CAUTION]
>
>Esse recurso não está disponível nas sandboxes de produção.

A lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos recipients ou domínios autorizados a receber os emails enviados de uma sandbox específica. Isso pode impedir que você envie emails acidentalmente para endereços de clientes reais quando estiver em um ambiente de teste.

>[!NOTE]
>
>Esse recurso se aplica somente ao canal de email.

## Ative a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões em uma sandbox de não produção, é necessário fazer uma chamada de API de Adobe.

* Com essa API, você também pode desativar o recurso a qualquer momento.

* Você pode atualizar a lista de permissões antes ou depois de habilitar o recurso.

* A lógica de lista de permissões se aplica quando o recurso é ativado e se a lista de permissões não está vazia. Saiba mais [nesta seção](#logic).

>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é honrado ao executar jornadas, mas também ao testar mensagens com [provas](preview.md#send-proofs) e testar jornadas usando o [modo de teste](building-journeys/testing-the-journey.md).

## Adicionar entidades à lista de permissões {#add-entities}

>[!CAUTION]
>
>Esse recurso está **não** disponível nas sandboxes de produção. Ela se aplica somente ao canal de email.

Para adicionar novos endereços de email ou domínios à lista de permissões para uma sandbox específica, você deve chamar a API de supressão com o valor `ALLOWED` para o atributo `listType` . Por exemplo:

![](assets/allow-list-api.png)

Você pode executar as operações **Adicionar**, **Excluir** e **Obter**.

>[!NOTE]
>
>A lista de permissões pode conter até 1.000 entradas.

Saiba mais sobre como fazer chamadas de API do Adobe na [documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## Lógica da lista de permissões {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Quando a lista de permissões é **empty**, a lógica de lista de permissões não é aplicada. Isso significa que você pode enviar emails para qualquer perfil, desde que não estejam na [lista de supressão](suppression-list.md).

1. Quando a lista de permissões for **not empty**, a lógica de lista de permissões será aplicada:

   * Se uma entidade não estiver **na lista de permissões** e não estiver na lista de supressão, o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Not allowed]**.

   * Se uma entidade estiver **na lista de permissões**, e não na lista de supressão, o email poderá ser enviado para o recipient correspondente. No entanto, se a entidade também estiver na [lista de supressão](suppression-list.md), o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Suppressed]**.




