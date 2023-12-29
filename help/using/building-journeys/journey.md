---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a jornadas
description: Introdução a jornadas
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: jornada, descobrir, introdução
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---


# Introdução a jornadas{#jo-general-principle}

Use o [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real, aproveitando dados contextuais armazenados em eventos ou fontes de dados.

Crie designs de cenários avançados com várias etapas e com os seguintes recursos:

* Envie uma **entrega unitária** em tempo real acionada quando um evento é recebido, ou **em lote** usando os públicos-alvo da Adobe Experience Platform.

* Aproveite **dados contextuais** de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

* Use as **ações incorporadas** para enviar mensagens projetadas no [!DNL Journey Optimizer] ou criar **ações personalizadas** se estiver usando um sistema de terceiros para enviar mensagens.

* Com o **Designer de jornadas**, crie seus casos de uso de várias etapas: arraste e solte facilmente um evento de entrada ou uma atividade de público-alvo de leitura, adicione condições e envie mensagens personalizadas.


>[!NOTE]
>
>Medidas de proteção e limitações da jornada estão detalhadas [nesta página](../start/guardrails.md)

## Etapas para criar uma jornada{#steps-journey}

Use o Adobe Journey Optimizer para projetar e orquestrar jornadas personalizadas a partir de uma única tela. As principais etapas para criar uma jornada são as seguintes:

![](assets/journey-creation-process.png)

O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite aos profissionais de marketing harmonizar o alcance do marketing com o engajamento individual com clientes. A interface permite arrastar e soltar facilmente as atividades da paleta na tela para criar a jornada.

![](assets/interface-journeys.png)

Saiba como iniciar e criar sua primeira jornada [nesta página](journey-gs.md).

O designer de jornada omnicanal ajuda a criar jornadas em várias etapas com públicos-alvo direcionados, atualizações com base em interações de clientes ou empresas em tempo real e mensagens omnicanal usando uma interface intuitiva de arrastar e soltar.

![](assets/journey38.png)

Saiba mais [nesta seção](using-the-journey-designer.md).

Como engenheiro de dados, as etapas para configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações são detalhadas [nesta seção](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Saiba como criar jornadas nos seguintes casos de uso de ponta a ponta.

Casos de uso comercial:

* [Enviar mensagens de vários canais](journeys-uc.md)
* [Enviar uma mensagem usando o Campaign v7/v8](ajo-ac.md)
* [Enviar uma mensagem aos assinantes](message-to-subscribers-uc.md)

Casos de uso técnico:

* [Envio dinâmico de coleções usando ações personalizadas](collections.md)
* [Incrementar entregas](ramp-up-deliveries-uc.md)
* [Limite a taxa de transferência com Fontes de dados externas e Ações personalizadas](limit-throughput.md)

## Versões de jornada{#journey-versions}

Na lista da jornada, todas as versões da jornada são exibidas com o número da versão. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Geralmente, um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo. Se a reentrada estiver habilitada, um perfil poderá ser inserido em uma jornada novamente, mas não poderá fazer isso até que tenha saído totalmente da instância anterior da jornada. [Leia mais](end-journey.md).

Se precisar modificar uma jornada ativa, crie uma nova versão da jornada.

1. Abra a versão mais recente da jornada ativa, clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Só é possível criar uma nova versão com base na versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

   ![](assets/journeyversions3.png)

A partir do momento em que a jornada for publicada, pessoas físicas começarão a acessar a versão mais recente da jornada. As pessoas que já acessaram uma versão anterior permanecerão nela até que concluam a jornada. Se mais tarde entrarem novamente na mesma jornada, elas acessarão a versão mais recente.

As versões da jornada podem ser interrompidas individualmente. Todas as versões das jornadas possuem o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior encerra automaticamente e alterna para o status **Fechado**. Nenhuma entrada na jornada pode acontecer. Mesmo que você interrompa a versão mais recente, a versão anterior permanecerá fechada.
