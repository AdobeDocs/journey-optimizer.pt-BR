---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com eventos de jornada
description: Saiba como trabalhar com eventos em suas jornadas
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: events, event, jornada, definition, start
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
TQID: https://experienceleague.adobe.com/xvLSBd-rwKKNqwQNDa4D8GfFzc-ND1FkC3EdstufkIY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e588992f914e67f482d6736d55c5a705da8d465f
workflow-type: tm+mt
source-wordcount: 2181
ht-degree: 27%

---

# Trabalhar com eventos de jornada {#about-events}

>[!BEGINSHADEBOX]

**Nesta página:** Eventos são os acionadores em tempo real que iniciam suas jornadas. Compare os tipos de qualificação unitário, comercial e de público-alvo para escolher o correto para cada caso de uso.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de jornada"
>abstract="O Journey Optimizer oferece suporte a três tipos de eventos nas jornadas: eventos unitários, vinculados ao comportamento de uma pessoa específica (como uma compra ou um marco de fidelidade); eventos comerciais, que são acionados por uma ocorrência global (como um cancelamento de voo ou uma atualização de estoque); e eventos de qualificação de público-alvo, que são acionados quando um perfil entra ou sai de um público-alvo. Use eventos para acionar jornadas e orquestrar as ações certas para os perfis."

Use eventos para acionar jornadas individualmente, fornecendo mensagens em tempo real a cada usuário ao entrarem na jornada.

>[!IMPORTANT]
>
>Para obter os requisitos e as limitações do evento (transmissão, Serviço de consulta, assimilação em lote), consulte [medidas de proteção de Jornada - Eventos](../start/guardrails.md#events-g).

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de transmissão para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). Você pode usar vários eventos (em diferentes etapas de uma jornada), e várias jornadas podem usar o mesmo evento.

A configuração do evento é **obrigatória** e deve ser executada por um engenheiro de dados.

Você pode configurar três tipos de eventos: **Eventos unitários**, **Eventos comerciais** e **Eventos de qualificação de público-alvo**.

➡️ [Conheça este recurso no vídeo](#video)

## Eventos unitários {#unitary-events}

**Unitário** eventos estão vinculados a uma pessoa. Elas estão relacionadas ao comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site etc.) ou um acontecimento ligado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos no programa de fidelidade). É o que o [!DNL Journey Optimizer] considera nas jornadas para orquestrar as melhores ações futuras. Os eventos unitários podem ser baseados em regras ou gerados pelo sistema. Para saber como criar um evento unitário, consulte esta [página](../event/about-creating.md).

As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada do perfil é temporariamente bloqueada por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (seja o mesmo evento ou outro que está acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

## Eventos de negócios {#business-events}

Os eventos de **Negócios** não estão vinculados a um perfil específico. Por exemplo, pode ser um alerta de notícias, uma atualização esportiva, uma alteração ou cancelamento de voo, uma atualização de inventário, eventos meteorológicos etc. Embora esses eventos não sejam específicos de um perfil, eles podem ser de interesse para qualquer número de perfis: indivíduos inscritos em tópicos de notícias específicos, passageiros em um voo, compradores interessados em um produto indisponível, etc. Os eventos comerciais sempre se baseiam em regras. Quando você solta um evento comercial em uma jornada, ele adiciona automaticamente uma atividade **Ler público-alvo**, logo em seguida. Saiba como criar um evento comercial [nesta página](../event/about-creating-business.md).

## Eventos de qualificação de público-alvo {#audience-qualification-events}

Um evento de **qualificação de público-alvo** é acionado quando um perfil entra ou sai de um público-alvo. Por exemplo, um cliente que ultrapassa um limite de gastos de fidelidade entra no público-alvo da camada Gold — essa qualificação aciona a jornada desse perfil em tempo real (para públicos de transmissão) ou na próxima avaliação em lote. Diferentemente dos eventos unitários, a qualificação de público-alvo permite criar uma lógica de acionamento complexa usando o poder total das definições de público-alvo, sem exigir alterações de implementação para enviar um novo evento. Saiba mais sobre [eventos de qualificação de público](../building-journeys/audience-qualification-events.md).

>[!NOTE]
>
>Os eventos de qualificação de público-alvo não estão configurados em **Administration > Events** — eles são selecionados diretamente na tela de jornada como a primeira etapa de uma jornada.

## Visão geral dos eventos unitários versus de negócios {#event-comparison}

| | Evento unitário | Evento comercial |
|---|---|---|
| **Vinculado a um perfil?** | Sim — acionado pela ação de um indivíduo específico. | Não — acionado por uma ocorrência externa não vinculada a uma pessoa. |
| **Comportamento da entrada** | Um perfil entra na jornada em tempo real. | Vários perfis são inseridos por meio de uma etapa automática Ler público. |
| **Casos de uso típicos** | Recuperação de abandono de carrinho, envio de formulário, logon no aplicativo, marco de fidelidade. | Cancelamento de voo, alerta de reposição de estoque, últimas notícias, evento meteorológico. |
| **Como ele inicia a jornada** | Entrada baseada em eventos — nenhum público-alvo necessário. | Evento comercial + Público-alvo de leitura automático (adicionado pelo Journey Optimizer). |
| **Vários por jornada?** | Sim — você pode ouvir vários eventos unitários nas etapas do jornada. | Não — somente um evento comercial por jornada, colocado no início. |
| **Tipo de ID do evento** | Baseado em regras ou gerado pelo sistema. | Sempre com base em regras. |

>[!NOTE]
>
>Uma jornada pode conter apenas **um** evento comercial, que deve ser a primeira atividade. O Journey Optimizer adiciona automaticamente uma atividade **Read Audience** após ela para definir quais perfis recebem a jornada acionada por esse evento.

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
>O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço Principal de Coleção de Dados (DCCS) para acionar uma jornada. Eventos assimilados em lote, eventos inseridos via **Serviço de consulta**, ou eventos de conjuntos de dados internos do Journey Optimizer (Feedback de mensagens, Rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, crie um público-alvo com base nesses eventos e use a atividade **Público-alvo de leitura**. Tecnicamente, a qualificação de público-alvo pode ser usada, mas ela pode causar desafios posteriores com base nas ações usadas. Esses dados não precisam necessariamente acessar o Perfil em tempo real. Se você quiser usar os eventos para segmentação, recomendamos ativar o conjunto de dados para perfil.

## Como escolher {#choose-event-type}

Use os critérios a seguir para selecionar o tipo de evento correto para sua jornada — a pergunta principal é: **você está acionando uma ação para uma pessoa específica ou transmitindo para muitos perfis?** [Saiba mais sobre os tipos de jornada](../building-journeys/journey.md#journey-types).

* **Escolha um evento unitário** quando o acionador estiver vinculado a um indivíduo específico, por exemplo, uma compra, um envio de formulário ou um marco de fidelidade. Os eventos unitários exigem uma identidade principal baseada em pessoas no esquema e iniciam a jornada imediatamente para esse perfil. [Saiba como configurar um evento unitário](../event/about-creating.md).

* **Escolha um evento comercial** quando o gatilho for uma ocorrência global — por exemplo, um reabastecimento de produto, uma queda de preço ou um cancelamento de voo — e você quiser transmitir para um conjunto de perfis relacionados a esse sinal. Os eventos comerciais devem ser a primeira etapa na jornada e direcionar perfis automaticamente por meio de uma atividade **Ler público**. Eles exigem um esquema de série temporal com uma identidade primária que não seja de pessoas e os campos `_id` e `timestamp`. Planeje um atraso na exportação de público de 15 minutos a até uma hora. [Saiba como configurar um evento comercial](../event/about-creating-business.md).

* **Escolha um evento de qualificação de público-alvo** quando o acionador for um perfil entrando ou saindo de um público-alvo, e você precisar de uma lógica de segmentação mais complexa do que um único evento pode fornecer — por exemplo, reengajar clientes que acabaram de atingir um limite de gastos ou acionar um fluxo de integração quando um membro do VIP sair do nível de fidelidade. [Saiba mais sobre eventos de qualificação de público-alvo](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Os eventos comerciais não podem ser usados na mesma jornada que os eventos unitários ou as atividades de qualificação de público.

## Ciclo de dados {#data-cycle}

Eventos são chamadas POST API. Os eventos são enviados para o Adobe Experience Platform por meio de APIs de assimilação de streaming. O destino do URL de eventos enviados por meio de APIs de mensagens transacionais é chamado de &quot;inlet&quot;. A carga útil de eventos segue a formatação XDM.

A carga contém informações necessárias para que as APIs de Assimilação de streaming funcionem (no cabeçalho) e as informações necessárias para que [!DNL Journey Optimizer] funcionem e as informações que serão usadas em jornadas (no corpo, por exemplo, a quantidade de um carrinho abandonado). Há dois modos para a ingestão de transmissão, autenticados e não autenticados. Para obter detalhes sobre as APIs de ingestão de transmissão, consulte [este link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR){target="_blank"}.

Depois de chegar através das APIs de assimilação de streaming, os eventos fluem para um serviço interno chamado Pipeline e, em seguida, para o Adobe Experience Platform. Se o esquema do evento tiver o sinalizador de Serviço de perfil do cliente em tempo real habilitado e uma ID de conjunto de dados que também tenha o sinalizador de Perfil do cliente em tempo real, ele fluirá para o Serviço de perfil do cliente em tempo real.

Para eventos gerados pelo sistema, o Pipeline filtra os eventos que têm uma carga contendo [!DNL Journey Optimizer] eventIDs (consulte o processo de criação de eventos abaixo) fornecidos por [!DNL Journey Optimizer] e contidos na carga do evento. Para eventos baseados em regras, o sistema identifica o evento usando a condição eventID. Esses eventos são acompanhados pelo [!DNL Journey Optimizer] e a jornada correspondente é acionada.


## Sobre a taxa de transferência de eventos do Jornada {#event-thoughput}

A Adobe Journey Optimizer impõe limites de taxa de transferência separados por tipo de evento, em nível de organização, em todas as sandboxes:

* **Eventos unitários**: 5.000 eventos por segundo
* **Ler eventos de jornada baseados em público-alvo**: 5.000 eventos por segundo

Esses limites se aplicam a todos os eventos usados no jornada ativo, que inclui as jornadas **Live**, **Dry run**, **Closed** e **Paused**. Quando um limite é atingido, novos eventos são enfileirados e processados a 5.000 por segundo até que a fila seja esgotada.

Para obter mais detalhes sobre as taxas de processamento da jornada e como os diferentes tipos de jornada afetam a taxa de transferência, consulte [esta seção](../building-journeys/entry-management.md#journey-processing-rate).

Os seguintes tipos de eventos são contados para essas cotas:

* **Eventos Unitários Externos**: Inclui eventos com base em regras e gerados pelo sistema. Se o mesmo evento bruto se qualificar para várias definições de regra, cada regra qualificada será contada como um evento separado. Mais detalhes abaixo.

* **Eventos de qualificação de público-alvo**: se o mesmo público-alvo de streaming for usado em várias jornadas, cada uso será contado separadamente. Por exemplo, usar o mesmo público-alvo em uma atividade de qualificação de público-alvo em duas jornadas resulta na contagem de dois eventos.

* **Eventos de Reação**: eventos acionados por reações de perfil (email aberto, email clicado, etc.) em uma jornada.

* **Eventos comerciais**: eventos não vinculados a um perfil específico, mas a um evento comercial.

* **Eventos do Analytics**: se a [integração com o Adobe Analytics para acionar o jornada](about-analytics.md) tiver sido habilitada, esses eventos também serão incluídos.

* **Retomar Eventos**: evento técnico disparado quando um perfil é retomado de uma jornada pausada. Saiba mais sobre [retomada de jornadas pausadas](../building-journeys/journey-pause.md#journey-resume-steps).

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
