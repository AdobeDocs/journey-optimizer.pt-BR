---
solution: Journey Optimizer
product: journey optimizer
title: Integração do Adobe Analytics
description: Saiba como aproveitar os dados do Adobe Analytics no Journey Optimizer
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analytics, integração, sdk da web, plataforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 5%

---

# Trabalhar com dados do Adobe Analytics {#analytics-data}

Você pode aproveitar todos os dados de evento comportamental da Web que já estão sendo capturados por meio do Adobe Analytics ou do Web SDK e streaming no Adobe Experience Platform, a fim de acionar jornadas e automatizar experiências para seus clientes.

Para que isso funcione com o Adobe Analytics, é necessário:

1. Ative o conjunto de relatórios que deseja usar. [Saiba mais](#leverage-analytics-data)
1. Ative o Journey Optimizer para usar sua fonte de dados do Adobe Analytics. [Saiba mais](#activate-analytics-data)
1. Adicione um evento específico na jornada. [Saiba mais](#event-analytic)

>[!NOTE]
>
>Essa seção se aplica somente a eventos com base em regras e clientes que precisam usar dados do Adobe Analytics ou do Web SDK.
> 
>Se você estiver usando o Adobe Customer Journey Analytics, consulte [esta página](../reports/cja-ajo.md).
>

## Configurar dados do Adobe Analytics ou da Web SDK {#leverage-analytics-data}

Os dados provenientes do Adobe Analytics ou do Adobe Experience Platform Web SDK precisam estar habilitados para serem usados em suas jornadas.

Para fazer isso, siga as etapas abaixo:

1. Navegue até o menu **[!UICONTROL Fontes]**.

1. Na seção Adobe Analytics, selecione **[!UICONTROL Adicionar dados]**

   ![](assets/ajo-aa_1.png)

1. Na lista de conjuntos de relatórios do Adobe Analytics disponíveis, selecione o **[!UICONTROL Conjunto de relatórios]** para habilitar. Em seguida, clique em **[!UICONTROL Avançar]**.

   ![](assets/ajo-aa_2.png)

1. Escolha se deseja usar um esquema Padrão ou Personalizado.

1. Na tela **[!UICONTROL Detalhes do fluxo de dados]**, escolha um **[!UICONTROL Nome do fluxo de dados]**.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Concluir]**.

   ![](assets/ajo-aa_3.png)

Isso ativa o conector de origem do Analytics para esse conjunto de relatórios. Sempre que os dados entram, são transformados em um evento de experiência e enviados para o Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Saiba mais sobre o conector de origem do Adobe Analytics na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target="_blank"} e no [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target="_blank"}.

## Ativar esta configuração {#activate-analytics-data}

Depois que essa configuração for concluída, entre em contato com o Adobe para ativar o ambiente Journey Optimizer para usar essa fonte de dados. Essa etapa só é necessária para fontes de dados do Adobe Analytics. Para fazer isso:

1. Obtenha a ID da fonte de dados. Essas informações estão disponíveis na interface do usuário: navegue até a fonte de dados criada na guia **Fluxos de Dados** do menu **Fontes**. A maneira mais fácil de encontrar é filtrar por fontes do Adobe Analytics.
1. Entre em contato com o Atendimento ao cliente da Adobe com os seguintes detalhes:

   * Assunto: Ativar eventos do Adobe Analytics para jornada

   * Conteúdo: ative meu ambiente para usar eventos AA.

      * ID da organização: &quot;XXX@AdobeOrg&quot;

      * ID da fonte de dados: &quot;ID: xxxxx&quot;

1. Depois de ter uma confirmação de que o ambiente está pronto, você poderá usar os dados do Adobe Analytics nas jornadas.

## Criar uma jornada com um evento usando dados do Adobe Analytics ou do Web SDK {#event-analytics}

Agora é possível criar um evento com base nos dados do Adobe Analytics ou do Adobe Experience Platform Web SDK para ser usado em uma jornada.

No exemplo abaixo, saiba como direcionar usuários que adicionaram um produto aos carrinhos:

* Se o pedido for concluído, os usuários receberão um email de acompanhamento dois dias depois para solicitar feedback.
* Se o pedido não for concluído, os usuários receberão um email para lembrá-los de concluí-lo.

1. No Adobe Journey Optimizer, acesse o menu **[!UICONTROL Configuração]**.

1. Em seguida, selecione **[!UICONTROL Gerenciar]** no cartão **[!UICONTROL Eventos]**.

   ![](assets/ajo-aa_5.png)

1. Clique em **[!UICONTROL Criar evento]**. O painel de configuração do evento é aberto no lado direito da tela.

1. Preencha os parâmetros **[!UICONTROL Event]**:

   * **[!UICONTROL Nome]**: personalize o nome do seu **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: escolha o Tipo **[!UICONTROL Unitário]**. [Saiba mais](../event/about-events.md)
   * **[!UICONTROL Tipo de ID do Evento]**: escolha o **[!UICONTROL Tipo de ID do Evento baseado em Regras]**. [Saiba mais](../event/about-events.md#event-id-type)
   * **[!UICONTROL Esquema]**: selecione o esquema do Analytics ou do WebSDK [criado antes](#leverage-analytics-data).
   * **[!UICONTROL Campos]**: selecione os campos de Carga. [Saiba mais](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condição de ID de Evento]**: defina a condição para identificar os eventos que dispararão sua jornada.

     Aqui, o Evento é acionado quando os clientes adicionam um item aos carrinhos.
   * **[!UICONTROL Identificador de perfil]**: escolha um campo nos campos de carga ou defina uma fórmula para identificar a pessoa associada ao evento.

   ![](assets/ajo-aa_6.png)

1. Quando configurado, selecione **[!UICONTROL Salvar]**.

Agora que o evento está pronto, crie uma jornada para usá-lo.

1. No menu **[!UICONTROL Jornadas]**, abra ou crie uma jornada. Para obter mais informações, consulte [esta seção](../building-journeys/journey-gs.md).

1. Adicione o evento do Analytics configurado anteriormente à jornada.

   ![](assets/ajo-aa_8.png)

1. Adicione um evento que será acionado se um pedido for concluído.

1. No **[!UICONTROL menu Evento]**, selecione as opções **[!UICONTROL Definir o tempo limite do evento]** e **[!UICONTROL Definir um caminho de tempo limite]**.

   ![](assets/ajo-aa_9.png)

1. No caminho de tempo limite, adicione uma ação **[!UICONTROL Email]**. Esse caminho será usado para enviar um email aos clientes que não concluíram um pedido para lembrá-los de que seus carrinhos ainda estão disponíveis.

1. Adicione uma atividade **[!UICONTROL Wait]** após o caminho principal e defina-a com a duração necessária.

   ![](assets/ajo-aa_10.png)

1. Em seguida, adicione uma **[!UICONTROL Ação de email]**. Neste e-mail, os clientes serão solicitados a fornecer feedback sobre o pedido feito.

Agora você pode testar e publicar sua jornada. [Saiba mais](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
