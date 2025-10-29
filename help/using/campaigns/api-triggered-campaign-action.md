---
solution: Journey Optimizer
product: journey optimizer
title: Configurar a ação de campanha acionada pela API
description: Saiba como configurar a ação de campanha acionada pela API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: 322e035c-7370-40c9-b1cb-3428bc26e874
source-git-commit: afac93abcd2bacc4371748b94c0e66942a4c5076
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 50%

---

# Configurar a ação de campanha acionada pela API {#api-action}

Use a guia **[!UICONTROL Ações]** para selecionar uma configuração de canal para a sua mensagem e definir configurações adicionais, como rastreamento, experimento de conteúdo ou conteúdo multilíngue.

1. **Escolha o canal**.

   Navegue até a guia **[!UICONTROL Ações]**, clique no botão **[!UICONTROL Adicionar ação]** e selecione o canal de comunicação.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >Para obter mais informações sobre os canais com suporte, consulte a tabela nesta seção: [Canais em jornadas e campanhas](../channels/gs-channels.md#channels). Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.
   >
   >Atualmente, as campanhas acionadas pela API de alta taxa de transferência são compatíveis apenas com o canal de email.

1. **Selecionar uma configuração de canal**

   Uma configuração é definida por um [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba como definir configurações de canal](../configuration/channel-surfaces.md)

   ![](assets/api-triggered-create-campaign-action.png)

1. **Aproveitar Otimização**

   Use a seção **[!UICONTROL Otimização de Mensagens]** para executar experimentos de conteúdo, aproveitar regras de direcionamento ou usar combinações avançadas de experimentação e direcionamento. Essas diferentes opções e as etapas a serem seguidas estão detalhadas nesta seção: [Otimização em campanhas](campaigns-message-optimization.md).
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **Adicionar conteúdo multilíngue**

   Use a seção **[!UICONTROL Idiomas]** para criar conteúdo em vários idiomas dentro da sua campanha. Para isso, clique no botão **[!UICONTROL Adicionar idiomas]** e selecione as **[!UICONTROL Configurações de idioma]** desejadas. Informações detalhadas sobre como configurar e usar recursos multilíngues estão disponíveis nesta seção: [Introdução a conteúdo multilíngue](../content-management/multilingual-gs.md)

Configurações adicionais estão disponíveis, dependendo do canal de comunicação selecionado. Expanda as seções abaixo para obter mais informações.

+++**Aplicar regras de limitação** (Email, Push, SMS)

Na lista suspensa **[!UICONTROL Regras de negócio]**, selecione um conjunto de regras para aplicar regras de limitação à sua campanha. O uso de conjuntos de regras de canal permite definir o limite de frequência por tipo de comunicação para evitar sobrecarga de clientes com mensagens semelhantes. [Saiba como trabalhar com conjuntos de regras](../conflict-prioritization/rule-sets.md)

+++

+++**Rastrear envolvimento** (Email, SMS).

Use a seção de **[!UICONTROL Rastreamento de ações]** para acompanhar como os seus destinatários reagem às suas entregas de email ou SMS. Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre os relatórios da campanha](../reports/campaign-global-report-cja.md)

+++

+++**Habilitar o modo de entrega rápida** (Push).

O modo de entrega rápida é um complemento do [!DNL Journey Optimizer] que permite um envio muito rápido de mensagens por push em grandes volumes por meio das campanhas. A entrega rápida é usada quando um atraso na entrega das mensagens seria crítico para os negócios, quando você deseja enviar um alerta por push urgente a telefones celulares, como, por exemplo, notícias de última hora para usuários que instalaram o seu aplicativo de canal de notícias. Saiba como habilitar o modo de entrega rápida para notificações por push [nesta página](../push/create-push.md#rapid-delivery).

Para mais informações sobre desempenho ao usar o modo de entrega rápida, consulte a [descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá criar o conteúdo. [Saiba mais](api-triggered-campaign-content.md)
