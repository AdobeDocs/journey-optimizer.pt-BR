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
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 7%

---


# Configurar a ação de campanha acionada pela API {#api-action}

Use a guia **[!UICONTROL Ações]** para selecionar uma configuração de canal para sua mensagem e definir configurações adicionais, como rastreamento, experimento de conteúdo ou conteúdo multilíngue.

1. **Escolha o canal**.

   Navegue até a guia **[!UICONTROL Ações]**, clique no botão **[!UICONTROL Adicionar ação]** e selecione o canal de comunicação.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.
   >
   >Para campanhas acionadas por API, somente os canais de Email, SMS e Notificação por push estão disponíveis.

1. **Selecionar uma configuração de canal**

   Uma configuração foi definida por um [Administrador do Sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba como definir configurações de canal](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Criar um experimento de conteúdo**

   Use a seção **[!UICONTROL Experimento de conteúdo]** para definir vários tratamentos de entrega para medir qual deles tem melhor desempenho para o público-alvo. Clique no botão **[!UICONTROL Criar experimento]** e siga as etapas detalhadas nesta seção: [Criar um experimento de conteúdo](../content-management/content-experiment.md).

1. **Adicionar conteúdo multilíngue**

   Use a seção **[!UICONTROL Idiomas]** para criar conteúdo em vários idiomas dentro da sua campanha. Para fazer isso, clique no botão **[!UICONTROL Adicionar idiomas]** e selecione as **[!UICONTROL configurações de idioma]** desejadas. Informações detalhadas sobre como configurar e usar recursos multilíngues estão disponíveis nesta seção: [Introdução a conteúdo multilíngue](../content-management/multilingual-gs.md)

Configurações adicionais estão disponíveis, dependendo do canal de comunicação selecionado. Expanda as seções abaixo para obter mais informações.

+++**Aplicar regras de limitação** (Email, Push, SMS)

Na lista suspensa **[!UICONTROL Regras de negócio]**, selecione um conjunto de regras para aplicar regras de limitação à sua campanha. O uso de conjuntos de regras de canal permite definir o limite de frequência por tipo de comunicação para evitar sobrecarga de clientes com mensagens semelhantes. [Saiba como trabalhar com conjuntos de regras](../conflict-prioritization/rule-sets.md)

+++

+++**Rastrear envolvimento** (Email, SMS).

Use a seção **[!UICONTROL Rastreamento de ação]** para acompanhar como seus destinatários reagem às suas entregas de email ou SMS. Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report-cja.md)

+++

+++**Habilitar o modo de entrega rápida** (Push).

O modo de entrega rápida é um complemento do [!DNL Journey Optimizer] que permite o envio muito rápido de mensagens por push em grandes volumes por meio de campanhas. A entrega rápida é usada quando o atraso na entrega da mensagem é essencial para os negócios, quando você deseja enviar um alerta de push urgente em telefones celulares, por exemplo, notícias de última hora para usuários que instalaram seu aplicativo de canal de notícias. Para obter mais informações sobre desempenho ao usar o modo de entrega rápida, consulte a [descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html).

+++

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá criar o conteúdo. [Saiba mais](api-triggered-campaign-content.md)
