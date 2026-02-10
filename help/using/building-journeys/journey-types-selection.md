---
solution: Journey Optimizer
product: journey optimizer
title: Tipos de jornada e guia de seleção
description: Compare os tipos de jornada e escolha o correto para seu caso de uso com guias de decisão e matriz de compatibilidade de recursos
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Tipos de jornada, unitário, ler público, qualificação de público, evento comercial, comparação, guia de decisão, escolher, seleção, tempo real, agendado, em lote, acionado por evento
version: Journey Orchestration
hide: true
hidefromtoc: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 4%

---

# Tipos de jornada e guia de seleção {#journey-types-selection}

O [!DNL Adobe Journey Optimizer] oferece suporte a quatro tipos de jornada, cada um projetado para diferentes mecanismos de entrada e cenários de negócios. Este guia ajuda você a entender as diferenças e escolher o tipo certo para seu caso de uso.

## Visão geral dos tipos de jornada {#journey-types}

>[!BEGINTABS]

>[!TAB jornadas unitárias]

**Quando usar:** experiências acionadas por eventos em tempo real

As **jornadas unitárias** são acionadas individualmente quando ocorre uma ação específica (compra, entrada no aplicativo, envio de formulário). Os perfis são inseridos um de cada vez em tempo real, tornando-os ideais para respostas imediatas e orientadas por comportamento.

**Perfeito para:** confirmações de pedidos após a compra, emails de boas-vindas quando alguém se inscreve, abandono de carrinho acionado pela navegação e notificações de redefinição de senha.

➡️ [Saiba mais sobre eventos](../event/about-events.md) | [Caso de uso de mensagem para assinantes](message-to-subscribers-uc.md)

>[!TAB Ler jornadas de Público-Alvo]

**Quando usar:** campanhas agendadas para segmentos de público-alvo

**Ler jornadas de Público-Alvo** inicia com um público-alvo [!DNL Adobe Experience Platform] e envia mensagens em lote para todos os perfis simultaneamente. Esse tipo de jornada é ideal para comunicações programadas em larga escala.

**Perfeito para:** Boletins informativos mensais, campanhas promocionais para segmentos do público-alvo, anúncios de produtos e campanhas de marketing sazonais.

➡️ [Saiba mais sobre a Leitura de Público](read-audience.md) | [Introdução aos públicos-alvo](../audience/about-audiences.md)

>[!TAB jornadas de qualificação de público-alvo]

**Quando usar:** respostas em tempo real para alterações de associação de público-alvo

**As jornadas de qualificação de público-alvo** são acionadas quando os perfis se qualificam para (ou saem de) um público-alvo específico. Os perfis entram individualmente, pois atendem aos critérios em tempo real, permitindo envolvimento imediato quando o comportamento do cliente muda.

**Perfeito para:** notificações de atualização de nível do VIP, reengajamento quando os clientes se tornam inativos, mensagens de comemoração da primeira compra e definição de metas geográficas quando os clientes se mudam.

➡️ [Saiba mais sobre a qualificação de público-alvo](audience-qualification-events.md) | [Criando públicos-alvo](../audience/creating-a-segment-definition.md)

>[!TAB jornadas de eventos comerciais]

**Quando usar:** Condições comerciais que afetam vários clientes

As **jornadas de eventos comerciais** são acionadas por eventos comerciais (atualizações de ações, alertas meteorológicos, alterações de preço) que afetam vários perfis simultaneamente. Elas respondem a condições empresariais mais amplas, em vez de ações individuais.

**Perfeito para:** alertas de baixo estoque para clientes interessados, anúncios de vendas rápidas, promoções baseadas em clima, notificações de queda de preço e alertas de devolução de produtos no estoque.

➡️ [Saiba mais sobre eventos comerciais](../event/about-creating-business.md) | [Gerenciamento de entradas](entry-management.md)

>[!ENDTABS]

## Guia de decisão: escolha do tipo de jornada {#decision-guide}

Siga esta árvore decisória para selecionar o tipo de jornada correto para seu caso de uso:

### Etapa 1: o que aciona a jornada?

* **O cliente executa uma ação específica** (compra, clique, logon) → Vá para a Etapa 2
* **Horário/agendamento** (enviar em horário específico ou recorrente) → **Usar jornada de Leitura de Público**
* **Alterações no status do cliente** (entra/sai de um segmento) → Vá para a Etapa 3
* **Condição comercial** (nível de ação, alteração de preço, clima) → **Usar jornada de eventos comerciais**

### Etapa 2: acionadores de ação individuais do cliente

* **É necessária resposta imediata em tempo real?**
   * Sim → **Usar jornada Unitária**
   * Não → Considere ler a jornada de público-alvo com execução programada

### Etapa 3: alterações de status do cliente

* **Precisa responder quando os clientes entrarem OU saírem de um segmento?**
   * Sim → **Usar jornada de qualificação de público-alvo**
   * Não, somente ao inserir → Considerar a jornada unitária com evento ou Ler público com filtro de público

### Seleção rápida por caso de uso

| Sua meta | Tipo de jornada recomendado | Por que |
|-----------|------------------------|-----|
| Enviar confirmação do pedido após a compra | Unitário | Resposta imediata a uma ação individual |
| Enviar informativo mensal aos assinantes | Ler público-alvo | Comunicação agendada em lote |
| Notificar os clientes quando eles atingirem o status do VIP | Qualificação de público-alvo | Resposta em tempo real à alteração de status |
| Alertar os clientes sobre baixo estoque de itens observados | Evento comercial | A condição dos negócios afeta vários clientes |
| Bem-vindos, novos usuários do aplicativo | Unitário | Acionado pelo evento de inscrição |
| Reengajamento de clientes inativos | Qualificação de público-alvo | Responde à entrada de segmento de inatividade |
| Promoção sazonal para o segmento do target | Ler público-alvo | Campanha programada para o público-alvo |
| Anúncio de venda do Flash | Evento comercial | As decisões de negócios afetam vários clientes |

>[!NOTE]
>
>Não tem certeza de qual tipo escolher? Comece com **jornadas unitárias** para experiências baseadas em eventos ou **Leia jornadas de público-alvo** para campanhas agendadas, que abrangem os casos de uso mais comuns.

## Comparação detalhada de tipos de jornada {#journey-types-comparison}

Use esta tabela para comparar rapidamente os tipos de jornada e escolher o correto para seu caso de uso:

| Aspecto | Jornadas unitárias | Ler jornadas de público-alvo | Jornadas de qualificação de público | Jornadas de eventos comerciais |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Mecanismo de entrada** | Acionador de evento individual | Lote agendado | Alteração na associação de público-alvo em tempo real | Evento de nível empresarial |
| **Tempo de entrada** | Tempo real, à medida que os eventos ocorrem | Agendado (único ou recorrente) | Em tempo real, conforme a qualificação ocorre | Em tempo real, quando um evento comercial é acionado |
| **Entrada de perfil** | Um de cada vez | Todos de uma vez (lote) | Um de cada vez | Vários perfis simultaneamente |
| **Origem do acionador** | Ação do cliente (compra, clique, logon) | Cronograma com base no tempo | Associação de público (entrada/saída) | Condição comercial (ação, clima, preço) |
| **Recomendado para** | Mensagens transacionais, respostas comportamentais | Campanhas de marketing, informativos | Programas de fidelidade, estágios do ciclo de vida | Alertas de estoque, promoções e condições comerciais |
| **Usar quando** | Resposta imediata a ações individuais necessárias | Atingir grandes segmentos de público-alvo no cronograma | Resposta às alterações de status do cliente | Os eventos comerciais afetam vários clientes |
| **Exemplos** | Confirmação de pedido, redefinição de senha | Informativo mensal, campanha sazonal | Atualização do VIP, alerta de inatividade | Alerta de baixo estoque, venda rápida, queda de preço |
| **Reentrada** | Configurável (permitir várias entradas por perfil) | Cada perfil é inserido uma vez por execução | Configurável por evento de qualificação | Vários perfis podem ser afetados pelo mesmo evento |
| **Requisitos de dados** | Esquema de evento com dados de acionador | [!DNL Adobe Experience Platform] público-alvo | Público-alvo em lote ou streaming | Esquema de evento comercial |

## Compatibilidade de recursos por tipo de jornada {#feature-compatibility}

Nem todos os recursos estão disponíveis para todos os tipos de jornada. Use esta matriz para entender quais recursos funcionam com quais tipos de jornada:

| Recurso/capacidade | Unitário | Ler público-alvo | Qualificação de público-alvo | Evento comercial |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Mecanismos de entrada** |
| Entrada acionada por evento | ✅ | ❌ | ❌ | ✅ |
| Entrada programada | ❌ | ✅ | ❌ | ❌ |
| Entrada baseada no público | ❌ | ✅ | ✅ | ❌ |
| **Recursos de orquestração** |
| Atividades de espera | ✅ | ✅ | ✅ | ✅ |
| Atividades de condição | ✅ | ✅ | ✅ | ✅ |
| Ações personalizadas | ✅ | ✅ | ✅ | ✅ |
| Ler atividade de público (dentro do jornada) | ✅ | ✅ | ✅ | ✅ |
| Atividade de qualificação de público | ✅ | ✅ | ✅ | ✅ |
| Atividade Salto | ✅ | ✅ | ✅ | ✅ |
| **Gerenciamento de perfis** |
| Reentrada do perfil | ✅ Configurável | ❌ Uma vez por execução | ✅ Configurável | ✅ Por evento |
| Configuração de namespace | ✅ Obrigatório | ✅ Opcional | ✅ Obrigatório | ✅ Obrigatório |
| Limite de perfil | ✅ | ✅ | ✅ | ✅ |
| **Testes e otimização** |
| Modo de teste | ✅ | ✅ | ✅ | ✅ |
| Secagem | ✅ | ✅ | ✅ | ✅ |
| Experimentos de caminho (teste A/B) | ✅ | ✅ | ✅ | ❌ |
| Otimização de hora de envio | ✅ | ✅ | ✅ | ✅ |
| **Canais** |
| Email | ✅ | ✅ | ✅ | ✅ |
| Notificações por push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Mensagens no aplicativo | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Cartões de conteúdo | ✅ | ✅ | ✅ | ✅ |
| **Recursos avançados** |
| Leitura incremental | ❌ | ✅ | ❌ | ❌ |
| Exportar público | ✅ | ✅ | ✅ | ✅ |
| Gerenciamento de fuso horário | ✅ | ✅ | ✅ | ✅ |
| Eventos de reação | ✅ | ✅ | ✅ | ✅ |
| Fontes de dados externas | ✅ | ✅ | ✅ | ✅ |
| Limitação/limitação | ✅ | ✅ | ✅ | ✅ |

**Legenda:** ✅ = Com Suporte | ❌ = Não suportado

## Próximas etapas {#next-steps}

Agora que você entende os tipos de jornada, está pronto para:

* **[Criar a primeira jornada](journey-gs.md)** - Guia passo a passo
* **[Saiba mais sobre o designer do jornada](using-the-journey-designer.md)** - Crie sua tela de jornada
* **[Explore os recursos do jornada](journey.md#capabilities)** - Descubra recursos avançados
* **[Exibir perguntas frequentes sobre o jornada](journey-faq.md)** - Perguntas frequentes respondidas

**Precisa comparar com campanhas?**

* [Guia de comparação de Jornadas vs Campanhas](../start/journeys-vs-campaigns.md) - Escolha entre jornadas, campanhas de Ação/API e campanhas Orquestradas
