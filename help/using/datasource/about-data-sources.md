---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a fontes de dados
description: Saiba como começar a usar fontes de dados
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: dados, fonte, jornada, plataforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
TQID: https://experienceleague.adobe.com/eG1QcfpHtxpabUt5e7RZiMIpSAJD6Z6bjO-4wtZEUOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 917
ht-degree: 29%

---

# Introdução a fontes de dados {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Sobre fontes de dados"
>abstract="A configuração da fonte de dados é sempre executada por um usuário técnico. A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas para: definição de condição, parâmetro e dados de personalização em ações, definição de espera personalizada e definição de fuso horário personalizado."

>[!TIP]
>Novo no gerenciamento de dados no Journey Optimizer? Comece com a [Visão geral do gerenciamento de dados](../data/gs-data.md) para entender esquemas, conjuntos de dados, identidades e como os dados fluem antes de configurar fontes de dados.

A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para:

* [definição de condição](../building-journeys/conditions.md)
* parâmetros e dados de personalização em [ações](../action/action.md)
* [definição de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definição de fuso horário](../building-journeys/timezone-management.md)

➡️ [Conheça este recurso no vídeo](#video)

Essa configuração não é necessária se suas jornadas só usarem os dados locais provenientes de uma carga útil do evento. Por exemplo, se sua jornada for composta por um evento seguido por uma atividade de ação de canal que usa apenas dados do evento, não será necessário configurar uma fonte de dados.

Há dois tipos de fontes de dados:

* A fonte de dados do Adobe Experience Platform **pré-configurada** que define a conexão com o Serviço de Perfil do Cliente em Tempo Real. Essa fonte de dados é integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* As fontes de dados **externas** que permitem definir uma conexão com sistemas externos. Essas são as que você pode criar. Consulte [esta página](../datasource/external-data-sources.md).

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas. Para obter mais informações sobre respostas, consulte esta [seção](../action/action-response.md)

Para cada fonte de dados, você define as informações que serão recuperadas usando grupos de campos. Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Não há suporte para relações de esquema em fontes de dados.

## Escolha sua estratégia de acesso aos dados {#data-access-strategy}

Antes de configurar uma fonte de dados, considere qual abordagem se adapta melhor ao seu caso de uso. Três opções estão disponíveis, cada uma com diferentes compensações em termos de persistência, enriquecimento de perfil e reutilização. Para obter uma discussão detalhada dessas opções, consulte [Práticas recomendadas para jornadas avançadas no Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Opção 1 — Acessar dados externos por meio de Ações Personalizadas (sem Data Lake)**

Conecte-se diretamente a uma API externa no tempo de execução do jornada sem persistir nos dados no Data Lake do Experience Platform. Mais adequado quando:

* Os dados só são úteis no contexto de jornada e não são necessários em outro lugar.
* O sistema externo pode ser acessado por meio de um endpoint de API que retorna os atributos necessários.

Saiba mais sobre [ações personalizadas](../action/action.md) e [respostas de ações personalizadas](../action/action-response.md).

>[!TIP]
>
>Esta opção é adequada se você responder **sim** às duas perguntas:
>* Os dados são úteis somente dentro do contexto da jornada e não são necessários em outro lugar? Se os dados também forem necessários para públicos ou outros canais, considere as Opções 2 ou 3.
>* O sistema externo pode ser acessado por meio de um endpoint de API que retorna os atributos necessários? Caso contrário, primeiro você precisará assimilar os dados no Data Lake.

**Opção 2 — Conjunto de dados no Data Lake, não habilitado para o Perfil**

Assimile dados em um conjunto de dados para acionar e personalizar jornadas com base em dados de evento contextuais, sem contribuir com o Perfil do cliente em tempo real. Mais adequado quando:

* Os registros contêm um campo de identidade que pode ser usado para acessar perfis já armazenados no Experience Platform.
* Os dados não são necessários para a criação de público-alvo ou a identificação de identidade fora do Journey Optimizer.

>[!TIP]
>
>Esta opção é adequada se você responder **sim** às duas perguntas:
>* Os registros contêm um campo de identidade que pode ser usado para acessar perfis já armazenados no Experience Platform? Caso contrário, o jornada não poderá acessar e entregar para perfis.
>* Os dados NÃO são necessários para a criação de [público-alvo](../audience/about-audiences.md) ou para a identificação fora do Journey Optimizer? Se for, use a Opção 3.

**Opção 3 — Conjunto de dados habilitado para perfil no Data Lake**

Assimile dados em um [conjunto de dados habilitado para perfil](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} para criar públicos, enriquecer gráficos de identidade e aproveitar dados em várias jornadas e destinos da RT-CDP. Mais adequado quando:

* Os dados são úteis para definições de público-alvo usadas em canais além do Journey Optimizer.
* Os dados contêm várias identidades que contribuem para fragmentos de perfil mais ricos e compilados.

>[!CAUTION]
>
>**Antes de habilitar um conjunto de dados para o Perfil**, avalie as seguintes áreas:
>* **Sincronização de dados** — Os bancos de dados externos devem ser sincronizados, com alertas em vigor para identificar falhas de assimilação.
>* **[Medidas de proteção de perfil](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"}** — Medidas de proteção específicas de perfil se aplicam além das [medidas de proteção de assimilação de dados gerais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/guardrails){target="_blank"} para o Experience Platform.
>* **Integridade da identidade** — Os dados de identidade nos sistemas de origem devem ser cuidadosamente planejados para manter gráficos de identidade íntegros.
>* **Utilização do Data Lake** — O consumo geral de armazenamento, as relações de tabela e os perfis endereçáveis devem ser avaliados antes da assimilação.

| | Dados persistentes no Data Lake | Conjunto de dados habilitado para o perfil |
| --- | --- | --- |
| **Opção 1** — Dados externos por meio de Ações Personalizadas | Não | Não |
| **Opção 2** — Conjunto de dados não habilitado para Perfil | Sim | Não |
| **Opção 3** — Conjunto de dados habilitado para perfil | Sim | Sim |

Para obter mais informações sobre como configurar uma fonte de dados da Adobe Experience Platform e uma fonte de dados externa, e como localizar e usar dados em uma jornada, assista a este [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Vídeo tutorial {#video}

Entenda o que é uma fonte de dados e saiba como configurar fontes de dados da Experience Platform e externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

