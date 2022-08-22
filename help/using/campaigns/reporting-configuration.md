---
title: Configuração de relatórios
description: Saiba como configurar a fonte de dados de relatórios
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 5%

---

# Configuração de relatórios {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configurar conjuntos de dados para relatórios"
>abstract="A configuração de relatórios permite definir uma conexão com um sistema para recuperar informações personalizadas adicionais que serão usadas em seus relatórios. Ele deve ser executado por um usuário técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Você só pode selecionar um conjunto de dados do tipo evento que deve conter pelo menos um dos grupos de campos compatíveis: experienceevent-web, experienceevent-application, experienceevent-commerce."

A configuração da fonte de dados de relatórios permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em seus relatórios.

>[!NOTE]
>
>A configuração da fonte de dados deve ser executada por um usuário técnico. <!--Rights?-->

Para essa configuração, é necessário adicionar um ou mais conjuntos de dados que contenham os atributos que você deseja usar para seus relatórios. Para fazer isso, siga as etapas abaixo.

>[!CAUTION]
>
>Antes de poder adicionar um conjunto de dados à configuração do relatório, você deve criá-lo. Saiba como na [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>Você só pode adicionar conjuntos de dados do tipo evento, que devem conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Por exemplo, se você quiser saber o impacto de uma campanha de email nos dados de comércio, como compras ou pedidos, será necessário criar um conjunto de dados de evento de experiência com a variável **experienceevent-commerce** grupo de campos. Da mesma forma, se você deseja criar relatórios sobre interações móveis, é necessário criar um conjunto de dados de evento de experiência com a variável **experienceevent-application** grupo de campos. <!--If you want to report on web interactions then you need to include the web field group.--> É possível adicionar esses grupos de campos a um ou vários esquemas que serão usados em um conjunto de dados ou em conjuntos de dados diferentes.

>[!NOTE]
>
>Saiba mais sobre esquemas XDM e grupos de campos no [Documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. No **[!UICONTROL ADMINISTRATION]** selecione **[!UICONTROL Configurations]**. No  **[!UICONTROL Reporting]** seção , clique em **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   A lista de conjuntos de dados que já foram adicionados é exibida.

1. Na guia **[!UICONTROL Dataset]**, clique em **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se você selecionar a variável **[!UICONTROL System dataset]** , somente os conjuntos de dados criados pelo sistema são exibidos. Não será possível adicionar outros conjuntos de dados.

1. No **[!UICONTROL Dataset]** na lista suspensa, selecione o conjunto de dados que deseja usar para seus relatórios.

   >[!CAUTION]
   >
   >Você só pode selecionar um conjunto de dados do tipo evento, que deve conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Se você selecionar um conjunto de dados que não corresponda a esses critérios, não será possível salvar suas alterações.

   ![](assets/reporting-config-datasets.png)

   Saiba mais sobre conjuntos de dados no [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

1. No **[!UICONTROL Profile ID]** na lista suspensa, selecione o atributo de campo do conjunto de dados que será usado para identificar cada perfil em seus relatórios.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Somente as IDs disponíveis para relatório são exibidas.

1. A opção **[!UICONTROL Use Primary ID namespace]** é ativada por padrão. Se a opção **[!UICONTROL Profile ID]** é **[!UICONTROL Identity Map]**, você pode desativar essa opção e escolher outro namespace na lista suspensa que é exibida.

   ![](assets/reporting-config-namespace.png)

   Saiba mais sobre namespaces no [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. Salve as alterações para adicionar o conjunto de dados selecionado à lista de configuração de relatórios.

   >[!CAUTION]
   >
   >Se você selecionou um conjunto de dados que não é do tipo de evento, não será possível continuar.

Ao criar relatórios dos deliveries, agora é possível usar dados desse conjunto de dados para recuperar informações personalizadas adicionais e ajustar melhor seus relatórios. [Saiba mais](campaign-global-report.md#objectives-global)

>[!NOTE]
>
>Se você adicionar vários conjuntos de dados, todos os dados de todos os conjuntos de dados estarão disponíveis para relatórios.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
