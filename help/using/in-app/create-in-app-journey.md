---
title: Criar uma notificação no aplicativo em uma Jornada
description: Saiba como criar uma mensagem no aplicativo no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informative"
source-git-commit: 2d3cb7e9981e7df1f2cdd6eff1506fce24a5a962
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 4%

---

# Criar uma mensagem no aplicativo em uma jornada {#create-in-app-journey}

1. Abra a jornada, arraste e solte um **[!UICONTROL No aplicativo]** atividade do **[!UICONTROL Ações]** seção da paleta.

   Quando um perfil atinge o fim da jornada, todas as mensagens no aplicativo exibidas para ele expiram automaticamente. Por esse motivo, uma atividade Wait é adicionada automaticamente após a atividade no aplicativo para garantir o tempo adequado.

   ![](assets/in_app_journey_1.png)

1. Insira um **[!UICONTROL Rótulo]** e **[!UICONTROL Descrição]** para sua mensagem.

1. Escolha o [Superfície no aplicativo](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Agora é possível começar a projetar o conteúdo com o **[!UICONTROL Editar conteúdo]** botão. [Saiba mais](design-in-app.md)

1. Clique em **[!UICONTROL Editar acionador]** para configurar seu Acionador.

   ![](assets/in_app_journey_4.png)

1. No **[!UICONTROL Acionador de mensagem no aplicativo]** escolha o(s) evento(s) e os critérios que acionarão sua mensagem:

   1. Clique em **[!UICONTROL Adicionar condição]** se desejar que o acionador considere vários eventos ou critérios.
   1. No **[!UICONTROL Selecionar um evento]** selecione o tipo de evento para o seu acionador.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL E]** se desejar **ambos** será verdadeiro para que uma mensagem seja exibida ou escolha **[!UICONTROL Ou]** se quiser que a mensagem seja exibida se **ou** dos acionadores são verdadeiros.
   1. Clique em **[!UICONTROL Criar grupo]** para agrupar acionadores.

   ![](assets/in_app_journey_3.png)

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa:

   * **[!UICONTROL Mostrar sempre]**: sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** lista suspensa.
   * **[!UICONTROL Mostrar uma vez]**: mostrar esta mensagem somente na primeira vez que os eventos forem selecionados na **[!UICONTROL Acionador do aplicativo móvel]** lista suspensa.
   * **[!UICONTROL Mostrar até clicar]**: mostrar esta mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** As listas suspensas ocorrem até que um evento de interação seja enviado pelo SDK com uma ação de &quot;clicado&quot;.

1. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

1. Quando a mensagem no aplicativo estiver pronta, finalize a configuração e publique sua jornada para ativá-la.

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

## Limitações de atividades no aplicativo {#in-app-activity-limitations}

* No momento, esse recurso não está disponível para clientes do setor de saúde.

* A personalização pode conter apenas atributos de perfil.

* A exibição no aplicativo está vinculada à duração da jornada, o que significa que, quando a jornada terminar para um perfil, todas as mensagens no aplicativo dentro dessa jornada deixarão de ser exibidas para esse perfil.  Consequentemente, não é possível interromper uma mensagem no aplicativo diretamente de uma atividade do jornada. Em vez disso, você precisará encerrar a jornada inteira para impedir que as mensagens no aplicativo sejam exibidas no perfil.

* No modo de teste, a Exibição no aplicativo depende da duração da jornada. Para evitar que a jornada termine muito cedo durante o teste, ajuste o **[!UICONTROL Tempo de espera]** valor para o seu **[!UICONTROL Aguardar]** atividades.

* **[!UICONTROL Reação]** As atividades do não podem ser usadas para reagir a uma abertura no aplicativo ou a um clique.

* Ocorre um atraso de ativação entre o momento em que um perfil de usuário atinge uma atividade no aplicativo na tela e o momento em que ele começa a ver essa mensagem no aplicativo. Esse atraso pode variar de 15 minutos a 1 hora.

**Tópicos relacionados:**

* [Criar mensagem no aplicativo](design-in-app.md)
* [Teste e envie sua mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)
* [Configuração no aplicativo](inapp-configuration.md)
