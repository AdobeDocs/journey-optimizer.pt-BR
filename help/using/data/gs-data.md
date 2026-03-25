---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao gerenciamento de dados no Journey Optimizer
description: Saiba como os dados fluem para dentro e para fora do Adobe Journey Optimizer, incluindo os principais conceitos, etapas de configuração e medidas de proteção.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 89d575834871a5c55bfce75511083b4b651301b8
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 1%

---


# Introdução ao gerenciamento de dados {#about-data}

Os dados são a base de cada jornada, decisão e mensagem que você envia com o [!DNL Adobe Journey Optimizer].

Esta página fornece um ponto de partida prático para entender:

* Os blocos de construção de dados principais usados pela Journey Optimizer (esquemas, conjuntos de dados, identidades, perfis)
* Como o Journey Optimizer usa os dados do Adobe Experience Platform
* Quais etapas de configuração de dados sua equipe deve concluir antes de criar jornadas e campanhas
* O próximo passo para obter configurações detalhadas e práticas recomendadas

Use este guia junto com seus engenheiros de dados, administradores e profissionais de marketing para que todos compartilhem uma imagem comum de como os dados fluem para dentro e para fora do Journey Optimizer.

>[!TIP]
>Novo no gerenciamento de dados no Journey Optimizer? Assista ao [Tutorial de visão geral da configuração](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} de dados para obter uma apresentação prática e fácil de iniciar de esquemas, conjuntos de dados e fontes.

## Como o Journey Optimizer usa os dados do Adobe Experience Platform {#aep-data}

[!DNL Adobe Journey Optimizer] é compilado em [!DNL Adobe Experience Platform]. Ele não mantém um armazenamento de dados separado e isolado. Em vez disso, ele usa a mesma base de dados que outros aplicativos da Experience Cloud.

Esquemas e conjuntos de dados vivem na Adobe Experience Platform. As identidades e o [Perfil de cliente em tempo real](../audience/get-started-profiles.md) são gerenciados pelo Serviço de identidade e pelo Serviço de perfil. O Journey Optimizer lê dados de perfil e evento do Adobe Experience Platform para avaliar condições de jornada, personalizar mensagens e selecionar ofertas. Ele grava dados de interação — como eventos de envio, abertura, clique e rejeição e eventos de etapa de jornada — de volta nos conjuntos de dados do Experience Platform. Ele também pode pesquisar conjuntos de dados adicionais no tempo de execução sem copiar esses dados no perfil.

>[!TIP]
>Pense no Adobe Experience Platform como sua camada de dados central e no Journey Optimizer como um aplicativo que orquestra jornadas e mensagens usando essa base de dados compartilhada.

➡️ [Saiba mais sobre a arquitetura do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Principais conceitos de dados no Journey Optimizer {#key-concepts}

Ao trabalhar com dados no Journey Optimizer, você encontrará vários conceitos relacionados. A tabela abaixo fornece uma visão geral rápida; as seções a seguir explicam cada conceito com mais detalhes.

| Conceito | O que é | Uso principal no Journey Optimizer |
|---|---|---|
| Esquema XDM | Regras que representam, validam e formatam seus dados (criadas a partir de uma classe + grupos de campos) | Atributos do perfil de modelo e eventos comportamentais |
| Conjunto de dados | Tabela de armazenamento para dados em conformidade com um esquema | Armazenar dados gerados pelo sistema, evento e perfil |
| Conector do Source | Transmissão ou agrupamento de dados de sistemas externos para o AEP | Assimilar dados do CRM, do Analytics e da Web |
| Fonte de dados | Expõe campos AEP ou externos dentro de jornadas | Condições de jornada de energia e personalização de mensagens |
| Identidade | Identificador que representa exclusivamente um cliente individual | Compilar perfis entre canais |
| Conjunto de dados de pesquisa | Referência de tempo de execução para dados do AEP sem armazenamento de perfil | Enriquecer mensagens com dados de referência em tempo real |

### Esquema (esquema XDM) {#schema}

Um esquema é um conjunto de regras que representam, validam e formatam os dados. Ele é composto de uma **classe** (que define o comportamento base: registro ou série temporal) e **grupos de campos** opcionais (que adicionam campos específicos). Os esquemas são definidos usando os padrões Experience Data Model (XDM) e residem no Adobe Experience Platform.

O XDM existe para resolver um problema real: o mesmo conceito — um cliente, uma compra, um produto — é nomeado e estruturado de forma diferente em todos os sistemas de origem. O XDM fornece uma linguagem compartilhada que unifica esses conceitos em uma única definição, independentemente da origem dos dados. É isso que permite que o Journey Optimizer funcione de forma consistente com dados do seu CRM, site, aplicativo móvel e data warehouse ao mesmo tempo.

No Journey Optimizer, você geralmente trabalha com esquemas do **Perfil individual XDM** para atributos do cliente (nome, preferências, consentimento) e esquemas do **XDM ExperienceEvent** para eventos comportamentais (compras, exibições de página, inscrições).

➡️ [Saiba mais sobre esquemas](get-started-schemas.md)

### Conjunto de dados {#dataset}

Um conjunto de dados é uma construção de armazenamento e gerenciamento para dados que estão em conformidade com um esquema — pense nele como uma tabela com um conjunto definido de colunas e linhas. Todos os dados usados pelo Journey Optimizer são armazenados em conjuntos de dados do Adobe Experience Platform. Podem ser conjuntos de dados de perfil (contribuindo para o Perfil do cliente em tempo real), conjuntos de dados de evento (armazenando dados comportamentais para jornadas e análises) ou conjuntos de dados do sistema criados automaticamente pela Journey Optimizer para rastreamento, feedback e eventos de etapa de jornada.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

### Conector do Source {#source-connector}

Um conector de origem (também conhecido como **origem**) ajuda você a assimilar dados de vários sistemas — como Adobe Analytics, Adobe Experience Platform Web SDK, armazenamento na nuvem (S3, Azure Blob) ou bancos de dados CRM — no Adobe Experience Platform. Além da assimilação bruta, os conectores permitem a estruturação, a rotulagem e o aprimoramento de dados usando serviços da Experience Platform, incluindo o mapeamento de campos para seus esquemas XDM e a rotulagem da governança de dados.

➡️ [Saiba mais sobre conectores de origem](../start/get-started-sources.md)

### Fonte de dados (Journey Optimizer) {#data-source}

Uma fonte de dados no Journey Optimizer define quais campos do Adobe Experience Platform (ou APIs externas) são expostos dentro das jornadas e mensagens. Configuradas na interface do usuário do Journey Optimizer, as fontes de dados normalmente incluem a fonte de dados integrada do Adobe Experience Platform (expondo atributos e eventos do Perfil do cliente em tempo real) e fontes de dados externas ou personalizadas opcionais chamadas no tempo de execução do jornada para enriquecimento adicional. Eles são usados para condições de jornada, ações personalizadas e personalização de mensagens.

➡️ [Saiba mais sobre fontes de dados](../datasource/about-data-sources.md)

>[!NOTE]
>O [Glossário do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/glossary){target="_blank"} define &quot;fonte de dados&quot; genericamente como a origem dos dados (um CRM, aplicativo móvel etc.). No Journey Optimizer, a **fonte de dados** tem um significado específico: uma configuração de interface do usuário que controla quais campos são expostos dentro de jornadas e mensagens.

### Identidade e perfil do cliente em tempo real {#identity}

Uma identidade é um identificador que representa exclusivamente um cliente individual, como uma ID de cookie, ID de dispositivo, endereço de email ou ID de CRM. As identidades são organizadas em namespaces (Email, ECID, CRMID) e várias identidades para a mesma pessoa são agrupadas em um gráfico de identidade unificado. O Perfil do cliente em tempo real usa esse gráfico para manter uma visualização integral de cada cliente individual, combinando dados de vários canais — incluindo fontes online, offline, de CRM e de terceiros.

Um conceito-chave para iniciantes é o modelo **fragmento de perfil**. Cada vez que um cliente interage com sua marca em um dispositivo ou canal específico — seu site, aplicativo móvel, uma loja — essa interação é registrada como um fragmento de perfil: uma visualização parcial desse cliente com base nesse ponto de contato específico. O Perfil do cliente em tempo real une continuamente esses fragmentos com base em valores de identidade compartilhados, criando um perfil completo e atualizado. O Journey Optimizer lê as mensagens desse perfil montado para avaliar condições, selecionar ofertas e personalizar mensagens em tempo real.

➡️ [Saiba mais sobre identidades no Journey Optimizer](../audience/get-started-identity.md)

### Conjunto de dados de pesquisa {#lookup-dataset}

Um conjunto de dados de pesquisa permite que a Journey Optimizer recupere dados de referência ou transacionais em tempo de execução de um conjunto de dados da Adobe Experience Platform, sem armazenar esses dados no Perfil do cliente em tempo real. Isso é útil para dados de referência que mudam com frequência (preços, inventário, horas de armazenamento) ou dados transacionais que são necessários no momento da mensagem, mas não pertencem ao perfil. O Journey Optimizer realiza a pesquisa durante a execução da jornada ou da mensagem com base em uma chave, como uma ID de produto.

➡️ [Saiba mais sobre conjuntos de dados de pesquisa](lookup-aep-data.md)

## Lista de verificação de preparação de dados {#checklist}

Antes de os profissionais de marketing começarem a criar jornadas e campanhas, sua organização deve concluir um conjunto de etapas de preparação de dados. Isso garante que a Journey Optimizer possa usar os dados certos, na hora certa e em conformidade.

>[!NOTE]
>As etapas abaixo envolvem várias funções: engenheiros de dados, administradores e profissionais de marketing. Use essa lista de verificação como um plano compartilhado para preparar seu ambiente. As etapas 1 a 4 são concluídas no Adobe Experience Platform; as etapas 5 a 6 são configuradas no Journey Optimizer.

As seis etapas abaixo orientam você pelo processo completo de configuração de dados, desde a configuração de identidade até a verificação de que os dados fluem corretamente para o Journey Optimizer:

1. Definir a estratégia de identidade
1. Criar esquemas para dados de perfil e evento
1. Criar conjuntos de dados habilitados para perfil
1. Assimilar dados de suas fontes
1. Configurar fontes de dados no Journey Optimizer
1. Verificar rastreamento, feedback e conjuntos de dados de jornada

+++ Definir a estratégia de identidade

Escolha uma identidade principal para seus clientes (como ECID, email ou CRMID) e configure os namespaces correspondentes no Serviço de identidade da Adobe Experience Platform. Verifique se os campos de identidade estão presentes em seus esquemas ativados por perfil e valide se os perfis estão compilados corretamente no gráfico de identidade.

➡️ [Saiba mais sobre identidades no Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Criar esquemas para dados de perfil e evento

Crie esquemas do **Perfil individual XDM** para capturar atributos do cliente, como nome e informações de contato, preferências e interesses, e estágio do ciclo de vida ou estado de consentimento. Crie esquemas **XDM ExperienceEvent** para capturar dados comportamentais e transacionais, como eventos da Web e do aplicativo, compras e interações offline. Marque os campos corretos como identidades e atributos de perfil, quando apropriado.

➡️ [Saiba mais sobre esquemas](get-started-schemas.md)

+++

+++ Criar conjuntos de dados habilitados para perfil

No Adobe Experience Platform, crie conjuntos de dados com base nos esquemas XDM e ative Criar perfil em qualquer conjunto de dados que deva contribuir para o Perfil do cliente em tempo real. Confirme se os conjuntos de dados gerados pelo sistema criados pela Journey Optimizer estão visíveis no espaço de trabalho Conjuntos de dados.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

+++

+++ Assimilar dados de suas fontes

Configure conectores de origem para seus sistemas corporativos — como Adobe Analytics, Adobe Experience Platform Web SDK ou suas plataformas CRM e POS — e mapeie os campos de entrada para seus esquemas XDM. Validar se os dados chegam aos conjuntos de dados corretos e são exibidos no Perfil do cliente em tempo real, onde esperado.

➡️ [Saiba mais sobre conectores de origem](../start/get-started-sources.md)

➡️ [Tutorial: Criar conjuntos de dados e assimilar dados](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configurar fontes de dados no Journey Optimizer

As fontes de dados são um conceito específico do Journey Optimizer: não são onde seus dados residem, mas onde você declara quais campos o Journey Optimizer tem permissão para ler durante a execução da jornada e da mensagem. Antes que uma jornada possa avaliar uma condição como &quot;o cliente é um membro do programa de fidelidade?&quot; Para personalizar uma mensagem com um nome, os campos de perfil relevantes devem ser expostos por meio de uma configuração de fonte de dados.

O Journey Optimizer inclui uma [fonte de dados Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) interna que dá acesso direto aos atributos do Perfil do Cliente em Tempo Real. Isso abrange a grande maioria dos casos de uso: ler atributos de perfil para personalização ou verificar campos de consentimento e preferência. Você também pode configurar [fontes de dados externas](../datasource/external-data-sources.md) para chamar APIs de terceiros no tempo de execução do jornada — por exemplo, para recuperar uma pontuação de fidelidade em tempo real, uma recomendação de produto ou um nível de inventário de loja que não esteja armazenado no Adobe Experience Platform.

>[!NOTE]
>O acesso direto aos dados do evento da experiência por meio da fonte de dados integrada do Adobe Experience Platform está obsoleto e sendo progressivamente desativado. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

Configurar fontes de dados é uma tarefa administrativa que desbloqueia a camada de dados completa para autores e profissionais de marketing do jornada. Depois que um campo é exposto por meio de uma fonte de dados, ele fica disponível no construtor de condições de jornada, em editores de personalização de mensagens e em regras do Offer Decisioning — sem exigir trabalho de engenharia adicional no momento da criação da jornada.

➡️ [Saiba mais sobre a configuração da fonte de dados](../datasource/about-data-sources.md)

+++

+++ Verificar rastreamento, feedback e conjuntos de dados de jornada

Confirme se os conjuntos de dados gerados pelo sistema da Journey Optimizer estão disponíveis no espaço de trabalho Conjuntos de dados. Execute jornadas e campanhas de teste e, em seguida, use o Editor de consultas para verificar se os eventos de envio, abertura, clique e rejeição estão registrados e se os eventos e estados de etapa de jornada foram capturados corretamente. Use esses conjuntos de dados para monitoramento contínuo, solução de problemas e otimização de jornadas.

➡️ [Saiba mais sobre consultas no Journey Optimizer](get-started-queries.md)

+++

## Medidas de proteção e considerações sobre o design de dados {#guardrails}

Algumas medidas de proteção e limitações do produto podem influenciar a maneira como você projeta o modelo de dados e as jornadas. Analise esses itens antecipadamente para evitar retrabalho posteriormente.

>[!IMPORTANT]
>Sempre consulte a página [Medidas de proteção e limitações do Journey Optimizer](../start/guardrails.md) para obter as informações mais recentes. Os resumos abaixo destacam os principais itens, mas podem evoluir com o tempo.

### Conjuntos de dados do sistema Journey Optimizer e TTL {#datasets-ttl}

O Journey Optimizer cria vários conjuntos de dados gerados pelo sistema para rastreamento, feedback e eventos de etapa de jornada. A partir de fevereiro de 2025, uma proteção de TTL (time-to-live, tempo de vida útil) está sendo implantada em alguns desses conjuntos de dados, o que pode afetar por quanto tempo os dados serão retidos para análise e solução de problemas.

➡️ [Saiba mais sobre as medidas de proteção do TTL do conjunto de dados](datasets-ttl.md)

### Segmentação de transmissão e eventos do Journey Optimizer {#streaming-segmentation}

A partir de 1º de novembro de 2024, a segmentação por transmissão não oferecerá mais suporte a eventos de envio e abertura de conjuntos de dados de rastreamento e feedback do Journey Optimizer. Para casos de uso como limite de frequência e gerenciamento de fadiga, use [Regras de negócio](../conflict-prioritization/rule-sets.md) em vez de segmentos de streaming com base em eventos de envio/abertura.

➡️ [Saiba mais sobre conjuntos de dados](get-started-datasets.md)

### Pesquisa e decisão do conjunto de dados {#lookup-guardrails}

A pesquisa do conjunto de dados é ideal para atributos (inventário, preços, clima) ou dados que mudam com frequência e que não precisam ser armazenados no Perfil do cliente em tempo real. Revise as medidas de proteção específicas do produto, como limites de tamanho do conjunto de dados e limites de consulta na documentação relevante antes de projetar sua estratégia de pesquisa.

➡️ [Saiba mais sobre conjuntos de dados de pesquisa](lookup-aep-data.md)

## Exemplo: preparação de dados para uma jornada de boas-vindas {#example}

O exemplo a seguir mostra como os conceitos desta página funcionam juntos em um cenário simples.

1. Um engenheiro de dados cria um [esquema do Perfil Individual XDM](get-started-schemas.md) para atributos do cliente (nome, email, nível de fidelidade, consentimento) e um esquema XDM ExperienceEvent para eventos de inscrição na Web.
1. [Conjuntos de dados habilitados para perfil](get-started-datasets.md) são criados para cada esquema: um para atributos do CRM e um para eventos de inscrição.
1. Equipes da Web e móveis transmitem eventos de inscrição por meio do Adobe Experience Platform Web SDK; os dados do CRM são assimilados por meio de um [conector de origem](../start/get-started-sources.md).
1. Um administrador configura a [fonte de dados do Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) no Journey Optimizer e expõe campos como `profile.person.name.firstName`, `profile.personalEmail.address` e `profile.loyaltyTier`.
1. Um comerciante [cria uma jornada de boas-vindas](../building-journeys/journey-gs.md) que escuta um evento de inscrição e usa esses atributos de perfil para [personalizar o email de boas-vindas](../personalization/personalize.md). O Journey Optimizer grava eventos de envio e abertos em conjuntos de dados de rastreamento e registra o progresso da jornada em conjuntos de dados de eventos de etapa do jornada.
1. Um desenvolvedor usa o [Editor de consultas](get-started-queries.md) para verificar se os eventos estão fluindo corretamente e analisa o desempenho (aberturas, cliques, tempo de envio). A equipe ajusta a jornada e o conteúdo com base nesses insights.

Esse fluxo ilustra como esquemas, conjuntos de dados, fontes, fontes de dados e consultas trabalham juntos em um caso de uso completo e de fácil introdução.

## Recursos relacionados {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

**Introdução a esquemas**

Saiba como criar esquemas XDM no Adobe Experience Platform, escolher a classe e os grupos de campos corretos e modelar os atributos de perfil e os eventos comportamentais.

[Saiba mais](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=pt-BR)

**Trabalhar com conjuntos de dados**

Entenda como criar conjuntos de dados habilitados para perfil e de evento, monitorar a assimilação de dados e explorar os conjuntos de dados gerados pelo sistema que a Journey Optimizer cria automaticamente para eventos de etapa de rastreamento, feedback e jornada.

[Saiba mais](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

**Configurar fontes de dados**

Orientação passo a passo sobre como configurar a fonte de dados integrada do Adobe Experience Platform e as fontes de dados externas opcionais para expor campos de perfil e respostas da API externa dentro das jornadas.

[Saiba mais](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

**Usar dados (pesquisa) do Adobe Experience Platform**

Descubra como enriquecer mensagens no tempo de execução com dados de referência ou transacionais de conjuntos de dados da AEP, sem armazenar esses dados no Perfil do cliente em tempo real.

[Saiba mais](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

**Introdução a consultas**

Use o Serviço de consulta para analisar conjuntos de dados do Journey Optimizer, verificar se os eventos estão fluindo corretamente e criar consultas de relatório sobre dados de envio, abertura, clique e rejeição.

[Saiba mais](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

**Introdução a perfis**

Saiba como o Perfil do cliente em tempo real funciona no Journey Optimizer e como procurar, inspecionar e validar perfis de clientes individuais na interface do usuário da plataforma.

[Saiba mais](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

**Configurar o tutorial de visão geral de dados**

Uma apresentação em vídeo de fácil introdução sobre a configuração de dados no Journey Optimizer, abrangendo esquemas, conjuntos de dados e fontes de ponta a ponta.

[Assistir ao tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

**Criar conjuntos de dados e assimilar tutorial de dados**

Um tutorial prático que mostra como criar conjuntos de dados no Adobe Experience Platform e assimilar dados usando conectores de origem, com instruções passo a passo que você pode seguir em sua própria sandbox.

[Assistir ao tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
