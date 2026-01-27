---
solution: Journey Optimizer
product: journey optimizer
title: Engaje clientes com base na atividade de navegação
description: Engaje clientes com base na atividade de navegação
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 4%

---

# Engaje clientes com base na atividade de navegação {#engage-customers-uc}

>[!BEGINSHADEBOX]

Observe que esse caso de uso começa com um público-alvo que já existe no Experience Platform, especificamente, um público-alvo de comportamento na Web em tempo real que coleta a atividade de navegação à medida que ocorre. [Saiba mais no Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Esquemas necessários para este caso de uso:**

* **Destinatários**: usados como dimensão de direcionamento, com campos: `email`, `churnprop`
* **Lista de desejos**: com campos: `description`, `priceref`, `imageurl`

➡️ [Saiba como configurar esquemas relacionais](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Esta campanha é direcionada aos clientes que navegaram pela categoria de equipamento de exercícios. O público-alvo é desduplicado e segmentado pelo risco de churn, a probabilidade de alguém parar de se envolver ou comprar.

Os clientes de alto risco são reunidos em um novo público-alvo separado que será usado posteriormente para uma comunicação específica, enquanto os clientes de baixo e médio risco passam por uma jornada em várias etapas com emails e acompanhamentos personalizados.

1. Comece configurando uma nova campanha especificamente direcionada a **Reengajamento na lista de desejos**. Isso garante que suas mensagens se concentrem nos clientes que já demonstraram a intenção de compra, salvando os produtos na lista de desejos.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Preencha suas **[!UICONTROL Configurações da campanha]**, como o nome da campanha, a descrição, as datas de início e término e as marcas relevantes.

1. Adicione uma atividade **[!UICONTROL Ler público-alvo]** para selecionar um público-alvo predefinido da Adobe Experience Platform, aqui, clientes que navegaram pela categoria de equipamento para exercícios em seu site.

   Os destinatários são identificados com seus endereços de email selecionados do campo **[!UICONTROL Entidade]**.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Adicione uma atividade **[!UICONTROL Deduplication]** para remover endereços de email duplicados de seu público, garantindo que cada cliente receba apenas uma mensagem.

1. Clique em **[!UICONTROL Adicionar atributo]** e selecione email como o atributo para desduplicação.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Em seguida, adicione uma atividade **[!UICONTROL Split]** para segmentar os clientes de acordo com a probabilidade de churn, permitindo que você forneça experiências personalizadas, personalizadas para cada grupo de clientes.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar segmento]** para criar três grupos:

   * Baixo risco

   * Risco do Medium

   * Alto risco

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Criar filtro]** para definir a probabilidade de churn para cada grupo.

   Use o **Editor de condições** para definir os valores específicos que determinam o risco de churn de cada cliente.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Cada segmento é tratado de forma diferente:

   * [Risco baixo/médio](#low-medium-risk)
   * [Alto risco](#high-risk)

1. Depois que a campanha for testada e estiver pronta, clique em **[!UICONTROL Publicar]** para colocá-la no ar.

Depois da execução da campanha, explore o painel de relatórios para analisar as métricas de desempenho e os principais insights.

➡️ [Saiba mais sobre relatórios](../reports/campaign-global-report-cja.md)

## Segmentos de alto risco {#high-risk}

Para clientes identificados como tendo um alto risco de churn, crie um segmento de público-alvo dedicado. Esse público-alvo é usado posteriormente para comunicação separada e direcionada.

1. Adicione um **[!UICONTROL Salvar público-alvo]**.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Adicione um **[!UICONTROL Rótulo]** ao seu público-alvo e escolha o **[!UICONTROL Campo de mapeamento de perfil]**, aqui **recipients-email**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Esse público-alvo é então salvo no Experience Cloud, onde pode ser usado posteriormente para uma campanha direcionada específica.

## Segmentos de baixo/médio risco {#low-medium-risk}

Para clientes com baixo e médio risco de churn, configure uma campanha em várias etapas com o objetivo de fortalecer o engajamento:

1. Combine riscos Low e Medium com uma atividade **[!UICONTROL Union]**.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Adicione uma atividade **[!UICONTROL Enrichment]** para personalizar a campanha com a Lista de desejos e informações do produto.

1. Clique em **[!UICONTROL Adicionar atributo]** para criar os três atributos a seguir:

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Isso enriquece a mensagem com informações detalhadas da lista de desejos.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Crie um novo público-alvo para redirecionamento com base no engajamento com emails.

   Aqui criamos um público-alvo com base em eventos de cliques em email, para redirecionar todas as pessoas que interagiram com um email enviado anteriormente e, mais especificamente, clicaram em um link dentro dessa mensagem.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Divida o engajamento uniformemente para enviar um acompanhamento por SMS ou notificações por push para incentivar conversões.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Crie o conteúdo da mensagem para cada canal, incluindo atributos de perfil, como o nome do recipient, junto com dados de enriquecimento como itens da Lista de desejos, para personalizar cada mensagem.

   ![](assets/uc-interest-13.png){zoomable="yes"}
