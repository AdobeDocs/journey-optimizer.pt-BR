---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Test em suas campanhas orquestradas
description: Saiba como usar a atividade Test
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3d33d0bdbaf5b56a68d4ea708ce023c6aaae4811
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 16%

---

# Teste {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Atividade de teste"
>abstract="A atividade **Teste** é uma atividade de **Controle de fluxo**. Ela permite habilitar transições com base nas condições especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condições"
>abstract="A atividade **Teste** pode ter várias transições de saída. Durante a execução orquestrada da campanha, cada condição é testada sequencialmente até que uma delas seja atendida. Se nenhuma das condições for atendida, a campanha orquestrada continuará no caminho da **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, a campanha orquestrada será interrompida nesse ponto."

A atividade **Teste** é uma atividade de **Controle de fluxo**. Ela permite habilitar transições com base nas condições especificadas.

## Configurar a atividade Test {#test-configuration}

Siga estas etapas para configurar a atividade **Test**:

1. Adicione uma atividade **Test** à sua campanha orquestrada.

1. Por padrão, a atividade **[!UICONTROL Test]** apresenta um teste booleano simples. Se a condição definida na transição &quot;True&quot; for atendida, essa transição será ativada. Caso contrário, uma transição padrão &quot;Falso&quot; será ativada.

1. Para configurar a condição associada a uma transição, clique no ícone **[!UICONTROL Abrir caixa de diálogo de personalização]**. Use o editor de expressão para definir as regras necessárias para ativar essa transição. Você também pode aproveitar variáveis de evento, condições e funções de data/hora.

   Além disso, você pode modificar o campo **[!UICONTROL Rótulo]** para personalizar o nome da transição na tela de campanha orquestrada.

   ![](../assets/workflow-test-default.png)

1. Você pode adicionar várias transições de saída a uma atividade **[!UICONTROL Test]**. Para fazer isso, clique no botão **[!UICONTROL Adicionar condição]** e configure o rótulo e a condição associada para cada transição.
v
1. Durante a execução orquestrada da campanha, cada condição é testada sequencialmente até que uma delas seja atendida. Se nenhuma das condições for atendida, as campanhas orquestradas continuarão no caminho da **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, os fluxos de trabalho serão interrompidos nesse ponto.

## Exemplo {#example}

Neste exemplo, transições diferentes são ativadas com base no número de perfis segmentados por uma atividade **[!UICONTROL Criar público-alvo]**:

* Se mais de 10.000 perfis forem alvos, uma mensagem de email será enviada.
* Para 1.000 a 10.000 perfis, um SMS é enviado.
* Se os perfis direcionados ficarem abaixo de 1.000, serão direcionados para uma transição &quot;não entrar em contato&quot;.

![](../assets/workflow-test-example.png)

Para fazer isso, a variável de evento `vars.recCount` foi aproveitada nas condições &quot;email&quot; e &quot;sms&quot; para contar o número de perfis direcionados e ativar a transição apropriada.

![](../assets/workflow-test-example-config.png)
