---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Associação
description: Saiba como usar a atividade AND-join em uma campanha orquestrada
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 71%

---


# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A atividade **And-join** permite sincronizar várias ramificações de execução de uma campanha Orquestrada. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite que você verifique se determinadas atividades foram concluídas antes de continuar a executar a campanha Orquestrada."

A atividade **[!UICONTROL Associação]** é uma atividade de **[!UICONTROL Controle de fluxo]**. Ele permite sincronizar várias ramificações de execução de uma campanha orquestrada.

Essa atividade só acionará a transição de saída depois que todas as transições de entrada estiverem ativadas, ou seja, depois que todas as atividades anteriores estiverem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a campanha Orquestrada.

## Configurar a atividade AND-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opções de mesclagem"
>abstract="Selecione de quais atividades deseja juntar. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter."

Siga estas etapas para configurar a atividade **[!UICONTROL Associação]**:

![](../assets/workflow-andjoin.png)

1. Adicione várias atividades, como atividades de canal, para criar pelo menos duas ramificações de execução diferentes.

1. Insira uma atividade **[!UICONTROL Associação]** a uma das ramificações.

1. Na seção **[!UICONTROL Opções de mesclagem]**, selecione todas as atividades anteriores que você deseja associar.

1. No menu suspenso **[!UICONTROL Conjunto primário]**, escolha a população de transição de entrada que deseja manter.

## Exemplo{#and-join-example}

Este exemplo ilustra duas ramificações de campanha coordenadas, cada uma com uma entrega de email, uma direcionada a membros ouro e a outra, a membros prata. A **[!UICONTROL Associação]** é ativada assim que ambas as transições de entrada são acionadas, e o SMS é enviado somente após a conclusão de ambas as entregas de email, após um atraso de 7 dias.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
