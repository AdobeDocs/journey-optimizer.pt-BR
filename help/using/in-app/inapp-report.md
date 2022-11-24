---
title: Relatório no aplicativo
description: Saiba como usar dados do relatório no aplicativo
feature: Reporting
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3d496efc-1bf9-4895-906c-3757f92c6fe3
source-git-commit: 3f43cfac56e4665dc16ce24e9736bcfcd3c544bf
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 3%

---

# Relatório no aplicativo {#inapp-report}

O Relatório no aplicativo está disponível no relatório Campanha .

A página Relatório da campanha será exibida com as seguintes guias:

* [Campaign](../reports/campaign-global-report.md#campaign-live)
* [Email](../reports/campaign-global-report.md#email-live)
* [Push](../reports/campaign-global-report.md#push-live)
* [SMS](../reports/campaign-global-report.md#sms-live)
* [No aplicativo](#in-app-global)

A campanha **[!UICONTROL Relatório global]** O é dividido em diferentes widgets detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/global-report.md#modify-dashboard).

Para obter uma lista detalhada de todas as métricas disponíveis no Adobe Journey Optimizer, consulte [esta página](../reports/global-report.md#list-of-components-global.md)

## Guia No aplicativo {#inapp-global}

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL No aplicativo]** detalha as informações principais relativas aos deliveries no aplicativo enviados na campanha.

![](assets/campaign_report_global_6.png)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório no aplicativo.

O **[!UICONTROL Desempenho no aplicativo]** Os KPIs detalham as principais informações relativas ao envolvimento de seus visitantes com suas mensagens no aplicativo, como:

* **[!UICONTROL Impressões únicas]**: número de usuários únicos para os quais a mensagem no aplicativo foi entregue.

* **[!UICONTROL Impressões]**: número total de mensagens no aplicativo entregues a todos os usuários.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que visualizaram a mensagem.

* **[!UICONTROL Taxa de rejeição]**: porcentagem de mensagens no aplicativo que os recipients rejeitaram.

O **[!UICONTROL Resumo no aplicativo]** gráfico mostra a evolução de suas impressões no aplicativo para o período relacionado.

O **[!UICONTROL Cliques por botão]** gráfico e tabela contêm os dados disponíveis para o comportamento do recipient por botão:

* **[!UICONTROL Cliques]**: número total de recipients que interagiram com os botões incluídos na mensagem no aplicativo.

* **[!UICONTROL Taxa de cliques]**: porcentagem de usuários que interagiram com os botões incluídos na mensagem no aplicativo em comparação aos usuários que visualizaram a mensagem.
+++

**Tópicos relacionados:**

* [Criar mensagem no aplicativo](../in-app/create-in-app.md)
* [Criar mensagem no aplicativo](../in-app/design-in-app.md)
* [Configuração no aplicativo](../in-app/inapp-configuration.md)


>[!BEGINTABS]

>[!TAB Adicionar um push a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.

>[!TAB Adicionar um push a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha.

1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua notificação por push:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mensalmente

>[!ENDTABS]

Teste 2:

1. Este é um teste

>[!BEGINTABS]

    >[!TAB Adicionar um push a uma Jornada]
    
    1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.
    
    1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.
    
    >[!TAB Adicionar um push a uma campanha]
    
    1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.
    
    1. Clique em **[!UICONTROL Criar]**.
    
    1. No **[!UICONTROL Propriedades]**, edite o ** de sua campanha[!UICONTROL Título]** e **[!UICONTROL Descrição]**.
    
    1. Clique no **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.
    
    1. No **[!UICONTROL Namespace de identidade]**, escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.
    
    1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha.
    
    1. No **[!UICONTROL Acionadores de ação]**, escolha o menu **[!UICONTROL Frequência]** da sua notificação por push:
    
    * Uma vez
    * Diariamente
    * Semanalmente
    * Mensal

>[!ENDTABS]

1. Isso faz parte do teste

Teste 3:

1. Este é um teste

   >[!BEGINTABS]

   >[!TAB Adicionar um push a uma Jornada]

   1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.

   1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.
   >[!TAB Adicionar um push a uma campanha]

   1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.

   1. Clique em **[!UICONTROL Criar]**.

   1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

   1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.

   1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

   1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha.

   1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua notificação por push:

      * Uma vez
      * Diariamente
      * Semanalmente
      * Mensalmente

   >[!ENDTABS]

1. Isso faz parte do teste

Teste 3:

1. Este é um teste

>[!BEGINTABS]

>[!TAB Adicionar um push a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.

>[!TAB Adicionar um push a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha.

1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua notificação por push:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mensalmente

>[!ENDTABS]

1. Isso faz parte do teste
