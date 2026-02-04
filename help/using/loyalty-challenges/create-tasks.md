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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# Criar tarefas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar e gerenciar desafios de fidelidade](access-loyalty-challenges.md) - gerenciamento de inventário, desafios e tarefas
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* **Criar tarefas** ◀︎ **Você está aqui** - Definir tarefas de desafio

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas em um desafio de fidelidade. Você pode configurar tipos de tarefa, quantidades e requisitos de produto para criar experiências de fidelidade envolventes e personalizadas.

Cada tarefa representa uma ação mensurável que contribui para a conclusão do desafio. As tarefas são componentes reutilizáveis que podem ser criados de forma independente e depois adicionados a um ou mais desafios, ou criados diretamente dentro de um desafio.

## Criar uma tarefa {#create-task}

É possível criar tarefas a partir de dois pontos de entrada. O processo de configuração é o mesmo, independentemente de onde você começa.

>[!BEGINTABS]

>[!TAB Do inventário de tarefas]

Selecione a guia **[!UICONTROL Tarefas]** e selecione **[!UICONTROL Criar tarefa]**.

![](assets/task-create-inventory.png)

As tarefas criadas no inventário são salvas e disponibilizadas para reutilização em vários desafios.

>[!TAB De dentro de um desafio]

Abrir um desafio existente ou criar um novo. Selecione **[!UICONTROL Adicionar tarefa]** e clique no botão **[!UICONTROL Novo]**.

![](assets/task-create-challenge.png)

Tarefas criadas dessa maneira são automaticamente adicionadas ao seu desafio e também salvas no inventário de Tarefas para reutilização em outros desafios.

>[!ENDTABS]

## Escolher atividade do cliente {#choose-activity}

Selecione o tipo de atividade que os clientes devem executar para concluir esta tarefa:

* **[!UICONTROL Compra]**: os clientes devem comprar um ou mais itens para concluir esta tarefa
* **[!UICONTROL Gastos]**: os clientes devem gastar um valor especificado para concluir esta tarefa

Para selecionar um tipo de atividade, clique no ícone `+` e selecione a atividade de cliente que melhor se alinha às suas metas de resultado. Cada tipo de atividade tem atributos configuráveis específicos para definir e moldar ainda mais os requisitos da tarefa.

![](assets/task-create-activitiy.png)

## Definir atributos {#define-attributes}

Configure os atributos da tarefa com base no tipo de atividade selecionado:

>[!BEGINTABS]

>[!TAB Atividade de compra]

![](assets/task-create-purchase.png)

Configure os seguintes atributos:

* **[!UICONTROL Quantidade]**: insira o número de itens que devem ser comprados para concluir esta tarefa
* **[!UICONTROL Itens qualificados e exclusões]**: defina itens ou grupos de itens que contam para a conclusão da tarefa e os que não contam. Saiba mais sobre [definição de itens qualificados e exclusões](#eligible-items-exclusions)

**Atributos opcionais** (ativados por meio do ícone de parâmetros):

* **[!UICONTROL Valor mínimo de gasto]**: definir um requisito de valor mínimo de compra
* **[!UICONTROL Número máximo de transações]**: limite quantas transações podem ser usadas para concluir a tarefa

>[!TAB Gastar atividade]

![](assets/task-create-spend.png)

Configure os seguintes atributos:

* **[!UICONTROL Valor]**: insira o valor total de gastos necessário para concluir a tarefa.
* **[!UICONTROL Número máximo de transações]**: especifique quantas transações podem atender ao requisito de gastos. Você pode desativar esse atributo do ícone de parâmetros se não quiser limitar o número de transações.
* **[!UICONTROL Itens qualificados e exclusões]**: (opcional) defina itens ou grupos de itens que contam para a conclusão de tarefas e os que não contam. Saiba mais sobre [definição de itens qualificados e exclusões](#eligible-items-exclusions)

>[!ENDTABS]

## Definir itens elegíveis e exclusões {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Para as atividades de **Compra** e **Gasto**, você pode usar o atributo **[!UICONTROL Itens qualificados e exclusões]** para definir quais itens e grupos estão qualificados e quais foram excluídos. Isso permite direcionar produtos, categorias ou locais específicos para se alinhar às suas metas de desafio.

Os casos de uso incluem: limitar uma tarefa de gastos a categorias de produtos específicas ou excluir cartões-presente ou itens promocionais da contagem para a conclusão da tarefa.

![](assets/tasks-create-eligible.png)

* Para definir itens qualificados, use a **[!UICONTROL As compras de tarefas qualificadas estão limitadas à seguinte seção]**. Insira IDs de item, categorias ou IDs de destino específicas, separadas por vírgulas.

  Exemplo: `SKU001, SKU002, CategoryA`

  Digite `*` para tornar todas as compras qualificadas (comportamento padrão se deixado em branco).

* Para excluir itens da tarefa, use a **[!UICONTROL Seção de tarefas]** a seguir. Insira IDs de item específicas, categorias ou IDs de destino que não devem contar para a conclusão da tarefa.

  Exemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

  >[!NOTE]
  >
  >As exclusões têm precedência sobre os itens elegíveis. Se um item corresponder a um item elegível e a uma exclusão, ele será excluído da tarefa.

## Definir propriedades da tarefa {#define-task-properties}

No painel de tarefas **[!UICONTROL Propriedades]**, configure as informações básicas da tarefa:

* **[!UICONTROL Nome da tarefa]**: digite um nome descritivo para a tarefa. Esse nome pode ser visto por você e sua equipe, mas pode não ser mostrado aos clientes dependendo do design do cartão de conteúdo.
* **[!UICONTROL Descrição da tarefa]**: a descrição é gerada automaticamente com base no tipo de atividade e nos atributos configurados para a tarefa. Você pode desativar a geração automática e inserir uma descrição personalizada, se necessário.

![](assets/tasks-create-properties.png)

Após configurar todos os atributos e propriedades, selecione **[!UICONTROL Criar]** para salvar a tarefa. A tarefa é salva no inventário de tarefas e, se criada a partir de um desafio, é automaticamente adicionada a esse desafio.
