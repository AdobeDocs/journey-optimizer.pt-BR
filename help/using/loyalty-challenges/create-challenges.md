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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
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

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **[Criar o desafio](#create-the-challenge)** - Escolha o tipo de desafio (Padrão, Streak ou Sequencial) que melhor se adapta às suas metas do programa de fidelidade.

1. **[Configurar a estrutura de desafio](#structure)** - Defina as propriedades de desafio, o agendamento, as tarefas que os clientes devem concluir e as recompensas que eles receberão.

1. **[Configurar cartões de conteúdo](#configure-content-cards)** - Crie cartões de conteúdo para representar visualmente seu desafio em dispositivos do cliente, exibindo informações de desafio, progresso e recompensas.

1. **[Configurar mensagens](#configure-messaging)** (Opcional) - Configure mensagens multicanais (no aplicativo, email, push) para estágios principais: inicialização, em andamento e conclusão.

1. **[Selecione o público-alvo do desafio](#audience)** - Defina quais clientes estão qualificados para participar do desafio.

1. **[Gerar e ativar a jornada](#review-and-publish)** - Gerar a jornada associada e ativá-la para disponibilizar o desafio para o público-alvo.

## Criar o desafio {#create-the-challenge}

1. Navegue até **[!UICONTROL Desafios de Fidelidade (Beta)]** no Journey Optimizer.

1. Selecione a guia **[!UICONTROL Desafios]** e selecione **[!UICONTROL Criar desafio]**.

   ![](assets/challenge-create.png)

1. Escolha o tipo de desafio:

   * **[!UICONTROL Padrão]**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem
   * **[!UICONTROL Série]**: os clientes concluem a mesma tarefa várias vezes consecutivamente
   * **[!UICONTROL Sequencial]**: os clientes concluem as tarefas em uma ordem definida

## Configurar a estrutura de desafio {#structure}

A guia Estrutura é onde você define como o desafio é organizado: suas propriedades, agendamento, as tarefas a serem concluídas e as recompensas a serem concedidas.

### Definir as propriedades do desafio e usar metadados personalizados {#properties}

1. No painel de propriedades Desafio, configure as propriedades de desafio:

   ![](assets/challenge-create-properties.png)

   **Nome**: insira um nome descritivo para o desafio. Esse nome aparece no inventário de desafios e ajuda a identificar o desafio.

   **Descrição**: insira uma descrição para o desafio.

1. Use a seção **[!UICONTROL Metadados personalizados]** para adicionar metadados personalizados usando pares de chave/valor. Esses metadados podem ser usados para rastreamento, segmentação ou integração com sistemas externos.

### Agendar o desafio {#schedule}

Agende o desafio selecionando o ícone ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Abrir agendamento]**.

* **Data e hora de início**: definir quando o desafio ficará disponível para os clientes (formato: mm/dd/aaaa, —:— AM/PM).

* **Data e hora de término**: definida quando o desafio expira e não aceita mais novas conclusões (formato: mm/dd/aaaa, —:— AM/PM).

* **Fuso horário**: o desafio usa o fuso horário local do destinatário por padrão.

* **As tarefas devem ser concluídas**: escolha quando os clientes poderão concluir as tarefas:

   * **[!UICONTROL Qualquer momento durante o desafio]**: os clientes podem concluir tarefas a qualquer momento entre as datas de início e término do desafio
   * **[!UICONTROL Durante horas específicas do dia]**: Restrinja a conclusão da tarefa a horas diárias específicas definindo a **[!UICONTROL Hora de Início]** e a **[!UICONTROL Hora de Término]**

A programação de desafio agora está configurada. Agora você pode adicionar as tarefas que os clientes precisam concluir.

### Adicionar tarefas {#add-tasks}

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas. Você configura tipos de tarefa (compra, gastos, visitas, envolvimento, eventos personalizados), quantidades, filtros de produto e recompensas.

Dependendo do seu tipo de desafio, os clientes concluem as tarefas de forma diferente:

* **Desafios padrão**: conclua qualquer número especificado de tarefas em qualquer ordem
* **Distribuir desafios**: complete a mesma tarefa várias vezes consecutivamente
* **Desafios sequenciais**: concluir tarefas em uma ordem definida

Para adicionar tarefas ao seu desafio, siga estas etapas:

1. Na seção **[!UICONTROL Tarefas]**, selecione **[!UICONTROL Adicionar tarefa]**.

   ![](assets/challenge-create-add-task.png)

1. O inventário de Tarefas é aberto. Selecione uma ou mais tarefas na lista e selecione **[!UICONTROL Adicionar]**. Para criar uma nova tarefa, selecione **[!UICONTROL Nova]**.

   Para obter instruções detalhadas sobre como criar e configurar tarefas, consulte [Criar tarefas](create-tasks.md).

1. Na seção **[!UICONTROL Requisito de conclusão da tarefa]**, especifique quando o desafio deve ser considerado concluído:

   * **[!UICONTROL O cliente escolhe 1 tarefa para ser concluída]**: o cliente pode selecionar e concluir qualquer tarefa individual a partir do desafio de ganhar recompensas
   * **[!UICONTROL O cliente conclui um número específico de tarefas]**: o cliente deve concluir um número definido de tarefas. Informe o número necessário de conclusões de tarefas.

1. Por padrão, os desafios permitem que os clientes concluam tarefas em várias transações. Para exigir que todas as tarefas sejam concluídas em uma única transação, selecione o ícone ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Configurações]** e alterne na opção **[!UICONTROL Transação única]**.

   ![](assets/challenge-create-single-transaction.png)

### Configurar recompensas {#rewards}

As recompensas são os pontos de fidelidade ou os benefícios que os clientes recebem por concluir os desafios. Configure como e quando as recompensas são entregues para motivar a participação do cliente.

1. Na lista suspensa **[!UICONTROL Entrega de recompensa]**, escolha quando as recompensas deverão ser entregues:

   * **[!UICONTROL Fornecer recompensas quando o desafio for concluído]**: premiar todas as recompensas quando o cliente concluir todo o desafio
   * **[!UICONTROL Fornecer recompensas nos marcos de conclusão da tarefa conforme o progresso do desafio for realizado]**: premiar de forma incremental à medida que os clientes concluírem tarefas individuais (disponível somente quando o desafio exigir a conclusão de mais de uma tarefa)

1. Selecione o provedor de premiação na lista suspensa. Esta é a sua solução de fidelidade que gerencia pontos e recompensas do cliente.

1. Configure os valores de premiação com base no método de delivery selecionado:

   +++Fornecer recompensas quando o desafio for concluído

   No campo **Número de [pontos de fidelidade] na conclusão do desafio**, especifique o valor total da premiação a ser dado quando o cliente concluir todo o desafio.

   O nome do campo exibe o nome dos pontos de fidelidade conforme definido no provedor selecionado. Por exemplo, se o provedor usar &quot;Pontos Luma&quot;, o campo exibirá &quot;Número de pontos Luma na conclusão do desafio&quot;.

   ![](assets/challenge-create-reward-total.png)

   **Exemplo**: na captura de tela acima, os clientes recebem 100 pontos ao concluir o desafio.

   +++

   +++Fornecer recompensas nos marcos de conclusão da tarefa

   Especificar valores de recompensa para marcos de conclusão de tarefas. Essa opção permite criar recompensas progressivas que aumentam a motivação do cliente à medida que avançam pelo desafio.

   Para qualquer tarefa em que você quiser oferecer uma recompensa, alterne para a opção de recompensa e especifique quantos pontos serão concedidos quando os clientes concluírem essa tarefa específica. Você pode optar por recompensar apenas determinadas conclusões de tarefa, por exemplo, se você tiver 10 tarefas, poderá recompensar apenas as tarefas 1, 5 e 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Exemplo**: na captura de tela acima, os clientes recebem 10 pontos ao concluir a primeira tarefa e 50 pontos adicionais após concluir a segunda tarefa, para um total de 60 pontos quando o desafio é concluído.

   >[!TIP]
   >
   >Considere aumentar os valores de recompensa para tarefas posteriores a fim de manter o engajamento do cliente durante todo o desafio.

   +++

A estrutura do desafio agora está configurada com tarefas e recompensas. Agora você pode projetar os cartões de conteúdo para exibir o desafio para os clientes.

## Configurar cartões de conteúdo {#configure-content-cards}

Os cartões de conteúdo fornecem a representação visual de seu desafio em dispositivos de clientes, exibindo informações de desafio, progresso e recompensas. Saiba mais sobre [cartões de conteúdo](../content-card/create-content-card.md).

Para configurar cartões de conteúdo para seu desafio:

1. No editor de desafios, navegue até a guia **[!UICONTROL Conteúdo]**.

1. Digite um **[!UICONTROL Nome]** para o cartão de conteúdo.

1. Selecione a **[!UICONTROL Configuração de canal]** associada. As configurações de canal definem como e onde seu conteúdo é entregue aos clientes. Para obter mais informações, consulte [Configurações de canal](../configuration/channel-surfaces.md).

1. Selecione **[!UICONTROL Editar conteúdo]** para criar seu cartão de conteúdo.

   ![](assets/challenge-create-content.png)

Para obter mais informações sobre como projetar e personalizar cartões de conteúdo, consulte [Criar cartões de conteúdo](../content-card/design-content-card.md).

O cartão de conteúdo agora está configurado. Agora você pode configurar as mensagens para envolver os clientes durante todo o ciclo de vida do desafio.

### Configurar mensagens {#configure-messaging}

Configurar mensagens multicanais para envolver os clientes em estágios fundamentais do ciclo de vida de desafio.

1. Navegue até a guia **[!UICONTROL Mensagens]**.

1. Configure as mensagens para cada estágio do ciclo de vida:

   ![](assets/challenge-create-messaging.png)

   * **Mensagens de lançamento**: notifique os clientes quando o desafio começar e forneça os detalhes iniciais
   * **Mensagens em andamento**: mantenha os clientes envolvidos durante o desafio com lembretes, atualizações de progresso e incentivo para continuar
   * **Mensagens de conclusão**: comemore o sucesso, confirme a alocação de premiação e sugira os próximos desafios ou ações

1. Para cada estágio, selecione **[!UICONTROL Adicionar *estágio* mensagem]** para criar uma mensagem para esse estágio.

1. Escolha o canal desejado: **[!UICONTROL No aplicativo]**, **[!UICONTROL Email]** ou **[!UICONTROL Notificação por push]** e selecione a configuração de canal associada.

1. Selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Editar]** para criar o conteúdo da sua mensagem.

   Para obter mais informações sobre como criar mensagens para canais específicos, consulte:

   * [Documentação de mensagens no aplicativo](../in-app/get-started-in-app.md)
   * [Documentação de mensagens de email](../email/get-started-email.md)
   * [Documentação de notificações por push](../push/get-started-push.md)

1. Repita essas etapas para cada estágio e canal, conforme necessário.

A configuração das mensagens está concluída. Agora você pode definir quais clientes estão qualificados para participar do desafio.

## Selecionar o público-alvo do desafio {#audience}

Defina quais clientes estão qualificados para participar do seu desafio de fidelidade.

1. Navegue até a guia **[!UICONTROL Público]** e clique no botão **[!UICONTROL Selecionar público-alvo]**.

   ![](assets/challenge-create-audience.png)

1. Todos os públicos-alvo do Adobe Experience Platform disponíveis são exibidos. Selecione o público-alvo desejado na lista.

1. Selecione **[!UICONTROL Adicionar público-alvo]** para confirmar sua seleção.

Sua configuração de desafio está concluída. Agora você pode gerar a jornada que orquestrará a entrega de desafio.

## Gerar e ativar a jornada {#review-and-publish}

Quando a configuração do desafio for concluída, gere a jornada associada que orquestrará a entrega do desafio e as interações com o cliente. Para fazer isso, selecione **[!UICONTROL Gerar Jornada]**.

![](assets/challenge-create-generate-journey.png)

O Journey Optimizer cria automaticamente uma [jornada](../building-journeys/journey-gs.md) no status Rascunho. A jornada gerada automaticamente aparece no inventário de jornadas com o formato de nome &quot;Desafio: [Nome do desafio]&quot;.

Revise a configuração da jornada, se necessário, e [ative a jornada](../building-journeys/publish-journey.md) para disponibilizar o desafio para os clientes.

A jornada será iniciada automaticamente na data de início do desafio especificada e entregará conteúdo e mensagens de acordo com sua configuração.

>[!NOTE]
>
>A jornada gerada automaticamente pode ser personalizada, se necessário, para adicionar lógica ou mensagens adicionais. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio. Se você editar o desafio mais tarde, qualquer personalização de jornada será perdida quando a jornada for gerada novamente.

## Próximas etapas {#next-steps}

* [Gerenciar desafios](manage-challenges.md) - Saiba como editar, monitorar e otimizar desafios
* [Entender os Desafios de Fidelidade](get-started.md) - Examinar recursos e funcionalidades
