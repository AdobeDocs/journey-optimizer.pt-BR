---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar desafios e tarefas
description: Saiba como acessar, gerenciar e organizar desafios e tarefas de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
source-git-commit: 342df0950622de1c4c246bf624d05843671e199f
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---


# Acessar e gerenciar desafios e tarefas {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos desafios de fidelidade](get-started.md)
* **Acessar e gerenciar desafios e tarefas** ◀︎ **Você está aqui**
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Acessar e gerenciar desafios e tarefas

Para acessar os Desafios de Fidelidade, navegue até Journey Optimizer e selecione **[!UICONTROL Desafio de Fidelidade (Beta)]** na seção **[!UICONTROL Gerenciamento de Jornada]**. A interface dos desafios de fidelidade fornece um local centralizado para exibir, gerenciar e organizar todos os seus desafios e tarefas.

A interface fornece acesso a dois inventários principais:

* **Desafios**: visualize e gerencie todos os desafios de fidelidade, monitore seus status e execute ações rápidas, como visualizar, editar, duplicar ou excluir desafios
* **Tarefas**: procure tarefas reutilizáveis que possam ser usadas em vários desafios e gerencie definições de tarefas independentemente


## Inventário de desafios {#challenges-tab}

A guia **[!UICONTROL Desafios]** exibe todos os desafios classificados por data da última modificação, com os desafios modificados mais recentemente aparecendo primeiro.

![](assets/challenges-inventory.png)

Informações-chave exibidas:

* **[!UICONTROL Estado]**: estado atual do desafio (Rascunho ou Publicado)
* **[!UICONTROL Tarefas]**: Número de tarefas configuradas no desafio
* **[!UICONTROL Jornada]**: link para a jornada gerada automaticamente associada ao desafio
* **[!UICONTROL Status]**: status atual da jornada associada (Rascunho, Ao Vivo, Parado, etc.)
* **[!UICONTROL Data de Início/Término (UTC)]**: quando o desafio se torna ativo e expira

Na guia Desafios, é possível executar ações em desafios:

* **Exibir desafio**: selecione o nome do desafio para abrir sua página de detalhes
* **Duplicar um desafio**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Duplicar]**. Uma cópia é criada com todas as tarefas, conteúdo e mensagens intactas.
* **Excluir um desafio**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Excluir]**
* **Editar um desafio**: selecione o nome do desafio para abrir sua página de detalhes e editá-lo.

  Ao abrir um desafio publicado para edição, primeiro é necessário revertê-lo para o status &quot;Rascunho&quot;. Qualquer personalização feita diretamente na jornada gerada automaticamente será perdida. Depois de fazer suas alterações, salve e publique o desafio novamente e publique novamente a jornada associada.

  >[!IMPORTANT]
  >
  >Reverter um desafio publicado para rascunho não pode ser desfeito. Considere o impacto na jornada ativa antes de continuar.

## Inventário de tarefas {#tasks-tab}

A guia **[!UICONTROL Tarefas]** exibe todas as tarefas reutilizáveis que podem ser usadas em vários desafios. As tarefas criadas aqui ficam disponíveis para seleção ao criar ou editar qualquer desafio.

![](assets/tasks-inventory.png)

Informações-chave exibidas:

* **[!UICONTROL Descrição]**: breve descrição do que a tarefa exige
* **[!UICONTROL Atividade da tarefa]**: tipo de atividade (Compra, Gasto)
* **[!UICONTROL SKU]**: itens qualificados e/ou excluídos
* **[!UICONTROL Usado em desafios]**: Número de desafios que estão usando esta tarefa no momento

Na guia Tasks (Tarefas), é possível executar ações em tarefas:

* **Exibir/Editar uma tarefa**: selecione o nome da tarefa para exibir a configuração completa e editar a tarefa
* **Duplicar uma tarefa**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Duplicar]**
* **Excluir uma tarefa**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Excluir]**
