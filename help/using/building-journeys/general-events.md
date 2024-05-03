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
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 12%

---

# Eventos gerais {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos unitários"
>abstract="Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens em tempo real à pessoa que flui para a jornada. Para esse tipo de evento, você só pode adicionar um rótulo e uma descrição. A configuração do evento é executada por um engenheiro de dados e não pode ser editada."

Os Eventos permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada.

Para esse tipo de evento, você só pode adicionar um rótulo e uma descrição. O restante da configuração não pode ser editado. Ele foi executado pelo usuário técnico. Consulte [esta página](../event/about-events.md).

![](assets/general-events.png)

Quando você solta um evento comercial, ele adiciona automaticamente um **Ler público-alvo** atividade. Para obter mais informações sobre eventos comerciais, consulte [nesta seção](../event/about-events.md)

## Acompanhamento de eventos durante um período específico {#events-specific-time}

Uma atividade de evento posicionada na jornada escuta eventos indefinidamente. Para acompanhar um evento somente durante um determinado tempo, você deve configurar um tempo limite para o evento.

A jornada ouvirá o evento durante o tempo especificado no tempo limite. Se um evento for recebido durante esse período, a pessoa fluirá no caminho do evento. Caso contrário, o cliente fluirá para o caminho de tempo limite, se estiver definido, ou continuará essa jornada.

Se nenhum caminho de tempo limite for definido, a configuração de tempo limite atuará como uma atividade de espera, fazendo com que o perfil aguarde um período, que pode ser interrompido se um evento ocorrer antes do fim dessa espera. Se desejar que os perfis sejam excluídos dessa jornada após o tempo limite, será necessário definir um caminho de tempo limite.

Para configurar um tempo limite para um evento, siga estas etapas:

1. Ativar o **[!UICONTROL Definir o tempo limite do evento]** nas propriedades do evento.

1. Especifique por quanto tempo a jornada aguardará pelo evento. A duração máxima é de 29 dias.

1. Se desejar enviar as pessoas físicas para um caminho de tempo limite quando nenhum evento for recebido dentro do tempo limite especificado, habilite o **[!UICONTROL Definir um caminho de tempo limite]** opção. Se essa opção não estiver ativada, a jornada continuará para o indivíduo assim que o tempo limite for atingido. Recomendamos que você sempre ative a opção **Definir um caminho de tempo limite** opção.

   ![](assets/event-timeout.png)

Neste exemplo, a jornada envia um primeiro email de boas-vindas para um cliente depois que ele entra no lobby. Em seguida, ele envia um email de desconto para refeições somente se o cliente entrar no restaurante no dia seguinte. Portanto, configuramos o evento do restaurante com um tempo limite de 1 dia:

* Se o evento do restaurante for recebido menos de 1 dia após o email de boas-vindas, o email de desconto para refeições será enviado.
* Se nenhum evento de restaurante for recebido no dia seguinte, a pessoa fluirá pelo caminho de tempo limite.

Observe que se quiser configurar um tempo limite em vários eventos posicionados após um **[!UICONTROL Aguardar]** atividade, é necessário configurar o tempo limite em apenas um desses eventos.

O tempo limite definido se aplica a todos os eventos posicionados após o **[!UICONTROL Aguardar]** atividade:

* Se um evento for revelado dentro da duração do tempo limite, o indivíduo fluirá para o caminho do evento recebido.
* Se nenhum evento for recebido dentro da duração do tempo limite, o indivíduo fluirá para a ramificação de tempo limite do evento em que o tempo limite foi definido.

![](assets/event-timeout-group.png)
