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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 1%

---


# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos Desafios de Fidelidade** ◀︎ **Você está aqui** - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar e gerenciar desafios de fidelidade](access-loyalty-challenges.md) - gerenciamento de inventário, desafios e tarefas
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Visão geral {#overview}

Os desafios de fidelidade fornecem uma solução completa para a criação de programas de fidelidade em escala, desde a definição de tarefas e marcos até o fornecimento de conteúdo e o rastreamento do desempenho em todos os canais.

![](assets/challenges-gs.png)

Você pode criar três tipos de experiências de desafio:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem\
  *Exemplo: Concluir 3 de 5 tarefas disponíveis*

* **Distribuir desafios**: os clientes concluem a mesma tarefa várias vezes consecutivamente\
  *Exemplo: faça uma compra em 7 dias consecutivos*

* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida\
  *Exemplo: Compra → Revisão → Compartilhar (deve ser concluído nesta sequência)*

Com os desafios de fidelidade, configure recompensas, envie notificações de vários canais em estágios-chave do ciclo de vida, usando jornadas geradas automaticamente — tudo isso enquanto mantém a integração com seu sistema externo de gerenciamento de fidelidade.

## Como funciona {#how-it-works}

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configure os conectores de origem do Experience Platform (como o [Conector capilar](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/home#loyalty)) para assimilar dados do evento de fidelidade que controlam o progresso e as ações do cliente. Esses dados possibilitam o rastreamento de desafios e a conclusão de tarefas.

1. **Criar um desafio** - Defina as propriedades de desafio básicas, incluindo nome, tipo (Padrão, Streak ou Sequencial) e intervalo de datas.

1. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefa (compra, gastos), quantidades, filtros de produto e recompensas.

1. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente. Os cartões de conteúdo mostram informações de desafio, progresso e recompensas.

1. **Configurar mensagens** (Opcional) - Configure mensagens multicanais (no aplicativo, email, push) para os principais estágios do ciclo de vida: inicialização, em andamento e conclusão.

1. **Selecionar público-alvo** - Defina quais clientes podem participar do seu desafio selecionando um público-alvo da Adobe Experience Platform.

1. **Publicar jornada** - O Journey Optimizer gera automaticamente uma jornada para o desafio. Navegue até o inventário de Jornadas e publique a jornada gerada automaticamente para disponibilizar o desafio aos clientes.

Para obter instruções detalhadas, consulte [Criar desafios](create-challenges.md).

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

+++Configuração de assimilação de dados

Os desafios de fidelidade dependem dos dados assimilados pelos conectores de origem da Experience Platform para rastrear o progresso do cliente e a conclusão das tarefas.

1. **Configurar um conector de origem com suporte**: atualmente, o Conector Capilar está disponível. Conectores adicionais estão planejados para versões futuras. [Saiba mais sobre conectores de origem de fidelidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/home#loyalty).

1. **Validar assimilação de dados**: verifique se os eventos de fidelidade e os dados do cliente estão fluindo para o Experience Platform e disponíveis no Journey Optimizer. Verifique se o esquema de dados inclui os campos necessários para rastrear as ações e o progresso do cliente.

Para obter instruções detalhadas, consulte [visão geral das fontes do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/home)

+++

+++Permissões necessárias

Para usar os Desafios de fidelidade, você precisa das permissões apropriadas no Journey Optimizer. As permissões necessárias incluem:

* Acesso ao recurso **[!UICONTROL Desafios de Fidelidade (Beta)]**
* Permissões para criar e gerenciar jornadas
* Permissões para criar e gerenciar cartões de conteúdo
* Permissões para criar e gerenciar públicos

Entre em contato com o administrador se não conseguir acessar o recurso ou precisar de permissões adicionais.

+++

+++Público-alvo

Defina um público-alvo que especifique quais clientes estão qualificados para participar de seus desafios de fidelidade. Você pode selecionar públicos existentes ou criar novos diretamente da interface de criação de desafios. [Saiba como trabalhar com públicos](../audience/about-audiences.md).

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
    <em>Definir ações a serem concluídas para desafios</em>
    </p>
  </td>
</tr>
</table>
