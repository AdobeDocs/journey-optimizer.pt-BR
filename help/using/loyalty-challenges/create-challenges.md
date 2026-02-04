---
solution: Journey Optimizer
product: journey optimizer
title: Criar desafios de fidelidade
description: Saiba como criar e configurar desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---


# Criar desafios {#create-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* **Criar desafios** ◀︎ **Você está aqui** - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Como funciona {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Criar um desafio** - Defina as propriedades básicas do desafio, incluindo nome, tipo (Padrão, Streak ou Sequencial), público-alvo e intervalo de datas.

1. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefas (compra, gastos, visitas, etc.), quantidades, filtros de produtos e recompensas.

1. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente.

1. **Configurar mensagens** (Opcional) - Configure mensagens multicanais (no aplicativo, email, push, SMS) para estágios principais: inicialização, em andamento e conclusão.

1. **Revisar e publicar** - Teste seu desafio com perfis de teste e publique-o para disponibilizá-lo para seu público-alvo.

## Criar o desafio {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

Para criar um novo desafio de fidelidade:

1. Navegue até **[!UICONTROL Desafios de fidelidade]** no Journey Optimizer.

1. Selecione a guia **[!UICONTROL Desafios]**.

1. Selecione **[!UICONTROL Criar desafio]**.

1. Configure as propriedades do desafio:

   **Nome do desafio**: insira um nome descritivo para o desafio. Esse nome aparece no inventário de desafios e ajuda a identificar o desafio.

   **Tipo de desafio**: selecione um dos seguintes tipos:
   * **[!UICONTROL Padrão]**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem
   * **[!UICONTROL Série]**: os clientes concluem a mesma tarefa várias vezes consecutivamente
   * **[!UICONTROL Sequencial]**: os clientes concluem as tarefas em uma ordem definida

   **Público-alvo**: selecione o segmento de público que define quem pode participar deste desafio. Você deve criar públicos-alvo no Experience Platform antes de criar desafios. Para obter mais informações, consulte [Introdução aos públicos](../audience/about-audiences.md).

   **Data de início**: definida quando o desafio se torna disponível para os clientes.

   **Data de término**: definida quando o desafio expira e não aceita mais novas conclusões.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Adicionar tarefas {#add-tasks}

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas. Você configura tipos de tarefa (compra, gastos, visitas, envolvimento, eventos personalizados), quantidades, filtros de produto e recompensas.

Dependendo do seu tipo de desafio, os clientes concluem as tarefas de forma diferente:

* **Desafios padrão**: conclua qualquer número especificado de tarefas em qualquer ordem
* **Distribuir desafios**: complete a mesma tarefa várias vezes consecutivamente
* **Desafios sequenciais**: concluir tarefas em uma ordem definida

Para adicionar tarefas ao seu desafio, selecione **[!UICONTROL Adicionar tarefa]** na seção Tarefas e configure as propriedades da tarefa.

Para obter instruções detalhadas sobre como criar e configurar tarefas, consulte [Criar tarefas](create-tasks.md).

### Configurar cartões de conteúdo {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

Os cartões de conteúdo fornecem a representação visual de seu desafio em dispositivos de clientes, exibindo informações de desafio, progresso e recompensas. Saiba mais sobre [cartões de conteúdo](../content-card/create-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

Para configurar cartões de conteúdo para seu desafio:

1. No editor de desafios, navegue até a seção **[!UICONTROL Cartões de conteúdo]**.

1. Selecione **[!UICONTROL Criar cartão de conteúdo]** ou escolha um modelo existente.

1. Projete seu cartão de conteúdo:
   * Adição de imagens, texto e elementos de marca
   * Inclua [tokens de personalização](../personalization/personalization-syntax.md) para exibir informações específicas do cliente
   * Mostrar indicadores de progresso do desafio
   * Exibir recompensas e incentivos

1. Configure quando o cartão de conteúdo é exibido:
   * **Início do desafio**: mostrar quando o desafio se torna disponível
   * **Em andamento**: exibir enquanto os clientes estão participando
   * **Conclusão**: mostrar após os clientes concluírem todas as tarefas

1. Visualize o cartão de conteúdo em diferentes dispositivos para garantir a exibição correta.

1. Salve a configuração do cartão de conteúdo.

Para obter mais informações sobre como projetar e personalizar cartões de conteúdo, consulte [Criar cartões de conteúdo](../content-card/design-content-card.md).

### Configurar mensagens {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

Configurar mensagens multicanais para envolver os clientes em estágios fundamentais do ciclo de vida de desafio.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

Para configurar as mensagens para seu desafio:

1. No editor de desafios, navegue até a seção **[!UICONTROL Mensagens]**.

1. Configure as mensagens para cada estágio do ciclo de vida:

   **Mensagens de inicialização** - Notificar clientes quando o desafio começar:
   * Selecionar canais: [No aplicativo](../in-app/get-started-in-app.md), [email](../email/get-started-email.md), [notificação por push](../push/get-started-push.md) ou [SMS](../sms/get-started-sms.md)
   * Projetar a mensagem com detalhes do desafio e call-to-action
   * Definir tempo de duração: enviar imediatamente quando o desafio entrar em vigor ou agendar um horário específico

   **Mensagens em andamento** - Mantenha os clientes envolvidos durante o desafio:
   * Definir as condições de acionamento (por exemplo, 50% de conclusão, tarefa específica concluída)
   * Crie mensagens de lembrete para incentivar a participação contínua
   * Incluir atualizações de progresso e próximas etapas

   **Mensagens de conclusão** - Comemore o sucesso e entregue recompensas:
   * Parabéns aos clientes por terem concluído o desafio
   * Confirmar alocação de premiação
   * Fornecer instruções para solicitar recompensas
   * Sugerir os próximos desafios ou ações

Para obter mais informações sobre como criar mensagens para canais específicos, consulte:

* [Documentação de mensagens no aplicativo](../in-app/get-started-in-app.md)
* [Documentação de mensagens de email](../email/get-started-email.md)
* [Documentação de notificações por push](../push/get-started-push.md)
* [Documentação de mensagens SMS](../sms/get-started-sms.md)

## Revisar e publicar o desafio {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Antes de publicar seu desafio:

1. **Revise todos os componentes**: verifique as propriedades de desafio, tarefas, recompensas, cartões de conteúdo e configurações de mensagens.

1. **Testar a experiência**: use [perfis de teste](../content-management/test-profiles.md) para validar a exibição do cartão de conteúdo e o comportamento do acionador da tarefa.

1. **Publicar**: selecione **[!UICONTROL Publicar]** para disponibilizar o desafio para seu público-alvo.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Ao publicar um desafio, o Journey Optimizer cria automaticamente uma [jornada](../building-journeys/journey-gs.md) no status Rascunho. A jornada gerada automaticamente aparece no inventário de jornadas com o formato de nome &quot;Desafio: [Nome do desafio]&quot;.

Para disponibilizar o desafio para os clientes:

1. Navegue até o inventário do **[!UICONTROL Jornada]** no Journey Optimizer.

1. Localize a jornada gerada automaticamente (ela terá &quot;Desafio:&quot; como um prefixo em seu nome).

1. [Ativar a jornada](../building-journeys/publish-journey.md).

A jornada começa automaticamente na data de início do desafio especificada.

>[!NOTE]
>
>A jornada gerada automaticamente é exibida no inventário de jornadas e pode ser personalizada, se necessário. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio.

## Próximas etapas {#next-steps}

* [Gerenciar desafios](manage-challenges.md) - Saiba como editar, monitorar e otimizar desafios
* [Entender os Desafios de Fidelidade](get-started.md) - Examinar recursos e funcionalidades

