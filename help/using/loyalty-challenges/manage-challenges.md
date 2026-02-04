---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar desafios de fidelidade
description: Saiba como gerenciar, monitorar e otimizar desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 1%

---


# Gerenciar desafios {#manage-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio
* **Gerenciar desafios** ◀︎ **Você está aqui** - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Gerenciar desafios {#manage-challenges-section}

### Desafiar o ciclo de vida {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

Os desafios passam por diferentes status durante seu ciclo de vida:

* **Rascunho**: o desafio está sendo criado ou editado e ainda não está disponível para os clientes
* **Agendado**: o desafio foi publicado e ficará ativo automaticamente na data de início especificada
* **Live**: o desafio está ativo no momento e os clientes podem participar
* **Concluído**: o desafio terminou - a data final já passou ou todos os objetivos foram atingidos
* **Parado**: o desafio foi manualmente parado antes de atingir sua conclusão natural
* **Arquivado**: o desafio foi arquivado para fins organizacionais e não está mais visível no inventário principal

### Editar desafios {#edit-challenges}

É possível editar os desafios dependendo de seu status atual:

* **Desafios de rascunho**: recurso de edição completo - todas as propriedades podem ser modificadas
* **Desafios agendados/ao vivo**: Edição limitada - você pode atualizar conteúdo, mensagens e estender datas, mas não pode alterar a estrutura do desafio principal (definições de tipo, público-alvo ou tarefa)

Para editar um desafio:

1. Navegue até a guia **[!UICONTROL Desafios]** no inventário de Desafios de Fidelidade.

1. Localize o desafio que deseja editar.

1. Selecione o nome do desafio para abri-lo no modo de edição.

1. Faça suas alterações com base no status do desafio:
   * **Desafios de rascunho**: modifique propriedades, tarefas, conteúdo ou mensagens
   * **Desafios agendados/ao vivo**: atualize cartões de conteúdo, mensagens ou estenda datas de término conforme necessário

1. Salve as alterações. Para desafios programados ou em tempo real, as alterações entram em vigor imediatamente ou de acordo com a programação de atualização.

>[!NOTE]
>
>Para alterações que exigem grandes modificações (como alterar o tipo de desafio, o público-alvo ou a estrutura de tarefas), duplique o desafio e crie uma nova versão em vez de editar a existente.

### Desafios duplicados {#duplicate-challenges}

Desafios duplicados para:

* Reexecutar desafios bem-sucedidos em novos períodos
* Criar variações para públicos diferentes
* Atualizar requisitos ou recompensas da tarefa
* Reativar desafios interrompidos ou concluídos

Duplicar um desafio cria uma cópia exata com todas as tarefas, conteúdo e mensagens intactas, permitindo que você crie rapidamente novas versões sem começar do zero.

Para duplicar um desafio:

1. Navegue até a guia **[!UICONTROL Desafios]** no inventário de Desafios de Fidelidade.

1. Localize o desafio que deseja duplicar.

1. Selecione o menu de mais ações (três pontos) ao lado desse desafio.

1. Escolha **[!UICONTROL Duplicar]**.

1. Uma cópia do desafio é criada com a &quot;[Cópia]&quot; anexada ao seu nome.

1. Abra o desafio duplicado e modifique as propriedades necessárias:
   * Atualizar o nome do desafio
   * Ajustar datas de início e término
   * Alterar o público-alvo, se necessário
   * Modifique tarefas, recompensas, conteúdo ou mensagens conforme necessário

1. Revise e publique o desafio duplicado.

### Monitorar desempenho {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Acompanhe o desempenho do desafio por meio das métricas principais:

* **Métricas de participação**:
   * Inscrição: número de clientes que se juntaram ao desafio
   * Participantes ativos: clientes atualmente envolvidos no desafio
* **Métricas de conclusão**:
   * Taxas de conclusão: Porcentagem de clientes inscritos que concluíram o desafio
   * Average completion time: Tempo médio necessário para concluir todas as tarefas
* **Métricas de recompensa**:
   * Total de recompensas distribuídas: valor agregado de todas as recompensas fornecidas
   * Recompensas por tipo: Detalhamento das recompensas por categoria de recompensa
* **Métricas de envolvimento**:
   * Impressões do cartão de conteúdo: Número de vezes que os cartões de conteúdo de desafio foram exibidos
   * Entrega de mensagem: contagem de mensagens enviadas com êxito em todos os canais

Para acessar os dados de desempenho:

1. Navegue até a guia **[!UICONTROL Desafios]** no inventário de Desafios de Fidelidade.

1. Selecione o desafio que deseja monitorar.

1. Abra a guia **[!UICONTROL Desempenho]** para exibir as métricas e análises em tempo real.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

Você também pode acessar dados detalhados de desempenho nos [relatórios de jornada gerados automaticamente](../reports/journey-global-report-cja.md), que fornecem insights adicionais e tendências históricas.

## Gerenciar tarefas {#manage-tasks}

As tarefas são componentes reutilizáveis que podem ser usados em vários desafios. O gerenciamento eficaz de tarefas garante a consistência em todo o programa de fidelidade e facilita a atualização central das definições de tarefas. As tarefas criadas em um desafio podem ser reutilizadas em outros desafios, reduzindo a duplicação e mantendo a padronização.

### Editar tarefas {#edit-tasks}

É possível editar tarefas existentes no Inventário de tarefas. Considere o seguinte:

* **Tarefas não usadas em desafios ativos**: podem ser editadas livremente - todas as propriedades podem ser modificadas sem impacto
* **Tarefas usadas em desafios dinâmicos**: tenha cuidado, pois as alterações afetam todos os desafios usando a tarefa. As modificações se aplicam imediatamente a todos os desafios de referência

Para editar uma tarefa:

1. Navegue até a guia **[!UICONTROL Tarefas]** no inventário de Desafios de Fidelidade.

1. Localize a tarefa que deseja editar.

1. Selecione o nome da tarefa para abri-la no modo de edição.

1. Modifique as propriedades da tarefa conforme necessário:
   * Atualizar nome ou descrição da tarefa
   * Alterar tipo ou atributos de atividade
   * Ajustar itens elegíveis e exclusões
   * Modificar necessidades de quantidade ou quantia

1. Salve as alterações.

>[!WARNING]
>
>Ao editar uma tarefa que seja usada ativamente em desafios em tempo real, considere criar uma duplicata com uma nova versão em vez de modificar a original. Isso evita alterações não intencionais em desafios ativos e permite testar as modificações antes de aplicá-las.

### Excluir tarefas {#delete-tasks}

As tarefas só podem ser excluídas se não estiverem sendo usadas atualmente em nenhum desafio. Antes de excluir uma tarefa:

* Verifique a contagem **[!UICONTROL Usados em desafios]** no inventário de tarefas
* Garantir que nenhum desafio de rascunho, agendado ou ativo faça referência à tarefa

Para excluir uma tarefa:

1. Navegue até a guia **[!UICONTROL Tarefas]** no inventário de Desafios de Fidelidade.

1. Localize a tarefa que deseja excluir.

1. Verifique se a contagem **[!UICONTROL Usado em desafios]** mostra 0. Se a contagem for maior que 0, você deverá primeiro remover a tarefa de todos os desafios antes de excluí-la.

1. Selecione o menu de mais ações (três pontos) ao lado da tarefa.

1. Escolha **[!UICONTROL Excluir]**.

1. Confirme a exclusão na caixa de diálogo.

>[!NOTE]
>
>Se uma tarefa for usada em qualquer desafio (rascunho, agendada ou ativa), você deverá primeiro removê-la de todos os desafios antes de excluí-la. Considere arquivar ou duplicar tarefas em vez de excluí-las, se necessário.
