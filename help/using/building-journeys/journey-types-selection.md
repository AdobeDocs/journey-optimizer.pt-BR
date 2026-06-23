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
hide: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
TQID: https://experienceleague.adobe.com/rEANha6Lppyd5vog-0kZ3aL9VvZHc9kziW-d-jiWqeA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 151b396b7945535cb4219f782dfb6a79e44463d4
workflow-type: tm+mt
source-wordcount: 2080
ht-degree: 2%

---

# Tipos de jornada: escolha a correta {#journey-types-selection}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como comparar os quatro tipos de jornada — evento unitário, público-alvo de leitura, qualificação de público-alvo e evento comercial — e usar o guia de decisão e a matriz de compatibilidade de recursos para escolher o caso de uso correto.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] oferece suporte a quatro tipos de jornada, cada um projetado para diferentes mecanismos de entrada e cenários de negócios. Este guia ajuda você a entender as diferenças e escolher o tipo certo para seu caso de uso.

>[!NOTE]
>
>Não tem certeza de qual tipo escolher? Comece com **jornadas de evento unitárias** para experiências baseadas em eventos ou **Leia jornadas de público-alvo** para campanhas agendadas — elas abrangem os casos de uso mais comuns.

## Visão geral dos tipos de jornada {#journey-types}

>[!BEGINTABS]

>[!TAB jornadas de eventos unitários]

**Quando usar:** experiências acionadas por eventos em tempo real

**As jornadas de eventos unitários** são acionadas individualmente quando ocorre uma ação específica (compra, entrada no aplicativo, envio de formulário). Os perfis são inseridos um de cada vez em tempo real, tornando-os ideais para respostas imediatas e orientadas por comportamento.

**Perfeito para:** Confirmações de pedidos após a compra, emails de boas-vindas quando alguém assinar, notificações de redefinição de senha e personalização pós-logon.

➡️ [Saiba mais sobre eventos](../event/about-events.md) | [Caso de uso de mensagem para assinantes](message-to-subscribers-uc.md) | [Criar uma jornada de eventos Unitária](#build-unitary-event)

>[!TAB Ler jornadas de Público-Alvo]

**Quando usar:** campanhas agendadas para segmentos de público-alvo

**Ler jornadas de Público-Alvo** inicia com um público-alvo [!DNL Adobe Experience Platform] e envia mensagens em lote para todos os perfis simultaneamente. Esse tipo de jornada é ideal para comunicações programadas em larga escala. Use a opção **leitura incremental** em jornadas recorrentes para processar somente perfis que ingressaram no público-alvo desde a última execução, em vez de reprocessar o público-alvo completo a cada vez.

**Perfeito para:** Boletins informativos mensais, campanhas promocionais para segmentos de público-alvo, anúncios de produtos, séries recorrentes de reengajamento e campanhas de marketing sazonais.

➡️ [Saiba mais sobre a Leitura de Público](read-audience.md) | [Introdução a públicos](../audience/about-audiences.md) | [Criar uma jornada de Leitura de Público](#build-read-audience)

>[!TAB jornadas de qualificação de público-alvo]

**Quando usar:** respostas em tempo real para alterações de associação de público-alvo

**As jornadas de qualificação de público-alvo** são acionadas quando os perfis se qualificam para (ou saem de) um público-alvo específico. Os perfis são inseridos individualmente à medida que atendem aos critérios, permitindo envolvimento imediato quando o comportamento do cliente muda. Para o comportamento de entrada em tempo real, o público deve ser **avaliado por transmissão**; os públicos avaliados em lote acionam a entrada somente na próxima janela de avaliação (até 24 horas).

**Perfeito para:** notificações de atualização no nível do VIP, mensagens de comemoração da primeira compra, alertas de risco de churn e transições de estágio do ciclo de vida de fidelidade.

➡️ [Saiba mais sobre a qualificação de público-alvo](audience-qualification-events.md) | [Criando públicos-alvo](../audience/creating-a-segment-definition.md) | [Criar uma jornada de qualificação de público-alvo](#build-audience-qualification)

>[!TAB jornadas de eventos comerciais]

**Quando usar:** Condições comerciais que afetam vários clientes

As **jornadas de eventos comerciais** são acionadas por um evento comercial (atualizações de ações, alterações de preço) que afeta vários perfis simultaneamente. Internamente, o acionador do evento comercial é sempre seguido por uma etapa Ler público-alvo que assimila os perfis relevantes, de modo que a entrada do perfil segue as regras de taxa de transferência de público-alvo de leitura, não a taxa de transferência de evento unitária.

**Perfeito para:** alertas de baixo estoque para clientes interessados, anúncios de vendas rápidas, notificações de queda de preço e alertas de produtos de volta ao estoque.

➡️ [Saiba mais sobre eventos comerciais](../event/about-creating-business.md) | [Gerenciamento de entradas](entry-management.md) | [Criar uma jornada de eventos comerciais](#build-business-event)

>[!ENDTABS]

## Guia de decisão: escolha do tipo de jornada {#decision-guide}

Use a tabela abaixo para corresponder sua meta ao tipo de jornada correto. Para a maioria dos novos usuários, as jornadas de **Evento unitário** ou **Ler público** abrangem a maioria dos casos de uso.

| Sua meta | Tipo de jornada recomendado | Por que |
|-----------|--------------------------|-----|
| Enviar confirmação do pedido após a compra | Evento unitário | Resposta imediata a uma ação individual |
| Enviar informativo mensal aos assinantes | Ler público-alvo | Comunicação agendada em lote |
| Notificar os clientes quando eles atingirem o status do VIP | Qualificação de público-alvo | Resposta em tempo real à entrada de público-alvo da transmissão |
| Alertar os clientes sobre baixo estoque de itens observados | Evento comercial | A condição dos negócios afeta vários clientes |
| Bem-vindos, novos usuários do aplicativo | Evento unitário | Acionado pelo evento de inscrição |
| Reengajamento de clientes inativos (recorrente, programado) | Ler público-alvo | Execução de lote recorrente em relação ao público-alvo de inatividade |
| Promoção sazonal para o segmento do target | Ler público-alvo | Campanha programada para o público-alvo |
| Anúncio de venda do Flash | Evento comercial | As decisões de negócios afetam vários clientes |
| Reaja assim que um cliente atingir o nível de fidelidade Gold | Qualificação de público-alvo | Público-alvo de transmissão, entrada individual em tempo real |

## Comparação detalhada de tipos de jornada {#journey-types-comparison}

| Aspecto | Jornadas de eventos unitários | Ler jornadas de público-alvo | Jornadas de qualificação de público | Jornadas de eventos comerciais |
|--------|------------------------|------------------------|--------------------------------|------------------------|
| **Mecanismo de entrada** | Acionador de evento individual | Lote agendado | Alteração na associação de público à transmissão em tempo real | Evento de nível empresarial + etapa Ler público |
| **Tempo de entrada** | Tempo real, à medida que os eventos ocorrem | Agendado (único ou recorrente) | Em tempo real, conforme a qualificação ocorre (públicos-alvo de transmissão); atrasado para públicos-alvo avaliados em lote | Acionador em tempo real; a assimilação de perfis segue a taxa de transferência Ler público-alvo |
| **Entrada de perfil** | Um de cada vez | Todos de uma vez (lote) | Um de cada vez | Vários perfis por meio da etapa interna Ler público |
| **Origem do acionador** | Ação do cliente (compra, clique, logon) | Cronograma com base no tempo | Entrada ou saída da associação de público | Condição comercial (ação, preço) |
| **Recomendado para** | Mensagens transacionais, respostas comportamentais | Campanhas de marketing, boletins informativos, programas recorrentes | Programas de fidelidade, transições de estágio do ciclo de vida | Alertas de estoque, promoções e condições comerciais |
| **Usar quando** | Resposta imediata a ações individuais necessárias | Atingir grandes segmentos de público-alvo no cronograma | Resposta às alterações no status do cliente em tempo real | Os eventos comerciais afetam vários clientes simultaneamente |
| **Exemplos** | Confirmação de pedido, redefinição de senha | Informativo mensal, campanha sazonal | Atualização do VIP, alerta de risco de churn | Alerta de baixo estoque, venda rápida, queda de preço |
| **Reentrada** | Configurável | Uma vez por execução | Configurável por evento de qualificação; um perfil que já está na jornada não pode inserir a mesma versão novamente | Vários perfis podem ser afetados pelo mesmo evento |
| **Taxa de transferência máxima** | 5.000 TPS (nível de organização compartilhada com qualificação de público-alvo) | 20.000 TPS por sandbox | 5.000 TPS (nível de organização compartilhado com evento Unitário) | Evento comercial: 5.000 TPS; etapa Ler público: 20.000 TPS |
| **Requisitos de dados** | Esquema de evento com dados de acionador | [!DNL Adobe Experience Platform] público-alvo | Público-alvo de transmissão (necessário para entrada em tempo real); público-alvo em lote suportado, mas atrasa a entrada | Esquema de evento comercial |

## Compatibilidade de recursos por tipo de jornada {#feature-compatibility}

Nem todos os recursos estão disponíveis para todos os tipos de jornada. Use esta matriz para entender quais recursos funcionam com quais tipos de jornada:

| Recurso/capacidade | Evento unitário | Ler público-alvo | Qualificação de público-alvo | Evento comercial |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mecanismos de entrada** | | | | |
| Entrada acionada por evento | ✅ | ❌ | ❌ | ✅ (o evento comercial aciona a jornada; os perfis entram por meio de uma etapa interna Ler público) |
| Entrada programada | ❌ | ✅ | ❌ | ❌ |
| Entrada baseada no público | ❌ | ✅ (lote) | ✅ (streaming) | ❌ |
| **Recursos de orquestração** | | | | |
| Atividades de espera | ✅ | ✅ | ✅ | ✅ |
| Atividades de condição | ✅ | ✅ | ✅ | ✅ |
| Ações personalizadas | ✅ | ✅ | ✅ | ✅ |
| Atividade Ler público (dentro do jornada) | ✅ | ✅ | ✅ | ✅ |
| Atividade de Qualificação de público-alvo (dentro do jornada) | ✅ | ✅ | ✅ | ✅ |
| Atividade Salto | ✅ | ❌ | ❌ | ✅ |
| **Gerenciamento de perfis** | | | | |
| Reentrada do perfil | ✅ Configurável | ❌ Uma vez por execução | ✅ Configurável (perfil já existente no jornada não pode inserir a mesma versão novamente) | ✅ Por evento |
| Configuração de namespace | ✅ Obrigatório | ✅ Opcional | ✅ Obrigatório | ✅ Obrigatório |
| Limite de perfil | ✅ | ✅ | ✅ | ✅ |
| **Testes e otimização** | | | | |
| Modo de teste | ✅ | ✅ | ✅ | ✅ |
| Secagem | ✅ | ✅ | ✅ | ✅ |
| Experimentos de caminho (teste A/B) | ✅ | ✅ | ✅ | ❌ |
| Otimização de hora de envio | ✅ | ✅ | ✅ | ✅ |
| **Canais** | | | | |
| Email | ✅ | ✅ | ✅ | ✅ |
| Notificações por push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Mensagens no aplicativo | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Cartões de conteúdo | ✅ | ✅ | ✅ | ✅ |
| **Recursos avançados** | | | | |
| Leitura incremental | ❌ | ✅ | ❌ | ❌ |
| Exportar público | ✅ | ✅ | ✅ | ✅ |
| Gerenciamento de fuso horário | ✅ | ✅ | ✅ | ✅ |
| Eventos de reação | ✅ | ✅ | ✅ | ✅ |
| Fontes de dados externas | ✅ | ✅ | ✅ | ✅ |
| Limitação/limitação | ✅ | ✅ | ✅ | ✅ |

**Legenda:** ✅ = Com Suporte | ❌ = Não suportado

>[!NOTE]
>
>Limitações da atividade de Jump: uma jornada que começa com uma atividade Ler público ou Qualificação de público-alvo não pode conter uma atividade de Jump e não pode ser o destino de uma atividade de Jump de outra jornada.

## Próximas etapas {#next-steps}

Cada tabela lista as etapas de configuração por meio do gerenciamento para esse tipo de jornada.

### Jornadas de eventos unitários {#build-unitary-event}

* **[Criar a primeira jornada](journey-gs.md)** - Guia passo a passo
* **[Saiba mais sobre o designer do jornada](using-the-journey-designer.md)** - Crie sua tela de jornada
* **[Explore os recursos do jornada](journey.md#capabilities)** - Descubra recursos avançados
* **[Exibir perguntas frequentes sobre o jornada](journey-faq.md)** - Perguntas frequentes respondidas

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
* A reentrada do perfil nas jornadas Read Audience é limitada a uma vez por execução
* As jornadas Qualificação de público-alvo e Público-alvo de leitura não podem conter uma atividade de salto e não podem ser o destino de uma atividade de salto de outra jornada
* As jornadas de qualificação de público exigem um público avaliado por transmissão para entrada em tempo real; os públicos avaliados em lote causam atrasos de entrada de até 24 horas
* As jornadas de qualificação de evento e público-alvo unitários compartilham um limite de taxa de transferência de 5.000 TPS no nível da organização; as jornadas de público-alvo de leitura suportam até 20.000 TPS por sandbox
* Um perfil já presente em uma jornada não pode inserir novamente a mesma versão dessa jornada, independentemente da configuração de reentrada

**Terminologia:**

* Nome canônico: jornada de evento unitária — variantes: jornada acionada por evento, jornada unitária
* Nome canônico: Read Audience jornada — variantes: jornada em lote, jornada de acionador de segmento, jornada de segmento de leitura
* Nome canônico: jornada de qualificação de público-alvo — variantes: jornada de eventos de qualificação de público-alvo
* Nome canônico: jornada de evento comercial — variantes: jornada acionada por evento comercial
* Não confunda: &quot;Ler jornada de público-alvo&quot; ≠ &quot;jornada de qualificação de público-alvo&quot; — Ler público-alvo processa todos os membros do público-alvo em lote de acordo com a programação; A qualificação de público-alvo responde a alterações individuais de associação em tempo real (públicos-alvo de transmissão somente para entrada imediata)
* Não confunda: &quot;jornada de evento unitária&quot; ≠ &quot;jornada de evento comercial&quot; — A unitária é acionada por uma ação do cliente que afeta um perfil; o evento comercial é acionado por uma condição comercial e assimila vários perfis por meio de uma etapa interna Ler público

**Perguntas frequentes:**

* **P: Qual tipo de jornada devo usar para um informativo mensal?** — use uma jornada Read Audience; ela foi projetada para comunicação em lote agendada para todos os perfis em um segmento de público-alvo simultaneamente.
* **P: Que tipo de jornada processa uma confirmação de pedido após uma compra?** — use uma jornada de eventos Unitária; ela fornece uma resposta imediata em tempo real a uma ação individual do cliente.
* **P: Posso executar experimentos de caminho A/B em uma jornada de eventos de Negócios?** — Não; experimentos de caminho não são aceitos em jornadas de eventos de negócios.
* **P: Qual é a diferença entre uma jornada de evento Unitária e uma jornada de Qualificação de Público-Alvo?** — Uma jornada de evento unitária é acionada por uma ação específica do cliente (por exemplo, compra); uma jornada de qualificação de público-alvo é acionada quando um perfil entra ou sai de um segmento de público-alvo com base na avaliação de critérios de transmissão.
* **P: Quais tipos de jornada oferecem suporte para leitura incremental?** — Somente jornadas de leitura de público-alvo oferecem suporte para leitura incremental; os outros três tipos de jornada não.
* **P: Posso usar uma atividade de salto em uma jornada de Leitura de Público?** — Não; jornadas que começam com uma atividade Ler público ou Qualificação de público não podem conter uma atividade de salto e não podem ser o destino de um salto de outra jornada.
* **P: minha jornada de qualificação de público-alvo não está sendo acionada em tempo real. Por quê?** — as jornadas de qualificação de público-alvo exigem um público-alvo avaliado por transmissão. Se o público-alvo for avaliado em lote (por exemplo, um instantâneo diário), a entrada será atrasada até a próxima janela de avaliação, que pode ser de até 24 horas.
* **P: Qual é a diferença de taxa de transferência entre o evento Unitário e as jornadas de Leitura de Público?** — As jornadas de eventos unitários compartilham um limite de 5.000 TPS com jornadas de qualificação de público-alvo no nível da organização. Leia As jornadas de público suportam até 20.000 TPS por sandbox, tornando-as mais adequadas para campanhas em lote de grande escala.

+++
