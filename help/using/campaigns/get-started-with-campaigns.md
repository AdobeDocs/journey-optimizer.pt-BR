---
title: Introdução às campanhas
description: Saiba mais sobre campanhas em [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 8%

---

# Introdução às campanhas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campanhas"
>abstract="Com Campanhas, você pode fornecer conteúdo único a um segmento específico em vários canais. Antes de criar uma nova campanha, verifique se você tem uma superfície de canal (ou seja, uma predefinição de mensagem) e um segmento do Adobe Experience Platform pronto para uso."

## Sobre campanhas {#about}

As campanhas permitem que você forneça conteúdo único para um segmento específico usando vários canais. Ao contrário das jornadas, onde as ações são projetadas para serem executadas em sequência, as campanhas executam ações simultaneamente, imediatamente ou em uma programação específica.

Você pode criar dois tipos de campanhas:

* **Campanhas programadas** permitir comunicações em lote ad-hoc simples para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, anúncios, avisos legais ou atualizações de políticas.
* **Campanhas acionadas pela API** permitir mensagens transacionais/operacionais simples com APIs REST (redefinição de senha, abandono de cartão etc.), onde a necessidade pode envolver personalização usando atributos de perfil e dados contextuais da carga.

Saiba como trabalhar com campanhas:
* [Criar uma campanha](create-campaign.md)
* [Criar campanhas acionadas por API](api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](modify-stop-campaign.md)
* [Relatório em tempo real da campanha](campaign-live-report.md)
* [Relatório global da campanha](campaign-global-report.md)

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
* **[!UICONTROL Completed]**: A campanha foi concluída.
* **[!UICONTROL Archived]**: A campanha foi arquivada.

>[!NOTE]
>
>O ícone &quot;Abrir versão de rascunho&quot; ao lado de um **[!UICONTROL Live]** ou **[!UICONTROL Scheduled]** indica que uma nova versão da campanha foi criada e ainda não foi ativada (consulte [Modificar uma campanha](modify-stop-campaign.md#modify)).
