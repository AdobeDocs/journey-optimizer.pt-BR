---
solution: Journey Optimizer
product: journey optimizer
title: Desafios de fidelidade de acesso
description: Saiba como acessar, pesquisar e filtrar desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# Desafios de fidelidade de acesso {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* **Acessar Desafios de Fidelidade** ◀︎ **Você está aqui** - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Acessar o inventário de desafios de fidelidade {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

Para acessar os Desafios de Fidelidade, navegue até Journey Optimizer e selecione **[!UICONTROL Desafios de fidelidade]** na seção **[!UICONTROL jornadas do cliente]**.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

A página Desafios de fidelidade é exibida com duas guias:

* **[!UICONTROL Desafios]**: visualizar e gerenciar todos os desafios de fidelidade

* **[!UICONTROL Tarefas]**: exibir e gerenciar todas as tarefas que podem ser reutilizadas entre desafios

## Inventário de desafios {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

A guia Desafios exibe todos os desafios classificados por data da última modificação, com os desafios modificados mais recentemente aparecendo primeiro. As seguintes informações são exibidas:

* **[!UICONTROL Nome do desafio]**: o nome que você atribuiu ao desafio
* **[!UICONTROL Status]**: estado atual do desafio (consulte as descrições de status abaixo)
* **[!UICONTROL Tipo]**: tipo de desafio (Padrão, Streak ou Sequencial)
* **[!UICONTROL Data de início]**: quando o desafio se torna ativo
* **[!UICONTROL Data final]**: quando o desafio expira
* **[!UICONTROL Criado por]**: usuário que criou o desafio
* **[!UICONTROL Última modificação]**: data e hora da última modificação
* **[!UICONTROL Marcas]**: todas as marcas aplicadas ao desafio da organização

### Status de desafio {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

Os desafios são exibidos com status diferentes, indicando seu estado atual no ciclo de vida:

* **Rascunho**: O desafio está sendo criado ou editado
* **Agendado**: o desafio foi publicado e ficará ativo na data de início
* **Live**: o desafio está ativo e os clientes podem participar
* **Concluído**: a data de término do desafio passou ou os objetivos foram atingidos
* **Parado**: o desafio foi manualmente parado antes da conclusão
* **Arquivado**: o desafio foi arquivado para fins organizacionais

Para obter informações detalhadas sobre as transições de status e o ciclo de vida de desafio, consulte [Ciclo de vida de desafio](manage-challenges.md#challenge-lifecycle).

### Pesquisar e filtrar desafios {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

Você pode localizar desafios rapidamente usando pesquisa e filtros:

**Pesquisar:**

* Use a barra de pesquisa para encontrar desafios, inserindo palavras-chave do nome ou da descrição do desafio. As atualizações de pesquisa resultam em tempo real à medida que você digita.

**Filtros:**

* Aplique um ou mais filtros para restringir seus resultados:
   * **Status**: filtrar por status de desafio (Rascunho, Agendado, Ao Vivo, Concluído, Interrompido, Arquivado)
   * **Tipo**: filtrar por tipo de desafio (Padrão, Streak, Sequencial)
   * **Datas**: filtrar por intervalos de datas de início ou término
   * **Marcas**: filtrar por marcas aplicadas a desafios

É possível combinar vários filtros simultaneamente. Por exemplo, filtre por desafios do Live Standard marcados com &quot;Verão de 2024&quot; para encontrar rapidamente campanhas sazonais ativas.

Para limpar filtros, selecione **[!UICONTROL Limpar tudo]** ou remover filtros individuais.

### Realizar ações em relação aos desafios {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

Na guia Desafios, é possível executar ações rápidas em desafios:

* **Exibir detalhes do desafio**: selecione o nome do desafio para abrir sua página de detalhes
* **Editar um desafio**: selecione o menu **[!UICONTROL Mais ações]** (três pontos) e escolha **[!UICONTROL Editar]**
* **Duplicar um desafio**: selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Duplicar]**
* **Parar um desafio em tempo real**: selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Parar]**
* **Arquivar um desafio**: selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Arquivar]**
* **Excluir um desafio de rascunho**: Selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Excluir]** (disponível somente para rascunhos)

Para obter informações detalhadas sobre como gerenciar desafios após a criação, incluindo limitações de edição, estratégias de duplicação, monitoramento de desempenho e solução de problemas, consulte [Gerenciar desafios](manage-challenges.md).

## Inventário de tarefas {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

A guia Tasks exibe todas as tarefas reutilizáveis que podem ser usadas em vários desafios. As tarefas criadas aqui ficam disponíveis para seleção ao criar ou editar qualquer desafio.

O inventário de tarefas exibe as seguintes informações:

* **[!UICONTROL Nome da tarefa]**: o nome que você atribuiu à tarefa
* **[!UICONTROL Tipo de tarefa]**: tipo de ação (Compra, Valor do gasto, Visita, Envolvimento, Evento personalizado)
* **[!UICONTROL Descrição]**: breve descrição do que a tarefa exige
* **[!UICONTROL Criado por]**: usuário que criou a tarefa
* **[!UICONTROL Última modificação]**: data e hora da última modificação
* **[!UICONTROL Usado em desafios]**: Número de desafios que estão usando esta tarefa no momento

### Realizar ações em tarefas {#tasks-actions}

Na guia Tasks (Tarefas), é possível executar ações em tarefas:

* **Exibir detalhes da tarefa**: selecione o nome da tarefa para exibir a configuração completa
* **Editar uma tarefa**: selecione o menu **[!UICONTROL Mais ações]** (três pontos) e escolha **[!UICONTROL Editar]**
* **Duplicar uma tarefa**: selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Duplicar]**
* **Excluir uma tarefa**: selecione o menu **[!UICONTROL Mais ações]** e escolha **[!UICONTROL Excluir]** (somente se não for usado em nenhum desafio ativo)
* **Uso da exibição**: veja quais desafios estão usando a tarefa no momento

## Próximas etapas {#next-steps}

Agora que você sabe como acessar e navegar pelo inventário de desafios de fidelidade:

* [Criar desafios](create-challenges.md) - Saiba como criar seu primeiro desafio e configurar tarefas
* [Criar tarefas](create-tasks.md) - Saiba como definir tarefas reutilizáveis para desafios
* [Gerenciar desafios](manage-challenges.md) - Saiba como editar, monitorar e otimizar desafios
