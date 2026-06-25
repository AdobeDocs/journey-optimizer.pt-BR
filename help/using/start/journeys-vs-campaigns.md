---
solution: Journey Optimizer
product: journey optimizer
title: Jornadas versus campanhas - escolha a abordagem correta
description: Compare Jornadas, campanhas de ação e campanhas acionadas por API para escolher a abordagem certa para suas necessidades de marketing no Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: jornada, campanha, comparação, escolher, decisão, fluxo de trabalho, tempo real, lote, orquestração, várias etapas, agendado, acionado por API, orientado por evento
hide: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: addf009e-030a-4310-8534-776a3e62ed48
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6f35d9b951850220382e3662502b9e1d7ad6b990
workflow-type: tm+mt
source-wordcount: 1660
ht-degree: 4%

---

# Jornadas versus campanhas: escolha a abordagem certa {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Nesta página:** compare as jornadas com campanhas acionadas por ação e API para poder escolher a abordagem certa para cada caso de uso de marketing no Adobe Journey Optimizer. Para campanhas orquestradas, consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] oferece duas formas principais de alcançar e envolver seus clientes: **Jornadas** e **Campanhas**. As jornadas foram projetadas para a orquestração em tempo real e em várias etapas, orientada pelo comportamento do cliente, enquanto as campanhas são mais adequadas para transmissões únicas ou programadas para um público definido. Depois de decidir sobre uma campanha, você pode escolher o tipo de campanha que melhor se adapta ao seu caso de uso.

Este guia ajuda você a escolher entre Jornadas, campanhas de ação e campanhas acionadas por API com base no estilo de execução, nas necessidades de dados e no caso de uso, com uma comparação rápida, uma árvore de decisão e exemplos concretos.

>[!NOTE]
>
>**Campanhas orquestradas** têm características de arquitetura distintas (execução em lote no hub, dados relacionais de várias entidades) que exigem orientação dedicada. Não são incluídas nos quadros comparativos abaixo para evitar uma simplificação excessiva. [Saiba mais sobre Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

## Visão geral da comparação rápida {#quick-overview}

| Abordagem | Melhor para | Estilo de execução |
|----------|----------|-----------------|
| **Jornadas** | Experiências do cliente em tempo real em várias etapas com lógica condicional | 1 orquestração :1 - cada perfil em seu próprio ritmo |
| **Campanhas de ação** | Transmissões programadas ou recorrentes para públicos-alvo | Execução em lote - público-alvo processado junto no momento do envio |
| **Campanhas acionadas por API** | Mensagens transacionais ou orientadas por eventos de sistemas externos | Execução sob demanda - acionada pela chamada à API com carga |

>[!TIP]
>
>**Princípio básico rápido:** Precisa que cada cliente se mova em seu próprio ritmo com lógica em tempo real? Use **Jornadas**. Enviar uma mensagem para um público-alvo de acordo com o cronograma? Use **Campanhas de ação**. Acionando uma única mensagem de um sistema externo por meio da API? Use **campanhas acionadas por API** — ou uma **jornada de eventos unitária** se precisar de orquestração em várias etapas após o evento enviado por API.

## Comparação detalhada {#detailed-comparison}

Use esta tabela abrangente para entender as principais diferenças:

| Recurso | Jornadas | Campanhas de ação | Campanhas acionadas por API |
|---------|----------|------------------|------------------------|
| **Finalidade principal** | Orquestração de várias etapas do :1 com contexto de cliente em tempo real | Entrega de mensagem única ou recorrente para públicos | Mensagens transacionais ou orientadas por eventos iniciadas por sistemas externos |
| **Tipo de tela** | Tela 1:1 - cada perfil viaja em seu próprio ritmo | Sem tela - execução de ação única | Sem tela - execução de ação única |
| **Fluxo de execução** | Ações sequenciais, o perfil mantém o estado em toda a jornada | Execução simultânea para todo o público | Execução imediata por chamada de API |
| **Mecanismo de entrada** | Eventos, públicos, qualificações, eventos comerciais | Ativação e programação manuais | Chamada de API do sistema externo |
| **Modelo de dados** | Perfil em tempo real + dados do evento | Dados de perfil de públicos da Experience Platform | Dados de carga da API com pesquisa de perfil opcional |
| **Segmentação** | Públicos-alvo pré-criados + condições em tempo real | Públicos-alvo pré-criados da Experience Platform | Direcionamento orientado por carga (sem público agendado) |
| **Processamento de perfil** | Individual, em tempo real (conforme os eventos ocorrem) | Em lote, tudo de uma vez | Por chamada de API, orientada por carga |
| **Personalização** | Dados contextuais em tempo real + atributos de perfil | Atributos do perfil | Dados de carga + atributos opcionais do perfil |
| **Complexidade** | Várias etapas com ramificação, tempos de espera e condições | Única ação ou fluxo de trabalho simples | Única ação com mapeamento de carga |
| **Recomendado para** | Jornadas de ciclo de vida do cliente, integração, abandono de carrinho | Campanhas promocionais, boletins informativos, anúncios | Confirmações de pedidos, alertas de envio, redefinições de senha |
| **Horário** | Contínuo, sempre ativo depois de publicado | Datas de início/término programadas | Sob demanda, orientado por eventos por meio da API |
| **Gerenciamento de estado** | Mantém o estado do cliente para ações em tempo real | Execução sem estado | Execução sem estado por chamada |
| **Usar quando** | Vários pontos de contato necessários com a lógica de decisão em tempo real | Mensagem simples para um público em um horário específico | O sistema externo precisa acionar uma mensagem imediatamente |
| **Recursos exclusivos** | Reações em tempo real, atividades de espera e ritmo baseado em perfil | Agendamento, direcionamento de público, controle de taxa | Mapeamento de carga da API, acionamento de sistema para sistema |

## Guia de decisão {#decision-guide}

Siga esta árvore decisória para escolher a abordagem correta. Muitas marcas usam mais de um tipo; escolha o melhor ajuste para cada caso de uso.

### Etapa 1: qual é o seu requisito de execução?

**Respostas individuais em tempo real ao comportamento do cliente?**
→ **Usar o Jornada**
* Os perfis precisam se mover em seu próprio ritmo
* Lógica condicional baseada em comportamento
* O contexto em tempo real é essencial

**Entrega de mensagem simples para um público-alvo em um horário agendado?**
→ **Usar campanhas de ação**
* Todos os perfis recebem mensagens simultaneamente
* Envios agendados ou recorrentes
* Não é necessária uma lógica complexa de várias etapas

**Mensagem imediata disparada por um sistema externo?**
→ **Usar campanhas acionadas por API** (mensagem única) **ou uma jornada de eventos Unitária** (orquestração de várias etapas)
* Acionado sob demanda por meio de chamada de API — as campanhas fornecem uma mensagem; as jornadas unitárias assimilam o evento por meio de [assimilação do Experience Platform](../event/additional-steps-to-send-events-to-journey.md) e executam um fluxo de jornada completo
* Personalização orientada por carga
* Escolher campanhas quando nenhuma lógica de várias etapas for necessária

**Fluxo de trabalho de lote complexo com segmentação avançada, dados de várias entidades ou contagens exatas de pré-envio?**
→ **Use campanhas orquestradas** — consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) para obter orientação detalhada.

### Etapa 2: validar sua escolha

| Sua necessidade | Método recomendado | Por que |
|-----------|---------------------|-----|
| Dê as boas-vindas a novos clientes com integração em várias etapas | Jornadas | Entrada em tempo real, vários pontos de contato, caminhos condicionais |
| Enviar informativo mensal aos assinantes | Campanhas de ação | Mensagem agendada simples para o público |
| Abandono do carrinho com sequência de lembretes | Jornadas | Acionador em tempo real, tempos de espera e acompanhamento condicional |
| Anúncio promocional para todos os clientes | Campanhas de ação | Mensagem única, entrega imediata |
| Reengajamento de usuários inativos com base no comportamento | Jornadas | Acionado pela qualificação de público-alvo, caminho personalizado |
| Venda rápida acionada por evento comercial | Jornadas (Evento Comercial) | Acionador em tempo real que afeta vários clientes |
| Mensagem transacional acionada por API (envio único) | Campanhas acionadas por API | Acionador do sistema externo, entrega imediata |
| Fluxo de várias etapas acionado por API | Jornadas (evento unitário) | O sistema externo envia evento unitário por meio da API; o jornada coordena as etapas de acompanhamento |
| Fluxo de trabalho de lote complexo com dados de várias entidades | Campanhas orquestradas | Consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |

## Principais distinções explicadas {#key-distinctions}

### Jornada: 1:1 Orquestração em tempo real

**O que o torna exclusivo:**
* Cada perfil mantém um estado e um contexto individuais
* Os perfis entram e avançam em seu próprio ritmo
* Tomada de decisões em tempo real com base em comportamentos e eventos
* As atividades de espera criam um tempo personalizado
* A ramificação condicional cria caminhos exclusivos por perfil
* Escuta ativa integrada — a inação por um período definido também pode acionar a próxima etapa, não apenas eventos explícitos. [Saiba mais sobre atividades de espera](../building-journeys/wait-activity.md)
* Limite de frequência — controla com que frequência um cliente pode inserir ou receber mensagens de uma jornada. [Saiba mais sobre o limite de jornada](../conflict-prioritization/journey-capping.md)
* Divisão de público-alvo por porcentagem: divida os perfis em grupos aleatórios baseados em porcentagem para executar experimentos A/B em caminhos de jornada. [Saiba mais sobre a divisão de porcentagem](../building-journeys/condition-activity.md)
* Modo de teste — valide a lógica de jornada e o delivery de mensagens com perfis de teste antes de publicar em tempo real. [Saiba mais sobre o modo de teste](../building-journeys/testing-the-journey.md)

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

## Exemplos de caso de uso {#use-cases}

### Jornada casos de uso

* **Recuperação de abandono do carrinho**: acionado pelo evento de adição do carrinho, aguarde o check-out e envie lembretes se não houver compra
* **Integração de clientes**: série de boas-vindas em várias etapas com conteúdo personalizado com base nos dados do perfil
* **Atualização da camada de fidelidade**: acionada quando o cliente atinge uma nova camada, envie parabéns e benefícios
* **Campanhas de aniversário**: entrada com base na data de nascimento, ofertas personalizadas
* **Reengajamento**: acionado por qualificação de público-alvo (inatividade), alcance progressivo

### Casos de uso do Campaign (acionados por ação e API)

**Campanhas de ação:**
* **Informativos mensais**: entrega em lote agendada para o segmento do assinante
* **Anúncios promocionais**: ofertas com diferenciação de tempo para direcionar públicos-alvo
* **Lançamentos de produto**: anúncio coordenado para todos os clientes
* **Saudações da estação**: mensagens de feriado em datas específicas

**Campanhas acionadas por API:**
* **Confirmações de pedidos**: acionadas pelo sistema de comércio eletrônico após a compra
* **Notificações de remessa**: acionadas pelo sistema logístico
* **Alertas de conta**: acionados pelo sistema de detecção de fraudes
* **Redefinições de senha**: acionado pela ação do usuário no aplicativo

## Disponibilidade de recursos {#feature-availability}

### Canais

| Canal | Jornadas | Campanhas de ação | Campanhas acionadas por API |
|---------|:--------:|:----------------:|:-----------------------:|
| Email | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ |
| No aplicativo | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Baseado em código | ✅ | ✅ | ❌ |
| Cartões de conteúdo | ✅ | ✅ | ❌ |
| Correspondência direta | ✅ | ✅ | ❌ |
| LINE | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ |

>[!NOTE]
>
>Para obter a disponibilidade do canal de campanhas orquestradas, consulte [Campanhas orquestradas — Canais suportados](../orchestrated/gs-orchestrated-campaigns.md).

### Recursos avançados

| Recurso | Jornadas | Campanhas de ação | Campanhas acionadas por API |
|-----------|:--------:|:----------------:|:-----------------------:|
| Fluxos de trabalho de várias etapas | ✅ | ❌ | ❌ |
| Acionadores em tempo real | ✅ | ❌ | ✅ |
| Atividades de espera | ✅ | ❌ | ❌ |
| Ramificação condicional | ✅ | ❌ | ❌ |
| Execução programada | ✅ | ✅ | ✅ |
| Acionamento da API | ✅ (somente evento unitário — evento enviado por API) | ❌ | ✅ |
| Dados de várias entidades | ❌ | ❌ | ❌ |
| Contagens exatas de pré-envio | ❌ | ❌ | ❌ |
| Segmentação sob demanda | ❌ | ❌ | ❌ |
| Otimização de hora de envio | ✅ | ❌ | ❌ |
| Teste AB | ✅ | ✅ | ❌ |
| Fluxos de trabalho de aprovação | ✅ | ✅ | ✅ |

>[!NOTE]
>
>Para obter detalhes sobre recursos de campanhas orquestradas, incluindo experimentos de conteúdo, acionamento de API em lote e segmentação de várias entidades, consulte [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

## Perguntas comuns {#common-questions}

+++ É possível combinar jornadas e campanhas em minha estratégia de marketing?

Sim. Muitas organizações usam todas as abordagens para diferentes cenários:

* **Jornadas** para envolvimento comportamental e em tempo real
* **Campanhas de ação** para comunicações de difusão agendadas
* **Campanhas acionadas por API** para mensagens transacionais
* **Campanhas orquestradas** para campanhas em lote complexas e com muitos dados — consulte [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

Use a ferramenta certa para cada caso de uso, em vez de forçar uma abordagem para tudo.

+++

+++ Posso converter uma campanha em uma jornada ou vice-versa?

Não, você deve recriar a experiência no formato apropriado. No entanto, você pode reutilizar conteúdo, públicos e conceitos lógicos.

+++

+++ Qual abordagem é mais fácil de criar?

As campanhas de ação normalmente são as mais simples (mensagem única para o público-alvo), seguidas por campanhas acionadas por API e Jornadas (mais complexas com lógica de várias etapas).

+++

+++ Qual dimensionamento é melhor para públicos-alvo grandes?

Todos os três podem ser bem dimensionados; a escolha certa depende do seu padrão:

* As **Jornadas de Leitura de Público** e as **Campanhas de ação** estão otimizadas para públicos de lote grandes (uma mensagem ou fluxo para muitos perfis de uma só vez).
* **O Jornada** unitário (baseado em eventos) processa perfis individualmente à medida que os eventos ocorrem, portanto, a escala depende do volume e da taxa de transferência do evento.

Para segmentação complexa com grandes conjuntos de dados e dados de várias entidades, consulte [Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Posso usar o mesmo público-alvo em jornadas e campanhas?

Sim. Os públicos-alvo criados em [!DNL Adobe Experience Platform] podem ser usados em Jornadas, campanhas de Ação e campanhas Orquestradas. As campanhas acionadas por API são orientadas por carga útil e não usam públicos pré-criados da mesma maneira.

+++

## Próximas etapas {#next-steps}

Pronto(a) para começar a criar? Explore a documentação detalhada da abordagem escolhida:

* **[Introdução ao Jornada](../building-journeys/journey.md)** - Tipos de Jornada, designer e fluxo de trabalho
* **[Introdução às Campanhas](../campaigns/get-started-with-campaigns.md)** - Campanhas acionadas por ação e API
* **[Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)** - Fluxos de trabalho de tela de lote com dados de várias entidades (orientação separada)

>[!MORELIKETHIS]
>
>* [comparação de tipos de Jornada](../building-journeys/journey.md#journey-types-comparison)
>* [Comparação de tipos de campanha](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Perguntas frequentes sobre o Jornada](../building-journeys/journey-faq.md)
>* [Perguntas frequentes sobre campanhas orquestradas](../orchestrated/orchestrated-campaigns-faq.md)
