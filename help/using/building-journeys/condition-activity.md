---
title: Atividade de condição
description: Saiba mais sobre a atividade de condição
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: 43e4e089025721180a6b8ce9ea9104a2f73d3e47
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 8%

---

# Atividade de condição{#section_e2n_pft_dgb}

Esses tipos de condições estão disponíveis:

* [Condição da fonte de dados](#data_source_condition)
* [Condição de tempo](#time_condition)
* [Divisão de porcentagem](#percentage_split)
* [Condição de data](#date_condition)
<!--
* [Profile cap](#profile_cap)
-->

![](../assets/journey49.png)

## Sobre a atividade Condição {#about_condition}

Ao usar várias condições em uma jornada, você pode definir rótulos para cada uma delas para identificá-las mais facilmente.

Clique em **[!UICONTROL Add a path]** se desejar definir várias condições. Para cada condição, um novo caminho é adicionado na tela após a atividade .

![](../assets/journey47.png)

Observe que o design das jornadas tem impactos funcionais. Quando vários caminhos são definidos após uma condição, somente o primeiro caminho elegível é executado. Isso significa que você pode variar a priorização de caminhos, colocando-os acima ou abaixo uns dos outros.

Por exemplo, vamos considerar o exemplo de uma condição de primeiro caminho &quot;A pessoa é um VIP&quot; e uma condição de segundo caminho &quot;A pessoa é um homem&quot;. Se uma pessoa que cumpre ambas as condições (um homem que é um VIP) passar por esta etapa, o primeiro caminho será escolhido mesmo que essa pessoa também seja elegível para a segunda, porque o primeiro caminho está &quot;acima&quot;. Para alterar essa prioridade, mova suas atividades para outra ordem vertical.

![](../assets/journey48.png)

Você pode criar outro caminho para públicos-alvo que não estejam qualificados para as condições definidas ao verificar **[!UICONTROL Show path for other cases than the one(s) above]**. Observe que essa opção não está disponível em condições de divisão. Consulte [Divisão de porcentagem](#percentage_split).

O modo simples permite executar consultas simples com base em uma combinação de campos. Todos os campos disponíveis são exibidos no lado esquerdo da tela. Arraste e solte campos na zona principal. Para combinar os diferentes elementos, faça o interbloqueio entre eles para criar grupos e/ou níveis de grupo diferentes. Você pode selecionar um operador lógico para combinar elementos no mesmo nível:

* E: uma interseção de dois critérios. Somente os elementos que correspondem a todos os critérios são considerados.
* OU: uma união de dois critérios. Os elementos correspondentes a pelo menos um dos critérios são considerados.

![](../assets/journey64.png)

Se estiver usando o [Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;} para criar seus segmentos, você pode aproveitá-los em suas condições de jornada. Consulte [Uso de segmentos em condições](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>Não é possível executar consultas em séries de tempo (por exemplo, uma lista de compras, cliques anteriores em mensagens) com o editor simples. Para isso, será necessário usar o editor avançado. Consulte [Documentação do Journey Orchestration Adobe](expression/expressionadvanced.md).

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. O único modo de fazê-la continuar é marcando a caixa **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

No editor simples, você também encontrará a categoria Propriedades da Jornada, abaixo das categorias de evento e fonte de dados. Esta categoria contém campos técnicos relacionados à jornada de um determinado perfil. Essas são as informações recuperadas pelo sistema a partir das jornadas ativas, como a ID da jornada ou os erros específicos encontrados. Para obter mais informações, consulte [Documentação do Journey Orchestration Adobe](expression/journey-properties.md)

## Condição da fonte de dados {#data_source_condition}

Isso permite definir uma condição com base nos campos das fontes de dados ou nos eventos posicionados anteriormente na jornada. Para saber como usar o editor de expressão, consulte [Documentação do Journey Orchestration Adobe](expression/expressionadvanced.md). Usando o editor de expressão avançado, você pode configurar condições mais avançadas manipulando coleções ou usando fontes de dados que exigem a passagem de parâmetros. Consulte [esta página](../datasource/external-data-sources.md).

![](../assets/journey50.png)

## Condição de tempo{#time_condition}

Isso permite executar ações diferentes de acordo com a hora do dia e/ou o dia da semana. Por exemplo, você pode decidir enviar mensagens SMS durante o dia e emails à noite durante os dias da semana.

>[!NOTE]
>
>O fuso horário não é mais específico de uma condição e agora é definido no nível da jornada nas propriedades da jornada. Consulte [esta página](../building-journeys/timezone-management.md).

![](../assets/journey51.png)

## Divisão de porcentagem {#percentage_split}

Essa opção permite dividir aleatoriamente o público-alvo para definir uma ação diferente para cada grupo. Defina o número de divisões e a repartição para cada caminho. O cálculo de divisão é estatístico, pois o sistema não pode prever quantas pessoas fluirão nessa atividade da jornada. Como resultado, a divisão tem uma margem de erro muito baixa. Essa função é baseada em um mecanismo aleatório Java (consulte esta seção [página](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html)).

No modo de teste, ao alcançar uma divisão, a ramificação superior é sempre escolhida. Você pode reorganizar a posição das ramificações divididas se quiser que o teste escolha um caminho diferente. Consulte [esta página](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Observe que não há um botão para adicionar um caminho na condição de divisão de porcentagem. O número de caminhos dependerá do número de divisões. Em condições divididas, não é possível adicionar um caminho para outros casos, pois ele não pode ocorrer. As pessoas sempre vão para um dos caminhos divididos.

![](../assets/journey52.png)

## Condição de data {#date_condition}

Isso permite definir um fluxo diferente com base na data. Por exemplo, se a pessoa entrar na etapa durante o período de &quot;vendas&quot;, você enviará uma mensagem específica para ela. No resto do ano, você enviará outra mensagem.

>[!NOTE]
>
>O fuso horário não é mais específico de uma condição e agora é definido no nível da jornada nas propriedades da jornada. Consulte [esta página](../building-journeys/timezone-management.md).

![](../assets/journey53.png)

<!--
## Profile cap {#profile_cap}

Use this condition type to set a maximum number of profiles for a journey path. When this limit is reached, the entering profiles take an alternate path.

You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).

The default cap is 1000. You can set an integer value from 1 to 20,000.

The counter applies only to the selected journey version. The counter is reset to zero after 180 days. After a reset, the entering profiles take the nominal path again until the counter limit is reached.

The nominal path always has priority over the alternate path, even if you move the alternate path above the nominal path on the journey canvas.

![](../assets/profile-cap-condition.png)
-->

## Uso de segmentos em condições {#using-a-segment}

Esta seção explica como usar um segmento em uma condição de jornada. Para obter mais informações sobre segmentos e como criá-los, consulte [esta seção](../segment/about-segments.md).

Para usar um segmento em uma condição de jornada, siga estas etapas:

1. Abra uma jornada, solte uma **[!UICONTROL Condition]** e escolha a **Condição da fonte de dados**.
   ![](../assets/journey47.png)

1. Clique em **[!UICONTROL Add a path]** para cada caminho extra necessário. Para cada caminho, clique no botão **[!UICONTROL Expression]** campo.

   ![](../assets/segment3.png)

1. No lado esquerdo, expanda-se **[!UICONTROL Segments]** nó . Arraste e solte o segmento que deseja usar para sua condição. Por padrão, a condição no segmento é verdadeira.

   ![](../assets/segment4.png)

   >[!NOTE]
   >
   >Observe que somente os indivíduos com a variável **Realizado** e **Existente** os status de participação do segmento serão considerados membros do segmento. Para obter mais informações sobre como avaliar um segmento, consulte [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.
