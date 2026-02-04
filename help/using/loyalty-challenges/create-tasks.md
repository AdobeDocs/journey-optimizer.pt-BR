---
solution: Journey Optimizer
product: journey optimizer
title: Criar tarefas para desafios de fidelidade
description: Saiba como criar e configurar tarefas para desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# Criar tarefas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* **Criar tarefas** ◀︎ **Você está aqui** - Definir tarefas de desafio
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Visão geral {#overview}

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas em um desafio de fidelidade. Você pode configurar tipos de tarefa, quantidades, requisitos de produto e valores de recompensa para criar experiências de fidelidade envolventes e personalizadas.

Cada tarefa representa uma ação mensurável que contribui para a conclusão do desafio. As tarefas são componentes reutilizáveis que podem ser criados de forma independente e depois adicionados a um ou mais desafios, ou criados diretamente dentro de um desafio.

### Como as tarefas funcionam em diferentes tipos de desafio {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

Dependendo do tipo de desafio (Padrão, Streak ou Sequencial), os clientes concluem as tarefas de forma diferente:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem
* **Distribuir desafios**: os clientes concluem a mesma tarefa várias vezes consecutivamente
* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida

## Criar uma tarefa {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

É possível criar tarefas a partir de dois pontos de entrada. O processo de configuração é o mesmo, independentemente de onde você começa.

+++No inventário de tarefas

1. Navegue até **[!UICONTROL Desafios de fidelidade]** no Journey Optimizer.

1. Selecione a guia **[!UICONTROL Tarefas]**.

1. Selecione **[!UICONTROL Criar tarefa]**.

As tarefas criadas no inventário são salvas e disponibilizadas para reutilização em vários desafios.

+++

+++De dentro de um desafio

1. Abrir um desafio existente ou criar um novo.

1. Navegue até a seção **[!UICONTROL Tarefas]**.

1. Selecione **[!UICONTROL Adicionar tarefa]** e escolha **[!UICONTROL Criar nova tarefa]**.

Tarefas criadas dessa maneira são automaticamente adicionadas ao seu desafio e também salvas no inventário de Tarefas para reutilização em outros desafios.

+++

### Definir propriedades da tarefa {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Configure as informações básicas da tarefa:

* **Nome da tarefa**: digite um nome descritivo para a tarefa. Esse nome pode ser visto por você e sua equipe, mas pode não ser mostrado aos clientes dependendo do design do cartão de conteúdo.
* **Descrição da tarefa**: (opcional) adicione detalhes sobre a finalidade ou os requisitos da tarefa.

### Escolher atividade do cliente {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Selecione o tipo de atividade de cliente que os clientes devem executar para concluir esta tarefa:

* **[!UICONTROL Compra]**: os clientes devem comprar um ou mais itens para concluir esta tarefa
* **[!UICONTROL Gastos]**: os clientes devem gastar um valor especificado para concluir esta tarefa

Selecione a atividade do cliente que melhor se alinha às suas metas de resultado. Cada tipo de atividade tem atributos configuráveis específicos para definir e moldar ainda mais os requisitos da tarefa.

### Definir atributos {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Configure os atributos da tarefa com base no tipo de atividade selecionado:

+++Para atividade de Compra

Configure os seguintes atributos:

* **Quantidade**: insira o número de itens que devem ser comprados para concluir esta tarefa
* **Itens qualificados e exclusões**: defina itens ou grupos de itens que contam para a conclusão da tarefa e os que não contam. Saiba mais sobre [definição de itens qualificados e exclusões](#eligible-items-exclusions)

**Atributos opcionais** (configure por meio do ícone de parâmetros):

* **Valor mínimo de gasto**: definir um requisito de valor mínimo de compra
* **Número máximo de transações**: limite quantas transações podem ser usadas para concluir a tarefa

+++

+++Para atividade de gasto

Configure os seguintes atributos:

* **Valor**: insira o valor total de gastos necessário para concluir a tarefa
* **Número máximo de transações**: especifique quantas transações podem atender ao requisito de gastos. Você pode desativar esse atributo do ícone de parâmetros se não quiser limitar o número de transações
* **Itens qualificados e exclusões**: (opcional) defina itens ou grupos de itens que contam para a conclusão de tarefas e os que não contam. Saiba mais sobre [definição de itens qualificados e exclusões](#eligible-items-exclusions)

+++

Após configurar todos os atributos, selecione **[!UICONTROL Criar]** para salvar a tarefa. A tarefa é salva no inventário de tarefas e, se criada a partir de um desafio, é automaticamente adicionada a esse desafio.

## Definir itens elegíveis e exclusões {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Para as atividades de Compra e Gasto, você pode definir itens e grupos elegíveis, e também excluir itens e grupos. Isso permite direcionar produtos, categorias ou locais específicos para se alinhar às suas metas de desafio.

**Casos de uso:**

* Crie uma tarefa que recompense os clientes pela compra de itens de café, mas exclua produtos de compensação
* Limitar uma tarefa de gastos a categorias de produtos específicas
* Excluir cartões-presente ou itens promocionais da contagem para a conclusão da tarefa

### Configurar itens elegíveis {#configure-eligible-items}

Para definir itens qualificados, use a **[!UICONTROL As compras de tarefas qualificadas estão limitadas à seguinte seção]**:

* Insira IDs de item, categorias ou IDs de destino específicas, separadas por vírgulas
* Exemplo: `SKU001, SKU002, CategoryA, StoreLocation123`
* **Dica**: insira `*` para qualificar todas as compras (comportamento padrão se deixado em branco)

### Configurar exclusões {#configure-exclusions}

Para excluir itens da tarefa, use a **[!UICONTROL Seção de itens a seguir excluídos desta tarefa]**:

* Insira IDs de item, categorias ou IDs de destino específicas que não devem ser consideradas na conclusão da tarefa
* Exemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Exclusões comuns: itens de venda ou compensação, cartões-presente, itens promocionais

>[!NOTE]
>
>As exclusões têm precedência sobre os itens elegíveis. Se um item corresponder a um item elegível e a uma exclusão, ele será excluído da tarefa.

## Próximas etapas {#next-steps}

Agora que você sabe como criar e configurar tarefas:

* [Criar desafios](create-challenges.md) - Saiba como criar desafios completos e configurar recompensas
* [Gerenciar desafios](manage-challenges.md) - Saiba como editar, monitorar e otimizar desafios
