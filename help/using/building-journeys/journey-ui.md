---
solution: Journey Optimizer
product: journey optimizer
title: Procurar e filtrar suas jornadas
description: Procurar e filtrar suas jornadas no Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: jornada, primeiro, iniciar, início rápido, público-alvo, evento, ação
exl-id: 770bdbf2-560d-4127-bdb9-1f82495a566f
source-git-commit: 29d12b6190f49e7f3f6fd2760e522a5a62c0de87
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 9%

---

# Procurar e filtrar suas jornadas {#browse-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_view"
>title="Exibições de lista e calendário do Jornada"
>abstract="Além da lista de jornadas, o [!DNL Journey Optimizer] fornece uma exibição de calendário de suas jornadas, oferecendo uma representação visual clara de suas agendas. Você pode alternar entre as visualizações de lista e calendário a qualquer momento usando esses botões."

## Painel da jornada {#dashboard-jo}

Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**. Duas guias estão disponíveis: **[!UICONTROL Visão geral]** e **[!UICONTROL Procurar]**.

### Visão geral do Jornada

A guia **[!UICONTROL Visão geral]** exibe um painel com as métricas principais relacionadas às suas jornadas.

![Painel de jornada destacando a guia Visão Geral](assets/journeys-dashboard.png)

* **Perfis processados**: número total de perfis processados nas últimas 24 horas
* **Live jornada**: número total de jornadas ativas com tráfego nas últimas 24 horas. O Live jornada inclui **jornadas Unitárias** (baseadas em eventos) e **jornadas em Lote** (ler público).
* **Taxa de erros**: taxa de todos os perfis com erro em comparação ao número total de perfis que entraram nas últimas 24 horas.
* **Taxa de descarte**: taxa de todos os perfis descartados em comparação ao número total de perfis que entraram nas últimas 24 horas. Um perfil descartado representa alguém que não está qualificado para entrar na jornada, por exemplo, devido a um namespace incorreto ou devido a regras de reentrada.

>[!NOTE]
>
>Esse painel considera as jornadas com tráfego nas últimas 24 horas. Somente as jornadas às quais você tem acesso são exibidas. As métricas são atualizadas a cada 30 minutos e somente quando novos dados estão disponíveis.

### Lista de jornadas

A guia **[!UICONTROL Procurar]** mostra a lista de jornadas existentes. Você pode pesquisar jornadas, usar filtros e executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item.

![Painel de jornada destacando a guia Procurar](assets/journeys-browse.png)

### Calendário do Jornada {#calendar}

Além da lista de jornadas, o [!DNL Journey Optimizer] fornece uma exibição de calendário de suas jornadas, oferecendo uma representação visual clara de suas agendas.

>[!AVAILABILITY]
>
>No momento, a exibição de calendário está disponível apenas para um conjunto de organizações (Disponibilidade limitada). Para solicitar acesso, use [este formulário](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}.
>
>Esse recurso está em desenvolvimento ativo. Suas solicitações e informações são bem-vindas usando o botão **[!UICONTROL Comentários sobre a Beta]** no menu superior.

Para acessar o modo de exibição de calendário, abra a lista jornadas e clique no ícone ![calendário](assets/do-not-localize/timeline-icon.svg).

O calendário exibe todas as jornadas programadas para a semana atual. Use os botões de seta acima do calendário para navegar entre semanas.

![exibição de calendário mostrando jornadas ao vivo](assets/timeline-journeys.png)

Como as jornadas são representadas:

* Por padrão, a grade de calendário mostra todas as jornadas ativas e programadas para a semana selecionada. Opções de filtro adicionais podem mostrar ativações ou ativações concluídas, interrompidas e concluídas.
* Jornadas de rascunho e jornadas no modo de teste não são exibidas.
* Jornadas que abrangem vários dias são exibidas na parte superior da grade do calendário.
* Se nenhuma hora de início for especificada, a hora de ativação manual mais próxima será usada para posicioná-la no calendário.
* As jornadas são exibidas como intervalos de tempo de 1 hora, mas isso não reflete a hora real de envio ou de conclusão.

Para obter mais detalhes sobre uma jornada, clique no bloco visual para abrir e explorar os detalhes.

Na lista da jornada, todas as versões da jornada são exibidas com o número da versão. Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela. Saiba mais sobre o [gerenciamento de versão do jornada](publishing-the-journey.md#journey-versions-journey-versions).



## Filtrar suas jornadas {#journey-filter}

Na lista de jornadas, use vários filtros para refinar a lista de jornadas.

![Tela mostrando um exemplo de filtragem de jornada com dois tipos de jornadas selecionados](assets/filter-journeys.png)

Você pode filtrar jornadas de acordo com seu [status](#journey-statuses), [tipo](#journey-types), [versão](publishing-the-journey.md#journey-versions-journey-versions) e [marcas](../start/search-filter-categorize.md#tags) atribuídas a partir dos **[!UICONTROL filtros de status e versão]**.

Use os **[!UICONTROL Filtros de criação]** para filtrar jornadas de acordo com a data de criação ou o usuário que as criou.

Exiba jornadas que usam um evento, grupo de campos ou ação específica dos **[!UICONTROL Filtros de atividade]** e **[!UICONTROL Filtros de dados]**.

Use os **[!UICONTROL Filtros de publicação]** para selecionar uma data de publicação ou um usuário. Você pode optar, por exemplo, por exibir as versões mais recentes de jornadas ao vivo que foram publicadas ontem.

Para filtrar jornadas com base em um intervalo de datas específico, selecione **[!UICONTROL Personalizado]** na lista suspensa **[!UICONTROL Publicado]**.

Além disso, nos painéis de configuração Evento, Fonte de dados e Ação, o campo **[!UICONTROL Usado em]** exibe o número de jornadas que usam aquele determinado evento, grupo de campos ou ação. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas correspondentes.

![](assets/journey3bis.png)

## Tipos de jornada {#journey-types}

O tipo de jornada depende das atividades usadas nessa jornada. Pode ser:

* **[!UICONTROL Evento unitário]** - As jornadas de eventos unitários estão vinculadas a um perfil específico. Os eventos estão relacionados ao comportamento de uma pessoa ou a algo que acontece vinculado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos de fidelidade). [Saiba mais](../event/about-events.md).
* **[!UICONTROL Evento comercial]**. A jornada de eventos comerciais começa com um evento não relacionado a perfis. A configuração do evento é executada por um usuário técnico e não pode ser editada. [Saiba mais](../event/about-events.md).
* **[!UICONTROL Qualificação de público-alvo]** - As jornadas de qualificação de público-alvo ouvem as entradas e saídas dos perfis nos públicos-alvo da Adobe Experience Platform para que os indivíduos entrem ou avancem em uma jornada. [Saiba mais](audience-qualification-events.md).
* **[!UICONTROL Ler público-alvo]** - Nas jornadas Ler público-alvo, todos os indivíduos no público-alvo entram na jornada e recebem as mensagens incluídas na jornada.  [Saiba mais](read-audience.md).


Saiba mais sobre os tipos de jornadas e o gerenciamento de entradas associado nesta [página](entry-management.md).

## Jornada status {#journey-statuses}

O status da jornada depende do seu ciclo de vida. Pode ser:

* **Fechada**: a jornada foi fechada usando o botão **Fechar para novas entradas**. A jornada pára de permitir que novos indivíduos entrem na jornada. As pessoas que já estão na jornada podem terminar a jornada normalmente.
* **Rascunho**: a jornada está em seu primeiro estágio. Ele ainda não foi publicado.
* **Rascunho (Teste)**: o modo de teste foi ativado usando o botão **Modo de teste**.
* **Concluído**: a jornada alterna automaticamente para esse status após o [tempo limite global](journey-properties.md#global_timeout) de 91 dias. Os perfis que já estão na jornada concluem a jornada normalmente. Novos perfis não podem mais entrar na jornada.
* **Ao vivo**: a jornada foi publicada usando o botão **Publicar**.
* **Parada**: a jornada foi desligada usando o botão **Parada**. Todos os indivíduos saem instantaneamente da jornada.

>[!NOTE]
>
>* O ciclo de vida de criação do Jornada também inclui um conjunto de status intermediários que não estão disponíveis para filtragem: &quot;Publicação&quot; (entre &quot;Rascunho&quot; e &quot;Ao vivo&quot;), &quot;Ativando modo de teste&quot; ou &quot;Desativando modo de teste&quot; (entre &quot;Rascunho&quot; e &quot;Rascunho (teste)&quot;) e &quot;Parando&quot; (entre &quot;Ao vivo&quot; e &quot;Parado&quot;). Quando uma jornada está em um estado intermediário, ela fica como de somente leitura.
>
>* Se você precisar modificar para uma jornada do **live**, [crie uma nova versão](#journey-versions) da jornada.


## Duplicar uma jornada {#duplicate-a-journey}

Você pode duplicar uma jornada existente da guia **Procurar**. Todos os objetos e configurações são duplicados na cópia de jornada.

Para fazer isso, siga as etapas abaixo:

1. Navegue até a jornada que deseja copiar e clique no ícone **Mais ações** (os três pontos ao lado do nome da jornada).
1. Selecione **Duplicar**.

   ![Duplicar uma jornada](assets/duplicate-jo.png)

1. Insira o nome da jornada e confirme. Você também pode alterar o nome na tela de propriedades da jornada. Por padrão, o nome é definido da seguinte maneira: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. A nova jornada é criada e está disponível na lista de jornadas.
