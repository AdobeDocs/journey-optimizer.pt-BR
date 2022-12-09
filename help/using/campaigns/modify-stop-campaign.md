---
solution: Journey Optimizer
product: journey optimizer
title: Modificar ou parar uma campanha
description: Saiba como modificar, parar ou duplicar campanhas ao vivo no [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Gerenciar campanhas {#modify-stop-campaign}

Depois que uma campanha é ativada, você pode modificá-la ou interrompê-la a qualquer momento. Essas operações estão disponíveis apenas para campanhas com uma execução recorrente.

Além disso, você pode duplicar campanhas ao vivo (executadas uma vez ou com uma execução recorrente) para criar novas campanhas e arquivar campanhas concluídas ou interrompidas.

## Campanhas de acesso {#access}

As campanhas podem ser acessadas a partir da variável **[!UICONTROL Campaigns]** menu.

Por padrão, a lista mostra todas as campanhas com a variável **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** e **[!UICONTROL Live]** status.

Para exibir campanhas interrompidas, concluídas e arquivadas, é necessário limpar o filtro.

![](assets/create-campaign-list.png)

## Status da campanha {#statuses}

As campanhas podem ter vários status:

* **[!UICONTROL Draft]**: A campanha está sendo editada e não foi ativada.
* **[!UICONTROL Activating]**: A campanha está sendo ativada.
* **[!UICONTROL Live]**: A campanha foi ativada.
* **[!UICONTROL Scheduled]**: A campanha está configurada para ser ativada em uma data de início específica.
* **[!UICONTROL Stopped]**: A campanha foi interrompida manualmente. Não é possível ativá-la ou reutilizá-la. [Saiba como parar uma campanha](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**: A campanha foi concluída. Esse status é automaticamente atribuído 3 dias após a ativação de uma campanha ou na data de término da campanha, se ela tiver uma execução recorrente.
* **[!UICONTROL Archived]**: A campanha foi arquivada. [Saiba como arquivar campanhas](modify-stop-campaign.md#archive)

>[!NOTE]
>
>O ícone &quot;Abrir versão de rascunho&quot; ao lado de um **[!UICONTROL Live]** ou **[!UICONTROL Scheduled]** indica que uma nova versão da campanha foi criada e ainda não foi ativada. [Saiba mais](modify-stop-campaign.md#modify).

## Modificar uma campanha recorrente {#modify}

Para modificar e criar uma nova versão de uma campanha recorrente, siga estas etapas:

1. Abra a campanha e clique no botão **[!UICONTROL Modify campaign]** botão.

1. Uma nova versão da campanha é criada. Você pode verificar a versão ao vivo clicando em **[!UICONTROL Open live version]**.

   ![](assets/create-campaign-draft.png)

   Na lista de campanhas, as campanhas ativadas com uma versão de rascunho em andamento são exibidas com um ícone específico na **[!UICONTROL Status]** coluna. Clique neste ícone para abrir a versão de rascunho da campanha.

   ![](assets/create-campaign-edit-list.png)

1. Quando as alterações estiverem prontas, você poderá ativar a nova versão da campanha (consulte [Revisar e ativar uma campanha](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Ativar o rascunho substituirá a versão ao vivo da campanha.

## Interromper uma campanha recorrente {#stop}

Para interromper uma campanha recorrente, abra-a e clique no botão **[!UICONTROL Stop campaign]** botão.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Parar uma campanha não interromperá um envio em andamento, mas interromperá um envio agendado ou as próximas ocorrências se o envio já estiver em andamento.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicar uma campanha {#duplicate}

Você pode duplicar uma campanha ao vivo para criar uma nova. Para fazer isso, abra a campanha e clique em **[!UICONTROL Duplicate]**.

![](assets/create-campaign-duplicate.png)

## Arquivar uma campanha {#archive}

Com o tempo, a lista de campanhas continua crescendo e, eventualmente, torna mais difícil navegar pelas campanhas concluídas e interrompidas.

Para evitar isso, você pode arquivar campanhas concluídas e interrompidas que não são mais necessárias. Para fazer isso, clique no botão elipse e selecione **[!UICONTROL Archive]**.

![](assets/create-campaign-archive.png)

Campanhas arquivadas podem ser recuperadas usando o filtro dedicado na lista. [Saiba como acessar campanhas](get-started-with-campaigns.md#access)
