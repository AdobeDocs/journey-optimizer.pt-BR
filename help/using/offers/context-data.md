---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introdução a dados de contexto
description: Saiba como aproveitar os dados de contexto na gestão de decisões.
badge: label="Legado" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 12%

---

# Introdução a dados de contexto {#context-data}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../experience-decisioning/gs-experience-decisioning.md)

Os dados enviados como parte da solicitação de decisão são considerados dados de contexto. Você pode aproveitar os dados de contexto no mecanismo de decisão, por exemplo, para projetar uma regra de decisão que exija que o tempo atual seja ≥ 80 graus no momento em que a solicitação de decisão é feita.

Os dados de contexto são definidos de forma diferente entre as solicitações de API de **Decisão** e **Decisão do Edge**. Para ambos os tipos de solicitações, os dados de contexto podem ser usados em regras de elegibilidade ou fórmulas de classificação, mas somente as solicitações de API do Edge Decisioning podem usar dados de contexto para personalizar o conteúdo.

Antes de iniciar, verifique as seguintes medidas de proteção e limitações:

* Devido à diferente maneira de transmitir o contexto entre as chamadas do Decisioning e do Edge Decisioning, as regras de elegibilidade baseadas em contexto e as fórmulas de classificação não são intercambiáveis entre as chamadas do Decisioning e do Edge Decisioning.
* O teste com o parâmetro `dryrun` é possível somente com a API de decisão. Não está disponível com a API de decisão do Edge. Observe que a configuração desse parâmetro para `true` com a API de decisão não afeta limites e o número de apresentações.

Informações detalhadas sobre como usar os dados de contexto em cada API estão disponíveis nestas seções:

* [Usar dados de contexto em solicitações do Edge Decisioning](context-data-edge.md)
* [Usar dados de contexto em solicitações de decisão](context-data-decisioning.md)
