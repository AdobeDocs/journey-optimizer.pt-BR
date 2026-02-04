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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Gerenciar desafios e tarefas {#manage-challenges}

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

### Estados de desafio {#challenge-lifecycle}

Os desafios passam por diferentes status durante seu ciclo de vida:

* **Rascunho**: o desafio está sendo criado ou editado e ainda não está disponível para os clientes.
* **Publicado**: o desafio está ativo e a jornada associada foi criada.

### Editar desafios {#edit-challenges}

Você pode editar desafios abrindo-os no inventário Desafios. O comportamento de edição é diferente dependendo do status de desafio:

**Desafios de rascunho**: você tem o recurso de edição completo. Todas as propriedades, tarefas, conteúdo e mensagens podem ser modificados sem restrições.

**Desafios publicados**: ao abrir um desafio publicado para edição, primeiro é necessário revertê-lo para o status Rascunho.

* Qualquer personalização feita diretamente na jornada gerada automaticamente será perdida.
* O desafio retorna ao status Rascunho.
* Depois de fazer suas alterações, você deve salvar e publicar o desafio novamente.
* Você deve republicar a jornada associada para disponibilizar o desafio atualizado para os clientes.

>[!IMPORTANT]
>
>Reverter um desafio publicado para rascunho não pode ser desfeito. Considere o impacto na jornada ativa antes de continuar.

### Desafios duplicados {#duplicate-challenges}

Duplicar um desafio cria uma cópia exata com todas as tarefas, conteúdo e mensagens intactas, permitindo que você crie rapidamente novas versões sem começar do zero.

Para duplicar um desafio:

1. Navegue até a guia **[!UICONTROL Desafios]** e localize o desafio que deseja duplicar.

1. Selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) ao lado desse desafio e escolha **[!UICONTROL Duplicar]**.

1. Uma cópia do desafio é criada. Abra o desafio duplicado e modifique as propriedades necessárias.

1. Salve o desafio duplicado e gere a jornada associada.

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

As tarefas são componentes reutilizáveis que podem ser usados em vários desafios. O gerenciamento eficaz de tarefas garante a consistência em todo o programa de fidelidade e facilita a atualização central das definições de tarefas. As tarefas criadas em um desafio podem ser reutilizadas em outros desafios, o que reduz a duplicação e mantém a padronização.

### Editar tarefas {#edit-tasks}

É possível editar tarefas existentes no Inventário de tarefas. Considere o seguinte:

* **Tarefas não usadas em desafios ativos**: podem ser editadas livremente. Todas as propriedades podem ser modificadas sem impacto.
* **Tarefas usadas em desafios dinâmicos**: tenha cuidado, pois as alterações afetam todos os desafios que usam a tarefa. As modificações se aplicam imediatamente a todos os desafios de referência.

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

* Verifique a contagem **[!UICONTROL Usados nos desafios]** no inventário de Tarefas.
* Certifique-se de que nenhum desafio de rascunho, agendado ou em tempo real faça referência à tarefa.

Para excluir uma tarefa:

1. Navegue até a guia **[!UICONTROL Tarefas]** no inventário de Desafios de Fidelidade.

1. Localize a tarefa que deseja excluir.

1. Verifique se a contagem **[!UICONTROL Usado em desafios]** mostra 0. Se a contagem for maior que 0, você deverá primeiro remover a tarefa de todos os desafios antes de excluí-la.

1. Selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) ao lado da tarefa.

1. Escolha **[!UICONTROL Excluir]**.

1. Confirme a exclusão na caixa de diálogo.

>[!NOTE]
>
>Se uma tarefa for usada em qualquer desafio (rascunho, agendada ou ativa), você deverá primeiro removê-la de todos os desafios antes de excluí-la. Considere arquivar ou duplicar tarefas em vez de excluí-las, se necessário.
