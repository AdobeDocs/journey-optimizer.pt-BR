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
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: c950bee8-4ea9-4b64-810d-91371e8b3e4c
source-git-commit: 7d107482d9041a115b7526a937cbb6f48793bffc
workflow-type: tm+mt
source-wordcount: '1973'
ht-degree: 16%

---

# Criar desafios {#create-challenges}

>[!BEGINSHADEBOX]

**Sumário**

[Introdução aos desafios de fidelidade](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Criar e gerenciar desafios**

* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* **Criar desafios** ◀︎ **Você está aqui**
* [Criar tarefas](create-tasks.md)
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configurar desafios de fidelidade](loyalty-admin.md)
* [Dados e conjuntos de dados de fidelidade](loyalty-data-and-datasets.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

Esta página aborda o processo completo de criação de um desafio de fidelidade, desde selecionar o tipo de desafio e configurar suas propriedades até gerar e publicar a jornada que fornecerá o desafio aos seus clientes.

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

   * **[!UICONTROL Traga seus próprios dados]**: selecione **[!UICONTROL Trazer seus próprios dados]** quando quiser que a estrutura de desafios, como tarefas e recompensas, seja montada a partir da integração de dados de Desafios de Fidelidade. Quando esse tipo é selecionado, você não precisa configurar a estrutura de desafio. Você só configura **[!UICONTROL Conteúdo]**, **[!UICONTROL Mensagens]** e **[!UICONTROL Público-alvo]** da mesma forma que outros desafios.

     >[!AVAILABILITY]
     >
     >O tipo de desafio **[!UICONTROL Traga seus próprios dados]** está disponível no momento para um conjunto restrito de organizações e será disponibilizado de forma mais ampla em uma versão futura.

   Após selecionar um tipo de desafio, a interface de criação de desafio é aberta com várias guias de configuração. Para todos os tipos, exceto **[!UICONTROL Traga seus próprios dados]**, comece configurando a estrutura de desafio.

## Configurar a estrutura de desafio {#structure}

Na guia **[!UICONTROL Estrutura]**, defina como seu desafio é organizado: suas propriedades, agendamento, tarefas a serem concluídas e recompensas a serem entregues.

### Definir as propriedades do desafio e usar metadados personalizados {#properties}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_properties"
>title="Propriedades do desafio"
>abstract="No painel de propriedades Desafio, defina o nome do desafio e a descrição. Depois, adicione metadados de chave/valor personalizados para rastreamento ou integrações externas."

1. No painel **[!UICONTROL Propriedades do desafio]**, defina configurações globais para o desafio:

   * **[!UICONTROL Nome]**: insira um nome descritivo para o desafio. Este nome aparece no inventário de desafios.
   * **[!UICONTROL Descrição]**: insira uma descrição que explique a finalidade e as metas do desafio.

1. Use a seção **[!UICONTROL Metadados personalizados]** para adicionar metadados personalizados usando pares de chave/valor. Esses metadados podem ser usados para rastreamento ou integração com sistemas externos.

   ![](assets/challenge-create-properties.png)

### Agendar o desafio {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_schedule"
>title="Cronograma de desafio"
>abstract="Use o cronograma para definir quando o desafio estará ativo: defina a data e a hora de início para quando ele se torna disponível para os clientes e a data e a hora de término para quando ele para de aceitar conclusões. Selecione um fuso horário e escolha quando os clientes poderão concluir tarefas na **[!UICONTROL seção Janela de conclusão de tarefas]**."

Configure quando seu desafio é executado:

1. Selecione o ícone **[!UICONTROL Abrir agendamento]**:

   ![](assets/challenge-create-schedule.png)

1. Configure as seguintes opções de agendamento:

   * **[!UICONTROL Data e hora de início]**: definir quando o desafio ficará disponível para os clientes.
   * **[!UICONTROL Data e hora de término]**: definida quando o desafio expira e não aceita mais novas conclusões.
   * **[!UICONTROL Fuso horário]**: o desafio usa o fuso horário local do destinatário por padrão.
   * **[!UICONTROL As tarefas devem ser concluídas]**: escolha quando os clientes poderão concluir as tarefas:

      * **[!UICONTROL A qualquer momento durante o desafio]**: os clientes podem concluir tarefas a qualquer momento entre as datas de início e término do desafio.
      * **[!UICONTROL Durante horas específicas do dia]**: Restrinja a conclusão da tarefa a horas diárias específicas definindo a **[!UICONTROL Hora de Início]** e a **[!UICONTROL Hora de Término]**.

A programação de desafio agora está configurada. Em seguida, adicione as tarefas que os clientes precisam concluir.

### Adicionar tarefas {#add-tasks}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_tasks"
>title="Tarefas"
>abstract="Selecione as tarefas que serão executadas para concluir o desafio. Em seguida, configure como o desafio é concluído. As opções disponíveis dependem do tipo de desafio (Padrão, Sequência ou Sequencial)."

As tarefas definem as ações específicas que os clientes devem concluir para ganhar recompensas. Você pode configurar tipos de tarefa (compra, gasto ou evento personalizado), quantidades, filtros de produto e outros atributos.

Para adicionar tarefas ao seu desafio, siga estas etapas:

1. Na seção **[!UICONTROL Tarefas]**, selecione **[!UICONTROL Adicionar tarefa]**.

   ![](assets/challenge-create-add-task.png)

1. O **[!UICONTROL Inventário de tarefas]** é aberto. Selecione uma ou mais tarefas na lista e selecione **[!UICONTROL Adicionar]**. Para criar uma nova tarefa, selecione **[!UICONTROL Nova]**. [Saiba como criar e configurar tarefas](create-tasks.md).

1. Especificar quando o desafio é considerado concluído. As configurações disponíveis dependem do tipo de desafio:

   +++Desafios padrão

   No menu suspenso **[!UICONTROL Requisito de conclusão da tarefa]**, escolha entre:

   * **[!UICONTROL O cliente escolhe 1 tarefa para ser concluída]** - *Os clientes podem selecionar e concluir qualquer tarefa individual para receber recompensas*
   * **[!UICONTROL O cliente conclui um número específico de tarefas]** - *Os clientes devem concluir um número definido de tarefas. Especifique o número necessário de tarefas a serem concluídas.*

   +++

   +++Desafios do Streak

   No menu suspenso **[!UICONTROL Tipo de Streak]**, escolha entre:

   * **Consecutivo**: os clientes devem concluir a tarefa em dias consecutivos sem interrupções. *Exemplo: Compra na segunda, terça, quarta-feira — falta um dia quebra a sequência.*

   * **Não consecutivo**: os clientes podem concluir a tarefa com intervalos entre as conclusões. *Exemplo: Conclua 7 compras em 30 dias, com interrupções permitidas.*

   No campo **[!UICONTROL Comprimento da sequência]**, especifique quantas vezes a tarefa deve ser concluída. *Exemplo: Defina como 7 para uma &quot;sequência de compras de 7 dias.&quot;*

   +++

   +++Desafios sequenciais

   No menu suspenso **[!UICONTROL Requisito de conclusão da tarefa]**, escolha entre:

   * **[!UICONTROL O cliente escolhe 1 tarefa para ser concluída]** - *Os clientes podem selecionar e concluir qualquer tarefa individual para receber recompensas*
   * **[!UICONTROL O cliente conclui um número específico de tarefas]** - *Os clientes devem concluir um número definido de tarefas na ordem exata que você definir. Faltando ou ignorando uma tarefa interrompe a sequência. Especifique o número necessário de tarefas para concluir*

   +++

1. Por padrão, os desafios padrão e sequenciais permitem que os clientes concluam tarefas em várias transações. Para exigir que todas as tarefas sejam concluídas em uma única transação, selecione o ícone **[!UICONTROL Configurações]** e alterne na opção abaixo.

   ![](assets/challenge-create-single-transaction.png)

Depois de adicionar tarefas ao seu desafio, configure as recompensas que os clientes ganharão ao concluí-las.

### Configurar recompensas {#rewards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_rewards"
>title="Recompensas"
>abstract="Escolha quando os clientes ganham pontos: quando eles concluem todo o desafio ou nos marcos da tarefa à medida que avançam. Selecione o provedor de premiação (a solução de fidelidade que gerencia pontos e recompensas) e defina valores: um único total para conclusão total ou valores por tarefa para determinar marcos, ativando as recompensas somente para as tarefas que deseja."

As recompensas são os pontos de fidelidade ou os benefícios que os clientes recebem por concluir os desafios.

Para configurar quando e como as recompensas serão entregues:

1. No menu suspenso **[!UICONTROL Entrega de recompensa]**, escolha quando entregar as recompensas:

   * **[!UICONTROL Fornecer recompensas quando o desafio for concluído]**: premiar recompensas quando os clientes concluírem todo o desafio\
     *Exemplo: premiar 100 pontos após concluir todas as 5 tarefas*

   * **[!UICONTROL Fornecer recompensas nos marcos de conclusão da tarefa conforme o progresso do desafio é realizado]**: premiar de forma incremental à medida que os clientes concluem tarefas individuais (disponível somente para desafios que exigem mais de uma tarefa)\
     *Exemplo: Premiar 10 pontos após a tarefa 1, 20 pontos após a tarefa 2 e 50 pontos após a tarefa 3*

1. Selecione seu provedor de premiação. Esta é a sua solução de fidelidade que gerencia pontos e recompensas do cliente. Os provedores de recompensa são criados no menu **[!UICONTROL Admin de fidelidade]** antes de você criar desafios. [Saiba como configurar provedores de premiação](loyalty-admin.md#reward-providers)

   ![](assets/challenge-create-reward-type.png)

1. Configure os valores de premiação com base no método de delivery selecionado:

   +++Fornecer recompensas quando o desafio for concluído

   Especifique o valor total de premiação a ser dado quando os clientes concluírem todo o desafio.

   *No exemplo abaixo, os clientes recebem 100 pontos ao concluírem o desafio.*

   ![](assets/challenge-create-reward-total.png)

   +++

   +++Fornecer recompensas nos marcos de conclusão da tarefa

   Especificar valores de recompensa para marcos de conclusão de tarefas. Essa opção permite criar recompensas progressivas que aumentam a motivação do cliente à medida que avançam pelo desafio.

   Para qualquer tarefa em que você quiser oferecer uma recompensa, alterne para a opção de recompensa e especifique quantos pontos serão concedidos quando os clientes concluírem essa tarefa específica. Você pode optar por recompensar apenas determinadas conclusões de tarefa, por exemplo, se você tiver 10 tarefas, poderá recompensar apenas as tarefas 1, 5 e 10.

   *No exemplo abaixo, os clientes recebem 10 pontos ao concluírem a primeira tarefa e 50 pontos adicionais após concluírem a segunda tarefa.*

   ![](assets/challenge-create-reward-milestones.png)

   +++

Depois de configurar a estrutura de desafios com tarefas e recompensas, crie os cartões de conteúdo para exibir o desafio aos clientes.

## Configurar cartões de conteúdo {#configure-content-cards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_content"
>title="Conteúdo"
>abstract="Configure o cartão de conteúdo que representa o desafio em dispositivos de clientes e mostra informações do desafio, progresso e recompensas. Insira um nome para o cartão, selecione uma configuração de canal para que a entrega use as configurações técnicas certas (por exemplo, cabeçalhos, subdomínio ou aplicativos móveis) e selecione Editar conteúdo para projetar e personalizar a experiência do cartão."

Os cartões de conteúdo representam visualmente seu desafio em dispositivos de clientes, exibindo informações de desafio, progresso e recompensas. [Saiba mais sobre cartões de conteúdo](../content-card/create-content-card.md).

Para configurar cartões de conteúdo para seu desafio:

1. Navegue até a guia **[!UICONTROL Conteúdo]** e digite um **[!UICONTROL Nome]** para o cartão de conteúdo.

1. Selecione a **[!UICONTROL Configuração de canal]**. As configurações de canal contêm todos os parâmetros técnicos para envio de mensagens, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais sobre as configurações de canal](../configuration/channel-surfaces.md).

1. Selecione **[!UICONTROL Editar conteúdo]** para criar seu cartão de conteúdo. [Saiba como criar e personalizar cartões de conteúdo](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Após configurar o cartão de conteúdo, configure as mensagens para envolver os clientes durante todo o ciclo de vida do desafio.

### Configurar mensagens {#configure-messaging}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_messaging"
>title="Mensagens"
>abstract="As mensagens ajudam a engajar durante todo o ciclo de vida do desafio. Na guia Mensagens, adicione mensagens para cada estágio: Lançamento (quando o desafio começa), Em andamento (lembretes e atualizações de progresso) e Conclusão (comemore o sucesso e confirme as recompensas). Para cada estágio, adicione uma mensagem, escolha o canal, selecione uma configuração de canal e selecione Editar para criar o conteúdo da mensagem."

Configurar mensagens multicanais para envolver os clientes em estágios fundamentais do ciclo de vida de desafio. As mensagens são opcionais, mas são recomendadas para maximizar o engajamento do cliente.

1. Navegue até a guia **[!UICONTROL Mensagens]** e configure as mensagens para cada estágio do ciclo de vida:

   * Mensagem de **Inicialização**: notificar os clientes quando o desafio começar
   * Mensagem **Em andamento**: mantenha os clientes envolvidos com lembretes e atualizações de progresso
   * Mensagem de **Conclusão**: comemorar o sucesso e confirmar a alocação da premiação

1. Para cada estágio, clique no botão adicionar mensagem para criar uma mensagem para esse estágio.

1. Escolha o canal desejado: **[!UICONTROL No aplicativo]**, **[!UICONTROL Email]** ou **[!UICONTROL Notificação por push]** e selecione a configuração de canal associada.

1. Selecione o ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e escolha **[!UICONTROL Editar]** para criar o conteúdo da sua mensagem.

   ![](assets/challenge-create-messaging.png)

Saiba como criar mensagens para canais específicos nestas seções: [Mensagens no aplicativo](../in-app/get-started-in-app.md) - [Mensagens de email](../email/get-started-email.md) - [Notificações por push](../push/get-started-push.md)

Após concluir a configuração de mensagens, defina quais clientes estão qualificados para participar do desafio.

## Selecione o público-alvo do desafio {#audience}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_audience"
>title="Público-alvo"
>abstract="Na guia Público-alvo, escolha quem pode participar do desafio nos públicos-alvo disponíveis na Adobe Experience Platform."

Defina quais clientes podem participar do seu desafio de fidelidade.

1. Navegue até a guia **[!UICONTROL Público]** e clique no botão **[!UICONTROL Selecionar público-alvo]**.

   ![](assets/challenge-create-audience.png)

1. Na caixa de diálogo de seleção de público, selecione seu público-alvo na lista de públicos-alvo disponíveis do Adobe Experience Platform e selecione **[!UICONTROL Adicionar público-alvo]**. [Saiba como trabalhar com públicos](../audience/about-audiences.md).

Seu desafio agora está totalmente configurado com sua estrutura, conteúdo, mensagens e público-alvo. Para iniciá-lo, você deve publicar o desafio e sua jornada associada.

## Lançando o desafio {#launch}

Para iniciar um desafio, são necessárias **três etapas**: (1) publicar o desafio, (2) gerar a jornada, (3) publicar a jornada. Todos os três devem ser preenchidos para que o desafio seja entregue aos clientes.

1. Revise sua configuração de desafio para garantir que todos os campos obrigatórios sejam preenchidos.

1. Clique no ícone ![](assets/do-not-localize/Smock_More_18_N.svg) e selecione **[!UICONTROL Publicar]**.

   ![](assets/challenge-create-publish.png)

1. Selecione **[!UICONTROL Gerar Jornada]** para criar a jornada que orquestrará a entrega de desafio.

   ![](assets/challenge-create-generate-journey.png)

1. O Journey Optimizer cria automaticamente uma jornada no status &quot;Rascunho&quot;. A jornada aparece no inventário de jornadas com o formato de nome *&quot;Jornada: [Nome do desafio]&quot;*. [Saiba mais sobre o inventário de jornadas](../building-journeys/journey-ui.md).

   ![](assets/challenge-create-journey.png)

1. Abra a jornada e publique-a. A jornada será iniciada automaticamente na data de início do desafio especificada e entregará conteúdo e mensagens de acordo com sua configuração. [Saiba como publicar uma jornada](../building-journeys/publish-journey.md).

1. Quando seu desafio estiver ativo, monitore os KPIs do programa, os resultados do desafio e as métricas no nível da tarefa nos [relatórios de desafio de fidelidade](loyalty-reporting.md). Você também pode monitorar a entrega de mensagens no [relatório de jornadas](../reports/journey-global-report-cja.md).

>[!NOTE]
>
>A jornada gerada automaticamente pode ser personalizada para adicionar lógica ou mensagens adicionais. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio. Se você editar o desafio mais tarde, qualquer personalização de jornada será perdida quando a jornada for gerada novamente.
