---
title: Decisão em lote
description: Saiba como fornecer decisões de oferta a todos os perfis em um determinado segmento do Adobe Experience Platform.
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: f3f38e7db95bd1a6dc41b1626177c800280fb71c
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 2%

---

# Decisão em lote {#deliver}

## Introdução à decisão em lote {#start}

O Journey Optimizer permite que você forneça decisões de ofertas a todos os perfis em um determinado segmento do Adobe Experience Platform.

Para fazer isso, você precisa criar uma solicitação de trabalho no Journey Optimizer que conterá informações sobre o segmento a ser direcionado e a decisão da oferta a ser usada. O conteúdo da oferta para cada perfil no segmento é colocado em um conjunto de dados do Adobe Experience Platform, onde está disponível para fluxos de trabalho em lote personalizados.

A entrega em lote também pode ser executada usando APIs. Para obter mais informações, consulte [Documentação da API do Batch Decisioning](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Pré-requisitos {#prerequisites}

Antes de configurar uma solicitação de trabalho, verifique se você criou:

* **Um conjunto de dados** no Adobe Experience Platform. Esse conjunto de dados será usado para armazenar o resultado da decisão usando o schema &quot;ODE DecisionEvents&quot;. Saiba mais na [Documentação de conjuntos de dados](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html).

* **Um segmento** no Adobe Experience Platform. O segmento deve ser avaliado e depois atualizado. Saiba como atualizar a avaliação de associação de segmento no [Documentação do Serviço de segmentação](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >Um trabalho em lote é executado do instantâneo de perfil que ocorre uma vez por dia. A decisão em lote limita a frequência e sempre carrega perfis do instantâneo mais recente.

* **Uma decisão** no Adobe Journey Optimizer. [Saiba como criar uma decisão](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Criar uma solicitação de trabalho

Para criar uma nova solicitação de emprego, siga as etapas abaixo.

1. No **[!UICONTROL Offers]** abra o **[!UICONTROL Batch decisioning]** e clique em **[!UICONTROL Create request]**.

   ![](assets/batch-create.png)

1. Nomeie sua solicitação de trabalho e selecione o conjunto de dados para o qual os dados da tarefa devem ser enviados.

1. Selecione o segmento do Adobe Experience Platform a ser direcionado.

1. Selecione um ou vários escopos de decisão de oferta que deseja usar para entregar ofertas ao segmento:
   1. Selecione uma disposição na lista.
   1. As decisões disponíveis para a disposição selecionada são exibidas. Selecione a decisão de sua escolha e clique em **[!UICONTROL Add]**.
   1. Repita a operação para adicionar quantos escopos de decisão desejar.

   ![](assets/batch-decision.png)

1. Por padrão, uma oferta do escopo de decisão é retornada para cada perfil. É possível ajustar o número de ofertas retornadas usando a variável **[!UICONTROL Request offer per profile]** opção. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para o escopo de decisão selecionado.

   >[!NOTE]
   >
   >Você pode solicitar até 30 ofertas por escopo de decisão.

1. Se desejar incluir o conteúdo da oferta no conjunto de dados, alterne a opção **[!UICONTROL Include content]** ativada. Essa opção está desabilitada por padrão.

1. Clique em **[!UICONTROL Create]** para executar a solicitação de trabalho.

## Monitorar trabalhos em lote

Todos os trabalhos em lote solicitados podem ser acessados a partir do **[!UICONTROL Batch decisioning]** guia . Além disso, as ferramentas de pesquisa e filtragem estão disponíveis para ajudar você a refinar a lista.

![](assets/batch-list.png)

### Status de solicitações de trabalho

Depois que uma solicitação de trabalho é criada, o trabalho em lote passa por vários status:

>[!NOTE]
>
>Para garantir que você esteja obtendo as informações mais recentes sobre o status de uma solicitação de trabalho, use o botão de elipse ao lado da tarefa para atualizá-la.

1. **[!UICONTROL Queued]**: A solicitação de trabalho foi criada e entrou na fila de processamento. É possível executar até 5 trabalhos em lote por vez, por conjunto de dados. Quaisquer outras solicitações em lote com o mesmo conjunto de dados de saída são adicionadas à fila. Um trabalho em fila é selecionado para o processamento quando o trabalho anterior terminar de ser executado.
1. **[!UICONTROL Processing]**: A solicitação de trabalho está sendo processada
1. **[!UICONTROL Ingesting]**: A solicitação de trabalho foi executada, os dados de resultado estão sendo assimilados no conjunto de dados selecionado,
1. **[!UICONTROL Completed]**: A solicitação de trabalho foi executada e os dados de resultado agora são armazenados no conjunto de dados selecionado.

   >[!NOTE]
   >
   >Você pode acessar o conjunto de dados em que os resultados de um trabalho são armazenados clicando no nome dele na lista de tarefas.

Se ocorrer um erro enquanto a solicitação de trabalho está sendo executada, ela receberá a variável **[!UICONTROL Error]** status. Tente duplicar o trabalho em lote para criar uma nova solicitação. [Saiba como duplicar um trabalho em lote](#duplicate)

### Tempo de processamento da tarefa em lote

O tempo de ponta a ponta para cada trabalho em lote é a duração do tempo em que a carga de trabalho é criada até o momento em que o resultado da decisão está disponível no conjunto de dados de saída.

O tamanho do segmento é o principal fator que afeta o tempo de decisão completo do lote. Se a oferta elegível tiver um limite de frequência global ativado, a decisão em lote levará mais tempo para ser concluída. Abaixo estão algumas aproximações do tempo de processamento completo para seus respectivos tamanhos de segmento, com e sem limite de frequência para ofertas elegíveis:

Com o limite de frequência ativado para ofertas qualificadas:

| Tamanho do segmento | Tempo de processamento completo |
|--------------|----------------------------|
| 10 mil perfis ou menos | 7 minutos |
| 1 milhão de perfis ou menos | 30 minutos |
| 15 milhões de perfis ou menos | 50 minutos |

Sem limite de frequência para ofertas elegíveis:

| Tamanho do segmento | Tempo de processamento completo |
|--------------|----------------------------|
| 10 mil perfis ou menos | 6 minutos |
| 1 milhão de perfis ou menos | 8 minutos |
| 15 milhões de perfis ou menos | 16 minutos |

## Duplicar uma solicitação de trabalho {#duplicate}

Você pode reutilizar informações de um trabalho existente para criar uma nova solicitação.

Para fazer isso, clique no ícone de duplicação, edite as informações da tarefa, se necessário, e clique em **[!UICONTROL Create]** para criar a nova solicitação.

![](assets/batch-duplicate.png)
