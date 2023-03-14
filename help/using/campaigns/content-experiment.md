---
solution: Journey Optimizer
product: journey optimizer
title: Criar um experimento de conteúdo
description: Saiba como criar um experimento de conteúdo em suas campanhas
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, vários, público-alvo, tratamento
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 5%

---

# Criar um experimento de conteúdo {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de conteúdo"
>abstract="Você pode optar por variar o conteúdo, o assunto ou o remetente do delivery para definir vários tratamentos e determinar a melhor combinação para seus públicos."

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao experimento de conteúdo](get-started-experiment.md)
* **[Criar um experimento de conteúdo](content-experiment.md)**
* [Compreender cálculos estatísticos](experiment-calculations.md)
* [Configurar relatórios de experimentação](reporting-configuration.md)
* [Cálculos estatísticos no relatório de Experimentação](experiment-report-calculations.md)

>[!ENDSHADEBOX]

O Experimento de conteúdo do Journey Optimizer permite definir vários tratamentos de delivery para medir qual tem melhor desempenho para o público-alvo. Você pode optar por variar o conteúdo do delivery, o assunto ou o remetente. O público-alvo de interesse é alocado aleatoriamente para cada tratamento para determinar qual funciona melhor em termos da métrica especificada.

>[!NOTE]
>
>Antes de começar com o Experimento de conteúdo, verifique se a configuração de relatórios está definida para seus conjuntos de dados personalizados. Saiba mais [nesta seção](reporting-configuration.md).

No exemplo abaixo, o target do delivery foi dividido em dois grupos, cada um representando 45% da população direcionada, e um grupo de controle de 10%, que não receberá o delivery.

Cada pessoa no público-alvo receberá uma versão de um email, com uma linha de assunto que é uma das duas a seguir:

* uma promovendo diretamente uma oferta de 10% na nova coleção e uma imagem.
* a outra só anuncia uma oferta especial sem especificar os 10% de desconto sem nenhuma imagem.

O objetivo aqui é ver se os recipients interagirão com o email dependendo do experimento recebido. Portanto, escolheremos **[!UICONTROL Aberturas de email]** como a principal métrica de meta neste Experimento de conteúdo.

![](assets/content_experiment.png)

## Criar sua campanha {#campaign-experiment}

1. No **[!UICONTROL Campanhas]** clique em **[!UICONTROL Criar campanha]**.

   ![](assets/content_experiment_1.png)

1. Selecione o canal e depois o **[!UICONTROL Superficial]** que deseja usar para esse delivery e clique em **[!UICONTROL Criar]**. Para obter mais informações, consulte [Superfícies de canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Configurar o **[!UICONTROL Propriedades]** do seu delivery:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Descrição]**

1. Defina o público-alvo para o target. Para fazer isso, clique no link **[!UICONTROL Selecionar público]** botão para exibir a lista de segmentos do Adobe Experience Platform disponíveis. [Saiba mais sobre segmentos](../segment/about-segments.md)

   No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. No **[!UICONTROL Rastreamento de ações]** especifique se deseja rastrear como seus recipients reagem ao seu delivery: é possível rastrear cliques e/ou aberturas.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha.

1. Para executar sua campanha em uma data específica ou em uma frequência recorrente, configure o **[!UICONTROL Agendar]** seção. [Saiba mais](create-campaign.md)

1. Clique em **[!UICONTROL Editar conteúdo]** para começar a personalizar o delivery. [Saiba mais](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. No **[!UICONTROL Editar conteúdo]** , comece a personalizar o tratamento A.

   Para esse tratamento, especificaremos a oferta especial diretamente na linha de assunto e adicionaremos personalização.

   ![](assets/content_experiment_5.png)

## Configurar seu experimento de conteúdo {#configure-experiment}

1. Quando o delivery for personalizado, na página Campaign summary, clique em **[!UICONTROL Criar experimento]** para configurar seu experimento de conteúdo.

   ![](assets/content_experiment_3.png)

1. Selecione o **[!UICONTROL Métrica de sucesso]** que deseja definir para o experimento.

   Para nosso experimento, selecionamos **[!UICONTROL Email aberto]** para testar se os recipients abrirão seus emails se o código promocional estiver na linha de assunto.

   ![](assets/content_experiment_11.png)

1. Clique em **[!UICONTROL Adicionar tratamento]** para criar quantos novos tratamentos forem necessários.

   ![](assets/content_experiment_8.png)

1. Altere o **[!UICONTROL Título]** do seu tratamento para diferenciá-los melhor.

1. Escolha adicionar um **[!UICONTROL Retenção]** grupo para o seu delivery. Este grupo não receberá nenhum conteúdo desta campanha.

   Se você ativar a barra de alternância ocupará automaticamente 10% da sua população, é possível ajustar essa porcentagem, se necessário.

   ![](assets/content_experiment_12.png)

1. Em seguida, é possível optar por alocar uma porcentagem precisa para cada **[!UICONTROL Tratamento]** ou simplesmente ligue o **[!UICONTROL Distribuir uniformemente]** barra de alternância.

   ![](assets/content_experiment_13.png)

1. Clique em **[!UICONTROL Criar]** quando sua configuração é definida.

## Projetar seus tratamentos {#treatment-experiment}

1. No **[!UICONTROL Editar conteúdo]** selecione seu tratamento B para alterar o conteúdo.

   Aqui, optamos por não especificar a oferta no **[!UICONTROL Linha de assunto]**.

   ![](assets/content_experiment_18.png)

1. Clique em **[!UICONTROL Editar corpo do email]** para personalizar ainda mais seu tratamento B.

   ![](assets/content_experiment_9.png)

1. Após criar o tratamento, clique em **[!UICONTROL Mais ações]** para acessar as opções relacionadas aos seus tratamentos: **[!UICONTROL Renomear]**, **[!UICONTROL Duplicar]** e **[!UICONTROL Excluir]**.

   ![](assets/content_experiment_7.png)

1. Se necessário, acesse o **[!UICONTROL Configurações de experimento]** para alterar a configuração de tratamentos.

   ![](assets/content_experiment_19.png)

1. Após definir o conteúdo da mensagem, clique no link **[!UICONTROL Simular conteúdo]** para controlar a renderização do delivery e verificar as configurações de personalização com perfis de teste. [Saiba mais](../email/preview.md)

1. Quando o experimento de conteúdo estiver pronto, na página de resumo da campanha, você pode clicar em **[!UICONTROL Revisar para ativar]** para exibir um resumo da campanha. Os alertas são exibidos se qualquer parâmetro estiver incorreto ou ausente.

   ![](assets/content_experiment_15.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Ativar]** para iniciá-lo.

   ![](assets/content_experiment_14.png)

Depois de configurar sua experimentação e campanha, você pode acompanhar o sucesso do delivery com o relatório Campanha.

## Relatório de objetivos {#objectives-global}

>[!AVAILABILITY]
>
>No momento, o recurso de experimento de conteúdo está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/performance_report.gif)

A variável **[!UICONTROL Objetivos]** permite ajustar melhor os relatórios dos deliveries ao direcionar uma métrica específica.

A variável **[!UICONTROL Objetivos]** listadas estão vinculadas a **[!UICONTROL Conjuntos de dados]** que definem uma conexão com um sistema para recuperar informações adicionais. Uma lista de componentes integrados **[!UICONTROL Objetivos]** está disponível, mas você pode adicionar a sua própria adicionando novas **[!UICONTROL Conjunto de dados]**. Para obter o procedimento detalhado, consulte este [seção](reporting-configuration.md).

Após selecionar os objetivos que deseja direcionar, os dois **[!UICONTROL Visão geral do desempenho]** e **[!UICONTROL Objetivo da campanha]** Os widgets fornecerão um resumo detalhado do desempenho do seu delivery.

Com o **[!UICONTROL Objetivo da campanha]** , você também pode optar por comparar seu objetivo principal com outra métrica.

Observe que cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/global-report.md#modify-dashboard).

## Relatório de experimentação {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de sucesso"
>abstract="O valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis."

>[!AVAILABILITY]
>
>No momento, o recurso de experimento de conteúdo está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/experimentation_report_3.png)

Da sua campanha **[!UICONTROL Relatório global]**, o **[!UICONTROL Experimentação]** A guia detalha as principais informações relacionadas ao desempenho de cada variante e se há um melhor desempenho.

Observe que a definição do melhor desempenho pode levar algum tempo. Ela será representada por esse ícone ![](assets/experimentation_report_1.png).

A variável **[!UICONTROL Resultado do experimento]** o widget detalha o desempenho de cada variante. Você pode alterar sua linha de base selecionando um dos tratamentos nas **[!UICONTROL Linha de base]** o menu suspenso. O melhor tratamento será representado com um ícone de estrela.

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Perfis]**: Número de perfis direcionados para este tratamento.

* **[!UICONTROL Cliques de saída únicos]**: Contagem total de cliques nos canais de saída.

* **[!UICONTROL Contagem por perfil]**: Valor total da métrica do objetivo do experimento dividido pelo número de perfis.

* **[!UICONTROL Intervalo de confiança]**: Diferença percentual de desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Aumento médio]**: melhora percentual na taxa de conversão de um determinado tratamento em relação à linha de base. [Saiba mais](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é igual ao tratamento inicial. [Saiba mais](../campaigns/experiment-calculations.md#understand-confidence)

Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
