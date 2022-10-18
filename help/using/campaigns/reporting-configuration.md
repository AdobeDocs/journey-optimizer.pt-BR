---
solution: Journey Optimizer
product: journey optimizer
title: Configurar relatórios do Journey Optimizer para experimentação
description: Saiba como configurar a fonte de dados de relatórios
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 29%

---

# Configurar relatórios para experimentação {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configurar conjuntos de dados para relatórios"
>abstract="A configuração de relatórios permite recuperar métricas adicionais que serão usadas na guia Objetivos dos relatórios de campanha. Ela deve ser feita por um usuário técnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Você só pode selecionar um conjunto de dados do tipo evento, que deve conter pelo menos um dos grupos de campos compatíveis: Detalhes do aplicativo, Detalhes do comércio, Detalhes da Web."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

A configuração da fonte de dados de relatórios permite recuperar métricas adicionais que serão usadas no **[!UICONTROL Objetivos]** dos relatórios da campanha. [Saiba mais](content-experiment.md#objectives-global)

>[!NOTE]
>
>A configuração de relatório deve ser executada por um usuário técnico. <!--Rights?-->

Para essa configuração, é necessário adicionar um ou mais conjuntos de dados contendo os elementos adicionais que você deseja usar nos relatórios. Para fazer isso, siga as etapas [below](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Pré-requisitos


Antes de poder adicionar um conjunto de dados à configuração do relatório, você deve criar esse conjunto de dados. Saiba mais na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=pt-BR#create){target=&quot;_blank&quot;}.

* Você só pode adicionar conjuntos de dados do tipo evento.

* Esses conjuntos de dados devem conter pelo menos um dos seguintes [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=pt-BR#field-group){target=&quot;_blank&quot;}: **Detalhes do aplicativo**, **Detalhes de comércio**, **Detalhes da Web**.

   >[!NOTE]
   >
   >No momento, somente esses grupos de campos são compatíveis.

   Por exemplo, se você quiser saber o impacto de uma campanha de email nos dados de comércio, como compras ou pedidos, será necessário criar um conjunto de dados de evento de experiência com a variável **Detalhes de comércio** grupo de campos.

   Da mesma forma, se você deseja criar relatórios sobre interações móveis, é necessário criar um conjunto de dados de evento de experiência com a variável **Detalhes do aplicativo** grupo de campos.

   As métricas correspondentes a cada grupo de campos são listadas [here](#objective-list).

* É possível adicionar esses grupos de campos a um ou vários esquemas que serão usados em um ou vários conjuntos de dados.

>[!NOTE]
>
>Saiba mais sobre esquemas XDM e grupos de campos na [documentação de visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

## Objetivos correspondentes a cada grupo de campos {#objective-list}

A tabela abaixo mostra quais métricas serão adicionadas ao **[!UICONTROL Objetivos]** dos relatórios da campanha para cada grupo de campos.

| Grupo de campos | Objetivos |
|--- |--- |
| Detalhes de comércio | Preço total<br>Valor do Pagamento<br>Check-outs (exclusivo)<br>(Exclusivo) Adições à lista de produtos<br>(Exclusivo) Aberturas da Lista de Produtos<br>Remoção da lista de produtos (exclusivo)<br>(Exclusivo) Exibições da lista de produtos<br>(Exclusivo) Exibições do produto<br>(Exclusivo) Compras<br>(Exclusivo) Salvar para mais tarde<br>Preço do Produto Total<br>Quantidade do produto |
| Detalhes do aplicativo | (Exclusivo) Inicializações de aplicativo<br>Primeiras inicializações do aplicativo<br>(Exclusivo) Instalações de aplicativos<br>Atualizações de aplicativos (exclusivas) |
| Detalhes da Web | Exibições de página (exclusivas) |

## Adicionar conjuntos de dados {#add-datasets}

1. No **[!UICONTROL ADMINISTRAÇÃO]** selecione **[!UICONTROL Configurações]**. No  **[!UICONTROL Relatório]** seção , clique em **[!UICONTROL Gerenciar]**.

   ![](assets/reporting-config-menu.png)

   A lista de conjuntos de dados que já foram adicionados é exibida.

1. No **[!UICONTROL Conjunto de dados]** clique em **[!UICONTROL Adicionar conjunto de dados]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se você selecionar a variável **[!UICONTROL Conjunto de dados do sistema]** , somente os conjuntos de dados criados pelo sistema são exibidos. Não será possível adicionar outros conjuntos de dados.

1. No **[!UICONTROL Conjunto de dados]** na lista suspensa, selecione o conjunto de dados que deseja usar para seus relatórios.

   >[!CAUTION]
   >
   >Você só pode selecionar um conjunto de dados do tipo evento, que deve conter pelo menos um dos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **Detalhes do aplicativo**, **Detalhes de comércio**, **Detalhes da Web**. Se você selecionar um conjunto de dados que não corresponda a esses critérios, não será possível salvar suas alterações.

   ![](assets/reporting-config-datasets.png)

   Saiba mais sobre conjuntos de dados na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. No **[!UICONTROL ID do perfil]** na lista suspensa, selecione o atributo de campo do conjunto de dados que será usado para identificar cada perfil em seus relatórios.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Somente as IDs disponíveis para relatórios são exibidas.

1. O **[!UICONTROL Usar namespace da ID primária]** está ativada por padrão. Se a opção **[!UICONTROL ID do perfil]** é **[!UICONTROL Mapa de identidade]**, você pode desativar essa opção e escolher outro namespace na lista suspensa que é exibida.

   ![](assets/reporting-config-namespace.png)

   Saiba mais sobre namespaces na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=pt-BR){target=&quot;_blank&quot;}.

1. Salve as alterações para adicionar o conjunto de dados selecionado à lista de configuração de relatórios.

   >[!CAUTION]
   >
   >Se você selecionou um conjunto de dados que não é do tipo evento, não será possível continuar.

Ao criar relatórios de campanha, agora é possível visualizar as métricas correspondentes aos grupos de campos usados nos conjuntos de dados adicionados. Vá para o **[!UICONTROL Objetivos]** e selecione as métricas de sua escolha para ajustar melhor seus relatórios. [Saiba mais](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Se você adicionar vários conjuntos de dados, todos os dados de todos os conjuntos de dados estarão disponíveis para os relatórios.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
