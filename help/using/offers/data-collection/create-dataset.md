---
product: experience platform
solution: Experience Platform
title: Criar um conjunto de dados para coletar eventos
description: Saiba como criar um conjunto de dados para coletar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 15%

---

# Criar um conjunto de dados para coletar eventos {#create-dataset}

Para coletar eventos de experiência, primeiro é necessário criar um conjunto de dados para enviar esses eventos.

Comece criando o schema que será usado em seu conjunto de dados:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Esquema]** e vá para o **[!UICONTROL Procurar]** guia .

1. Clique em **[!UICONTROL Criar esquema]** e escolha **[!UICONTROL ExperiênciaEvento XDM]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. No **[!UICONTROL Grupos de campos]** à esquerda, selecione **[!UICONTROL Adicionar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. No **[!UICONTROL Pesquisar]** , digite &quot;interação de proposta&quot;.

1. Selecione o **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos e clique em **[!UICONTROL Adicionar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >O esquema que será usado em seu conjunto de dados deve ter a variável **[!UICONTROL Evento de experiência - Interações de proposta]** grupo de campos associado a ele. Caso contrário, você não poderá usá-lo em sua estratégia de classificação.

1. Digite um nome e salve o esquema.

>[!NOTE]
>
>Saiba mais sobre como criar schemas no [Noções básicas da composição do schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

Agora você está pronto para criar um conjunto de dados usando esse esquema. Para fazer isso, siga as etapas abaixo:

1. No **[!UICONTROL Gerenciamento de dados]** selecione **[!UICONTROL Conjuntos de dados]** e vá para o **[!UICONTROL Procurar]** guia .

1. Clique em **[!UICONTROL Criar conjunto de dados]** e selecione **[!UICONTROL Criar conjunto de dados a partir do esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecione o schema que você acabou de criar na lista e clique em **[!UICONTROL Próximo]**.

1. Forneça um nome exclusivo para o conjunto de dados na **[!UICONTROL Nome]** e clique em **[!UICONTROL Concluir]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Esse conjunto de dados agora pode ser selecionado para coletar dados de evento quando [criar uma estratégia de classificação](#create-ranking-strategy).
