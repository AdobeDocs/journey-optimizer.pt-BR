---
title: Relatórios no Customer Journey Analytics
description: Saiba como executar relatórios no Customer Journey Analytics
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilidade limitada"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 2349145fcf698769d16326a19a48a413a3c1dd95
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# Relatórios no Customer Journey Analytics {#cja}

Se estiver trabalhando com o Customer Journey Analytics, você pode criar painéis de relatórios personalizados para suas campanhas baseadas em código aproveitando o Experience Decisioning.

As principais etapas estão listadas abaixo. Informações detalhadas sobre como trabalhar com o Customer Journey Analytics estão disponíveis no [Documentação do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Criar e configurar um **conexão** em Customer Journey Analytics. Isso permite que você se conecte ao conjunto de dados para o qual deseja relatórios. [Saiba como criar uma conexão](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Criar um **visualização de dados** e associá-lo à conexão criada anteriormente. No **[!UICONTROL Componentes]** escolha os campos de esquema relevantes que deseja exibir nos relatórios. Para o Experience Decisioning, inclua a variável **propositioninteraction** e **propositiondisplay** campos. [Saiba como criar e configurar visualizações de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combinar componentes de dados, tabelas e visualizações em **projetos do workspace** para criar e compartilhar relatórios para sua campanha baseada em código.[Saiba como criar projetos do Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
