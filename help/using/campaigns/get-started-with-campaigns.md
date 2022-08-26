---
title: Introdução às campanhas
description: Saiba mais sobre campanhas em [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: bc036fc52424adaf129ab379872dedfc5994c3bb
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---

# Introdução às campanhas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campanhas"
>abstract="Com Campanhas, você pode fornecer conteúdo único a um segmento específico em vários canais. Antes de criar uma nova campanha, verifique se você tem uma superfície de canal (ou seja, uma predefinição de mensagem) e um segmento do Adobe Experience Platform pronto para uso."

## Sobre campanhas {#about}

>[!IMPORTANT]
>
>Esse recurso só está disponível para usuários com acesso a um Perfil de produto relacionado à campanha, como administrador do Campaign, aprovador do Campaign, gerente de campanha e/ou visualizador do Campaign. Para obter mais informações sobre como atribuir perfis de produto, consulte [esta página](../administration/permissions.md).

As campanhas permitem que você forneça conteúdo único para um segmento específico usando vários canais. Ao contrário das jornadas, onde as ações são projetadas para serem executadas em sequência, as campanhas executam ações simultaneamente, imediatamente ou em uma programação específica.

Isso permite enviar comunicações ad-hoc simples para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, anúncios, avisos legais ou atualizações de políticas.

➡️ [Descubra este recurso no vídeo](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Acessar campanhas {#access}

As campanhas podem ser acessadas a partir da variável **[!UICONTROL Campaigns]** menu.

Por padrão, a lista mostra todas as campanhas com a variável **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** e **[!UICONTROL Live]** status. Para exibir campanhas interrompidas, concluídas e arquivadas, é necessário limpar o filtro.

![](assets/create-campaign-list.png)

## Status da campanha {#statuses}

As campanhas podem ter vários status:

* **[!UICONTROL Draft]**: A campanha está sendo editada e não foi ativada.
* **[!UICONTROL Activating]**: A campanha está sendo ativada.
* **[!UICONTROL Live]**: A campanha foi ativada.
* **[!UICONTROL Scheduled]**: A campanha foi configurada para ser ativada em uma data de início específica.
* **[!UICONTROL Stopped]**: A campanha foi interrompida manualmente. Não é possível ativá-la ou reutilizá-la (consulte [Parar uma campanha](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: A campanha foi concluída. Esse status é automaticamente atribuído 3 dias após a ativação de uma campanha ou na data de término da campanha, se ela tiver uma execução recorrente.
* **[!UICONTROL Archived]**: A campanha foi arquivada.

>[!NOTE]
>
>O ícone &quot;Abrir versão de rascunho&quot; ao lado de um **[!UICONTROL Live]** ou **[!UICONTROL Scheduled]** indica que uma nova versão da campanha foi criada e ainda não foi ativada (consulte [Modificar uma campanha](modify-stop-campaign.md#modify)).

## Vídeo tutorial {#video}

Saiba como criar sua primeira campanha.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
