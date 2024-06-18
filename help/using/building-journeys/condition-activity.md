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
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 14%

---

# Atividade de condição{#condition-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_condition"
>title="Atividade de condição"
>abstract="Essa atividade permite definir como a pessoa fluirá na jornada. Vários caminhos serão criados com base em vários critérios. Você também pode criar um caminho alternativo no caso de tempo limite ou erro."

Estes tipos de condições estão disponíveis:

* [Condição da fonte de dados](#data_source_condition)
* [Condição de tempo](#time_condition)
* [Divisão de porcentagem](#percentage_split)
* [Condição de data](#date_condition)
* [Limite de perfil](#profile_cap)

![](assets/journey49.png)

## Sobre a atividade Condição {#about_condition}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple"
>title="Sobre o editor de expressão simples"
>abstract="O modo editor de expressão simples permite executar consultas simples com base em uma combinação de campos. Todos os campos disponíveis são exibidos no lado esquerdo da tela. Arraste e solte campos na zona principal. Para combinar os elementos diferentes, faça o interbloqueio entre eles para criar grupos e/ou níveis de grupo diferentes. Você pode selecionar um operador lógico para combinar elementos no mesmo nível."

Ao usar várias condições em uma jornada, você pode definir rótulos para cada uma delas para identificá-las mais facilmente.

Clique em **[!UICONTROL Adicionar um caminho]** se quiser definir várias condições. Para cada condição, um novo caminho é adicionado na tela após a atividade.

![](assets/journey47.png)

Observe que o design das jornadas tem impactos funcionais. Quando vários caminhos são definidos após uma condição, somente o primeiro caminho qualificado é executado. Isso significa que é possível variar a priorização de caminhos colocando-os um acima ou abaixo do outro.

Por exemplo, vamos pegar o exemplo de uma condição de primeiro caminho &quot;A pessoa é um VIP&quot; e uma condição de segundo caminho &quot;A pessoa é um homem&quot;. Se uma pessoa que atende às duas condições (um homem que é VIP) passar por essa etapa, o primeiro caminho será escolhido mesmo que essa pessoa também seja elegível para o segundo, porque o primeiro caminho é &quot;acima&quot;. Para alterar essa prioridade, mova suas atividades em outra ordem vertical.

![](assets/journey48.png)

Você pode criar outro caminho para públicos-alvo que não se qualifiquem para as condições definidas marcando **[!UICONTROL Mostrar o caminho para casos diferentes dos mencionados acima]**. Observe que essa opção não está disponível em condições de divisão. Consulte [Divisão de porcentagem](#percentage_split).

O modo simples permite executar consultas simples com base em uma combinação de campos. Todos os campos disponíveis são exibidos no lado esquerdo da tela. Arraste e solte campos na zona principal. Para combinar os elementos diferentes, faça o interbloqueio entre eles para criar grupos e/ou níveis de grupo diferentes. Você pode selecionar um operador lógico para combinar elementos no mesmo nível:

* AND: uma interseção de dois critérios. Somente os elementos correspondentes a todos os critérios são considerados.
* OR: uma união de dois critérios. Os elementos correspondentes a pelo menos um dos dois critérios são considerados.

![](assets/journey64.png)

Se você estiver usando o [Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"} para criar públicos-alvo, você pode aproveitá-los nas condições de jornada. Consulte [Uso do público-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>Não é possível executar consultas em séries de tempo (por exemplo, uma lista de compras, cliques anteriores em mensagens) com o editor simples. Para isso, será necessário usar o editor avançado. Consulte [esta página](expression/expressionadvanced.md).

Quando ocorre um erro em uma ação ou condição, a jornada de um indivíduo é interrompida. A única maneira de fazê-lo continuar é marcando a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]**. Consulte [nesta seção](../building-journeys/using-the-journey-designer.md#paths).

No editor simples, você também encontrará a categoria Propriedades da Jornada, abaixo das categorias de evento e fonte de dados. Essa categoria contém campos técnicos relacionados à jornada para um determinado perfil. Essas são as informações recuperadas pelo sistema a partir das jornadas ativas, como a ID da jornada ou os erros específicos encontrados. [Saiba mais](expression/journey-properties.md)

## Condição da fonte de dados {#data_source_condition}

Isso permite definir uma condição com base nos campos das fontes de dados ou nos eventos posicionados anteriormente na jornada. Saiba como usar o editor de expressão no [nesta seção](expression/expressionadvanced.md).

Por exemplo, se você estiver direcionando um público-alvo com atributos de enriquecimento gerados usando um fluxo de trabalho de composição ou um upload personalizado (arquivo CSV), você pode aproveitar esses atributos de enriquecimento para criar sua condição.

Usando o editor de expressão avançado, você pode configurar condições mais avançadas que manipulem coleções ou usem fontes de dados que exijam a transmissão de parâmetros. [Saiba mais](../datasource/external-data-sources.md).

![](assets/journey50.png)

## Condição de tempo{#time_condition}

Isso permite executar ações diferentes de acordo com a hora do dia e/ou o dia da semana. Por exemplo, você pode decidir enviar notificações por push durante o dia e emails à noite durante os dias da semana.

>[!NOTE]
>
>O fuso horário não é específico de uma condição e é definido no nível da jornada nas propriedades da jornada. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey51.png)

Três opções de filtragem de tempo estão disponíveis:

* Hora: permite configurar uma condição com base na hora do dia. Em seguida, você define as horas de início e término. Os indivíduos entrarão no caminho somente durante o intervalo de horas definido.
* Dia da semana: permite configurar uma condição com base no dia da semana. Em seguida, selecione em quais dias você deseja que as pessoas insiram o caminho.
* Day of the week and hour: essa opção combina as duas primeiras opções.

## Divisão de porcentagem {#percentage_split}

Essa opção permite dividir aleatoriamente o público para definir uma ação diferente para cada grupo. Defina o número de divisões e a repartição para cada caminho. O cálculo dividido é estatístico, pois o sistema não pode prever quantas pessoas fluirão nessa atividade da jornada. Como resultado, a divisão tem uma margem de erro muito baixa. Esta função é baseada em um mecanismo aleatório Java (consulte esta [página](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html)).

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

O limite padrão é 1000.

O contador se aplica somente à versão do jornada selecionada. O contador é redefinido para zero quando a jornada é duplicada ou quando uma nova versão é criada. Após uma redefinição, os perfis que entram tomam o caminho nominal novamente até que o limite do contador seja atingido.

Quando o limite de perfil é definido em uma jornada recorrente, o contador não é redefinido após cada recorrência.

O caminho nominal sempre tem prioridade sobre o caminho alternativo, mesmo que você mova o caminho alternativo acima do caminho nominal na tela de jornada.

Para jornadas em tempo real, estes são os limites a serem considerados para garantir que o limite seja atingido:

* Para um limite superior a 10000, o número de perfis distintos a serem injetados deve ser pelo menos 1,3 vezes superior ao limite.
* Para um limite inferior a 10000, o número de perfis distintos a serem injetados deve ser 1000 mais o limite.

O limite de perfil não é considerado no modo de teste.

![](assets/profile-cap-condition.png)

## Uso de públicos-alvo em condições {#using-a-segment}

Esta seção explica como usar um público-alvo em uma condição de jornada. Para obter mais informações sobre públicos-alvo e como criá-los, consulte [nesta seção](../audience/about-audiences.md).

Para usar um público-alvo em uma condição de jornada, siga estas etapas:

1. Abra uma jornada, solte uma **[!UICONTROL Condição]** e escolha a **Condição da fonte de dados**.

   ![](assets/segment3.png)

1. Clique em **[!UICONTROL Adicionar um caminho]** para cada caminho extra necessário. Para cada caminho, clique no link **[!UICONTROL Expressão]** campo.

1. No lado esquerdo, expanda **[!UICONTROL Públicos-alvo]** nó. Arraste e solte o público-alvo que deseja usar com sua condição. Por padrão, a condição no público-alvo é verdadeira.

   ![](assets/segment4.png)

   >[!NOTE]
   >
   >Observe que somente os indivíduos com o **Realizado** e **Existente** os status de participação do público serão considerados membros do público. Para obter mais informações sobre como avaliar um público-alvo, consulte a [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.
