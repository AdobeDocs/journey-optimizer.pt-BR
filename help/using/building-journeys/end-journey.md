---
solution: Journey Optimizer
product: journey optimizer
title: Fim da jornada
description: Saiba como uma jornada termina no Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: inserir novamente, jornada, encerrar, ao vivo, parar
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: a7468879b36dfe9184471824b387f1638fae3d50
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Encerrar uma jornada {#journey-ending}

## Como uma jornada ativa termina

As jornadas são fechadas quando o tempo limite da jornada global é atingido ou após a última ocorrência de uma jornada recorrente baseada no público-alvo. [Saiba como as jornadas são fechadas](#close-journey).

Se precisar encerrar uma jornada em tempo real, recomendamos que [você a feche](#close-to-new-entrances) manualmente. A chegada de novos clientes à jornada é então bloqueada. Os perfis que já entraram na jornada podem experimentá-la até o fim.

Você também pode [parar uma jornada](#stop-journey), somente em caso de emergência e se todo o processamento da jornada precisar ser finalizado imediatamente. As pessoas que já entraram em uma jornada são todas interrompidas em seu progresso.

>[!IMPORTANT]
>
>* Não é possível reiniciar ou excluir uma jornada [fechada](#close-journey) ou [interrompida](#stop-journey). Você pode [criar uma nova versão](publishing-the-journey.md#journey-versions-journey-versions) ou [duplicá-la](journey-ui.md#duplicate-a-journey-duplicate-a-journey).
>
>* Somente as jornadas concluídas podem ser excluídas.

## Como os perfis encerram uma jornada

Uma jornada termina para um indivíduo em dois contextos específicos:

* O indivíduo atinge a última atividade de um caminho e, em seguida, se move para a [Marca de fim](#end-tag).
* O indivíduo atinge uma atividade de **Condição** (ou uma atividade de **Espera** com uma condição) e não corresponde a nenhuma das condições.

O indivíduo pode então entrar novamente na jornada se a reentrada for permitida. [Saiba mais sobre o gerenciamento de entrada/reentrada](../building-journeys/journey-properties.md#entrance)

## Jornada marca de fim {#end-tag}

Ao criar uma jornada, uma tag End é exibida no final de cada caminho. Este nó não pode ser adicionado por um usuário, não pode ser removido e somente seu rótulo pode ser alterado. Ele marca o fim de cada caminho da jornada.

Se a jornada tiver vários caminhos, recomendamos adicionar um rótulo a cada extremidade para facilitar a leitura dos relatórios. Saiba mais sobre [relatórios do jornada](../reports/live-report.md).

![](assets/journey-end.png)

## Fechar uma jornada {#close-journey}

Uma jornada pode ser fechada pelos seguintes motivos:

* Uma jornada única baseada em segmento que terminou de ser executada e atingiu o tempo limite global de 91 dias.
* Após a última ocorrência de uma jornada recorrente baseada no público-alvo.
* A jornada é fechada manualmente pelo botão [**[!UICONTROL Fechar para novas entradas]**](#close-to-new-entrances).

Após o tempo limite global de **jornada de 91 dias**, uma jornada Ler público alterna para o status **Concluído**. Esse comportamento é definido para 91 dias somente, pois todas as informações sobre os perfis que entraram na jornada são removidas 91 dias após terem entrado. As pessoas que ainda estão na jornada são afetadas automaticamente. Eles saem da jornada após o tempo limite de 91 dias.  Saiba mais sobre [o tempo limite global do jornada](../building-journeys/journey-properties.md#global_timeout).

>[!TIP]
>
>Uma jornada única baseada em segmento mantém o status do **Live** mesmo após ser executada uma vez. Os perfis não podem ser reinseridos após a conclusão, mas a jornada permanece com o status **Ativo** até que o tempo limite global padrão expire. Você pode fechá-lo manualmente antes usando a opção **Fechar para novas entradas**.

### Fechar para novas entradas {#close-to-new-entrances}

Fechar uma jornada manualmente garante que os clientes que já entraram na jornada possam concluir seu caminho, mas os novos usuários não podem entrar na jornada. Quando uma jornada for fechada (por qualquer um dos motivos acima), ela terá o status **[!UICONTROL Fechada]**. A jornada pára de permitir que novos indivíduos entrem na jornada. Os perfis que já estão na jornada jornada podem concluí-la normalmente. Após o tempo limite global padrão de 91 dias, a jornada mudará para o status **Concluído**.

Para fechar uma jornada da lista de jornadas, clique no botão **[!UICONTROL Reticências]** localizado à direita do nome da jornada e selecione **[!UICONTROL Fechar para novas entradas]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. Na lista **[!UICONTROL Jornadas]**, clique na jornada que deseja fechar.
1. No canto superior direito, clique na seta para baixo.

   ![](assets/finish_drop_down_list.png){width="50%" align="left" zoomable="yes"}

1. Clique em **[!UICONTROL Fechar para novas entradas]** e confirme na caixa de diálogo.




## Parar uma jornada {#stop-journey}

Caso precise interromper o progresso de todos os indivíduos na jornada, você pode interrompê-lo. Interromper o tempo limite da jornada para todos os indivíduos na jornada. No entanto, parar uma jornada envolve que as pessoas que já entraram em uma jornada sejam todas interrompidas em seu progresso. A jornada está basicamente desligada. Se você deseja terminar com uma jornada, a prática recomendada é [fechá-la](#close-journey).


Você pode interromper uma jornada, por exemplo, se um profissional de marketing perceber que a jornada está direcionada ao público errado ou se uma ação personalizada que deveria entregar mensagens não está funcionando corretamente. Para interromper uma jornada da lista de jornadas, clique no botão **[!UICONTROL Reticências]** localizado à direita do nome da jornada e selecione **[!UICONTROL Parar]**.

![](assets/journey-finish-quick-action.png)

Você também pode:

1. Na lista **[!UICONTROL Jornadas]**, clique na jornada que deseja parar.
1. No canto superior direito, clique na seta para baixo.

   ![](assets/finish_drop_down_list2.png){width="50%" align="left" zoomable="yes"}

1. Clique em **[!UICONTROL Parar]** e confirme na caixa de diálogo.

Quando parado, o status da jornada é definido como **[!UICONTROL Parado]**.
