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
source-git-commit: 2f2b53fd74a51e96e61ddaf9e489c07bd359294f
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 26%

---

# Trabalhar com eventos de jornada {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de jornada"
>abstract="Um evento está vinculado a uma pessoa. Relaciona-se com o comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site, etc.) ou algo que acontece vinculado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos de fidelidade). É o que o Journey Optimizer considera nas jornadas para organizar as melhores ações futuras."

A configuração do evento permite definir as informações [!DNL Journey Optimizer] receberá como eventos. Você pode usar vários eventos (em etapas diferentes de uma jornada) e várias jornadas podem usar o mesmo evento.

>[!CAUTION]
>
>A configuração do evento é **obrigatório** e deve ser executado por um **engenheiro de dados**.

Você pode configurar dois tipos de eventos:

* **Unitário** events: esses eventos estão vinculados a uma pessoa. Elas estão relacionadas ao comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site etc.) ou algo que acontece vinculado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos de fidelidade). Isso é o que [!DNL Journey Optimizer] O escutará no jornada para orquestrar as melhores ações futuras. Os eventos unitários podem ser baseados em regras ou gerados pelo sistema. Para saber como criar um evento unitário, consulte este [página](../event/about-creating.md).

* **Empresas** eventos: um evento comercial é um evento que, ao contrário de um evento unitário, não está vinculado a um perfil específico. Por exemplo, pode ser um alerta de notícias, uma atualização esportiva, uma alteração ou cancelamento de voo, uma atualização de inventário, eventos meteorológicos etc. Embora esses eventos não sejam específicos de um perfil, eles podem ser de interesse para qualquer número de perfis: indivíduos inscritos em tópicos de notícias específicos, passageiros em um voo, compradores interessados em um produto indisponível, etc. Os eventos comerciais sempre se baseiam em regras. Quando você solta um evento comercial em uma jornada, ele adiciona automaticamente um **Ler público** atividade logo após. Para saber como criar um evento comercial, consulte esta [página](../event/about-creating-business.md).


>[!NOTE]
>
>Se você editar um evento usado em um rascunho ou em uma jornada em tempo real, poderá apenas alterar o nome, a descrição ou adicionar campos de carga útil. Limitamos rigorosamente a edição de jornadas de rascunho ou ao vivo para evitar a quebra de jornadas.

As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

➡️ [Descubra este recurso no vídeo](#video)

## Tipo de ID do evento{#event-id-type}

Para eventos comerciais, o tipo de ID do evento sempre se baseia em regras.

Para eventos unitários, há dois tipos de ID de evento:

* **Baseado em regras** events: esse tipo de evento não gera uma eventID. Usando o editor de expressões simples, basta definir uma regra que será usada pelo sistema para identificar os eventos relevantes que acionarão suas jornadas. Essa regra pode ser baseada em qualquer campo disponível na carga do evento, por exemplo, o local do perfil ou o número de itens adicionados ao carrinho do perfil.

  >[!CAUTION]
  >
  >Uma regra de limite é definida para eventos baseados em regras. Limita o número de eventos qualificados que uma jornada pode processar para 5000 por segundo em uma determinada organização. Corresponde aos SLAs do Journey Optimizer. Journey Optimizer Consulte as licenças e os [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html).

* **Gerado pelo sistema** events: esses eventos exigem uma eventID. Este campo eventID é gerado automaticamente ao criar o evento. O sistema que envia o evento não deve gerar uma ID, mas sim passar a disponível na pré-visualização de carga.

>[!NOTE]
>
>O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço principal de coleção de dados (DCCS) para acionar uma jornada. Eventos assimilados em lote ou eventos de conjuntos de dados internos do Journey Optimizer (feedback de mensagem, rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, crie um público-alvo com base nesses eventos e use a atividade **Público-alvo de leitura**. Tecnicamente, a qualificação de público-alvo pode ser usada, mas ela pode causar desafios posteriores com base nas ações usadas. Esses dados não precisam necessariamente acessar o Perfil em tempo real. Se você quiser usar os eventos para segmentação ou pesquisa em uma jornada separada, recomendamos ativar o conjunto de dados para perfil.

## Ciclo de dados {#data-cycle}

Eventos são chamadas de API POST. Os eventos são enviados para o Adobe Experience Platform por meio de APIs de assimilação de streaming. O destino do URL de eventos enviados por meio de APIs de mensagens transacionais é chamado de &quot;inlet&quot;. A carga útil de eventos segue a formatação XDM.

O payload contém informações necessárias para que as APIs de assimilação de streaming funcionem (no cabeçalho) e as informações necessárias para [!DNL Journey Optimizer] para trabalhar e as informações a serem usadas em jornadas (no corpo, por exemplo, a quantidade de um carrinho abandonado). Há dois modos para a assimilação de streaming, autenticados e não autenticados. Para obter detalhes sobre as APIs de assimilação de fluxo, consulte [este link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR).

Depois de chegar através das APIs de assimilação de streaming, os eventos fluem para um serviço interno chamado Pipeline e, em seguida, para o Adobe Experience Platform. Se o esquema de evento tiver o sinalizador de Serviço de perfil do cliente em tempo real ativado e uma ID de conjunto de dados que também tenha o sinalizador de Perfil do cliente em tempo real, ele fluirá para o Serviço de perfil do cliente em tempo real.

Para eventos gerados pelo sistema, o Pipeline filtra os eventos que têm uma carga útil contendo [!DNL Journey Optimizer] eventIDs (consulte o processo de criação de eventos abaixo) fornecidos pelo [!DNL Journey Optimizer] e contido na carga do evento. Para eventos baseados em regras, o sistema identifica o evento usando a condição eventID. Esses eventos são acompanhados pelo [!DNL Journey Optimizer] e a jornada correspondente é acionada.

## Vídeos tutoriais {#video}

Saiba como configurar um evento, especificar o ponto final de transmissão e a carga útil de um evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Entenda os casos de uso aplicáveis a eventos comerciais. Saiba como criar uma jornada usando um evento comercial e quais práticas recomendadas devem ser aplicadas.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
