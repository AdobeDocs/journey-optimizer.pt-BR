---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas
description: Saiba mais sobre campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campanha, como, iniciar, otimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 70%

---

# Introdução às campanhas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programação de campanha"
>abstract="Por padrão, as campanhas começam com uma ativação manual e terminam imediatamente após a mensagem ser enviada uma vez. Você tem a flexibilidade de definir a data e hora específicas para o envio da mensagem. Além disso, é possível especificar uma data final para campanhas de ação recorrentes. Nos acionadores de ação, você também pode configurar a frequência de envio de mensagens de acordo com suas preferências."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Início da campanha"
>abstract="Especifique a data e a hora em que a mensagem deve ser enviada."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fim da campanha"
>abstract="Especifique quando uma campanha recorrente deve parar de ser executada."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Acionadores de ação da campanha"
>abstract="Defina uma frequência na qual a mensagem da campanha deve ser enviada."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Controle da taxa de limitação"
>abstract="Controle da taxa de limitação"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Criar campanhas"
>abstract="Use o **Adobe Journey Optimizer** para fornecer conteúdo único a um público-alvo usando vários canais. Ao usar jornadas, as ações são executadas em sequência. Com campanhas, as ações são executadas simultaneamente, imediatamente ou com base em um cronograma especificado."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campanhas"
>abstract="Crie campanhas para fornecer conteúdo uma única vez a um público-alvo específico em vários canais. Antes de criar a campanha, verifique se você tem uma configuração de canal e um público-alvo da Adobe Experience Platform prontos para uso."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campanha"
>abstract="**Campanhas programadas** são executadas imediatamente ou em uma data especificada e devem enviar mensagens de marketing. Campanhas **acionadas por API** são executadas usando uma chamada de API. O objetivo é enviar mensagens de marketing (mensagens promocionais que exigem o consentimento da pessoa) ou mensagens transacionais (mensagens não comerciais, que também podem ser enviadas a perfis não assinantes em contextos específicos)."

Use as campanhas do Journey Optimizer para fornecer conteúdo uma única vez a um público-alvo específico usando vários canais. Ao usar jornadas, as ações são executadas em sequência. Com campanhas, as ações são executadas simultaneamente, imediatamente ou com base em um cronograma especificado.

![](assets/gs-campaigns.png)

Você pode criar diferentes tipos de campanhas no Journey Optimizer:

* **Campanhas de ação**

  As campanhas de ação (ou campanhas programadas) permitem comunicações em lote ad hoc simples para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, anúncios, avisos legais ou atualizações de políticas.

* **Campanhas acionadas por API**

  As campanhas acionadas por API permitem que as comunicações de marketing alcancem um público-alvo na hora certa ou mensagens transacionais/operacionais para um indivíduo, como uma redefinição de senha, em que a necessidade pode envolver a personalização não apenas usando o atributo de perfil, mas também os dados de contexto em tempo real no acionador, que é uma carga de API REST.

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, Orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## Antes de começar {#campaign-prerequisites}

Verifique os seguintes pré-requisitos antes de começar a criar sua primeira campanha no [!DNL Journey Optimizer]:

1. **Você precisa de permissões adequadas**. As campanhas só estão disponíveis para usuários com acesso a um **[!UICONTROL Perfil de produto]** relacionado à campanha, como administrador da campanha, aprovador da campanha, gerente da campanha e/ou visualizador da campanha. Se não conseguir acessar campanhas, suas permissões deverão ser estendidas.

   +++Saiba como atribuir uma função relacionada à campanha

   1. Para atribuir uma função a um usuário em [!DNL Permissions] do produto, navegue até a guia **[!UICONTROL Funções]** e selecione uma das **[!UICONTROL funções]** integradas relacionadas à campanha: admin da campanha, aprovador da campanha, gerente de campanha ou visualizador da campanha.

   1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

   1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

      Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

   O usuário deve receber um email de redirecionamento para sua instância.

   +++

1. **Você precisa de um público-alvo**. Os públicos-alvo precisam estar disponíveis antes de criar a campanha. [Introdução aos públicos](../audience/about-audiences.md).

1. **Você precisa de uma configuração de canal**. Para selecionar um canal, é necessário ter a configuração de canal correspondente (ou seja, predefinição) criada e disponível. [Saiba como definir as configurações de canal](../configuration/channel-surfaces.md).

## Vamos nos aprofundar um pouco mais

Agora que você conhece as campanhas do [!DNL Journey Optimizer], é hora de se aprofundar nessas seções de documentação para começar a criar suas primeiras campanhas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="campanhas de ação" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">Campanhas de ação</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">Campanhas acionadas por API</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
