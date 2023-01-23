---
solution: Journey Optimizer
product: journey optimizer
title: Integração do Adobe Analytics
description: Saiba como aproveitar os dados do Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics, integração, web sdk, plataforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 10%

---

# Integração do Adobe Analytics {#analytics-data}

## Aproveite os dados do Adobe Analytics ou do SDK da Web {#leverage-analytics-data}

Você pode aproveitar todos os dados de evento comportamental da Web (por meio do Adobe Analytics ou do SDK da Web) que já estão sendo capturados e transmitidos no Adobe Experience Platform para acionar jornadas e automatizar experiências para seus clientes.

>[!NOTE]
>
>Esta seção se aplica somente a eventos com base em regras e clientes que precisam usar dados do Adobe Analytics ou do WebSDK.

Para que isso funcione com o Adobe Analytics, é necessário ativar, no Adobe Experience Platform, o conjunto de relatórios que deseja usar. Para fazer isso, siga as etapas abaixo:

1. Conecte-se ao Adobe Experience Platform e navegue até **[!UICONTROL Fontes]**.

1. Na seção Adobe Analytics , selecione **[!UICONTROL Adicionar dados]**

   ![](assets/ajo-aa_1.png)

1. Na lista de report suites disponíveis do Adobe Analytics, selecione o **[!UICONTROL Conjunto de relatórios]** para ativar. Em seguida, clique em **[!UICONTROL Próximo]**.

   ![](assets/ajo-aa_2.png)

1. Escolha se deseja usar um esquema Padrão ou Personalizado.

1. No **[!UICONTROL Detalhes do fluxo de dados]** , escolha uma **[!UICONTROL Nome do fluxo de dados]**.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Concluir]**.

   ![](assets/ajo-aa_3.png)

Isso ativa o conector de origem do Analytics para esse conjunto de relatórios. Sempre que os dados entram, eles são transformados em um evento de Experiência e enviados para o Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Saiba mais sobre o conector de origem do Adobe Analytics em  [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=pt-BR){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=pt-BR){target="_blank"}.

## Criar uma jornada com um evento usando dados do Adobe Analytics ou do SDK da Web {#event-analytics}

Após implementar sua integração com o Adobe Analytics com a [Fontes Adobe Analytics](#leverage-analytics-data) ou com a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR), é possível criar um evento que pode ser usado posteriormente em uma jornada.

Neste exemplo, vamos direcionar os usuários que adicionaram um produto aos carrinhos:

* Se o pedido for concluído, eles receberão um email de acompanhamento dois dias depois para solicitar feedback.
* Se o pedido não estiver concluído, eles receberão um email para lembrá-los de concluir o pedido.

1. No Adobe Journey Optimizer, acesse o **[!UICONTROL Configuração]** menu.

1. Em seguida, selecione **[!UICONTROL Gerenciar]** do **[!UICONTROL Eventos]** cartão.

   ![](assets/ajo-aa_5.png)

1. Clique em **[!UICONTROL Criar evento]**. O painel de configuração do evento é aberto no lado direito da tela.

1. Preencha o **[!UICONTROL Evento]** parâmetros:

   * **[!UICONTROL Nome]**: Personalize o nome do seu **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: Escolha a **[!UICONTROL Unitário]** Tipo. [Saiba mais](../event/about-events.md)
   * **[!UICONTROL Tipo de ID de evento]**: Escolha a **[!UICONTROL Baseado em regras]** Tipo de ID de evento. [Saiba mais](../event/about-events.md#event-id-type)
   * **[!UICONTROL Esquema]**: Selecione o esquema Analytics ou WebSDK criado na seção acima.
   * **[!UICONTROL Campos]**: Selecione os campos Carga. [Saiba mais](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condição de ID de evento]**: Defina a condição que será usada pelo sistema para identificar os eventos que acionarão sua jornada.

      Aqui, o Evento é acionado quando os clientes adicionam um item ao carrinho.
   * **[!UICONTROL Identificador de perfil]**: Escolha um campo nos campos de carga útil ou defina uma fórmula para identificar a pessoa associada ao evento.

   ![](assets/ajo-aa_6.png)

1. Quando configurado, selecione **[!UICONTROL Salvar]**. Seu evento agora está pronto para ser usado em uma jornada.

1. No **[!UICONTROL Jornada]**, agora é possível começar a criar a jornada. Para obter mais informações, consulte [esta seção](../building-journeys/journey-gs.md).

1. Adicione à jornada os eventos do Analytics configurados anteriormente.

   ![](assets/ajo-aa_8.png)

1. Adicione um Evento que será acionado se um pedido for concluído.

1. Em seu **[!UICONTROL Menu Evento]**, selecione o **[!UICONTROL Definir o tempo limite do evento]** e **[!UICONTROL Definir um caminho de tempo limite]** opções.

   ![](assets/ajo-aa_9.png)

1. No caminho de tempo limite, adicione um **[!UICONTROL Email]** ação. Esse caminho será usado para enviar um email para clientes que não concluíram um pedido para lembrá-los de que seus carrinhos ainda estão disponíveis.

1. Adicione um **[!UICONTROL Aguardar]** atividade após o caminho principal e defina-o para a duração necessária.

   ![](assets/ajo-aa_10.png)

1. Em seguida, adicione um **[!UICONTROL Ação de email]**. Neste email, os clientes serão solicitados a fornecer feedback sobre o pedido colocado.

Agora você pode publicar sua jornada após testar sua validade. [Saiba mais](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
