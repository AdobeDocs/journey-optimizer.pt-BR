---
solution: Journey Optimizer
product: journey optimizer
title: Fonte de dados da Adobe Experience Platform
description: Saiba como configurar a fonte de dados da Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 69037a070f43fa89d0971cedc03adb577e1450d9
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Fonte de dados da Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Fonte de dados da Adobe Experience Platform"
>abstract="A fonte de dados da Adobe Experience Platform define a conexão com o Perfil do cliente em tempo real da Adobe. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Ele foi projetado para recuperar e usar dados do Serviço de perfil do cliente em tempo real (por exemplo, verifique se a pessoa que entrou em uma jornada é uma mulher). Ela permite usar os dados de Perfil e os dados de Eventos de experiência."

A fonte de dados da Adobe Experience Platform define a conexão com o Perfil do cliente em tempo real da Adobe. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Essa fonte de dados foi projetada para recuperar e usar dados do Serviço de perfil do cliente em tempo real (por exemplo, verifique se a pessoa que entrou em uma jornada é uma mulher). Ela permite usar os dados de Perfil e os dados de Eventos de experiência. Para obter mais informações sobre o Perfil do cliente em tempo real da Adobe, consulte [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.


Para permitir a conexão com o Serviço de perfil do cliente em tempo real, devemos usar uma chave para identificar uma pessoa e um namespace que contextualize a chave. Como resultado, você só poderá usar essa fonte de dados se suas jornadas começarem com um evento contendo uma chave e um namespace. [Saiba mais](../building-journeys/journey.md).

Você pode editar o grupo de campos pré-configurado chamado &quot;ProfileFieldGroup&quot;, adicionar novos campos e remover aqueles que não são usados em nenhum rascunho ou jornadas ao vivo. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Você pode recuperar os 1000 eventos de experiência mais recentes criados há menos de um ano.

Estas são as etapas principais para adicionar grupos de campos à fonte de dados integrada.

1. Na lista de fontes de dados, selecione a fonte de dados integrada da Adobe Experience Platform.

   Isso abrirá o painel de configuração da fonte de dados no lado direito da tela.

   ![](assets/journey23.png)

1. Clique em **[!UICONTROL Add a New Field Group]** para definir uma nova série de campos a serem recuperados. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecione um schema no **[!UICONTROL Schema]** lista suspensa. Este campo lista os esquemas Perfil e Eventos de experiência disponíveis na Adobe Experience Platform. A criação do schema não é executada em [!DNL Journey Optimizer]. Ele é executado na Adobe Experience Platform.
1. Selecione os campos que deseja usar.
1. Clique em **[!UICONTROL Save]**.

Ao colocar o cursor no nome de um grupo de campos, você verá dois ícones à direita. Eles permitem excluir e duplicar o grupo de campos. Observe que a variável **[!UICONTROL Delete]** O ícone só estará disponível se o grupo de campos não for usado em nenhuma jornada ao vivo ou de rascunho (informações exibidas no **[!UICONTROL Used in]** campo ).
