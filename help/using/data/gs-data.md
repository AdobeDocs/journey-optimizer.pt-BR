---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao gerenciamento de dados no Journey Optimizer
description: Saiba como os dados fluem para dentro e para fora do Adobe Journey Optimizer, incluindo os principais conceitos, etapas de configuração e medidas de proteção.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 2612
ht-degree: 100%

---

# Introdução ao gerenciamento de dados {#about-data}

Os dados são a base de cada jornada, decisão e mensagem que você envia com o [!DNL Adobe Journey Optimizer].

Esta página fornece um ponto de partida prático para entender:

* Os elementos de dados principais usados pelo Journey Optimizer (esquemas, conjuntos de dados, identidades, perfis)
* Como o Journey Optimizer usa os dados da Adobe Experience Platform
* Quais etapas de configuração de dados sua equipe deve concluir antes de criar jornadas e campanhas
* O próximo passo para obter configurações detalhadas e práticas recomendadas

Use este guia em conjunto com seus engenheiros de dados, administradores e profissionais de marketing para que todos compartilhem uma visão comum de como os dados entram e saem do Journey Optimizer.

>[!TIP]
>Novo no gerenciamento de dados no Journey Optimizer? Assista ao [Tutorial de visão geral de configuração de dados](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} para obter um passo a passo prático e fácil para iniciantes sobre esquemas, conjuntos de dados e fontes.

## Como o Journey Optimizer usa os dados da Adobe Experience Platform {#aep-data}

O [!DNL Adobe Journey Optimizer] está integrado na [!DNL Adobe Experience Platform]. Ele não mantém um armazenamento de dados separado e isolado. Em vez disso, usa a mesma base de dados que outros aplicativos da Experience Cloud.

Esquemas e conjuntos de dados ficam na Adobe Experience Platform. As identidades e o [Perfil do cliente em tempo real](../audience/get-started-profiles.md) são gerenciados pelo Serviço de identidade e pelo Serviço de perfil. O Journey Optimizer lê dados de perfil e evento da Adobe Experience Platform para avaliar as condições da jornada, personalizar mensagens e selecionar ofertas. Ele grava dados de interação (como eventos de envio, abertura, clique, rejeição e eventos de etapa de jornada) de volta nos conjuntos de dados da Experience Platform. Também pode pesquisar conjuntos de dados adicionais no tempo de execução sem copiar esses dados no perfil.

>[!TIP]
>Pense na Adobe Experience Platform como a camada de dados central e no Journey Optimizer como um aplicativo que orquestra jornadas e mensagens usando essa base de dados compartilhada.

➡️ [Saiba mais sobre a arquitetura do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Principais conceitos de dados no Journey Optimizer {#key-concepts}

Ao trabalhar com dados no Journey Optimizer, você encontra vários conceitos relacionados. A tabela abaixo fornece uma visão geral rápida; as seções a seguir explicam cada conceito com mais detalhes.

| Conceito | O que é | Uso principal no Journey Optimizer |
|---|---|---|
| Esquema XDM | Regras que representam, validam e formatam os dados (criadas a partir de uma classe + grupos de campos) | Atributos do perfil de modelo e eventos comportamentais |
| Conjunto de dados | Tabela de armazenamento para dados em conformidade com um esquema | Reter dados de perfil, eventos e gerados pelo sistema |
| Conector de origem | Transmite ou processa dados em lotes de sistemas externos para a AEP | Assimilar dados do CRM, do Analytics e da Web |
| Fonte de dados | Expõe campos da AEP ou externos dentro de jornadas | Promover condições de jornada e a personalização de mensagens |
| Identidade | Identificador que representa exclusivamente um cliente individual | Compilar perfis entre canais |
| Conjunto de dados de pesquisa | Referência de tempo de execução para dados da AEP sem armazenamento de perfil | Enriquecer mensagens com dados de referência em tempo real |

### Esquema (esquema XDM) {#schema}

Um esquema é um conjunto de regras que representam, validam e formatam os dados. Ele é composto de uma **classe** (que define o comportamento base: registro ou série temporal) e **grupos de campos** opcionais (que adicionam campos específicos). Os esquemas são definidos usando os padrões do Experience Data Model (XDM) e ficam na Adobe Experience Platform.

O XDM existe para resolver um problema real: o mesmo conceito — um cliente, uma compra, um produto — é nomeado e estruturado de forma diferente em todos os sistemas de origem. O XDM fornece uma linguagem compartilhada que unifica esses conceitos em uma única definição, independentemente da origem dos dados. É isso que permite que o Journey Optimizer funcione de forma consistente com dados do CRM, site, aplicativo móvel e data warehouse ao mesmo tempo.

No Journey Optimizer, você geralmente trabalha com esquemas do **Perfil individual XDM** para atributos do cliente (nome, preferências, consentimento) e esquemas do **XDM ExperienceEvent** para eventos comportamentais (compras, exibições de página, inscrições).

➡️ [Saiba mais sobre esquemas](get-started-schemas.md)

### Conjunto de dados {#dataset}

Um conjunto de dados é uma construção de armazenamento e gerenciamento de dados que estão em conformidade com um esquema — pense nele como uma tabela com um conjunto definido de colunas e linhas. Todos os dados usados pelo Journey Optimizer são armazenados em conjuntos de dados da Adobe Experience Platform. Podem ser conjuntos de dados de perfil (contribuindo para o Perfil do cliente em tempo real), conjuntos de dados de evento (armazenando dados comportamentais para jornadas e análises) ou conjuntos de dados do sistema criados automaticamente pelo Journey Optimizer para rastreamento, feedback e eventos de etapa de jornada.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

### Conector de origem {#source-connector}

Um conector de origem (também conhecido como **origem**) ajuda você a assimilar dados de vários sistemas — como Adobe Analytics, SDK da Web da Adobe Experience Platform, armazenamento na nuvem (S3, Azure Blob) ou bancos de dados de CRM — na Adobe Experience Platform. Além da ingestão bruta, os conectores permitem a estruturação, a rotulagem e o aprimoramento de dados usando serviços da Experience Platform, incluindo o mapeamento de campos para esquemas XDM e a rotulagem da governança de dados.

➡️ [Saiba mais sobre conectores de origem](../start/get-started-sources.md)

### Fonte de dados (Journey Optimizer) {#data-source}

Uma fonte de dados no Journey Optimizer define quais campos da Adobe Experience Platform (ou APIs externas) são expostos dentro das jornadas e mensagens. Configuradas na interface do Journey Optimizer, as fontes de dados normalmente incluem a fonte de dados integrada da Adobe Experience Platform (expondo os atributos do Perfil do cliente em tempo real) e fontes de dados opcionais externas ou personalizadas chamadas no tempo de execução da jornada para enriquecimento adicional. Elas são usadas para condições de jornada, ações personalizadas e personalização de mensagens.

➡️ [Saiba mais sobre fontes de dados](../datasource/about-data-sources.md)

>[!NOTE]
>O [Glossário da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/glossary){target="_blank"} define “fonte de dados” genericamente como a origem dos dados (um CRM, aplicativo móvel etc.). No Journey Optimizer, **fonte de dados** tem um significado específico: uma configuração da interface que controla quais campos são expostos dentro de jornadas e mensagens.

### Identidade e perfil do cliente em tempo real {#identity}

Uma identidade é um identificador que representa exclusivamente um cliente individual, como uma ID de cookie, ID de dispositivo, endereço de email ou ID de CRM. As identidades são organizadas em namespaces (Email, ECID, CRMID) e várias identidades para a mesma pessoa são agrupadas em um gráfico de identidade unificado. O Perfil do cliente em tempo real usa esse gráfico para manter uma visão integral de cada cliente individual, combinando dados de vários canais, incluindo canais online e offline, o CRM e fontes de terceiros.

Um conceito-chave para iniciantes é o modelo de **fragmento de perfil**. Cada vez que um cliente interage com sua marca em um dispositivo ou canal específico — seu site, aplicativo móvel, uma loja — essa interação é registrada como um fragmento de perfil: uma visualização parcial desse cliente com base nesse ponto de contato específico. O Perfil do cliente em tempo real une continuamente esses fragmentos com base em valores de identidade compartilhados, criando um perfil completo e atualizado. O Journey Optimizer lê esse perfil consolidado para avaliar condições, selecionar ofertas e personalizar mensagens em tempo real.

➡️ [Saiba mais sobre identidades no Journey Optimizer](../audience/get-started-identity.md)

### Conjunto de dados de pesquisa {#lookup-dataset}

Um conjunto de dados de pesquisa permite que o Journey Optimizer recupere dados de referência ou transacionais no tempo de execução de um conjunto de dados da Adobe Experience Platform, sem armazenar esses dados no Perfil do cliente em tempo real. Isso é útil para dados de referência que mudam com frequência (preços, inventário, horas de armazenamento) ou dados transacionais que são necessários no momento da mensagem, mas não pertencem ao perfil. O Journey Optimizer realiza a pesquisa durante a execução da jornada ou da mensagem com base em uma chave, como uma ID de produto.

➡️ [Saiba mais sobre conjuntos de dados de pesquisa](lookup-aep-data.md)

## Lista de verificação de preparação de dados {#checklist}

Antes de os profissionais de marketing começarem a criar jornadas e campanhas, sua organização deve concluir um conjunto de etapas de preparação de dados. Isso garante que o Journey Optimizer possa usar os dados certos, na hora certa e em conformidade.

>[!NOTE]
>As etapas abaixo envolvem várias funções: engenheiros de dados, administradores e profissionais de marketing. Use essa lista de verificação como um plano compartilhado para preparar seu ambiente. As etapas 1 a 4 são concluídas na Adobe Experience Platform; as etapas 5 a 6 são configuradas no Journey Optimizer.

As seis etapas abaixo orientam você pelo processo completo de configuração de dados, desde a configuração de identidade até a verificação de que os dados fluem corretamente para o Journey Optimizer:

1. Definir a estratégia de identidade
1. Criar esquemas para dados de perfil e evento
1. Criar conjuntos de dados habilitados para perfil
1. Assimilar dados de suas origens
1. Configurar fontes de dados no Journey Optimizer
1. Verificar rastreamento, feedback e conjuntos de dados de jornada

+++ Definir a estratégia de identidade

Escolha uma identidade principal para seus clientes (como ECID, email ou CRMID) e configure os namespaces correspondentes no Serviço de identidade da Adobe Experience Platform. Verifique se os campos de identidade estão presentes em seus esquemas habilitados por perfil e valide se os perfis estão compilados corretamente no gráfico de identidade.

➡️ [Saiba mais sobre identidades no Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Criar esquemas para dados de perfil e evento

Crie esquemas do **Perfil individual XDM** para capturar atributos do cliente, como nome e informações de contato, preferências e interesses, e estágio do ciclo de vida ou estado de consentimento. Crie esquemas do **XDM ExperienceEvent** para capturar dados comportamentais e transacionais, como eventos da Web e do aplicativo, compras e interações offline. Marque os campos corretos como identidades e atributos de perfil, quando apropriado.

➡️ [Saiba mais sobre esquemas](get-started-schemas.md)

+++

+++ Criar conjuntos de dados habilitados para perfil

Na Adobe Experience Platform, crie conjuntos de dados com base em esquemas XDM e habilite o recurso Perfil em qualquer conjunto de dados que deva contribuir para o Perfil do cliente em tempo real. Confirme se os conjuntos de dados gerados pelo sistema criados pelo Journey Optimizer estão visíveis no espaço de trabalho Conjuntos de dados.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

+++

+++ Assimilar dados de suas origens

Configure conectores de origem para seus sistemas corporativos, como o Adobe Analytics, SDK da web da Adobe Experience Platform ou suas plataformas CRM e POS, e mapeie os campos de entrada para os esquemas XDM. Verifique se os dados são inseridos nos conjuntos de dados corretos e se aparecem no Perfil do cliente em tempo real conforme o esperado.

➡️ [Saiba mais sobre conectores de origem](../start/get-started-sources.md)

➡️ [Tutorial: criar conjuntos de dados e assimilar dados](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configurar fontes de dados no Journey Optimizer

As fontes de dados são um conceito específico do Journey Optimizer: não são onde seus dados residem, mas onde você declara quais campos o Journey Optimizer tem permissão para ler durante a execução da jornada e da mensagem. Antes que uma jornada possa avaliar uma condição como “o cliente é um membro do programa de fidelidade?” ou personalizar uma mensagem com um nome, os campos de perfil relevantes devem ser expostos por meio de uma configuração de fonte de dados.

O Journey Optimizer inclui uma [fonte de dados integrada da Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) que dá acesso direto aos atributos do Perfil do cliente em tempo real. Isso abrange a grande maioria dos casos de uso: ler atributos de perfil para personalização ou verificar campos de consentimento e preferência. Você também pode configurar [fontes de dados externas](../datasource/external-data-sources.md) para chamar APIs de terceiros no tempo de execução da jornada, por exemplo, para recuperar uma pontuação de fidelidade em tempo real, uma recomendação de produto ou um nível de inventário de loja que não esteja armazenado na Adobe Experience Platform.

>[!NOTE]
>O acesso direto aos dados do evento de experiência por meio da fonte de dados integrada da Adobe Experience Platform está obsoleto e sendo progressivamente desativado. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

Configurar fontes de dados é uma tarefa administrativa que desbloqueia a camada de dados completa para autores e profissionais de marketing da jornada. Depois que um campo é exposto por meio de uma fonte de dados, ele fica disponível no construtor de condições de jornada, em editores de personalização de mensagens e em regras de definição de ofertas — sem exigir trabalho de engenharia adicional no momento da criação da jornada.

➡️ [Saiba mais sobre a configuração de fonte de dados](../datasource/about-data-sources.md)

+++

+++ Verificar rastreamento, feedback e conjuntos de dados de jornada

Confirme se os conjuntos de dados gerados pelo sistema do Journey Optimizer estão disponíveis no espaço de trabalho de Conjuntos de dados. Execute jornadas e campanhas de teste e, em seguida, use o Editor de consultas para verificar se os eventos de envio, abertura, clique e rejeição estão registrados e se os eventos e estados de etapa de jornada foram capturados corretamente. Use esses conjuntos de dados para monitoramento contínuo, solução de problemas e otimização de jornadas.

➡️ [Saiba mais sobre consultas no Journey Optimizer](get-started-queries.md)

+++

## Medidas de proteção e considerações sobre o design de dados {#guardrails}

Algumas medidas de proteção e limitações do produto podem influenciar a maneira como você projeta o modelo de dados e as jornadas. Analise esses itens antecipadamente para evitar retrabalho depois.

>[!IMPORTANT]
>Sempre consulte a página [Medidas de proteção e limitações do Journey Optimizer](../start/guardrails.md) para obter as informações mais recentes. Os resumos abaixo destacam os principais itens, mas podem evoluir com o tempo.

### Conjuntos de dados do sistema Journey Optimizer e TTL {#datasets-ttl}

O Journey Optimizer cria vários conjuntos de dados gerados pelo sistema para rastreamento, feedback e eventos de etapa de jornada. A partir de fevereiro de 2025, uma proteção de TTL (time-to-live, tempo de vida útil) está sendo implantada em alguns desses conjuntos de dados, o que pode afetar por quanto tempo os dados serão retidos para análise e solução de problemas.

➡️ [Saiba mais sobre as medidas de proteção de TTL do conjunto de dados](datasets-ttl.md)

### Segmentação de transmissão e eventos do Journey Optimizer {#streaming-segmentation}

A partir de 1º de novembro de 2024, a segmentação de transmissão se tornou incompatível com eventos de envio e abertura dos conjuntos de dados de rastreamento e feedback do Journey Optimizer. Em casos de uso como limite de frequência e gerenciamento de fadiga, use [Regras de negócios](../conflict-prioritization/rule-sets.md) em vez de segmentos de transmissão com base em eventos de envio/abertura.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

### Pesquisa e decisão do conjunto de dados {#lookup-guardrails}

A pesquisa do conjunto de dados é ideal para atributos (inventário, preços, clima) ou dados que mudam com frequência e que não precisam ser armazenados no Perfil do cliente em tempo real. Revise as medidas de proteção específicas do produto, como limites de tamanho do conjunto de dados e limites de consulta na documentação relevante antes de projetar sua estratégia de pesquisa.

➡️ [Saiba mais sobre conjuntos de dados de pesquisa](lookup-aep-data.md)

## Exemplo: preparação de dados para uma jornada de boas-vindas {#example}

O exemplo a seguir mostra como os conceitos desta página funcionam juntos em um cenário simples.

1. Um engenheiro de dados cria um [esquema do Perfil individual XDM](get-started-schemas.md) para atributos do cliente (nome, email, nível de fidelidade, consentimento) e um esquema XDM ExperienceEvent para eventos de inscrição na Web.
1. [Conjuntos de dados habilitados para perfil](get-started-datasets.md) são criados para cada esquema: um para atributos do CRM e um para eventos de inscrição.
1. Equipes da Web e móveis transmitem eventos de inscrição por meio do SDK da Web da Adobe Experience Platform; os dados do CRM são assimilados por meio de um [conector de origem](../start/get-started-sources.md).
1. Um(a) admin configura a [fonte de dados da Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) no Journey Optimizer e expõe campos como `profile.person.name.firstName`, `profile.personalEmail.address` e `profile.loyaltyTier`.
1. Um profissional de marketing [cria uma jornada de boas-vindas](../building-journeys/journey-gs.md) que acompanha um evento de inscrição e usa esses atributos de perfil para [personalizar o email de boas-vindas](../personalization/personalize.md). O Journey Optimizer grava eventos de envio e abertos em conjuntos de dados de rastreamento e registra o progresso da jornada em conjuntos de dados de eventos de etapa da jornada.
1. Um desenvolvedor usa o [Editor de consultas](get-started-queries.md) para verificar se os eventos estão fluindo corretamente e analisa o desempenho (aberturas, cliques, tempo de envio). A equipe ajusta a jornada e o conteúdo com base nesses insights.

Esse fluxo ilustra como esquemas, conjuntos de dados, fontes, fontes de dados e consultas trabalham juntos em um caso de uso completo e fácil de usar para iniciantes.

## Recursos relacionados {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Introdução a esquemas**

Saiba como criar esquemas XDM na Adobe Experience Platform, escolher a classe e os grupos de campos corretos e modelar os atributos de perfil e os eventos comportamentais.

[Saiba mais](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Trabalhar com conjuntos de dados**

Entenda como criar conjuntos de dados de evento e habilitados para perfil, monitorar a ingestão de dados e explorar os conjuntos de dados gerados pelo sistema que o Journey Optimizer cria automaticamente para eventos de rastreamento, feedback e etapa da jornada.

[Saiba mais](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Configurar fontes de dados**

Instruções passo a passo sobre como configurar a fonte de dados integrada da Adobe Experience Platform e as fontes de dados externas opcionais para expor campos de perfil e respostas da API externa dentro das jornadas.

[Saiba mais](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Usar dados da Adobe Experience Platform (pesquisa)**

Descubra como enriquecer mensagens no tempo de execução com dados de referência ou transacionais de conjuntos de dados da AEP, sem armazenar esses dados no Perfil do cliente em tempo real.

[Saiba mais](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Introdução a consultas**

Use o Serviço de consulta para analisar conjuntos de dados do Journey Optimizer, verificar se os eventos estão fluindo corretamente e criar consultas de relatório sobre dados de envio, abertura, clique e rejeição.

[Saiba mais](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Introdução a perfis**

Saiba como o Perfil do cliente em tempo real funciona no Journey Optimizer e descubra como procurar, inspecionar e validar perfis de clientes individuais na interface da Platforma.

[Saiba mais](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial de visão geral da configuração de dados**

Uma apresentação em vídeo de fácil introdução sobre a configuração de dados no Journey Optimizer, abrangendo esquemas, conjuntos de dados e fontes do início ao fim.

[Assistir ao tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial de criação e ingestão de conjuntos de dados**

Um tutorial prático que mostra como criar conjuntos de dados na Adobe Experience Platform e assimilar dados usando conectores de origem, com instruções passo a passo que você pode seguir em sua própria sandbox.

[Assistir ao tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
