---
solution: Journey Optimizer
product: journey optimizer
title: Envie atualizações de itens da lista de desejos
description: Envie atualizações de itens da lista de desejos
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 4%

---

# Envie atualizações de itens da lista de desejos {#wishist-uc}

>[!BEGINSHADEBOX]

Embora este exemplo use um esquema **Lista de desejos**, o mesmo método se aplica a qualquer entidade com uma relação um para muitos com **Destinatários**, como **Compras**, **Assinaturas** ou qualquer esquema personalizado no qual cada destinatário possa ter vários registros associados.

**Esquemas necessários para este caso de uso:**

* **Destinatários**: usados como dimensão de direcionamento
* **Itens da lista de desejos**: com campos: `creationDate`, `product`, `Wishlistid`
* **Produto**: com campos: `description`, `priceref`, `imageurl`
* **Carrinhos abandonados** (opcional): com campo: `lastmodified`

➡️ [Saiba como configurar esquemas relacionais](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Essa campanha orquestrada se concentra em reengajar os visitantes, lembrando-os dos produtos salvos na Lista de desejos. Usando o Campaign Orchestration, defina o público-alvo com condições baseadas na atividade da Lista de desejos, ajudando a impulsionar a conversão dos visitantes.

1. Comece criando uma nova campanha especificamente direcionada ao reengajamento na Lista de desejos. Isso ajudará a focalizar as mensagens nos clientes que demonstraram a intenção de compra ao salvar os itens.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Preencha suas **configurações da campanha**.

1. Adicione uma atividade **[!UICONTROL Criar público-alvo]** para identificar o grupo de clientes a serem direcionados com base no comportamento da Lista de desejos.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Defina um **[!UICONTROL Rótulo]** descritivo para este público e escolha **[!UICONTROL Destinatários]** como **[!UICONTROL Dimensão de direcionamento]**. Em seguida, clique em **[!UICONTROL Continuar]** para configurar o público-alvo.

1. Clique em **[!UICONTROL Adicionar condição]** para refinar seu público-alvo criando a seguinte condição:

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
OU
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Esse público-alvo é baseado em recipients que têm uma Lista de desejos, contêm itens com imagens de produtos ou têm um carrinho abandonado no período definido.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Clique em **[!UICONTROL Calcular]** para ver o número de perfis afetados por essas condições e em **[!UICONTROL Exibir resultados]** para inspecionar os detalhes de cada condição e confirmar se o público-alvo corresponde ao segmento de destino.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Clique em **[!UICONTROL Confirmar]**.

1. Adicione uma atividade **[!UICONTROL Enrichment]** para personalizar a campanha com **Lista de desejos** e **informações sobre o produto**.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar dados de enriquecimento]**.

1. Acessar `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Selecione como os dados são coletados. Nesse caso, **[!UICONTROL Colete dados]** para coletar os detalhes da Lista de desejos do seu público.

1. Escolha o número de linhas a serem recuperadas. Por padrão, três itens por Lista de desejos são recuperados, mas isso pode ser ajustado dependendo das necessidades da campanha para destacar mais ou menos produtos.

1. Clique em **[!UICONTROL Adicionar atributo]** para criar os três atributos a seguir:

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Isso enriquece a mensagem com informações detalhadas do produto para gerar conversões.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Adicione uma atividade de email para criar uma mensagem de reengajamento personalizada individualmente para cada cliente. Clique em **[!UICONTROL Editar conteúdo]** para começar a criar seu conteúdo.

   ➡️ [Saiba mais sobre personalização de email](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Depois de finalizar o email, salve e execute a campanha no modo de rascunho clicando em **[!UICONTROL Start]** da sua campanha orquestrada.

1. Depois de iniciar o modo de rascunho, visualize o público-alvo com os detalhes da Lista de desejos.

   Para obter insights mais profundos, clique em um resultado de saída e selecione **[!UICONTROL Visualizar resultados]**.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Depois que a campanha é executada, podemos explorar nossos relatórios, o que nos dá um conjunto robusto de dados e KPIs sobre o desempenho da campanha.

➡️ [Saiba mais sobre relatórios](../reports/campaign-global-report-cja.md)
