---
solution: Journey Optimizer
product: journey optimizer
title: Executar o plano de aquecimento de IP
description: Saiba como executar e monitorar um plano de aquecimento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 1%

---

# Executar o plano de aquecimento de IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* **[Executar o plano de aquecimento de IP](ip-warmup-running.md)**

>[!ENDSHADEBOX]

Depois de [um plano de aquecimento de IP foi criado](ip-warmup-plan.md) e fez upload do arquivo preparado com seu consultor de entrega, você pode definir as fases e as execuções em seu plano.

Cada fase corresponde a um período composto por várias execuções, às quais você atribui uma única campanha.

Para cada execução, você tem um determinado número de recipients e agenda quando essa execução será executada.

## Definir as fases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Selecionar públicos das campanhas a serem excluídos"
>abstract="Selecione os públicos-alvo de outras campanhas que deseja excluir da fase atual."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Selecionar grupos de domínio a serem excluídos"
>abstract="Selecione os domínios que deseja excluir da fase atual."

Você precisa associar a campanha e o público-alvo no nível da fase e ativar algumas configurações, conforme necessário, para todas as execuções associadas a uma única campanha/criativa

No nível da fase, o sistema garante que perfis previamente direcionados + novos sejam selecionados E no nível da iteração, o sistema garante que cada execução tenha perfis únicos e que a contagem corresponda ao que está declarado no plano

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

1. No **[!UICONTROL Grupos de domínios excluídos]** selecione os domínios que deseja excluir dessa fase.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Por exemplo, após executar o aquecimento de IP por alguns dias, você percebe que a reputação do ISP com um domínio (ou seja, Adobe) não é boa e deseja resolvê-la sem interromper seu plano de aquecimento de IP. Nesse caso, você pode excluir o grupo de domínio Adobe.

   >[!NOTE]
   >
   >A exclusão de domínio requer uma fase não executada, portanto, talvez seja necessário dividir uma fase em execução para adicionar exclusões. Da mesma forma, se o grupo de domínios não for um grupo de domínios OOTB, será necessário adicionar esse grupo de domínios ao arquivo do Excel, carregá-lo e, em seguida, excluir o domínio.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Você pode adicionar uma fase, se necessário. Ele será adicionado após a última fase atual.

1. Use o **[!UICONTROL Excluir fase]** botão para remover qualquer fase indesejada.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >Não é possível desfazer a variável **[!UICONTROL Excluir]** ação.
   >
   >Se você excluir todas as fases do plano de aquecimento de IP, recomendamos refazer o upload de um plano.

## Definir as execuções {#define-runs}

1. Selecione uma programação para cada execução. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Como opção, selecione a janela dentro da qual a campanha de aquecimento de IP pode ser executada em caso de atrasos na execução do trabalho de segmentação de público-alvo. Se nenhuma hora de término for especificada, a execução será tentada na hora de início e falhará se a segmentação não tiver sido concluída.

1. Ativar cada execução. Certifique-se de agendar um horário com antecedência suficiente para permitir que o trabalho de segmentação seja executado. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Cada execução deve ser ativada pelo menos 12 horas antes da hora real de envio. Caso contrário, a segmentação pode não ser concluída. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Se a execução da campanha não tiver sido iniciada, é possível interromper uma execução.<!--why?-->

   >[!NOTE]
   >
   >Depois que a execução da campanha for iniciada, a variável **[!UICONTROL Parar]** fica indisponível. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Para adicionar uma execução, selecione **[!UICONTROL Adicionar uma execução abaixo]** no ícone de três pontos.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Dividir uma fase {#split-phase}

A qualquer momento, se quiser usar uma campanha diferente a partir de uma execução específica, selecione a **[!UICONTROL Opção Dividir para uma nova fase]** no ícone de três pontos.

Uma nova fase é criada para as execuções restantes da fase atual. Siga as etapas [acima](#define-phases) para definir a nova fase.

Por exemplo, se você selecionar esta opção para Run #4, Runs #4 to #8 será movido para uma nova fase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Marcar um plano como concluído {#mark-as-completed}

Se seu plano não estiver funcionando bem o suficiente ou se você quiser descartá-lo para criar outro, poderá marcá-lo como concluído.

Para fazer isso, clique no link **[!UICONTROL Mais]** no canto superior direito, registre o plano de aquecimento de IP e selecione **[!UICONTROL Marcar como concluído]**.

![](assets/ip-warmup-plan-mark-completed.png)

Essa opção só estará disponível se todas as execuções no plano estiverem em **[!UICONTROL Com êxito]** ou **[!UICONTROL Rascunho]** status. Nenhuma execução pode ser **[!UICONTROL Ao vivo]**.

Os diferentes status de execução são listados em [nesta seção](#monitor-plan).

## Monitorar o plano {#monitor-plan}

Para medir o impacto do seu plano, você pode verificar o desempenho de suas campanhas de aquecimento de IP usando relatórios. Saiba mais sobre o email da campanha [relatório ao vivo](../reports/campaign-live-report.md#email-live) e [relatório global](../reports/campaign-global-report.md##email-global).

O próprio plano de aquecimento de IP também serve como um relatório consolidado em um único local. É possível verificar elementos como o número de **[!UICONTROL Ao vivo]** ou **[!UICONTROL Com êxito]** O é executado para cada fase e visualizam o andamento de seu plano de aquecimento de IP.

Uma execução pode ter os seguintes status:

* **[!UICONTROL Rascunho]** : sempre que uma execução é criada, quando [fazendo upload de um novo plano](ip-warmup-plan.md) ou [adicionar uma execução](#define-runs) a partir da interface do usuário, é necessário **[!UICONTROL Rascunho]** status.
* **[!UICONTROL Ao vivo]**: sempre que você ativar uma execução, será necessário **[!UICONTROL Ao vivo]** status.
* **[!UICONTROL Com êxito]**<!--TBC-->: a execução da campanha para essa execução foi concluída. <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL Cancelado]**: a **[!UICONTROL Ao vivo]** execução foi cancelada usando o **[!UICONTROL Parar]** botão. Esse botão só estará disponível se a execução da campanha não tiver sido iniciada. [Saiba mais](#define-runs)
* **[!UICONTROL Failed]**: erro encontrado pelo sistema ou a campanha usada para a fase atual foi interrompida<!--what should the user do in that case?-->.
