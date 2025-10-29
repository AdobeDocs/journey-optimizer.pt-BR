---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas
description: Saiba mais sobre campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campanha, como, iniciar, otimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: afac93abcd2bacc4371748b94c0e66942a4c5076
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 89%

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
>title="Controle de taxa"
>abstract="Defina o controle de taxa da campanha, especificando os limites de taxa desejados. Esse recurso é particularmente útil para evitar sobrecarga em sistemas downstream, como páginas de destino ou plataformas de atendimento ao cliente."

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
>abstract="Selecione o tipo de campanha. Os canais disponíveis variam de acordo com o tipo selecionado. <br>**Campanhas agendadas** (campanhas de ação): ideais para comunicações em lote simples e únicas que você pode agendar para execução em um horário específico.<br>**Campanhas acionadas por API** - Ativadas por meio de uma chamada de API, permitindo o envio automatizado de mensagens baseadas em eventos diretamente de sistemas externos.<br>**Campanhas orquestradas**: fornece uma tela visual com interface de arrastar e soltar para projetar e automatizar fluxos de trabalho de marketing complexos e com várias etapas, desde a segmentação de público-alvo até a entrega personalizada de mensagens entre canais."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campanhas"
>abstract="Crie um fluxo de segmentação, crie mensagens entre canais e planeje as campanhas. Canais compatíveis: email, SMS, notificação por push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campanhas"
>abstract="Envie entregas de saída individuais ou recorrentes, ou ações de entrada contínuas."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campanhas"
>abstract="Entregue ações transacionais de saída únicas ou recorrentes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campanhas"
>abstract="Envie comunicações de marketing personalizadas aos seus públicos-alvo. Canais compatíveis: email, SMS, notificações por push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campanhas"
>abstract="Envie comunicações transacionais a perfis individuais ou conjuntos de perfis. Canais compatíveis: email, SMS, notificações por push."

Use campanhas do [!DNL Journey Optimizer] para fornecer conteúdo único a um público-alvo específico em vários canais. Ao contrário das jornadas, que executam ações passo a passo, as campanhas realizam ações simultaneamente: imediatamente ou em um cronograma definido.

![](assets/gs-campaigns.png)

## Tipos de campanha

O [!DNL Journey Optimizer] é compatível com três tipos de campanha. Cada tipo se encaixa em diferentes casos de uso e oferece suporte a diferentes canais. Para obter mais informações sobre os canais disponíveis com cada tipo de campanha, consulte a tabela nesta seção: [Canais em jornadas e campanhas](../channels/gs-channels.md#channels)

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campanhas orquestradas]

As **campanhas orquestradas** viabilizam campanhas de marketing sofisticadas e iniciadas pela marca em vários canais, ajudando a impulsionar o engajamento, a receita e a fidelidade do cliente em grande escala.

Embora o marketing entre canais seja essencial, as campanhas orquestradas permitem que ele flua melhor. Com uma interface visual do tipo arrastar e soltar, você pode projetar e automatizar fluxos de trabalho de marketing complexos, desde a segmentação até a entrega de mensagens, em vários canais. Tudo acontece em um ambiente intuitivo, criado para proporcionar velocidade, controle e eficiência.

➡️ [Saiba como trabalhar com campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Campanhas de ação (ou campanhas agendadas)]

**Campanhas de ação**, também conhecidas como campanhas agendadas, permitem comunicações ad hoc em lote simples.

* **Agendado - Marketing** - Para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, anúncios, avisos legais ou atualizações de políticas. Exige a aceitação dos destinatários.
* **Agendado - Transacional** - Ao contrário das campanhas de marketing, as campanhas transacionais não exigem a aceitação dos destinatários. Use esta categoria para comunicações relacionadas a interrupções, emergências e cancelamentos. Canais compatíveis: email, SMS, notificação por push.

➡️ [Saiba como trabalhar com campanhas de ação](create-campaign.md)

>[!TAB Campanhas acionadas por API]

**Campanhas acionadas por API** permitem acionar a execução da campanha usando uma chamada de API. Essas comunicações podem ser enviadas onde a necessidade pode envolver personalização, não apenas usando atributos de perfil como redefinição de senha, mas também dados de contexto em tempo real no acionador, que é uma carga da API REST.

* **Acionada por API - Marketing** - Enviar comunicações de marketing personalizadas para públicos-alvo direcionados.
* **Acionada por API - Transacional** - Enviar mensagens seguindo uma ação realizada por uma pessoa física, como uma solicitação de redefinição de senha, compra de carrinho, etc.

➡️ [Saiba como trabalhar com campanhas acionadas por API](api-triggered-campaigns.md)


>[!ENDTABS]

## Pré-requisitos {#prerequisites}

Antes de trabalhar com campanhas, certifique-se de analisar os pré-requisitos abaixo.

* **Públicos-alvo** Os públicos-alvo precisam estar disponíveis antes de criar a campanha. [Introdução aos públicos-alvo](../audience/about-audiences.md).

* **Configurações de canal** - Para selecionar um canal, é necessário ter a configuração de canal correspondente (ou seja, predefinição) criada e disponível. [Saiba como definir as configurações de canal](../configuration/channel-surfaces.md).

* **Permissões** - As campanhas estão disponíveis apenas aos usuários com as permissões apropriadas listadas abaixo. Se não conseguir acessar as funcionalidades da campanha, entre em contato com o(a) admin para solicitar as permissões necessárias. [Saiba mais sobre as funções integradas do Journey Optimizer](../administration/ootb-product-profiles.md)

  | Tipo de campanha | Permissões |
  |----------------------------|----------------------------------------------------------------------------|
  | **Campanhas de ação** | Admin da campanha<br>Aprovador da campanha<br>Gerente da campanha<br>Visualizador da campanha |
  | **Campanhas acionadas por API** | Admin da campanha<br>Aprovador da campanha<br>Gerente da campanha<br>Visualizador da campanha |
  | **Campanhas orquestradas** | Admin de campanha orquestrada<br>Aprovador de campanha orquestrada<br>Gerente de campanha orquestrada<br>Visualizador de campanha orquestrada |

  +++Saiba como atribuir uma função relacionada à campanha

   1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e selecione uma das **[!UICONTROL Funções]** integradas relacionadas à campanha detalhadas acima.

   1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

   1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

      Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

  O usuário deve receber um email de redirecionamento para sua instância.

  +++

## Vamos nos aprofundar um pouco mais

Agora que você conhece as campanhas do [!DNL Journey Optimizer], é hora de se aprofundar nessas seções da documentação para começar a criar suas primeiras campanhas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campanhas de ação" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campanhas de ação</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campanhas acionadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campanhas orquestradas</a></td>
</tr></table>
