---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Test em suas campanhas orquestradas
description: Saiba como usar a atividade Testar
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 28%

---


# Teste {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Atividade de teste"
>abstract="A atividade **Teste** é uma atividade de **Controle de fluxo**. Ela permite habilitar transições com base nas condições especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condições"
>abstract="A atividade **Teste** pode ter várias transições de saída. Durante a execução da campanha orquestrada, cada condição é testada sequencialmente até que uma delas seja atendida. Se nenhuma das condições for atendida, a campanha orquestrada continuará com base na **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, a campanha orquestrada será interrompida nesse ponto."

A atividade **[!UICONTROL Teste]** é uma atividade de **[!UICONTROL Controle de fluxo]**. Use-o para ramificar o fluxo da campanha ativando transições diferentes, dependendo das condições definidas. Cada condição pode avaliar os dados da transição de entrada e você pode escolher qual transição é executada primeiro pela ordem em que as condições são avaliadas.

## Configurar a atividade Testar {#test-configuration}

Para configurar a atividade **[!UICONTROL Test]**:

1. Solte uma atividade **[!UICONTROL Test]** na tela da campanha Orquestrada.

1. Por padrão, a atividade fornece um único teste booleano: quando a condição &quot;True&quot; é atendida, essa transição é ativada; caso contrário, a transição &quot;False&quot; (padrão) é ativada.

   ![](../assets/test-1.png)

1. Defina a condição para uma transição preenchendo estes campos:

   * **Rótulo**: um nome para a transição para que você possa identificá-la na tela.

   * **Tipo de condição**: os dados para avaliar, por padrão, a contagem de população.

   * **Operador**: a comparação a ser aplicada, por exemplo, igual a, maior que, menor que. A lista de operadores depende do tipo de dados do tipo de condição.

   * **Valor**: o valor com o qual comparar o tipo de condição.

   ![](../assets/test-2.png)

1. Para ramificar mais de dois resultados, clique em **[!UICONTROL Adicionar condição]** e defina um rótulo e uma condição para cada transição adicional.

1. No tempo de execução, a campanha avalia as condições em ordem e segue a primeira que corresponde a. Quando nenhuma condição é correspondente, a execução segue a **[!UICONTROL Condição padrão]** se uma estiver definida; caso contrário, a campanha para na atividade **[!UICONTROL Test]**.

## Exemplo {#example}

Neste exemplo, transições diferentes são ativadas com base no número de perfis segmentados por uma atividade **[!UICONTROL Criar público]**. As condições são avaliadas em ordem; a última transição é o padrão e é usada quando nenhuma condição anterior é correspondente.

* Se mais de 10 mil perfis forem direcionados, uma mensagem de email será enviada.
* Padrão (nenhuma condição correspondida): quando a contagem é de 10.000 ou menos, a população é direcionada para uma transição &quot;não entrar em contato&quot;.

![](../assets/workflow-test-example.png)
