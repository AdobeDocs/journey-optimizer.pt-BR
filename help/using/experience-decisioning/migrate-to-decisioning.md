---
title: Benefícios da migração para o Decisioning
description: Saiba mais sobre os benefícios de migrar da Gestão de decisões para o Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: d336684656c75af682a72b0acab071df15a79004
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 2%

---

# Benefícios da migração para o Decisioning {#migrate-to-decisioning}

## O que é a Decisão? {#what-is-decisioning}

O Journey Optimizer Decisioning é uma expansão da funcionalidade de decisão que estabelece a base para a tomada de decisões em outros objetos (como jornadas) no futuro. Esse novo recurso unifica os principais conceitos do fluxo de trabalho para criação e gerenciamento simplificados, introduz a experimentação na tomada de decisões e transforma itens de decisão em uma abordagem baseada em esquema para a renderização dinâmica de itens.

A estrutura de decisão e o conjunto de recursos de próxima geração no Adobe Journey Optimizer permitem que as marcas usem dados, inteligência e o contexto disponíveis de um cliente para determinar a melhor experiência para cada cliente para otimizar o valor comercial. [Saiba mais](gs-experience-decisioning.md)

## Por que migrar para o Decisioning? {#why-migrate}

A Decisão oferece recursos e benefícios significativos em relação à estrutura herdada de Gestão de decisões:

### Recursos de IA e aprendizado de máquina

* **Métricas personalizadas**: capacidade de usar métricas de otimização personalizadas para modelos de IA. Isso proporciona interoperabilidade de relatórios com o [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview){target="_blank"}, padroniza os relatórios entre ambas as plataformas e melhora a consistência e confiabilidade dos dados. A integração perfeita fornece uma visualização mais clara das métricas de desempenho e adiciona novos recursos, como criar métricas simples, publicar públicos, fazer perguntas ad hoc usando o Insight Builder e agendar relatórios.

* **Medição de aumento**: capacidade de visualizar exploração vs. explorar o tráfego em modelos de IA. Isso permite que profissionais de marketing e cientistas de dados quantifiquem como a exploração de IA melhora o desempenho do modelo a longo prazo e a capacidade de descoberta de novas ofertas vencedoras. A transparência na alocação de tráfego cria confiança nas decisões de IA e capacita as equipes a otimizar tanto o aprendizado quanto o desempenho ao longo do tempo. [Saiba mais](ranking/auto-optimization-model.md#lift)

* **Construtor de fórmulas de IA**: capacidade de aplicar saídas de pontuação do modelo de IA aos recursos de fórmula existentes. Isso permite que os profissionais de marketing combinem saídas de IA perfeitamente com regras e pesos determinísticos para estratégias de otimização mais aprimoradas, aumentando o controle e a flexibilidade e ainda aproveitando a inteligência de aprendizado de máquina. [Saiba mais](ranking/ranking-formulas.md)

### Experimentação

Capacidade de experimentar ofertas, aspectos de uma determinada oferta e/ou métodos de classificação. Isso permite que os profissionais de marketing executem experimentos controlados sobre lógica criativa, de qualificação e de classificação para identificar variantes de alto desempenho, acelerando os ciclos de aprendizado e impulsionando a otimização contínua do sistema de decisão.

### Relatórios aprimorados

Painel que documenta o desempenho dos itens de decisão e as estratégias de seleção em relação aos principais elementos do envolvimento com a funnel. Um painel de decisão intuitivo e pronto para uso mostra rapidamente o valor do desempenho da campanha e da jornada para os principais KPIs na oferta e entrega de conteúdo, exibição e engajamento de cliques, taxas de uso de fallback e elevação de modelos de classificação de aprendizado de máquina e IA. [Saiba mais](cja-reporting.md)

### Eficiência operacional

* **Cópia da sandbox**: capacidade de copiar objetos entre sandboxes (por exemplo, Dev para Prod). Isso simplifica a implantação e os fluxos de trabalho de teste, permitindo a migração perfeita de lógica de decisão, ofertas e objetos de configuração entre ambientes, reduzindo o tempo de configuração e minimizando o erro humano. [Saiba mais](../configuration/copy-objects-to-sandbox.md)

* **Gerenciamento de catálogo de itens baseado em esquema**: capacidade de definir e gerenciar itens de decisão diretamente para conjuntos de dados vinculados a esquema, permitindo atualizações dinâmicas e governança simplificada. Isso simplifica o gerenciamento de catálogos, sincronizando itens de decisão com fontes de dados subjacentes, garantindo a precisão do conteúdo, permitindo atualizações mais rápidas e oferecendo suporte ao controle em escala. [Saiba mais](items.md)

* **Decisão independente de localização**: capacidade de tornar a lógica de decisão reutilizável em disposições/localizações, desvinculando a seleção de decisão da entrega. Isso promove a reutilização e a eficiência, permitindo que um único modelo de decisão potencialize vários posicionamentos ou superfícies (por exemplo, Web, aplicativo, email), centralizando a lógica e acelerando os esforços de personalização entre canais. [Saiba mais](placements.md)

* **Fragmentos de conteúdo reutilizáveis**: capacidade de definir blocos de conteúdo JSON ou HTML (por exemplo, títulos, cabeçalhos, rodapés, CTAs) uma vez e referenciá-los em vários objetos de oferta. Isso simplifica a criação e o controle de conteúdo, permitindo que os componentes compartilhados sejam gerenciados centralmente e atualizados automaticamente em todas as ofertas. [Saiba mais](../content-management/fragments.md)

### Futuros recursos

* **Decisão de canal**: capacidade de usar a lógica de decisão para determinar o melhor canal para participação (por exemplo, email vs. push vs. web), em vez de apenas a melhor oferta em um único canal. Isso melhora a experiência do cliente ao otimizar onde uma mensagem é entregue, não apenas o que é entregue.

* **Otimização da mensagem**: capacidade de usar IA ou abordagens baseadas em regras para otimizar o conteúdo da mensagem para cada perfil, melhorando os resultados da participação e da conversão. Isso permite que os profissionais de marketing personalizem o tom, a imagem e o layout dinamicamente com base nos atributos do público-alvo e nos dados de desempenho.

* **Otimização do caminho de Jornada**: capacidade de determinar qual caminho de jornada um perfil deve seguir, com base em resultados experimentais, contexto em tempo real, regras e/ou propensão a converter. Isso permite que as equipes roteiem perfis de forma inteligente por meio da ramificação de jornada ideal, garantindo a cadência e o conteúdo corretos para cada usuário.

* **Decisão de Jornada**: capacidade de arbitrar entre várias jornadas quando um perfil se qualifica para mais de uma, garantindo que a jornada mais valiosa ou relevante seja selecionada. Isso evita conflitos de mensagens e mensagens excessivas ao classificar e selecionar a jornada de maior prioridade para cada perfil.

### Recursos adicionais

* **Imposição de política**: capacitação do usuário empresarial para usar recursos como [Rotulagem e Imposição de Uso de Dados (DULE)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/labels/overview){target="_blank"} e [Consentimento](../action/consent.md) na Decisão, habilitando a proteção de blindagem de privacidade no fluxo de trabalho de decisão. Isso garante que as decisões respeitem automaticamente as políticas de uso de dados e as preferências de consentimento do cliente.

* **Suporte a canal de mensagens nativo**: mensagens e decisões integradas em uma única estrutura em vários canais ([Experiência baseada em código](../code-based/get-started-code-based.md) e [Email](../email/get-started-email.md) disponíveis no momento, outros canais disponíveis no 1º semestre de 2026). O suporte intuitivo à interface permite que os usuários insiram componentes de decisão diretamente nos fluxos de trabalho de criação de mensagens.

* **Pesquisa de conjunto de dados do Experience Platform**: capacidade de carregar e referenciar [conjuntos de dados do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"} diretamente nas regras de seleção de oferta, classificação e conteúdo de oferta personalizado. Isso expande a flexibilidade para personalização e direcionamento ao permitir que a lógica de decisão use fontes de dados externas dinâmicas. [Saiba mais](../data/lookup-aep-data.md)

* **Escalabilidade e desempenho**: aprimoramento da arquitetura que move a computação de decisão do hub para a borda, reduzindo significativamente a latência e melhorando a taxa de transferência para casos de uso de alto tráfego.

## Exemplo de casos de uso {#use-cases}

| Caso de uso | Gestão de decisões | Tomada de decisão |
|----------|---------------------|-------------|
| **Estratégia de vários posicionamentos** | Lógica de decisão vinculada a um posicionamento específico (por exemplo, local da Web ou de email) | Uma única estratégia capacita tanto a página inicial quanto o aplicativo móvel |
| **Atributos de oferta consistentes** | Cada oferta gerencia seus próprios atributos manualmente; sem consistência no nível do esquema | Um profissional de marketing define &quot;discountType&quot; e &quot;offerValue&quot; uma vez; cada oferta herda esses campos automaticamente |
| **Classificação de IA dinâmica** | As classificações dependem exclusivamente da saída do modelo ou de regras estáticas | Um profissional de marketing pode ajustar a ponderação (por exemplo, 60% de pontuação de conversão de IA + 40% de margem de lucro) para equilibrar as metas de receita e engajamento |
| **Estratégias de teste A/B** | Nenhum suporte para experimentação integrado | Uma equipe pode testar A/B se a &quot;IA + regras de negócios&quot; supera o desempenho da &quot;classificação baseada em prioridade&quot; |
| **Métricas personalizadas de IA** | Otimiza apenas em relação à propensão a cliques; sem visibilidade na exploração ou no aumento do modelo | A retailer treina um modelo de &quot;probabilidade de compra&quot; e os monitores passam por produtos novos comparados aos conhecidos |
| **Reusabilidade do conteúdo** | Cada oferta armazena conteúdo completo de forma independente | A atualização de um cabeçalho ou CTA se propaga automaticamente para centenas de ofertas |
| **Criação integrada** | A decisão e as mensagens são disponibilizadas em estruturas separadas com integração limitada | Um profissional de marketing insere ofertas personalizadas em um email sem sair do editor de mensagens |
| **Conformidade com a privacidade** | Requer coordenação manual com as equipes de engenharia e de dados para aplicação | Um profissional de marketing cria uma regra de oferta sabendo que as preferências de consentimento excluem automaticamente determinados perfis |
| **Estoque em tempo real** | Dados estáticos; flexibilidade limitada para usar conjuntos de dados externos ou contextuais | Usar um conjunto de dados de inventário de produtos para suprimir ofertas de itens indisponíveis em tempo real |
| **Dimensionar desempenho** | Decisões tomadas no hub com latência mais alta | Personalização em tempo real para milhões de solicitações recebidas com tempo de resposta inferior a 100 ms |

## Ferramentas de migração {#migration-tooling}

Um conjunto abrangente de **APIs de ferramentas de migração** está disponível para migrar entidades de Gestão de decisões para o Decisioning. Essas APIs permitem uma migração perfeita entre sandboxes com recursos automatizados de resolução de dependências e reversão.

As APIs de ferramentas de migração permitem:

* **Analisar dependências** entre sandboxes de origem e destino
* **Migrar em escopos diferentes** - nível de sandbox, oferta ou decisão
* **Migrações de reversão** se forem descobertos problemas

Para obter a documentação completa da API, incluindo autenticação, endpoints, exemplos de solicitação/resposta e fluxos de trabalho passo a passo, consulte [esta página](decisioning-migration-api.md).

## Tópicos relacionados {#related-topics}

* [Introdução ao serviço de decisão](gs-experience-decisioning.md)
* [Medidas de proteção e limitações da decisão](decisioning-guardrails.md)
* [Perguntas frequentes sobre decisão](decisioning-faq.md)

