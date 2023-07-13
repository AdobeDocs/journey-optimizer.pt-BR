---
solution: Journey Optimizer
product: journey optimizer
title: Fim da jornada
description: Saiba como uma jornada termina no Journey Optimizer
feature: Journeys
role: User
level: Beginner
keywords: inserir novamente, jornada, finalizar, ao vivo, parar
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Encerrar uma jornada{#journey-ending}

Uma jornada pode terminar para um indivíduo em dois contextos específicos:

* A pessoa chega à última atividade de um caminho.
* A pessoa chega a um **Condição** atividade (ou um **Aguardar** atividade com uma condição) e não corresponde a nenhuma das condições.

A pessoa pode então entrar novamente na jornada se a reentrada for permitida. Consulte [esta página](../building-journeys/journey-gs.md#change-properties)

Para encerrar uma jornada em tempo real, recomendamos que você a feche. A chegada de novos clientes à jornada será então bloqueada. Os clientes que já entraram na jornada podem experimentá-la até o final. Consulte [esta seção](../building-journeys/journey.md#close-journey)

Você só pode interromper uma jornada se ocorrer uma emergência e todo o processamento precisar ser encerrado imediatamente em uma jornada. As pessoas que já entraram em uma jornada são todas interrompidas em seu progresso. Consulte [esta seção](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Observe que não é possível retomar uma jornada fechada ou interrompida.

## Jornada marca de fim{#end-tag}

Ao criar uma jornada, uma &quot;marca de fim&quot; é exibida no final de cada caminho. Este nó não pode ser adicionado por um usuário, não pode ser removido e somente seu rótulo pode ser alterado. Ele marca o fim de cada caminho da jornada. Se a jornada tiver vários caminhos, recomendamos adicionar um rótulo a cada extremidade para facilitar a leitura dos relatórios. Consulte [esta página](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Fechar uma jornada{#close-journey}

Uma jornada pode ser fechada pelos seguintes motivos:

* A jornada é fechada manualmente por meio do **[!UICONTROL Fechar para novas entradas]** botão.
* Uma jornada única baseada em segmento que terminou de ser executada.
* Após a última ocorrência de uma jornada baseada em público-alvo recorrente.

Fechar uma jornada manualmente garante que os clientes que já entraram na jornada possam concluir seu caminho, mas os novos usuários não podem entrar na jornada. Quando uma jornada for fechada (por qualquer um dos motivos acima), ela terá o status **[!UICONTROL Fechado]**. A jornada pára de permitir que novos indivíduos entrem na jornada. As pessoas que já estão na jornada podem terminar a jornada normalmente. Após o tempo limite global padrão de 30 dias, a jornada será alternada para a variável **Concluído** status. Consulte esta [seção](../building-journeys/journey-gs.md#global_timeout).

Uma versão de jornada fechada não pode ser reiniciada ou excluída. Você pode criar uma nova versão ou duplicá-la. Somente as jornadas concluídas podem ser excluídas.

Para fechar uma jornada da lista de jornadas, clique no link **[!UICONTROL Reticências]** botão localizado à direita do nome da jornada e selecione **[!UICONTROL Fechar para novas entradas]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. No **[!UICONTROL Jornadas]** clique na jornada que deseja fechar.
1. No canto superior direito, clique na seta para baixo.

   ![](assets/finish_drop_down_list.png)

1. Clique em **[!UICONTROL Fechar para novas entradas]** e confirme na caixa de diálogo.

## Parar uma jornada{#stop-journey}

Caso precise interromper o progresso de todos os indivíduos na jornada, você pode interrompê-lo. A interrupção da jornada expirará o tempo limite de todos os indivíduos na jornada. No entanto, parar uma jornada envolve que as pessoas que já entraram em uma jornada sejam todas interrompidas em seu progresso. A jornada está basicamente desligada. Se quiser colocar um fim em uma jornada, recomendamos que você a feche.

Uma versão do jornada interrompida não pode ser reiniciada.

Quando interrompido, o status da jornada é definido como **[!UICONTROL Parado]**.

Você pode interromper uma jornada, por exemplo, se um profissional de marketing perceber que a jornada está direcionada ao público errado ou se uma ação personalizada que deveria entregar mensagens não está funcionando corretamente. Para interromper uma jornada da lista de jornadas, clique no link **[!UICONTROL Reticências]** botão localizado à direita do nome da jornada e selecione **[!UICONTROL Parar]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. No **[!UICONTROL Jornadas]** clique na jornada que deseja parar.
1. No canto superior direito, clique na seta para baixo.
   ![](assets/finish_drop_down_list.png)
1. Clique em **[!UICONTROL Parar]** e confirme na caixa de diálogo.
