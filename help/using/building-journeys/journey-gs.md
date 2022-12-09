---
solution: Journey Optimizer
product: journey optimizer
title: Criar sua primeira jornada
description: Etapas principais para criar sua primeira jornada com o Adobe Journey Otimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 978751263ba2ed21e35e41e767f1e31ddbe59d53
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# Criar sua primeira jornada{#jo-quick-start}

## Pré-requisitos{#start-prerequisites}

Para enviar mensagens com jornadas, as seguintes configurações são necessárias:

1. **Configurar um evento**: se quiser acionar suas jornadas de forma unitária quando um evento for recebido, será necessário configurar um evento. Você define as informações esperadas e como processá-las. Esta etapa é executada por uma **usuário técnico**. [Leia mais](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Criar um segmento**: sua jornada também pode acompanhar os segmentos da Adobe Experience Platform para enviar mensagens em lote a um conjunto específico de perfis. Para isso, é necessário criar segmentos. [Leia mais](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configurar a fonte de dados**: você pode definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Uma fonte de dados integrada da Adobe Experience Platform também é configurada no momento do provisionamento. Essa etapa não é necessária se você usar apenas os dados dos eventos na jornada. Esta etapa é executada por uma **usuário técnico**. [Leia mais](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar uma ação**: Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta seção [seção](../action/action.md). Esta etapa é executada por uma **usuário técnico**. Se estiver usando os recursos de mensagem integrados do Journey Otimizer, basta adicionar uma ação de canal à sua jornada e projetar seu conteúdo.

   ![](assets/custom2.png)

## Construa sua jornada{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Construa sua jornada"
>abstract="Essa tela exibe a lista de jornadas existentes. Abra uma jornada ou clique em &quot;Criar jornada&quot; e combine as diferentes atividades de evento, orquestração e ação para criar seus cenários de multicanal."

Essa etapa é executada pela **usuário empresarial**. É aqui que você cria suas jornadas. Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

Estas são as principais etapas para enviar mensagens por meio de jornadas:

1. Na seção do menu GERENCIAMENTO DE JORNADAS , clique em **[!UICONTROL Journeys]**. A lista de jornadas é exibida.

   ![](assets/interface-journeys.png)

1. Clique em **[!UICONTROL Create Journey]** para criar uma nova jornada.

1. Edite as propriedades da jornada no painel de configuração, exibido no lado direito. Saiba mais nesta seção [seção](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Comece arrastando e soltando um evento ou um **Ler segmento** atividade da paleta na tela. Para saber mais sobre design de jornada, consulte [esta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arraste e solte as próximas etapas que o indivíduo seguirá. Por exemplo, é possível adicionar uma condição seguida de uma ação de canal. Para saber mais sobre atividades, consulte [esta seção](using-the-journey-designer.md).

1. Teste sua jornada usando perfis de teste. Saiba mais nesta seção [seção](testing-the-journey.md)

1. Publique sua jornada para ativá-la. Saiba mais nesta seção [seção](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitore sua jornada usando as ferramentas de relatório dedicadas para medir a eficácia da sua jornada. Saiba mais nesta seção [seção](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definir as propriedades da jornada {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriedades da jornada"
>abstract="Esta seção mostra as propriedades da jornada. Por padrão, os parâmetros somente leitura ficam ocultos. As configurações disponíveis dependem do status da jornada, das permissões e da configuração do produto."

Clique no ícone de lápis, na parte superior direita para acessar as propriedades da jornada.

Você pode alterar o nome da jornada, adicionar uma descrição, permitir nova entrada, escolher datas de início e término e, como um usuário administrador, definir um **[!UICONTROL Timeout and error]** duração.

Para jornadas ao vivo, essa tela exibe a data da publicação e o nome do usuário que publicou a jornada.

O **Copiar detalhes técnicos** O permite copiar informações técnicas sobre a jornada que a equipe de suporte pode usar para solucionar problemas. As seguintes informações são copiadas: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrada{#entrance}

Por padrão, novas jornadas permitem reentrada. Você pode desmarcar a opção para jornadas de &quot;uma só vez&quot;, por exemplo, se quiser oferecer um presente único quando uma pessoa entrar em uma loja.

Saiba mais sobre o gerenciamento de entrada de perfil, em [esta seção](entry-management.md).

### Tempo limite e erro nas atividades da jornada {#timeout_and_error}

Ao editar uma ação ou atividade de condição, você pode definir um caminho alternativo em caso de erro ou tempo limite. Se o processamento da atividade de interrogação de um sistema de terceiros exceder a duração do tempo limite definida nas propriedades da viagem (**[!UICONTROL Timeout and  error]** ), o segundo caminho será escolhido para executar uma ação de fallback potencial.

Os valores autorizados estão entre 1 e 30 segundos.

Recomendamos que você defina uma **[!UICONTROL Timeout and error]** valor se sua jornada for sensível ao tempo (por exemplo: reação ao local em tempo real de uma pessoa) porque não é possível atrasar a ação por mais de alguns segundos. Se sua jornada for menos sensível ao tempo, você poderá usar um valor mais longo para dar mais tempo ao sistema chamado para enviar uma resposta válida.

As jornadas também usam um tempo limite global. Consulte a [próxima seção](#global_timeout).

### Tempo limite da jornada global {#global_timeout}

Além do [timeout](#timeout_and_error) usada em atividades de jornada, também há um tempo limite de jornada global que não é exibido na interface e não pode ser alterado. Esse tempo limite interromperá o progresso das pessoas físicas na jornada 30 dias após a sua entrada. Isto significa que a viagem de um indivíduo não pode durar mais de 30 dias. Após o período de tempo limite de 30 dias, os dados do indivíduo são excluídos. Os indivíduos que ainda fluem na jornada no final do período limite serão interrompidos e serão considerados como erros no relatório.

>[!NOTE]
>
>As jornadas não reagem diretamente às solicitações de recusa, acesso ou exclusão de privacidade. No entanto, o tempo limite global garante que os indivíduos nunca permaneçam mais de 30 dias em qualquer jornada.

Devido ao tempo limite de 30 dias da jornada, quando a reentrada da jornada não é permitida, não podemos garantir que o bloqueio de reentrada funcionará mais de 30 dias. Na verdade, ao removermos todas as informações sobre as pessoas que entraram na viagem 30 dias após a sua entrada, não podemos conhecer a pessoa que entrou anteriormente, há mais de 30 dias.

### Fuso horário e fuso horário do perfil {#timezone}

O fuso horário é definido no nível da jornada.

Você pode inserir um fuso horário fixo ou usar perfis da Adobe Experience Platform para definir o fuso horário da jornada.

Se um fuso horário for definido no perfil da Adobe Experience Platform, ele poderá ser recuperado na jornada.

Para obter mais informações sobre o gerenciamento de fuso horário, consulte [esta página](../building-journeys/timezone-management.md).

### Gerenciar acesso {#access}

Para atribuir rótulos de uso de dados personalizados ou principais à jornada, clique no botão **[!UICONTROL Manage access]** botão. [Saiba mais sobre o Controle de acesso no nível do objeto (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
