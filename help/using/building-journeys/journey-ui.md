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
source-git-commit: d7ebba4144eeb5b29e9e6fa21afde06a7e520e07
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 26%

---

# Procurar e filtrar suas jornadas {#browse-journeys}

## Jornada painel {#dashboard-jo}

Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**. Duas guias estão disponíveis: **[!UICONTROL Visão geral]** e **[!UICONTROL Procurar]**.


* A guia **[!UICONTROL Visão geral]** exibe um painel com as métricas principais relacionadas às suas jornadas.

  ![Painel de jornada destacando a guia Visão Geral](assets/journeys-dashboard.png)

   * **Perfis processados**: número total de perfis processados nas últimas 24 horas
   * **Live jornada**: número total de jornadas ativas com tráfego nas últimas 24 horas. O Live jornada inclui **jornadas Unitárias** (baseadas em eventos) e **jornadas em Lote** (ler público).
   * **Taxa de erros**: taxa de todos os perfis com erro em comparação ao número total de perfis que entraram nas últimas 24 horas.
   * **Taxa de descarte**: taxa de todos os perfis descartados em comparação ao número total de perfis que entraram nas últimas 24 horas. Um perfil descartado representa alguém que não está qualificado para entrar na jornada, por exemplo, devido a um namespace incorreto ou devido a regras de reentrada.

  >[!NOTE]
  >
  >Esse painel considera as jornadas com tráfego nas últimas 24 horas. Somente as jornadas às quais você tem acesso são exibidas. As métricas são atualizadas a cada 30 minutos e somente quando novos dados estão disponíveis.


* A guia **[!UICONTROL Procurar]** mostra a lista de jornadas existentes. Você pode pesquisar jornadas, usar filtros e executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item.

  ![Painel de jornada destacando a guia Procurar](assets/journeys-browse.png)

## Filtrar suas jornadas {#journey-filter}

Na lista de jornadas, use vários filtros para refinar a lista de jornadas.

![](assets/filter-journeys.png)

Você pode filtrar jornadas de acordo com seu [status](#journey-statuses), [tipo](#journey-types), [versão](#journey-versions) e [marcas](../start/search-filter-categorize.md#tags) atribuídas a partir dos **[!UICONTROL filtros de status e versão]**.

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


Saiba mais sobre os tipos de jornada e o gerenciamento de entradas associado em [esta página](entry-management.md).

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


## Versões de jornada {#journey-versions}

Na lista da jornada, todas as versões da jornada são exibidas com o número da versão. Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Geralmente, um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo. Se a reentrada estiver habilitada, um perfil poderá ser inserido em uma jornada novamente, mas não poderá fazer isso até que tenha saído totalmente da instância anterior da jornada. [Leia mais](end-journey.md).

### Criar uma nova versão de uma jornada {#journey-create-new-version}

Se precisar modificar para uma jornada em tempo real, crie uma nova versão da jornada. Para criar uma nova versão de uma jornada existente, siga as etapas abaixo:

1. Abra a versão mais recente da jornada ativa, clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Só é possível criar uma nova versão com base na versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

A partir do momento em que a jornada for publicada, pessoas físicas começarão a acessar a versão mais recente da jornada. As pessoas que já acessaram uma versão anterior permanecerão nela até que concluam a jornada. Se mais tarde entrarem novamente na mesma jornada, a versão mais recente será acessada.

As versões da jornada podem ser interrompidas individualmente. Todas as versões das jornadas possuem o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior encerra automaticamente e alterna para o status **Fechado**. Nenhuma entrada na jornada pode acontecer. Mesmo que você interrompa a versão mais recente, a versão anterior permanecerá fechada.



## Duplicar uma jornada {#duplicate-a-journey}

Você pode duplicar uma jornada existente da guia **Procurar**. Todos os objetos e configurações são duplicados na cópia de jornada.

Para fazer isso, siga as etapas abaixo:

1. Navegue até a jornada que deseja copiar e clique no ícone **Mais ações** (os três pontos ao lado do nome da jornada).
1. Selecione **Duplicar**.

   ![Duplicar uma jornada](assets/duplicate-jo.png)

1. Insira o nome da jornada e confirme. Você também pode alterar o nome na tela de propriedades da jornada. Por padrão, o nome é definido da seguinte maneira: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. A nova jornada é criada e está disponível na lista de jornadas.
