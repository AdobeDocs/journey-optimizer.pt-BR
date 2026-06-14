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
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 678
ht-degree: 22%

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
