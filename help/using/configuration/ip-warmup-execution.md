---
solution: Journey Optimizer
product: journey optimizer
title: Executar o plano de aquecimento de IP
description: Saiba como executar e monitorar um plano de aquecimento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: 205f26d3f31b9f003fc1dbaf679021464429d144
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 20%

---

# Executar o plano de aquecimento de IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* **[Executar o plano de aquecimento de IP](ip-warmup-execution.md)**

>[!ENDSHADEBOX]

Depois de [um plano de aquecimento de IP foi criado](ip-warmup-plan.md) e fez upload do arquivo preparado com seu consultor de entrega, você pode definir as fases e as execuções em seu plano.

Cada fase é composta por várias execuções, às quais você atribui uma única campanha.

## Definir as fases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Excluir públicos-alvo da campanha"
>abstract="Selecione os públicos-alvo de outras campanhas que deseja excluir da fase atual. Isso evita que perfis contatados anteriormente (em outras fases ou planos de aquecimento de IP) sejam direcionados novamente."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Excluir grupos de domínio"
>abstract="Selecione os domínios que deseja excluir da fase atual. A exclusão de domínios requer uma fase não executada, portanto, talvez seja necessário dividir uma fase em execução para adicionar exclusões."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html?lang=pt-BR#split-phase" text="Dividir uma fase"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="Definir as fases do plano"
>abstract="Cada fase é composta por várias execuções, às quais você atribui uma única campanha."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. Para cada fase, selecione a campanha que deseja associar a esta fase do plano de aquecimento de IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Observe o seguinte:

   * Somente as campanhas com o **[!UICONTROL Ativação do plano de aquecimento de IP]** opção ativada <!--and live?--> estão disponíveis para seleção. [Saiba mais](#create-ip-warmup-campaign)

   * Você deve selecionar uma campanha que use a mesma superfície que a selecionada para o plano de aquecimento de IP atual.

   * Não é possível selecionar uma campanha que já está em uso em outra campanha de aquecimento de IP.

1. No **[!UICONTROL Exclusão de perfil]** é possível ver que os perfis das execuções anteriores dessa fase são sempre excluídos. Por exemplo, se em Run #1 um perfil foi coberto nas primeiras 4.800 pessoas que foram alvos, o sistema garantirá automaticamente que o mesmo perfil não receba o email em Run #2.

1. No **[!UICONTROL Públicos-alvo de campanha excluídos]** selecione os públicos-alvo de outros <!--executed/live?-->campanhas que você deseja excluir da fase atual.

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   Por exemplo, ao executar a Fase 1, você tinha que [dividir](#split-phase) por qualquer motivo. Portanto, você pode excluir a campanha usada na Fase 1 para que os perfis contatados anteriormente da Fase 1 não sejam incluídos na Fase 2. Você também pode excluir campanhas de outros planos de aquecimento de IP.

1. No **[!UICONTROL Grupos de domínio excluídos]** selecione os domínios que deseja excluir dessa fase.

   >[!NOTE]
   >
   >A exclusão de domínio requer uma fase não executada, portanto, talvez seja necessário [dividir uma fase em execução](#split-phase) para adicionar exclusões.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Por exemplo, após executar o aquecimento de IP por alguns dias, você percebe que a reputação do ISP com um domínio (por exemplo, Adobe) não é boa e deseja resolvê-la sem interromper o plano de aquecimento de IP. Nesse caso, você pode excluir o grupo de domínio Adobe.

   >[!NOTE]
   >
   >Se o domínio não for um grupo de domínio pronto para uso, você precisará trabalhar com o consultor de entrega para adicionar esse domínio à [Arquivo de plano de aquecimento de IP](ip-warmup-plan.md#prepare-file) e [fazer upload novamente](#re-upload-plan) para poder excluir esse domínio.

1. Você pode adicionar uma fase, se necessário. Ele será adicionado após a última fase atual.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Use o **[!UICONTROL Excluir fase]** botão para remover qualquer fase indesejada.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!CAUTION]
   >
   >Não é possível desfazer a variável **[!UICONTROL Excluir]** ação.
   >
   >Se você excluir todas as fases do plano de aquecimento de IP, é recomendável fazer upload de um plano novamente. [Saiba mais](#re-upload-plan)

## Definir as execuções {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="Definir cada execução"
>abstract="Defina e ative cada execução para todas as fases."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="Filtrar no engajamento"
>abstract="Essa coluna é um filtro que direciona somente os usuários engajados com sua marca nos últimos 20 dias, por exemplo. Também é possível alterar essa configuração por meio da opção **Editar execução**."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="Definir uma janela de tempo"
>abstract="Você pode definir uma janela de tempo durante a qual a campanha de aquecimento de IP poderá ser executada, caso haja atrasos no processo de segmentação."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="Cancelar execuções com erros de público-alvo"
>abstract="Selecione essa opção para cancelar uma execução se os perfis qualificados forem menores que os perfis direcionados após o público-alvo ter sido avaliado para a execução."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="Exibir os perfis qualificados"
>abstract="Essa coluna exibe o número de perfis qualificados. Caso haja mais perfis direcionados do que perfis qualificados após o público-alvo ter sido avaliado para uma execução, ela ainda será executada, a menos que a opção **Pausar em caso de erros** esteja habilitada. Nesse caso, a execução é cancelada."

1. Selecione uma programação para cada execução.

   ![](assets/ip-warmup-plan-send-time.png)

1. Como opção, você pode definir uma janela de tempo durante a qual a campanha de aquecimento de IP pode ser executada em caso de atrasos no [segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} tarefa. Para fazer isso, clique no ícone Propriedades na parte superior esquerda, ao lado do nome do plano, e use o **[!UICONTROL Tentar novamente o tempo de execução]** para selecionar uma duração - até 240 minutos (4 horas).

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Por exemplo, se você definir um horário de envio em um determinado dia às 9h e selecionar 120 minutos como o tempo de execução de repetição, isso permitirá uma janela de oportunidade de 2 horas (9h - 11h) para o trabalho de segmentação ser executado.

   >[!NOTE]
   >
   >Se nenhuma janela de tempo for especificada, a execução será tentada no momento do envio e falhará se o trabalho de segmentação não for concluído.

1. Se necessário, selecione **[!UICONTROL Editar execução]** no ícone Mais ações. Lá é possível atualizar os números de endereços em cada coluna. Você também pode atualizar a variável **[!UICONTROL Último envolvimento]** para direcionar somente os usuários engajados com sua marca nos últimos 20 dias, por exemplo.

   ![](assets/ip-warmup-plan-edit-run.png)

1. Selecione o **[!UICONTROL Pausar para erros]** opção para cancelar uma execução se os perfis qualificados forem menores que os perfis direcionados depois que o público-alvo tiver sido avaliado para essa execução.

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL Ativar]** a execução. [Saiba mais](#activate-run)

1. O status dessa execução muda para **[!UICONTROL Ao vivo]**. Os diferentes status de execução são listados em [nesta seção](#monitor-plan).

1. Se a execução da campanha não tiver sido iniciada, é possível interromper uma execução em tempo real.<!--why?-->

   ![](assets/ip-warmup-plan-stop-run.png)

   >[!NOTE]
   >
   >Depois que a execução da campanha for iniciada, a variável **[!UICONTROL Parar]** fica indisponível.

1. Para adicionar uma execução, selecione **[!UICONTROL Adicionar uma execução abaixo]** no ícone Mais ações.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Ativar uma execução {#activate-run}

Para ativar uma execução, selecione o **[!UICONTROL Ativar]** botão.

Verifique se você programou tempo suficiente para permitir a [segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} tarefa a ser executada.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>Cada execução deve ser ativada pelo menos 12 horas antes da hora real de envio. Caso contrário, a segmentação pode não ser concluída.

Quando você ativa uma execução, vários segmentos são criados automaticamente.

* Se ativar a primeira execução de uma fase:

   * A [segmento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=pt-br){target="_blank"} é criado para os públicos-alvo excluídos (se houver).
   * Outro segmento é criado para os grupos de domínio excluídos (se houver).

* Ao ativar qualquer execução:

   * Outro segmento é criado para o último filtro de envolvimento.
   * Um [composição de público](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=pt-BR){target="_blank"} é criada e corresponde ao público para o qual a campanha será enviada.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## Gerencie seu plano {#manage-plan}

A qualquer momento, se o seu plano de aquecimento de IP não estiver funcionando como o esperado, você poderá executar as ações abaixo.

### Dividir uma fase {#split-phase}

Se quiser adicionar uma nova fase começando em uma execução específica, selecione a **[!UICONTROL Opção Dividir para uma nova fase]** no ícone Mais ações.

![](assets/ip-warmup-plan-run-split-run.png)

Uma nova fase é criada para as execuções restantes da fase atual.

Por exemplo, se você selecionar esta opção para Run #4, as execuções #4 para #8 serão movidas para uma nova fase logo após a fase atual.

Siga as etapas [acima](#define-phases) para definir a nova fase.

* Você pode usar o **[!UICONTROL Substituir campanha]** para essa nova fase.

* Você também pode excluir a campanha anterior ou um domínio que não esteja apresentando um bom desempenho. Saiba mais em [nesta seção](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Marcar um plano como concluído {#mark-as-completed}

Se seu plano não estiver funcionando bem o suficiente ou se você quiser descartá-lo para criar outro, poderá marcá-lo como concluído.

Para fazer isso, clique no link **[!UICONTROL Mais]** na parte superior direita do plano de aquecimento de IP e selecione **[!UICONTROL Marcar como concluído]**.

![](assets/ip-warmup-plan-mark-completed.png)

Essa opção só estará disponível se todas as execuções no plano estiverem em **[!UICONTROL Concluído]** ou **[!UICONTROL Rascunho]** status. Se uma execução for **[!UICONTROL Ao vivo]**, a opção fica esmaecida.

Os diferentes status de execução são listados em [nesta seção](#monitor-plan).

### Recarregar um plano de aquecimento de IP {#re-upload-plan}

Se o plano de aquecimento de IP não estiver funcionando como esperado (por exemplo, se você observar que alguns ISPs estão marcando suas mensagens como spam), você pode pedir ao seu especialista de capacidade de entrega para configurar outro arquivo de plano de aquecimento de IP e fazer upload novamente usando o botão correspondente.

![](assets/ip-warmup-re-upload-plan.png)

Todas as execuções executadas anteriormente serão somente leitura. O novo plano é exibido abaixo do primeiro plano.

Siga as etapas [acima](#define-phases) para definir as fases do novo plano.

>[!NOTE]
>
>Os detalhes do plano de aquecimento de IP serão alterados conforme o arquivo recém-carregado. As execuções executadas anteriormente (independentemente de suas [status](#monitor-plan)) não são afetadas.

Vamos ver um exemplo:

* Com o plano inicial de aquecimento de IP, a Fase 2 tinha 9 execuções.

* 4 execuções foram executadas (não importa se falharam, foram concluídas ou foram canceladas<!--as long as a run has been attempted, it is an executed run-->).

* Se você fizer upload novamente de um novo plano, a Fase 2 com as primeiras 4 execuções executadas entrará no modo somente leitura.

* As 5 execuções restantes (que estão em estado de rascunho) são movidas para uma nova fase (Fase 3) que é exibida de acordo com o plano recém-carregado.

## Monitorar o plano {#monitor-plan}

Para medir o impacto do seu plano, você pode verificar o desempenho das campanhas de aquecimento de IP usando o [!DNL Journey Optimizer] relatórios de campanha. Para fazer isso, para cada execução concluída, você pode clicar no botão **[!UICONTROL Exibir relatórios]** botão. Saiba mais sobre o email da campanha [relatório ao vivo](../reports/campaign-live-report.md#email-live) e [relatório global](../reports/campaign-global-report.md##email-global).

![](assets/ip-warmup-plan-reports.png)

O próprio plano de aquecimento de IP também serve como um relatório consolidado em um único local. É possível verificar elementos como o número de **[!UICONTROL Ao vivo]** ou **[!UICONTROL Concluído]** O é executado para cada fase e visualizam o andamento de seu plano de aquecimento de IP.

Uma execução pode ter os seguintes status:

* **[!UICONTROL Rascunho]** : sempre que uma execução é criada, quando [criação de um novo plano](ip-warmup-plan.md) ou [adicionar uma execução](#define-runs) a partir da interface do usuário, é necessário **[!UICONTROL Rascunho]** status.
* **[!UICONTROL Ao vivo]**: sempre que você ativar uma execução, será necessário **[!UICONTROL Ao vivo]** status.
* **[!UICONTROL Concluído]**: a execução da campanha para essa execução foi concluída. <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL Cancelado]**: a **[!UICONTROL Ao vivo]** execução foi cancelada usando o **[!UICONTROL Parar]** ou você ativou o botão **[!UICONTROL Pausar para erros]** e ocorreu um erro. [Saiba mais](#define-runs)
* **[!UICONTROL Failed]**: erro encontrado pelo sistema ou a campanha usada para a fase atual foi interrompida. Se uma execução falhar, você poderá programar outra execução para o dia seguinte.
