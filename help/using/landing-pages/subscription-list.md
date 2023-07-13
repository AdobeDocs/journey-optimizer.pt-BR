---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma lista de assinaturas
description: Saiba como configurar uma lista de assinaturas no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: landing page, landing page, lista, assinatura, serviço
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 12%

---

# Listas de assinaturas {#create-subscription-list}

## O que é uma lista de assinaturas? {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Configurar uma lista de assinaturas"
>abstract="Crie uma lista de assinaturas para coletar perfis que aceitaram receber comunicações sobre um assunto ou evento específico. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html#define-subscription-list" text="Criar uma lista de assinaturas"

Um serviço de assinatura refere-se aos bens e serviços de marketing fornecidos aos clientes que optaram por receber comunicações sobre um assunto/evento/interesse/etc. específico. numa base contínua. Entrada [!DNL Journey Optimizer], esses clientes aceitos são incluídos em uma lista de assinaturas.

Um serviço de assinatura pode ser:

* um boletim informativo, por exemplo: &quot;Série em execução&quot;
* um evento, por exemplo: &quot;Summit 2021&quot;
* um webinário, por exemplo: &quot;Saiba mais sobre criptografia&quot;
* um interesse em um produto/esporte/serviço/etc específico, por exemplo: &quot;Interessado em comprar uma casa nos próximos 12 meses&quot;
* uma preferência sobre como ser notificado, por exemplo: &quot;Receber notificações de novas músicas por email&quot;

Os perfis podem ser adicionados a uma lista de inscrição por meio de um [landing page](create-lp.md). Um exemplo é apresentado em [nesta seção](lp-use-cases.md#subscription-to-a-service).

## Criar uma lista de assinaturas {#define-subscription-list}

Para criar uma lista de assinaturas, siga as etapas abaixo.

1. Para acessar as listas de assinaturas, selecione **[!UICONTROL Cliente]** > **[!UICONTROL Lista de assinaturas]**.

   ![](assets/lp_subscription-lists.png)

1. Selecione o **[!UICONTROL Criar lista de assinaturas]** botão.

   ![](assets/lp_create-subscription-list.png)

1. Adicione um título e uma descrição. Esses campos são obrigatórios.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >No momento, não é possível usar o espaçamento ou inserir um nome que já existe para outra lista de assinaturas na **[!UICONTROL Título]** campo.

1. Você pode definir uma data inicial e uma data final.

   ![](assets/lp_subscription-list-dates.png)

1. Clique em **[!UICONTROL Salvar]**.

A lista exibe todas as listas de assinaturas criadas. Você pode filtrá-los com base na data de criação ou de modificação e seus status.

![](assets/lp_subscription-filters.png)

Os status possíveis são os seguintes:

* **[!UICONTROL Não iniciado]**: Você definiu uma data de início posterior ao dia atual. Os perfis inscritos ainda não receberão comunicações relacionadas a esta lista de assinaturas.
* **[!UICONTROL Ao vivo]**: O dia atual é composto entre a data de início e a data de término da lista de assinaturas ou você não definiu datas de término/início, o que significa que a lista de assinaturas está sempre ativa.
* **[!UICONTROL Expirado]**: a data de término é passada e, portanto, a lista de assinaturas não é mais válida. Os perfis inscritos não receberão mais comunicações relacionadas a esta lista de assinaturas.

Depois que a lista de assinaturas for criada, você poderá usá-la em uma landing page. Os perfis que optarem por usar o formulário de página de aterrissagem serão adicionados à lista. [Saiba mais](design-lp.md)

Você também pode usar listas de assinaturas como públicos-alvo quando [criação de jornadas](../building-journeys/journey-gs.md#jo-build) e adicionar personalização.

>[!NOTE]
>
>Você pode monitorar os impactos da lista de assinaturas por meio de relatórios específicos. [Saiba mais](../reports/subscription-report-live.md)
