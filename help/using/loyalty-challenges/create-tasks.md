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
mini-toc-levels: 2
source-git-commit: 43d3593264ea6d33794914e1b1f9ea45c295c79e
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---


# Criar tarefas {#create-tasks}

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md) - Gerenciamento de inventário, desafio e tarefa
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* **Criar tarefas** ◀︎ **Você está aqui** - Definir tarefas de desafio

>[!ENDSHADEBOX]

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas em um desafio de fidelidade. Você pode configurar tipos de tarefa, quantidades e requisitos de produto para criar experiências de fidelidade envolventes e personalizadas.

Cada tarefa representa uma ação mensurável que contribui para a conclusão do desafio. As tarefas são componentes reutilizáveis que podem ser criados de forma independente e depois adicionados a um ou mais desafios, ou criados diretamente dentro de um desafio.

## Criar uma tarefa {#create-task}

É possível criar tarefas a partir de dois pontos de entrada. O processo de configuração é o mesmo, independentemente de onde você começa.

>[!BEGINTABS]

>[!TAB Do inventário de tarefas]

Selecione a guia **[!UICONTROL Tarefas]** e selecione **[!UICONTROL Criar tarefa]**. As tarefas criadas no inventário são salvas e disponibilizadas para reutilização em vários desafios.

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
