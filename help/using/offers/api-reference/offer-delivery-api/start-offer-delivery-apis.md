---
title: Introdução às APIs de entrega de ofertas
description: Saiba mais sobre as APIs disponíveis para fornecer ofertas personalizadas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 4%

---

# Introdução às APIs de entrega de ofertas {#about-decisioning-apis}

Você pode entregar ofertas usando a API de **Decisão** ou a **Decisão da Edge**. Além disso, a API de **Decisão em lote** permite entregar ofertas a todos os perfis em um determinado público-alvo através de uma única chamada. O conteúdo da oferta de cada perfil no público-alvo é colocado em um conjunto de dados do Adobe Experience Platform, onde ele estará disponível para fluxos de trabalho em lote personalizados.

Nesta página, você encontrará informações sobre funcionalidades específicas disponíveis com as APIs da **Decisão** e do **Edge Decisioning**. Embora ambos permitam entregar ofertas aos seus clientes, recomendamos usar a API do **Edge Decisioning** sempre que possível para casos de uso de entrada e para garantir melhor latência e taxa de transferência na sua plataforma.

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:
* [API de decisão](decisioning-api.md)
* [API de decisão do Edge](edge-decisioning-api.md)
* [API de decisão em lote](batch-decisioning-api.md)

## Recursos da API do Edge Decisioning {#edge}

**Solicitação exclusiva para eventos de experiência e solicitações de decisão**

Com a API de decisão do Edge, é possível enviar o próprio evento de experiência juntamente com a solicitação de decisão em uma única solicitação, em vez de ter duas solicitações diferentes.

Por exemplo, se um cliente visitar seu site, a solicitação incluirá o evento de experiência (a visita do cliente à página) e obterá uma oferta para preencher a página visitada.

**Armazenamento de dados de contexto no Adobe Experience Platform**

Dados de contexto se referem a dados que você só sabe no momento em que deseja uma oferta de volta. Por exemplo, a cor do artigo comprado, o clima no momento da compra etc.

Ao transmitir dados de contexto com uma solicitação da API do Edge Decisioning, os dados são armazenados no perfil do Adobe Experience Platform, permitindo reutilização futura.

>[!NOTE]
>
>Para que os dados de contexto sejam armazenados, é necessário ter um esquema XDM dedicado configurado.

**Atualização do contador de limite de frequência**

Se o limite de frequência tiver sido ativado para algumas de suas ofertas para definir a frequência com que sua contagem de limite é redefinida, o contador será atualizado e estará disponível em uma decisão da API do Edge Decisioning em menos de 3 segundos. [Saiba como adicionar restrições a uma oferta](../../offer-library/add-constraints.md)

## Recursos da API de decisão {#decisioning}

As funcionalidades listadas abaixo só estão disponíveis com a API de decisão. Se você precisar usar uma delas para atender aos seus requisitos, use a API de decisão. Caso contrário, recomendamos usar as APIs do Edge Decisioning.

* **Conteúdo e características da oferta**: você pode optar por não retornar o conteúdo e as características de uma oferta usando uma opção dedicada.
* **Metadados da oferta**: habilite uma opção para retornar os metadados de uma oferta.
* **Política de mesclagem**: use em sua solicitação uma política de mesclagem diferente da que está associada à sua sandbox.
* **Eventos de decisão e limite de frequência**: impede que os eventos de decisão sejam contados por qualquer limite de frequência que ocorra.
* **Proposições duplicadas**: habilite uma opção para não desduplicar propostas.
