---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos desafios de fidelidade
description: Saiba como criar e gerenciar desafios de fidelidade no Adobe Journey Optimizer para criar programas de fidelidade envolventes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: bd98e4dc77a0adde83df6251af749aa6da8c058d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos Desafios de Fidelidade** ◀︎ **Você está aqui** - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Visão geral {#overview}

Os desafios de fidelidade fornecem uma solução completa para a criação de programas de fidelidade em escala, desde a definição de tarefas e marcos até o fornecimento de conteúdo e o rastreamento do desempenho em todos os canais.

Você pode criar três tipos de experiências de desafio:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem
* **Distribuir desafios**: os clientes concluem a mesma tarefa várias vezes consecutivamente
* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida

Com os desafios de fidelidade, você pode configurar recompensas, enviar notificações de vários canais em estágios-chave do ciclo de vida e monitorar o desempenho por meio de jornadas geradas automaticamente — tudo isso mantendo a integração com seu sistema externo de gerenciamento de fidelidade.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Como funciona {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configure os conectores de origem do Experience Platform (como o Conector Capilar) para assimilar dados do evento de fidelidade que controlam as ações e o progresso do cliente. Esses dados possibilitam o rastreamento de desafios e a conclusão de tarefas.

1. **Criar um desafio** - Defina as propriedades básicas do desafio, incluindo nome, tipo (Padrão, Streak ou Sequencial), público-alvo e intervalo de datas. Consulte [Criar desafios](create-challenges.md) para obter etapas detalhadas.

1. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefas (compra, gastos, visitas, envolvimento, eventos personalizados), quantidades, filtros de produtos e recompensas. Consulte [Criar tarefas](create-tasks.md) para obter instruções detalhadas.

1. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando os [cartões de conteúdo](../content-card/create-content-card.md) do Journey Optimizer exibidos nos dispositivos do cliente. Os cartões de conteúdo mostram informações de desafio, progresso e recompensas.

1. **Configurar mensagens** (Opcional) - Configure mensagens multicanais ([no aplicativo](../in-app/get-started-in-app.md), [email](../email/get-started-email.md), [push](../push/get-started-push.md)) para estágios-chave do ciclo de vida: inicialização, em andamento e conclusão.

1. **Revisar e publicar** - Teste seu desafio com [perfis de teste](../test-approve/test-profiles.md) e publique-o para disponibilizá-lo para seu público-alvo.

1. **Ativar jornada** - Quando você publica um desafio, o Journey Optimizer cria automaticamente uma [jornada](../building-journeys/journey-gs.md) no status Rascunho que orquestra a entrega de cartões de conteúdo e as mensagens. Navegue até o inventário do Jornada, localize a jornada gerada automaticamente (chamada &quot;Desafio: [Nome do Desafio]&quot;) e [ative-a](../building-journeys/publishing-the-journey.md) para disponibilizar o desafio aos seus clientes.

1. **Monitorar desempenho** - Acompanhe a participação, as taxas de conclusão, a distribuição de recompensas e o envolvimento com mensagens por meio de relatórios internos e da tela de jornada. Consulte [Gerenciar desafios](manage-challenges.md) para obter detalhes sobre o monitoramento.

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

+++Configuração de assimilação de dados

Os desafios de fidelidade dependem dos dados assimilados pelos conectores de origem da Experience Platform para rastrear o progresso do cliente e a conclusão das tarefas.

1. **Configurar um conector de origem com suporte**: atualmente, o Conector Capilar está disponível. Conectores adicionais estão planejados para versões futuras.

1. **Validar assimilação de dados**: verifique se os eventos de fidelidade e os dados do cliente estão fluindo para o Experience Platform e disponíveis no Journey Optimizer. Verifique se o esquema de dados inclui os campos necessários para rastrear as ações e o progresso do cliente.

Para obter instruções detalhadas, consulte:

* [Documentação de origens do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configurar conectores de origem no Journey Optimizer](../start/get-started-sources.md)

+++

+++Permissões necessárias

Para usar os Desafios de fidelidade, você precisa das permissões apropriadas no Journey Optimizer. As permissões necessárias incluem:

* Acesso ao recurso **[!UICONTROL Desafios de fidelidade]**
* Permissões para criar e gerenciar jornadas
* Permissões para criar e gerenciar cartões de conteúdo
* Permissões para criar e gerenciar públicos

Entre em contato com o administrador se não conseguir acessar o recurso ou precisar de permissões adicionais.

+++

+++Públicos-alvo

Crie públicos-alvo no Experience Platform antes de criar desafios. Esses públicos-alvo definem quais clientes estão qualificados para participar de seus desafios de fidelidade. Para obter mais informações sobre como criar públicos, consulte [Introdução aos públicos](../audience/about-audiences.md).

+++

## Próximas etapas {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Acessar Desafios de Fidelidade</strong></a>
    </div>
    <p>
    <em>Saiba como acessar o inventário e filtrar desafios</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Criar desafios</strong></a>
    </div>
    <p>
    <em>Crie e configure seu primeiro desafio de fidelidade</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Criar tarefas</strong></a>
    </div>
    <p>
    <em>Definir ações e recompensas para desafios</em>
    </p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Gerenciar desafios</strong></a>
    </div>
    <p>
    <em>Editar, monitorar e otimizar desafios</em>
    </p>
  </td>
</tr>
</table>
