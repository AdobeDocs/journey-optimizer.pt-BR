---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade AND-join
description: Saiba como usar a atividade AND-join em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 65%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A atividade **And-join** permite sincronizar várias ramificações de execução de uma campanha orquestrada. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite que você verifique se determinadas atividades foram concluídas antes de continuar a executar a campanha orquestrada."

A atividade **AND-join** é uma atividade de **Controle de fluxo**. Ele permite sincronizar várias ramificações de execução de uma campanha orquestrada.

Essa atividade só acionará a transição de saída depois que todas as transições de entrada estiverem ativadas, ou seja, depois que todas as atividades anteriores estiverem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a campanha orquestrada.

## Configurar a atividade AND-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opções de mesclagem"
>abstract="Selecione de quais atividades deseja juntar. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter."

Siga estas etapas para configurar a atividade **AND-join**:

![](../assets/workflow-andjoin.png)

1. Adicione várias atividades, como atividades de canal, para formar pelo menos duas ramificações de execução diferentes.
1. Adicione uma atividade **AND-join** a qualquer uma das ramificações.
1. Na seção **Opções de mesclagem**, marque todas as atividades anteriores que você deseja mesclar.
1. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter. A transição de saída só pode conter uma das populações de transição de entrada.

## Exemplo{#and-join-example}

O exemplo a seguir mostra duas ramificações de campanha orquestradas com um delivery de email e SMS. A AND-join será acionada quando ambas as transições de entrada estiverem habilitadas. As notificações por push serão enviadas somente após a conclusão de ambas as entregas.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
