---
solution: Journey Optimizer
product: journey optimizer
title: Acesse e gerencie os desafios de fidelidade
description: Saiba como acessar, gerenciar e organizar desafios e tarefas de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Acesse e gerencie os desafios de fidelidade {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* **Acessar Desafios de Fidelidade** ◀︎ **Você está aqui** - Gerenciamento de inventário, desafios e tarefas
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Acesse os desafios leais

Para acessar os Desafios de Fidelidade, navegue até Journey Optimizer e selecione **[!UICONTROL Desafio de Fidelidade (Beta)]** na seção **[!UICONTROL Gerenciamento de Jornada]**.

A interface dos desafios de fidelidade fornece um local centralizado para exibir, gerenciar e organizar todos os seus desafios e tarefas. Você pode acessar dois inventários principais:

* **Inventário de desafios**: visualize e gerencie todos os desafios de fidelidade, monitore seu status e execute ações rápidas
* **Inventário de tarefas**: procure tarefas reutilizáveis que possam ser usadas em vários desafios

## Inventário de desafios {#challenges-tab}

A guia **[!UICONTROL Desafios]** exibe todos os desafios classificados por data da última modificação, com os desafios modificados mais recentemente aparecendo primeiro.

![](assets/challenges-inventory.png)

Informações-chave exibidas:

* **[!UICONTROL Desafio]**: nome do desafio
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

  Ao abrir um desafio publicado para edição, primeiro é necessário revertê-lo para o status Rascunho:

   * Qualquer personalização feita diretamente na jornada gerada automaticamente será perdida
   * O desafio retorna ao status Rascunho
   * Depois de fazer suas alterações, você deve salvar e publicar o desafio novamente
   * Você deve republicar a jornada associada para disponibilizar o desafio atualizado para os clientes

  >[!IMPORTANT]
  >
  >Reverter um desafio publicado para rascunho não pode ser desfeito. Considere o impacto na jornada ativa antes de continuar.

## Inventário de tarefas {#tasks-tab}

A guia **[!UICONTROL Tarefas]** exibe todas as tarefas reutilizáveis que podem ser usadas em vários desafios. As tarefas criadas aqui ficam disponíveis para seleção ao criar ou editar qualquer desafio.

![](assets/tasks-inventory.png)

Informações-chave exibidas:

* **[!UICONTROL Nome da tarefa]**: o nome que você atribuiu à tarefa
* **[!UICONTROL Descrição]**: breve descrição do que a tarefa exige
* **[!UICONTROL Atividade da tarefa]**: tipo de atividade (Compra, Gasto)
* **[!UICONTROL SKU]**: itens qualificados e/ou excluídos
* **[!UICONTROL Usado em desafios]**: Número de desafios que estão usando esta tarefa no momento

Na guia Tasks (Tarefas), é possível executar ações em tarefas:

* **Exibir/Editar tarefa**: selecione o nome da tarefa para exibir a configuração completa e editar a tarefa
* **Duplicar uma tarefa**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Duplicar]**
* **Excluir uma tarefa**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Excluir]**
