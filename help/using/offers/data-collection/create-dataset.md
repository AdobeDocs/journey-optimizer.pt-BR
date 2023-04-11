---
product: experience platform
solution: Experience Platform
title: Criar um conjunto de dados para coletar eventos
description: Saiba como criar um conjunto de dados para coletar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 17%

---

# Criar um conjunto de dados para coletar eventos {#create-dataset}

Para coletar eventos de experiência, primeiro é necessário criar um conjunto de dados para enviar esses eventos.

Comece criando o schema que será usado em seu conjunto de dados:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Esquema]**, acesse o **[!UICONTROL Procurar]** e clique em **[!UICONTROL Criar esquema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Choose **[!UICONTROL ExperiênciaEvento XDM]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. No **[!UICONTROL Grupos de campos]** à esquerda, selecione **[!UICONTROL Adicionar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. No **[!UICONTROL Pesquisar]** , digite &quot;interação de proposta&quot; e selecione o **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >O esquema que será usado em seu conjunto de dados deve ter a variável **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos associado a ele. Caso contrário, você não poderá usá-lo em sua estratégia de classificação.

1. Clique em **[!UICONTROL Adicionar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >O grupo de campos era anteriormente conhecido como mixin.

1. Digite um nome e salve o esquema.

>[!NOTE]
>
>Saiba mais sobre como criar schemas no [Noções básicas da composição do schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

Agora você está pronto para criar um conjunto de dados usando esse esquema. Para fazer isso, siga as etapas abaixo:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Conjuntos de dados]**, acesse o **[!UICONTROL Procurar]** e clique em **[!UICONTROL Criar conjunto de dados]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Selecione **[!UICONTROL Criar conjunto de dados a partir do esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecione o schema que você acabou de criar na lista.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Clique em **[!UICONTROL Próximo]**.

1. Forneça um nome exclusivo para o conjunto de dados na **[!UICONTROL Nome]** e clique em **[!UICONTROL Concluir]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Esse conjunto de dados agora pode ser selecionado para coletar dados de evento quando [criar uma estratégia de classificação](#create-ranking-strategy).
