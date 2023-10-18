---
solution: Journey Optimizer
product: journey optimizer
title: Modificar ou interromper uma campanha
description: Saiba como modificar, interromper ou duplicar campanhas ativas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: gerenciar campanhas, status, agendamento, acesso, otimizador
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# Gerenciar campanhas {#modify-stop-campaign}

Depois que uma campanha é ativada, você pode modificá-la ou interrompê-la a qualquer momento. Essas operações estão disponíveis somente para campanhas com uma execução recorrente.

Além disso, você pode duplicar campanhas ativas (executadas uma vez ou com uma execução recorrente) para criar novas campanhas e arquivar campanhas concluídas ou interrompidas.

## Acessar campanhas {#access}

As campanhas podem ser acessadas no **[!UICONTROL Campanhas]** menu.

Por padrão, a lista mostra todas as campanhas com **[!UICONTROL Rascunho]**, **[!UICONTROL Agendado]**, e **[!UICONTROL Ao vivo]** status. Para exibir campanhas interrompidas, concluídas e arquivadas, é necessário limpar o filtro.

![](assets/create-campaign-list.png)

Além disso, você pode filtrar a lista com base no tipo de campanha e no canal, ou nas tags atribuídas às campanhas ao criá-las. [Saiba como atribuir tags a uma campanha](create-campaign.md#create)

## Status da campanha {#statuses}

As campanhas podem ter vários status:

* **[!UICONTROL Rascunho]**: A campanha está sendo editada e não foi ativada.
* **[!UICONTROL Ativando]**: a campanha está sendo ativada.
* **[!UICONTROL Ao vivo]**: a campanha foi ativada.
* **[!UICONTROL Agendado]**: a campanha é configurada para ser ativada em uma data de início específica.
* **[!UICONTROL Parado]**: a campanha foi interrompida manualmente. Não é possível ativá-lo ou reutilizá-lo. [Saiba como interromper uma campanha](modify-stop-campaign.md#stop)
* **[!UICONTROL Concluído]**: a campanha está concluída. Esse status é atribuído automaticamente 3 dias após a ativação de uma campanha ou na data final da campanha, se houver uma execução recorrente.
* **[!UICONTROL Arquivado]**: a campanha foi arquivada. [Saiba como arquivar campanhas](modify-stop-campaign.md#archive)

>[!NOTE]
>
>O ícone &quot;Abrir versão de rascunho&quot; ao lado de um **[!UICONTROL Ao vivo]** ou **[!UICONTROL Agendado]** O status indica que uma nova versão da campanha foi criada e ainda não foi ativada. [Saiba mais](modify-stop-campaign.md#modify).

## Modificar uma campanha recorrente {#modify}

Para modificar e criar uma nova versão de uma campanha recorrente, siga estas etapas:

1. Abra a campanha e clique no link **[!UICONTROL Modificar campanha]** botão.

1. Uma nova versão da campanha é criada. Você pode verificar a versão ao vivo clicando em **[!UICONTROL Abrir versão ao vivo]**.

   ![](assets/create-campaign-draft.png)

   Na lista Campanhas, as campanhas ativadas com uma versão de rascunho em andamento são exibidas com um ícone específico na **[!UICONTROL Status]** coluna. Clique nesse ícone para abrir a versão de rascunho da campanha.

   ![](assets/create-campaign-edit-list.png)

1. Quando as alterações estiverem prontas, você poderá ativar a nova versão da campanha (consulte [Revisar e ativar uma campanha](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Ativar o rascunho substituirá a versão ao vivo da campanha.

## Interromper uma campanha recorrente {#stop}

Para interromper uma campanha recorrente, abra-a e clique no link **[!UICONTROL Interromper campanha]** botão.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Interromper uma campanha não interromperá um envio em andamento, mas interromperá um envio agendado ou as próximas ocorrências se o envio já estiver em andamento.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicar uma campanha {#duplicate}

Você pode duplicar uma campanha em tempo real para criar uma nova. Para fazer isso, abra a campanha e clique em **[!UICONTROL Duplicar]**.

![](assets/create-campaign-duplicate.png)

## Arquivar uma campanha {#archive}

Com o tempo, a lista de campanhas continua crescendo e, eventualmente, dificulta a navegação em campanhas concluídas e interrompidas.

Para evitar isso, você pode arquivar campanhas concluídas e interrompidas que não são mais necessárias. Para fazer isso, clique no botão de reticências e selecione **[!UICONTROL Arquivar]**.

![](assets/create-campaign-archive.png)

As campanhas arquivadas podem ser recuperadas usando o filtro dedicado na lista. [Saiba como acessar campanhas](get-started-with-campaigns.md#access)
