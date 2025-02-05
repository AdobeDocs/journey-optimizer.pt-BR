---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com eventos de jornada
description: Saiba como trabalhar com eventos em suas jornadas
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: events, event, jornada, definition, start
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: aec3d79ad07ec6904e55afd6fc61ba9b4f403fc8
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 52%

---

# Trabalhar com eventos de jornada {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de jornada"
>abstract="Um evento está vinculado a uma pessoa. Ele se refere ao comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site etc.) ou a um acontecimento relacionado a uma pessoa (por exemplo, uma pessoa acumulou 10 mil pontos de fidelidade). É o que o Journey Optimizer considera nas jornadas para organizar as melhores ações futuras."

A configuração do evento permite definir as informações que o [!DNL Journey Optimizer] receberá como eventos. Você pode usar vários eventos (em etapas diferentes de uma jornada) e várias jornadas podem usar o mesmo evento.

>[!CAUTION]
>
>A configuração do evento é **obrigatória** e deve ser executada por um **engenheiro de dados**.

Você pode configurar dois tipos de eventos:

* Eventos **Unitários**: esses eventos estão vinculados a uma pessoa. Relacionam-se com o comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site, etc.) ou com algo que acontece ligado a uma pessoa (por exemplo, uma pessoa atingiu 10 000 pontos de fidelidade). É o que [!DNL Journey Optimizer] escutará no jornada para orquestrar as melhores ações futuras. Os eventos unitários podem ser baseados em regras ou gerados pelo sistema. Para saber como criar um evento unitário, consulte esta [página](../event/about-creating.md).

* **Eventos comerciais**: um evento comercial é um evento que, ao contrário de um evento unitário, não está vinculado a um perfil específico. Por exemplo, pode ser um alerta de notícias, uma atualização esportiva, uma alteração ou cancelamento de voo, uma atualização de inventário, eventos meteorológicos etc. Embora esses eventos não sejam específicos de um perfil, eles podem ser de interesse para qualquer número de perfis: indivíduos inscritos em tópicos de notícias específicos, passageiros em um voo, compradores interessados em um produto indisponível, etc. Os eventos comerciais sempre se baseiam em regras. Quando você solta um evento comercial em uma jornada, ele adiciona automaticamente uma atividade **Ler público-alvo**, logo em seguida. Para saber como criar um evento comercial, consulte esta [página](../event/about-creating-business.md).


>[!NOTE]
>
>Se você editar um evento usado em um rascunho ou em uma jornada ao vivo, será possível apenas alterar o nome, a descrição ou adicionar campos de carga útil. Limitamos rigorosamente a edição de rascunho ou jornadas ao vivo para evitar a quebra de jornadas.

As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada do perfil é temporariamente bloqueada por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (quer seja o mesmo evento ou outro que acione a mesma jornada), essa jornada não será reiniciada para esse perfil.

➡️ [Descubra este recurso no vídeo](#video)

## Tipo de ID do evento{#event-id-type}

Para eventos comerciais, o tipo de ID do evento sempre se baseia em regras.

Para eventos unitários, há dois tipos de ID de evento:

* **Eventos baseados em regras**: esse tipo de evento não gera uma eventID. Usando o editor de expressões simples, basta definir uma regra que será usada pelo sistema para identificar os eventos relevantes que acionarão suas jornadas. Essa regra pode ser baseada em qualquer campo disponível na carga do evento, por exemplo, o local do perfil ou o número de itens adicionados ao carrinho do perfil.

  >[!CAUTION]
  >
  >Uma regra de limite é definida para eventos baseados em regras. Limita o número de eventos qualificados que uma jornada pode processar para 5.000 por segundo em uma determinada organização. Corresponde aos SLAs do Journey Optimizer. Consulte seu licenciamento da Journey Optimizer e a [Descrição do Produto da Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html).

* **Eventos gerados pelo sistema**: esses eventos exigem uma eventID. Esse campo eventID é gerado automaticamente ao criar o evento. O sistema que envia o evento não deve gerar uma ID, mas sim passar a disponível na pré-visualização de carga.

>[!NOTE]
>
>O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço principal de coleção de dados (DCCS) para acionar uma jornada. Eventos assimilados em lote ou eventos de conjuntos de dados internos da Journey Optimizer (Feedback de mensagem, Rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, crie um público-alvo com base nesses eventos e use a atividade **Público-alvo de leitura**. Tecnicamente, a qualificação de público-alvo pode ser usada, mas ela pode causar desafios posteriores com base nas ações usadas. Esses dados não precisam necessariamente acessar o Perfil em tempo real. Se você quiser usar os eventos para segmentação ou pesquisa em uma jornada separada, recomendamos ativar o conjunto de dados para perfil.

## Ciclo de dados {#data-cycle}

Eventos são chamadas POST API. Os eventos são enviados para o Adobe Experience Platform por meio de APIs de assimilação de streaming. O destino do URL de eventos enviados por meio de APIs de mensagens transacionais é chamado de &quot;inlet&quot;. A carga útil de eventos segue a formatação XDM.

A carga contém informações necessárias para que as APIs de Assimilação de streaming funcionem (no cabeçalho) e as informações necessárias para que [!DNL Journey Optimizer] funcionem e as informações que serão usadas em jornadas (no corpo, por exemplo, a quantidade de um carrinho abandonado). Há dois modos para a assimilação de fluxo, autenticados e não autenticados. Para obter detalhes sobre as APIs de assimilação de fluxo, consulte [este link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR).

Depois de chegar através das APIs de assimilação de streaming, os eventos fluem para um serviço interno chamado Pipeline e, em seguida, para o Adobe Experience Platform. Se o schema do evento tiver o sinalizador de Serviço de perfil do cliente em tempo real ativado e uma ID de conjunto de dados que também tenha o sinalizador de Perfil do cliente em tempo real, ele fluirá para o Serviço de perfil do cliente em tempo real.

Para eventos gerados pelo sistema, o Pipeline filtra os eventos que têm uma carga contendo [!DNL Journey Optimizer] eventIDs (consulte o processo de criação de eventos abaixo) fornecidos por [!DNL Journey Optimizer] e contidos na carga do evento. Para eventos baseados em regras, o sistema identifica o evento usando a condição eventID. Esses eventos são acompanhados pelo [!DNL Journey Optimizer] e a jornada correspondente é acionada.

## Vídeos tutoriais {#video}

Saiba como configurar um evento, especificar o ponto final de transmissão e a carga útil de um evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Entenda os casos de uso aplicáveis a eventos comerciais. Saiba como criar uma jornada usando um evento comercial e quais práticas recomendadas devem ser aplicadas.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
