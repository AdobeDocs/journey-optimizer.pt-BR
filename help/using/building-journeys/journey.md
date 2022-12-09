---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a jornadas
description: Introdução a jornadas
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---


# Introdução a jornadas{#jo-general-principle}

Use [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados.

Projete cenários avançados com várias etapas e com os seguintes recursos:

* Enviar em tempo real **entrega unitária** acionado quando um evento é recebido, ou **em lote** usando segmentos da Adobe Experience Platform.

* Aproveitamento **dados contextuais** de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

* Use o **ações integradas** para enviar mensagens projetadas no [!DNL Journey Optimizer] ou criar **ações personalizadas** se estiver usando um sistema de terceiros para enviar mensagens.

* Com o **designer de jornada** crie seus casos de uso em várias etapas: arraste e solte facilmente um evento de entrada ou uma atividade de segmento de leitura, adicione condições e envie mensagens personalizadas.

## Etapas para criar uma jornada{#steps-journey}

Use o Adobe Journey Otimizer para projetar e orquestrar jornadas personalizadas de uma única tela.

O Adobe Journey Otimizer inclui uma tela de orquestração omnicanal que permite que os profissionais de marketing harmonizem o alcance de marketing com o envolvimento de um para um cliente. A interface do usuário permite arrastar e soltar facilmente atividades da paleta na tela para criar sua jornada.

![](assets/interface-journeys.png)

Saiba como iniciar e criar sua primeira jornada no [esta página](journey-gs.md).

O designer de jornada omnicanal ajuda você a criar jornadas em várias etapas com públicos-alvo direcionados, atualizações baseadas em interações comerciais ou clientes em tempo real e mensagens omnicanais usando uma interface de arrastar e soltar intuitiva.

![](assets/journey38.png)

Leia mais em [esta seção](using-the-journey-designer.md).

Como engenheiro de dados, as etapas para configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações são detalhadas em [esta seção](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Saiba como criar jornadas nos seguintes casos de uso completos.

Casos de uso comercial:

* [Enviar mensagens de vários canais](journeys-uc.md)
* [Enviar uma mensagem usando o Campaign v7/v8](ajo-ac.md)
* [Enviar uma mensagem aos assinantes](message-to-subscribers-uc.md)

Casos de uso técnico:

* [Envie coleções dinamicamente usando ações personalizadas](collections.md)
* [Aumentar entregas](ramp-up-deliveries-uc.md)
* [Limite a taxa de transferência com fontes de dados externas e ações personalizadas](limit-throughput.md)

## Versões de jornada{#journey-versions}

Na lista de jornada, todas as versões da jornada são exibidas com o número da versão. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Quando você procura por uma jornada, as versões mais recentes aparecem no topo da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida no topo da interface da edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Geralmente, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá entrar novamente em uma jornada, mas não poderá fazê-lo até que ele tenha saído totalmente dessa instância anterior da jornada. [Leia mais](end-journey.md).

Se precisar modificar para uma jornada ao vivo, crie uma nova versão da jornada.

1. Abra a versão mais recente da sua jornada ao vivo, clique em **[!UICONTROL Create a new version]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Você só pode criar uma nova versão da versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publish]** e confirme.

   ![](assets/journeyversions3.png)

A partir do momento em que a jornada é publicada, os indivíduos começarão a fluir para a versão mais recente da jornada. As pessoas que já entraram em uma versão anterior ficam lá até terminarem a jornada. Se mais tarde entrarem na mesma jornada, vão para a versão mais recente.

As versões de jornada podem ser interrompidas individualmente. Todas as versões de jornadas têm o mesmo nome.

Quando você publica uma nova versão de uma jornada, a versão anterior automaticamente termina e alterna para a **Fechado** status. Nenhuma entrada na jornada pode acontecer. Mesmo que você pare a versão mais recente, a versão anterior permanecerá fechada.

>[!NOTE]
>
>Saiba mais sobre as medidas de proteção e limitações das versões da jornada, em [esta página](../start/guardrails.md#journey-versions-limitations)