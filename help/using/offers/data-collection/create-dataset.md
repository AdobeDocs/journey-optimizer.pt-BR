---
product: experience platform
solution: Experience Platform
title: Criar um conjunto de dados para coletar eventos
description: Saiba como criar um conjunto de dados para coletar eventos
feature: Ranking, Offers, Datasets
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 0ea2ed03a476e0b64a8ebfadde403ff9f9e57bba
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 17%

---

# Criar um conjunto de dados para coletar eventos {#create-dataset}

Para coletar eventos de experiência, primeiro é necessário criar um conjunto de dados para onde esses eventos serão enviados.

Comece criando o esquema que será usado no seu conjunto de dados:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Esquema]**.

1. Clique em **[!UICONTROL Criar esquema]**, no canto superior direito, selecione **[!UICONTROL Evento de experiência]** e clique em **Próxima**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. Insira um nome e uma descrição para o esquema e clique em **Concluir**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. No **[!UICONTROL Grupos de campos]** à esquerda, selecione **[!UICONTROL Adicionar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. No **[!UICONTROL Pesquisar]** digite &quot;interação de proposta&quot;.

1. Selecione o **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos e clique **[!UICONTROL Adicionar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >O esquema que será usado no conjunto de dados deve ter a **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos associado a ele. Caso contrário, você não poderá usá-lo no modelo de IA.

1. Salve o esquema.

>[!NOTE]
>
>Saiba mais sobre a criação de esquemas em [Noções básicas da composição do esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR#understanding-schemas){target="_blank"}.

Agora você está pronto para criar um conjunto de dados usando este esquema. Para fazer isso, siga as etapas abaixo:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Conjuntos de dados]** e vá para a página **[!UICONTROL Procurar]** guia.

1. Clique em **[!UICONTROL Criar conjunto de dados]** e selecione **[!UICONTROL Criar conjunto de dados a partir do esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecione o schema que acabou de criar na lista e clique em **[!UICONTROL Próxima]**.

1. Forneça um nome exclusivo para o conjunto de dados na **[!UICONTROL Nome]** e clique em **[!UICONTROL Concluir]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Esse conjunto de dados agora pode ser selecionado para coletar dados do evento quando [criação de um modelo de IA](../ranking/create-ranking-strategies.md).
