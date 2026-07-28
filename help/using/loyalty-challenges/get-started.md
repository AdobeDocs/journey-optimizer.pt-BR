---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos desafios de fidelidade
description: Saiba como criar e gerenciar desafios de fidelidade no Adobe Journey Optimizer para criar programas de fidelidade envolventes e gratificantes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: b45a83f480603ecd38cfcbdf31ccc639f617f592
workflow-type: tm+mt
source-wordcount: 917
ht-degree: 13%

---

# Introdução aos desafios de fidelidade {#get-started-loyalty-challenges}

## Visão geral {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Desafios de fidelidade"
>abstract="Os Desafios de Fidelidade permitem criar programas de fidelidade envolventes e gamificados que impulsionam o comportamento do cliente e aprofundam os relacionamentos com a marca. Crie desafios que recompensem os clientes por ações específicas, desde fazer compras e escrever avaliações até se envolver com redes sociais e indicar a amigos."

>[!AVAILABILITY]
>
>* O Journey Optimizer Loyalty não está disponível atualmente para clientes do Healthcare Shield e do Privacy and Security Shield. A disponibilidade para clientes do Healthcare Shield e do Privacy and Security Shield será atualizada quando os recursos estiverem prontos.

Os Desafios de Fidelidade permitem criar programas de fidelidade envolventes e gamificados que impulsionam o comportamento do cliente e aprofundam os relacionamentos com a marca. Crie desafios que recompensem os clientes por ações específicas, desde fazer compras e escrever avaliações até se envolver com redes sociais e indicar a amigos.

Com os desafios de fidelidade, você pode:

* **Crie tipos de desafios flexíveis**: Crie desafios Padrão, Streak ou Sequenciais para atender às suas metas comerciais
* **Configurar as recompensas estrategicamente**: entregar pontos nos marcos da tarefa ou após a conclusão completa para manter o engajamento
* **Personalizar a experiência**: use cartões de conteúdo e mensagens multicanais para criar experiências imersivas e de marca
* **Integre-se perfeitamente**: conecte-se com seus provedores de fidelidade existentes e aproveite os dados do Experience Platform
* **Rastrear automaticamente**: monitore o progresso do cliente através de jornadas geradas automaticamente sem desenvolvimento personalizado
* **Meça o desempenho**: use painéis de relatório internos para rastrear KPIs de programa, resultados de desafio e métricas no nível da tarefa

![](assets/challenges-gs.png)

Você pode criar estes tipos de experiências de desafio:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem. Use esse tipo quando quiser flexibilidade e vários caminhos para conclusão.\
  *Exemplo: &quot;Desafio de Bem-Estar de Verão&quot; - Conclua 3 de 5 tarefas: compre produtos de saúde, compartilhe em redes sociais, indique um amigo, escreva uma avaliação ou participe de um evento virtual*

* **Desafios em série**: os clientes concluem a mesma tarefa várias vezes consecutivamente. Use esse tipo para incentivar um comportamento consistente e repetido ao longo do tempo.\
  *Exemplo: &quot;Semana do Amante do Café&quot; - Compre produtos de café por 7 dias consecutivos para desbloquear uma recompensa para bebida gratuita*

* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida. Use esse tipo para orientar os clientes por meio de uma jornada específica ou processo de integração.\
  *Exemplo: &quot;Nova Jornada de Membro&quot; - Inscreva-se para receber emails → Faça sua primeira compra → Escreva uma análise do produto → Indique um amigo (complete nesta ordem exata)*

* **Traga seus próprios desafios de dados** (disponibilidade restrita): a estrutura de desafios (tarefas e recompensas) é montada a partir da integração de dados dos Desafios de Fidelidade. Defina Configurações, Conteúdo e Mensagens da mesma maneira que faria para qualquer outro tipo de desafio.

## Como funciona {#how-it-works}

O uso dos desafios de fidelidade envolve três fases abrangentes — configuração, execução e medição — normalmente compartilhadas entre funções de administrador e de profissional.

**1. Configurar o seu programa** *(admin)*

Antes que os desafios possam ser criados, um administrador configura os fundamentos do programa: provedores de recompensa, definições de eventos que mapeiam as ações do cliente para conclusões de tarefas, inventário de produtos e listas de exclusão. [Saiba como configurar desafios de fidelidade](loyalty-admin.md).

**2. Desafios de criação e inicialização** *(profissional)*

Os profissionais de marketing criam desafios selecionando um tipo (Padrão, Streak, Sequencial ou Trazer seus próprios dados), definindo configurações (público-alvo, programação, regras) e definindo tarefas e recompensas. Como opção, eles podem exibir o desafio em interfaces voltadas para membros usando um **cartão de conteúdo** ou uma **experiência baseada em código** e configurar notificações de canal para momentos-chave do ciclo de vida do desafio. Depois de configurados, eles publicam o desafio, geram a jornada criada automaticamente e a publicam para ativá-lo. [Saiba como criar desafios](create-challenges.md).

**3. Monitorar desempenho** *(profissional/analista)*

Quando um desafio estiver ativo, os painéis de relatórios integrados fornecerão métricas de nível de desafio: desempenho do funnel de público-alvo, taxas de conclusão de tarefas, emissão de recompensa e impacto na receita. O mecanismo de insights alimentado por IA também exibe recomendações contextuais para ajudar a otimizar o desempenho do programa. [Saiba mais sobre relatórios de fidelidade](loyalty-reporting.md).

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

+++Permissões necessárias

Para usar os Desafios de Fidelidade, você deve ser atribuído a uma função de Fidelidade. As funções padrão estão disponíveis para administradores, profissionais e analistas na sandbox Produção. Para sandboxes de não produção, o administrador deve criar uma função personalizada com as permissões de Fidelidade necessárias.

Entre em contato com o administrador se não conseguir acessar o recurso ou precisar de permissões adicionais. [Saiba como configurar permissões de Desafios de Fidelidade](loyalty-permissions.md).

+++

+++Configurar o programa de fidelidade (administradores)

Os administradores configuram provedores de premiação, definições de eventos, inventário de produtos, exclusões e configurações globais no menu **[!UICONTROL Admin. de fidelidade]**. Os profissionais de marketing que apenas criam desafios não precisam acessar esse menu. [Saiba como configurar desafios de fidelidade](loyalty-admin.md)

Entre em contato com o administrador se o menu de **[!UICONTROL Administrador de fidelidade]** não estiver visível na navegação à esquerda.

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
  <td>
    <a href="loyalty-reporting.md">
      <img alt="Relatórios" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>Monitorar desempenho</strong></a>
    </div>
    <p>
    <em>Rastreie KPIs de programa, resultados de desafio e métricas de tarefa com painéis integrados</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
  -->
    <a href="loyalty-admin.md"><strong>Configurar desafios de fidelidade</strong></a>
    </div>
    <p>
    <em>Configurar provedores de premiação, definições de eventos e configurações da organização</em>
    </p>
  </td>
</tr>
</table>

## Referência da API {#api-reference}

Para gerenciar desafios de fidelidade de forma programática, use a [API de Desafios de Fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. A API permite criar, atualizar e gerenciar desafios e tarefas por meio de endpoints REST.
