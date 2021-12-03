---
title: Criar uma lista de assinaturas
description: Saiba como configurar uma lista de assinaturas no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Criar uma lista de assinaturas {#create-subscription-list}

## O que é uma lista de assinaturas?

Um serviço de assinatura refere-se aos bens e serviços de marketing fornecidos aos clientes que optaram por receber comunicações sobre um assunto/evento/interesse/etc. específico. numa base contínua. Em [!DNL Journey Optimizer], esses clientes que optaram por participar são coletados em uma lista de assinaturas.

Um serviço de assinatura pode ser:

* um boletim informativo, por exemplo, &quot;Série em execução&quot;
* um evento, por exemplo &quot;Summit 2021&quot;
* um webinário, por exemplo, &quot;Saiba mais sobre o crypto&quot;
* um interesse em um determinado produto/esporte/serviço/etc., por exemplo &quot;Interessado em comprar uma casa nos próximos 12 meses&quot;
* preferência por como ser notificado, por exemplo &quot;Receber novas notificações de música por email&quot;

Os perfis podem ser adicionados a uma lista de assinaturas por meio de uma [página de aterrissagem](create-lp.md). Um exemplo é apresentado em [esta seção](get-started-lp.md#subscription-to-a-service).

## Definir uma lista de assinaturas {#define-subscription-list}

Para criar uma lista de subscrição, siga as etapas abaixo.

1. Para acessar as listas de subscrição, selecione **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Na lista de assinaturas, clique em **[!UICONTROL Create subscription]** lista.

   ![](../assets/lp_create-subscription-list.png)

1. Adicione um nome e uma descrição. Esses campos são obrigatórios.

1. Você pode definir uma data de início e uma data de término.

   ![](../assets/lp_subscription-list-dates.png)

1. Clique em **[!UICONTROL Save]**.

A lista exibe todas as listas de assinaturas criadas. Você pode filtrá-los com base na data de criação ou na data de modificação.

![](../assets/lp_subscription-filters.png)

Os status possíveis são os seguintes:

* **[!UICONTROL Not started]**: Você definiu uma data de início posterior ao dia atual. Os perfis inscritos nessa lista ainda não receberão comunicações relacionadas a essa lista de assinaturas.
* **[!UICONTROL Live]**: O dia atual é composto pela data de início e de término da lista de assinaturas ou por datas de término/início não definidas, o que significa que a lista de assinaturas está sempre ativa.
* **[!UICONTROL Expired]**: A data de término é passada, a lista de assinaturas não é mais válida. Qualquer perfil inscrito nessa lista não receberá mais comunicações relacionadas a essa lista de assinaturas.

Depois que a lista de assinaturas for criada, você poderá usá-la em uma landing page para que os perfis possam aderir a um formulário e ser adicionados à lista. [Saiba mais](design-lp.md)

Também é possível usar listas de assinaturas como segmentos ao criar jornadas e personalização.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->