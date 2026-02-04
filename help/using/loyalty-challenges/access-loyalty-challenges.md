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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Desafios de fidelidade de acesso {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* **Acessar Desafios de Fidelidade** ◀︎ **Você está aqui** - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

## Acessar o inventário de desafios de fidelidade {#access-inventory}

Para acessar os desafios de fidelidade:

1. No Adobe Journey Optimizer, selecione **[!UICONTROL Desafios de fidelidade]** no menu de navegação esquerdo, na seção **[!UICONTROL jornadas do cliente]**.

2. A página Desafios de fidelidade é exibida com duas guias:
   * **[!UICONTROL Desafios]**: visualizar e gerenciar todos os desafios de fidelidade
   * **[!UICONTROL Tarefas]**: exibir e gerenciar todas as tarefas que podem ser reutilizadas entre desafios

Por padrão, a guia **[!UICONTROL Desafios]** é selecionada, mostrando todos os desafios existentes em sua organização.

## Guia Desafios {#challenges-tab}

A guia Desafios exibe todos os desafios classificados por data da última modificação, com os desafios modificados mais recentemente aparecendo primeiro.

### Compreender o inventário de desafios {#inventory-overview}

O inventário Desafios exibe todos os desafios com as seguintes informações:

* **[!UICONTROL Nome do desafio]**: o nome que você atribuiu ao desafio
* **[!UICONTROL Status]**: estado atual do desafio (consulte as descrições de status abaixo)
* **[!UICONTROL Tipo]**: tipo de desafio (Padrão, Streak ou Sequencial)
* **[!UICONTROL Data de início]**: quando o desafio se torna ativo
* **[!UICONTROL Data final]**: quando o desafio expira
* **[!UICONTROL Criado por]**: usuário que criou o desafio
* **[!UICONTROL Última modificação]**: data e hora da última modificação
* **[!UICONTROL Marcas]**: todas as marcas aplicadas ao desafio da organização

### Status de desafio {#challenge-statuses}

Os desafios podem ter os seguintes status:

* **[!UICONTROL Rascunho]**: o desafio está sendo criado ou editado, mas ainda não foi publicado
* **[!UICONTROL Agendado]**: o desafio foi publicado e está agendado para iniciar em uma data futura
* **[!UICONTROL Live]**: o desafio está ativo no momento e disponível para o público-alvo
* **[!UICONTROL Concluído]**: o desafio ultrapassou sua data de término ou todos os objetivos foram atingidos
* **[!UICONTROL Parado]**: o desafio foi manualmente parado antes da conclusão
* **[!UICONTROL Arquivado]**: o desafio foi arquivado para fins organizacionais

### Pesquisar e filtrar desafios {#search-challenges}

Use a funcionalidade de pesquisa para encontrar rapidamente desafios específicos por nome ou descrição.

Também é possível aplicar filtros para restringir a lista de desafios com base em critérios específicos. É possível combinar vários filtros para refinar a pesquisa.

Você pode filtrar os desafios pelo status atual, pelo tipo de desafio, com base nas datas de início ou término, ou pelas tags aplicadas para a organização.

### Realizar ações em relação aos desafios {#inventory-actions}

Na guia Desafios, é possível executar ações rápidas em desafios:

* **Exibir detalhes do desafio**: selecione um nome de desafio para abrir sua página de detalhes
* **Editar um desafio**: selecione o menu de mais ações (três pontos) e escolha **[!UICONTROL Editar]**
* **Duplicar um desafio**: selecione o menu de mais ações e escolha **[!UICONTROL Duplicar]**
* **Parar um desafio em tempo real**: selecione o menu de mais ações e escolha **[!UICONTROL Parar]**
* **Arquivar um desafio**: selecione o menu de mais ações e escolha **[!UICONTROL Arquivar]**
* **Excluir um desafio de rascunho**: Selecione o menu de mais ações e escolha **[!UICONTROL Excluir]** (disponível somente para rascunhos)

### Criar um novo desafio {#create-from-inventory}

Para criar um novo desafio na guia Desafios:

1. Selecione **[!UICONTROL Criar desafio]** no canto superior direito.

2. O fluxo de trabalho de criação do desafio é iniciado.

Para obter instruções detalhadas, consulte [Criar desafios](create-challenges.md).

## Guia Tarefas {#tasks-tab}

A guia Tasks exibe todas as tarefas reutilizáveis que podem ser usadas em vários desafios. As tarefas criadas aqui ficam disponíveis para seleção ao criar ou editar qualquer desafio.

### Noções básicas sobre o inventário de tarefas {#tasks-inventory-overview}

O inventário de tarefas exibe todas as tarefas com as seguintes informações:

* **[!UICONTROL Nome da tarefa]**: o nome que você atribuiu à tarefa
* **[!UICONTROL Tipo de tarefa]**: tipo de ação (Compra, Valor do gasto, Visita, Envolvimento, Evento personalizado)
* **[!UICONTROL Descrição]**: breve descrição do que a tarefa exige
* **[!UICONTROL Criado por]**: usuário que criou a tarefa
* **[!UICONTROL Última modificação]**: data e hora da última modificação
* **[!UICONTROL Usado em desafios]**: Número de desafios que estão usando esta tarefa no momento

### Criar tarefas na guia Tarefas {#create-tasks-from-tab}

É possível criar tarefas de duas maneiras:

1. **Na guia Tarefas** (recomendado para tarefas reutilizáveis):
   * Navegue até a guia **[!UICONTROL Tarefas]**
   * Selecione **[!UICONTROL Criar tarefa]**
   * Configurar as propriedades da tarefa (nome, tipo, quantidade, filtros de produto, prêmios)
   * Salve a tarefa para disponibilizá-la para uso em qualquer desafio

2. **Ao criar um desafio** (para tarefas específicas de desafio):
   * Durante a criação do desafio, selecione **[!UICONTROL Adicionar tarefa]** na seção Tarefas
   * Escolha **[!UICONTROL Criar nova tarefa]** ou selecione uma das tarefas existentes
   * Tarefas criadas dessa maneira também são salvas no inventário de Tarefas e podem ser reutilizadas

>[!TIP]
>
>Criar tarefas a partir da guia Tasks é recomendado quando você planeja usar a mesma tarefa em vários desafios. Isso garante a consistência e facilita a atualização central das definições de tarefa.

### Realizar ações em tarefas {#tasks-actions}

Na guia Tasks (Tarefas), é possível executar ações em tarefas:

* **Exibir detalhes da tarefa**: selecione um nome de tarefa para exibir a configuração completa
* **Editar uma tarefa**: selecione o menu de mais ações (três pontos) e escolha **[!UICONTROL Editar]**
* **Duplicar uma tarefa**: selecione o menu de mais ações e escolha **[!UICONTROL Duplicar]**
* **Excluir uma tarefa**: selecione o menu de mais ações e escolha **[!UICONTROL Excluir]** (somente se não for usado em nenhum desafio ativo)
* **Uso da exibição**: veja quais desafios estão usando a tarefa no momento

## Próximas etapas {#next-steps}

Agora que você sabe como acessar e navegar pelo inventário de desafios de fidelidade:

* [Criar desafios](create-challenges.md) - Saiba como criar seu primeiro desafio
* [Gerenciar desafios](manage-challenges.md) - Saiba como editar e monitorar desafios
