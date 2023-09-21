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
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '809'
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

1. Para cada fase, aplica-se o seguinte:

   * **[!UICONTROL Exclusão de perfil]** - Os perfis das execuções anteriores dessa fase são sempre excluídos. Por exemplo, se na corrida #1 Leo foi coberto nas primeiras 6300 pessoas que estão sendo alvo, o sistema irá automaticamente garantir que Leo não receba o e-mail na execução #2.

   * **[!UICONTROL Públicos-alvo de campanha excluídos]** - Selecione os públicos-alvo de outros <!--executed/live?-->campanhas que você deseja excluir da fase atual.

     Por exemplo, talvez você esteja executando uma fase e tenha que dividi-la por qualquer motivo. Nesse caso, na fase 2, você gostaria de incluir a campanha usada na fase 1 nesta seção para que, na fase 2, as pessoas contatadas anteriormente da fase 1 não sejam incluídas. Isso pode ser feito não apenas com campanhas usadas no mesmo plano de aquecimento de IP, mas também de outro plano de aquecimento de IP.

   * **[!UICONTROL Grupos de domínios excluídos]** - Selecione os domínios que deseja excluir dessa fase, por exemplo, Gmail. <!--??-->

     Depois de executar o aquecimento de IP por alguns dias, você percebe que a reputação do ISP com um domínio diz que o hotmail não é bom e deseja resolvê-lo com o ISP, mas não deseja interromper o plano de aquecimento de IP. Nesse caso, você pode colocar o grupo de domínio hotmail na categoria excluída.

     >[!NOTE]
     >
     >A exclusão de domínio requer uma fase não executada, portanto, talvez seja necessário dividir uma fase em execução para adicionar exclusões. Da mesma forma, se o grupo de domínio não for um grupo de domínio OOTB, talvez seja necessário criar um grupo de domínio no Excel e carregá-lo e, em seguida, excluí-lo.

   ![](assets/ip-warmup-plan-phase-1.png)

1. É possível adicionar uma fase, se necessário. Ela será adicionada após a última fase atual. Use o **[!UICONTROL Excluir fase]** botão para remover qualquer fase indesejada.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >Não é possível desfazer a variável **[!UICONTROL Excluir]** ação.
   >
   >Se você excluir todas as fases do plano de aquecimento de IP, recomendamos refazer o upload de um plano.

## Definir as execuções {#define-runs}

1. Selecione uma programação para cada execução. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Selecione uma hora de término, que basicamente significa a janela dentro da qual podemos executar a campanha de aquecimento caso haja atrasos no trabalho do público-alvo. Se não for especificado, tentaremos na hora de início e falharemos. Se a hora de término for fornecida, executaremos a execução entre essa janela.

1. Ativar cada execução. Certifique-se de agendar um horário com antecedência suficiente para permitir que o trabalho de segmentação seja executado. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Cada execução deve ser ativada pelo menos 12 horas antes da hora real de envio. Caso contrário, a segmentação pode não ser concluída. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Se a execução da campanha não tiver sido iniciada, é possível interromper uma execução.<!--why?-->

   Depois que a execução da campanha for iniciada, a variável **[!UICONTROL Parar]** fica indisponível. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Para adicionar uma execução, selecione **[!UICONTROL Adicionar uma execução abaixo]** no ícone de três pontos.

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. A qualquer momento, se quiser usar uma campanha diferente a partir de uma execução específica, selecione a **[!UICONTROL Opção Dividir para uma nova fase]** no ícone de três pontos. Uma nova fase é criada para as execuções restantes da fase atual. Siga as etapas [acima](#define-phases) para definir a nova fase.

   Por exemplo, se você selecionar essa opção para executar #4, as execuções de #4 para #8 serão movidas para uma nova fase.

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