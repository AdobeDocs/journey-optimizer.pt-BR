---
solution: Journey Optimizer
product: journey optimizer
title: Create tasks for loyalty challenges
description: Learn how to create and configure tasks for loyalty challenges in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---

# Criar tarefas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos desafios de fidelidade](get-started.md)
* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* **Create tasks** ◀︎ **You are here**
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

Tasks define the specific actions or milestones that customers must complete to earn rewards in a loyalty challenge. You can configure task types, quantities, and product requirements to create engaging and personalized loyalty experiences.

Each task represents a measurable action that contributes toward challenge completion. Tasks are reusable components that can be created independently and then added to one or more challenges, or created directly within a challenge.

## Create a task {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="Create a task"
>abstract="Select a customer activity (Purchase or Spend), then configure activity-specific attributes: quantities or amounts, eligible items and exclusions, and optional limits such as minimum spend or maximum transactions. In the Properties pane, set the task name and description."

You can create tasks from two entry points. The configuration process is the same regardless of where you start.

>[!BEGINTABS]

>[!TAB From the Tasks inventory]

Select the **[!UICONTROL Tasks]** tab and select **[!UICONTROL Create Task]**. Tasks created from the inventory are saved and available for reuse across multiple challenges.

![](assets/task-create-inventory.png)

>[!TAB De dentro de um desafio]

Abrir um desafio existente ou criar um novo. Selecione **[!UICONTROL Adicionar tarefa]** e clique no botão **[!UICONTROL Novo]**. Tarefas criadas dessa maneira são automaticamente adicionadas ao seu desafio e também salvas no inventário de Tarefas para reutilização em outros desafios.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Escolher atividade do cliente {#choose-activity}

Selecione o tipo de atividade que os clientes devem executar para concluir esta tarefa:

* **[!UICONTROL Compra]**: os clientes devem comprar um ou mais itens para concluir esta tarefa
* **[!UICONTROL Gastos]**: os clientes devem gastar um valor especificado para concluir esta tarefa

Para selecionar uma atividade, clique no ícone **+** e selecione a atividade de cliente que melhor se alinha às suas metas de resultado. Cada tipo de atividade tem atributos configuráveis específicos para definir e moldar ainda mais os requisitos da tarefa.
![](assets/task-create-activity.png)

## Definir os atributos da tarefa {#define-attributes}

Configure os atributos da tarefa com base no tipo de atividade selecionado. Navegue pelas guias abaixo para ver os atributos disponíveis para cada tipo de atividade:

>[!BEGINTABS]

>[!TAB Atividade de compra]

Atributos disponíveis para atividades de **Compra**:

* **[!UICONTROL Quantidade]**: insira o número de itens que devem ser comprados para concluir esta tarefa.
* **[!UICONTROL Itens qualificados e exclusões]**: defina itens ou grupos de itens que contam para a conclusão da tarefa e os que não contam. [Saiba mais sobre itens qualificados e exclusões](#eligible-items-exclusions)
* **[!UICONTROL Valor mínimo de gasto]**: defina um requisito de valor mínimo de compra.
* **[!UICONTROL Número máximo de transações]**: limite quantas transações podem ser usadas para concluir a tarefa.

![](assets/task-create-purchase.png)

>[!TAB Gastar atividade]

Atributos disponíveis para atividades de **Gasto**:

* **[!UICONTROL Valor]**: insira o valor total de gastos necessário para concluir a tarefa.
* **[!UICONTROL Itens qualificados e exclusões]**: defina itens ou grupos de itens que contam para a conclusão da tarefa e os que não contam. [Saiba mais sobre itens qualificados e exclusões](#eligible-items-exclusions)
* **[!UICONTROL Número máximo de transações]**: especifique quantas transações podem atender ao requisito de gastos. Você pode ativar esse atributo no ícone de parâmetros.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Definir itens elegíveis e exclusões {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="Itens elegíveis e exclusões"
>abstract="Para as atividades de **Compra** e **Gasto**, você pode usar o atributo **[!UICONTROL Itens qualificados e exclusões]** para definir quais itens e grupos estão qualificados e quais foram excluídos. Isso permite direcionar produtos, categorias ou locais específicos para se alinhar às suas metas de desafio. Por exemplo, é possível limitar uma tarefa de gastos a categorias de produtos específicas ou excluir cartões-presente ou itens promocionais da contagem até a conclusão da tarefa."

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Para as atividades de **Compra** e **Gasto**, você pode usar o atributo **[!UICONTROL Itens qualificados e exclusões]** para definir quais itens e grupos estão qualificados e quais foram excluídos. Isso permite direcionar produtos, categorias ou locais específicos para se alinhar às suas metas de desafio.

Por exemplo, é possível limitar uma tarefa de gastos a categorias de produtos específicas ou excluir cartões-presente ou itens promocionais da contagem até a conclusão da tarefa.

![](assets/tasks-create-eligible.png)

* Para definir itens qualificados, insira IDs de item específicas, categorias ou IDs de destino, separadas por vírgulas no campo **[!UICONTROL As compras de tarefas qualificadas são limitadas ao seguinte]**. Se deixar esse campo vazio, todas as compras serão qualificadas por padrão. Você também pode inserir `*` para qualificar explicitamente todas as compras.

  Exemplo: `SKU001, SKU002, CategoryA`

* Para excluir itens da tarefa, insira IDs de item específicas, categorias ou IDs de destino no **[!UICONTROL Os itens a seguir são excluídos do campo desta tarefa]**.

  Exemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Definir propriedades da tarefa {#define-task-properties}

No painel de tarefas **[!UICONTROL Propriedades]**, configure as informações básicas da tarefa:

* **[!UICONTROL Nome da tarefa]**: digite um nome descritivo para a tarefa.
* **[!UICONTROL Descrição da tarefa]**: a descrição é gerada automaticamente com base na atividade e nos atributos configurados. Para inserir uma descrição personalizada, desative a opção de geração automática e insira sua descrição no campo de texto.

![](assets/tasks-create-properties.png)

Após configurar todos os atributos e propriedades, selecione **[!UICONTROL Criar]** para salvar a tarefa. A tarefa é salva no inventário de tarefas e, se criada a partir de um desafio, é automaticamente adicionada a esse desafio.
