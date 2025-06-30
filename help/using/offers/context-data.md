---
product: experience platform
solution: Experience Platform
title: Introdução a dados de contexto
description: Saiba como aproveitar os dados de contexto na gestão de decisões.
badge: label="Herdados" type="Informative"
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 4%

---

# Introdução a dados de contexto {#context-data}

Os dados enviados como parte da solicitação de decisão são considerados dados de contexto. Você pode aproveitar os dados de contexto no mecanismo de decisão, por exemplo, para projetar uma regra de decisão que exija que o tempo atual seja ≥ 80 graus no momento em que a solicitação de decisão é feita.

Os dados de contexto são definidos de forma diferente entre as solicitações de API de **Decisão** e **Decisão do Edge**. Para ambos os tipos de solicitações, os dados de contexto podem ser usados em regras de elegibilidade ou fórmulas de classificação, mas somente as solicitações de API do Edge Decisioning podem usar dados de contexto para personalizar o conteúdo.

Antes de iniciar, verifique as seguintes medidas de proteção e limitações:

* Devido à diferente maneira de transmitir o contexto entre as chamadas do Decisioning e do Edge Decisioning, as regras de elegibilidade baseadas em contexto e as fórmulas de classificação não são intercambiáveis entre as chamadas do Decisioning e do Edge Decisioning.
* O teste com o parâmetro `dryrun` é possível somente com a API de decisão. Não está disponível com a API de decisão do Edge. Observe que a configuração desse parâmetro para `true` com a API de decisão não afeta limites e o número de apresentações.

Informações detalhadas sobre como usar os dados de contexto em cada API estão disponíveis nestas seções:

* [Usar dados de contexto em solicitações do Edge Decisioning](context-data-edge.md)
* [Usar dados de contexto em solicitações de decisão](context-data-decisioning.md)
