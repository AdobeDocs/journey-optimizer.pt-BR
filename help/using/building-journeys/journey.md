---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a jornadas
description: Introdução a jornadas
feature: Journeys
role: User
level: Beginner
keywords: jornada, descobrir, começar
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: c235e7cd77e50a15a12f6ed14e51ca4185ecb7c2
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 24%

---


# Introdução a jornadas{#jo-general-principle}

Uso [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados.

Crie designs de cenários avançados com várias etapas e com os seguintes recursos:

* Envie **entrega unitária** em tempo real acionada quando um evento é recebido, ou **em lote** usando segmentos da Adobe Experience Platform.

* Aproveite **dados contextuais** de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

* Use o **ações integradas** para enviar mensagens projetadas no [!DNL Journey Optimizer] ou criar **ações personalizadas** se você estiver usando um sistema de terceiros para enviar mensagens.

* Com o **Designer de jornadas**, crie seus casos de uso em várias etapas: arraste e solte facilmente um evento de entrada ou uma atividade de segmento de leitura, adicione condições e envie mensagens personalizadas.


>[!NOTE]
>
>As medidas de proteção e limitações da jornada são detalhadas em [esta página](../start/guardrails.md)

## Etapas para criar uma jornada{#steps-journey}

Use o Adobe Journey Optimizer para projetar e orquestrar jornadas personalizadas com base em uma única tela. As principais etapas para criar uma jornada são as seguintes:

![](assets/journey-creation-process.png)

O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite aos profissionais de marketing harmonizar o alcance de marketing com o envolvimento individual do cliente. A interface de usuário do permite arrastar e soltar facilmente as atividades da paleta na tela para criar sua jornada.

![](assets/interface-journeys.png)

Saiba como iniciar e criar sua primeira jornada no [esta página](journey-gs.md).

O designer de jornadas omnicanal auxilia você na construção de jornadas de várias etapas, direcionando públicos especificamente e incorporando atualizações com base em interações de clientes ou negócios em tempo real. Ela também permite criar mensagens omnicanal por meio de uma interface intuitiva de arrastar e soltar.

![](assets/journey38.png)

Leia mais em [nesta seção](using-the-journey-designer.md).

Como engenheiro de dados, as etapas para configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações, são detalhadas em [nesta seção](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Saiba como criar jornadas nos seguintes casos de uso completos.

Casos de uso comercial:

* [Enviar mensagens de vários canais](journeys-uc.md)
* [Enviar uma mensagem usando o Campaign v7/v8](ajo-ac.md)
* [Enviar uma mensagem aos assinantes](message-to-subscribers-uc.md)

Casos de uso técnicos:

* [Envio dinâmico de coleções usando ações personalizadas](collections.md)
* [Incrementar entregas](ramp-up-deliveries-uc.md)
* [Limite a taxa de transferência com Fontes de dados externas e Ações personalizadas](limit-throughput.md)

## Versões de jornada{#journey-versions}

Na lista de jornada, todas as versões de jornada são exibidas com o número da versão. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada, e o aplicativo a manterá como uma preferência do usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Geralmente, um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá inserir uma jornada novamente, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada. [Leia mais](end-journey.md).

Se precisar modificar para uma jornada em tempo real, crie uma nova versão da jornada.

1. Abra a versão mais recente da sua jornada em tempo real e clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Você só pode criar uma nova versão com base na versão mais recente de uma jornada.

1. Faça suas modificações, clique em **[!UICONTROL Publish]** e confirme.

   ![](assets/journeyversions3.png)

A partir do momento em que a jornada é publicada, os indivíduos começarão a entrar na versão mais recente da jornada. As pessoas que já inseriram uma versão anterior permanecem nela até que concluam a jornada. Se posteriormente entrarem novamente na mesma jornada, eles entrarão na versão mais recente.

As versões de Jornada podem ser interrompidas individualmente. Todas as versões do jornada têm o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior encerra automaticamente e alterna para a **Fechado** status. Nenhuma entrada na jornada pode acontecer. Mesmo que você interrompa a versão mais recente, a versão anterior permanece fechada.
