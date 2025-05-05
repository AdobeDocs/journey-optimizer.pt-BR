---
solution: Journey Optimizer
product: journey optimizer
title: Configurar relatórios do Journey Optimizer para experimentação
description: Saiba como configurar a fonte de dados de relatórios
feature: Experimentation, Reporting
topic: Administration
role: Admin
level: Intermediate
keywords: configuração, experimentação, relatórios, otimizador
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 29%

---

# Pré-requisitos de relatórios e experimentação {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configurar conjuntos de dados para relatórios"
>abstract="A configuração de relatórios permite recuperar métricas adicionais que serão usadas nos relatórios de campanha. Ela deve ser feita por um usuário técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Você só pode selecionar um conjunto de dados do tipo evento, que deve conter pelo menos um dos grupos de campos compatíveis: Detalhes do aplicativo, Detalhes do comércio, Detalhes da Web."

>[!NOTE]
>
>A configuração de relatórios deve ser executada por um usuário técnico.

A configuração da fonte de dados de relatórios permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em seus relatórios.

Para essa configuração, é necessário adicionar um ou mais conjuntos de dados que contenham os elementos adicionais que você deseja usar em seus relatórios. Para fazer isso, siga as etapas [abaixo](#add-datasets).

Observe que, para canais na Web, baseados em código e no aplicativo, é necessário verificar se o [conjunto de dados](../data/get-started-datasets.md) configurado para a coleta de dados também é adicionado a essa configuração de relatórios. Caso contrário, os dados na Web e no aplicativo não serão exibidos nos relatórios de experimento de conteúdo.

## Pré-requisitos

Antes de poder adicionar um conjunto de dados à configuração de relatórios, você deve criar esse conjunto de dados. Saiba mais na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=pt-BR#create){target="_blank"}.

* Você só pode adicionar conjuntos de dados do tipo evento.

* Esses conjuntos de dados devem incluir o `Experience Event - Proposition Interactions` [grupo de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"}.

* Esses conjuntos de dados também podem conter um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} a seguir: `Application Details`, `Commerce Details`, `Web Details`.

  >[!NOTE]
  >
  >Outros grupos de campos também podem ser incluídos, mas somente os grupos de campos acima são compatíveis com os relatórios do Journey Optimizer no momento.

  Por exemplo, se você quiser saber o impacto de uma campanha de email nos dados de comércio, como compras ou pedidos, será necessário criar um conjunto de dados de evento de experiência com o grupo de campos `Commerce Details`.

  Da mesma forma, se quiser criar relatórios sobre interações móveis, será necessário criar um conjunto de dados de evento de experiência com o grupo de campos `Application Details`.

  <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* É possível adicionar esses grupos de campos a um ou vários esquemas que serão usados em um ou vários conjuntos de dados.

>[!NOTE]
>
>Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## Adicionar conjuntos de dados {#add-datasets}

>[!NOTE]
>
>Quaisquer conjuntos de dados recém-criados só estarão disponíveis nos relatórios do Customer Journey Analytics.

1. No menu **[!UICONTROL Administração]**, selecione **[!UICONTROL Configurações]**. Na seção **[!UICONTROL Relatórios]**, clique em **[!UICONTROL Gerenciar]**.

   ![](assets/reporting-config-menu.png)

   A lista de conjuntos de dados que já foram adicionados é exibida.

1. Na guia **[!UICONTROL Conjunto de Dados]**, clique em **[!UICONTROL Adicionar conjunto de dados]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se você selecionar a guia **[!UICONTROL Conjunto de dados do sistema]**, somente os conjuntos de dados criados pelo sistema serão exibidos. Não será possível adicionar outros conjuntos de dados.

1. Na lista suspensa **[!UICONTROL Conjunto de Dados]**, selecione o conjunto de dados que deseja usar para seus relatórios.

   >[!CAUTION]
   >
   >Você só pode selecionar um conjunto de dados do tipo evento, o qual deve conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target="_blank"} compatíveis: **Detalhes do Aplicativo**, **Detalhes do Commerce**, **Detalhes da Web**. Se você selecionar um conjunto de dados que não corresponda a esses critérios, não será possível salvar suas alterações.

   ![](assets/reporting-config-datasets.png)

   Saiba mais sobre conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=pt-BR){target="_blank"}.

1. Na lista suspensa **[!UICONTROL ID do Perfil]**, selecione o atributo de campo do conjunto de dados que será usado para identificar cada perfil em seus relatórios.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Somente as IDs disponíveis para relatórios são exibidas.

1. A opção **[!UICONTROL Usar namespace de ID Primária]** está habilitada por padrão. Se a **[!UICONTROL ID do Perfil]** selecionada for **[!UICONTROL Mapa de Identidade]**, você poderá desabilitar esta opção e escolher outro namespace na lista suspensa que será exibida.

   ![](assets/reporting-config-namespace.png)

   Saiba mais sobre namespaces na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=pt-BR){target="_blank"}.

1. Salve as alterações para adicionar o conjunto de dados selecionado à lista de configuração de relatórios.

   >[!CAUTION]
   >
   >Se você selecionou um conjunto de dados que não é do tipo evento, não será possível continuar.


<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
