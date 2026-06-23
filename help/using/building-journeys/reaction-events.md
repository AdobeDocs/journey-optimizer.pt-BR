---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de reações
description: Saiba como usar eventos de reação para responder aos dados de rastreamento de mensagens, como aberturas e cliques em suas jornadas, e configurar caminhos de tempo limite para não respondedores.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: jornada, eventos, reação, rastreamento, plataforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1030
ht-degree: 7%

---

# Eventos de reação {#reaction-events}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade Reação para responder aos dados de rastreamento de mensagens, como aberturas e cliques na mesma jornada, e configurar caminhos de tempo limite para indivíduos que não participam.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reação"
>abstract="Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a [!DNL Adobe Experience Platform]."

## Visão geral {#overview}

Entre as diferentes atividades de evento disponíveis na paleta, você encontrará o evento **[!UICONTROL Reações]** interno. Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a [!DNL Adobe Experience Platform].

Você pode reagir a mensagens clicadas ou abertas. Por exemplo, você pode enviar outra mensagem se um indivíduo tiver aberto o email anterior ou clicado nele, ou enviar uma mensagem de acompanhamento diferente se ele não interagiu com a sua comunicação.

Consulte [Atividades de ação](../building-journeys/about-journey-activities.md#action-activities).

Você pode usar a atividade **[!UICONTROL Reação]** para executar uma ação quando não houver reação às suas mensagens. Para fazer isso, crie um segundo caminho paralelo à atividade **[!UICONTROL Reaction]** e adicione uma atividade **[!UICONTROL Wait]**. Se não houver reação durante o período definido na atividade **[!UICONTROL Wait]**, o segundo caminho será escolhido. Você pode optar por enviar, por exemplo, uma mensagem de acompanhamento.

## Como configurar eventos de reação {#configure}

![Reagir à configuração do evento com a seleção de canal e as opções de tipo de evento](assets/journey45.png)

Siga estas etapas para configurar os eventos de reação:

1. Coloque uma atividade **[!UICONTROL Reação]** **imediatamente** após uma [atividade de ação de canal](journey-action.md) na tela de jornada.
1. Adicione um **[!UICONTROL Rótulo]** à reação. Esta etapa é opcional.
1. Na lista suspensa, selecione a atividade de ação à qual deseja reagir. Você pode selecionar qualquer atividade de ação posicionada nas etapas anteriores do caminho.
1. Dependendo da ação selecionada, escolha a que deseja reagir.
1. Você pode definir um tempo limite de evento (entre 40 segundos e 90 dias) e um caminho de tempo limite. Isso cria um segundo caminho para indivíduos que não reagiram dentro da duração definida. Ao testar uma jornada que usa um evento de reação, o padrão do modo de teste **[!UICONTROL Tempo de espera]** e o valor mínimo é de 40 segundos. Consulte [esta seção](../building-journeys/testing-the-journey.md).

## Medidas de proteção e limitações {#guardrails-limitations}

* Uma atividade **[!UICONTROL Reação]** deve ser colocada **imediatamente** após uma [atividade de ação de canal](journey-action.md) na tela de jornada.
* Você não pode usar uma atividade **[!UICONTROL Reação]** se não houver uma atividade de ação de canal antes dela.
* Não há suporte para a colocação de uma atividade **[!UICONTROL Wait]** ou qualquer outra atividade entre a ação de canal e a atividade **[!UICONTROL Reaction]** e pode fazer com que a Reação não funcione conforme esperado.
* Os eventos de reação só podem rastrear mensagens enviadas na mesma jornada. Eles não podem rastrear mensagens que ocorrem em uma jornada diferente.
* Os eventos de reação rastreiam cliques em links do tipo &quot;rastreado&quot;. Links de unsubscription e mirror pages não são considerados.
* As aberturas de email são rastreadas usando uma imagem de 0 pixel incluída no email. Se os clientes de email (como o Gmail) bloquearem imagens, as aberturas de email não serão consideradas.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página explica como usar a atividade de evento Reação integrada no Adobe Journey Optimizer para ramificar caminhos de jornada com base em dados de envolvimento de mensagens em tempo real, como aberturas de email e cliques em links.

**Intenções:**
* Adicionar uma atividade de evento de reação para responder a aberturas ou cliques de mensagem em uma jornada
* Configure uma duração de tempo limite e um caminho de fallback para os perfis que não interagem
* Criar um caminho paralelo com uma atividade de espera para lidar com usuários que não respondem
* Selecionar uma atividade de ação de canal upstream específica a ser ouvida

**Glossário:**
* **Evento de reação**: uma atividade de evento de jornada interna que escuta dados de rastreamento em tempo real (aberturas, cliques) de uma mensagem enviada anteriormente na mesma jornada *(específico do produto)*
* **Caminho de tempo limite**: uma ramificação de jornada secundária que os perfis seguem se não produzirem a reação esperada dentro do período de tempo limite definido *(específico do produto)*

**Medidas de Proteção:**
* A atividade Reaction deve ser colocada imediatamente após uma atividade channel action; nenhuma outra atividade pode ser colocada entre elas.
* Uma atividade Reaction não pode ser usada se não houver uma atividade de ação de canal antes dela no caminho.
* Os eventos de reação só podem rastrear mensagens enviadas na mesma jornada; não há suporte para rastreamento entre jornadas.
* Links de unsubscription e links de mirror pages não são rastreados por eventos de reação.
* As aberturas de email dependem de uma imagem de rastreamento de 0 pixel; se o cliente de email bloquear imagens (por exemplo, Gmail), as aberturas não serão registradas.
* O intervalo de tempo limite do evento é de 40 segundos a 90 dias; o valor mínimo no modo de teste também é de 40 segundos.

**Terminologia:**
* Nome canônico: Eventos de reação — Acrônimo: none — variantes: atividade de reação, evento de rastreamento de engajamento
* Sinônimos: &quot;Evento de reação&quot; = &quot;evento de envolvimento de mensagem&quot; = &quot;evento de rastreamento&quot;
* Não confunda: &quot;Evento de reação&quot; ≠ &quot;evento externo&quot; (os eventos de reação são incorporados e vinculados a mensagens de mesma jornada; os eventos externos vêm de fora da jornada)

**Perguntas frequentes:**
* **P: Um evento de Reação pode rastrear uma mensagem enviada em uma jornada diferente?** — Não; os eventos de reação só rastreiam mensagens enviadas na mesma jornada.
* **P: Como faço para lidar com perfis que não abrem ou clicam em uma mensagem?** — Adicione um caminho paralelo ao lado da atividade Reaction com uma atividade Wait; os perfis que não reagirem dentro da duração de espera seguirão esse segundo caminho.
* **P: Os cliques no link de cancelamento de inscrição são rastreados por eventos de reação?** — Não; somente os tipos de links rastreados são capturados. Os links de unsubscription e mirror page são excluídos.
* **P: O que acontece se um cliente de email bloquear imagens?** — Aberturas de email rastreadas pela imagem de 0 pixel não serão gravadas para clientes que bloqueiam imagens, como o Gmail.
* **P: Qual é o intervalo de tempo limite válido para um evento de reação?** — Entre 40 segundos e 90 dias.

+++
