---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com eventos de jornada
description: Saiba como trabalhar com eventos em suas jornadas
feature: Journeys, Events
topic: Administration
role: Engineer, Admin
level: Intermediate, Experienced
keywords: events, event, jornada, definition, start
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 33%

---

# Trabalhar com eventos de jornada {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de jornada"
>abstract="Um evento está vinculado a uma pessoa. Ele se refere ao comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site, etc.) ou a um acontecimento relacionado a uma pessoa (por exemplo, uma pessoa acumulou 10.000 pontos de fidelidade). O Journey Optimizer acompanha eventos unitários em jornadas para orquestrar as melhores ações futuras."

Use eventos para acionar jornadas individualmente, fornecendo mensagens em tempo real a cada usuário ao entrarem na jornada.

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de streaming para eventos autenticados e não autenticados (como eventos do SDK móvel da Adobe). Você pode usar vários eventos (em etapas diferentes de uma jornada) e várias jornadas podem usar o mesmo evento.

A configuração do evento é **obrigatória** e deve ser executada por um engenheiro de dados.

Você pode configurar dois tipos de eventos: **Eventos unitários** e **Eventos comerciais**.

➡️ [Conheça este recurso no vídeo](#video)

## Eventos unitários {#unitary-events}

**Unitário** eventos estão vinculados a uma pessoa. Relacionam-se com o comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site, etc.) ou com algo que acontece vinculado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos de fidelidade). É o que [!DNL Journey Optimizer] escutará no jornada para orquestrar as melhores ações futuras. Os eventos unitários podem ser baseados em regras ou gerados pelo sistema. Para saber como criar um evento unitário, consulte esta [página](../event/about-creating.md).

As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada do perfil é temporariamente bloqueada por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (seja o mesmo evento ou outro que está acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

## Eventos de negócios {#business-events}

Os eventos de **Negócios** não estão vinculados a um perfil específico. Por exemplo, pode ser um alerta de notícias, uma atualização esportiva, uma alteração ou cancelamento de voo, uma atualização de inventário, eventos meteorológicos etc. Embora esses eventos não sejam específicos de um perfil, eles podem ser de interesse para qualquer número de perfis: indivíduos inscritos em tópicos de notícias específicos, passageiros em um voo, compradores interessados em um produto indisponível, etc. Os eventos comerciais sempre se baseiam em regras. Quando você solta um evento comercial em uma jornada, ele adiciona automaticamente uma atividade **Ler público** logo em seguida.Saiba como criar um evento comercial [nesta página](../event/about-creating-business.md).


## Tipo de ID do evento {#event-id-type}

Para eventos de **negócios**, o tipo de ID de evento sempre é baseado em regras.

Para eventos **unitários**, há dois tipos de ID de evento:

* **Eventos baseados em regras**: esse tipo de evento não gera uma eventID. Usando o editor de expressões simples, basta definir uma regra que será usada pelo sistema para identificar os eventos relevantes que acionarão suas jornadas. Essa regra pode ser baseada em qualquer campo disponível na carga do evento, por exemplo, o local do perfil ou o número de itens adicionados ao carrinho do perfil.

  >[!CAUTION]
  >
  >Uma regra de limite é definida para eventos baseados em regras. Limita o número de eventos qualificados que uma jornada pode processar para 5.000 por segundo em uma determinada organização. Corresponde aos SLAs do Journey Optimizer. Consulte seu licenciamento da Journey Optimizer e a [Descrição do Produto da Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* **Eventos gerados pelo sistema**: esses eventos exigem uma eventID. Esse campo eventID é gerado automaticamente ao criar o evento. O sistema que envia o evento não deve gerar uma ID, mas sim passar a disponível na pré-visualização de carga.

>[!NOTE]
>
>O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço Principal de Coleção de Dados (DCCS) para acionar uma jornada. Não é possível usar eventos assimilados em lote ou eventos de conjuntos de dados internos do Journey Optimizer (feedback de mensagem, rastreamento de email etc.) para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, crie um público-alvo com base nesses eventos e use a atividade **Público-alvo de leitura**. Tecnicamente, a qualificação de público-alvo pode ser usada, mas ela pode causar desafios posteriores com base nas ações usadas. Esses dados não precisam necessariamente acessar o Perfil em tempo real. Se você quiser usar os eventos para segmentação, recomendamos ativar o conjunto de dados para perfil.

## Ciclo de dados {#data-cycle}

Eventos são chamadas POST API. Os eventos são enviados para o Adobe Experience Platform por meio de APIs de assimilação de streaming. O destino do URL de eventos enviados por meio de APIs de mensagens transacionais é chamado de &quot;inlet&quot;. A carga útil de eventos segue a formatação XDM.

A carga contém informações necessárias para que as APIs de Assimilação de streaming funcionem (no cabeçalho) e as informações necessárias para que [!DNL Journey Optimizer] funcionem e as informações que serão usadas em jornadas (no corpo, por exemplo, a quantidade de um carrinho abandonado). Há dois modos para a ingestão de fluxo, autenticados e não autenticados. Para obter detalhes sobre as APIs de ingestão de fluxo, consulte [este link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR){target="_blank"}.

Depois de chegar através das APIs de assimilação de streaming, os eventos fluem para um serviço interno chamado Pipeline e, em seguida, para o Adobe Experience Platform. Se o esquema do evento tiver o sinalizador de Serviço de perfil do cliente em tempo real habilitado e uma ID de conjunto de dados que também tenha o sinalizador de Perfil do cliente em tempo real, ele fluirá para o Serviço de perfil do cliente em tempo real.

Para eventos gerados pelo sistema, o Pipeline filtra os eventos que têm uma carga contendo [!DNL Journey Optimizer] eventIDs (consulte o processo de criação de eventos abaixo) fornecidos por [!DNL Journey Optimizer] e contidos na carga do evento. Para eventos baseados em regras, o sistema identifica o evento usando a condição eventID. Esses eventos são acompanhados pelo [!DNL Journey Optimizer] e a jornada correspondente é acionada.


## Sobre a taxa de transferência de eventos do Jornada {#event-thoughput}

A Adobe Journey Optimizer oferece suporte a um volume máximo de 5.000 eventos de jornada por segundo em nível de organização, em todas as sandboxes. Esta cota se aplica a todos os eventos usados no jornada ativo, que inclui jornadas do **Live**, **Dry run**, **Closed** e **Paused**. Quando essa cota é atingida, novos eventos são enfileirados com uma taxa de processamento de 5.000 por segundo. O tempo máximo que um evento pode passar na fila é de **24 horas**.

Os seguintes tipos de eventos são contados para a cota de 5.000 TPS:

* **Eventos Unitários Externos**: Inclui eventos com base em regras e gerados pelo sistema. Se o mesmo evento bruto se qualificar para várias definições de regra, cada regra qualificada será contada como um evento separado. Mais detalhes abaixo.

* **Eventos de qualificação de público-alvo**: se o mesmo público-alvo de streaming for usado em várias jornadas, cada uso será contado separadamente. Por exemplo, usar o mesmo público-alvo em uma atividade de qualificação de público-alvo em duas jornadas resulta na contagem de dois eventos.

* **Eventos de reação**: eventos acionados por reações de perfil (email aberto, email clicado, etc.) em uma jornada.

* **Eventos comerciais**: eventos não vinculados a um perfil específico, mas a um evento comercial.

* **Eventos do Analytics**: se a [integração com o Adobe Analytics para acionar o jornada](about-analytics.md) tiver sido habilitada, esses eventos também serão incluídos.

* **Retomar Eventos**: evento técnico disparado quando um perfil é retomado de uma jornada pausada. Saiba mais sobre [retomada de jornadas pausadas](../building-journeys/journey-pause.md#how-to-resume-a-paused-journey).

* **Eventos de Conclusão do Nó de Espera**: quando um perfil sai de um nó de espera, um evento técnico é gerado para retomar a jornada.

>[!NOTE]
>
>Exceto para eventos de espera e retomada, todos os outros tipos de evento também contam para a cota quando usados em jornadas com base em públicos-alvo de leitura.

### Sobre eventos brutos qualificados para várias definições de regras

O mesmo evento bruto pode se qualificar para várias definições de regra no jornada. Quando um evento é configurado na seção **Administração**, para o mesmo esquema de evento, várias regras de evento podem ser definidas. Digamos, por exemplo, que temos um evento de compra que tem os campos city e purchaseValue. Vamos considerar os seguintes cenários:

1. Um evento **E1** chamado `newYorkPurchases` é criado com uma definição de regra informando que `city=='New York'`. Esse evento pode ser usado em 10 jornadas, mas ainda será contado apenas como 1 evento, quando ele vier.

1. Agora, digamos que um evento **E2** chamado `highValuePurchases` com `purchaseValue > 1000` como uma definição de regra também seja criado, no mesmo esquema de evento que **E1**. Nesse caso, o mesmo evento de entrada será avaliado em relação a duas regras: `newYorkPurchases` e `highValuePurchases`. Agora, pode acontecer que uma compra em Nova York também seja uma compra de alto valor.

   Nesse caso, o Journey Optimizer criará dois eventos, **E1** e **E2**, a partir do mesmo evento de entrada, o que fará com que esse único evento de entrada conte como dois eventos.

   Observe que esses eventos começam a ser contados quando são usados em uma jornada ativa, incluindo a jornada **Em tempo real**, **Execução seca**, **Fechada** e **Pausada**.

## Atualizar e deletar um evento {#update-event}


Para evitar a quebra de jornadas existentes, ao editar um evento usado em uma jornada do **Rascunho**, do **Ao Vivo** ou do **Fechado**, você só poderá alterar o nome, a descrição ou adicionar campos de carga.

Não é possível excluir nenhum evento usado nas jornadas do **Live**, **Rascunho** ou **Fechadas**. Para excluir um evento usado, você deve interromper as jornadas que o utilizam e/ou removê-lo das jornadas de rascunho onde é usado. Você pode verificar o campo **[!UICONTROL Usado em]**. Ele exibe o número de jornadas que usam esse evento específico. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas correspondentes.

## Vídeos tutoriais {#video}

Saiba como configurar um evento, especificar o ponto final de transmissão e a carga útil de um evento.

>[!VIDEO](https://video.tv.adobe.com/v/3431510?captions=por_br&quality=12)

Entenda os casos de uso aplicáveis a eventos de negócios. Saiba como criar uma jornada usando um evento de negócios e quais práticas recomendadas devem ser aplicadas.

>[!VIDEO](https://video.tv.adobe.com/v/3417595?captions=por_br&quality=12)
