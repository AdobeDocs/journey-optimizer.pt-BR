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
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 48a0fb11c141d847fae444909a7e6080e4a4935a
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 11%

---

# Criar um experimento de conteúdo {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de conteúdo"
>abstract="É possível optar por variar o conteúdo, o assunto ou o remetente da mensagem para definir vários tratamentos e determinar a melhor combinação para os públicos-alvo."

>[!NOTE]
>
>Antes de começar com o Experimento de conteúdo, verifique se a configuração de relatórios está definida para seus conjuntos de dados personalizados. Saiba mais [nesta seção](reporting-configuration.md).

O Experimento de conteúdo do Journey Optimizer permite definir vários tratamentos de delivery para medir qual tem melhor desempenho para o público-alvo. Você pode optar por variar o conteúdo do delivery, o assunto ou o remetente. O público-alvo de interesse é alocado aleatoriamente para cada tratamento para determinar qual funciona melhor em termos da métrica especificada.

No exemplo abaixo, o target do delivery foi dividido em dois grupos, cada um representando 45% da população direcionada, e um grupo de controle de 10%, que não receberá o delivery.

Cada pessoa no público-alvo receberá uma versão de um email, com uma linha de assunto que é uma das duas a seguir:

* uma promovendo diretamente uma oferta de 10% na nova coleção e uma imagem.
* a outra só anuncia uma oferta especial sem especificar os 10% de desconto sem nenhuma imagem.

O objetivo aqui é ver se os recipients interagirão com o email dependendo do experimento recebido. Portanto, escolheremos **[!UICONTROL Aberturas de email]** como a principal métrica de meta neste Experimento de conteúdo.

![](assets/content_experiment.png)

## Criar sua campanha {#campaign-experiment}

1. No **[!UICONTROL Campanhas]** clique em **[!UICONTROL Criar campanha]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. Selecione o canal e depois o **[!UICONTROL Superficial]** que deseja usar para esse delivery e clique em **[!UICONTROL Criar]**. Para obter mais informações, consulte [Superfícies de canal](../configuration/channel-surfaces.md) página.

   Neste exemplo, optamos por enviar uma campanha usando emails.

   ![](assets/content_experiment_2.png)

1. Configurar o **[!UICONTROL Propriedades]** do seu delivery:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Descrição]**

1. Defina o público-alvo para o target. Para fazer isso, clique no link **[!UICONTROL Selecionar público]** botão para exibir a lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais sobre públicos](../audience/about-audiences.md)

   No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do público-alvo selecionado. [Saiba mais](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. No **[!UICONTROL Rastreamento de ações]** especifique se deseja rastrear como os recipients reagem ao seu delivery: é possível rastrear cliques e/ou aberturas.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha.

1. Para executar sua campanha em uma data específica ou em uma frequência recorrente, configure o **[!UICONTROL Agendar]** seção. [Saiba mais](create-campaign.md)

1. Clique em **[!UICONTROL Editar conteúdo]** para começar a personalizar o delivery.

   ![](assets/content_experiment_17.png)

1. No **[!UICONTROL Editar conteúdo]** , comece a personalizar o tratamento A.

   Para esse tratamento, especificaremos a oferta especial diretamente na linha de assunto e adicionaremos personalização.

   ![](assets/content_experiment_5.png)

## Configurar seu experimento de conteúdo {#configure-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_dimension"
>title="Dimensão"
>abstract="Escolha a dimensão específica a ser rastreada para o seu experimento, como certos cliques ou visualizações de determinadas páginas."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_success_metric"
>title="Métrica de sucesso"
>abstract="A métrica de sucesso é usada para rastrear e avaliar o tratamento com melhor desempenho em um experimento. Certifique-se de configurar seu conjunto de dados para determinadas métricas antes de usá-lo."

1. Quando a mensagem for personalizada, na página de resumo da campanha, clique em **[!UICONTROL Criar experimento]** para configurar seu experimento de conteúdo.

   ![](assets/content_experiment_3.png)

1. Selecione o **[!UICONTROL Métrica de sucesso]** que deseja definir para o experimento.

   Para este exemplo, selecione **[!UICONTROL Email aberto]** para testar se os perfis abrem seus emails se o código promocional estiver na linha de assunto.

   ![](assets/content_experiment_11.png)

1. Ao configurar um experimento usando o canal no aplicativo ou na Web e escolher o **[!UICONTROL Cliques de entrada]**, **[!UICONTROL Cliques de entrada únicos]** , **[!UICONTROL Exibições de página]** ou **[!UICONTROL Métricas de Visualizações de página únicas]** , o **[!UICONTROL Ação do clique]**  permite rastrear e monitorar com precisão os cliques e as exibições em páginas específicas.

   ![](assets/content_experiment_20.png)

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

Depois de configurar sua experimentação e campanha, você pode acompanhar o sucesso do delivery com o relatório Campanha. [Saiba mais](../reports/campaign-global-report.md#experimentation-report)
