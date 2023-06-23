---
solution: Journey Optimizer
product: journey optimizer
title: Criar a primeira jornada
description: Etapas principais para criar sua primeira jornada com o Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: jornada, primeiro, iniciar, início rápido, segmento, evento, ação
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 27%

---

# Criar a primeira jornada{#jo-quick-start}

## Pré-requisitos{#start-prerequisites}

Para enviar mensagens com jornadas, as seguintes configurações são necessárias:

1. **Configurar um evento**: se quiser acionar as jornadas de forma unitária quando um evento for recebido, será necessário configurar um evento. Você define as informações esperadas e como processá-las. Esta etapa é executada por um **usuário técnico**. [Leia mais](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Criar um segmento**: sua jornada também pode ouvir segmentos do Adobe Experience Platform para enviar mensagens em lote para um conjunto especificado de perfis. Para isso, você precisa criar segmentos. [Leia mais](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configurar a fonte de dados**: é possível definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Uma fonte de dados integrada da Adobe Experience Platform também é configurada no momento do provisionamento. Esta etapa não é necessária se você usar somente os dados dos eventos em sua jornada. Esta etapa é executada por um **usuário técnico**. [Leia mais](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar uma ação**: se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md). Esta etapa é executada por um **usuário técnico**. Se você estiver usando os recursos de mensagem incorporados do Journey Optimizer, basta adicionar uma ação de canal à jornada e projetar o conteúdo.

   ![](assets/custom2.png)

## Acessar jornadas {#journey-access}

Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**. Duas guias estarão disponíveis:

**Visão geral**: esta guia exibe um painel com as métricas principais relacionadas às suas jornadas:

* **Perfis processados**: número total de perfis processados nas últimas 24 horas
* **Jornada ao vivo**: número total de jornadas ativas com tráfego nas últimas 24 horas. As jornadas em tempo real incluem **Jornadas unitárias** (com base em eventos) e **Jornadas em lote** (ler segmento).
* **Taxa de erros**: taxa de todos os perfis com erro em comparação ao número total de perfis que entraram nas últimas 24 horas.
* **Taxa de descarte**: taxa de todos os perfis descartados em comparação ao número total de perfis que entraram nas últimas 24 horas. Um perfil descartado representa alguém que não está qualificado para entrar na jornada, por exemplo, devido a um namespace incorreto ou a regras de reentrada.

>[!NOTE]
>
>Esse painel considera as jornadas com tráfego nas últimas 24 horas. Somente as jornadas às quais você tem acesso são exibidas.

![](assets/journeys-dashboard.png)

**Procurar**: esta guia exibe a lista de jornadas existentes. Você pode pesquisar jornadas, usar filtros e executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item. Para obter mais informações, consulte [esta seção](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

Na lista de jornadas, você pode filtrar jornadas de acordo com o status, tipo e versão por meio do menu **[!UICONTROL Filtros de status e versão]**. O tipo pode ser: **[!UICONTROL Evento unitário]**, **[!UICONTROL Qualificação do segmento]**, **[!UICONTROL Ler segmento]** ou **[!UICONTROL Evento comercial]**.

Você pode optar por exibir somente jornadas que usam um evento, grupo de campos ou ação específica a partir dos **[!UICONTROL Filtros de atividade]** e **[!UICONTROL Filtros de dados]**. Além disso, a **[!UICONTROL Filtros de publicação]** permite selecionar uma data de publicação ou um usuário. Por exemplo, você pode optar por exibir somente as versões mais recentes de jornadas ao vivo que foram publicadas ontem. [Saiba mais](../building-journeys/using-the-journey-designer.md).

![](assets/filter-journeys.png)

Use as colunas **[!UICONTROL Última atualização]** e **[!UICONTROL Última atualização por]** para verificar quando aconteceu a última atualização de suas jornadas e quem as salvou.

Nos painéis de configuração Evento, Fonte de dados e Ação, o campo **[!UICONTROL Usado em]** exibe o número de jornadas que usam aquele determinado evento, grupo de campo ou ação. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas correspondentes.

![](assets/journey3bis.png)

## Criar sua jornada{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Criar sua jornada"
>abstract="Essa tela exibe a lista de jornadas existentes. Abra uma jornada ou clique em “Criar jornada” e combine as diferentes atividades de evento, orquestração e ação para criar os cenários de vários canais em várias etapas."

Esta etapa é executada pelo **usuário empresarial**. É aqui que você cria suas jornadas. Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

Estas são as etapas principais para enviar mensagens por meio do jornada:

1. No **Procurar** clique em **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite as propriedades da jornada no painel de configuração exibido no lado direito. Saiba mais nesta [seção](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Comece arrastando e soltando um evento ou uma **Segmento de leitura** atividade da paleta para a tela. Para saber mais sobre o design do jornada, consulte [nesta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arraste e solte as próximas etapas que o indivíduo seguirá. Por exemplo, é possível adicionar uma condição seguida por uma ação de canal. Para saber mais sobre atividades, consulte [nesta seção](using-the-journey-designer.md).

1. Teste a jornada usando perfis de teste. Saiba mais nesta [seção](testing-the-journey.md)

1. Publique sua jornada para ativá-la. Saiba mais nesta [seção](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitore sua jornada usando as ferramentas de relatório dedicadas para medir a eficiência da sua jornada. Saiba mais nesta [seção](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definir as propriedades da jornada {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriedades da jornada"
>abstract="Essa seção mostra as propriedades da jornada. Por padrão, os parâmetros somente leitura ficam ocultos. As configurações disponíveis dependem do status da jornada, das permissões e da configuração do produto."

Clique no ícone de lápis, na parte superior direita, para acessar as propriedades da jornada.

É possível alterar o nome da jornada, adicionar uma descrição, permitir a reentrada, escolher datas de início e término e, como usuário administrador, definir um **[!UICONTROL Tempo limite e erro]** duração. Você também pode atribuir Tags unificadas do Adobe Experience Platform à sua jornada. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

Para jornadas ao vivo, essa tela exibe a data da publicação e o nome do usuário que publicou a jornada.

A variável **Copiar detalhes técnicos** O permite copiar informações técnicas sobre a jornada que a equipe de suporte pode usar para a solução de problemas. As seguintes informações são copiadas: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrada{#entrance}

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção **Permitir reentrada** opção para jornadas &quot;one shot&quot;, por exemplo, se você quiser oferecer um presente único quando uma pessoa entrar em uma loja.

Quando a variável **Permitir reentrada** estiver ativada, a variável **Período de espera de reentrada** é exibido. Este campo possibilita definir o tempo de espera antes de permitir que um perfil entre novamente em jornadas unitárias (que começam com um evento ou uma qualificação de segmento). Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos.

Saiba mais sobre o gerenciamento de entrada de perfis, em [nesta seção](entry-management.md).

### Gerenciar acesso {#access}

Para atribuir rótulos de uso de dados personalizados ou principais à jornada, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o OLA (Object Level Access Control, controle de acesso em nível de objeto)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Fuso horário e fuso horário do perfil {#timezone}

O fuso horário é definido no nível da jornada.

Você pode inserir um fuso horário fixo ou usar perfis do Adobe Experience Platform para definir o fuso horário de jornada.

Se um fuso horário for definido no perfil do Adobe Experience Platform, ele poderá ser recuperado na jornada.

Para obter mais informações sobre o gerenciamento de fuso horário, consulte [esta página](../building-journeys/timezone-management.md).

### Datas de início e término {#dates}

Você pode definir um **Data inicial**. Se não tiver especificado um, ele será definido automaticamente no momento da publicação.

Você também pode adicionar um **Data final**. Isso permite que os perfis saiam automaticamente quando a data for atingida. Se você não especificar uma data de término, os perfis poderão permanecer até o tempo limite padrão da jornada (geralmente 30 dias, 7 dias com a oferta complementar Healthcare Shield). A única exceção são as jornadas recorrentes de segmentos de leitura com **Forçar reentrada na recorrência** ativadas, que terminam na data de início da próxima ocorrência.

### Tempo limite e erro em atividades de jornada {#timeout_and_error}

Ao editar uma atividade de ação ou condição, você tem a opção de especificar um caminho alternativo no caso de um erro ou tempo limite. Se o processamento da atividade, que envolve a consulta de um sistema de terceiros, exceder a duração especificada nas propriedades da jornada para tempo limite e tratamento de erros (**[!UICONTROL Tempo limite e erro]** ), o segundo caminho será selecionado para executar uma ação de fallback, se necessário.

Os valores autorizados estão entre 1 e 30 segundos.

Recomendamos que você defina um período muito curto **[!UICONTROL Tempo limite e erro]** valor se a jornada for sensível ao tempo (por exemplo: reagir ao local em tempo real de uma pessoa) porque você não pode atrasar a ação por mais de alguns segundos. Se a jornada for menos sensível ao tempo, você poderá usar um valor mais longo para dar mais tempo ao sistema chamado para enviar uma resposta válida.

O Jornada também usa um tempo limite global. Consulte a [próxima seção](#global_timeout).

### Tempo limite de jornada global {#global_timeout}

Além do [timeout](#timeout_and_error) usado em atividades de jornada, também há um tempo limite de jornada global que não é exibido na interface e não pode ser alterado. Esse tempo limite interromperá o progresso das pessoas físicas na jornada 30 dias após a sua entrada. Isso significa que a jornada de um indivíduo não pode durar mais de 30 dias. Após o período de tempo limite de 30 dias, os dados do indivíduo são excluídos. As pessoas que ainda fluem na jornada no final do período de tempo limite serão interrompidas e serão consideradas como erros no relatório.

>[!NOTE]
>
>As jornadas não reagem diretamente a solicitações de recusa de privacidade, acesso ou exclusão. No entanto, o tempo limite global garante que os indivíduos nunca fiquem mais de 30 dias em qualquer jornada.

Devido ao tempo limite de jornada de 30 dias, quando a reentrada da jornada não é permitida, não podemos garantir que o bloqueio de reentrada funcionará por mais de 30 dias. Na verdade, à medida que removemos todas as informações sobre as pessoas que entraram na jornada 30 dias depois de entrarem, não podemos saber a pessoa inserida anteriormente, há mais de 30 dias.

