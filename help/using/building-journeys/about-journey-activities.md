---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às atividades de jornada
description: Introdução às atividades de jornada
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: jornada, atividades, introdução, eventos, ação
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 527a539272460aa6aa22de5bb3da2223521ee2a3
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 15%

---

# Introdução às atividades de jornada {#about-journey-activities}

Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

## Atividades de evento {#event-activities}

As jornadas personalizadas são acionadas por eventos, como uma compra online. Depois que um perfil entra em uma jornada, ele se move como um indivíduo e nenhum dos dois indivíduos se move ao longo da mesma taxa ou ao longo do mesmo caminho. Ao iniciar a jornada com um evento, a jornada é acionada quando o evento é recebido. Cada pessoa na jornada segue, individualmente, as próximas etapas definidas na jornada.

Os eventos configurados pelo usuário técnico (consulte [esta página](../event/about-events.md)) são todos exibidos na primeira categoria da paleta, no lado esquerdo da tela. As seguintes atividades de evento estão disponíveis:

* [Eventos gerais](../building-journeys/general-events.md)
* [Reação](../building-journeys/reaction-events.md)
* [Qualificação de público-alvo](../building-journeys/audience-qualification-events.md)

![Paleta de atividades de evento no designer de jornada](assets/journey43.png)

Para iniciar a jornada, arraste e solte uma atividade de evento. Você também pode clicar duas vezes nela.

![Arraste e solte a atividade de evento no designer de jornada](assets/journey44.png)

## Atividades de orquestração {#orchestration-activities}

As atividades de orquestração são condições diferentes que ajudam a determinar a próxima etapa da jornada. Essas condições podem incluir se a pessoa tem um caso de suporte aberto, a previsão do tempo em seu local atual, se concluiu uma compra ou se atingiu 10.000 pontos de fidelidade.

Na paleta, no lado esquerdo da tela, as seguintes atividades de orquestração estão disponíveis:

* [Condição](../building-journeys/condition-activity.md)
* [Aguardar](../building-journeys/wait-activity.md)
* [Ler público-alvo](../building-journeys/read-audience.md)

![Paleta de atividades de orquestração no designer de jornada](assets/journey49.png)

## Atividades de ação {#action-activities}

As ações são o que você deseja que aconteça como resultado de algum tipo de acionador, como o envio de uma mensagem. É a parte da jornada que o cliente experimenta.

Na paleta, no lado esquerdo da tela, abaixo de **[!UICONTROL Eventos]** e **[!UICONTROL Orquestração]**, você pode encontrar a categoria **[!UICONTROL Ações]**. As seguintes atividades de ação estão disponíveis:

* [Ações de canal integradas](../building-journeys/journeys-message.md)
* [Ações personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![Paleta de atividades de ação no designer de jornada](assets/journey58.png)

Essas atividades representam os diferentes canais de comunicação disponíveis. É possível combiná-los para criar um cenário entre canais.

Você também pode configurar ações específicas para enviar mensagens:

* Se você estiver usando um sistema de terceiros para enviar mensagens, poderá criar uma ação personalizada específica. [Saiba mais](../action/action.md)

* Se estiver trabalhando com o Campaign e o Journey Optimizer, consulte estas seções:

   * [[!DNL Journey Optimizer] e o Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)
   * [[!DNL Journey Optimizer] e Marketo Engage](../action/marketo-engage.md)

## Práticas recomendadas {#best-practices}

### Adicionar um rótulo

A maioria das atividades permite definir um **[!UICONTROL Rótulo]**. Isso adiciona um sufixo ao nome que aparece em sua atividade na tela. Isso é útil se você usar a mesma atividade várias vezes na jornada e quiser identificá-la mais facilmente. Também facilita a depuração em caso de erro e facilita a leitura dos relatórios. Você também pode adicionar uma **[!UICONTROL Descrição]** opcional.

![Campos de rótulo e descrição nas propriedades da atividade de jornada](assets/journey-action-label.png)

>[!NOTE]
>
>Para algumas atividades, a ID também está visível no painel. Essa ID pode ser usada nos relatórios como uma chave mais estável do que o rótulo, que pode mudar.

### Gerenciar os parâmetros avançados {#advanced-parameters}

A maioria das atividades do exibe vários parâmetros avançados e/ou técnicos que você não pode modificar.

![Campos de parâmetros avançados nas propriedades da atividade de jornada](assets/journey-advanced-parameters.png)

Para melhorar a compreensão, oculte esses parâmetros usando o botão **[!UICONTROL Ocultar campos somente leitura]**.

![Ocultar o ícone de campos somente leitura nas propriedades da atividade de jornada](assets/journey-hide-read-only-fields.png)

Em alguns contextos específicos, é possível substituir os valores desses parâmetros para uso específico. Para forçar um valor, clique no ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo. [Saiba mais](../configuration/primary-email-addresses.md#journey-parameters)

![Habilitar a opção de substituição de parâmetro nas propriedades da atividade de email](assets/journey-enable-parameter-override.png)

### Adicionar um caminho alternativo

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. A única maneira de fazê-lo continuar é marcar a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

![Adicionar uma opção de caminho alternativo nas propriedades da atividade de Condição](assets/journey42.png)

## Solução de problemas {#troubleshooting}

Antes de testar e publicar sua jornada, verifique se todas as atividades estão configuradas corretamente. Não é possível executar testes ou publicações se os erros ainda forem detectados pelo sistema.

Saiba como solucionar erros nas atividades e na jornada [nesta página](troubleshooting.md).
