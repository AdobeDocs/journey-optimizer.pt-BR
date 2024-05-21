---
solution: Journey Optimizer
product: journey optimizer
title: Criar a primeira jornada
description: Etapas principais para criar sua primeira jornada com o Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: jornada, primeiro, iniciar, início rápido, público-alvo, evento, ação
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: c68e72d170792fc0ea3b6eb09b3acf818ec2cfd5
workflow-type: tm+mt
source-wordcount: '2086'
ht-degree: 17%

---

# Criar a primeira jornada{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Criar jornadas"
>abstract="Use o **Adobe Journey Optimizer** para criar casos de uso de orquestração em tempo real, aproveitando dados contextuais armazenados em eventos ou fontes de dados."



## Pré-requisitos{#start-prerequisites}

Para enviar mensagens com jornadas, as seguintes configurações são necessárias:

1. **Configurar um evento**: se quiser acionar as jornadas de forma unitária quando um evento for recebido, será necessário configurar um evento. Você define as informações esperadas e como processá-las. Esta etapa é executada por um **usuário técnico**. [Leia mais](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Criar um público**: sua jornada também pode ouvir os públicos da Adobe Experience Platform para enviar mensagens em lote para um conjunto especificado de perfis. Para isso, você precisa criar públicos. [Leia mais](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configurar a fonte de dados**: é possível definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Uma fonte de dados integrada da Adobe Experience Platform também é configurada no momento do provisionamento. Esta etapa não é necessária se você usar somente os dados dos eventos em sua jornada. Esta etapa é executada por um **usuário técnico**. [Leia mais](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar uma ação**: se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta página [seção](../action/action.md). Esta etapa é executada por um **usuário técnico**. Se você estiver usando os recursos de mensagem incorporados do Journey Optimizer, basta adicionar uma ação de canal à jornada e projetar o conteúdo.

   ![](assets/custom2.png)

## Acessar jornadas {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Jornadas"
>abstract="Crie jornadas do cliente para fornecer experiências personalizadas e contextuais. O Journey Optimizer permite criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados. A guia **Visão geral** exibe um painel com as métricas principais relacionadas às suas jornadas. A guia **Procurar** exibe a lista de jornadas existentes."

### Métricas principais e lista de jornadas {#access-metrics}

Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**. Duas guias estarão disponíveis:

**Visão geral**: esta guia exibe um painel com as métricas principais relacionadas às suas jornadas:

* **Perfis processados**: número total de perfis processados nas últimas 24 horas
* **Jornada ao vivo**: número total de jornadas ativas com tráfego nas últimas 24 horas. As jornadas em tempo real incluem **Jornadas unitárias** (com base em eventos) e **Jornadas em lote** (leia público).
* **Taxa de erros**: taxa de todos os perfis com erro em comparação ao número total de perfis que entraram nas últimas 24 horas.
* **Taxa de descarte**: taxa de todos os perfis descartados em comparação ao número total de perfis que entraram nas últimas 24 horas. Um perfil descartado representa alguém que não está qualificado para entrar na jornada, por exemplo, devido a um namespace incorreto ou a regras de reentrada.

>[!NOTE]
>
>Esse painel considera as jornadas com tráfego nas últimas 24 horas. Somente as jornadas às quais você tem acesso são exibidas. As métricas são atualizadas a cada 30 minutos e somente quando novos dados estão disponíveis.

![](assets/journeys-dashboard.png)

**Procurar**: esta guia exibe a lista de jornadas existentes. Você pode pesquisar jornadas, usar filtros e executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item. Para obter mais informações, consulte [esta seção](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

### Filtrar jornadas {#filter}

Na lista de jornadas, você pode aproveitar vários filtros para refinar a lista de jornadas para melhorar a legibilidade.

![](assets/filter-journeys.png)

Estas são as várias operações de filtragem que você pode executar:

Filtre as jornadas de acordo com seu status, tipo, versão e tags atribuídas do **[!UICONTROL Filtros de status e versão]**.

O tipo pode ser: **[!UICONTROL Evento unitário]**, **[!UICONTROL Qualificação de público]**, **[!UICONTROL Ler público]** ou **[!UICONTROL Evento comercial]**.

O status pode ser:

* **Fechado**: a jornada foi fechada usando o **Fechar para novas entradas** botão. A jornada pára de permitir que novos indivíduos entrem na jornada. As pessoas que já estão na jornada podem terminar a jornada normalmente.
* **Rascunho**: a jornada está em seu primeiro estágio. Ele ainda não foi publicado.
* **Rascunho (Teste)**: o modo de teste foi ativado usando o **Modo de teste** botão.
* **Concluído**: a jornada alterna automaticamente para esse status após o tempo limite global padrão de 30 dias. Os perfis que já estão na jornada concluem a jornada normalmente. Novos perfis não podem mais entrar na jornada.
* **Ao vivo**: a jornada foi publicada usando o **Publish** botão.
* **Parado**: a jornada foi desligada usando o **Parar** botão. Todos os indivíduos saem instantaneamente da jornada.

>[!NOTE]
>
>O ciclo de vida de criação do Jornada também inclui um conjunto de status intermediários que não estão disponíveis para filtragem: &quot;Publicação&quot; (entre &quot;Rascunho&quot; e &quot;Ao vivo&quot;), &quot;Ativando modo de teste&quot; ou &quot;Desativando modo de teste&quot; (entre &quot;Rascunho&quot; e &quot;Rascunho (teste)&quot;) e &quot;Parando&quot; entre &quot;Ao vivo&quot; e &quot;Parado&quot;). Quando uma jornada está em um estado intermediário, ela fica como de somente leitura.

Use o **[!UICONTROL Filtros de criação]** para filtrar jornadas de acordo com a data de criação ou o usuário que as criou.

Exibir jornadas que usam um evento, grupo de campos ou ação específica do **[!UICONTROL Filtros de atividade]** e **[!UICONTROL Filtros de dados]**.

Use o **[!UICONTROL Filtros de publicação]** para selecionar uma data de publicação ou um usuário. Você pode optar, por exemplo, por exibir as versões mais recentes de jornadas ao vivo que foram publicadas ontem.

Para filtrar jornadas com base em um intervalo de datas específico, selecione **[!UICONTROL Personalizado]** do **[!UICONTROL Publicado]** lista suspensa.

Além disso, nos painéis de configuração Evento, Fonte de dados e Ação, a variável **[!UICONTROL Usado em]** campo exibe o número de jornadas que usam esse evento, grupo de campos ou ação específica. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas correspondentes.

![](assets/journey3bis.png)

## Criar sua jornada{#jo-build}

Esta etapa é executada pelo **usuário empresarial**. É aqui que você cria suas jornadas. Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

➡️ [Descubra este recurso no vídeo](journey.md#video)

Estas são as etapas principais para enviar mensagens por meio do jornada:

1. No **Procurar** clique em **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite as propriedades da jornada no painel de configuração exibido no lado direito. Saiba mais nesta [seção](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Comece arrastando e soltando um evento ou uma **Ler público-alvo** atividade da paleta para a tela. Para saber mais sobre o design do jornada, consulte [nesta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arraste e solte as próximas etapas que o indivíduo seguirá. Por exemplo, é possível adicionar uma condição seguida por uma ação de canal. Para saber mais sobre atividades, consulte [nesta seção](using-the-journey-designer.md).

1. Teste a jornada usando perfis de teste. Saiba mais nesta página [seção](testing-the-journey.md)

1. Publique sua jornada para ativá-la. Saiba mais nesta [seção](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitore sua jornada usando as ferramentas de relatório dedicadas para medir a eficiência da sua jornada. Saiba mais nesta [seção](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definir as propriedades da jornada {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriedades da jornada"
>abstract="Essa seção mostra as propriedades da jornada. Por padrão, os parâmetros somente leitura ficam ocultos. As configurações disponíveis dependem do status da jornada, das permissões e da configuração do produto."

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Critérios de saída da jornada"
>abstract="Esta seção mostra as opções de critérios de saída. É possível criar uma ou várias regras de critérios de saída para a sua jornada."

Clique no ícone de lápis, ao lado do nome da jornada, para acessar suas propriedades.

É possível alterar o nome da jornada, adicionar uma descrição, permitir a reentrada, escolher datas de início e término e, como usuário administrador, definir um **[!UICONTROL Tempo limite e erro]** duração. Você também pode atribuir Tags unificadas do Adobe Experience Platform à sua jornada. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

Para jornadas ao vivo, essa tela exibe a data da publicação e o nome do usuário que publicou a jornada.

A variável **Copiar detalhes técnicos** O permite copiar informações técnicas sobre a jornada que a equipe de suporte pode usar para a solução de problemas. As seguintes informações são copiadas: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrada e reentrada {#entrance}

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção **Permitir reentrada** opção para jornadas &quot;one shot&quot;, por exemplo, se você quiser oferecer um presente único quando uma pessoa entrar em uma loja.

Quando a variável **Permitir reentrada** estiver ativada, a variável **Período de espera de reentrada** é exibido. Este campo possibilita definir o tempo de espera antes de permitir que um perfil entre novamente em jornadas unitárias (que começam com um evento ou uma qualificação de público-alvo). Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. A duração máxima é de 29 dias.

Saiba mais sobre o gerenciamento de entrada e reentrada de perfis, em [nesta seção](entry-management.md).

### Gerenciar acesso {#manage-access}

Para atribuir rótulos de uso de dados personalizados ou principais à jornada, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o OLA (Object Level Access Control, controle de acesso em nível de objeto)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Fusos horários de Jornada e perfil {#timezone}

O fuso horário é definido no nível da jornada. Você pode inserir um fuso horário fixo ou usar perfis do Adobe Experience Platform para definir o fuso horário de jornada. Se um fuso horário for definido no perfil do Adobe Experience Platform, ele poderá ser recuperado na jornada.

Para obter mais informações sobre o gerenciamento de fuso horário, consulte [esta página](../building-journeys/timezone-management.md).

### Datas de início e término {#dates}

Você pode definir um **Data inicial**. Se não tiver especificado um, ele será definido automaticamente no momento da publicação.

Você também pode adicionar um **Data final**. Isso permite que os perfis saiam automaticamente quando a data for atingida. Se nenhuma data final for especificada, os perfis poderão permanecer até que o [tempo limite de jornada global](#global_timeout) (que geralmente é de 30 dias e é reduzido para 7 dias com a oferta complementar do Healthcare Shield). A única exceção são as jornadas recorrentes de leitura de público com **Forçar reentrada na recorrência** ativadas, que terminam na data de início da próxima ocorrência.

### Tempo limite e erro em atividades de jornada {#timeout_and_error}

Ao editar uma atividade de ação ou condição, é possível definir um caminho alternativo em caso de erro ou tempo limite. Se o processamento da atividade que interroga um sistema de terceiros exceder a duração do tempo limite definida nas propriedades da jornada (**[!UICONTROL Tempo limite e erro]** ), o segundo caminho será escolhido para executar uma possível ação de fallback.

Os valores autorizados estão entre 1 e 30 segundos.

Recomendamos que você defina um período muito curto **[!UICONTROL Tempo limite e erro]** valor se a jornada for sensível ao tempo (por exemplo: reagir ao local em tempo real de uma pessoa) porque você não pode atrasar a ação por mais de alguns segundos. Se a jornada for menos sensível ao tempo, você poderá usar um valor mais longo para dar mais tempo ao sistema chamado para enviar uma resposta válida.

O Jornada também usa um tempo limite global. Consulte a [próxima seção](#global_timeout).

### Tempo limite de jornada global {#global_timeout}

Além do [timeout](#timeout_and_error) usado em atividades de jornada, também há um tempo limite de jornada global que não é exibido na interface e não pode ser alterado.

Esse tempo limite global interrompe o progresso das pessoas físicas na jornada **30 dias** após entrarem. Este tempo limite é reduzido a **7 dias** com a oferta complementar do Healthcare Shield. Isso significa que a jornada de um indivíduo não pode durar mais de 30 dias (ou 7 dias). Após esse período de tempo limite, os dados do indivíduo são excluídos. Os indivíduos que ainda fluem na jornada no final do período de tempo limite serão interrompidos e não serão considerados nos relatórios. Portanto, você poderia ver mais pessoas entrando na jornada do que saindo.

>[!NOTE]
>
>As jornadas não reagem diretamente a solicitações de recusa de privacidade, acesso ou exclusão. No entanto, o tempo limite global garante que os indivíduos nunca fiquem mais de 30 dias em qualquer jornada.

Devido ao tempo limite de jornada de 30 dias, quando a reentrada da jornada não é permitida, não podemos garantir que o bloqueio de reentrada funcionará por mais de 30 dias. Na verdade, à medida que removemos todas as informações sobre as pessoas que entraram na jornada 30 dias depois de entrarem, não podemos saber a pessoa inserida anteriormente, há mais de 30 dias.

Um indivíduo só poderá inserir uma atividade de espera se tiver tempo suficiente na jornada para concluir a duração da espera antes do tempo limite de jornada de 30 dias. Consulte [esta página](../building-journeys/wait-activity.md).

### Políticas de mesclagem {#merge-policies}

O Jornada usa políticas de mesclagem ao recuperar dados de perfil do Adobe Experience Platform. Dependendo do tipo de jornada, são usadas diferentes políticas de mesclagem:

* Em Ler jornadas de qualificação de público ou público-alvo: a política de mesclagem do público-alvo é usada
* Em jornadas acionadas por eventos: a política de mesclagem padrão é usada

O Jornada seguirá a política de mesclagem usada em toda a jornada.

>[!NOTE]
>
>Esse recurso só está disponível em Disponibilidade limitada (DL) para clientes selecionados.

Para saber mais sobre políticas de mesclagem, consulte este [página](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview)

## Duplicar uma jornada {#duplicate-a-journey}

É possível duplicar uma jornada existente do **Procurar** guia. Todos os objetos e configurações são duplicados na cópia de jornada.

Para fazer isso, siga as etapas abaixo:

1. Navegue até a jornada que deseja copiar, clique na guia **Mais ações** ícone (os três pontos ao lado do nome da jornada).
1. Selecione **Duplicar**.

   ![Duplicar uma jornada](assets/duplicate-jo.png)

1. Insira o nome da jornada e confirme. Você também pode alterar o nome na tela de propriedades da jornada. Por padrão, o nome é definido da seguinte maneira: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. A nova jornada é criada e está disponível na lista de jornadas.
