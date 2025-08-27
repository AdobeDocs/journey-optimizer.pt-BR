---
solution: Journey Optimizer
product: journey optimizer
title: Atividade de condição
description: Saiba mais sobre a atividade de condição
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: atividade, condição, tela, jornada
source-git-commit: a7cfbd5c13ddf70f2a86fb0e19bd3b2fc43393e7
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 19%

---

# Atividade de condição {#condition-activity}

## Adicione uma atividade de condição {#add-condition-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_condition"
>title="Atividade de condição"
>abstract="A Atividade de **condição** permite definir como as pessoas avançam pela sua jornada criando vários caminhos com base em critérios específicos. Você também pode configurar um caminho alternativo para lidar com tempos limite ou erros, garantindo uma experiência contínua."

A Atividade de **condição** permite definir como as pessoas avançam pela sua jornada criando vários caminhos com base em critérios específicos. Você também pode configurar um caminho alternativo para lidar com tempos limite ou erros, garantindo uma experiência contínua.

![](assets/journey49.png)

Os seguintes tipos de condições estão disponíveis:

* [Condição de Source de Dados](#data_source_condition)
* [Condição de tempo](#time_condition)
* [Divisão de porcentagem](#percentage_split)
* [Condição de data](#date_condition)
* [Limite de perfil](#profile_cap)

Você também pode usar um público-alvo em uma condição de jornada. [Saiba mais](#using-a-segment)

## Adicionar e gerenciar caminhos de condição {#about_condition}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple"
>title="Sobre o editor de expressão simples"
>abstract="O modo editor de expressão simples permite executar consultas simples com base em uma combinação de campos. Todos os campos disponíveis são exibidos no lado esquerdo da tela. Arraste e solte campos na zona principal. Para combinar os elementos diferentes, faça o interbloqueio entre eles para criar grupos e/ou níveis de grupo diferentes. Você pode selecionar um operador lógico para combinar elementos no mesmo nível."

Ao usar várias condições em uma jornada, você pode definir rótulos para cada uma delas para identificá-las mais facilmente.

Clique em **[!UICONTROL Adicionar um caminho]** se desejar definir várias condições. Para cada condição, um novo caminho é adicionado na tela após a atividade.

![](assets/journey47.png)

Observe que o design das jornadas tem impactos funcionais. Quando vários caminhos são definidos após uma condição, somente o primeiro caminho qualificado é executado. Isso significa que é possível variar a priorização de caminhos colocando-os um acima ou abaixo do outro.

Vejamos o exemplo da condição de um primeiro caminho &quot;A pessoa é um VIP&quot; e a condição de um segundo caminho &quot;A pessoa é um homem&quot;. Se uma pessoa que atende a ambas as condições (um homem que é um VIP) passar por essa etapa, o primeiro caminho será escolhido, mesmo que essa pessoa também seja elegível para o segundo, porque o primeiro caminho é &quot;acima&quot;. Para alterar essa prioridade, mova suas atividades em outra ordem vertical.

![](assets/journey48.png)

Você pode criar outro caminho para públicos que não estejam qualificados para as condições definidas verificando **[!UICONTROL Mostrar caminho para casos diferentes dos mencionados acima]**. Observe que essa opção não está disponível em condições de divisão. Consulte [Divisão de porcentagem](#percentage_split).

O modo simples permite executar consultas simples com base em uma combinação de campos. Todos os campos disponíveis são exibidos no lado esquerdo da tela. Arraste e solte campos na zona principal. Para combinar os elementos diferentes, faça o interbloqueio entre eles para criar grupos e/ou níveis de grupo diferentes. Você pode selecionar um operador lógico para combinar elementos no mesmo nível:

* AND: uma interseção de dois critérios. Somente os elementos correspondentes a todos os critérios são considerados.
* OR: uma união de dois critérios. Os elementos correspondentes a pelo menos um dos critérios são considerados.

![](assets/journey64.png)

Se você estiver usando o [Serviço de Segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"} para criar públicos, poderá aproveitá-los nas condições de jornada. Consulte [Uso de público-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>Não é possível executar consultas em séries de tempo (por exemplo, uma lista de compras, cliques anteriores em mensagens) com o editor simples. Para isso, será necessário usar o editor avançado. Consulte [esta página](expression/expressionadvanced.md).



A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. A única maneira de fazê-lo continuar é marcar a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

No editor simples, você também encontrará a categoria Propriedades da Jornada, abaixo das categorias de evento e fonte de dados. Essa categoria contém campos técnicos relacionados à jornada para um determinado perfil. Essas são as informações recuperadas pelo sistema a partir das jornadas ativas, como a ID da jornada ou os erros específicos encontrados. [Saiba mais](expression/journey-properties.md)

## Condição do Source de dados {#data_source_condition}

Use uma **[!UICONTROL Condição de Source de Dados]** para definir uma condição com base nos campos das fontes de dados ou nos eventos posicionados anteriormente na jornada. Esse tipo de condição é definido com o editor de expressão. Saiba como usar o editor de expressão [nesta seção](expression/expressionadvanced.md).

Por exemplo, se você estiver direcionando um público-alvo com atributos de enriquecimento gerados usando um fluxo de trabalho de composição ou um upload personalizado (arquivo CSV), você pode aproveitar esses atributos de enriquecimento para criar sua condição.

Usando o editor de expressão avançado, você pode configurar condições mais avançadas que manipulem coleções ou usem fontes de dados que exijam a transmissão de parâmetros. [Saiba mais](../datasource/external-data-sources.md).

![](assets/journey50.png)

## Condição de tempo {#time_condition}

Use uma **[!UICONTROL Condição de tempo]** para executar ações diferentes de acordo com a hora do dia e/ou o dia da semana. Por exemplo, você pode decidir enviar notificações por push durante o dia e emails à noite durante os dias da semana.

>[!NOTE]
>
>* O fuso horário não é específico de uma condição e é definido no nível da jornada nas propriedades da jornada. Saiba mais [nesta página](../building-journeys/timezone-management.md).
>
>* Por padrão, a **[!UICONTROL Condição de tempo]** é definida por hora, de 00:00 a 12:00.

![](assets/journey51.png)

Três opções de filtragem de tempo estão disponíveis:

* Hora: permite configurar uma condição com base na hora do dia. Em seguida, você define as horas de início e término. Os indivíduos entrarão no caminho somente durante o intervalo de horas definido.
* Dia da semana: permite configurar uma condição com base no dia da semana. Em seguida, selecione em quais dias você deseja que as pessoas insiram o caminho.
* Day of the week and hour: essa opção combina as duas primeiras opções.

## Divisão de porcentagem {#percentage_split}

Essa opção permite dividir aleatoriamente o público para definir uma ação diferente para cada grupo. Defina o número de divisões e a repartição para cada caminho. O cálculo dividido é estatístico, pois o sistema não pode prever quantas pessoas fluirão nessa atividade da jornada. Como resultado, a divisão tem uma margem de erro muito baixa. Esta função é baseada em um mecanismo aleatório Java (consulte esta [página](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html){target="_blank"}).

No modo de teste, ao atingir uma divisão, a ramificação superior é sempre escolhida. É possível reorganizar a posição das ramificações de divisão se quiser que o teste escolha um caminho diferente. Consulte [esta página](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Observe que não há nenhum botão para adicionar um caminho na condição de divisão de porcentagem. O número de caminhos dependerá do número de divisões. Em condições de divisão, não é possível adicionar um caminho para outros casos, pois isso não pode ocorrer. As pessoas sempre entrarão em um dos caminhos divididos.

![](assets/journey52.png)

## Condição de data {#date_condition}

Isso permite definir um fluxo diferente com base na data. Por exemplo, se a pessoa entrar na etapa durante o período de &quot;vendas&quot;, você enviará a ela uma mensagem específica. No resto do ano, você enviará outra mensagem.

>[!NOTE]
>
>O fuso horário não é mais específico para uma condição e agora é definido no nível da jornada nas propriedades da jornada. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey53.png)

## Limite de perfil {#profile_cap}

Use esse tipo de condição para definir um número máximo de perfis para um caminho de jornada. Quando esse limite é atingido, os perfis que entram pegam um caminho alternativo. Isso garante que suas jornadas nunca excederão o limite definido.

>[!NOTE]
>
>Recomendamos que você defina um limite de perfil de alto valor. A precisão e a probabilidade de uma população atingir o número de limites exato só aumentam à medida que o limite aumenta. Para números pequenos (por exemplo, um limite de 50), os números nem sempre corresponderão, pois o limite pode não ser atingido antes que os perfis tomem um caminho alternativo.

<!--You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).-->

O limite padrão é 1.000.

O contador se aplica somente à versão do jornada selecionada. O contador é redefinido para zero quando a jornada é duplicada ou quando uma nova versão é criada. Após uma redefinição, os perfis que entram tomam o caminho nominal novamente até que o limite do contador seja atingido.

Quando o limite de perfil é definido em uma jornada recorrente, o contador não é redefinido após cada recorrência.

O caminho nominal sempre tem prioridade sobre o caminho alternativo, mesmo que você mova o caminho alternativo acima do caminho nominal na tela de jornada.

Para jornadas em tempo real, estes são os limites a serem considerados para garantir que o limite seja atingido:

* Para um limite superior a 10.000, o número de perfis distintos a serem injetados deve ser pelo menos 1,3 vezes superior ao limite.
* Para um limite inferior a 10.000, o número de perfis distintos a serem injetados deve ser 1000 mais o limite.

O limite de perfil não é considerado no modo de teste.

![](assets/profile-cap-condition.png)

## Uso de públicos-alvo em condições {#using-a-segment}

Esta seção explica como usar um público-alvo em uma condição de jornada. Para obter mais informações sobre públicos-alvo e como criá-los, consulte [esta seção](../audience/about-audiences.md).

Para usar um público-alvo em uma condição de jornada, siga estas etapas:

1. Abra uma jornada, solte uma atividade de **[!UICONTROL Condição]** e escolha a **Condição de Source de Dados**.

   ![](assets/segment3.png)

1. Clique em **[!UICONTROL Adicionar um caminho]** para cada caminho extra necessário. Para cada caminho, clique no campo **[!UICONTROL Expression]**.

1. No lado esquerdo, abra o nó **[!UICONTROL Públicos-alvo]**. Arraste e solte o público-alvo que deseja usar com sua condição. Por padrão, a condição no público-alvo é verdadeira.

   ![](assets/segment4.png)

   >[!NOTE]
   >
   >Observe que somente os indivíduos com o status de participação de público **Realizado** serão considerados membros do público. Para obter mais informações sobre como avaliar um público, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=pt-BR#interpret-segment-results){target="_blank"}.
