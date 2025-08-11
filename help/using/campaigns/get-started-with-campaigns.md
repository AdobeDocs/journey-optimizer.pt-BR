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
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '708'
ht-degree: 100%

---

# Introdução às campanhas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programação de campanha"
>abstract="Por padrão, as campanhas começam com uma ativação manual e terminam imediatamente após a mensagem ser enviada uma vez. Você tem a flexibilidade de definir a data e hora específicas para o envio da mensagem. Além disso, é possível especificar uma data final para campanhas com ações recorrentes. Nos acionadores de ação, você também pode configurar a frequência de envio de mensagens de acordo com suas preferências."

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

É possível criar diferentes tipos de campanhas no Journey Optimizer:

* **Campanhas de ação**

  As campanhas de ação (ou campanhas programadas) permitem criar comunicações ad-hoc simples em lote para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, comunicados, avisos legais ou atualizações de políticas.

* **Campanhas acionadas por API**

  Campanhas acionadas por API permitem que as comunicações de marketing alcancem um público-alvo na hora certa ou que mensagens transacionais/operacionais cheguem a uma pessoa, como uma redefinição de senha, em que a necessidade pode envolver personalização, não apenas usando o atributo de perfil, mas também os dados de contexto em tempo real no acionador, que é um conteúdo da API REST.

* **Campanhas orquestradas**

  A orquestração de campanhas no Adobe Journey Optimizer permite a criação de campanhas de marketing sofisticadas e iniciadas pela marca em todos os canais, ajudando a impulsionar o engajamento, a receita e a fidelidade do cliente em grande escala.

  Embora o marketing entre canais seja essencial, as campanhas orquestradas permitem que ele flua melhor. Com uma interface visual do tipo arrastar e soltar, você pode projetar e automatizar fluxos de trabalho de marketing complexos, desde a segmentação até a entrega de mensagens, em vários canais. Tudo acontece em um ambiente intuitivo, criado para proporcionar velocidade, controle e eficiência.

## Pré-requisitos {#prerequisites}

Antes de criar a sua campanha, verifique os pré-requisitos abaixo.

### Permissões

As campanhas só estão disponíveis para usuários com as permissões apropriadas listadas abaixo. [Saiba mais sobre as funções integradas do Journey Optimizer](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB Campanhas de ação]

Administrador da campanha
Aprovador da campanha
Gerente de campanha
Visualizador da campanha

>[!TAB Campanhas acionadas por API]

Administrador da campanha
Aprovador da campanha
Gerente de campanha
Visualizador da campanha

>[!TAB Campanhas orquestradas]

Administrador de campanhas orquestradas
Aprovador de campanhas orquestradas
Gerenciador de campanhas orquestradas
Visualizador de campanhas orquestradas

>[!ENDTABS]

Se não conseguir acessar as funcionalidades da campanha, entre em contato com o administrador para solicitar as permissões necessárias.

+++Saiba como atribuir uma função relacionada à campanha

1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e selecione uma das **[!UICONTROL Funções]** integradas relacionadas à campanha detalhadas acima.

1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

   Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

O usuário deve receber um email de redirecionamento para sua instância.

+++

### Público-alvo

Os públicos-alvo precisam estar disponíveis antes de criar a campanha. [Introdução aos públicos-alvo](../audience/about-audiences.md).

### Configuração de canais

Para selecionar um canal, é necessário ter a configuração de canal correspondente (ou seja, predefinição) criada e disponível. [Saiba como definir as configurações de canal](../configuration/channel-surfaces.md).

## Vamos nos aprofundar um pouco mais

Agora que você conhece as campanhas do [!DNL Journey Optimizer], é hora de se aprofundar nessas seções da documentação para começar a criar suas primeiras campanhas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campanhas de ação" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campanhas de ação</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campanhas acionadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campanhas orquestradas</a></td>
</tr></table>
