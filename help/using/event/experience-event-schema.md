---
solution: Journey Optimizer
product: journey optimizer
title: Sobre schemas ExperienceEvent para eventos jornada
description: Saiba mais sobre Esquemas ExperienceEvent para eventos de jornada
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: dd65c4155320c818f97400548c0f9d4d6d4e2507
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 3%

---

# Sobre schemas ExperienceEvent para [!DNL Journey Optimizer] Eventos {#about-experienceevent-schemas}

[!DNL Journey Optimizer] são Eventos de experiência XDM enviados para a Adobe Experience Platform por assimilação de fluxo.

Dessa forma, um pré-requisito importante para configurar eventos para [!DNL Journey Optimizer] O é que você está familiarizado com o Experience Data Model (ou XDM) da Adobe Experience Platform e como compor schemas de evento de experiência XDM, bem como como fazer o stream de dados formatados em XDM para o Adobe Experience Platform.

## Requisitos de esquema para [!DNL Journey Optimizer] Eventos  {#schema-requirements}

A primeira etapa na configuração de um evento para [!DNL Journey Optimizer] O é garantir que você tenha um esquema XDM definido para representar o evento e um conjunto de dados criado para registrar instâncias do evento no Adobe Experience Platform. Ter um conjunto de dados para seus eventos não é estritamente necessário, mas enviar os eventos para um conjunto de dados específico permitirá manter o histórico de eventos dos usuários para referência e análise futuras, portanto, é sempre uma boa ideia. Se você ainda não tiver um esquema e conjunto de dados adequados para o evento, ambas as tarefas podem ser realizadas na interface da Web do Adobe Experience Platform.

![](assets/schema1.png)

Qualquer esquema XDM que será usado para [!DNL Journey Optimizer] Os eventos devem atender aos seguintes requisitos:

* O esquema deve ser da classe XDM ExperienceEvent.

   ![](assets/schema2.png)

* Para eventos gerados pelo sistema, o esquema deve incluir o grupo de campos Orchestration eventID . [!DNL Journey Optimizer] O usa esse campo para identificar eventos usados em jornadas.

   ![](assets/schema3.png)

* Declarar um campo de identidade para identificar o assunto do evento. Se nenhuma identidade for especificada, um mapa de identidade poderá ser usado. Isso não é recomendado.

   ![](assets/schema4.png)

* Se desejar que esses dados estejam disponíveis para pesquisa posteriormente em uma Jornada, marque o esquema e o conjunto de dados para o perfil.

   ![](assets/schema5.png)

   ![](assets/schema6.png)

* Você pode incluir campos de dados para capturar quaisquer outros dados de contexto que deseja incluir com o evento, como informações sobre o usuário, o dispositivo do qual o evento foi gerado, o local ou quaisquer outras circunstâncias significativas relacionadas ao evento.

   ![](assets/schema7.png)

   ![](assets/schema8.png)

## Aproveitar relacionamentos de esquema{#leverage_schema_relationships}

A Adobe Experience Platform permite definir relações entre esquemas para usar um conjunto de dados como uma tabela de pesquisa para outro.

Digamos que seu modelo de dados de marca tenha um esquema capturando compras. Você também tem um schema para o catálogo de produtos. Você pode capturar a ID do produto no esquema de compra e usar uma relação para pesquisar detalhes do produto mais completos do catálogo de produtos. Isso permite criar um segmento para todos os clientes que compraram um laptop, por exemplo, sem precisar listar explicitamente todas as IDs do laptop ou capturar todos os detalhes de produtos em sistemas transacionais.

Para definir uma relação, é necessário ter um campo dedicado no schema de origem, nesse caso, o campo ID do produto no schema de compra. Esse campo precisa fazer referência ao campo de ID do produto no schema de destino. As tabelas de origem e de destino devem estar habilitadas para perfis e o schema de destino deve ter esse campo comum definido como sua identidade primária.

Este é o esquema de catálogo de produtos ativado para o perfil com a ID de produto definida como a identidade primária.

![](assets/schema9.png)

Este é o schema de compra com o relacionamento definido no campo ID do produto.

![](assets/schema10.png)

>[!NOTE]
>
>Saiba mais sobre relações de schema no [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en).

No Journey Optimizer, você pode aproveitar todos os campos das tabelas vinculadas:

* ao configurar um evento comercial ou unitário, [Leia mais](../event/experience-event-schema.md#unitary_event_configuration)
* ao usar condições em uma jornada, [Leia mais](../event/experience-event-schema.md#journey_conditions_using_event_context)
* na personalização de mensagens, [Leia mais](../event/experience-event-schema.md#message_personalization)
* na personalização da ação personalizada, [Leia mais](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### Matrizes{#relationships_limitations}

Você pode definir uma relação de schema em uma matriz de strings, por exemplo, uma lista de IDs de produto.

![](assets/schema15.png)

No entanto, não é possível definir uma relação de schema com um atributo dentro de uma matriz de objetos, por exemplo, uma lista de informações de compra (ID do produto, nome do produto, preço, desconto). Os valores de pesquisa não estarão disponíveis em jornadas (condições, ações personalizadas, etc.) e personalização de mensagens.

![](assets/schema16.png)

### Configuração de evento{#unitary_event_configuration}

Os campos de esquema vinculados estão disponíveis na configuração de evento unitário e comercial:

* ao navegar pelos campos do schema do evento na tela de configuração do evento.
* ao definir uma condição para eventos gerados pelo sistema.

![](assets/schema11.png)

Os campos vinculados não estão disponíveis:

* na fórmula da chave de evento
* na condição de id de evento (eventos com base em regras)

Para saber como configurar um evento unitário, consulte esta seção [página](../event/about-creating.md).

### Condições de jornada usando o contexto do evento{#journey_conditions_using_event_context}

Você pode usar dados de uma tabela de pesquisa vinculada a um evento usado em uma jornada para a criação de condições (editor de expressão).

Adicione uma condição em uma jornada, edite a expressão e expanda o nó do evento no editor de expressão.

![](assets/schema12.png)

Para saber como definir condições de jornada, consulte esta seção [página](../building-journeys/condition-activity.md).

### Personalização de mensagem{#message_personalization}

Os campos vinculados estão disponíveis ao personalizar uma mensagem. Os campos relacionados são exibidos no contexto transmitido da jornada para a mensagem.

![](assets/schema14.png)

Para saber como personalizar uma mensagem com informações de jornada contextual, consulte esta seção [página](../personalization/personalization-use-case.md).

### Personalização de ação personalizada com o contexto de evento de jornada{#custom_action_personalization_with_journey_event_context}

Os campos vinculados estão disponíveis ao configurar os parâmetros de ação de uma atividade de ação personalizada do jornada.

![](assets/schema13.png)

Para saber como usar ações personalizadas, consulte esta seção [página](../building-journeys/using-custom-actions.md).
