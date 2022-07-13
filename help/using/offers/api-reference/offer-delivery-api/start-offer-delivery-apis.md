---
title: Introdução às APIs de entrega de oferta
description: Saiba mais sobre as APIs disponíveis para fornecer ofertas personalizadas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 4%

---

# Introdução às APIs de entrega de oferta {#about-decisioning-apis}

Você pode fornecer ofertas usando a variável **Decisão** ou **Edge Decisioning** API. Além disso, a variável **Decisão em lote** A API permite fornecer ofertas a todos os perfis em um determinado segmento em uma chamada. O conteúdo da oferta para cada perfil no segmento é colocado em um conjunto de dados do Adobe Experience Platform, onde está disponível para fluxos de trabalho em lote personalizados.

Nesta página, você encontrará informações sobre funcionalidades específicas disponíveis com o **Decisão** e **Edge Decisioning** APIs. Embora ambos permitam que você entregue ofertas aos seus clientes, recomendamos usar a variável **Edge Decisioning** API sempre que possível para casos de uso de entrada e para garantir melhor latência e throughput na plataforma.

|  | Solicitações/s | Latência |
|---|---|---|
| API de decisão | 2000 | &lt;500ms |
| API de decisão do Edge | 5000 | &lt;250ms |

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:
* [API de decisão](decisioning-api.md)
* [API de decisão do Edge](edge-decisioning-api.md)
* [API de decisão em lote](batch-decisioning-api.md)

## Recursos da API do Edge Decisioning {#edge}

**Solicitação exclusiva para eventos de experiência e solicitações de decisão**

Com a API do Edge Decisioning, você pode enviar em uma única solicitação o evento de experiência juntamente com a solicitação de decisão, em vez de ter duas solicitações diferentes.

Por exemplo, se um cliente visitar seu site, a solicitação incluirá o evento de experiência (a visita do cliente à página) e obterá uma oferta de volta para preencher a página visitada.

**Armazenamento de dados de contexto no Adobe Experience Platform**

Os dados de contexto se referem a dados que você só conhece no momento em que deseja que uma oferta volte. Por exemplo, a cor do artigo comprado, o tempo no momento da compra etc.

Ao transmitir dados de contexto com uma solicitação de API do Edge Decisioning, os dados são armazenados no perfil do Adobe Experience Platform, permitindo uma futura reutilização.

>[!NOTE]
>
>Para que os dados de contexto sejam armazenados, é necessário ter um esquema XDM dedicado configurado.

## Recursos da API de decisão {#decisioning}

As funcionalidades listadas abaixo só estão disponíveis com a API de decisão. Se você precisar aproveitar um deles para atender aos seus requisitos, use a API de tomada de decisão. Caso contrário, recomendamos usar as APIs do Edge Decisioning.

* **Eventos de experiência**: aproveite os eventos de experiência para criar suas regras de decisão.
* **Conteúdo e características da oferta**: é possível optar por não retornar o conteúdo e as características de uma oferta usando uma opção dedicada.
* **Metadados da oferta**: habilite uma opção para retornar os metadados de uma oferta.
* **Política de mesclagem**: use em sua solicitação uma política de mesclagem diferente daquela associada à sandbox.
* **Eventos de decisão e limite de frequência**: impede que os eventos de decisão sejam contados por qualquer limite de frequência que ocorrer.
* **Duplicação de apresentações**: habilite uma opção para não desduplicar apresentações.
