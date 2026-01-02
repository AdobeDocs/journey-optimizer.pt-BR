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
source-git-commit: edf8ad3cf95cc2a8dcaf3e1abd0203785eda8fb5
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 31%

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
>abstract="Selecione o tipo de campanha. Os canais disponíveis variam de acordo com o tipo selecionado. <br>**Campanhas agendadas** (campanhas de ação): ideais para comunicações em lote simples e únicas que você pode agendar para execução em um horário específico.<br>**Campanhas acionadas por API**: ativadas por meio de uma chamada de API, permitindo o envio automatizado de mensagens baseadas em eventos diretamente de sistemas externos.<br>**Campanhas orquestradas**: fornece uma tela visual com interface de arrastar e soltar para projetar e automatizar fluxos de trabalho de marketing complexos e com várias etapas, desde a segmentação de público-alvo até a entrega personalizada de mensagens entre canais."

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

O Adobe Journey Optimizer permite que você forneça conteúdo direcionado e único para públicos-alvo específicos em vários canais. Com campanhas, você pode executar ações de marketing coordenadas simultaneamente, atingindo seu público-alvo com a mensagem certa na hora certa.

Este guia fornece um roteiro claro para ajudá-lo a entender os fundamentos da campanha, escolher o tipo de campanha certo para o seu caso de uso e criar campanhas com confiança que forneçam experiências de cliente impactantes.

## O que são campanhas?

**Campanhas** são ações de marketing coordenadas que fornecem conteúdo a um público específico através de um ou mais canais. Diferentemente das jornadas em que as ações são executadas sequencialmente, as campanhas executam ações simultaneamente — imediatamente ou de acordo com um cronograma definido.

Use [!DNL Journey Optimizer] para:

* Entregar **conteúdo único ou recorrente** aos segmentos de público-alvo direcionados
* Execute **comunicações coordenadas multicanais** por email, push, SMS, no aplicativo, Web e muito mais
* Acionar **respostas automatizadas** por meio de chamadas de API para mensagens em tempo real orientadas por eventos
* Crie **fluxos de trabalho de marketing complexos** com ferramentas de orquestração visual

![](assets/gs-campaigns.png)

➡️ **Pronto para começar a criar?** [Crie sua primeira campanha](create-campaign.md) em minutos.

## Escolha seu tipo de campanha {#campaign-types}

**Antes de começar a criar**, é importante entender qual tipo de campanha se adequa ao seu caso de uso. O Adobe Journey Optimizer oferece suporte a três tipos de campanha, cada uma projetada para cenários e mecanismos de ativação diferentes:

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campanhas de ação (Agendadas)]

**Quando usar:** comunicações em lotes simples e agendadas

**Campanhas de ação** (também conhecidas como campanhas agendadas) são ideais para comunicações em lote diretas, únicas ou recorrentes executadas em um momento específico.

**Duas categorias:**

* **Marketing** - Ofertas promocionais, campanhas de participação, anúncios, avisos legais ou atualizações de políticas. Exige a aceitação dos destinatários.
* **Transacional** - Interrupções, emergências, cancelamentos. Não requer aceitação.

**Perfeito para:** boletins informativos mensais para segmentos de clientes, anúncios promocionais sensíveis ao tempo, campanhas de marketing sazonais, comunicações de lançamento de produtos e notificações de interrupção de serviços.

➡️ [Saiba mais sobre as campanhas de ação](create-campaign.md)

>[!TAB Campanhas acionadas por API]

**Quando usar:** Mensagens orientadas por eventos em tempo real com sistemas externos

As **campanhas acionadas por API** são ativadas por meio de chamadas de API, permitindo o envio automatizado de mensagens diretamente de sistemas externos. Essas campanhas oferecem suporte à personalização usando atributos de perfil e dados de contexto em tempo real da carga da API.

**Duas categorias:**

* **Marketing** - Comunicações de marketing personalizadas para públicos-alvo direcionados
* **Transacional** - Mensagens após ações individuais (redefinições de senha, compras de carrinho etc.)

**Perfeito para:** confirmações de redefinição de senha, recuperação de abandono de carrinho, confirmações de pedidos e atualizações de envio, notificações de atividades de conta e recomendações personalizadas em tempo real.

➡️ [Saiba mais sobre campanhas acionadas por API](api-triggered-campaigns.md)

>[!TAB Campanhas orquestradas]

**Quando usar:** fluxos de trabalho de marketing complexos, de várias etapas

**As campanhas orquestradas** oferecem uma tela visual de arrastar e soltar para projetar e automatizar fluxos de trabalho de marketing sofisticados. Desde a segmentação de público até a entrega de mensagens personalizadas em canais, tudo acontece em um ambiente intuitivo criado para oferecer velocidade e controle.

**Perfeito para:** programas de engajamento do cliente em várias etapas, estratégias complexas de segmentação e direcionamento, orquestração de campanhas entre canais, marketing iniciado pela marca em escala e automação avançada de fluxo de trabalho com vários pontos de decisão.

➡️ [Saiba mais sobre campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>Não tem certeza de qual tipo escolher? Comece com **Campanhas de ação** para comunicações em lote agendadas ou **campanhas acionadas por API** para mensagens em tempo real; essas campanhas abordam os casos de uso mais comuns.

## Seu fluxo de trabalho de criação de campanha {#workflow}

A criação de campanhas bem-sucedidas segue um processo claro e repetível. Este é o seu fluxo de trabalho passo a passo:

**1. Plano** → **2. Configurar** → **3. Design** → **4. Revisão** → **5. Ativar** → **6. Monitorar**

### &#x200B;1. Planeje sua campanha {#plan}

Antes de começar, esclareça seus objetivos:

* **Qual é a meta?** (por exemplo, gerar conversões, aumentar o engajamento, notificar os clientes)
* **Quem é o público-alvo?** (por exemplo, compilar ou selecionar do Adobe Experience Platform)
* **Que tipo de campanha se encaixa?** (Consulte [tipos de campanha](#campaign-types) acima)
* **Quais canais você usará?** (email, push, SMS, no aplicativo, Web etc.) → [Veja os canais compatíveis por tipo de campanha](../channels/gs-channels.md#channels)
* **Quando ele deve ser executado?** (imediato, agendado ou acionado por API)

### &#x200B;2. Configurar as propriedades da campanha {#configure}

Configure a base da sua campanha:

1. **Nomeie e descreva** sua campanha para facilitar a identificação
2. **Selecionar tipo de campanha** (Ação, acionada por API ou Orquestrada)
3. **Escolha seu público-alvo**
4. **Definir prioridade** se estiver usando o gerenciamento de conflitos
5. **Configurar agendamento** (para campanhas de Ação) ou detalhes da API (para acionado por API)

**Guias específicos de tipo:** [Propriedades da campanha de ação](campaign-properties.md) | [Propriedades de campanha acionadas por API](api-triggered-campaign-properties.md) | [Configuração de campanha orquestrada](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;3. Projetar o conteúdo {#design}

Crie mensagens atraentes para seu público-alvo:

* Use o **Designer de email** para experiências de email avançadas
* Configurar **notificações por push** com imagens e deep links
* Criar **mensagens SMS/MMS** com personalização
* Criar experiências **no aplicativo** e **na Web**
* Adicionar **personalização** usando atributos de perfil e dados contextuais

**Guias específicos de tipo:** [Conteúdo da campanha de ação](campaign-content.md) | [Conteúdo de campanha acionado por API](api-triggered-campaign-content.md) | [Conteúdo de campanha orquestrada](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;4. Revisar e testar {#review}

Sempre revise sua campanha antes da ativação:

* **Visualizar conteúdo** com perfis de teste
* **Verifique o direcionamento** para garantir o público-alvo correto
* **Verificar agendamento** e configurações de ativação
* **Solicitar aprovação** se estiver usando o fluxo de trabalho de aprovação
* **Testar a capacidade de entrega** com listas de propagação

**Guias específicos de tipo:** [Campanhas de ação de revisão](review-activate-campaign.md) | [Revisar campanhas acionadas por API](review-activate-api-triggered-campaign.md) | [Revisar campanhas orquestradas](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;5. Ativar a campanha {#activate}

Quando a revisão for concluída, ative sua campanha:

* **Ativação manual** - Ativar imediatamente ou no horário agendado
* **Ativação de API** - Para campanhas acionadas por API, use o ponto de extremidade de ativação
* **Processo de aprovação** - Se necessário, aguarde a aprovação da parte interessada
* Observação: campanhas ativas não podem ser editadas (você deve duplicar para fazer alterações)

**Guias específicos de tipo:** [Ativar campanhas de ação](review-activate-campaign.md) | [Ativar campanhas acionadas por API](review-activate-api-triggered-campaign.md) | [Ativar campanhas orquestradas](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;6. Monitorar e analisar {#monitor}

Rastreie o desempenho da sua campanha:

* Exibir relatórios e análises de campanha
* Monitorar taxas de entrega e métricas de envolvimento
* Rastrear erros e rejeições
* Analisar conversão e ROI
* Usar insights para otimização

**Guias específicos de tipo:** [Relatórios de campanha de ação](../reports/campaign-global-report-cja.md) | [Monitoramento de campanha acionado por API](api-triggered-campaigns.md#monitor) | [Análise de campanha orquestrada](../orchestrated/create-orchestrated-campaign.md)

➡️ **Pronto para começar?** Escolha seu tipo de campanha:
* [Criar campanha de ação →](create-campaign.md)
* [Criar campanha acionada por API →](api-triggered-campaigns.md)
* [Criar campanha orquestrada →](../orchestrated/gs-orchestrated-campaigns.md)

## Pré-requisitos {#prerequisites}

Antes de trabalhar com campanhas, verifique se você tem o seguinte em vigor:

### Configuração necessária

* **Públicos-alvo** - Os públicos-alvo devem estar disponíveis no Adobe Experience Platform antes da criação de campanhas. [Introdução a públicos →](../audience/about-audiences.md)

* **Configurações de canal** - As configurações de canal (predefinições) devem ser criadas e estar disponíveis para os canais que você deseja usar. [Definir configurações de canal →](../configuration/channel-surfaces.md)

* **Permissões** - Você precisa das permissões apropriadas com base no tipo de campanha. Entre em contato com o administrador se não conseguir acessar as funcionalidades da campanha. [Saiba mais sobre funções integradas →](../administration/ootb-product-profiles.md)

| Tipo de campanha | Permissões |
|----------------------------|----------------------------------------------------------------------------|
| **Campanhas de ação** | Admin da campanha<br>Aprovador da campanha<br>Gerente da campanha<br>Visualizador da campanha |
| **Campanhas acionadas por API** | Admin da campanha<br>Aprovador da campanha<br>Gerente da campanha<br>Visualizador da campanha |
| **Campanhas orquestradas** | Admin de campanha orquestrada<br>Aprovador de campanha orquestrada<br>Gerente de campanha orquestrada<br>Visualizador de campanha orquestrada |

+++Atribuir permissões de campanha

1. Navegue até a guia **[!UICONTROL Funções]** no produto [!DNL Permissions] e selecione uma das **[!UICONTROL Funções]** relacionadas à campanha interna.

1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

   Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users){target="_blank"}.

O usuário deve receber um email de redirecionamento para sua instância.

+++

## Recursos do Campaign {#capabilities}

À medida que você se familiariza com as campanhas, explore esses recursos avançados:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Agendamento e sincronização**

Programe campanhas para datas/horas específicas, defina entregas recorrentes e otimize os tempos de envio para obter o impacto máximo.

[Saiba mais sobre agendamento](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Controle de taxa**

Limite a taxa de transferência de mensagens para evitar sobrecarga em sistemas downstream, como páginas de aterrissagem ou plataformas de atendimento ao cliente.

[Limites da taxa de controlo](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Direcionamento de público-alvo**

Direcione públicos-alvo específicos da Adobe Experience Platform com precisão e gerencie qualificações de público-alvo dinamicamente.

[Selecionar público da campanha](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Fluxos de trabalho de aprovação**

Implemente processos de revisão e aprovação antes que as campanhas entrem em vigor, garantindo qualidade e conformidade.

[Revisar e ativar](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Período de silêncio**

Respeite as preferências do cliente evitando a entrega de mensagens durante as janelas de tempo especificadas.

[Configurar horas de silêncio](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Otimização de hora de envio**

Use a IA para determinar o melhor momento para enviar mensagens para obter o máximo de engajamento com cada indivíduo.

[Otimizar o tempo de envio](campaigns-message-optimization.md)
:::

::::

## Introdução aos tipos de campanha {#get-started-types}

Agora que você entende as campanhas no [!DNL Journey Optimizer], escolha o seu tipo de campanha para começar:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campanhas de ação" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campanhas de ação</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campanhas acionadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campanhas orquestradas</a></td>
</tr></table>
