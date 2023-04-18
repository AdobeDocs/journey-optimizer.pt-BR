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
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 3%

---

# Criar uma mensagem no aplicativo em uma Jornada {#create-in-app-journey}

>[!AVAILABILITY]
>
>A atividade no aplicativo está disponível atualmente como um beta para selecionar somente usuários. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

1. Abra a jornada e arraste e solte uma **[!UICONTROL No aplicativo]** da **[!UICONTROL Ações]** da paleta.

   Quando um perfil atingir o fim de sua jornada, todas as mensagens no aplicativo exibidas a ele expirarão automaticamente. Por esse motivo, uma atividade Wait é adicionada automaticamente após a atividade In-app para garantir o tempo adequado.

   ![](assets/in_app_journey_1.png)

1. Insira um **[!UICONTROL Rótulo]** e **[!UICONTROL Descrição]** para sua mensagem.

1. Escolha a [Superfície do aplicativo](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Agora você pode começar a projetar seu conteúdo com a variável **[!UICONTROL Editar conteúdo]** botão. [Saiba mais](design-in-app.md)

1. Clique em **[!UICONTROL Editar acionador]** para configurar o Acionador.

   ![](assets/in_app_journey_4.png)

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa:

   * **[!UICONTROL Mostrar sempre]**: Sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Mostrar uma vez]**: Mostrar esta mensagem somente na primeira vez que os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Mostrar até o click-through]**: Mostrar esta mensagem quando os eventos forem selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre até que um evento de interação seja enviado pelo SDK com uma ação &quot;clicada&quot;.

1. No **[!UICONTROL Acionador do aplicativo móvel]** selecione os eventos e critérios que acionarão sua mensagem:

   1. Na lista suspensa esquerda, selecione o evento necessário para acionar a mensagem.
   1. Na lista suspensa direita, selecione a validação necessária no evento selecionado.
   1. Clique no botão **[!UICONTROL Adicionar]** se desejar que o acionador considere vários eventos ou critérios. Em seguida, repita as etapas acima.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL E]** se desejar **both** aciona como true para que uma mensagem seja exibida ou escolha **[!UICONTROL Ou]** se quiser que a mensagem seja exibida, se **ou** dos acionadores são verdadeiros.
   1. Clique em **[!UICONTROL Salvar]** quando os Triggers tiverem sido configurados.

   ![](assets/in_app_journey_3.png)

1. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

1. Quando a mensagem no aplicativo estiver pronta, finalize a configuração e publique a jornada para ativá-la.

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

## Limitações da atividade no aplicativo {#in-app-activity-limitations}

* No momento, esse recurso não está disponível para clientes do Healthcare.

* A personalização só pode conter atributos de perfil.

* A exibição no aplicativo está vinculada ao tempo de vida da jornada, o que significa que quando a jornada terminar para um perfil, todas as mensagens no aplicativo dentro dessa jornada deixarão de ser exibidas para esse perfil.  Consequentemente, não é possível parar uma mensagem no aplicativo diretamente de uma atividade do jornada. Em vez disso, será necessário encerrar a jornada inteira para impedir que as mensagens no aplicativo sejam exibidas no perfil.

* No modo de teste, a exibição no aplicativo depende da duração da jornada. Para evitar que a jornada termine muito cedo durante o teste, ajuste a **[!UICONTROL Tempo de espera]** para seu **[!UICONTROL Aguardar]** atividades.

* **[!UICONTROL Reação]** não podem ser usadas para reagir a uma abertura ou clique no aplicativo.

* Um atraso de ativação ocorre entre o momento em que um perfil de usuário atinge uma atividade no aplicativo na tela e o momento em que ele começa a ver essa mensagem no aplicativo. Esse atraso pode variar de 15 minutos a 1 hora.

**Tópicos relacionados:**

* [Criar mensagem no aplicativo](design-in-app.md)
* [Teste e envie a mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)
* [Configuração no aplicativo](inapp-configuration.md)
