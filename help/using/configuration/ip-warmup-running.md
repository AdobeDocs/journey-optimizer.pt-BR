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
source-git-commit: 11bdb3ddc666d2025133f70ab522c4ce2d676aa6
workflow-type: tm+mt
source-wordcount: '791'
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

1. Selecione uma hora de término, que define a janela dentro da qual a campanha de aquecimento de IP pode ser executada em caso de atrasos na execução da tarefa de segmentação de público-alvo. Se nenhuma hora de término for especificada, a execução será tentada na hora de início e falhará se a segmentação não tiver sido concluída.

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

## Monitorar o plano

Uma execução pode ter os seguintes status<!--TBC with Medha-->:

* **[!UICONTROL Concluído]**:
* **[!UICONTROL Falha]**:
* **[!UICONTROL Cancelado]**: você interrompeu a execução antes do início da execução da campanha.

Benefícios :

* Os relatórios continuarão a ser exibidos no nível da campanha com recursos semelhantes aos de hoje. Mas o plano de aquecimento de IP também serve como um relatório consolidado em um único local de quantas execuções foram feitas e assim por diante.

* Local único para gerenciar e visualizar como o aquecimento de IP está progredindo.

* Relatório consolidado no nível criativo/de campanha, pois todas as execuções são realizadas em uma fase