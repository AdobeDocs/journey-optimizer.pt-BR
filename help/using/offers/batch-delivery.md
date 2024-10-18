---
title: Decisão em lote
description: Saiba como fornecer decisões de oferta a todos os perfis em um determinado público-alvo da Adobe Experience Platform.
feature: Decision Management
role: User
level: Intermediate
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: b057d198d3c5b12121ee50d7a97ff4b33b8209b4
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 3%

---

# Decisão em lote {#deliver}

## Introdução à decisão em lote {#start}

O Journey Optimizer permite que você forneça decisões de oferta para todos os perfis em um determinado público-alvo da Adobe Experience Platform.

Para fazer isso, você precisa criar uma solicitação de trabalho no Journey Optimizer que conterá informações sobre o público-alvo a ser direcionado e a decisão de oferta a ser usada. O conteúdo da oferta de cada perfil no público-alvo é então colocado em um conjunto de dados do Adobe Experience Platform, onde ele estará disponível para fluxos de trabalho em lote personalizados.

A entrega em lote também pode ser executada usando APIs. Para obter mais informações, consulte a [documentação da API de decisão em lote](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Pré-requisitos {#prerequisites}

Antes de configurar uma solicitação de tarefa, verifique se você criou:

* **Um conjunto de dados** no Adobe Experience Platform. Esse conjunto de dados será usado para armazenar o resultado da decisão usando o schema &quot;ODE DecisionEvents&quot;. Saiba mais na [documentação sobre conjuntos de dados](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=pt-BR).

* **Um público-alvo** na Adobe Experience Platform. O público-alvo deve ser avaliado e depois atualizado. Saiba como atualizar a avaliação de associação de público na [documentação do Serviço de segmentação](https://www.adobe.com/go/segmentation-overview-en)

  >[!NOTE]
  >
  >Um trabalho em lote é executado fora do instantâneo do perfil que ocorre uma vez por dia. A decisão em lote limita a frequência e sempre carrega perfis do instantâneo mais recente. Aguarde até 24 horas após a criação de um público-alvo antes de tentar a API de decisão em lote.

* **Uma decisão** no Adobe Journey Optimizer. [Saiba como criar uma decisão](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Criar uma solicitação de trabalho

Para criar uma nova solicitação de trabalho, siga as etapas abaixo.

1. No menu **[!UICONTROL Ofertas]**, abra a guia **[!UICONTROL Decisão em lote]** e clique em **[!UICONTROL Criar solicitação]**.

   ![](assets/batch-create.png)

1. Nomeie sua solicitação de trabalho e selecione o conjunto de dados para o qual os dados de trabalho devem ser enviados.

1. Selecione o público-alvo do Adobe Experience Platform para direcionar.

1. Selecione um ou vários escopos de decisão de oferta que você deseja usar para entregar ofertas ao público:
   1. Selecione uma disposição na lista.
   1. As decisões disponíveis para a disposição selecionada são exibidas. Selecione a decisão de sua escolha e clique em **[!UICONTROL Adicionar]**.
   1. Repita a operação para adicionar quantos escopos de decisão desejar.

   ![](assets/batch-decision.png)

1. Por padrão, uma oferta do escopo de decisão é retornada para cada perfil. Você pode ajustar o número de ofertas retornadas usando a opção **[!UICONTROL Solicitar oferta por perfil]**. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para o escopo de decisão selecionado.

   >[!NOTE]
   >
   >É possível solicitar até 30 ofertas por escopo de decisão.

1. Se quiser incluir o conteúdo da oferta no conjunto de dados, alterne a opção **[!UICONTROL Incluir conteúdo]** para ativada. Essa opção está desabilitada por padrão.

1. Clique em **[!UICONTROL Criar]** para executar a solicitação de trabalho.

## Monitorar trabalhos em lotes

Todos os trabalhos em lotes solicitados podem ser acessados na guia **[!UICONTROL Decisão em lote]**. Além disso, as ferramentas de pesquisa e filtragem estão disponíveis para ajudar você a refinar a lista.

![](assets/batch-list.png)

### Status de solicitações de trabalho

Depois que uma solicitação de tarefa é criada, a tarefa em lote passa por vários status:

>[!NOTE]
>
>Para garantir que você esteja obtendo as informações mais recentes sobre o status de uma solicitação de trabalho, use o botão de reticências ao lado do trabalho para atualizá-lo.

1. **[!UICONTROL Em fila]**: a solicitação de trabalho foi criada e entrou na fila de processamento. Até 5 trabalhos em lote podem ser executados de cada vez por conjunto de dados. Quaisquer outras solicitações em lote com o mesmo conjunto de dados de saída são adicionadas à fila. Uma tarefa em fila será processada assim que a tarefa anterior terminar de ser executada.
1. **[!UICONTROL Processando]**: a solicitação de trabalho está sendo processada
1. **[!UICONTROL Assimilação]**: a solicitação de trabalho foi executada, os dados de resultado estão sendo assimilados no conjunto de dados selecionado,
1. **[!UICONTROL Concluído]**: a solicitação de trabalho foi executada e os dados resultantes agora são armazenados no conjunto de dados selecionado.

   >[!NOTE]
   >
   >Você pode acessar o conjunto de dados em que os resultados de um trabalho são armazenados clicando no nome na lista de trabalhos.

Se ocorrer um erro enquanto a solicitação de trabalho estiver sendo executada, ela receberá o status **[!UICONTROL Erro]**. Tente duplicar o trabalho em lote para criar uma nova solicitação. [Saiba como duplicar um trabalho em lotes](#duplicate)

### Tempo de processamento do trabalho em lotes

A hora de ponta a ponta para cada processo em lote é a duração da hora em que a carga de trabalho é criada até o momento em que o resultado da decisão está disponível no conjunto de dados de saída.

O tamanho do público-alvo é o principal fator que afeta o tempo completo de decisão do lote. Se a oferta elegível tiver um limite de frequência global ativado, a decisão em lote levará mais tempo para ser concluída. Abaixo estão algumas aproximações do tempo de processamento completo para seus respectivos tamanhos de público, com e sem limite de frequência para ofertas elegíveis:

Com o limite de frequência habilitado para ofertas qualificadas:

| Tamanho do público-alvo | Tempo de processamento de ponta a ponta |
|--------------|----------------------------|
| 10 mil perfis ou menos | 7 minutos |
| 1 milhão de perfis ou menos | 30 minutos |
| 15 milhões de perfis ou menos | 50 minutos |

Sem limite de frequência para ofertas elegíveis:

| Tamanho do público-alvo | Tempo de processamento de ponta a ponta |
|--------------|----------------------------|
| 10 mil perfis ou menos | 6 minutos |
| 1 milhão de perfis ou menos | 8 minutos |
| 15 milhões de perfis ou menos | 16 minutos |

## Duplicar uma solicitação de tarefa {#duplicate}

Você pode reutilizar informações de um job existente para criar uma nova solicitação.

Para fazer isso, clique no ícone de duplicação, edite as informações do trabalho, se necessário, e clique em **[!UICONTROL Criar]** para criar a nova solicitação.

![](assets/batch-duplicate.png)
