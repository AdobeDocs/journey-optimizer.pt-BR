---
title: Configuração de relatórios
description: Saiba como configurar a fonte de dados de relatórios
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# Configuração de relatórios {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configurar conjuntos de dados para relatórios"
>abstract="A configuração de relatórios permite definir uma conexão com um sistema para recuperar informações personalizadas adicionais que serão usadas em seus relatórios. Ela deve ser feita por um usuário técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Você só pode selecionar um conjunto de dados do tipo evento, o qual deve conter pelo menos um dos grupos de campos compatíveis: experienceevent-web, experienceevent-application, experienceevent-commerce."

A configuração da fonte de dados de relatórios permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em seus relatórios.

>[!NOTE]
>
>A configuração da fonte de dados deve ser feita por um usuário técnico. <!--Rights?-->

Para essa configuração, é necessário adicionar um ou mais conjuntos de dados que contenham os atributos que você deseja usar em seus relatórios. Para fazer isso, siga as etapas abaixo.

>[!CAUTION]
>
>Antes de poder adicionar um conjunto de dados à configuração de relatórios, você deve criá-lo. Saiba mais na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=pt-BR#create){target=&quot;_blank&quot;}.
>
>Você só pode adicionar conjuntos de dados do tipo evento, os quais devem conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target=&quot;_blank&quot;} compatíveis: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Por exemplo, se você quiser saber o impacto de uma campanha de email nos dados de comércio, como compras ou pedidos, será necessário criar um conjunto de dados de evento de experiência com o grupo de campos **experienceevent-commerce**. Da mesma forma, se quiser criar relatórios sobre interações móveis, será necessário criar um conjunto de dados de evento de experiência com o grupo de campos **experienceevent-application**. <!--If you want to report on web interactions then you need to include the web field group.--> É possível adicionar esses grupos de campos a um ou vários esquemas que serão usados em um conjunto de dados ou em conjuntos de dados diferentes.

>[!NOTE]
>
>Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. No menu **[!UICONTROL ADMINISTRATION]**, selecione **[!UICONTROL Configurations]**. Na seção **[!UICONTROL Reporting]**, clique em **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   A lista de conjuntos de dados que já foram adicionados é exibida.

1. Na guia **[!UICONTROL Dataset]**, clique em **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se você selecionar a guia **[!UICONTROL System dataset]**, somente os conjuntos de dados criados pelo sistema serão exibidos. Não será possível adicionar outros conjuntos de dados.

1. Na lista suspensa **[!UICONTROL Dataset]**, selecione o conjunto de dados que deseja usar para seus relatórios.

   >[!CAUTION]
   >
   >Você só pode selecionar um conjunto de dados do tipo evento, o qual deve conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} compatíveis: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Se você selecionar um conjunto de dados que não corresponda a esses critérios, não será possível salvar suas alterações.

   ![](assets/reporting-config-datasets.png)

   Saiba mais sobre conjuntos de dados na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. Na lista suspensa **[!UICONTROL Profile ID]**, selecione o atributo de campo do conjunto de dados que será usado para identificar cada perfil em seus relatórios.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Somente as IDs disponíveis para relatórios são exibidas.

1. A opção **[!UICONTROL Use Primary ID namespace]** é ativada por padrão. Se a **[!UICONTROL Profile ID]** selecionada for **[!UICONTROL Identity Map]**, você poderá desativar essa opção e escolher outro namespace na lista suspensa que será exibida.

   ![](assets/reporting-config-namespace.png)

   Saiba mais sobre namespaces na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. Salve as alterações para adicionar o conjunto de dados selecionado à lista de configuração de relatórios.

   >[!CAUTION]
   >
   >Se você selecionou um conjunto de dados que não é do tipo evento, não será possível continuar.

Ao criar relatórios dos deliveries, agora é possível usar dados desse conjunto de dados para recuperar informações personalizadas adicionais e ajustar melhor seus relatórios. [Saiba mais](content-experiment.md#objectives-global)

>[!NOTE]
>
>Se você adicionar vários conjuntos de dados, todos os dados de todos os conjuntos de dados estarão disponíveis para os relatórios.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
