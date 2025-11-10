---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes sobre campanhas orquestradas
description: Perguntas frequentes sobre as campanhas do Journey Optimizer Orchestrated
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 536d080e455e4872ed6e58b11adc3324b332f7b5
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 13%

---

# Perguntas frequentes {#faq-oc}

Você encontrará abaixo Perguntas frequentes sobre as campanhas do Adobe Journey Optimizer Orchestrated.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++ O que é a orquestração de campanhas?

O Campaign Orchestration é um recurso do Journey Optimizer que oferece suporte a fluxos de trabalho de etapa única ou de várias etapas que aproveitam o armazenamento de dados relacional para criar e segmentar públicos-alvo com a finalidade de envolvimento em lote.

Ela traz um novo tipo de campanha para a Journey Optimizer: **Campanhas orquestradas**. As campanhas orquestradas ajudam as marcas a executar campanhas de marketing complexas, de um para muitos, em escala. Eles foram projetados para engajamento iniciado pela marca, como promoções, campanhas sazonais ou comunicações baseadas em conta.

Comparado às campanhas de envio único/ação, eles trazem a **orquestração e o sequenciamento** para o marketing de saída: os públicos-alvo se movem em conjunto por um fluxo de trabalho de várias etapas, em vez de receberem uma explosão única.

**Saiba mais**

* [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)
* [Crie sua primeira campanha orquestrada](gs-campaign-creation.md)

+++

+++ O que posso fazer com uma campanha orquestrada?

Os principais recursos incluem:

* **Públicos-alvo sob demanda**: crie e refine instantaneamente grupos-alvo usando consultas relacionais.
* **Segmentação de Várias Entidades**: crie públicos-alvo precisos conectando dados do cliente a entidades relacionadas (por exemplo, contas, compras, reservas).
* **Visibilidade de pré-envio**: veja a contagem precisa de públicos-alvo antes de iniciar para otimizar o direcionamento.
* **Fluxos de Trabalho de Várias Etapas**: Execute campanhas sequenciadas, como promoções sazonais, inicializações de produtos ou ofertas de fidelidade.

**Práticas recomendadas**

* Defina um **limpar objetivo de campanha** antes de criar fluxos de trabalho.
* Comece com um **público-alvo piloto** para validar as contagens e a lógica antes do dimensionamento.
* Mantenha as regras de segmentação **o mais simples possível** para otimizar o desempenho e a transparência.
* Use **convenções de nomenclatura consistentes** para públicos e campanhas para facilitar o gerenciamento.

**Saiba mais**

* [Criar uma campanha orquestrada](create-orchestrated-campaign.md)
* [Trabalhar com atividades de campanha](activities/about-activities.md)
* [Criar sua regra usando o modelador de consultas](build-query.md)

+++

+++ Como obter acesso à orquestração do Campaign?

Para acessar a Orquestração de campanha, sua licença deve incluir o pacote **Journey Optimizer – Campanhas e jornadas** ou **Journey Optimizer – Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizá-la, se necessário.

**Saiba mais**

* [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)
* [Descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}

+++

+++ Como as campanhas orquestradas são diferentes do Jornada?

* **Campanhas orquestradas**: ideal para **campanhas em lote, de um para muitos**. Os públicos-alvo avançam em massa, de acordo com uma programação.
* **Jornadas**: ideal para o engajamento **em tempo real, um para um**. Cada cliente percorre a jornada em seu próprio ritmo, acionado por comportamento ou eventos.

**Prática recomendada**: use-as juntas — Jornadas para experiências acionadas e reativas e Campanhas orquestradas para iniciativas planejadas baseadas em calendário.

**Saiba mais**

* [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)
* [Criar a primeira jornada](../building-journeys/journey-gs.md)
* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

+++

+++ O que é a segmentação de várias entidades?

O Campaign Orchestration no Adobe Journey Optimizer usa um banco de dados relacional. Esse tipo de modelo de dados tem esquemas separados de dados que são conectados por meio de relações 1:1 ou 1:many. Isso permite que os usuários iniciem um query em qualquer esquema, não apenas no nível do recipient, e então virem e voltarem para outros esquemas relacionados, como compras, produtos, reservas ou detalhes do recipient, proporcionando grande flexibilidade em como segmentos e públicos-alvo podem ser criados e refinados.

**Exemplo** - Direcione todos os destinatários com assinaturas que vencem nos próximos 30 dias. No Campaign Orchestration, a consulta pode começar com o schema Subscriptions, pesquisar apenas a coluna Data de expiração desse esquema e retornar todas as assinaturas que estão prestes a expirar e, em seguida, acumular para os dados do recipient relacionados a essas IDs de assinaturas específicas que retornam resultados de forma mais rápida e eficiente do que os modelos de dados que começam cada consulta no nível do recipient.

**Saiba mais**

* [Introdução a esquemas e conjuntos de dados](gs-schemas.md)
* [Configurar um targeting dimension](target-dimension.md)
* [Criar sua regra usando o modelador de consultas](build-query.md)

+++

+++ Como funciona o modelo de dados?

As campanhas usam um **banco de dados relacional**. Isso permite consultar diferentes conjuntos de dados (por exemplo, clientes, produtos, assinaturas) e conectá-los de forma flexível para segmentação avançada.

**Práticas recomendadas**

* Organize os conjuntos de dados para que **relacionamentos (junções)** reflitam a lógica de negócios.
* Evite associações desnecessárias para manter as consultas com desempenho.
* Valide os resultados da amostra antes de executar extrações em larga escala.

**Saiba mais**

* [Introdução a esquemas e conjuntos de dados](gs-schemas.md)
* [Criar um esquema manualmente](manual-schema.md)
* [Assimilar dados](ingest-data.md)

+++

+++ Posso personalizar mensagens com dados relacionais?

Sim. Na Orquestração de campanhas, um perfil de recipient conhecido como &quot;Entidade de Pessoas&quot; pode ser atualizado e esses dados são usados para personalização. Além disso, dados enriquecidos de entidades vinculadas no banco de dados relacional também podem ser usados para personalização. Você pode usar perfis de clientes juntamente com dados vinculados (como compras ou assinaturas) para personalizar o conteúdo em todos os canais compatíveis.

**Recommendations**

* Use **dados transacionais e comportamentais** para tornar as ofertas relevantes.
* Combinar **atributos estáticos** (por exemplo, nível de fidelidade) com **atributos dinâmicos** (por exemplo, data da última compra).
* Mantenha a personalização concisa — sobrecarregar mensagens com dados pode prejudicar a legibilidade.

**Saiba mais**

* [Usar a atividade Enriquecimento](activities/enrichment.md)
* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)

+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Quais canais são compatíveis?

Você pode criar campanhas orquestradas para enviar **emails**, **SMS** e **notificações por push**.

**Saiba mais**

* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)
* [Trabalhar com atividades de campanha](activities/about-activities.md)

+++

+++ É possível iniciar várias comunicações e canais diferentes na mesma campanha orquestrada?

Sim, as campanhas orquestradas oferecem suporte à orquestração entre canais. Você pode combinar atividades de email, SMS e notificação por push em uma tela de campanha com várias etapas para criar experiências abrangentes para o cliente.

**Saiba mais**

* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)
* [Trabalhar com atividades de campanha](activities/about-activities.md)

+++

+++ Os templates de campanha orquestrados estão disponíveis?

Não, você não pode definir ou usar modelos de campanha, mas pode usar modelos de conteúdo para suas comunicações.

**Saiba mais**

* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)
* [Criar uma campanha orquestrada](create-orchestrated-campaign.md)

+++

+++ O designer de conteúdo é responsável por mensagens específicas para campanhas orquestradas?

Não, o designer de conteúdo, incluindo o Designer de email, é comum em todos os recursos do Journey Optimizer.

**Saiba mais**

* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)
* [Usar a atividade Enriquecimento](activities/enrichment.md)

+++

+++ Como os diferentes canais são conectados nas campanhas Orquestradas?

O componente de canal e o tempo de execução são comuns a todas as campanhas do Journey Optimizer, no entanto, os canais compatíveis diferem. As campanhas orquestradas aceitam notificações por email, SMS e por push.

**Saiba mais**

* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)
* [Medidas de proteção e limitações](guardrails.md)

+++


+++ As campanhas orquestradas podem se conectar com canais de saída (web, inApp)?

Não, canais de entrada como web e no aplicativo não são compatíveis com campanhas orquestradas. Somente canais de saída (email, SMS e notificações por push) são compatíveis.

**Saiba mais**

* [Medidas de proteção e limitações](guardrails.md)
* [Adicionar uma atividade de canal em uma campanha orquestrada](activities/channels.md)

+++

+++ E quanto a permissões e consentimento?

As permissões e o consentimento para campanhas e jornadas orquestradas são gerenciados centralmente no Adobe Experience Platform. Essas configurações são aplicadas em ambas as soluções para cada recipient antes do envio.

**Práticas recomendadas**

* Aplique a **governança centralizada** — evite gerenciar o consentimento separadamente no nível da campanha.
* Auditoria periódica de dados de consentimento para detectar inconsistências.
* Respeite as **opções de não participação específicas do canal** — não assuma que o consentimento global abranja todos os canais.

**Saiba mais**

* [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)
* [Medidas de proteção e limitações](guardrails.md)

+++


+++ Posso fazer a segmentação ad-hoc em campanhas orquestradas?

No Campaign Orchestration, nós nos referimos à segmentação ad-hoc como &quot;Segmentação em tempo real&quot;, onde você pode acessar todos os dados disponíveis na loja relacional em tempo real, criar uma consulta complexa sobre ela e obter o resultado para ativação instantânea por meio de canais de saída (por exemplo: Email + SMS).

**Dicas**

* Use a segmentação ad-hoc para **necessidades sensíveis ao tempo** (por exemplo, promoções em flash).
* Salve e documente consultas úteis para que elas possam ser reutilizadas em campanhas futuras.
* Valide a contagem de público-alvo antes da ativação para evitar o envio insuficiente ou excessivo.

**Saiba mais**

* [Criar sua regra usando o modelador de consultas](build-query.md)
* [Usar a atividade de criar público-alvo](activities/build-audience.md)
* [Configurar um targeting dimension](target-dimension.md)

+++


+++ O Campaign Orchestration acessa apenas dados carregados por lote ou também pode consultar tabelas atualizadas em tempo real (como dados do Analytics)?

O Journey Optimizer Campaign Orchestration pode criar consultas ad-hoc com base em esquemas baseados em modelo. Por enquanto, os esquemas baseados em modelo oferecem suporte apenas a origens em lote. Além disso, oferece suporte às atividades Ler público-alvo de qualquer tipo de público-alvo da Adobe Experience Platform.

**Saiba mais**

* [Introdução a esquemas e conjuntos de dados](gs-schemas.md)
* [Assimilar dados](ingest-data.md)
* [Usar a atividade Público-alvo de leitura](activities/read-audience.md)

+++

+++ As campanhas orquestradas são compatíveis com a tomada de decisão?

Não, as campanhas orquestradas não oferecem suporte aos recursos de decisão. Para recursos de decisão, use jornadas padrão do Journey Optimizer ou campanhas de ação.

**Saiba mais**

* [Introdução à Escolha de experiências](../experience-decisioning/gs-experience-decisioning.md)
* [Criar a primeira jornada](../building-journeys/journey-gs.md)
* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

+++


+++ Como funciona a implantação entre ambientes?

Objetos criados em campanhas orquestradas (por exemplo, públicos, fluxos de trabalho) são vinculados à sandbox em que são criados. Os workflows padrão de empacotamento e implantação em ambientes (desenvolvimento, preparo, produção) não estão disponíveis no momento para campanhas orquestradas.

**Práticas recomendadas**

* Mantenha **sandboxes separadas** para experimentação, controle de qualidade e produção.
* Documente as configurações completamente para permitir a replicação manual, se necessário.
* Alinhe-se às equipes de governança para reduzir a variação de configuração entre ambientes.

**Saiba mais**

* [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)
* [Medidas de proteção e limitações](guardrails.md)

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Qual é a relação entre Entidades de Destinatário e Perfil?

A segmentação é executada nos recipients ao enviar para o Perfil do Adobe Experience Platform. A dimensão de destino do Recipient estende o Perfil unificado com dados adicionais que são usados para segmentação em campanhas orquestradas, enquanto o Recipient é reconciliado com o Perfil no tempo de execução para enviar mensagens e verificar a política de consentimento e as regras de negócios. Essa reconciliação é útil para unificar regras de negócios e aplicativos de consentimento no nível do perfil.

![](assets/recipients-and-profiles.png)

**Saiba mais**

* [Configurar um targeting dimension](target-dimension.md)
* [Introdução a esquemas e conjuntos de dados](gs-schemas.md)
* [Criar sua regra usando o modelador de consultas](build-query.md)

+++

+++ Em quais casos é recomendável usar Entidades de destinatário vs. de perfil?

Responder &quot;Sim&quot; sugere o melhor armazenamento de dados, mas sempre confirme a melhor abordagem com base no caso de uso e nas restrições com o representante da Adobe.

| Armazenamento Relacional | Perfil do cliente em tempo real |
|---------|----------|
| A origem já é o relacional de dados? | A origem do streaming de dados é? |
| Você planeja assimilar dados como eles para casos de uso de marketing? | A atualização de dados é um requisito importante? |
| Há um grande volume de dados históricos (`>` 2 meses) necessários para casos de uso de ativação de marketing? | Existem cenários em que a ação ou a decisão no momento exigem dados? |
| Há necessidades específicas para criação, avaliação e ativação de públicos-alvo? | Os dados comportamentais podem ser limitados a `<` 90 dias usando agregados pré-calculados? |
|  | Os dados são necessários para personalizar mensagens em tempo real? |

**Saiba mais**

* [Configurar um targeting dimension](target-dimension.md)
* [Introdução a esquemas e conjuntos de dados](gs-schemas.md)
* [Criar sua regra usando o modelador de consultas](build-query.md)

+++

+++ Qual é o número máximo de atividades por campanha orquestrada?

O número de atividades em uma campanha orquestrada é limitado a 500.

**Saiba mais**

* [Medidas de proteção e limitações](guardrails.md)
* [Trabalhar com atividades de campanha](activities/about-activities.md)

+++

+++ É possível executar enriquecimentos para acrescentar dados adicionais?

Sim, você pode enriquecer dados da loja relacional e dos públicos da Adobe Experience Platform. Use a atividade Enrichment para aprimorar os dados do público-alvo com atributos adicionais de esquemas relacionados.

**Saiba mais**

* [Usar a atividade Enriquecimento](activities/enrichment.md)
* [Usar a atividade de reconciliação](activities/reconciliation.md)

+++

+++ Todos os filtros devem ser definidos por meio de públicos-alvo ou algum tipo de filtro pode ser configurado?

As campanhas orquestradas são compatíveis com Filtros predefinidos: é possível definir e salvar uma consulta como filtro e adicioná-la aos favoritos para ser reutilizada em tarefas de segmentação adicionais.

**Saiba mais**

* [Criar sua regra usando o modelador de consultas](build-query.md)
* [Usar a atividade de criar público-alvo](activities/build-audience.md)
* [Trabalhar com filtros predefinidos](orchestrated-rule-builder.md)

+++


## Recursos adicionais

Para obter mais informações e atualizações, explore os seguintes recursos:

* [Medidas de proteção e limitações para campanhas orquestradas](guardrails.md)
* [Introdução a esquemas e conjuntos de dados em campanhas orquestradas](gs-schemas.md)
* [Crie sua primeira campanha orquestrada](gs-campaign-creation.md)
* [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
