---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes sobre campanhas orquestradas
description: Perguntas frequentes sobre as campanhas do Journey Optimizer Orchestrated
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 9ae0d910f6246b87683b04db97bbdb7355beb349
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 3%

---

# Perguntas frequentes {#faq-oc}

Você encontrará abaixo Perguntas frequentes sobre as campanhas do Adobe Journey Optimizer Orchestrated.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## O que é a orquestração de campanhas? {#what-are-oc}

O Campaign Orchestration é um recurso do Journey Optimizer que oferece suporte a fluxos de trabalho de etapa única ou de várias etapas que aproveitam o armazenamento de dados relacional para criar e segmentar públicos-alvo com a finalidade de envolvimento em lote.

Ela traz um novo tipo de campanha para a Journey Optimizer: **Campanhas orquestradas**. As campanhas orquestradas ajudam as marcas a executar campanhas de marketing complexas, de um para muitos, em escala. Eles foram projetados para engajamento iniciado pela marca, como promoções, campanhas sazonais ou comunicações baseadas em conta.

Comparado às campanhas de envio único/ação, eles trazem a **orquestração e o sequenciamento** para o marketing de saída: os públicos-alvo se movem em conjunto por um fluxo de trabalho de várias etapas, em vez de receberem uma explosão única.

## O que posso fazer com uma campanha orquestrada? {#what-can-i-do}

Os principais recursos incluem:

* **Públicos-alvo sob demanda**: crie e refine instantaneamente grupos-alvo usando consultas relacionais.
* **Segmentação de Várias Entidades**: crie públicos-alvo precisos conectando dados do cliente a entidades relacionadas (por exemplo, contas, compras, reservas).
* **Visibilidade de pré-envio**: veja a contagem precisa de públicos-alvo antes de iniciar para otimizar o direcionamento.
* **Fluxos de Trabalho de Várias Etapas**: Execute campanhas sequenciadas, como promoções sazonais, inicializações de produtos ou ofertas de fidelidade.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Defina um **limpar objetivo de campanha** antes de criar fluxos de trabalho.
* Comece com um **público-alvo piloto** para validar as contagens e a lógica antes do dimensionamento.
* Mantenha as regras de segmentação **o mais simples possível** para otimizar o desempenho e a transparência.
* Use **convenções de nomenclatura consistentes** para públicos e campanhas para facilitar o gerenciamento.

>[!ENDSHADEBOX]

## Como acessar a orquestração do Campaign? {#access-oc}

Para acessar a Orquestração de campanha, sua licença deve incluir o pacote **Journey Optimizer – Campanhas e jornadas** ou **Journey Optimizer – Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizá-la, se necessário.

Saiba mais sobre o modelo de licenciamento do Campaign Orchestration em [descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

## Como as campanhas orquestradas são diferentes do Jornada? {#oc-vs-journeys}

* **Campanhas orquestradas**: ideal para **campanhas em lote, de um para muitos**. Os públicos-alvo avançam em massa, de acordo com uma programação.
* **Jornadas**: ideal para o engajamento **em tempo real, um para um**. Cada cliente percorre a jornada em seu próprio ritmo, acionado por comportamento ou eventos.

>[!BEGINSHADEBOX]

**Prática recomendada**: use-as juntas — Jornadas para experiências acionadas e reativas e Campanhas orquestradas para iniciativas planejadas baseadas em calendário.

>[!ENDSHADEBOX]

## O que é a segmentação de várias entidades? {#multi-entity}

O Campaign Orchestration no Adobe Journey Optimizer usa um banco de dados relacional. Esse tipo de modelo de dados tem esquemas separados de dados que são conectados por meio de relações 1:1 ou 1:many. Isso permite que os usuários iniciem um query em qualquer esquema - não apenas no nível do recipient - e, em seguida, virem e voltarem para outros esquemas relacionados, como compras, produtos, reservas ou detalhes do recipient, proporcionando grande flexibilidade em como segmentos e públicos-alvo podem ser criados e
refinado.

>[!BEGINSHADEBOX]

**Exemplo** - Direcione todos os destinatários com assinaturas que vencem nos próximos 30 dias. No Campaign Orchestration, a consulta pode começar com o schema Subscriptions, pesquisar apenas a coluna Data de expiração desse esquema e retornar todas as assinaturas que estão prestes a expirar e, em seguida, acumular para os dados do recipient relacionados a essas IDs de assinaturas específicas que retornam resultados de forma mais rápida e eficiente do que os modelos de dados que começam cada consulta no nível do recipient.

>[!ENDSHADEBOX]


## Como funciona o modelo de dados? {#data-model}

As campanhas usam um **banco de dados relacional**. Isso permite consultar diferentes conjuntos de dados (por exemplo, clientes, produtos, assinaturas) e conectá-los de forma flexível para segmentação avançada.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Organize os conjuntos de dados para que **relacionamentos (junções)** reflitam a lógica de negócios.
* Evite associações desnecessárias para manter as consultas com desempenho.
* Valide os resultados da amostra antes de executar extrações em larga escala.

>[!ENDSHADEBOX]

## Posso personalizar mensagens com dados relacionais? {#personalization}

Sim. Na Orquestração de campanhas, um perfil de recipient conhecido como &quot;Entidade de Pessoas&quot; pode ser atualizado e esses dados são usados para personalização. Além disso, dados enriquecidos de entidades vinculadas no banco de dados relacional também podem ser usados para personalização. Você pode usar perfis de clientes juntamente com dados vinculados (como compras ou assinaturas) para personalizar o conteúdo em todos os canais compatíveis.

>[!BEGINSHADEBOX]

**Recommendations**

* Use **dados transacionais e comportamentais** para tornar as ofertas relevantes.
* Combinar **atributos estáticos** (por exemplo, nível de fidelidade) com **atributos dinâmicos** (por exemplo, data da última compra).
* Mantenha a personalização concisa — sobrecarregar mensagens com dados pode prejudicar a legibilidade.

>[!ENDSHADEBOX]

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

## Quais canais são compatíveis? {#channels}

Você pode criar campanhas orquestradas para enviar **emails**, **SMS** e **notificações por push**.

## É possível iniciar várias comunicações e canais diferentes na mesma campanha orquestrada?

Sim, as campanhas orquestradas oferecem suporte à orquestração entre canais.

## Os templates de campanha orquestrados estão disponíveis?

Não, você não pode definir ou usar modelos de campanha, mas pode usar modelos de conteúdo para suas comunicações.

## O designer de conteúdo é responsável por mensagens específicas para campanhas orquestradas?

Não, o designer de conteúdo, incluindo o Designer de email, é comum em todos os recursos do Journey Optimizer.

## Como os diferentes canais são conectados nas campanhas Orquestradas?

O componente de canal e o tempo de execução são comuns a todas as campanhas do Journey Optimizer, no entanto, os canais compatíveis diferem.

## As campanhas orquestradas podem se conectar com canais de saída (web, inApp)?

Não, os canais de saída não são compatíveis com campanhas orquestradas.


## E quanto a permissões e consentimento? {#permissions}

As permissões e o consentimento para campanhas e jornadas orquestradas são gerenciados centralmente no Adobe Experience Platform. Essas configurações são aplicadas em ambas as soluções para cada recipient antes do envio.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Aplique a **governança centralizada** — evite gerenciar o consentimento separadamente no nível da campanha.
* Auditoria periódica de dados de consentimento para detectar inconsistências.
* Respeite as **opções de não participação específicas do canal** — não assuma que o consentimento global abranja todos os canais.

>[!ENDSHADEBOX]

## Posso fazer a segmentação ad-hoc em campanhas orquestradas? {#ad-hoc}

No Campaign Orchestration, nós nos referimos à segmentação ad-hoc como &quot;Segmentação em tempo real&quot;, onde você pode acessar todos os dados disponíveis na loja relacional em tempo real, criar uma consulta complexa sobre ela e obter o resultado para ativação instantânea por meio de canais de saída (por exemplo: Email + SMS).

>[!BEGINSHADEBOX]

**Dicas**

* Use a segmentação ad-hoc para **necessidades sensíveis ao tempo** (por exemplo, promoções em flash).
* Salve e documente consultas úteis para que elas possam ser reutilizadas em campanhas futuras.
* Valide a contagem de público-alvo antes da ativação para evitar o envio insuficiente ou excessivo.

>[!ENDSHADEBOX]

## O Campaign Orchestration acessa apenas dados carregados por lote ou também pode consultar tabelas atualizadas em tempo real (como dados do Analytics)?

O Journey Optimizer Campaign Orchestration pode criar primeiro uma consulta ad-hoc com base em Esquemas relacionais. Os Esquemas Relacionais suportam Origens em Lote somente por enquanto. Além disso, oferece suporte para o recurso Ler público-alvo de qualquer tipo de público-alvo da Adobe Experience Platform.

## As campanhas orquestradas são compatíveis com a tomada de decisão? {#decisioning}

Sim. A Decisão pode usar dados relacionais de campanhas orquestradas. Depois que o esquema relacional é conectado aos esquemas XDM, os dados XDM podem ser usados na tomada de decisão.

## Como funciona a implantação entre ambientes? {#deployment}

Objetos criados em campanhas orquestradas (por exemplo, públicos, fluxos de trabalho) são vinculados à sandbox em que são criados. Os workflows padrão de empacotamento e implantação em ambientes (desenvolvimento, preparo, produção) não estão disponíveis no momento para campanhas orquestradas.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Mantenha **sandboxes separadas** para experimentação, controle de qualidade e produção.
* Documente as configurações completamente para permitir a replicação manual, se necessário.
* Alinhe-se às equipes de governança para reduzir a variação de configuração entre ambientes.

>[!ENDSHADEBOX]

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

## Qual é a relação entre Entidades de Destinatário e Perfil?

A segmentação é executada nos recipients ao enviar para o Perfil do Adobe Experience Platform. A dimensão de destino do Recipient estende o Perfil unificado com dados adicionais que são usados para segmentação em campanhas orquestradas, enquanto o Recipient é reconciliado com o Perfil no tempo de execução para enviar mensagens e verificar a política de consentimento e as regras de negócios. Essa reconciliação é útil para unificar regras de negócios e aplicativos de consentimento no nível do perfil

![](assets/recipients-and-profiles.png)


## Em quais casos é recomendável usar Entidades de destinatário vs. de perfil?

Responder &quot;Sim&quot; sugere o melhor armazenamento de dados, mas sempre confirme a melhor abordagem com base no caso de uso e nas restrições com o representante da Adobe.

| Armazenamento Relacional | Perfil do cliente em tempo real |
|---------|----------|
| A origem já é o relacional de dados? | A origem do streaming de dados é? |
| Você planeja assimilar dados como eles para casos de uso de marketing? | A atualização de dados é um requisito importante? |
| Há um grande volume de dados históricos (`>` 2 meses) necessários para casos de uso de ativação de marketing? | Existem cenários em que a ação ou a decisão no momento exigem dados? |
| Há necessidades específicas para criação, avaliação e ativação de públicos-alvo? | Os dados comportamentais podem ser limitados a `<` 90 dias usando agregados pré-calculados? |
|  | Os dados são necessários para personalizar mensagens em tempo real? |


## Qual é o número máximo de atividades por campanha orquestrada?

O número de atividades em uma campanha orquestrada é limitado a 500.

## É possível executar enriquecimentos para acrescentar dados adicionais?

Sim, você pode enriquecer dados da loja relacional e dos públicos da Adobe Experience Platform.

## Todos os filtros devem ser definidos por meio de públicos-alvo ou algum tipo de filtro pode ser configurado?

As campanhas orquestradas são compatíveis com Filtros predefinidos: é possível definir e salvar uma consulta como filtro e adicioná-la aos favoritos para ser reutilizada em tarefas de segmentação adicionais.



>[!MORELIKETHIS]
>
>* [Medidas de proteção e limitações para campanhas orquestradas](../orchestrated/guardrails.md)
>* [Introdução a esquemas e conjuntos de dados em campanhas orquestradas](../orchestrated/gs-schemas.md)
>* [Crie sua primeira campanha orquestrada](../orchestrated/gs-campaign-creation.md)
>* [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
