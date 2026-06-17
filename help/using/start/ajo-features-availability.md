---
solution: Journey Optimizer
product: journey optimizer
title: Disponibilidade de recursos do Journey Optimizer
description: Uma única referência consolidada para descobrir quais recursos do Adobe Journey Optimizer estão disponíveis, seu status de ciclo de vida (Disponibilidade geral, Disponibilidade limitada ou Beta), a qual oferta básica eles se aplicam e quando são enviados, sem fazer referência cruzada às notas de versão.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner, Intermediate
keywords: jornada otimizer, disponibilidade de recursos, o que está disponível, GA, disponibilidade limitada, beta, ciclo de vida, data de lançamento, direito, oferta básica, campanhas, jornada
hide: true
source-git-commit: f13e351c6c3851f9c031e7aa907ecc5924e0df4f
workflow-type: tm+mt
source-wordcount: '1880'
ht-degree: 13%

---


# Disponibilidade de recursos do Journey Optimizer {#ajo-features-availability}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra quais [!DNL Adobe Journey Optimizer] recursos estão disponíveis, em qual estágio do ciclo de vida cada um está (Disponibilidade Geral, Disponibilidade Limitada ou Beta), a qual oferta básica eles se aplicam e quando foram enviados — para que você possa responder *&quot;Posso usar isso?&quot;* sem analisar as notas de versão.

>[!ENDSHADEBOX]

Esta página consolida a disponibilidade de recursos no [!DNL Adobe Journey Optimizer] para que você possa confirmar o que pode usar durante o escopo de pré-implementação. Os recursos são agrupados por área de capacidade. Em cada área, cada recurso lista seu status do ciclo de vida atual, a oferta base à qual se aplica, a data em que ficou disponível e quaisquer notas sobre configuração ou restrições regionais.

As linhas marcadas como **Recurso principal** na *Disponível desde* coluna são recursos fundamentais de longa data que estão disponíveis desde antes de 2026. As linhas datadas refletem as alterações entregues em 2026.

>[!IMPORTANT]
>
>**Por que não posso ver um recurso em meu ambiente?** Os recursos da **Disponibilidade Limitada** ou da **Beta** não estão visíveis para todos — eles são implantados primeiro em um conjunto restrito de organizações. Se um recurso sobre o qual você leu não aparecer no seu ambiente, verifique o status abaixo: se for **LA** ou **Beta**, entre em contato com o representante da Adobe para solicitar acesso. Um recurso listado aqui não significa que ele está ativado em seu ambiente.

>[!NOTE]
>
>**Disponibilidade vs. qualificação.** Esta página rastreia o *ciclo de vida e a disponibilidade do recurso* (se um recurso foi fornecido e em que maturidade). A inclusão ou não de um recurso *na sua licença* depende da oferta base e dos complementos — consulte [Pacotes e recursos](ajo-packages.md).

## O que significam os status do ciclo de vida {#status-definitions}

| Status | O que significa |
|--------|--------------|
| **GA** — Disponibilidade Geral | Lançado para todos os ambientes. Disponível para qualquer organização cuja licença inclua o recurso. |
| **LA** — Disponibilidade limitada | Liberado para um conjunto restrito de organizações. **Contate seu representante da Adobe** para solicitar acesso. |
| **Beta** | Lançamento de acesso antecipado para avaliação. Pode mudar antes de Disponibilidade geral. Pode exigir a aceitação. |

## Como &quot;Aplica-se a&quot; é mapeado para ofertas básicas {#applies-to}

A coluna **Aplica-se a** se refere às três ofertas base [!DNL Adobe Journey Optimizer]:

- **Journey Optimizer - Campanhas** — lote, orquestração baseada em público
- **Journey Optimizer - Jornada** — orquestração em tempo real orientada por eventos
- **Journey Optimizer - Campanhas e Jornadas** — ambos

Recursos de canal, conteúdo e plataforma marcados como **Todas as ofertas básicas** estão disponíveis independentemente da oferta básica, mas a maioria ainda requer o canal relevante ou o complemento de recurso avançado. Consulte [Pacotes e recursos](ajo-packages.md) para obter detalhes sobre os direitos.

## Recursos por área de recurso {#features-by-area}

>[!BEGINTABS]

>[!TAB Canais]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Novo canal de mensagens móveis (SMS, MMS, RCS) | GA | Todas as ofertas básicas | 20 de maio de 2026 | Unifica SMS/MMS/RCS; criação de RCS nativo (imagens, carrosséis) |
| Deep links no Designer de email | GA | Todas as ofertas básicas | 12 de maio de 2026 | Requer configuração de aplicativo móvel |
| Otimizar email para caixas de entrada de IA | GA | Todas as ofertas básicas | 17 de abril de 2026 | Apple Intelligence, Gmail Gemini |
| Parâmetros de remetente no cabeçalho do email | GA | Todas as ofertas básicas | Abril de 2026 | &quot;Remetente em nome de&quot;/&quot;via&quot; |
| Campo CC nas configurações do canal de email | GA | Todas as ofertas básicas | Abril de 2026 | Oferece suporte à personalização |
| Caixa de entrada | GA | Todas as ofertas básicas | 7 de abril de 2026 | — |
| Canal de notificações por push na web | GA | Todas as ofertas básicas | 13 de fevereiro de 2026 | Anteriormente Beta |
| Atividade em tempo real no iOS | GA | Todas as ofertas básicas | 3 de março de 2026 | Tela de bloqueio / Dynamic Island; anteriormente Beta |
| Canal de correspondência direta em jornadas | GA | Jornada; Campanhas e Jornadas | 29 de janeiro de 2026 | Anteriormente: LA |
| Canal de correspondência direta em campanhas orquestradas | GA | Campanhas, Campanhas e Jornadas | 28 de janeiro de 2026 | — |
| Canal LINE | GA | Todas as ofertas básicas | 2025 | — |
| Suporte e rastreamento de botões do WhatsApp | GA | Todas as ofertas básicas | Maio de 2026 | Resposta rápida, URL/telefone do CTA |
| Email | GA | Todas as ofertas básicas | Recurso principal | Exige complemento de Entrega de saída |
| Notificações por push | GA | Todas as ofertas básicas | Recurso principal | Requer entrega de saída ou complemento para dispositivos móveis |
| SMS/MMS | GA | Todas as ofertas básicas | Recurso principal | Baseado na sua configuração licenciada |
| Correspondência direta | GA | Todas as ofertas básicas | Recurso principal | Exige complemento de Entrega de saída |
| Mensagens no aplicativo | GA | Todas as ofertas básicas | Recurso principal | Exige complemento para dispositivos móveis |
| Cartões de conteúdo | GA | Todas as ofertas básicas | Recurso principal | Exige complemento para dispositivos móveis |
| Canal da web | GA | Todas as ofertas básicas | Recurso principal | Requer complemento da Web |
| Experiências baseadas em código | GA | Todas as ofertas básicas | Recurso principal | Requer complemento para dispositivos móveis ou Web |
| Páginas de destino | GA | Todas as ofertas básicas | Recurso principal | — |
| WhatsApp | GA | Todas as ofertas básicas | Recurso principal | Requer o complemento WhatsApp; com base na configuração licenciada |

>[!TAB Jornadas]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Fragmentos de jornada | GA | Jornada; Campanhas e Jornadas | 9 de junho de 2026 | Nós de jornada reutilizáveis; suporte a ferramentas de sandbox |
| Simulação de jornada | GA | Jornada; Campanhas e Jornadas | 9 de junho de 2026 | Validar a lógica com usuários simulados |
| Otimização do caminho de Jornada - Direcionamento | GA | Jornada; Campanhas e Jornadas | 8 de junho de 2026 | Direcionamento de caminho determinístico |
| Suporte de identificador complementar para públicos externos | GA | Jornada; Campanhas e Jornadas | 11 de junho de 2026 | Composição de CSV e público-alvo federado |
| Experimentação do caminho da jornada | GA | Jornada; Campanhas e Jornadas | 7 de abril de 2026 | A/B e bandit multi-armed; &quot;dimensionar o vencedor&quot; |
| Atividade de ação em jornadas | GA | Jornada; Campanhas e Jornadas | 20 de fevereiro de 2026 | Substitui atividades de canal nativas obsoletas |
| Atividade de decisão de conteúdo | GA | Jornada; Campanhas e Jornadas | 10 de fevereiro de 2026 | Anteriormente: LA |
| Períodos de silêncio (exclusões com base no tempo) | GA | Jornada; Campanhas e Jornadas | 29 de janeiro de 2026 | Anteriormente: LA |
| Assistente do AI para expressões de jornada | Beta | Jornada; Campanhas e Jornadas | 3 de junho de 2026 | Beta público |
| Arbitragem de jornada | LA | Jornada; Campanhas e Jornadas | 24 de fevereiro de 2026 | Entre em contato com seu representante da Adobe |
| Arbitragem de jornada - Modelos de IA | LA | Jornada; Campanhas e Jornadas | Abril de 2026 | Entre em contato com seu representante da Adobe |
| Suporte à pesquisa de conjunto de dados em jornadas | LA | Jornada; Campanhas e Jornadas | Março de 2026 | Para clientes qualificados para pesquisa de conjunto de dados |
| Envio de onda de mensagens de saída (jornada) | LA | Jornada; Campanhas e Jornadas | 16 de março de 2026 | GA em campanhas; LA em jornadas |
| Jornadas automatizadas (acionadas por eventos) | GA | Jornada; Campanhas e Jornadas | Recurso principal | Orquestração em tempo real do :1 |
| Acionadores de eventos em tempo real | GA | Jornada; Campanhas e Jornadas | Recurso principal | — |
| Ler jornadas de público (com base no público) | GA | Jornada; Campanhas e Jornadas | Recurso principal | — |
| Relatórios de jornada | GA | Jornada; Campanhas e Jornadas | Recurso principal | — |

>[!TAB Campanhas]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Campanhas orquestradas encadeadas | GA | Campanhas, Campanhas e Jornadas | 20 de maio de 2026 | Acionar uma campanha da atividade End de outra campanha |
| Atividade de query incremental em campanhas orquestradas | GA | Campanhas, Campanhas e Jornadas | 30 de abril de 2026 | Direciona somente perfis/eventos novos e qualificados |
| Copiar campanhas orquestradas em sandboxes | GA | Campanhas, Campanhas e Jornadas | Abril de 2026 | As campanhas importadas são direcionadas para o status de rascunho |
| Atividade de teste em campanhas orquestradas | GA | Campanhas, Campanhas e Jornadas | Março de 2026 | — |
| Acionar campanhas orquestradas usando um sinal | GA | Campanhas, Campanhas e Jornadas | Março de 2026 | Permanece uma campanha em lote |
| Categoria transacional em campanhas orquestradas | GA | Campanhas, Campanhas e Jornadas | Março de 2026 | Distribuído gradualmente por região |
| Envio de onda de mensagens de saída (campanhas) | GA | Campanhas, Campanhas e Jornadas | 19 de fevereiro de 2026 | LA no jornada |
| Campanhas em lote | GA | Campanhas, Campanhas e Jornadas | Recurso principal | Envios programados e baseados no público-alvo |
| Campanhas orquestradas (fluxos de trabalho de várias etapas) | GA | Campanhas, Campanhas e Jornadas | Recurso principal | email, SMS, push, somente correspondência direta |
| Mensagens transacionais | GA | Todas as ofertas básicas | Recurso principal | email, push, SMS; incluído em cada oferta básica |

>[!TAB IA e conteúdo]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Seletor do Assessor de conteúdo | GA | Todas as ofertas básicas | 19 de maio de 2026 | Pesquisa semântica de IA para ativos e fragmentos |
| Integrações (fontes de dados de terceiros) | GA | Todas as ofertas básicas | 4 de maio de 2026 | Anteriormente Beta |
| Restringir quebra de herança em fragmentos | GA | Todas as ofertas básicas | 21 de maio de 2026 | Bloquear fragmentos em edições locais |
| Integração do Adobe Express | GA | Todas as ofertas básicas | 23 de abril de 2026 | Anteriormente: LA |
| Assistente de IA para expressões de personalização | GA | Todas as ofertas básicas | 13 de abril de 2026 | No editor de personalização e no Email Designer |
| Converter imagens em modelos de conteúdo de email | GA | Todas as ofertas básicas | 31 de março de 2026 | Anteriormente: LA |
| Formulários personalizados de página de destino | GA | Todas as ofertas básicas | 26 de março de 2026 | Anteriormente LA (EUA e Austrália) |
| Integração de modelos de imagem personalizados do Firefly e de terceiros | GA | Todas as ofertas básicas | 2 de março de 2026 | Adobe, Partner (Gemini) e modelos personalizados |
| Editor avançado de HTML para modelos de email | LA | Todas as ofertas básicas | 10 de março de 2026 | Enviar modelos de conteúdo por e-mail somente; entrar em contato com seu representante |
| Modo de email de especialista no conteúdo de email | LA | Todas as ofertas básicas | 9 de abril de 2026 | Entre em contato com seu representante da Adobe |
| Temas do Designer de email | LA | Todas as ofertas básicas | 5 de novembro de 2025 | Anteriormente Beta; entre em contato com seu representante |
| Designer de email (arrastar e soltar) | GA | Todas as ofertas básicas | Recurso principal | Criação no Visual e no HTML |
| Fragmentos de conteúdo | GA | Todas as ofertas básicas | Recurso principal | Blocos de conteúdo reutilizáveis |
| Modelos de conteúdo | GA | Todas as ofertas básicas | Recurso principal | — |
| editor do Personalization | GA | Todas as ofertas básicas | Recurso principal | Personalização baseada em expressão |
| Assistente de IA para geração de conteúdo | GA | Todas as ofertas básicas | Recurso principal | Exige termos de licenciamento de IA |

>[!TAB Decisão]

Todos os recursos do Decisioning exigem o complemento **Decisioning**. Consulte [Pacotes e recursos](ajo-packages.md).

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Suporte ao Serviço de decisão no canal de correspondência direta | GA | Todas as ofertas básicas | 3 de junho de 2026 | Oferece suporte à decisão em lote |
| Otimização das regras de decisão e da fórmula de classificação usando IA | GA | Todas as ofertas básicas | 5 de maio de 2026 | Simplificações sugeridas por IA |
| Apoio à decisão no canal de email | GA | Todas as ofertas básicas | 6 de abril de 2026 | Páginas espelhadas compatíveis |
| Monitoramento de modelo de IA | GA | Todas as ofertas básicas | 9 de março de 2026 | Somente modelos de otimização personalizados |
| Apoio à decisão no canal de SMS | GA | Todas as ofertas básicas | 2 de fevereiro de 2026 | — |
| Apoio à decisão no canal de push | GA | Todas as ofertas básicas | 30 de janeiro de 2026 | — |
| Fragmentos de conteúdo do Adobe Experience Manager na Decisão | LA | Todas as ofertas básicas | 20 de maio de 2026 | Entre em contato com seu representante da Adobe |
| Offer Decisioning (políticas de decisão) | GA | Todas as ofertas básicas | Recurso principal | Seleção da melhor oferta em tempo real |
| Classificação baseada em IA | GA | Todas as ofertas básicas | Recurso principal | Otimização da oferta de aprendizado de máquina |

>[!TAB Agentes de IA]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Journey Agent: criar uma jornada | GA | Jornada; Campanhas e Jornadas | terça-feira, 12 de janeiro de 2026 | Criação de jornada em linguagem natural |
| Integração do Journey Optimizer AI Agent via MCP | Beta | Todas as ofertas básicas | Abril de 2026 | Beta público; Claude Web e desktop |
| Journey Agent: criação de conteúdo do canal | LA | Todas as ofertas básicas | 4 de março de 2026 | Entre em contato com seu representante da Adobe |

>[!TAB Administração e dados]

| Recurso | Status | Aplicável a | Disponível desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Autenticação personalizada baseada em certificado em ações personalizadas | GA | Todas as ofertas básicas | 4 de junho de 2026 | Para identidade baseada em certificado (por exemplo, Microsoft Entra ID) |
| Alertas do cliente para eventos de ciclo de vida da campanha | GA | Todas as ofertas básicas | 1 de junho de 2026 | Assinar no nível da sandbox |
| Criptografia de parâmetro de URL | GA | Todas as ofertas básicas | 1 de junho de 2026 | Anteriormente, o LA; precisa de permissões de registro de chaves |
| APIs de ferramentas de migração de autoatendimento | GA | Todas as ofertas básicas | 3 de fevereiro de 2026 | — |
| Monitoramento de ação personalizado | GA | Todas as ofertas básicas | 3 de fevereiro de 2026 | Anteriormente: LA |
| Exportação de mensagem | GA | Todas as ofertas básicas | 28 de janeiro de 2026 | Disponível como um complemento |
| API de recuperação da campanha de ação | GA | Todas as ofertas básicas | 24 de novembro de 2025 | — |
| Migrar subdomínios para delegação personalizada | LA | Todas as ofertas básicas | 19 de fevereiro de 2026 | Entre em contato com seu representante da Adobe |
| Sandboxes | GA | Todas as ofertas básicas | Recurso principal | Até 5 sandboxes; disponíveis adicionais |
| Perfis e públicos unificados | GA | Todas as ofertas básicas | Recurso principal | Baseado em Adobe Experience Platform |
| Relatórios e relatórios ao vivo | GA | Todas as ofertas básicas | Recurso principal | — |
| Permissões e controle de acesso | GA | Todas as ofertas básicas | Recurso principal | Acesso baseado em função |
| REST APIs | GA | Todas as ofertas básicas | Recurso principal | Estrutura API-first |

>[!ENDTABS]

>[!NOTE]
>
>Esta lista foi compilada das [notas de versão de 2026](../rn/release-notes-2026.md) e das [notas de versão atuais](../rn/release-notes.md) e reflete o status mais recente conhecido de cada recurso. Não é exaustivo. Para obter o histórico completo e as adições mais recentes, sempre verifique as [notas de versão](../rn/release-notes.md).

## Recursos relacionados {#related}

- **Entenda o que há em seu pacote** — [Pacotes e recursos](ajo-packages.md)
- **Ver tudo que foi enviado** — [Notas de versão](../rn/release-notes.md) | [notas de versão de 2026](../rn/release-notes-2026.md)
- **Introdução** — [Introdução ao Journey Optimizer](get-started.md)
