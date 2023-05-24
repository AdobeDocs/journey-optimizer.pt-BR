---
solution: Journey Optimizer
product: journey optimizer
title: Fonte de dados da Adobe Experience Platform
description: Saiba como configurar a fonte de dados do Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: integrado, origem, dados, plataforma, integração
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 32%

---

# Fonte de dados da Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Fonte de dados da Adobe Experience Platform"
>abstract="A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Ela foi criada para recuperar e usar dados do Real-Time Customer Profile Service (por exemplo, verificar se a pessoa que inseriu uma jornada é uma mulher). Ela permite usar os dados de Perfil e de Eventos de experiência."

A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Essa fonte de dados foi projetada para recuperar e usar dados do Serviço de perfil do cliente em tempo real (por exemplo, verificar se a pessoa que inseriu uma jornada é do sexo feminino). Ela permite usar os dados de Perfil e de Eventos de experiência. Para obter mais informações sobre o Perfil do cliente em tempo real do Adobe, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.


Para permitir a conexão com o Serviço de perfil do cliente em tempo real, devemos usar uma chave para identificar uma pessoa e um namespace que contextualiza a chave. Como resultado, você só poderá usar essa fonte de dados se suas jornadas começarem com um evento contendo uma chave e um namespace. [Saiba mais](../building-journeys/journey.md).

Você pode editar o grupo de campos pré-configurado chamado &quot;ProfileFieldGroup&quot;, adicionar novos e remover os que não são usados em nenhum rascunho ou jornada em tempo real. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Você pode recuperar os 1000 eventos de experiência mais recentes criados há menos de um ano.

Estas são as etapas principais para adicionar grupos de campos à fonte de dados integrada.

1. Na lista de fontes de dados, selecione a fonte de dados integrada do Adobe Experience Platform.

   Essa ação abre o painel de configuração da fonte de dados no lado direito da tela.

   ![](assets/journey23.png)

1. Clique em **[!UICONTROL Adicionar um novo grupo de campos]** para definir uma nova série de campos a serem recuperados. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecione um esquema na **[!UICONTROL Esquema]** menu suspenso. Este campo lista os esquemas de Perfil e Eventos de experiência disponíveis no Adobe Experience Platform. A criação do esquema não é executada em [!DNL Journey Optimizer]. É realizado no Adobe Experience Platform.
1. Selecione os campos que deseja usar.
1. Clique em **[!UICONTROL Salvar]**.

Ao colocar o cursor no nome de um grupo de campos, você verá dois ícones à direita. Eles permitem excluir e duplicar o grupo de campos. Observe que **[!UICONTROL Excluir]** O ícone só estará disponível se o grupo de campos não for usado em nenhuma jornada ativa ou de rascunho (informações exibidas na **[!UICONTROL Usado em]** campo).
