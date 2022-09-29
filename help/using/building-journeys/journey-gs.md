---
title: Introdução a jornadas
description: Etapas principais para criar sua primeira jornada com o Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 11%

---

# Introdução a jornadas{#jo-quick-start}

## Pré-requisitos{#start-prerequisites}

Para enviar mensagens com o jornada, as seguintes configurações são necessárias:

1. **Configurar um evento**: se quiser acionar as jornadas manualmente quando um evento for recebido, será necessário configurar um evento. Você define as informações esperadas e como processá-las. Esta etapa é executada por um **usuário técnico**. [Leia mais](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Criar um segmento**: sua jornada também pode acompanhar segmentos do Adobe Experience Platform para enviar mensagens em lote a um conjunto especificado de perfis. Para isso, é necessário criar segmentos. [Leia mais](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configurar a fonte de dados**: você pode definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Uma fonte de dados integrada da Adobe Experience Platform também é configurada no momento do provisionamento. Esta etapa não é necessária se você usar somente os dados dos eventos em sua jornada. Esta etapa é executada por um **usuário técnico**. [Leia mais](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar uma ação**: Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md). Esta etapa é executada por um **usuário técnico**. Se estiver usando os recursos de mensagem integrados do Journey Optimizer, basta adicionar uma ação de canal à jornada e projetar o conteúdo. Consulte [esta seção](../messages/get-started-content.md).

   ![](assets/custom2.png)

## Crie sua jornada{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Crie sua jornada"
>abstract="Esta tela exibe a lista de jornadas existentes. Abra uma jornada ou clique em &quot;Criar jornada&quot; e combine as diferentes atividades de evento, orquestração e ação para criar os cenários de vários canais em várias etapas."

Essa etapa é executada pela **usuário empresarial**. É aqui que você cria suas jornadas. Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

Estas são as principais etapas para enviar mensagens por meio do jornada:

1. Na seção do menu GERENCIAMENTO DE JORNADAS , clique em **[!UICONTROL Jornada]**. A lista de jornadas é exibida.

   ![](assets/interface-journeys.png)

1. Clique em **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite as propriedades da jornada no painel de configuração exibido no lado direito. Saiba mais nesta [seção](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Comece arrastando e soltando um evento ou um **Ler segmento** atividade da paleta na tela. Para saber mais sobre design de jornada, consulte [esta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arraste e solte as próximas etapas que o indivíduo seguirá. Por exemplo, é possível adicionar uma condição seguida de uma ação de canal. Para saber mais sobre atividades, consulte [esta seção](using-the-journey-designer.md).

1. Teste sua jornada usando perfis de teste. Saiba mais nesta [seção](testing-the-journey.md)

1. Publique sua jornada para ativá-la. Saiba mais nesta [seção](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitore sua jornada usando as ferramentas de relatório dedicadas para medir a eficácia da jornada. Saiba mais nesta [seção](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Defina as propriedades da jornada {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriedades da jornada"
>abstract="Esta seção mostra as propriedades da jornada. Por padrão, os parâmetros somente leitura ficam ocultos. As configurações disponíveis dependem do status da jornada, das permissões e da configuração do produto."

Clique no ícone de lápis, na parte superior direita para acessar as propriedades da jornada.

Você pode alterar o nome da jornada, adicionar uma descrição, permitir nova entrada, escolher datas de início e término e, como um usuário administrador, definir uma **[!UICONTROL Tempo limite e erro]** duração.

Para jornadas ao vivo, essa tela exibe a data da publicação e o nome do usuário que publicou a jornada.

O **Copiar detalhes técnicos** O permite copiar informações técnicas sobre a jornada que a equipe de suporte pode usar para a solução de problemas. As seguintes informações são copiadas: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrada{#entrance}

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção por jornadas de &quot;uma ocorrência&quot;, por exemplo, se quiser oferecer um presente único quando uma pessoa entrar em uma loja. Nesse caso, você não deseja que o cliente possa entrar novamente na jornada e receber a oferta novamente.

Quando uma jornada &quot;terminar&quot;, ela terá o status **[!UICONTROL Fechado]**. A jornada deixará de permitir que novos indivíduos entrem na jornada. Pessoas que já estão na jornada vão terminar a jornada normalmente.

Após o tempo limite global padrão de 30 dias, a jornada será alternada para a variável **Concluído** status. Veja isso [seção](../building-journeys/journey-gs.md#global_timeout).

>[!NOTE]
>
>As jornadas Unitárias (começando com um evento ou uma qualificação de segmento) incluem uma garantia que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

### Tempo limite e erro nas atividades do jornada {#timeout_and_error}

Ao editar uma ação ou atividade de condição, você pode definir um caminho alternativo em caso de erro ou tempo limite. Se o tratamento da atividade de interrogação de um sistema de terceiros exceder o tempo limite definido nas propriedades da jornada (**[!UICONTROL Tempo limite e erro]** ), o segundo caminho será escolhido para executar uma ação de fallback potencial.

Os valores autorizados estão entre 1 e 30 segundos.

Recomendamos que você defina uma **[!UICONTROL Tempo limite e erro]** se sua jornada for sensível ao tempo (por exemplo: reação ao local em tempo real de uma pessoa) porque não é possível atrasar a ação por mais de alguns segundos. Se sua jornada for menos sensível ao tempo, você poderá usar um valor mais longo para dar mais tempo ao sistema chamado para enviar uma resposta válida.

O Jornada também usa um tempo limite global. Consulte a [próxima seção](#global_timeout).

### Tempo limite da jornada global {#global_timeout}

Além do [timeout](#timeout_and_error) usada em atividades de jornada, também há um tempo limite de jornada global que não é exibido na interface e não pode ser alterado. Esse tempo limite interromperá o progresso dos indivíduos na jornada 30 dias após sua entrada. Isso significa que a jornada de um indivíduo não pode durar mais de 30 dias. Após o período de tempo limite de 30 dias, os dados do indivíduo são excluídos. Os indivíduos que ainda fluem na jornada no final do período limite serão interrompidos e serão considerados como erros no relatório.

>[!NOTE]
>
>As jornadas não reagem diretamente às solicitações de recusa, acesso ou exclusão de privacidade. No entanto, o tempo limite global garante que os indivíduos nunca permaneçam mais de 30 dias em qualquer jornada.

Devido ao tempo limite da jornada de 30 dias, quando a reentrada da jornada não é permitida, não podemos garantir que o bloqueio de reentrada funcione por mais de 30 dias. Na verdade, à medida que removemos todas as informações sobre pessoas que entraram na jornada 30 dias depois de terem entrado, não podemos conhecer a pessoa que entrou anteriormente, há mais de 30 dias.

### Fuso horário e fuso horário do perfil {#timezone}

O fuso horário é definido no nível da jornada.

Você pode inserir um fuso horário fixo ou usar perfis do Adobe Experience Platform para definir o fuso horário da jornada.

Se um fuso horário for definido no perfil do Adobe Experience Platform, ele poderá ser recuperado na jornada.

Para obter mais informações sobre o gerenciamento de fuso horário, consulte [esta página](../building-journeys/timezone-management.md).

### Gerenciar acesso {#access}

Para atribuir rótulos de uso de dados personalizados ou principais à jornada, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o Controle de acesso no nível do objeto (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
