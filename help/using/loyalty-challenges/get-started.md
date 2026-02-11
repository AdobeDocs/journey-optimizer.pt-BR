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
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: c5d7cbde6e0a9b4b835abac19d33b973f9f364e4
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 2%

---

# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* **Introdução aos desafios de fidelidade** ◀︎ **Você está aqui**
* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges/){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

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

1. **Criar um desafio** - Defina as propriedades de desafio básicas, incluindo nome, tipo (Padrão, Streak ou Sequencial) e intervalo de datas.

1. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefa (compra, gastos), quantidades, filtros de produto e recompensas.

1. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente. Os cartões de conteúdo mostram informações de desafio, progresso e recompensas.

1. **Configurar mensagens** (opcional) - Configure mensagens multicanais (no aplicativo, email, push) para os principais estágios do ciclo de vida: inicialização, em andamento e conclusão.

1. **Selecionar público-alvo** - Defina quais clientes podem participar do seu desafio selecionando um público-alvo da Adobe Experience Platform.

1. **Iniciar o desafio** - Publique o desafio e gere uma jornada. O Journey Optimizer cria automaticamente a jornada para o seu desafio. Publique a jornada gerada automaticamente para disponibilizar o desafio aos clientes.

Para obter instruções detalhadas, consulte [Criar desafios](create-challenges.md).

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

+++Permissões necessárias

Para usar os Desafios de fidelidade, você precisa das permissões apropriadas no Journey Optimizer e no Adobe Experience Platform.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Entre em contato com o administrador se não conseguir acessar o recurso ou precisar de permissões adicionais.

+++

+++Público-alvo

Verifique se o público-alvo necessário existe no Adobe Experience Platform antes de criar seu desafio. Durante a configuração do desafio, você selecionará o público-alvo que define quais clientes estão qualificados para participar. [Saiba como trabalhar com públicos](../audience/about-audiences.md).

+++

## Vamos nos aprofundar um pouco mais {#lets-dive-deeper}

Agora que você sabe o que são desafios de fidelidade e como eles funcionam, é hora de mergulhar nos detalhes. Explore os tópicos a seguir para acessar a interface, criar o primeiro desafio e definir as tarefas que os clientes concluirão.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Acesso" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Acessar e gerenciar desafios e tarefas</strong></a>
    </div>
    <p>
    <em>Saiba como acessar o inventário e gerenciar desafios e tarefas</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Criar" src="assets/do-not-localize/icon-challenge.png" width="200"/>
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
      <img alt="Tarefas" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>Criar tarefas</strong></a>
    </div>
    <p>
    <em>Saiba como definir tarefas que os clientes concluem para desafios</em>
    </p>
  </td>
</tr>
</table>

## Referência da API {#api-reference}

Para gerenciar desafios de fidelidade de forma programática, use a [API de Desafios de Fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges/){target="_blank"}. A API permite criar, atualizar e gerenciar desafios e tarefas por meio de endpoints REST.
