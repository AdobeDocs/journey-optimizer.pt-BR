---
solution: Journey Optimizer
product: journey optimizer
title: Combinar direcionamento e experimentação
description: Saiba como combinar direcionamento e experimentos em uma única jornada ou campanha para criar estratégias de otimização sofisticadas.
role: User
level: Intermediate
keywords: otimização, direcionamento, experimentação, combinação, avançado
exl-id: dafcb4d3-e33c-40c5-a5c6-972822a23cc0
TQID: https://experienceleague.adobe.com/klXmy7KQLcIHm-T6BMS1RaMKrwzdCfzvK3KK6fUs7KU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 3%

---

# Combinar direcionamento e experimentação {#combination}

O Journey Optimizer também permite combinar direcionamento e experimentos em uma única jornada ou campanha para criar estratégias mais sofisticadas.

Na verdade, você pode usar o direcionamento para criar várias variantes e, para cada variante, usar a experimentação para otimizar ainda mais cada conteúdo. Isso garante que os experimentos sejam específicos para cada regra de direcionamento e não se estendam entre variantes.

Por exemplo, você pode testar uma &quot;promoção com 50% de desconto&quot; em comparação com um &quot;cartão-presente de 50 dólares&quot; para clientes nos EUA e executar um teste diferente para clientes na Europa, como &quot;frete gratuito em pedidos acima de 50 euros&quot; em comparação com &quot;20% de desconto em sua próxima compra&quot;.

Para combinar o direcionamento e os experimentos em uma jornada ou campanha, siga as etapas abaixo.

1. Crie uma jornada ou campanha onde você define várias regras de direcionamento. [Saiba como](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. Crie um experimento para a primeira regra de direcionamento.

1. Projete e configure seu experimento de conteúdo conforme desejado. [Saiba como](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Depois que a experimentação é definida, ela se aplica somente à primeira regra de direcionamento.

1. De volta à guia **[!UICONTROL Ações]**, selecione **[!UICONTROL Editar conteúdo]**.

1. Para o grupo definido pela primeira regra de direcionamento, é possível definir um conteúdo específico para cada variante do experimento.

   Se você adicionou mais de uma ação de entrada à jornada ou campanha, a mesma combinação de direcionamento e experimento se aplica a cada ação. No entanto, é necessário definir um conteúdo específico para cada variante de cada ação.

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Continue de forma semelhante nas outras regras de direcionamento e projete o conteúdo correspondente para cada variante.

1. Salve as alterações e [ative](../campaigns/review-activate-campaign.md) sua jornada ou campanha.

Quando a jornada/campanha estiver ativa, os usuários de cada grupo direcionado receberão aleatoriamente as diferentes variações de conteúdo definidas para o grupo ao qual pertencem.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->
