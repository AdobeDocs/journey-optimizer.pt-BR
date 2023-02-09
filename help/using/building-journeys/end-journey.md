---
solution: Journey Optimizer
product: journey optimizer
title: Jornada final
description: Saiba como uma jornada termina no Journey Optimizer
feature: Journeys
role: User
level: Beginner
keywords: entrar novamente, jornada, fim, ao vivo, parar
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Encerrar uma jornada{#journey-ending}

Uma jornada pode terminar para um indivíduo em dois contextos específicos:

* A pessoa chega à última atividade de um caminho.
* A pessoa chega em um **Condição** atividade (ou uma **Aguardar** com uma condição) e não corresponde a nenhuma das condições.

A pessoa pode então entrar novamente na jornada se a reentrada for permitida. Consulte [esta página](../building-journeys/journey-gs.md#change-properties)

Para encerrar uma jornada ao vivo, recomendamos que você a feche. A chegada de novos clientes à jornada será bloqueada. Os clientes que já entraram na jornada podem experimentá-la até o fim. Consulte [esta seção](../building-journeys/journey.md#close-journey)

Você só pode interromper uma jornada se ocorrer uma emergência e todo o processamento precisar ser encerrado imediatamente em uma jornada. As pessoas que já entraram em uma jornada são todas interrompidas em seus progressos. Consulte [esta seção](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Observe que não é possível retomar uma jornada fechada ou interrompida.

## Tag final da jornada{#end-tag}

Ao criar uma jornada, uma &quot;tag final&quot; é exibida no final de cada caminho. Este nó não pode ser adicionado por um usuário, não pode ser removido e somente seu rótulo pode ser alterado. Ele marca o fim de cada caminho da jornada. Se a jornada tiver vários caminhos, recomendamos que você adicione um rótulo a cada extremidade para facilitar a leitura dos relatórios. Consulte [esta página](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Fechar uma jornada{#close-journey}

Uma jornada pode ser fechada pelos seguintes motivos:

* A jornada é fechada manualmente por meio do **[!UICONTROL Próximo de novas entradas]** botão.
* Uma jornada baseada em segmento que terminou de ser executada.
* Após a última ocorrência de uma jornada recorrente baseada em segmentos.

Fechar uma jornada manualmente garante que os clientes que já entraram na jornada possam concluir seu caminho, mas os novos usuários não poderão entrar na jornada. Quando uma jornada for fechada (por qualquer um dos motivos acima), ela terá o status **[!UICONTROL Fechado]**. A jornada para de deixar novos indivíduos entrarem na jornada. As pessoas que já estão na jornada podem terminar a jornada normalmente. Após o tempo limite global padrão de 30 dias, a jornada será alternada para a variável **Concluído** status. Consulte esta [seção](../building-journeys/journey-gs.md#global_timeout).

Uma versão de jornada fechada não pode ser reiniciada ou excluída. Você pode criar uma nova versão ou duplicá-la. Somente jornadas concluídas podem ser excluídas.

Para fechar uma jornada da lista de jornadas, clique no botão **[!UICONTROL Elipse]** botão localizado à direita do nome da jornada e selecione **[!UICONTROL Próximo de novas entradas]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. No **[!UICONTROL Jornada]** , clique na jornada que deseja fechar.
1. No canto superior direito, clique na seta para baixo.

   ![](assets/finish_drop_down_list.png)

1. Clique em **[!UICONTROL Próximo de novas entradas]** e confirmar na caixa de diálogo.

## Parar uma jornada{#stop-journey}

Caso precise parar o progresso de todos os indivíduos na jornada, você pode pará-la. Parar a jornada atingirá o tempo limite para todos os indivíduos na jornada. No entanto, parar uma jornada envolve que as pessoas que já entraram em uma jornada são todas interrompidas em seus progressos. A jornada está basicamente desligada. Se você quiser terminar com uma jornada, recomendamos que a feche.

Não é possível reiniciar uma versão de jornada interrompida.

Quando parado, o status da jornada é definido como **[!UICONTROL Parado]**.

Você pode interromper uma jornada, por exemplo, se um profissional de marketing perceber que a jornada direciona o público-alvo errado ou se uma ação personalizada que deveria entregar mensagens não está funcionando corretamente. Para interromper uma jornada da lista de jornadas, clique no botão **[!UICONTROL Elipse]** botão localizado à direita do nome da jornada e selecione **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. No **[!UICONTROL Jornada]** , clique na jornada que deseja parar.
1. No canto superior direito, clique na seta para baixo.
   ![](assets/finish_drop_down_list.png)
1. Clique em **[!UICONTROL Stop]** e confirmar na caixa de diálogo.
