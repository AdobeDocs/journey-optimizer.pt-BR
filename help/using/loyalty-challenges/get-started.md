---
solution: Journey Optimizer
product: journey optimizer
title: Entender os desafios da fidelidade
description: Saiba mais sobre os recursos, o fluxo de trabalho e os recursos dos Desafios de fidelidade na Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# Entender os desafios da fidelidade {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Sobre os desafios de fidelidade"
>abstract="Os Desafios de fidelidade permitem criar ofertas de engajamento personalizadas que motivam os clientes a concluir ações específicas e ganhar recompensas."

Os Desafios de fidelidade permitem projetar e implantar ofertas de envolvimento personalizadas que motivam os clientes a realizar ações específicas e receber recompensas.

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](gs-loyalty-challenges.md) - Visão geral rápida e próximas etapas
* **Entender os Desafios de Fidelidade** ◀︎ **Você está aqui** - Recursos, fluxo de trabalho, pré-requisitos
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

## Visão geral {#overview}

Os Desafios de fidelidade fornecem uma solução completa para a criação de programas de fidelidade em escala, desde a definição de tarefas e marcos até o fornecimento de conteúdo e o rastreamento do desempenho em todos os canais. Você pode criar três tipos de experiências de desafio, configurar recompensas, enviar notificações de vários canais em estágios-chave do ciclo de vida e monitorar o desempenho por meio de jornadas geradas automaticamente — tudo isso enquanto mantém a integração com seu sistema externo de gerenciamento de fidelidade.

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

## Principais recursos {#key-capabilities}

Use os desafios de fidelidade para:

* **Crie três tipos de desafios**:
   * **Padrão**: os clientes concluem qualquer número de tarefas para receber recompensas.
   * **Streak**: os clientes concluem a mesma tarefa várias vezes.
   * **Sequencial**: os clientes concluem as tarefas em uma ordem específica.

* **Criar conteúdo de desafio**: use cartões de conteúdo do Journey Optimizer para criar a representação visual de seu desafio em dispositivos do cliente. Os cartões de conteúdo exibem as informações de desafio, o progresso e as recompensas no dispositivo do cliente.

* **Configurar requisitos da tarefa**: defina o que os clientes devem fazer para receber recompensas, incluindo:
   * Tipos de tarefa (compra, valor de gasto, visita etc.)
   * Requisitos de quantidade
   * Inclusões/exclusões de produto usando SKUs
   * Atributos e condições personalizados

* **Configurar recompensas**: defina recompensas que os clientes ganharão ao concluir a tarefa ou após concluir todo o desafio

* **Enviar notificações**: entregar mensagens em vários canais (no aplicativo, email, push) em estágios-chave:
   * **Inicialização**: quando o desafio começa
   * **Em andamento**: quando os clientes estão em processo
   * **Concluído**: quando os clientes concluírem o desafio

* **Acompanhe o desempenho**: monitore jornadas geradas automaticamente e analise o desempenho do desafio

### Limitações importantes {#limitations}

* **Nenhum sistema de razão**: os Desafios de Fidelidade não rastreiam valores monetários ou saldos de pontos. Quando os clientes concluem um desafio e ganham uma recompensa, a Journey Optimizer chama seu sistema de gerenciamento de fidelidade externo para lidar com a alocação de pontos.

* **Somente seleção de público-alvo**: você pode selecionar públicos-alvo existentes, mas não pode criar novos públicos-alvo na interface de desafios de fidelidade.

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

## Desafios de fidelidade de acesso {#access}

Para acessar os desafios de fidelidade:

1. No Adobe Journey Optimizer, selecione **[!UICONTROL Desafios de fidelidade]** no menu de navegação esquerdo.

2. O inventário de desafios de fidelidade exibe todos os desafios existentes com informações como:
   * Nome e descrição do desafio
   * Status (Rascunho, Ao vivo, Interrompido etc.)
   * Tipo de desafio (Padrão, Streak, Sequencial)
   * Datas iniciais e finais
   * Data da última modificação

3. Selecione **[!UICONTROL Criar desafio]** para começar a criar um novo desafio.

### Pesquisar e filtrar desafios {#search-filter}

Use os recursos de pesquisa e filtragem para encontrar rapidamente desafios específicos:

* **Pesquisa**: insira o nome do desafio ou palavras-chave no campo Pesquisa
* **Filtrar por status**: Rascunho, Agendado, Ao Vivo, Concluído, Interrompido ou Arquivado
* **Filtrar por tipo**: desafios padrão, de Streak ou sequenciais
* **Filtrar por data**: desafios em um intervalo de datas específico
* **Filtrar por marcas**: desafios com marcas específicas aplicadas

## Próximas etapas {#next-steps}

Agora que você entende os desafios de fidelidade, saiba como criar seu primeiro desafio:

* [Criar desafios](create-challenges.md)
* [Gerenciar desafios](manage-challenges.md)
