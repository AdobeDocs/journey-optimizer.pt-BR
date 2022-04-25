---
title: APIs de decisão e decisão de borda
description: O Gerenciamento de decisões é uma coleção de serviços e programas de interface do usuário que permite aos profissionais de marketing criar e fornecer experiências de ofertas personalizadas para o usuário final em canais e aplicativos usando lógica de negócios e regras de decisão.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 1%

---

# APIs de decisão e decisão de borda {#about-decisioning-apis}

Você pode fornecer ofertas usando a variável **Decisão** ou **Edge Decisioning** API.

Nesta página, você encontrará informações sobre funcionalidades específicas disponíveis com cada API. Embora ambos permitam que você entregue ofertas aos seus clientes, recomendamos usar a variável **Edge Decisioning** API sempre que possível para casos de uso de entrada e para garantir melhor latência e throughput na plataforma.

|  | Solicitações/s | Latência |
|---|---|---|
| API de decisão | 2000 | &lt;500ms |
| API do Edge Decisioning | 5000 | &lt;250ms |

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:
* [API de decisão](decisioning-api.md)
* [API do Edge Decisioning](edge-decisioning-api.md)

## Recursos da API do Edge Decisioning {#edge}

**Solicitação exclusiva para eventos de experiência e solicitações de decisão**

Com a API do Edge Decisioning, você pode enviar em uma única solicitação o evento de experiência juntamente com a solicitação de decisão, em vez de ter duas solicitações diferentes.

Por exemplo, se um cliente visitar seu site, a solicitação incluirá o evento de experiência (a visita do cliente à página) e obterá uma oferta de volta para preencher a página visitada.

**Armazenamento de dados de contexto no Adobe Experience Platform**

Os dados de contexto se referem a dados que você só conhece no momento em que deseja que uma oferta volte. Por exemplo, a cor do artigo comprado, o tempo no momento da compra etc.

Ao transmitir dados de contexto com uma solicitação de API do Edge Decisioning, os dados são armazenados no perfil do Adobe Experience Platform, permitindo uma futura reutilização.

>[!NOTE]
>
>Para que os dados de contexto sejam armazenados, é necessário ter um esquema XDM dedicado configurado. (+ link para o documento XDM)

## Recursos da API de decisão {#decisioning}

As funcionalidades listadas abaixo só estão disponíveis com a API de decisão. Se você precisar aproveitar um deles para atender aos seus requisitos, use a API de tomada de decisão. Caso contrário, recomendamos usar as APIs do Edge Decisioning.

* **Eventos de experiência**: aproveite os eventos de experiência para criar suas regras de decisão.
* **Conteúdo e características da oferta**: é possível optar por não retornar o conteúdo e as características de uma oferta usando uma opção dedicada.
* **Metadados da oferta**: habilite uma opção para retornar os metadados de uma oferta.
* **Política de mesclagem**: use em sua solicitação uma política de mesclagem diferente daquela associada à sandbox.
* **Eventos de decisão e limite de frequência**: impede que os eventos de decisão sejam contados por qualquer limite de frequência que ocorrer.
* **Duplicação de apresentações**: habilite uma opção para não desduplicar apresentações.
