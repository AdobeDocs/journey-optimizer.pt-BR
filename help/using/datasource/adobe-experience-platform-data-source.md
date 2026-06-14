---
solution: Journey Optimizer
product: journey optimizer
title: Fonte de dados da Adobe Experience Platform
description: Saiba como configurar a fonte de dados do Adobe Experience Platform
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: integrado, origem, dados, plataforma, integração
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
TQID: https://experienceleague.adobe.com/tvO8GjVADFHV1i6ff5krss2YyS-rtnQZ4BHcvvhG-t4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e366af78935405cd5acb15269194875098b20914
workflow-type: tm+mt
source-wordcount: 481
ht-degree: 25%

---

# Fonte de dados da Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!BEGINSHADEBOX]

**Nesta página:** configure grupos de campos na fonte de dados interna do Adobe Experience Platform para que você possa recuperar e usar os dados do Perfil do Cliente em Tempo Real em suas jornadas.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Fonte de dados da Adobe Experience Platform"
>abstract="A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Ele foi projetado para recuperar e usar dados do serviço de perfil do cliente em tempo real (por exemplo, verificar se a pessoa que entrou na jornada é uma mulher)."

A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados é incorporada e pré-configurada e não pode ser excluída. Essa fonte de dados foi projetada para recuperar e usar dados do Serviço de perfil do cliente em tempo real (por exemplo, verificar se a pessoa que inseriu uma jornada é do sexo feminino). Para obter mais informações sobre o Perfil do Cliente em tempo real da Adobe, consulte [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

Para permitir a conexão com o Serviço de perfil do cliente em tempo real, devemos usar uma chave para identificar uma pessoa e um namespace que contextualiza a chave. Como resultado, você só poderá usar essa fonte de dados se suas jornadas começarem com um evento contendo uma chave e um namespace. [Saiba mais](../building-journeys/journey.md).

Você pode editar o grupo de campos pré-configurado chamado &quot;ProfileFieldGroup&quot;, adicionar novos e remover os que não são usados em nenhum rascunho ou jornada em tempo real. [Saiba mais](../datasource/configure-data-sources.md#define-field-groups).

>[!CAUTION]
>
>Não há suporte para o uso de eventos de experiência em expressões/condições de jornada. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos. [Saiba mais](../building-journeys/exp-event-lookup.md)

As principais etapas para adicionar grupos de campos à fonte de dados integrada estão detalhadas abaixo:

1. Na lista de fontes de dados, selecione a fonte de dados interna **Adobe Experience Platform**.

   Essa ação abre o painel de configuração da fonte de dados no lado direito da tela.

   ![](assets/journey23.png)

1. Selecione **[!UICONTROL Adicionar Novo Grupo de Campos]** para definir uma [nova série de campos a serem recuperados](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecione um esquema no menu suspenso **[!UICONTROL Esquema]**. A criação do esquema é realizada no Adobe Experience Platform, não no Adobe Journey Optimizer.

   >[!NOTE]
   >
   >Somente esquemas XDM baseados em perfis individuais têm suporte na configuração do Data Source [!DNL Journey Optimizer]. Para obter mais informações, consulte [classe de Perfil Individual XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile){target="_blank"}.

1. Selecione os campos que serão usados e salve as alterações.

>[!TIP]
>
>Passe o mouse sobre o nome de um grupo de campos para revelar dois ícones à direita. Use-os para **Duplicar** ou **Excluir** o grupo de campos. Observe que o ícone **[!UICONTROL Excluir]** só estará disponível se o grupo de campos não for usado em nenhuma jornada do **Live**, **Rascunho** ou **Concluído**. Consulte o campo **[!UICONTROL Usado em]** para verificar se esse é o caso.
