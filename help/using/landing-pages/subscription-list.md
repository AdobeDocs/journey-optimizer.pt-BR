---
title: Criar uma lista de assinaturas
description: Saiba como configurar uma lista de assinaturas no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 2%

---

# Listas de assinaturas {#create-subscription-list}

## O que é uma lista de assinaturas?

Um serviço de assinatura refere-se aos bens e serviços de marketing fornecidos aos clientes que optaram por receber comunicações sobre um assunto/evento/interesse/etc. específico. numa base contínua. Em [!DNL Journey Optimizer], esses clientes que optaram por participar são coletados em uma lista de assinaturas.

Um serviço de assinatura pode ser:

* um informativo, por exemplo: &quot;Série em execução&quot;
* um evento, por exemplo: &quot;Summit 2021&quot;
* um webinar, por exemplo: &quot;Saiba mais sobre o crypto&quot;
* um interesse em um produto/esporte/serviço/etc., por exemplo: &quot;Interessado em comprar uma casa nos próximos 12 meses&quot;
* uma preferência sobre como ser notificado, por exemplo: &quot;Receba novas notificações de música por email&quot;

Os perfis podem ser adicionados a uma lista de assinaturas por meio de uma [página de aterrissagem](create-lp.md). Um exemplo é apresentado em [esta seção](lp-use-cases.md#subscription-to-a-service).

## Definir uma lista de assinaturas {#define-subscription-list}

Para criar uma lista de subscrição, siga as etapas abaixo.

1. Para acessar as listas de subscrição, selecione **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Selecione o botão **[!UICONTROL Create subscription list]**.

   ![](../assets/lp_create-subscription-list.png)

1. Adicione um nome e uma descrição. Esses campos são obrigatórios.

1. Você pode definir uma data de início e uma data de término.

   ![](../assets/lp_subscription-list-dates.png)

1. Clique em **[!UICONTROL Save]**.

A lista exibe todas as listas de assinaturas criadas. Você pode filtrá-los com base na data de criação ou na data de modificação e em seu status.

![](../assets/lp_subscription-filters.png)

Os status possíveis são os seguintes:

* **[!UICONTROL Not started]**: Você definiu uma data de início posterior ao dia atual. Os perfis subscritos ainda não receberão comunicações relacionadas a esta lista de subscrição.
* **[!UICONTROL Live]**: O dia atual é composto pela data de início e de término da lista de assinaturas ou por datas de término/início não definidas, o que significa que a lista de assinaturas está sempre ativa.
* **[!UICONTROL Expired]**: A data de término é passada, portanto, a lista de assinaturas não é mais válida. Qualquer perfil inscrito não receberá mais comunicações relacionadas a esta lista de assinaturas.

Depois que a lista de assinaturas for criada, você poderá usá-la em uma landing page. Os perfis que optarem pelo formulário de landing page serão adicionados à lista. [Saiba mais](design-lp.md)

Também é possível usar as listas de assinatura como segmentos quando [jornadas de construção](../building-journeys/journey-gs.md#jo-build) e adicionar personalização.

>[!NOTE]
>
>Você pode monitorar os impactos da sua lista de assinaturas por meio de relatórios específicos. [Saiba mais](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
