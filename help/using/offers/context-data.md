---
product: experience platform
solution: Experience Platform
title: Introdução aos dados de contexto
description: Saiba como aproveitar os dados de contexto na gestão de decisões.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Introdução aos dados de contexto {#context-data}

Os dados enviados como parte da solicitação de decisão são considerados dados de contexto. Você pode aproveitar os dados de contexto no mecanismo de decisão, por exemplo, para projetar uma regra de decisão que exija que o tempo atual seja ≥ 80 graus no momento em que a solicitação de decisão é feita.

Os dados de contexto são definidos de forma diferente entre as solicitações de API de **Decisão** e **Decisão do Edge**. Para ambos os tipos de solicitações, os dados de contexto podem ser usados em regras de elegibilidade ou fórmulas de classificação, mas somente as solicitações de API do Edge Decisioning podem usar dados de contexto para personalizar o conteúdo.

Antes de iniciar, verifique as seguintes medidas de proteção e limitações:

* Devido à diferente maneira de transmitir o contexto entre as chamadas do Decisioning e do Edge Decisioning, as regras de elegibilidade baseadas em contexto e as fórmulas de classificação não são intercambiáveis entre as chamadas do Decisioning e do Edge Decisioning.
* O teste com o parâmetro `dryrun` é possível somente com a API de decisão. Não está disponível com a API de decisão do Edge. Observe que a configuração desse parâmetro para `true` com a API de decisão não afeta limites e o número de apresentações.

Informações detalhadas sobre como usar os dados de contexto em cada API estão disponíveis nestas seções:

* [Usar dados de contexto em solicitações do Edge Decisioning](context-data-edge.md)
* [Usar dados de contexto em solicitações de decisão](context-data-decisioning.md)

