---
solution: Journey Optimizer
product: journey optimizer
title: Jornadas versus campanhas - escolha a abordagem correta
description: Compare Jornadas, Campanhas de ação, Campanhas acionadas por API e Campanhas orquestradas para escolher a abordagem certa para suas necessidades de marketing no Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: jornada, campanha, orquestrado, comparação, escolher, decisão, fluxo de trabalho, tempo real, lote, orquestração, várias etapas, agendado, acionado por API, orientado por evento
hide: true
hidefromtoc: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
source-git-commit: fc2dc5924f4998d1285dee9c19a0d7e71a1e5722
workflow-type: tm+mt
source-wordcount: '1593'
ht-degree: 3%

---

# Jornadas versus campanhas: escolha a abordagem certa {#journeys-vs-campaigns}

O [!DNL Adobe Journey Optimizer] oferece quatro formas principais de alcançar e envolver seus clientes: **Jornada**, **Campanhas de Ação**, **Campanhas acionadas por API** e **Campanhas Orquestradas**. Escolher a correta depende de você precisar de orquestração em tempo real do :1, difusões agendadas, mensagens orientadas por eventos ou fluxos de trabalho em lote complexos.

Este guia ajuda você a escolher com base no estilo de execução, nas necessidades de dados e no caso de uso, com uma comparação rápida, uma árvore de decisão e exemplos concretos.

## Visão geral da comparação rápida {#quick-overview}

| Abordagem | Melhor para | Estilo de execução |
|----------|----------|-----------------|
| **Jornadas** | Experiências do cliente em tempo real em várias etapas com lógica condicional | 1 orquestração :1 - cada perfil em seu próprio ritmo |
| **Campanhas de ação** | Transmissões programadas ou recorrentes para públicos-alvo | Execução em lote - público-alvo processado junto no momento do envio |
| **Campanhas acionadas por API** | Mensagens transacionais ou orientadas por eventos de sistemas externos | Execução sob demanda - acionada pela chamada à API com carga |
| **Campanhas orquestradas** | Fluxos de trabalho em lote complexos com segmentação de várias entidades | Tela em lote - todos os perfis processados juntos |

>[!TIP]
>
>**Princípio básico rápido:** Precisa que cada cliente se mova em seu próprio ritmo com lógica em tempo real? Use **Jornadas**. Enviar uma mensagem para um público-alvo de acordo com o cronograma? Use **Campanhas de Ação**. Acionamento de um sistema externo via API? Use **Campanhas acionadas por API**. Precisa de dados de várias entidades, contagens exatas ou uma tela de lote? Use **Campanhas Orquestradas**.

## Comparação detalhada {#detailed-comparison}

Use esta tabela abrangente para entender as principais diferenças:

| Recurso | Jornadas | Campanhas de ações | Campanhas acionadas por API | Campanhas orquestradas |
|---------|----------|------------------|------------------------|----------------------|
| **Finalidade principal** | Orquestração de várias etapas do :1 com contexto de cliente em tempo real | Entrega de mensagem única ou recorrente para públicos | Mensagens transacionais ou orientadas por eventos iniciadas por sistemas externos | Campanhas em lote de várias etapas com fluxos de trabalho de segmentação complexos |
| **Tipo de tela** | Tela 1:1 - cada perfil viaja em seu próprio ritmo | Sem tela - execução de ação única | Sem tela - execução de ação única | Tela em lote - todos os perfis processados juntos |
| **Fluxo de execução** | Ações sequenciais, o perfil mantém o estado em toda a jornada | Execução simultânea para todo o público | Execução imediata por chamada de API | Fluxo de trabalho em lote de várias etapas com atividades e transições |
| **Mecanismo de entrada** | Eventos, públicos, qualificações, eventos comerciais | Ativação e programação manuais | Chamada de API do sistema externo | Execução agendada do fluxo de trabalho em lote |
| **Modelo de dados** | Perfil em tempo real + dados do evento | Dados de perfil de públicos da Experience Platform | Dados de carga da API com pesquisa de perfil opcional | Dados relacionais de várias entidades (perfis, produtos, lojas, reservas) |
| **Segmentação** | Públicos-alvo pré-criados + condições em tempo real | Públicos-alvo pré-criados da Experience Platform | Direcionamento orientado por carga (sem público agendado) | Públicos sob demanda criados na tela com contagens exatas |
| **Processamento de perfil** | Individual, em tempo real (conforme os eventos ocorrem) | Em lote, tudo de uma vez | Por chamada de API, orientada por carga | Em lote, tudo junto com suporte a várias entidades |
| **Personalização** | Dados contextuais em tempo real + atributos de perfil | Atributos do perfil | Dados de carga + atributos opcionais do perfil | Dados de várias entidades para direcionamento de precisão |
| **Complexidade** | Várias etapas com ramificação, tempos de espera e condições | Única ação ou fluxo de trabalho simples | Única ação com mapeamento de carga | Fluxos de trabalho em lote de várias etapas com segmentação, enriquecimento, divisões |
| **Recomendado para** | Jornadas de ciclo de vida do cliente, integração, abandono de carrinho | Campanhas promocionais, boletins informativos, anúncios | Confirmações de pedidos, alertas de envio, redefinições de senha | Campanhas sazonais complexas, promoções em várias etapas, lançamentos de produtos |
| **Horário** | Contínuo, sempre ativo depois de publicado | Datas de início/término programadas | Sob demanda, orientado por eventos por meio da API | Execução em lote agendada |
| **Gerenciamento de estado** | Mantém o estado do cliente para ações em tempo real | Execução sem estado | Execução sem estado por chamada | Processamento em lote com tabelas de trabalho |
| **Usar quando** | Vários pontos de contato necessários com a lógica de decisão em tempo real | Mensagem simples para um público em um horário específico | O sistema externo precisa acionar uma mensagem imediatamente | Necessidade de segmentação complexa, dados de várias entidades ou contagens exatas de pré-envio |
| **Recursos exclusivos** | Reações em tempo real, atividades de espera e ritmo baseado em perfil | Agendamento, direcionamento de público, controle de taxa | Mapeamento de carga da API, acionamento de sistema para sistema | Conjuntos de dados relacionais, segmentação de várias entidades, contagens exatas, envio de vários níveis |

## Guia de decisão {#decision-guide}

Siga esta árvore decisória para escolher a abordagem correta. Muitas marcas usam mais de um tipo; escolha o melhor ajuste para cada caso de uso.

### Etapa 1: qual é o seu requisito de execução?

**Respostas individuais em tempo real ao comportamento do cliente?**
→ **Usar Jornadas**
* Os perfis precisam se mover em seu próprio ritmo
* Lógica condicional baseada em comportamento
* O contexto em tempo real é essencial

**Entrega de mensagem simples para um público-alvo em um horário agendado?**
→ **Usar Campanhas de Ação**
* Todos os perfis recebem mensagens simultaneamente
* Envios agendados ou recorrentes
* Não é necessária uma lógica complexa de várias etapas

**Mensagem imediata acionada por um sistema externo?**
→ **Usar campanhas acionadas por API**
* Acionado sob demanda por meio de chamada de API
* Personalização orientada por carga
* Não é necessária uma lógica complexa de várias etapas

**Fluxo de trabalho em lotes complexo com segmentação avançada?**
→ **Usar Campanhas Orquestradas**
* Necessidade de dados de várias entidades (produtos, lojas, reservas)
* Exigir contagens exatas de pré-envio
* Processamento em lote de várias etapas com divisões e enriquecimento

### Etapa 2: validar sua escolha

| Sua necessidade | Método recomendado | Por que |
|-----------|---------------------|-----|
| Dê as boas-vindas a novos clientes com integração em várias etapas | Jornadas | Entrada em tempo real, vários pontos de contato, caminhos condicionais |
| Enviar informativo mensal aos assinantes | Campanhas de ações | Mensagem agendada simples para o público |
| Abandono do carrinho com sequência de lembretes | Jornadas | Acionador em tempo real, tempos de espera e acompanhamento condicional |
| Anúncio promocional para todos os clientes | Campanhas de ações | Mensagem única, entrega imediata |
| Reengajamento de usuários inativos com base no comportamento | Jornadas | Acionado pela qualificação de público-alvo, caminho personalizado |
| Venda rápida acionada por evento comercial | Jornadas (Evento Comercial) | Acionador em tempo real que afeta vários clientes |
| Promoção sazonal com integração ao catálogo de produtos | Campanhas orquestradas | Dados de várias entidades, segmentação complexa, contagem exata |
| Mensagem transacional acionada por API | Campanhas acionadas por API | Acionador do sistema externo, entrega imediata |
| Envio de vários níveis por reserva | Campanhas orquestradas | Relacionamentos de várias entidades, uma mensagem por reserva |

## Principais distinções explicadas {#key-distinctions}

### Jornada: 1:1 Orquestração em tempo real

**O que o torna exclusivo:**
* Cada perfil mantém um estado e um contexto individuais
* Os perfis entram e avançam em seu próprio ritmo
* Tomada de decisões em tempo real com base em comportamentos e eventos
* As atividades de espera criam um tempo personalizado
* A ramificação condicional cria caminhos exclusivos por perfil

**Exemplo de fluxo:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Cada cliente tem sua própria linha do tempo de jornada com base em suas ações.

[Saiba mais sobre Jornadas](../building-journeys/journey.md)

### Campanhas: entrega em lote simples ou acionada

**O que o torna exclusivo:**
* Todos os perfis processados de forma idêntica e simultaneamente
* Execução sem estado - nenhum contexto mantido
* Agendamento simples ou acionamento de API
* Ideal para comunicações por transmissão

**Exemplo de fluxo:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Todos recebem a mesma mensagem ao mesmo tempo.

**Tipos:**
* **Campanhas de ação**: entrega agendada para públicos-alvo (única ou recorrente)
* **Campanhas acionadas por API**: entrega sob demanda acionada por uma chamada de API com dados de carga

[Saiba mais sobre Campanhas](../campaigns/get-started-with-campaigns.md)

### Campanhas orquestradas: workflows da tela em lote

**O que o torna exclusivo:**
* Tela em lote com atividades e transições (semelhante à tela do jornada, mas orientada a lote)
* Suporte a dados relacionais de várias entidades (perfis + produtos + lojas + reservas)
* Criação de público-alvo sob demanda na tela
* Contagens exatas antes do envio (visibilidade pré-envio)
* Envio em vários níveis (uma mensagem por entidade, por exemplo, por reserva)
* Todos os perfis processados juntos em lote

**Exemplo de fluxo:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combina a complexidade do fluxo de trabalho com a execução da campanha em lote.

[Saiba mais sobre Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

## Exemplos de caso de uso {#use-cases}

### Jornada casos de uso

* **Recuperação de abandono do carrinho**: acionado pelo evento de adição do carrinho, aguarde o check-out e envie lembretes se não houver compra
* **Integração de clientes**: série de boas-vindas em várias etapas com conteúdo personalizado com base nos dados do perfil
* **Atualização da camada de fidelidade**: acionada quando o cliente atinge uma nova camada, envie parabéns e benefícios
* **Campanhas de aniversário**: entrada com base na data de nascimento, ofertas personalizadas
* **Reengajamento**: acionado por qualificação de público-alvo (inatividade), alcance progressivo

### Casos de uso do Campaign (acionados por ação e API)

**Campanhas de Ação:**
* **Informativos mensais**: entrega em lote agendada para o segmento do assinante
* **Anúncios promocionais**: ofertas com diferenciação de tempo para direcionar públicos-alvo
* **Lançamentos de produto**: anúncio coordenado para todos os clientes
* **Saudações da estação**: mensagens de feriado em datas específicas

**Campanhas acionadas por API:**
* **Confirmações de pedidos**: acionadas pelo sistema de comércio eletrônico após a compra
* **Notificações de remessa**: acionadas pelo sistema logístico
* **Alertas de conta**: acionados pelo sistema de detecção de fraudes
* **Redefinições de senha**: acionado pela ação do usuário no aplicativo

### Casos de uso do Campaign orquestrados

* **Promoção sazonal com integração de catálogo**: consultar catálogo de produtos, identificar clientes qualificados, segmentar por preferências, enviar recomendações personalizadas de produto
* **Campanhas específicas da loja**: clientes-alvo próximos a locais de loja específicos com dados de inventário da loja
* **Comunicações de várias reservas**: envie uma mensagem por reserva (reservas de hotel, reservas de voos)
* **Orquestração de segmentos complexos**: crie públicos passo a passo com enriquecimento de várias fontes de dados
* **Validação de pré-envio**: obtenha contagens exatas de destinatários antes de iniciar campanhas importantes

## Disponibilidade de recursos {#feature-availability}

### Canais

| Canal | Jornadas | Campanhas de ações | Campanhas acionadas por API | Campanhas orquestradas |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Email | ✅ | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| No aplicativo | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Baseado em código | ✅ | ✅ | ❌ | ❌ |
| Cartões de conteúdo | ✅ | ✅ | ❌ | ❌ |
| Correspondência direta | ✅ | ✅ | ❌ | ✅ |

### Recursos avançados

| Recurso | Jornadas | Campanhas de ações | Campanhas acionadas por API | Campanhas orquestradas |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Fluxos de trabalho de várias etapas | ✅ | ❌ | ❌ | ✅ |
| Acionadores em tempo real | ✅ | ❌ | ✅ | ❌ |
| Atividades de espera | ✅ | ❌ | ❌ | ✅ |
| Ramificação condicional | ✅ | ❌ | ❌ | ✅ |
| Execução programada | ✅ | ✅ | ✅ | ✅ |
| Acionamento da API | ❌ | ❌ | ✅ | ❌ |
| Dados de várias entidades | ❌ | ❌ | ❌ | ✅ |
| Contagens exatas de pré-envio | ❌ | ❌ | ❌ | ✅ |
| Segmentação sob demanda | ❌ | ❌ | ❌ | ✅ |
| Otimização de hora de envio | ✅ | ✅ | ✅ | ✅ |
| Teste AB | ✅ | ✅ | ❌ | ❌ |
| Fluxos de trabalho de aprovação | ✅ | ✅ | ✅ | ❌ |

## Perguntas comuns {#common-questions}

+++ É possível combinar jornadas e campanhas em minha estratégia de marketing?

Sim. Muitas organizações usam todas as quatro abordagens para diferentes cenários:

* **Jornadas** para envolvimento comportamental e em tempo real
* **Campanhas de ação** para comunicações de difusão agendadas
* **Campanhas acionadas por API** para mensagens transacionais
* **Campanhas orquestradas** para campanhas em lote complexas e com muitos dados

Use a ferramenta certa para cada caso de uso, em vez de forçar uma abordagem para tudo.

+++

+++ Posso converter uma campanha em uma jornada ou vice-versa?

Não, você deve recriar a experiência no formato apropriado. No entanto, você pode reutilizar conteúdo, públicos e conceitos lógicos.

+++

+++ Qual abordagem é mais fácil de criar?

As Campanhas de ação normalmente são as mais simples (mensagem única para o público), seguidas por Campanhas acionadas por API, Jornadas (mais complexas com lógica de várias etapas) e Campanhas orquestradas (mais complexas devido ao fluxo de trabalho da tela e recursos de várias entidades).

+++

+++ Qual dimensionamento é melhor para públicos-alvo grandes?

Todos os quatro podem ser bem dimensionados; a escolha certa depende do seu padrão:

* As **Jornadas de Leitura de Público** e as **Campanhas de Ação** estão otimizadas para públicos de lote grandes (uma mensagem ou fluxo para vários perfis de uma só vez).
* As **Campanhas orquestradas** são excelentes em segmentações complexas com grandes conjuntos de dados e dados de várias entidades.
* **O Jornada** unitário (baseado em eventos) processa perfis individualmente à medida que os eventos ocorrem, portanto, a escala depende do volume e da taxa de transferência do evento.

+++

+++ Posso usar o mesmo público-alvo em jornadas e campanhas?

Sim. Os públicos-alvo criados no [!DNL Adobe Experience Platform] podem ser usados em Jornadas, Campanhas de Ação e Campanhas Orquestradas (em que a lógica do público-alvo também pode ser criada sob demanda na tela). As Campanhas acionadas por API são orientadas por carga e não usam públicos-alvo pré-criados da mesma maneira.

+++

## Próximas etapas {#next-steps}

Pronto(a) para começar a criar? Explore a documentação detalhada da abordagem escolhida:

* **[Introdução ao Jornada](../building-journeys/journey.md)** - Tipos de Jornada, designer e fluxo de trabalho
* **[Introdução às Campanhas](../campaigns/get-started-with-campaigns.md)** - Campanhas acionadas por ação e API
* **[Introdução às Campanhas Orquestradas](../orchestrated/gs-orchestrated-campaigns.md)** - Fluxos de trabalho de tela de lote

>[!MORELIKETHIS]
>
>* [comparação de tipos de Jornada](../building-journeys/journey.md#journey-types-comparison)
>* [Comparação de tipos de campanha](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Perguntas frequentes sobre o Jornada](../building-journeys/journey-faq.md)
>* [Perguntas frequentes sobre Campanhas Orquestradas](../orchestrated/orchestrated-campaigns-faq.md)
