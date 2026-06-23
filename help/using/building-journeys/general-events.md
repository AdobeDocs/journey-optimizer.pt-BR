---
solution: Journey Optimizer
product: journey optimizer
title: Eventos gerais
description: Saiba como usar eventos gerais
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: personalizado, geral, eventos, jornada
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jKMddtFlzmUinPK5-onY2u-kRAd1MD126biQVwq3aAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1253
ht-degree: 12%

---

# Eventos gerais {#general-events}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar eventos gerais para acionar jornadas de forma unitária em tempo real e configurar tempos limite de eventos e caminhos de tempo limite para ouvir um evento apenas durante um período definido.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos unitários"
>abstract="Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens em tempo real à pessoa que flui para a jornada. Para esse tipo de evento, só é possível adicionar um rótulo e uma descrição. A configuração do evento é executada por um engenheiro de dados e não pode ser editada."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="Eventos de negócios"
>abstract="Esses eventos permitem iniciar uma jornada usando um evento não relacionado a perfis. Quando esse evento é acionado, é possível enviar mensagens para um público-alvo de perfis. Para esse tipo de evento, só é possível adicionar um rótulo e uma descrição. A configuração do evento é executada por um usuário técnico e não pode ser editada."

Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens em tempo real à pessoa que flui para a jornada.

Para esse tipo de evento, só é possível adicionar um rótulo e uma descrição. O restante da configuração não pode ser editado. Ele foi executado pelo usuário técnico. Consulte [esta página](../event/about-events.md).

Saiba mais sobre a taxa de transferência de eventos e as taxas de processamento de jornada em [esta seção](entry-management.md#journey-processing-rate).

![Painel de configuração de eventos gerais com seleção e configurações de evento](assets/general-events.png)

Quando você solta um evento comercial, ele adiciona automaticamente uma atividade **Ler público**. Para obter mais informações sobre eventos comerciais, consulte [esta seção](../event/about-events.md)

## Acompanhamento de eventos durante um período específico {#events-specific-time}

Uma atividade de evento posicionada na jornada escuta eventos indefinidamente. Para acompanhar um evento somente durante um determinado tempo, você deve configurar um tempo limite para o evento.

A jornada ouvirá o evento durante o tempo especificado no tempo limite. Se um evento for recebido durante esse período, a pessoa fluirá no caminho do evento. Caso contrário, o cliente fluirá para o caminho de tempo limite, se estiver definido, ou continuará essa jornada.

Se nenhum caminho de tempo limite for definido, a configuração de tempo limite atuará como uma atividade de espera, fazendo com que o perfil aguarde um período, que pode ser interrompido se um evento ocorrer antes do fim dessa espera. Se desejar que os perfis sejam excluídos dessa jornada após o tempo limite, será necessário definir um caminho de tempo limite.

Para configurar um tempo limite para um evento, siga estas etapas:

1. Ative a opção **[!UICONTROL Definir o tempo limite do evento]** nas propriedades do evento.

1. Especifique por quanto tempo a jornada aguardará pelo evento. A duração máxima é de **90 dias**.

1. Quando nenhum evento é recebido dentro do tempo limite especificado, a prática recomendada é enviar os indivíduos para um caminho de tempo limite. Para isso, habilite a opção **[!UICONTROL Definir um caminho de tempo limite]**. Nesse caso, a jornada continua para o indivíduo assim que o tempo limite é atingido. Recomendamos que você sempre habilite a opção **[!UICONTROL Definir um caminho de tempo limite]**.

   ![Configuração de tempo limite de evento com opções de caminho de duração e tempo limite](assets/event-timeout.png)

Neste exemplo, a jornada envia um primeiro email de boas-vindas para um cliente depois que ele entra no lobby. Em seguida, ele envia um email de desconto para refeições somente se o cliente entrar no restaurante no dia seguinte. Portanto, configuramos o evento do restaurante com um tempo limite de 1 dia:

* Se o evento do restaurante for recebido menos de 1 dia após o email de boas-vindas, o email de desconto para refeições será enviado.
* Se nenhum evento de restaurante for recebido no dia seguinte, a pessoa fluirá pelo caminho de tempo limite.

Observe que se quiser configurar um tempo limite em vários eventos posicionados após uma atividade **[!UICONTROL Wait]**, será necessário configurar o tempo limite apenas em um desses eventos.

O tempo limite definido se aplica a todos os eventos posicionados após a atividade **[!UICONTROL Wait]**:

* Se um evento for recebido dentro da duração do tempo limite, o indivíduo fluirá para o caminho do evento recebido.
* Se nenhum evento for recebido dentro da duração do tempo limite, o indivíduo fluirá para a ramificação de tempo limite do evento em que o tempo limite foi definido.

![Vários eventos com configurações de tempo limite no jornada](assets/event-timeout-group.png)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página explica como usar eventos gerais (unitários e comerciais) no jornada para acionar a entrega de mensagens em tempo real e em nível individual, incluindo como configurar tempos limite de eventos e caminhos de tempo limite.

**Intenções:**
* Adicione uma atividade de evento geral a uma tela de jornada para acionar a entrada de perfil em tempo real
* Configure o tempo limite de um evento para limitar por quanto tempo uma jornada escuta um evento
* Configure um caminho de tempo limite para lidar com perfis que não acionam o evento esperado a tempo
* Faça a distinção entre eventos unitários e eventos de negócios e entenda quando cada um é adicionado automaticamente
* Combine tempos limite de evento com atividades de espera para controlar o comportamento do tempo limite de vários eventos

**Glossário:**
* **Evento unitário**: um evento que dispara a jornada para um indivíduo de cada vez, em tempo real *(específico do produto)*
* **Evento comercial**: um evento não relacionado a perfis que dispara uma jornada para um público de perfis, adicionando automaticamente uma atividade Ler público *(específico do produto)*
* **Tempo limite de evento**: uma duração configurável (até 90 dias) após a qual a jornada para de aguardar um evento específico e direciona o perfil para um caminho de tempo limite *(específico do produto)*
* **Caminho de tempo limite**: uma ramificação de jornada opcional que os perfis seguem quando o evento esperado não é recebido na janela de tempo limite *(específico do produto)*

**Medidas de Proteção:**
* O rótulo e a descrição do evento são os únicos campos editáveis para um evento geral na tela; todas as outras configurações são executadas por um usuário técnico e não podem ser alteradas na jornada
* O tempo limite máximo do evento é de 90 dias
* Quando vários eventos seguem uma atividade Wait, o tempo limite deve ser configurado em apenas um desses eventos; o tempo limite definido se aplica a todos os eventos após a atividade Wait
* Se nenhum caminho de tempo limite for definido, o tempo limite atuará como uma atividade Wait; os perfis que não recebem o evento permanecerão na jornada até que o tempo limite expire

**Terminologia:**
* Nome canônico: Evento geral — Acrônimo: none — variantes: evento unitário, evento personalizado
* Sinônimos: &quot;evento geral&quot; = &quot;evento unitário&quot; (no contexto da atividade da tela)
* Não confunda: &quot;evento comercial&quot; ≠ &quot;evento unitário&quot; — um evento comercial direciona um público-alvo de perfis, enquanto um evento unitário direciona um único indivíduo

**Perguntas frequentes:**
* **P: Posso alterar a configuração do evento na tela de jornada?** — Não; somente o rótulo e a descrição podem ser editados na tela. A configuração completa do evento é definida por um usuário técnico e não pode ser modificada na jornada.
* **P: O que acontece se nenhum evento for recebido antes que o tempo limite expire?** — Se um caminho de tempo limite for definido, o perfil fluirá para esse caminho. Se nenhum caminho de tempo limite for definido, o tempo limite se comportará como uma atividade de espera e o perfil continuará a jornada após o período de tempo limite.
* **P: Qual é a duração máxima do tempo limite do evento?** — 90 dias.
* **P: Quando devo habilitar a opção de caminho de tempo limite?** — Sempre ative-a se quiser que os perfis saiam dessa ramificação depois do tempo limite; sem um caminho de tempo limite, os perfis permanecem na jornada aguardando o evento.
* **P: Como um evento comercial difere de um evento unitário na tela de jornada?** — a eliminação de um evento comercial adiciona automaticamente uma atividade Ler público, pois os eventos comerciais visam vários perfis simultaneamente, em vez de um único indivíduo.

+++
