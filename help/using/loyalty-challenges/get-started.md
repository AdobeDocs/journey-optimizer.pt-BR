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
mini-toc-levels: 1
source-git-commit: 94b553b19dbb0ba3020979fa710c2c35af237816
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 1%

---


# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos Desafios de Fidelidade** ◀︎ **Você está aqui** - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md) - Gerenciamento de inventário, desafio e tarefa
* [Criar desafios](create-challenges.md) - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio

>[!ENDSHADEBOX]

## Visão geral {#overview}

Os desafios de fidelidade permitem criar programas de fidelidade envolventes e gamificados que impulsionam o comportamento do cliente e aprofundam os relacionamentos com a marca. Crie desafios que recompensem os clientes por ações específicas, desde fazer compras e escrever avaliações até se envolver com redes sociais e fazer referência a amigos.

Com os desafios de fidelidade, você pode:

* **Crie tipos de desafios flexíveis**: Crie desafios Padrão, Streak ou Sequenciais para atender às suas metas comerciais
* **Configurar as recompensas estrategicamente**: entregar pontos nos marcos da tarefa ou após a conclusão completa para manter o engajamento
* **Personalizar a experiência**: use cartões de conteúdo e mensagens multicanais para criar experiências imersivas e de marca
* **Integre-se perfeitamente**: conecte-se com seus provedores de fidelidade existentes e aproveite os dados do Experience Platform
* **Rastrear automaticamente**: monitore o progresso do cliente através de jornadas geradas automaticamente sem desenvolvimento personalizado

![](assets/challenges-gs.png)

Você pode criar três tipos de experiências de desafio:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem. Use esse tipo quando quiser flexibilidade e vários caminhos para conclusão.\
  *Exemplo: &quot;Desafio de Bem-Estar de Verão&quot; - Conclua 3 de 5 tarefas: compre produtos de saúde, compartilhe em redes sociais, indique um amigo, escreva uma avaliação ou participe de um evento virtual*

* **Desafios em série**: os clientes concluem a mesma tarefa várias vezes consecutivamente. Use esse tipo para incentivar um comportamento consistente e repetido ao longo do tempo.\
  *Exemplo: &quot;Semana do Amante do Café&quot; - Compre produtos de café por 7 dias consecutivos para desbloquear uma recompensa para bebida gratuita*

* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida. Use esse tipo para orientar os clientes por meio de uma jornada específica ou processo de integração.\
  *Exemplo: &quot;Nova Jornada de Membro&quot; - Inscreva-se para receber emails → Faça sua primeira compra → Escreva uma análise do produto → Indique um amigo (complete nesta ordem exata)*

## Como funciona {#how-it-works}

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configure os conectores de origem do Experience Platform (como o [Conector capilar](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty)) para assimilar dados do evento de fidelidade que controlam o progresso e as ações do cliente. Esses dados possibilitam o rastreamento de desafios e a conclusão de tarefas.

1. **Criar um desafio** - Defina as propriedades de desafio básicas, incluindo nome, tipo (Padrão, Streak ou Sequencial) e intervalo de datas.

1. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefa (compra, gastos), quantidades, filtros de produto e recompensas.

1. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente. Os cartões de conteúdo mostram informações de desafio, progresso e recompensas.

1. **Configurar mensagens** (opcional) - Configure mensagens multicanais (no aplicativo, email, push) para os principais estágios do ciclo de vida: inicialização, em andamento e conclusão.

1. **Selecionar público-alvo** - Defina quais clientes podem participar do seu desafio selecionando um público-alvo da Adobe Experience Platform.

1. **Publicar jornada** - O Journey Optimizer gera automaticamente uma jornada para o desafio. Navegue até o inventário de Jornadas e publique a jornada gerada automaticamente para disponibilizar o desafio aos clientes.

Para obter instruções detalhadas, consulte [Criar desafios](create-challenges.md).

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

+++Configuração de assimilação de dados

Os desafios de fidelidade dependem dos dados assimilados pelos conectores de origem da Experience Platform para rastrear o progresso do cliente e a conclusão das tarefas.

Antes de iniciar, configure um conector de origem compatível. Atualmente, o Conector capilar está disponível. Conectores adicionais estão planejados para versões futuras. [Saiba mais sobre conectores de origem de fidelidade](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty).

+++

<!--+++Required permissions

To use Loyalty Challenges, you need appropriate permissions in Journey Optimizer. Required permissions include:

TBD

Contact your administrator if you cannot access the feature or need additional permissions.

+++-->

+++Público-alvo

Verifique se o público-alvo necessário existe no Adobe Experience Platform antes de criar seu desafio. Durante a configuração do desafio, você selecionará o público-alvo que define quais clientes estão qualificados para participar. [Saiba como trabalhar com públicos](../audience/about-audiences.md).

+++

## Próximas etapas {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Acessar e gerenciar desafios e tarefas</strong></a>
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
    <em>Saiba como criar e configurar seu primeiro desafio de fidelidade</em>
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
    <em>Saiba como configurar ações que os clientes concluem para desafios</em>
    </p>
  </td>
</tr>
</table>
