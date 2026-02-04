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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos Desafios de Fidelidade** ◀︎ **Você está aqui** - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Sobre os desafios de fidelidade"
>abstract="Os Desafios de fidelidade permitem criar ofertas de engajamento personalizadas que motivam os clientes a concluir ações específicas e ganhar recompensas."

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Entre em contato com o representante da Adobe para obter acesso.

## Visão geral {#overview}

Os Desafios de fidelidade fornecem uma solução completa para a criação de programas de fidelidade em escala, desde a definição de tarefas e marcos até o fornecimento de conteúdo e o rastreamento do desempenho em todos os canais. Você pode criar três tipos de experiências de desafio, configurar recompensas, enviar notificações de vários canais em estágios-chave do ciclo de vida e monitorar o desempenho por meio de jornadas geradas automaticamente — tudo isso enquanto mantém a integração com seu sistema externo de gerenciamento de fidelidade.

## Principais recursos {#key-capabilities}

Use os desafios de fidelidade para:

* **Crie três tipos de desafios**:
   * **Padrão**: os clientes concluem qualquer número de tarefas para receber recompensas
   * **Série**: os clientes concluem a mesma tarefa várias vezes consecutivamente
   * **Sequencial**: os clientes concluem as tarefas em uma ordem específica

* **Criar conteúdo de desafio**: use cartões de conteúdo do Journey Optimizer para criar a representação visual de seu desafio em dispositivos do cliente. Os cartões de conteúdo exibem as informações de desafio, o progresso e as recompensas.

* **Configurar requisitos da tarefa**: defina o que os clientes devem fazer para receber recompensas, incluindo:
   * Tipos de tarefa (compra, valor de gastos, visita, envolvimento, eventos personalizados)
   * Requisitos de quantidade
   * Inclusões/exclusões de produto usando SKUs, categorias ou atributos
   * Atributos e condições personalizados

* **Configurar recompensas**: defina as recompensas que os clientes ganharão ao concluir a tarefa (recompensas progressivas) ou após concluir todo o desafio (recompensas finais).

* **Enviar notificações de vários canais**: entregar mensagens em vários canais (no aplicativo, email, push) em estágios-chave:
   * **Inicialização**: quando o desafio começa
   * **Em andamento**: quando os clientes estão em processo
   * **Concluído**: quando os clientes concluírem o desafio

* **Acompanhe o desempenho**: monitore jornadas geradas automaticamente e analise o desempenho de desafios por meio de relatórios internos.

## Como funciona {#how-it-works}

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configure os conectores de origem do Experience Platform (como Capilar) para assimilar dados do evento de fidelidade que controlam as ações e o progresso do cliente.

2. **Criar um desafio** - Defina as propriedades básicas do desafio, incluindo nome, tipo (Padrão, Streak ou Sequencial), público-alvo e intervalo de datas.

3. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefas (compra, gastos, visitas, etc.), quantidades, filtros de produtos e recompensas.

4. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente.

5. **Configurar mensagens** (Opcional) - Configure mensagens multicanais (no aplicativo, email, push) para estágios principais: inicialização, em andamento e conclusão.

6. **Revisar e publicar** - Teste seu desafio com perfis de teste e publique-o para disponibilizá-lo para seu público-alvo.

7. **jornada gerada automaticamente** - Quando você publica, o Journey Optimizer cria automaticamente uma jornada que orquestra a entrega de cartões de conteúdo e mensagens.

8. **Ativar jornada** - A jornada gerada automaticamente é ativada na data de início do desafio e gerencia todas as interações com os clientes.

9. **Monitorar desempenho** - Acompanhe a participação, as taxas de conclusão, a distribuição de recompensas e o envolvimento com mensagens por meio de relatórios internos e da tela de jornada.

>[!NOTE]
>
>A jornada gerada automaticamente é exibida no inventário de jornadas e pode ser personalizada, se necessário. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio.

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

### Configuração de assimilação de dados {#data-ingestion}

Os desafios de fidelidade dependem dos dados assimilados pelos conectores de origem do Experience Platform para rastrear o progresso do cliente e a conclusão das tarefas.

1. **Configurar um conector de origem com suporte**: atualmente, o Conector Capilar está disponível. Conectores adicionais estão planejados.

2. **Validar assimilação de dados**: verifique se os eventos de fidelidade e os dados do cliente estão fluindo para o Experience Platform e disponíveis no Journey Optimizer.

Para obter instruções detalhadas, consulte:

* [Documentação de origens do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configurar conectores de origem no Journey Optimizer](../start/get-started-sources.md)

### Permissões necessárias {#required-permissions}

Para usar os Desafios de fidelidade, você precisa das permissões apropriadas no Journey Optimizer. Entre em contato com o administrador se não conseguir acessar o recurso.

### Públicos-alvo {#target-audiences}

Crie públicos-alvo no Experience Platform antes de criar desafios. Você pode selecionar públicos existentes, mas não pode criar novos públicos na interface dos Desafios de fidelidade.

## Limitações importantes {#limitations}

* **Nenhum sistema de razão**: os Desafios de Fidelidade não rastreiam valores monetários ou saldos de pontos. Quando os clientes concluem um desafio e ganham uma recompensa, a Journey Optimizer chama seu sistema de gerenciamento de fidelidade externo para lidar com a alocação de pontos.

* **Somente seleção de público-alvo**: você pode selecionar públicos-alvo existentes, mas não pode criar novos públicos-alvo na interface de desafios de fidelidade.

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
