---
solution: Journey Optimizer
product: journey optimizer
title: Criar um experimento de conteúdo
description: Saiba como criar um experimento de conteúdo em suas campanhas
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, múltiplo, público-alvo, tratamento
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informative"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 9%

---

# Criar um experimento de conteúdo {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de conteúdo"
>abstract="Você pode optar por variar o conteúdo, o assunto ou o remetente da entrega para definir vários tratamentos de entrega e determinar a melhor combinação para os públicos."

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao experimento de conteúdo](get-started-experiment.md)
* **[Criar um experimento de conteúdo](content-experiment.md)**
* [Compreender cálculos estatísticos](experiment-calculations.md)
* [Configurar relatórios de experimentação](reporting-configuration.md)
* [Cálculos estatísticos no relatório de Experimentação](experiment-report-calculations.md)

>[!ENDSHADEBOX]

O Experimento de conteúdo do Journey Optimizer permite definir vários tratamentos de delivery para medir qual deles tem melhor desempenho para o público-alvo. Você pode optar por variar o conteúdo, o assunto ou o remetente do delivery. O público-alvo de interesse é alocado aleatoriamente para cada tratamento para determinar qual funciona melhor em termos da métrica especificada.

>[!NOTE]
>
>Antes de começar com o Experimento de conteúdo, verifique se a configuração de relatório está definida para seus conjuntos de dados personalizados. Saiba mais [nesta seção](reporting-configuration.md).

No exemplo abaixo, o target do delivery foi dividido em dois grupos, cada um representando 45% da população direcionada, e um grupo de espera de 10%, que não receberá o delivery.

Cada pessoa no público-alvo receberá uma versão de um email, com uma linha de assunto que é uma das duas seguintes:

* uma promovendo diretamente uma oferta de 10% na nova coleção e uma imagem.
* o outro apenas anuncia uma oferta especial sem especificar 10% de desconto sem nenhuma imagem.

O objetivo aqui é ver se os recipients interagem com o email, dependendo do experimento recebido. Por conseguinte, escolheremos **[!UICONTROL Aberturas de email]** como a principal métrica de meta neste Experimento de conteúdo.

![](assets/content_experiment.png)

## Criar sua campanha {#campaign-experiment}

1. No **[!UICONTROL Campanhas]** página, clique em **[!UICONTROL Criar campanha]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. Selecione seu canal e depois o **[!UICONTROL Superfície]** você deseja usar para este delivery e clique em **[!UICONTROL Criar]**. Para obter mais informações, consulte [Superfícies do canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Configure o **[!UICONTROL Propriedades]** do seu delivery:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Descrição]**

1. Defina o público-alvo como meta. Para fazer isso, clique no botão **[!UICONTROL Seleção do público-alvo]** para exibir a lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais sobre segmentos](../segment/about-segments.md)

   No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. No **[!UICONTROL Rastreamento de ações]** , especifique se deseja rastrear como os recipients reagem ao seu delivery: você pode rastrear cliques e/ou aberturas.

   Os resultados do rastreamento serão acessíveis no relatório da campanha após a execução da campanha.

1. Para executar sua campanha em uma data específica ou em uma frequência recorrente, configure a variável **[!UICONTROL Agendar]** seção. [Saiba mais](create-campaign.md)

1. Clique em **[!UICONTROL Editar conteúdo]** para começar a personalizar o delivery. [Saiba mais](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. No **[!UICONTROL Editar conteúdo]** , comece a personalizar o tratamento A.

   Para esse tratamento, especificaremos a oferta especial diretamente na linha de assunto e adicionaremos a personalização.

   ![](assets/content_experiment_5.png)

## Configurar o experimento de conteúdo {#configure-experiment}

1. Quando o delivery for personalizado, na página Campaign summary , clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo.

   ![](assets/content_experiment_3.png)

1. Selecione o **[!UICONTROL Métrica de sucesso]** você quer definir para o seu experimento.

   Para nosso experimento, selecionamos **[!UICONTROL Abertura de email]** para testar se os recipients abrirão seus emails se o código promocional estiver na linha de assunto.

   ![](assets/content_experiment_11.png)

1. Clique em **[!UICONTROL Adicionar tratamento]** para criar quantos novos tratamentos forem necessários.

   ![](assets/content_experiment_8.png)

1. Altere o **[!UICONTROL Título]** do seu tratamento para os diferenciar melhor.

1. Escolha adicionar um **[!UICONTROL Retenção]** ao seu delivery. Este grupo não receberá nenhum conteúdo desta campanha.

   Ao ativar a barra de alternância, serão automaticamente necessários 10% de sua população. Você pode ajustar essa porcentagem se necessário.

   ![](assets/content_experiment_12.png)

1. Você pode optar por alocar uma porcentagem precisa para cada **[!UICONTROL Tratamento]** ou simplesmente ative a **[!UICONTROL Distribuir uniformemente]** barra de alternância.

   ![](assets/content_experiment_13.png)

1. Clique em **[!UICONTROL Criar]** quando sua configuração for definida.

## Projetar os tratamentos {#treatment-experiment}

1. No **[!UICONTROL Editar conteúdo]** selecione o tratamento B para alterar o conteúdo.

   Aqui, optamos por não especificar a oferta na variável **[!UICONTROL Linha de assunto]**.

   ![](assets/content_experiment_18.png)

1. Clique em **[!UICONTROL Editar corpo do email]** para personalizar ainda mais o tratamento B.

   ![](assets/content_experiment_9.png)

1. Depois de criar seus tratamentos, clique em **[!UICONTROL Mais ações]** para acessar opções relacionadas aos seus tratamentos: **[!UICONTROL Renomear]**, **[!UICONTROL Duplicar]** e **[!UICONTROL Excluir]**.

   ![](assets/content_experiment_7.png)

1. Se necessário, acesse o **[!UICONTROL Configurações do experimento]** para alterar a configuração dos tratamentos.

   ![](assets/content_experiment_19.png)

1. Depois que o conteúdo da mensagem for definido, clique no link **[!UICONTROL Simular conteúdo]** para controlar a renderização do delivery e verificar as configurações de personalização com perfis de teste. [Saiba mais](../email/preview.md)

1. Quando seu experimento de conteúdo estiver pronto, na página de resumo do Campaign, você pode clicar em **[!UICONTROL Revisar para ativar]** para exibir um resumo da campanha. Os alertas são exibidos se qualquer parâmetro estiver incorreto ou ausente.

   ![](assets/content_experiment_15.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Ativar]** para iniciá-lo.

   ![](assets/content_experiment_14.png)

Após configurar sua experimentação e campanha, você pode seguir o sucesso de seu delivery com o relatório Campanha .

## Relatório de objetivos {#objectives-global}

>[!AVAILABILITY]
>
>O recurso de Experiência de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/performance_report.gif)

O **[!UICONTROL Objetivos]** A guia do relatório Campanha permite ajustar melhor os relatórios dos deliveries, direcionando uma métrica específica.

O **[!UICONTROL Objetivos]** listadas estão vinculadas a **[!UICONTROL Conjuntos de dados]** que definem uma conexão com um sistema para recuperar informações adicionais. Uma lista de **[!UICONTROL Objetivos]** está disponível, mas você pode adicionar o seu ao adicionar novo **[!UICONTROL Conjunto de dados]**. Para obter o procedimento detalhado, consulte este [seção](reporting-configuration.md).

Após selecionar os Objetivos que deseja definir como meta, os dois **[!UICONTROL Visão geral do desempenho]** e **[!UICONTROL Objetivo da campanha]** os widgets fornecerão um resumo detalhado do desempenho do seu delivery.

Com o **[!UICONTROL Objetivo da campanha]** no widget, você também pode optar por comparar seu objetivo principal com outra métrica.

Observe que cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações sobre isso, consulte esta seção [seção](../reports/global-report.md#modify-dashboard).

## Relatório de experiência {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de sucesso"
>abstract="O valor total da métrica sucesso, anteriormente selecionado ao criar seus experimentos, dividido pelo número de perfis."

>[!AVAILABILITY]
>
>O recurso de Experiência de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/experimentation_report_3.png)

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Experimentação]** detalha as informações principais sobre o desempenho de cada variante e se há um melhor desempenho.

Observe que a definição do melhor desempenho pode levar algum tempo, ele será representado por este ícone ![](assets/experimentation_report_1.png).

O **[!UICONTROL Resultado do experimento]** O widget detalha o desempenho de cada variante. Pode alterar o seu valor basal selecionando um dos tratamentos na **[!UICONTROL Linha de base]** o menu suspenso. O melhor tratamento será representado com um ícone de estrela.

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Perfis]**: Número de perfis direcionados para este tratamento.

* **[!UICONTROL Cliques de saída exclusivos]**: Contagem total de cliques em canais de saída.

* **[!UICONTROL Contagem por perfil]**: O valor total da métrica de objetivo do Experimento dividido pelo número de perfis.

* **[!UICONTROL Intervalo de confiança]**: Diferença percentual no desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Aumento médio]**: Melhoria da percentagem na taxa de conversão de um determinado tratamento em relação ao valor basal. [Saiba mais](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é o mesmo que o tratamento inicial. [Saiba mais](../campaigns/experiment-calculations.md#understand-confidence)

Para detalhar esses resultados e como interpretá-los, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
