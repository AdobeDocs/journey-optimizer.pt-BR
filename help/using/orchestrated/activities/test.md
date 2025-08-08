---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Test em suas campanhas orquestradas
description: Saiba como usar a atividade Testar
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 83%

---


# Testar {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Atividade de teste"
>abstract="A atividade **Teste** é uma atividade de **Controle de fluxo**. Ela permite habilitar transições com base nas condições especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condições"
>abstract="A atividade **Teste** pode ter várias transições de saída. Durante a execução da campanha orquestrada, cada condição é testada sequencialmente até que uma delas seja atendida. Se nenhuma das condições for atendida, a campanha orquestrada continuará com base na **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, a campanha orquestrada será interrompida nesse ponto."

A atividade **[!UICONTROL Teste]** é uma atividade de **[!UICONTROL Controle de fluxo]**. Ela permite habilitar transições com base nas condições especificadas.

## Configurar a atividade Testar {#test-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Testar]**:

1. Adicione uma atividade **[!UICONTROL Test]** à sua campanha Orquestrada.

1. Por padrão, a atividade **[!UICONTROL Testar]** apresenta um teste booleano simples. Se a condição definida na transição “Verdadeira” for satisfeita, essa transição será ativada. Caso contrário, uma transição padrão “Falsa” será ativada.

1. Para configurar a condição associada a uma transição, clique no ícone de **[!UICONTROL Abrir caixa de diálogo de personalização]**. Use o editor de expressão para definir as regras necessárias para ativar essa transição. Você também pode utilizar variáveis de evento, condições e funções de data/hora.

   Além disso, você pode modificar o campo **[!UICONTROL Rótulo]** para personalizar o nome da transição na tela de campanha Orquestrada.

   ![](../assets/workflow-test-default.png)

1. Você pode adicionar várias transições de saída a uma atividade **[!UICONTROL Testar]**. Para isso, clique no botão **[!UICONTROL Adicionar condição]** e configure o rótulo e a condição associada para cada transição.
v
1. Durante a execução da campanha orquestrada, cada condição é testada sequencialmente até que uma delas seja atendida. Se nenhuma das condições for atendida, as campanhas Orquestradas continuarão no caminho da **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, a campanha será interrompida nesse ponto.

## Exemplo {#example}

Neste exemplo, transições diferentes são ativadas com base no número de perfis direcionados por uma atividade **[!UICONTROL Criar público-alvo]**:

* Se mais de 10 mil perfis forem direcionados, uma mensagem de email será enviada.
* No caso de mil a 10 mil perfis, um SMS será enviado.
* Se os perfis direcionados ficarem abaixo de mil, eles serão direcionados a uma transição de “não entrar em contato”.

![](../assets/workflow-test-example.png)

Para isso, a variável de evento `vars.recCount` foi utilizada nas condições de “email” e “sms” para contar o número de perfis direcionados e ativar a transição apropriada.

![](../assets/workflow-test-example-config.png)
