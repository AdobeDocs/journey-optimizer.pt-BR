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
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: 8907c18e-4623-4743-a76b-333f34e13baf
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 4%

---

# Acessar e gerenciar desafios e tarefas {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Sumário**

[Introdução aos desafios de fidelidade](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Criar e gerenciar desafios**

* **Acessar e gerenciar desafios e tarefas** ◀︎ **Você está aqui**
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configurar desafios de fidelidade](loyalty-admin.md)
* [Guia de definição de recompensa](reward-definition-guide.md)
* [Guia do Transformador de eventos](event-transformer-guide.md)
* [Dados e conjuntos de dados de fidelidade](loyalty-data-and-datasets.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

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
* **[!UICONTROL Status]**: status atual da jornada gerada automaticamente que fornece o desafio.
* **[!UICONTROL Data de Início/Término (UTC)]**: quando o desafio se torna ativo e expira

Na guia Desafios, é possível executar ações em desafios:

* **Exibir desafio**: selecione o nome do desafio para abrir sua página de detalhes
* **Duplicar um desafio**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Duplicar]**. Uma cópia é criada com todas as tarefas, conteúdo e mensagens intactas.
* **Excluir um desafio**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Excluir]**.

  >[!IMPORTANT]
  >
  >Você pode excluir um desafio mesmo quando ele é publicado. Considere o impacto antes de excluir.

* **Editar um desafio**: selecione o nome do desafio para abrir sua página de detalhes e fazer as alterações desejadas.

  Ao abrir um desafio publicado para edição, primeiro é necessário revertê-lo para o estado Rascunho. Qualquer personalização feita diretamente na jornada gerada automaticamente será perdida. Depois de fazer suas alterações, salve e publique o desafio novamente e, em seguida, publique a jornada associada. [Saiba como iniciar um desafio](create-challenges.md#launch)

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
* **Excluir uma tarefa**: selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Excluir]**.

  >[!IMPORTANT]
  >
  >Você pode excluir uma tarefa mesmo quando ela é usada em um ou mais desafios. Considere o impacto nos desafios que fazem referência à tarefa antes de excluir.
