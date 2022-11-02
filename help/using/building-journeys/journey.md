---
solution: Journey Optimizer
product: journey optimizer
title: Princípio geral
description: Princípio geral
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 19%

---


# Princípio geral{#jo-general-principle}

Use [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real aproveitando dados contextuais armazenados em eventos ou fontes de dados.

Crie designs de cenários avançados com várias etapas e com os seguintes recursos:

* Envie **entrega unitária** em tempo real acionada quando um evento é recebido, ou **em lote** usando segmentos da Adobe Experience Platform.

* Aproveite **dados contextuais** de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

* Use o **ações integradas** para enviar mensagens projetadas no [!DNL Journey Optimizer] ou criar **ações personalizadas** se estiver usando um sistema de terceiros para enviar mensagens.

* Com o **Designer de jornadas**, crie seus casos de uso em várias etapas: arraste e solte facilmente um evento de entrada ou uma atividade de segmento de leitura, adicione condições e envie mensagens personalizadas.

## Etapas para criar uma jornada{#steps-journey}

O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite que os profissionais de marketing harmonizem o alcance de marketing com o envolvimento de um para um cliente. A interface do usuário permite arrastar e soltar facilmente as atividades da paleta na tela para criar a jornada. Observe que também é possível clicar duas vezes em uma atividade para adicioná-la à tela, na próxima etapa disponível.

Saiba como iniciar e criar sua primeira jornada em [esta página](journey-gs.md).

Saiba como usar o designer do jornada e combinar atividades para orquestrar jornadas omnicanais poderosas no [esta seção](using-the-journey-designer.md).

Como engenheiro de dados, saiba como configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações em [esta seção](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Descubra os seguintes casos de uso completos para alavancar
* Casos de uso de negócios
   * [Enviar mensagens de vários canais](journeys-uc.md)
   * [Enviar uma mensagem usando o Campaign v7/v8](campaign-classic-use-case.md)
   * [Enviar uma mensagem aos assinantes](message-to-subscribers-uc.md)

* Casos de uso técnico
   * [Envio dinâmico de coleções usando ações personalizadas](collections.md)
   * [Incrementar entregas](ramp-up-deliveries-uc.md)
   * [Limite a taxa de transferência com fontes de dados externas e ações personalizadas](limit-throughput.md)

## Versões de jornada{#journey-versions}

Na lista jornada, todas as versões do jornada são exibidas com o número da versão. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Quando você pesquisa por uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida no topo da interface da edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Na maioria dos casos, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá inserir uma jornada novamente, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada. [Leia mais](end-journey.md).

Se precisar modificar para uma jornada ao vivo, crie uma nova versão da jornada.

1. Abra a versão mais recente da jornada dinâmica e clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Você só pode criar uma nova versão a partir da versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

   ![](assets/journeyversions3.png)

A partir do momento em que a jornada for publicada, os indivíduos começarão a fluir para a versão mais recente da jornada. As pessoas que já entraram em uma versão anterior ficam nela até terminarem a jornada. Se, posteriormente, eles digitarem novamente a mesma jornada, acessarão a versão mais recente.

As versões do Jornada podem ser interrompidas individualmente. Todas as versões do jornada têm o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior automaticamente termina e alterna para a **Fechado** status. Nenhuma entrada na jornada pode acontecer. Mesmo que você pare a versão mais recente, a versão anterior permanecerá fechada.

>[!NOTE]
>
>Saiba mais sobre as medidas de proteção e limitações das versões do jornada, em [esta página](../start/guardrails.md#journey-versions-limitations)