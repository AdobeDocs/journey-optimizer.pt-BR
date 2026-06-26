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
source-git-commit: d4ed86ea2833c1753d89186a460ba24ae57773fd
workflow-type: tm+mt
source-wordcount: '2109'
ht-degree: 0%

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página fornece uma comparação abrangente dos quatro tipos de jornada do AJO — Evento unitário, Público de leitura, Qualificação de público-alvo e Evento comercial — juntamente com um guia de decisão e uma matriz de compatibilidade de recursos para ajudar os usuários a escolher o tipo certo para seus casos de uso.

**Intenções:**

* Escolha o tipo de jornada correto para um determinado caso de uso comercial usando a tabela de decisões
* Comparar tipos de jornada lado a lado usando a matriz de compatibilidade de recursos detalhada
* Entenda quando usar Ler jornadas de público-alvo para comunicações em lote agendadas
* Entenda quando usar as jornadas de evento unitárias para experiências acionadas por eventos em tempo real
* Entenda quando usar as jornadas de qualificação de público-alvo para respostas de alteração de status em tempo real
* Entenda quando usar jornadas de eventos comerciais para comunicações orientadas por condições comerciais
* Entenda os limites de taxa de transferência por tipo de jornada ao planejar implantações de alto volume

**Glossário:**

* **jornada de eventos unitária**: uma jornada acionada por uma ação individual do cliente (por exemplo, compra, logon) em que os perfis inserem um de cada vez em tempo real. *(específico do produto)*
* **Ler jornada de público-alvo**: uma jornada que começa com um público-alvo da Adobe Experience Platform e envia mensagens em lote para todos os perfis simultaneamente, de acordo com uma agenda. *(específico do produto)*
* **jornada de qualificação de público-alvo**: uma jornada que dispara quando os perfis se qualificam para um segmento de público-alvo específico ou saem dele. Requer um público avaliado por transmissão para o comportamento de entrada em tempo real. *(específico do produto)*
* **jornada de eventos comerciais**: uma jornada acionada por um evento comercial (por exemplo, atualização de estoque, alteração de preço) que afeta vários perfis simultaneamente; sempre combinada a uma etapa interna Ler público para assimilação de perfil. *(específico do produto)*
* **Leitura incremental**: um recurso de Leitura de público que processa somente os perfis que ingressaram no público desde a última execução, não o público-alvo completo a cada vez. Disponível somente para jornadas de leitura de público-alvo. *(específico do produto)*
* **Público-alvo da transmissão**: um público-alvo da Adobe Experience Platform avaliado continuamente em tempo real, em vez de um público-alvo em lote avaliado em um cronograma (por exemplo, diariamente). Obrigatório para jornadas de qualificação de público-alvo para alcançar o comportamento de entrada em tempo real. *(específico do produto)*

**Medidas de Proteção:**

* A leitura incremental está disponível somente para jornadas de leitura de público, não para jornadas de evento unitário, qualificação de público ou evento comercial
* Experimentos de caminho (teste A/B) não são compatíveis com jornadas de eventos comerciais
* A reentrada de perfil em jornadas de Leitura de público é limitada a uma vez por execução por padrão; use Forçar reentrada na recorrência em execuções programadas para permitir que os perfis entrem novamente na próxima execução
* A atividade Ler público-alvo só está disponível como uma entrada de jornada nas jornadas Ler público-alvo e evento comercial — não nas jornadas de entrada Unitário de evento ou Qualificação de público-alvo
* As jornadas Qualificação de público-alvo e Público-alvo de leitura não podem conter uma atividade de salto e não podem ser o destino de uma atividade de salto de outra jornada
* As jornadas de qualificação de público-alvo exigem um público-alvo avaliado por transmissão. A partir de agosto de 2026, os públicos avaliados em lote não poderão ser usados em um nó de Qualificação de público-alvo — consulte o [guia de migração](aq-batch-audiences-migration.md)
* As jornadas de qualificação de evento e público-alvo unitários compartilham um limite de taxa de transferência de 5.000 TPS no nível da organização; as jornadas de público-alvo de leitura suportam até 20.000 TPS por sandbox
* Um perfil já presente em uma jornada não pode inserir novamente a mesma versão dessa jornada, independentemente da configuração de reentrada

**Terminologia:**

* Nome canônico: jornada de evento unitária — variantes: jornada acionada por evento, jornada unitária
* Nome canônico: Read Audience jornada — variantes: jornada em lote
* Nome canônico: jornada de qualificação de público-alvo — variantes: jornada de eventos de qualificação de público-alvo
* Nome canônico: jornada de evento comercial — variantes: jornada acionada por evento comercial
* Não confunda: &quot;Ler jornada de público-alvo&quot; ≠ &quot;jornada de qualificação de público-alvo&quot; — Ler público-alvo processa todos os membros do público-alvo em lote de acordo com a programação; A qualificação de público-alvo responde a alterações individuais de associação em tempo real (públicos-alvo de transmissão somente para entrada imediata)
* Não confunda: &quot;jornada de evento unitária&quot; ≠ &quot;jornada de evento comercial&quot; — A unitária é acionada por uma ação do cliente que afeta um perfil; o evento comercial é acionado por uma condição comercial e assimila vários perfis por meio de uma etapa interna Ler público

**Perguntas frequentes:**

* **P: Qual tipo de jornada devo usar para um informativo mensal?** — use uma jornada Read Audience; ela foi projetada para comunicação em lote agendada para todos os perfis em um segmento de público-alvo simultaneamente.
* **P: Qual tipo de jornada devo usar para recuperar um carrinho abandonado?** — Utilizar uma jornada de eventos Unitários; é acionada imediatamente quando o evento de abandono ocorre e responde ao comportamento do indivíduo em tempo real.
* **P: Posso executar experimentos de caminho A/B em uma jornada de eventos de Negócios?** — Não; experimentos de caminho não são aceitos em jornadas de eventos de negócios.
* **P: Qual é a diferença entre uma jornada de evento Unitária e uma jornada de Qualificação de Público-Alvo?** — Uma jornada de evento unitária é acionada por uma ação específica do cliente (por exemplo, compra); uma jornada de qualificação de público-alvo é acionada quando um perfil entra ou sai de um segmento de público-alvo com base na avaliação de critérios de transmissão.
* **P: Quais tipos de jornada oferecem suporte para leitura incremental?** — Somente jornadas de leitura de público-alvo oferecem suporte para leitura incremental; os outros três tipos de jornada não.
* **P: Posso adicionar uma atividade Ler público-alvo a uma jornada de eventos Unitária?** — Não; a atividade Ler público só está disponível como entrada de jornada em Ler público e jornadas de eventos comerciais.
* **P: Posso usar uma atividade de salto em uma jornada de Leitura de Público?** — Não; jornadas que começam com uma atividade Ler público ou Qualificação de público não podem conter uma atividade de salto e não podem ser o destino de um salto de outra jornada.
* **P: Posso dar as boas-vindas a novos usuários do aplicativo com uma jornada de Qualificação de Público-Alvo?** — Sim, se a entrada for orientada por um público-alvo de transmissão (por exemplo, quando um perfil ingressa em um segmento de novo usuário); uma jornada de evento unitário de inscrição também é um padrão comum.
* **P: minha jornada de qualificação de público-alvo não está sendo acionada em tempo real. Por quê?** — as jornadas de qualificação de público-alvo exigem um público-alvo avaliado por transmissão. O uso de um público avaliado em lote está obsoleto e será bloqueado a partir de agosto de 2026. [Consulte o guia de migração](aq-batch-audiences-migration.md)
* **P: Qual é a diferença de taxa de transferência entre o evento Unitário e as jornadas de Leitura de Público?** — As jornadas de eventos unitários compartilham um limite de 5.000 TPS com jornadas de qualificação de público-alvo no nível da organização. Leia As jornadas de público suportam até 20.000 TPS por sandbox, tornando-as mais adequadas para campanhas em lote de grande escala.

+++
