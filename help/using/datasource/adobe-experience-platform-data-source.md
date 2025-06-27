---
solution: Journey Optimizer
product: journey optimizer
title: Fonte de dados da Adobe Experience Platform
description: Saiba como configurar a fonte de dados do Adobe Experience Platform
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: integrado, origem, dados, plataforma, integração
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: dbb1a4d649f29b763121c7856cecca16dcd2864f
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 26%

---

# Fonte de dados da Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Fonte de dados da Adobe Experience Platform"
>abstract="A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Ela foi criada para recuperar e usar dados do Real-Time Customer Profile Service (por exemplo, verificar se a pessoa que inseriu uma jornada é uma mulher). Ela permite usar os dados do Perfil."

A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Essa fonte de dados foi projetada para recuperar e usar dados do Serviço de perfil do cliente em tempo real (por exemplo, verificar se a pessoa que inseriu uma jornada é do sexo feminino). Ela permite usar os dados do Perfil. Para obter mais informações sobre o Perfil do Cliente em tempo real da Adobe, consulte [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

Para permitir a conexão com o Serviço de perfil do cliente em tempo real, devemos usar uma chave para identificar uma pessoa e um namespace que contextualiza a chave. Como resultado, você só poderá usar essa fonte de dados se suas jornadas começarem com um evento contendo uma chave e um namespace. [Saiba mais](../building-journeys/journey.md).

Você pode editar o grupo de campos pré-configurado chamado &quot;ProfileFieldGroup&quot;, adicionar novos e remover os que não são usados em nenhum rascunho ou jornada em tempo real. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).


>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../building-journeys/exp-event-lookup.md)


As principais etapas para adicionar grupos de campos à fonte de dados integrada estão detalhadas abaixo:

1. Na lista de fontes de dados, selecione a fonte de dados **Adobe Experience Platform** interna.

   Essa ação abre o painel de configuração da fonte de dados no lado direito da tela.

   ![](assets/journey23.png)

1. Selecione **[!UICONTROL Adicionar Novo Grupo de Campos]** para definir uma [nova série de campos a serem recuperados](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecione um esquema no menu suspenso **[!UICONTROL Esquema]**. A criação do esquema é realizada no Adobe Experience Platform, não no Adobe Journey Optimizer.
1. Selecione os campos que serão usados e salve as alterações.


>[!TIP]
>
>Passe o mouse sobre o nome de um grupo de campos para revelar dois ícones à direita. Use-os para **Duplicar** ou **Excluir** o grupo de campos. Observe que o ícone **[!UICONTROL Excluir]** só estará disponível se o grupo de campos não for usado em nenhuma jornada do **Live**, **Rascunho** ou **Concluído**. Consulte o campo **[!UICONTROL Usado em]** para verificar se esse é o caso.
