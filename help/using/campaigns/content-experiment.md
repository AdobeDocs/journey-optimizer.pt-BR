---
title: Criar um experimento de conteúdo
description: Saiba como criar um experimento de conteúdo em suas campanhas
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 0fb54571ea7620c981e746f8ac240b675e2f0d64
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---

# Criar um experimento de conteúdo {#content-experiment}

>[!AVAILABILITY]
>
>O recurso de Experiência de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

O recurso de experimento de conteúdo permite definir vários tratamentos de delivery. O público-alvo de interesse é alocado aleatoriamente para cada tratamento a fim de determinar qual delas tem melhor desempenho em relação à métrica de interesse. Você pode optar por variar o conteúdo, o assunto ou o remetente do email.

No exemplo abaixo, o target do delivery foi dividido em dois grupos, cada um representando 45% da população direcionada, e um grupo de espera de 10%, que não receberá o delivery.

Cada pessoa no público-alvo receberá uma versão do email, com uma linha de assunto que é uma das duas seguintes:

* uma promovendo diretamente uma oferta de 10% na nova coleção e uma imagem.
* o outro apenas anuncia uma oferta especial sem especificar 10% de desconto sem nenhuma imagem.

O objetivo aqui é ver se os recipients interagem com o email, dependendo do experimento recebido. Por conseguinte, escolheremos **[!UICONTROL Email Opens]** como a principal métrica de meta neste Experimento de conteúdo.

![](assets/content_experiment.png)

## Criar sua campanha {#campaign-experiment}

1. No **[!UICONTROL Campaigns]** página, clique em **[!UICONTROL Create Campaign]**.

   ![](assets/content_experiment_1.png)

1. Selecionar **[!UICONTROL Email]** em seguida, **[!UICONTROL Surface]** você deseja usar para este delivery. Para obter mais informações, consulte [Superfícies do canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Clique em **[!UICONTROL Create]**.

1. Configure o **[!UICONTROL Properties]** do seu delivery:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Para iniciar seu experimento de conteúdo, alterne a **[!UICONTROL Content experiment]** opção. O **[!UICONTROL Content experiment]** será exibido.

   ![](assets/content_experiment_3.png)

1. Configure o **[!UICONTROL Audience]** e **[!UICONTROL Schedule]** parâmetros para seus deliveries. [Saiba mais](create-campaign.md)

1. Clique em **[!UICONTROL Edit content]** para começar a personalizar seus diferentes **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Crie seus tratamentos {#treatment-experiment}

1. No **[!UICONTROL Edit content]** , adicione a **[!UICONTROL Subject line]** para o seu Tratamento Um e-mail e clique em **[!UICONTROL Save]**.

   Para esse tratamento, especificamos a oferta diretamente na linha de assunto.

   ![](assets/content_experiment_5.png)

1. Clique em **[!UICONTROL Email designer]** para começar a personalizar seus deliveries.

   ![](assets/content_experiment_6.png)

1. Depois de criar o email, clique em **[!UICONTROL Save]** e voltar ao **[!UICONTROL Edit content]** para criar o Tratamento B.

1. No **[!UICONTROL More actions]** , clique em **[!UICONTROL Duplicate]**.

   Você também pode optar por iniciar um novo tratamento clicando no botão **[!UICONTROL Content experiment]** para acessar as opções avançadas e **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Altere o **[!UICONTROL Title]** do seu tratamento para os diferenciar melhor.

   ![](assets/content_experiment_8.png)

1. Selecione o delivery de email vinculado ao seu **[!UICONTROL Treatment]**.

1. Adicione o **[!UICONTROL Subject line]** para o seu delivery.

   Para esse tratamento, optamos por não especificar a oferta no **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

1. Clique em **[!UICONTROL Email designer]** para personalizar ainda mais o delivery de Tratamento B, se necessário.

Depois que seus tratamentos forem personalizados, você poderá começar a configurar seu experimento de conteúdo.

## Configurar o experimento de conteúdo {#configure-experiment}

1. Quando ambos os deliveries são personalizados, na variável **[!UICONTROL Edit content]** janela , selecione **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Selecione os objetivos que deseja definir para o seu experimento.

   Para nosso experimento, selecionamos **[!UICONTROL Email open]** para testar se os recipients abrirão seus emails se o código promocional estiver na linha de assunto.

   ![](assets/content_experiment_11.png)

1. Escolha adicionar um **[!UICONTROL Holdout]** ao seu delivery. Este grupo não receberá nenhum conteúdo desta campanha.

   Ao ativar a barra de alternância, serão automaticamente necessários 10% de sua população. Você pode ajustar essa porcentagem se necessário.

   ![](assets/content_experiment_12.png)

1. Você pode optar por alocar uma porcentagem precisa para cada **[!UICONTROL Treatment]** ou simplesmente ative a **[!UICONTROL Distribute evenly]** barra de alternância.

   ![](assets/content_experiment_13.png)

1. Clique em **[!UICONTROL Save]** quando sua configuração for definida.

1. Quando seu experimento de conteúdo estiver pronto, você pode clicar em **[!UICONTROL Review to activate]** para exibir um resumo da campanha. Os alertas são exibidos se qualquer parâmetro estiver incorreto ou ausente.

   ![](assets/content_experiment_15.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Activate]** para iniciá-lo.

   ![](assets/content_experiment_14.png)

## Relatório de experiência {#experimentation-report}

![](assets/experimentation_report_3.png)

Da sua campanha **[!UICONTROL Global report]**, o **[!UICONTROL Experimentation]** detalha as informações principais relativas ao desempenho de cada variante e se houve um melhor desempenho durante o teste.

Para obter mais detalhes sobre esse relatório, consulte [Relatório de campanha global](../campaigns/content-experiment.md#experimentation-report) página.
