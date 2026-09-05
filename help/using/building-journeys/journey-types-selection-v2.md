---
solution: Journey Optimizer
product: journey optimizer
title: 'Tipos de jornada: escolha a correta'
description: Compare os tipos de jornada e escolha o correto para seu caso de uso com guias de decisão e matriz de compatibilidade de recursos
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Tipos de jornada, unitário, ler público, qualificação de público, evento comercial, comparação, guia de decisão, escolher, seleção, tempo real, agendado, em lote, acionado por evento
version: Journey Orchestration
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 3%

---


# Tipos de jornada: escolha a correta {#journey-types-selection}

>[!BEGINSHADEBOX]

**Nesta página:** saiba mais sobre os quatro tipos de jornadas do AJO — evento unitário, público-alvo de leitura, qualificação de público-alvo e evento comercial — e descubra qual deles se encaixa no seu caso de uso.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] oferece suporte a quatro tipos de jornada, cada um criado para um tipo diferente de gatilho e cenário de negócios. Entender a diferença ajuda a criar a experiência certa desde o início.

## Os quatro tipos de jornada {#journey-types}

>[!BEGINTABS]

>[!TAB jornadas de eventos unitários]

**Quando usar:** experiências acionadas por eventos em tempo real

**As jornadas de eventos unitários** são acionadas individualmente quando ocorre uma ação específica (compra, entrada no aplicativo, envio de formulário). Os perfis são inseridos um de cada vez em tempo real, tornando-os ideais para respostas imediatas e orientadas por comportamento.

**Perfeito para:** recuperação de abandono de carrinho, integração de novo membro, emails de boas-vindas quando alguém se inscreve e personalização pós-logon.

➡️ [Saiba mais sobre eventos](../event/about-events.md) | [Caso de uso de mensagem para assinantes](message-to-subscribers-uc.md) | [Crie sua primeira jornada](journey-gs.md)

>[!TAB Ler jornadas de Público-Alvo]

**Quando usar:** campanhas agendadas para segmentos de público-alvo

**Ler jornadas de Público-Alvo** inicia com um público-alvo [!DNL Adobe Experience Platform] e envia mensagens em lote para todos os perfis simultaneamente. Esse tipo de jornada é ideal para comunicações programadas em larga escala. Use a opção **leitura incremental** em jornadas recorrentes para processar somente perfis que ingressaram no público-alvo desde a última execução, em vez de reprocessar o público-alvo completo a cada vez.

**Perfeito para:** Boletins informativos mensais, campanhas promocionais para segmentos de público-alvo, anúncios de produtos, séries recorrentes de reengajamento e campanhas de marketing sazonais.

➡️ [Saiba mais sobre a Leitura de Público](read-audience.md) | [Introdução a públicos](../audience/about-audiences.md) | [Crie sua primeira jornada](journey-gs.md)

>[!TAB jornadas de qualificação de público-alvo]

**Quando usar:** respostas em tempo real para alterações de associação de público-alvo

**As jornadas de qualificação de público-alvo** são acionadas quando os perfis se qualificam para (ou saem de) um público-alvo específico. Os perfis são inseridos individualmente à medida que atendem aos critérios, permitindo envolvimento imediato quando o comportamento do cliente muda. Usar **públicos-alvo avaliados por transmissão** — esses são os únicos tipos de público-alvo com suporte para esta atividade.

>[!CAUTION]
>
>A partir de **agosto de 2026**, as jornadas que usam um público-alvo em lote em um nó de Qualificação de público-alvo não poderão ser publicadas. [Saiba como migrar suas jornadas](aq-batch-audiences-migration.md)

**Perfeito para:** notificações de atualização no nível do VIP, mensagens de comemoração da primeira compra, alertas de risco de churn e transições de estágio do ciclo de vida de fidelidade.

➡️ [Saiba mais sobre a qualificação de público-alvo](audience-qualification-events.md) | [Criando públicos-alvo](../audience/creating-a-segment-definition.md) | [Crie sua primeira jornada](journey-gs.md)

>[!TAB jornadas de eventos comerciais]

**Quando usar:** Condições comerciais que afetam vários clientes

As **jornadas de eventos comerciais** são acionadas por um evento comercial (atualizações de ações, alterações de preço) que afeta vários perfis simultaneamente. Internamente, o acionador do evento comercial é sempre seguido por uma etapa Ler público-alvo que assimila os perfis relevantes, de modo que a entrada do perfil segue as regras de taxa de transferência de público-alvo de leitura, não a taxa de transferência de evento unitária.

**Perfeito para:** alertas de baixo estoque para clientes interessados, anúncios de vendas rápidas, notificações de queda de preço e alertas de produtos de volta ao estoque.

➡️ [Saiba mais sobre eventos comerciais](../event/about-creating-business.md) | [Gerenciamento de entradas](entry-management.md) | [Crie sua primeira jornada](journey-gs.md)

>[!ENDTABS]

## Qual tipo você deve usar? {#decision-guide}

A resposta geralmente resume-se a uma pergunta: *o que inicia a jornada?*

Se um **cliente fizer algo específico** — abandonar um carrinho, se inscrever, fazer uma compra — usar uma **jornada de eventos unitária**. Ele é acionado imediatamente quando a ação acontece, um perfil por vez.

Se você quiser **atingir um público-alvo de acordo com um agendamento** — um boletim informativo mensal, uma campanha sazonal, uma série de reenvolvimentos recorrentes — use uma **jornada de leitura de público-alvo**. Você define o público-alvo e o tempo; o AJO processa todos de uma só vez.

Se você quiser responder **no momento em que um cliente atingir uma etapa** — ingressar em uma camada de fidelidade, atingir um limite de risco de churn, concluir uma primeira compra — use uma **jornada de Qualificação de Público-Alvo**. Ele é acionado assim que a associação do público-alvo de transmissão é alterada, não em uma programação fixa.

Se algo mudar **em seu negócio** que afete vários clientes de uma só vez — uma queda no nível das ações, uma mudança de preço, uma venda começa — use uma **jornada de evento comercial**.

>[!TIP]
>
>**Não tem certeza de onde começar?** A maioria das equipes começa com **Evento unitário** para experiências acionadas por comportamento e **Ler público** para campanhas. Esses dois abrangem a maioria dos casos de uso.

| Sua meta | Tipo de jornada recomendado | Por que |
|-----------|--------------------------|-----|
| Recuperar um carrinho abandonado | Evento unitário | Resposta imediata a comportamento individual |
| Enviar informativo mensal aos assinantes | Ler público-alvo | Comunicação agendada em lote |
| Notificar os clientes quando eles atingirem o status do VIP | Qualificação de público-alvo | Resposta em tempo real à entrada de público-alvo da transmissão |
| Alertar os clientes sobre baixo estoque de itens observados | Evento comercial | A condição dos negócios afeta vários clientes |
| Bem-vindos, novos usuários do aplicativo | Evento unitário ou qualificação de público-alvo | Evento de inscrição (evento unitário) ou entrada em um público-alvo de transmissão de novo usuário (Qualificação de público-alvo) |
| Reengajamento de clientes inativos (recorrente, programado) | Ler público-alvo | Execução de lote recorrente em relação ao público-alvo de inatividade |
| Promoção sazonal para o segmento do target | Ler público-alvo | Campanha programada para o público-alvo |
| Anúncio de venda do Flash | Evento comercial | As decisões de negócios afetam vários clientes |
| Reaja assim que um cliente atingir o nível de fidelidade Gold | Qualificação de público-alvo | Público-alvo de transmissão, entrada individual em tempo real |

## Referência de disponibilidade de recursos {#feature-compatibility}

Todos os tipos de jornada são compatíveis com o conjunto completo de canais do AJO (email, push, SMS, no aplicativo, Web, cartões de conteúdo), as atividades principais de orquestração (espera, condição, ações personalizadas), o modo de teste, simulação e otimização de tempo de envio. A tabela abaixo mostra apenas os recursos que diferem entre os tipos.

>[!NOTE]
>
>Limitações da atividade de Jump: uma jornada que começa com uma atividade Ler público ou Qualificação de público-alvo não pode conter uma atividade de Jump e não pode ser o destino de uma atividade de Jump de outra jornada.
>
>A atividade Ler público-alvo como entrada de jornada só está disponível nas jornadas **Ler público-alvo** e **Evento comercial** — ela não pode ser adicionada às jornadas de entrada de Evento unitário ou Qualificação de público-alvo.

| Recurso | Evento unitário | Ler público-alvo | Qualificação de público-alvo | Evento comercial |
|-----------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Entrada** | | | | |
| Entrada acionada por evento | ✅ | ❌ | ❌ | ✅ (o evento comercial aciona a jornada; os perfis entram por meio de uma etapa interna Ler público) |
| Entrada programada | ❌ | ✅ | ❌ | ❌ |
| Entrada baseada no público | ❌ | ✅ (lote) | ✅ (somente streaming) | ❌ |
| **Orquestração** | | | | |
| Atividade Ler público (entrada de jornada) | ❌ | ✅ | ❌ | ✅ (etapa automática após evento comercial) |
| Atividade Salto | ✅ | ❌ | ❌ | ✅ |
| **Gerenciamento de perfis** | | | | |
| Reentrada do perfil | ✅ Configurável | ❌ Uma vez por execução por padrão ([Forçar reentrada na recorrência](read-audience.md#schedule) disponível) | ✅ Configurável (perfil já existente no jornada não pode inserir a mesma versão novamente) | ✅ Por evento |
| **Otimização** | | | | |
| Experimentos de caminho (teste A/B) | ✅ | ✅ | ✅ | ❌ |
| **Avançado** | | | | |
| Leitura incremental | ❌ | ✅ | ❌ | ❌ |
| Taxa de transferência máxima | 5.000 TPS (nível de organização compartilhada com qualificação de público-alvo) | 20.000 TPS por sandbox | 5.000 TPS (nível de organização compartilhado com evento Unitário) | Evento comercial: 5.000 TPS; etapa Ler público: 20.000 TPS |

**Legenda:** ✅ = Com Suporte | ❌ = Não suportado

## Próximas etapas {#next-steps}

Agora que você escolheu um tipo de jornada:

* **[Criar a primeira jornada](journey-gs.md)** — guia passo a passo da entrada à publicação
* **[Saiba mais sobre o designer do jornada](using-the-journey-designer.md)** — Projete sua tela de jornada
* **[Entrada de perfil no jornada](entry-management.md)** — Regras de entrada, reentrada e taxa de transferência por tipo
* **[Introdução ao jornada](journey.md)** — visão geral de fundamentos e recursos
* **[Perguntas frequentes sobre o Journey Orchestration](journey-faq.md)** — perguntas comuns respondidas

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-journey-types-selection-v2.md}}
