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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 0%

---


# Criar desafios {#create-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar e gerenciar desafios de fidelidade](access-loyalty-challenges.md) - gerenciamento de inventário, desafios e tarefas
* **Criar desafios** ◀︎ **Você está aqui** - Criar e configurar desafios
* [Criar tarefas](create-tasks.md) - Definir tarefas de desafio

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Criar o desafio {#create-the-challenge}

1. Navegue até **[!UICONTROL Desafios de Fidelidade (Beta)]** no Journey Optimizer.

1. Selecione a guia **[!UICONTROL Desafios]** e selecione **[!UICONTROL Criar desafio]**.

   ![](assets/challenge-create.png)

1. Escolha o tipo de desafio:

   * **[!UICONTROL Padrão]**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem\
     *Exemplo: Concluir 3 de 5 tarefas disponíveis*

   * **[!UICONTROL Série]**: os clientes concluem a mesma tarefa várias vezes consecutivamente\
     *Exemplo: faça uma compra em 7 dias consecutivos*

   * **[!UICONTROL Sequencial]**: os clientes concluem as tarefas em uma ordem definida\
     *Exemplo: Compra → Revisão → Compartilhar (deve ser concluído nesta sequência)*

## Configurar a estrutura de desafio {#structure}

Na guia **[!UICONTROL Estrutura]**, defina como seu desafio é organizado: suas propriedades, agendamento, tarefas a serem concluídas e recompensas a serem entregues.

### Definir as propriedades do desafio e usar metadados personalizados {#properties}

1. No painel **[!UICONTROL Propriedades do desafio]**, defina configurações globais para o desafio:

   * **[!UICONTROL Nome]**: insira um nome descritivo para o desafio. Este nome aparece no inventário de desafios.
   * **[!UICONTROL Descrição]**: insira uma descrição que explique a finalidade e as metas do desafio.

   ![](assets/challenge-create-properties.png)

1. Use a seção **[!UICONTROL Metadados personalizados]** para adicionar metadados personalizados usando pares de chave/valor. Esses metadados podem ser usados para rastreamento ou integração com sistemas externos.

### Agendar o desafio {#schedule}

Configure quando seu desafio for executado selecionando o ícone ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Abrir agendamento]**:

![](assets/challenge-create-properties.png)

* **[!UICONTROL Data e hora de início]**: definir quando o desafio ficará disponível para os clientes.
* **[!UICONTROL Data e hora de término]**: definida quando o desafio expira e não aceita mais novas conclusões.
   * **[!UICONTROL Fuso horário]**: o desafio usa o fuso horário local do destinatário por padrão.
* **[!UICONTROL As tarefas devem ser concluídas]**: escolha quando os clientes poderão concluir as tarefas:

   * **[!UICONTROL A qualquer momento durante o desafio]**: os clientes podem concluir tarefas a qualquer momento entre as datas de início e término do desafio.
   * **[!UICONTROL Durante horas específicas do dia]**: Restrinja a conclusão da tarefa a horas diárias específicas definindo a **[!UICONTROL Hora de Início]** e a **[!UICONTROL Hora de Término]**.

A programação de desafio agora está configurada. Em seguida, adicione as tarefas que os clientes precisam concluir.

### Adicionar tarefas {#add-tasks}

As tarefas definem as ações específicas que os clientes devem concluir para ganhar recompensas. Você pode configurar tipos de tarefa (compra, gastos), quantidades, filtros de produto e outros atributos.

Dependendo do seu tipo de desafio, os clientes concluem as tarefas de forma diferente:

* **Desafios padrão**: conclua qualquer número especificado de tarefas em qualquer ordem\
  *Exemplo: Conclua 3 de 5 tarefas - faça uma compra, escreva uma revisão, indique um amigo, compartilhe em redes sociais ou atualize o perfil*

* **Distribuir desafios**: complete a mesma tarefa várias vezes consecutivamente\
  *Exemplo: faça uma compra por 7 dias consecutivos para ganhar prêmios de bônus*

* **Desafios sequenciais**: concluir tarefas em uma ordem definida\
  *Exemplo: primeiro faça uma compra, depois escreva uma revisão e, em seguida, compartilhe em redes sociais - as tarefas devem ser concluídas nesta sequência exata*

Para adicionar tarefas ao seu desafio, siga estas etapas:

1. Na seção **[!UICONTROL Tarefas]**, selecione **[!UICONTROL Adicionar tarefa]**.

   ![](assets/challenge-create-add-task.png)

1. O **[!UICONTROL Inventário de tarefas]** é aberto. Selecione uma ou mais tarefas na lista e selecione **[!UICONTROL Adicionar]**. Para criar uma nova tarefa, selecione **[!UICONTROL Nova]**. [Saiba como criar e configurar tarefas](create-tasks.md).

1. Na seção **[!UICONTROL Requisito de conclusão da tarefa]**, especifique quando o desafio será considerado concluído:

   * **[!UICONTROL O cliente escolhe 1 tarefa para ser concluída]**: os clientes podem selecionar e concluir qualquer tarefa individual para receber recompensas.
   * **[!UICONTROL O cliente conclui um número específico de tarefas]**: os clientes devem concluir um número definido de tarefas.

1. Por padrão, os desafios permitem que os clientes concluam tarefas em várias transações. Para exigir que todas as tarefas sejam concluídas em uma única transação, selecione o ícone ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Configurações]** e alterne na opção abaixo.

   ![](assets/challenge-create-single-transaction.png)

Depois de adicionar tarefas ao seu desafio, configure as recompensas que os clientes ganharão ao concluí-las.

### Configurar recompensas {#rewards}

As recompensas são os pontos de fidelidade ou os benefícios que os clientes recebem por concluir os desafios. Configure quando e como as recompensas serão entregues.

1. Na lista suspensa **[!UICONTROL Entrega de recompensa]**, escolha quando entregar as recompensas:

   * **[!UICONTROL Fornecer recompensas quando o desafio for concluído]**: premiar recompensas quando os clientes concluírem todo o desafio\
     *Exemplo: premiar 100 pontos após concluir todas as 5 tarefas*

   * **[!UICONTROL Fornecer recompensas nos marcos de conclusão da tarefa conforme o progresso do desafio é realizado]**: premiar de forma incremental à medida que os clientes concluem tarefas individuais (disponível somente para desafios que exigem mais de uma tarefa)\
     *Exemplo: Premiar 10 pontos após a tarefa 1, 20 pontos após a tarefa 2 e 50 pontos após a tarefa 3*

1. Selecione seu provedor de premiação. Esta é a sua solução de fidelidade que gerencia pontos e recompensas do cliente.

1. Configure os valores de premiação com base no método de delivery selecionado:

   +++Fornecer recompensas quando o desafio for concluído

   Especifique o valor total de premiação a ser dado quando os clientes concluírem todo o desafio.

   ![](assets/challenge-create-reward-total.png)

   **Exemplo**: os clientes recebem 100 pontos ao concluir o desafio.

   +++

   +++Fornecer recompensas nos marcos de conclusão da tarefa

   Especificar valores de recompensa para marcos de conclusão de tarefas. Essa opção permite criar recompensas progressivas que aumentam a motivação do cliente à medida que avançam pelo desafio.

   Para qualquer tarefa em que você quiser oferecer uma recompensa, alterne para a opção de recompensa e especifique quantos pontos serão concedidos quando os clientes concluírem essa tarefa específica. Você pode optar por recompensar apenas determinadas conclusões de tarefa, por exemplo, se você tiver 10 tarefas, poderá recompensar apenas as tarefas 1, 5 e 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Exemplo**: os clientes recebem 10 pontos ao concluir a primeira tarefa e 50 pontos adicionais após concluir a segunda tarefa, para um total de 60 pontos quando o desafio é concluído.

   >[!TIP]
   >
   >Considere aumentar os valores de recompensa para tarefas posteriores a fim de manter o engajamento do cliente durante todo o desafio.

   +++

Depois de configurar a estrutura de desafios com tarefas e recompensas, crie os cartões de conteúdo para exibir o desafio aos clientes.

## Configurar cartões de conteúdo {#configure-content-cards}

Os cartões de conteúdo representam visualmente seu desafio em dispositivos de clientes, exibindo informações de desafio, progresso e recompensas. [Saiba mais sobre cartões de conteúdo](../content-card/create-content-card.md).

Para configurar cartões de conteúdo para seu desafio:

1. Navegue até a guia **[!UICONTROL Conteúdo]** e digite um **[!UICONTROL Nome]** para o cartão de conteúdo.

1. Selecione a **[!UICONTROL Configuração de canal]**. As configurações de canal contêm todos os parâmetros técnicos para enviar mensagens, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais sobre as configurações de canal](../configuration/channel-surfaces.md).

1. Selecione **[!UICONTROL Editar conteúdo]** para criar seu cartão de conteúdo. [Saiba como criar e personalizar cartões de conteúdo](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Após configurar o cartão de conteúdo, configure as mensagens para envolver os clientes durante todo o ciclo de vida do desafio.

### Configurar mensagens {#configure-messaging}

Configurar mensagens multicanais para envolver os clientes em estágios fundamentais do ciclo de vida de desafio. As mensagens são opcionais, mas são recomendadas para maximizar o engajamento do cliente.

1. Navegue até a guia **[!UICONTROL Mensagens]** e configure as mensagens para cada estágio do ciclo de vida:

   * Mensagem de **Inicialização**: notificar os clientes quando o desafio começar
   * Mensagem **Em andamento**: mantenha os clientes envolvidos com lembretes e atualizações de progresso
   * Mensagem de **Conclusão**: comemorar o sucesso e confirmar a alocação da premiação

1. Para cada estágio, selecione **[!UICONTROL Adicionar [estágio] mensagem]** (onde [estágio] representa Inicialização, Em andamento ou Conclusão) para criar uma mensagem para esse estágio.

1. Escolha o canal desejado: **[!UICONTROL No aplicativo]**, **[!UICONTROL Email]** ou **[!UICONTROL Notificação por push]** e selecione a configuração de canal associada.

1. Selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Editar]** para criar o conteúdo da sua mensagem.

   ![](assets/challenge-create-messaging.png)

Saiba como criar mensagens para canais específicos:

* [Mensagens no aplicativo](../in-app/get-started-in-app.md)
* [Mensagens de email](../email/get-started-email.md)
* [Notificações por push](../push/get-started-push.md)

Após concluir a configuração de mensagens, defina quais clientes estão qualificados para participar do desafio.

## Selecionar o público-alvo do desafio {#audience}

Defina quais clientes podem participar do seu desafio de fidelidade.

1. Navegue até a guia **[!UICONTROL Público-alvo]** e selecione o botão **[!UICONTROL Selecionar público-alvo]**.

   ![](assets/challenge-create-audience.png)

1. Selecione o público-alvo na lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba como trabalhar com públicos](../audience/about-audiences.md).

1. Selecione **[!UICONTROL Adicionar audiência]**.

Seu desafio agora está totalmente configurado com sua estrutura, conteúdo, mensagens e público-alvo. A etapa final é gerar e publicar a jornada.

## Gerar e publicar a jornada {#review-and-publish}

Gere a jornada que orquestrará o delivery de desafio e as interações do cliente. Para fazer isso, selecione **[!UICONTROL Gerar Jornada]**.

![](assets/challenge-create-generate-journey.png)

O Journey Optimizer cria automaticamente uma [jornada](../building-journeys/journey-gs.md) no status Rascunho. A jornada gerada automaticamente aparece no inventário de jornadas com o formato de nome &quot;Desafio: [Nome do desafio]&quot;.

![](assets/challenge-create-journey.png)

Revise a configuração da jornada, se necessário, e publique a jornada para disponibilizar o desafio para os clientes. [Saiba como publicar uma jornada](../building-journeys/publish-journey.md).

A jornada será iniciada automaticamente na data de início do desafio especificada e entregará conteúdo e mensagens de acordo com sua configuração.

>[!NOTE]
>
>A jornada gerada automaticamente pode ser personalizada para adicionar lógica ou mensagens adicionais. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio. Se você editar o desafio mais tarde, qualquer personalização de jornada será perdida quando a jornada for gerada novamente.
