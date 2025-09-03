---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes sobre campanhas orquestradas
description: Perguntas frequentes sobre as campanhas do Journey Optimizer Orchestrated
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: a6a8521254005159b410790f88877d0591a16d15
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 4%

---

# Perguntas frequentes {#faq-oc}

Você encontrará abaixo Perguntas frequentes sobre as campanhas do Adobe Journey Optimizer Orchestrated.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para levantar sua pergunta.

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


## Quais canais são compatíveis? {#channels}

Você pode criar campanhas orquestradas para enviar **emails**, **SMS** e **notificações por push**.


>[!BEGINSHADEBOX]

**Recommendations**

* Corresponda o canal à **natureza da sua mensagem** (por exemplo, urgente = SMS, ofertas personalizadas = email, contextual = push).
* Sempre valide as preferências de consentimento e assinatura antes de ativar um canal.
* Teste a renderização da mensagem em vários dispositivos e clientes para garantir uma experiência consistente.

>[!ENDSHADEBOX]


## Como as campanhas orquestradas são diferentes do Jornada? {#oc-vs-journeys}

* **Campanhas orquestradas**: ideal para **campanhas em lote, de um para muitos**. Públicos-alvo inteiros se movem pela tela de campanha juntos.
* **Jornadas**: ideal para o engajamento **em tempo real, um para um**. Cada cliente percorre a jornada em seu próprio ritmo, acionado por comportamento ou eventos.

>[!BEGINSHADEBOX]

**Dica** - Muitas organizações usam **as duas opções juntas**—Jornadas para experiências acionadas e reativas e campanhas orquestradas para iniciativas planejadas baseadas em calendário.

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

## Posso personalizar mensagens com esses dados? {#personalization}

Sim. Na Orquestração de campanhas, um perfil de recipient conhecido como &quot;Entidade de Pessoas&quot; pode ser atualizado e esses dados são usados para personalização. Além disso, dados enriquecidos de entidades vinculadas no banco de dados relacional também podem ser usados para personalização. Você pode usar perfis de clientes juntamente com dados vinculados (como compras ou assinaturas) para personalizar o conteúdo em todos os canais compatíveis.

>[!BEGINSHADEBOX]

**Recommendations**

* Use **dados transacionais e comportamentais** para tornar as ofertas relevantes.
* Combinar **atributos estáticos** (por exemplo, nível de fidelidade) com **atributos dinâmicos** (por exemplo, data da última compra).
* Mantenha a personalização concisa — sobrecarregar mensagens com dados pode prejudicar a legibilidade.

>[!ENDSHADEBOX]


## Ele se integra a outras soluções da Adobe? {#integrations}

Sim. A orquestração de campanha é integrada nativamente com:

* **Customer Journey Analytics**: os relatórios de orquestração de campanha estão disponíveis.
* **Real-Time CDP**: os públicos-alvo criados nas Campanhas podem ser lidos no Real-Time CDP.
* **Federated Audience Composition (FAC)**: disponível como um complemento.

## E quanto a permissões e consentimento? {#permissions}

As permissões e o consentimento para campanhas e jornadas orquestradas são gerenciados centralmente no Adobe Experience Platform. Essas configurações são aplicadas em ambas as soluções para cada recipient antes do envio.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Aplique a **governança centralizada** — evite gerenciar o consentimento separadamente no nível da campanha.
* Auditoria periódica de dados de consentimento para detectar inconsistências.
* Respeite as **opções de não participação específicas do canal** — não assuma que o consentimento global abranja todos os canais.

>[!ENDSHADEBOX]

## Posso fazer a segmentação ad-hoc? {#ad-hoc}

No Campaign Orchestration, nós nos referimos à segmentação ad-hoc como &quot;Segmentação em tempo real&quot;, onde você pode acessar todos os dados disponíveis na loja relacional em tempo real, criar uma consulta complexa sobre ela e obter o resultado para ativação instantânea por meio de canais de saída (por exemplo: Email + SMS).

>[!BEGINSHADEBOX]

**Dicas**

* Use a segmentação ad-hoc para **necessidades sensíveis ao tempo** (por exemplo, promoções em flash).
* Salve e documente consultas úteis para que elas possam ser reutilizadas em campanhas futuras.
* Valide a contagem de público-alvo antes da ativação para evitar o envio insuficiente ou excessivo.

>[!ENDSHADEBOX]


## Isso apoia a tomada de decisões? {#decisioning}

Atualmente, o decisioning não usa dados relacionais de campanhas orquestradas.

## Como funciona a implantação entre ambientes? {#deployment}

Objetos criados em campanhas orquestradas (por exemplo, públicos, fluxos de trabalho) são vinculados à sandbox em que são criados. Os workflows padrão de empacotamento e implantação em ambientes (desenvolvimento, preparo, produção) não estão disponíveis no momento para campanhas orquestradas.

>[!BEGINSHADEBOX]

**Práticas recomendadas**

* Mantenha **sandboxes separadas** para experimentação, controle de qualidade e produção.
* Documente as configurações completamente para permitir a replicação manual, se necessário.
* Alinhe-se às equipes de governança para reduzir a variação de configuração entre ambientes.

>[!ENDSHADEBOX]

## Existem práticas recomendadas para executar campanhas em escala? {#scale}

Sim, siga as práticas recomendadas abaixo:

* **Planeje campanhas em torno de calendários comerciais** (lançamentos de produtos, picos sazonais) para alinhar volume e recursos.
* Use **pré-visualizações de público-alvo** antes de enviar para confirmar o tamanho esperado e evitar surpresas.
* Sempre que possível, **enviar horários alternados** para evitar a sobrecarga dos sistemas downstream (por exemplo, call centers, sites).
* Estabeleça uma **rotina de monitoramento** — rastreie os logs de entrega, as taxas de erro e as opções de não participação após cada envio.
* Execute a **análise pós-campanha** no Customer Journey Analytics para refinar o direcionamento e a orquestração para o próximo ciclo.



>[!MORELIKETHIS]
>
>* [Medidas de proteção e limitações para campanhas orquestradas](../orchestrated/guardrails.md)
>* [Introdução a esquemas e conjuntos de dados em campanhas orquestradas](../orchestrated/gs-schemas.md)
>* [Crie sua primeira campanha orquestrada](../orchestrated/gs-campaign-creation.md)
>* [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
