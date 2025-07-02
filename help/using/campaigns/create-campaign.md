---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma campanha
description: Saiba como criar campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: criar, otimizador, campanha, superfície, mensagens
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 22%

---

# Criar uma campanha {#create-campaign}

Para criar uma nova campanha, navegue até o menu **[!UICONTROL Campanhas]** no painel esquerdo e clique em **[!UICONTROL Criar campanha]**. Você também pode duplicar uma campanha ao vivo existente para criar uma nova. [Saiba como](modify-stop-campaign.md#duplicate).

Antes de começar, leia os pré-requisitos da campanha nesta [página](get-started-with-campaigns.md#before-starting-campaign-prerequisites).

## Escolha o tipo de campanha {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campanha"
>abstract="**Campanhas programadas** são executadas imediatamente ou em uma data especificada e devem enviar mensagens de marketing. Campanhas **acionadas por API** são executadas usando uma chamada de API. O objetivo é enviar mensagens de marketing (mensagens promocionais que exigem o consentimento da pessoa) ou mensagens transacionais (mensagens não comerciais, que também podem ser enviadas a perfis não assinantes em contextos específicos)."

Ao criar uma nova campanha, primeiro selecione o tipo de campanha. Três tipos de campanhas estão disponíveis:

1. **[!UICONTROL Agendado - Marketing]** - Essas campanhas são executadas imediatamente ou em uma data especificada. As campanhas agendadas têm como objetivo enviar mensagens de **marketing** ou criar ações de entrada. Eles são configurados e executados na interface do usuário do.

1. **[!UICONTROL Acionado por API - Marketing]** - Essas campanhas são executadas usando uma chamada de API. Selecione esse tipo de campanha para enviar comunicações de marketing personalizadas para públicos-alvo direcionados.  [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)

1. **[!UICONTROL Acionado por API - Transacional]** - Igual ao acionado por API - Campanhas de marketing; essas campanhas são executadas usando uma chamada de API. As campanhas transacionais acionadas por API têm como objetivo enviar **mensagens transacionais**, ou seja, mensagens enviadas após uma ação executada por um indivíduo: solicitação de redefinição de senha, compra de carrinho etc.  [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

## Definir as propriedades da campanha {#create}

Depois que a campanha for criada, você deverá definir suas propriedades. Siga as etapas abaixo:

1. Na seção **[!UICONTROL Properties]**, digite o nome e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. (opcional) Use o campo **Tags** para atribuir Tags unificadas do Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com marcas](../start/search-filter-categorize.md#tags).

1. (opcional) Você pode limitar o acesso a esta campanha com base nos rótulos de acesso. Para adicionar uma limitação de acesso, navegue até o botão **[!UICONTROL Gerenciar acesso]** na parte superior desta página. Selecione apenas os rótulos para os quais você tem permissão. [Saiba mais sobre o Controle de Acesso em Nível de Objeto](../administration/object-based-access.md).

## Definir o público da campanha {#audience}

Agora você pode selecionar o público da sua campanha. Um público-alvo é um conjunto de pessoas que compartilham comportamentos e/ou características semelhantes.

>[!IMPORTANT]
>
>* O uso de públicos-alvo e atributos da [composição de público-alvo](../audience/get-started-audience-orchestration.md) não está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.
>
>* Para campanhas acionadas por API, o público-alvo deve ser definido por meio de uma chamada de API.

Para definir a população direcionada por uma campanha de marketing agendada, siga estas etapas:

1. Na seção **Público-alvo**, clique no botão **[!UICONTROL Selecionar público-alvo]** para exibir a lista de públicos-alvo do Adobe Experience Platform disponíveis. Saiba mais sobre públicos em [esta seção](../audience/about-audiences.md).

1. No campo **[!UICONTROL Tipo de identidade]**, escolha o tipo de chave a ser usado para identificar os indivíduos do público-alvo selecionado. Você pode usar um tipo de identidade existente ou criar um novo usando o Serviço de identidade da Adobe Experience Platform. Os namespaces de Identidade Padrão estão listados em [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Somente um tipo de identidade é permitido por campanha. Indivíduos pertencentes a um segmento que não tem o tipo de identidade selecionado entre suas diferentes identidades não podem ser alvos da campanha.

   ![](assets/create-campaign-namespace.png){width="80%"}

   Saiba mais sobre tipos de identidade e namespaces na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->


## Selecionar o canal {#channel}

Agora você pode selecionar o canal e sua configuração. Siga as etapas abaixo:

1. Na seção **[!UICONTROL Action]**, selecione o canal de comunicação.

   A lista de canais disponíveis depende do modelo de licenciamento e dos complementos. Para campanhas acionadas por API, somente os canais de Email, SMS e Notificação por push estão disponíveis.

1. Selecione a configuração do canal.

   Uma configuração foi definida por um [Administrador do Sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   Somente as configurações de canal compatíveis com o tipo de campanha de marketing são listadas na lista suspensa.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se estiver criando uma campanha de notificação por push, você poderá habilitar o **[!UICONTROL Modo de entrega rápida]**, que é um complemento do Journey Optimizer que permite o envio muito rápido de mensagens por push em grandes volumes. [Saiba mais](../push/create-push.md#rapid-delivery)

## Editar o conteúdo {#content}

Agora você pode definir o conteúdo da mensagem usando o botão **[!UICONTROL Editar conteúdo]**. O processo de criação de conteúdo depende do canal selecionado.

Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:


<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>Email</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Notificação por push</strong></a></div></td>
<td><a href="../direct-mail/create-direct-mail.md"><img alt="Correspondência direta" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/create-direct-mail.md"><strong>Correspondência direta</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/create-in-app.md"><img alt="No aplicativo" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/create-in-app.md"><strong>No aplicativo</strong></a></div></td>
<td><a href="../web/create-web.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/create-web.md"><strong>Web</strong></a></div></td>
<td><a href="../code-based/create-code-based.md"><img alt="Experiência baseada em código" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/create-code-based.md"><strong>Experiência baseada em código</strong></a></div></td>
<td><a href="../content-card/create-content-card.md"><img alt="Cartões de conteúdo" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/create-content-card.md"><strong>Cartões de conteúdo</strong></a></div></td>
</tr></table>

Depois que o conteúdo for definido, use o botão **[!UICONTROL Simular conteúdo]** para visualizar e testar o conteúdo com perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba mais](../content-management/preview-test.md). Para voltar para a tela de criação da campanha, clique na seta para a esquerda.

![](assets/create-campaign-design.png)

Além do conteúdo da mensagem propriamente dita, você pode definir as seguintes configurações:

1. (opcional) Na seção **[!UICONTROL Experimento de conteúdo]**, você pode usar o botão **[!UICONTROL Criar experimento]** para testar qual conteúdo funciona melhor. Os recursos de experimentação de conteúdo estão detalhados em [esta seção](../content-management/content-experiment.md).

1. Na seção **[!UICONTROL Rastreamento de ações]**, especifique se deseja acompanhar como seus destinatários reagem à sua entrega: é possível rastrear cliques e/ou aberturas.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report-cja.md)

## Agendar a campanha {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programação de campanha"
>abstract="Por padrão, as campanhas começam com uma ativação manual e terminam imediatamente após a mensagem ser enviada uma vez. Você tem a flexibilidade de definir a data e hora específicas para o envio da mensagem. Além disso, é possível especificar uma data final para campanhas recorrentes ou acionadas por API. Nos acionadores de ação, você também pode configurar a frequência de envio de mensagens de acordo com suas preferências."

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

Por padrão, as campanhas programadas começam assim que são ativadas manualmente e terminam assim que a mensagem é enviada uma vez.

Se você não quiser executar sua campanha logo após a ativação, poderá especificar uma data e hora em que a mensagem deverá ser enviada usando a opção **[!UICONTROL Início da campanha]**. A opção **[!UICONTROL Campaign end]** permite especificar quando uma campanha deve parar de ser executada.

![](assets/create-campaign-schedule.png)

Para campanhas de Email, SMS e Notificação por push, você pode definir uma frequência na qual a mensagem da campanha deve ser enviada. Para fazer isso, use as opções **[!UICONTROL Action triggers]** na tela de criação da campanha para especificar se a campanha deve ser executada diariamente, semanalmente ou mensalmente.

>[!NOTE]
>
>Ao agendar campanhas em [!DNL Adobe Journey Optimizer], verifique se a data/hora de início está alinhada com a primeira entrega desejada. Para campanhas recorrentes, se o horário agendado inicial já tiver passado, as campanhas serão transferidas para o próximo período disponível, de acordo com suas regras de recorrência.

## Outras configurações {#settings}

Algumas configurações são específicas do canal de comunicação selecionado para a campanha ou usadas para casos de uso específicos. Elas estão detalhadas abaixo.

* Para emails, você pode criar campanhas específicas de ativação do plano de aquecimento de IP. Saiba mais [nesta seção](../configuration/ip-warmup-campaign.md).
* Para canais da Web, no aplicativo e baseados em código, você pode atribuir uma pontuação de prioridade à sua campanha. Saiba mais [nesta seção](../conflict-prioritization/priority-scores.md).
* Para campanhas de cartão de conteúdo, você pode habilitar regras de entrega adicionais para escolher os eventos e critérios que acionam sua mensagem. Saiba mais [nesta seção](../content-card/create-content-card.md).
* Para mensagens no aplicativo, você pode usar o botão **[!UICONTROL Editar acionadores]** para escolher os eventos e critérios que acionam sua mensagem. Saiba mais [nesta seção](../in-app/create-in-app.md).

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá revisá-los e ativá-los. [Saiba mais](review-activate-campaign.md)
