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
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 3%

---


# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Entre em contato com o representante da Adobe para obter acesso.

Os Desafios de fidelidade permitem criar ofertas de envolvimento personalizadas para seus clientes, ajudando você a organizar programas de fidelidade em escala. Você pode projetar desafios com tarefas e marcos específicos, recompensar os clientes por concluí-los e fornecer a experiência por meio de canais da Adobe Journey Optimizer.

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos Desafios de Fidelidade** ◀︎ **Você está aqui** - Visão geral rápida e próximas etapas
* [Entender os desafios da fidelidade](get-started.md) - Recursos, fluxo de trabalho, pré-requisitos
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

## Visão geral rápida {#quick-overview}

Use os desafios de fidelidade para:

* **Crie três tipos de desafios**: Padrão (qualquer tarefa), Streak (tarefas repetidas) ou Sequencial (tarefas ordenadas)
* **Conteúdo de desafio de design**: use cartões de conteúdo para exibir desafios em dispositivos de clientes
* **Configurar requisitos da tarefa**: defina ações como compras, visitas ou eventos personalizados com recompensas
* **Enviar notificações de vários canais**: entregar mensagens no aplicativo, por email e por push em estágios-chave
* **Rastrear desempenho**: monitorar por meio de jornadas geradas automaticamente e relatórios internos

## Como funciona {#how-it-works-overview}

A criação de um desafio de fidelidade segue este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configurar conectores de origem para rastrear ações do cliente
2. **Criar um desafio** - Definir tipo, público-alvo e datas
3. **Adicionar tarefas** - Configurar ações e recompensas
4. **Criar conteúdo** - Criar cartões de conteúdo e mensagens opcionais
5. **Publicar** - o Journey Optimizer gera e ativa automaticamente uma jornada
6. **Monitor** - Acompanhe a participação e o desempenho

>[!NOTE]
>
>A jornada gerada automaticamente é exibida no inventário de jornadas e pode ser personalizada, se necessário. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio.

## Pré-requisitos {#prerequisites-overview}

Antes de usar os desafios de fidelidade:

* Configurar conectores de origem do Experience Platform (por exemplo, Capilar) para assimilar dados do evento de fidelidade
* Verifique se você tem as permissões apropriadas no Journey Optimizer
* Criar públicos-alvo na Experience Platform

Para obter pré-requisitos detalhados, consulte [Entender os desafios de fidelidade](get-started.md#prerequisites).

## Limitações importantes {#limitations-overview}

* **Nenhum sistema de razão**: os Desafios de Fidelidade não rastreiam valores monetários ou saldos de pontos. O Journey Optimizer chama seu sistema de gerenciamento de fidelidade externo para lidar com a alocação de pontos.
* **Somente seleção de público-alvo**: você pode selecionar públicos-alvo existentes, mas não pode criar novos públicos-alvo na interface de desafios de fidelidade.

## Próximas etapas {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="Compreender" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>Entender os desafios da fidelidade</strong></a>
    </div>
    <p>
    <em>Saiba mais sobre recursos, fluxo de trabalho e funcionalidades</em>
    <p>
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
    <p>
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
    <p>
  </td>
</tr>
</table>
