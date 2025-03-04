---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à composição de público-alvo
description: Saiba mais sobre a composição de público-alvo
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 1ff33c3da5236cb4a89a893f83476867a2ecddd3
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 52%

---

# Introdução à composição de público-alvo {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="Criar uma composição"
>abstract="Crie um fluxo de trabalho de composição para combinar públicos-alvo da Adobe Experience Platform em uma tela visual e aproveitar várias atividades (divisão, exclusão...) para criar novos públicos-alvo."

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar o público"
>abstract="Publique a composição para salvar os públicos resultantes na Adobe Experience Platform."

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Atividade de público-alvo"
>abstract="A atividade de público permite incluir em sua composição perfis adicionais pertencentes a um público existente."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipos de mesclagem"
>abstract="Especifique como os perfis dos públicos selecionados devem ser mesclados."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Excluir tipo"
>abstract="Use o tipo Excluir público para excluir perfis pertencentes a um público existente. O tipo Excluir usando atributo permite excluir perfis com base em um atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Atividade Excluir"
>abstract="A atividade Excluir permite excluir perfis de sua composição ao selecionar um público existente ou usar uma regra."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="Atividade Enriquecer"
>abstract="Use a atividade Enriquecimento para enriquecer seu público-alvo com atributos adicionais provenientes de conjuntos de dados da Adobe Experience Platform. Por exemplo, é possível adicionar informações relacionadas ao produto comprado, como nome, preço ou ID do fabricante e aproveitar essas informações para personalizar as entregas enviadas ao público-alvo."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="Conjunto de dados de enriquecimento"
>abstract="Selecione o conjunto de dados de enriquecimento que contém os dados que você deseja associar ao público."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="Critérios de enriquecimento"
>abstract="Selecione os campos a serem usados como chave de reconciliação entre o conjunto de dados de origem, ou seja, o público, e o conjunto de dados de enriquecimento."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="Atributos de enriquecimento"
>abstract="Selecione um ou vários atributos do conjunto de dados de enriquecimento para associar ao público. Após a publicação da composição, esses atributos são associados ao público-alvo e podem ser aproveitados em campanhas do Journey Optimizer para personalizar entregas."

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Atividade de classificação"
>abstract="A atividade Classificação permite classificar perfis com base em um atributo específico e incluí-los na composição. Por exemplo, inclua os 50 perfis com a maior quantidade de pontos de fidelidade."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Adicionar limite de perfil"
>abstract="Ative essa opção para especificar um número máximo de perfis para incluir na composição."

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Atividade de divisão"
>abstract="A atividade de divisão permite dividir a composição em vários caminhos. Ao publicar a composição, um público será salvo na Adobe Experience Platform para cada caminho."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Tipo de divisão"
>abstract="Use o tipo de divisão de porcentagem para dividir perfis aleatoriamente em vários caminhos. O tipo de divisão de atributo permite dividir perfis com base em um atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Outros perfis"
>abstract="Ative essa opção para criar um caminho adicional com os perfis restantes que não correspondem a nenhuma das condições especificadas nos outros caminhos."

>[!BEGINSHADEBOX]

Estas documentações fornecem informações detalhadas sobre como trabalhar com a composição de público-alvo no Adobe Journey Optimizer. Se você for um cliente somente do Perfil do cliente em tempo real e não estiver usando o Adobe Journey Optimizer, [clique aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=pt-BR){target="_blank"}.

>[!ENDSHADEBOX]

A composição de público-alvo permite criar **fluxos de trabalho de composição**, nos quais você pode combinar públicos-alvo existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (dividir, excluir...) para criar novos públicos-alvo.

Depois de concluído, os **públicos-alvo resultantes** são salvos na Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados nas campanhas e jornadas da Journey Optimizer para clientes-alvo. Saiba como direcionar públicos-alvo no Journey Optimizer
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>O uso de públicos-alvo e atributos da composição de público-alvo está indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.
>
>Os atributos de enriquecimento ainda não estão integrados ao serviço de aplicação de políticas. Portanto, quaisquer rótulos de uso de dados que você aplicar aos atributos de enriquecimento não serão aplicados em campanhas ou jornadas do Journey Optimizer.

A composição de público-alvo é acessível no menu **[!UICONTROL Públicos-alvo]** do Adobe Journey Optimizer:

![](assets/audiences-browse.png)

* A guia **[!UICONTROL Visão geral]** fornece um painel dedicado com métricas principais relacionadas aos dados de público-alvo da sua organização. Para saber mais, consulte [Guia de painéis da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=pt-BR).

* A guia **[!UICONTROL Procurar]** lista todos os públicos-alvo existentes armazenados na Adobe Experience Platform.

* A guia **[!UICONTROL Composições]** permite criar workflows de composição em que é possível combinar e organizar públicos-alvo para criar novos.

## Criar um fluxo de trabalho de composição {#create}

Para criar um fluxo de trabalho de composição, siga estas etapas:

1. Acesse o menu **[!UICONTROL Públicos-alvo]** e selecione **[!UICONTROL Criar público-alvo]**.

1. Selecione **[!UICONTROL Compor Público]**.

   ![](assets/audiences-create.png)

1. A tela de composição é exibida com duas atividades padrão:

   * **[!UICONTROL Público-alvo]**: o ponto inicial da sua composição. Essa atividade permite selecionar um ou vários públicos-alvo como base para o fluxo de trabalho,

   * **[!UICONTROL Salvar]**: a última etapa da sua composição. Essa atividade permite salvar o resultado do fluxo de trabalho em um novo público-alvo.

1. Abra as propriedades de composição para especificar um título e uma descrição.

   Se nenhum título for definido nas propriedades, o rótulo da composição é definido como &quot;Composição&quot;, seguido pela data e hora de criação.

   ![](assets/audiences-properties.png)

1. Configure sua composição adicionando quantas atividades forem necessárias entre as atividades de **[!UICONTROL Público]** e **[!UICONTROL Salvar]**. Para obter mais informações sobre como criar uma composição, consulte a [Documentação de composição de público-alvo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition).

   ![](assets/audiences-publish.png)

1. Quando a composição estiver pronta, clique no botão **[!UICONTROL Publicar]** para publicar a composição e salvar os públicos resultantes no Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Você pode publicar até 10 composições em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

   Se ocorrer algum erro durante a publicação, os alertas serão exibidos com informações sobre como resolver o problema.

   ![](assets/audiences-alerts.png)

1. A composição é publicada. Os públicos-alvo resultantes são salvos no Adobe Experience Platform e estão prontos para serem direcionados no Journey Optimizer. [Saiba como direcionar públicos no Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>Os públicos-alvo de **composição de público-alvo** são executados diariamente, portanto, talvez seja necessário aguardar até 24 horas para usá-los no Journey Optimizer. Os atributos enriquecidos nos públicos-alvo de composição do público-alvo estão tão atualizados quanto a última execução de composição, que pode durar até 24 horas no passado.

## Acessar composições {#access}

Todas as composições criadas podem ser acessadas na guia **[!UICONTROL Composições]**. É possível duplicar ou excluir uma composição existente a qualquer momento usando o botão de reticências na lista.

As composições podem ter vários status:

* **[!UICONTROL Rascunho]**: a composição está em andamento e não foi publicada.
* **[!UICONTROL Publicado]**: a composição foi publicada, os públicos resultantes foram salvos e estão disponíveis para uso.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>No momento, a composição de público-alvo não está integrada ao recurso de redefinição da sandbox. Antes de iniciar uma redefinição de sandbox, é necessário excluir as composições manualmente para garantir que os dados do público-alvo associado sejam limpos corretamente. Informações detalhadas estão disponíveis na [Documentação de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions) do Adobe Experience Platform
