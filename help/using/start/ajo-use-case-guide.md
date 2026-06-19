---
solution: Journey Optimizer
product: journey optimizer
title: Visão geral dos casos de uso do Journey Optimizer | ADOBE JOURNEY OPTIMIZER
description: Descubra os principais casos de uso para os quais a Adobe Journey Optimizer foi projetada, com orientações sobre quais recursos da AJO se encaixam melhor em cada cenário.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: Otimizador de jornadas, caso de uso, guia de decisão, qual recurso, introdução, objetivos de profissionais, tutoriais
source-git-commit: 3c737f88116a28ef217b53f95754504f537b3cd0
workflow-type: tm+mt
source-wordcount: '3310'
ht-degree: 32%

---

# Encontre a capacidade certa do Journey Optimizer para sua meta {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**Nesta página:** comece pelo que você deseja realizar e vá para o recurso do Adobe Journey Optimizer que o resolve, sem precisar saber o nome do recurso primeiro.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] oferece muitos recursos, e o correto depende do que você está tentando alcançar. Este guia é organizado em torno de metas comerciais, em vez de recursos do produto: encontre a meta que corresponda a sua necessidade e, em seguida, siga o link para começar com o recurso recomendado.

Use esta página como um roteador rápido — verifique sua meta e vá direto para o recurso certo. Se você está apenas começando, comece com [Comece a usar o Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) para encontrar o ponto de entrada correto para sua função.

>[!NOTE]
>
>Para obter amostras passo a passo de implementação, consulte a [biblioteca de casos de uso do Jornada](../building-journeys/jo-use-cases.md).

Quando um tutorial completo não está disponível para um cenário específico, o link direciona você ao melhor ponto de partida atual para conhecer o recurso e começar.

A IA está incorporada em muitos desses recursos — procure a tag **(AI)** nas tabelas abaixo. O conversacional [Assistente de IA](ai-features.md#ai-assistant) também pode responder perguntas sobre produtos e exibir insights operacionais sobre suas jornadas a qualquer momento. Para obter o conjunto completo de recursos inteligentes, consulte [IA e recursos inteligentes](ai-features.md).

>[!TIP]
>
>Novo no Journey Optimizer? Comece com [Comece a usar o Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) para escolher o caminho certo para sua função e leia [O que é o Journey Optimizer](get-started.md) para o básico. Para criar confiança prática, navegue pelos [tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}, siga uma [lista de reprodução de vídeo](https://experienceleague.adobe.com/pt-br/playlists?solution=Journey+Optimizer){target="_blank"} com curadoria de especialista e pratique em uma [sandbox de treinamento](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} ou com os [desafios práticos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}.

## Configurar o Journey Optimizer para a sua equipe {#setup-admin}

Para administradores e usuários técnicos que precisam configurar o ambiente antes de criar jornadas ou campanhas.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Configurar canais de email, SMS ou push antes de enviar | Configuração de canais | [Introdução à configuração de canal](../configuration/get-started-configuration.md) |
| Aqueça um novo endereço IP para envio de email | Plano de aquecimento de IP | [Introdução ao aquecimento de IP](../configuration/ip-warmup-gs.md) |
| Configurar funções, permissões e controle de acesso | Controle de acesso | [Introdução ao controle de acesso](../administration/permissions-overview.md) |
| Trabalhe em vários ambientes ou regiões | Sandboxes | [Trabalhar com sandboxes](../administration/sandboxes.md) |

## Envolva os clientes em tempo real {#engage-real-time}

Para cenários em que você reage a uma ação ou evento do cliente conforme ele ocorre.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Dê as boas-vindas a um novo cliente ou assinante automaticamente | Jornada acionada por evento | [Introdução ao jornada](../building-journeys/journey-gs.md) · [Introdução à criação de uma jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de compilar:** verifique se você tem (1) um [evento de entrada de jornada configurado](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configure-journeys/events-journeys/about-events) para capturar o disparador de inscrição, (2) uma [superfície de canal de email ou push](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/channel-surfaces) configurada para sua sandbox e (3) pelo menos um [perfil de teste](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles) disponível para validar a jornada antes de publicar.

>[!ENDSHADEBOX]

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Recuperar um carrinho abandonado ou procurar uma sessão | Jornada acionada por evento | [Introdução ao jornada](../building-journeys/journey-gs.md) · [Tutorial de navegação abandonada](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de criar:** você precisa (1) de um [evento comportamental](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configure-journeys/events-journeys/about-events) que capture o carrinho ou a ação de navegação de sua Web ou SDK móvel, (2) de uma estratégia de [atividade de espera](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/wait-activity) decidida (normalmente uma a quatro horas antes da primeira chamada de atenção) e (3) de uma superfície de canal pronta para a mensagem de acompanhamento. Observação: a jornada deve incluir uma condição para sair dos perfis que concluíram a compra antes do fim do período de espera.

>[!ENDSHADEBOX]

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Acionar uma jornada a partir do envio de um formulário de site | Jornada acionada por evento | [Introdução ao jornada](../building-journeys/journey-gs.md) · [Tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| Reagir ao comportamento no aplicativo (aplicativo aberto, exibição de tela) | Jornada + No aplicativo | [Introdução ao No aplicativo](../in-app/get-started-in-app.md) |
| Enviar confirmações de pedido, remessa ou compromisso | Campanha acionada por API | [Trabalhar com campanhas acionadas por API](../campaigns/api-triggered-campaigns.md) |
| Reengajamento de clientes inativos ou antigos | Jornada + públicos | [Introdução a perfis e públicos](../audience/get-started-profiles.md) · [Criar públicos usando o construtor de regras](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de criar:** você precisa (1) de um [público-alvo definido no Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences) que identifique perfis inativos (por exemplo, nenhuma compra ou logon em 60 dias), (2) de uma decisão sobre o canal de reengajamento (email, push ou SMS) e (3) de uma regra de supressão ou [limite de frequência](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/conflict-prioritization/capping-rules/channel-capping) para evitar contatar perfis com mensagens recentes. Use uma entrada de jornada **Ler Público** — não um evento — para este cenário.

>[!ENDSHADEBOX]

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Testar uma jornada com dados reais antes de ativá-la | Jornada simulação | [Testar sua jornada com simulação](../building-journeys/journey-dry-run.md) |
| Pausar uma jornada em tempo real para fazer edições sem interromper perfis em andamento | Jornada pausa e retomar | [Pausar e retomar uma jornada](../building-journeys/journey-pause.md) |
| Criar ou otimizar uma jornada a partir de um prompt em linguagem natural | Journey Agent **(IA)** | [Agentes de IA](ai-features.md#ai-agents) · [Tutorial do Journey Agent](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## Alcance públicos-alvo em escala {#reach-at-scale}

Para alcance agendado de um para muitos para um público-alvo definido.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Enviar um informativo ou uma promoção a um segmento | Campanha programada | [Introdução às campanhas](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**Antes de compilar:** você precisa (1) de um [segmento de público-alvo publicado](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences) no Adobe Experience Platform, (2) de uma [superfície de canal de email](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/channel-surfaces) com um domínio de envio verificado e (3) de quaisquer [fragmentos de conteúdo ou modelos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/fragments/fragments) que você planeje reutilizar já publicados. As campanhas programadas são a escolha certa aqui, não as jornadas, se for um envio único ou recorrente sem lógica de ramificação.

>[!ENDSHADEBOX]

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Iniciar um produto com um teste A/B | Experimentação de conteúdo **(AI)** | [Introdução à experimentação de conteúdo](../content-management/experiment-accelerator-gs.md) · [Criar experimentos de conteúdo para campanhas de email](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| Notificar os clientes sobre uma interrupção ou atualização de serviço | Campanha programada + públicos-alvo | [Sobre públicos-alvo](../audience/about-audiences.md) |
| Criar uma campanha em várias etapas com lógica de ramificação | Campanhas orquestradas | [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |
| Direcionar somente perfis que foram alterados desde a última execução da campanha | Campanhas orquestradas — query incremental | [Criar consultas em campanhas orquestradas](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| Verificar quantos perfis correspondem ao meu público-alvo antes de iniciar | Visualização de público | [Sobre públicos-alvo](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| Coordenar mensagens em vários canais em escala | Orquestração | [Dimensionamento de orquestração para engajamento onicanal](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| Envie cada mensagem na melhor hora para cada cliente | Otimização de hora de envio **(AI)** | [Otimização de tempo de envio](../building-journeys/send-time-optimization.md) |

## Personalize o que cada cliente vê {#personalize}

Para personalizar ofertas e conteúdo para cada indivíduo.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Mostrar a melhor oferta para cada cliente | Tomada de decisão | [Introdução ao Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) · [Tutorial de ofertas da Web](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**Antes de compilar:** a decisão requer uma sequência de configuração específica. Você precisa (1) [de itens de decisão (ofertas) criados](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/items) com regras de qualificação e atributos, (2) uma [estratégia de seleção](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/experience-decisioning-selection/selection-strategies) ou fórmula de classificação configurada e (3) uma [política de decisão](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/experience-decisioning/decision-policies/create-decision) anexada à superfície onde as ofertas serão exibidas. Ignorar essa sequência é o motivo mais comum para as configurações da primeira decisão não retornarem resultados.

>[!ENDSHADEBOX]

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Classifique as ofertas usando uma fórmula (código postal, renda, clima) | Decisão — fórmula de classificação | [Tutorial de fórmula de classificação](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [Tutorial de dados meteorológicos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| Usar produto externo ou dados de CRM para personalizar ofertas | Decisão — Pesquisa de conjunto de dados do AEP | [Usar pesquisa de conjunto de dados na decisão](../experience-decisioning/context-data.md) |
| Personalizar o conteúdo da mensagem com os dados do perfil | Personalização | [Personalizar seu conteúdo](../personalization/personalize.md) |
| Gerar variações de cópia, imagens e mensagem | Geração de conteúdo de IA **(AI)** | [Geração de conteúdo de IA](../content-management/gs-generative.md) · [Tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| Converter uma imagem de design em um modelo de email editável | Conversor de imagem para HTML **(AI)** | [Converter uma imagem em um modelo de email](../content-management/image-to-html.md) |
| Classificar e personalizar ofertas automaticamente | Modelos de classificação de IA **(AI)** | [Modelos de IA para decisão](../experience-decisioning/ranking/ai-models.md) |
| Fornecer conteúdo contextual sempre ativo (sem campanha) | Cartões de conteúdo | [Introdução a cartões de conteúdo](../content-card/get-started-content-card.md) · [Criar cartões de conteúdo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| Forneça conteúdo personalizado via API para qualquer aplicativo ou superfície | Experiência baseada em código | [Introdução à experiência baseada em código](../code-based/get-started-code-based.md) |
| Controlar quais partes de um modelo de email minha equipe pode editar | Bloqueio de conteúdo | [Bloquear conteúdo em modelos de email](../content-management/content-locking.md) |

## Coordenar e administrar a entrega {#coordinate-govern}

Para controlar como, quando e com que frequência os clientes são contatados entre canais.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Evitar a fadiga da mensagem entre canais | Limite de frequência | [Definir limite de frequência por canal](../conflict-prioritization/channel-capping.md) |
| Resolver mensagens conflitantes ou concorrentes | Priorização de conflito | [Identificar possíveis conflitos](../conflict-prioritization/conflicts.md) · [Tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| Decidir qual jornada tem prioridade | Arbitragem de jornada | [Usar fórmulas para classificar jornadas](../conflict-prioritization/journey-ranking-formulas.md) |
| Respeitar horários de silêncio e consentimento | Quiet hours / Privacidade | [Definir horas de silêncio](../conflict-prioritization/quiet-hours.md) |
| Aplicar políticas de consentimento e rótulos de uso de dados em canais | Consentimento e governança de dados | [Introdução à privacidade](../privacy/get-started-privacy.md) |
| Receber alerta quando uma jornada tiver altas taxas de erro ou descarte | Jornada alertas | [Configurar alertas de jornada](../reports/alerts.md) |

## Escolha um canal no qual entregar {#choose-channel}

| Eu quero enviar em... | Canal | Comece aqui |
| --- | --- | --- |
| Enviar por email informativos, promoções ou mensagens transacionais | Email | [Introdução ao email](../email/get-started-email.md) |
| Notificações por push de dispositivos móveis (iOS e Android) | Push | [Introdução às notificações por push](../push/get-started-push.md) |
| Mensagens de texto SMS, MMS ou RCS | SMS/MMS/RCS | [Introdução a SMS/MMS/RCS](../mobile/get-started-mobile.md) · [Hub de Aprendizado Móvel](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| Mensagens do WhatsApp por meio da API da Meta Cloud | WhatsApp | [Começar a usar o WhatsApp](../whatsapp/get-started-whatsapp.md) |
| Sobreposições e banners no navegador ou no aplicativo | No aplicativo | [Introdução ao No aplicativo](../in-app/get-started-in-app.md) |
| Conteúdo personalizado da página da Web | Web | [Introdução ao canal Web](../web/get-started-web.md) |
| Qualquer superfície via API (quiosque, dispositivo conectado, aplicativo headless) | Experiência baseada em código | [Introdução à experiência baseada em código](../code-based/get-started-code-based.md) |
| Partes de email físico acionadas a partir de uma jornada | Correspondência direta | [Introdução à correspondência direta](../direct-mail/get-started-direct-mail.md) |

## Medir e otimizar {#measure-optimize}

Para rastrear o desempenho, diagnosticar problemas e melhorar os resultados ao longo do tempo.

| Eu quero... | Capacidade recomendada | Comece aqui |
| --- | --- | --- |
| Consulte as métricas de desempenho para uma jornada ou campanha em tempo real | Relatórios ao vivo | [Relatórios ao vivo](../reports/live-report.md) · [Monitore e analise sua jornada com relatórios ao vivo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| Relatar o desempenho completo da campanha ou da jornada após o término | Relatórios globais | [Introdução aos relatórios](../reports/gs-reports.md) |
| Analisar um experimento e obter recomendações para a próxima etapa | Experimentation Agent **(IA)** | [Experimentation Agent](ai-features.md#experimentation-agent) · [Tutorial](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| Monitorar a integridade e a latência de ações personalizadas em minhas jornadas | Monitoramento de ação personalizado | [Usar ações personalizadas](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| Receber alerta quando as taxas de erro de jornada ou descarte excederem os limites | Jornada alertas | [Configurar alertas de jornada](../reports/alerts.md) |

## Fluxos iniciais {#starter-flows}

Cada fluxo inicial abaixo é um conjunto de etapas curto e orientado por resultados: para que você construirá, para quem é e como chegar lá. Escolha a meta que corresponde ao primeiro projeto e siga os links para a documentação detalhada.

### Dê as boas-vindas a novos clientes {#flow-welcome}

**Você criará:** uma série de boas-vindas automatizada que saúda cada novo assinante e estimula os assinantes inativos.
**Recomendado para:** Profissionais de marketing · **Recurso:** jornada acionada por evento

1. Confirme se os [perfis e públicos-alvo unificados](../audience/get-started-profiles.md) estão recebendo o evento de inscrição.
1. [Crie sua primeira jornada](../building-journeys/journey-gs.md) e use o evento de inscrição como entrada.
1. Adicione um [email](../email/get-started-email.md) de boas-vindas, uma etapa de espera e uma [notificação por push](../push/get-started-push.md) de acompanhamento para perfis que não estejam envolvidos.
1. [Personalize o conteúdo](../personalization/personalize.md) com atributos de perfil, como nome e interesses declarados.

➡️ [Iniciar com jornadas](../building-journeys/journey-gs.md)

### Recuperar carrinhos abandonados {#flow-cart}

**Você compilará:** um fluxo de recuperação em tempo real que lembra aos clientes os itens deixados para trás.
**Recomendado para:** Profissionais de marketing · **Recurso:** jornada acionada por evento

1. Certifique-se de que o evento de abandono do carrinho chegue à Journey Optimizer (trabalhe com sua [equipe de dados](../data/gs-data.md), se necessário).
1. [Criar uma jornada](../building-journeys/journey-gs.md) acionada pelo evento de abandono.
1. Envie um email de lembrete personalizado. Se não houver clique em 24 horas, ramifique para um acompanhamento de [push](../push/get-started-push.md).
1. [Personalize](../personalization/personalize.md) com os itens abandonados e o status de fidelidade.

➡️ [Iniciar com jornadas](../building-journeys/journey-gs.md)

### Enviar mensagens transacionais {#flow-transactional}

**Você compilará:** Confirmações de pedidos, remessas ou compromissos sob demanda disparadas por um sistema externo.
**Recomendado para:** Profissionais de marketing e desenvolvedores · **Recurso:** Campanha acionada por um sistema externo

1. Revise como [campanhas acionadas por um sistema externo](../campaigns/api-triggered-campaigns.md) funcionam e qual carga eles esperam.
1. Crie o modelo de mensagem e [personalize](../personalization/personalize.md) com os detalhes da transação.
1. Peça ao desenvolvedor para chamar o endpoint da campanha a partir do seu pedido ou sistema de atendimento.

➡️ [Trabalhar com campanhas acionadas por um sistema externo](../campaigns/api-triggered-campaigns.md)

### Iniciar uma campanha com teste de conteúdo {#flow-campaign}

**Você compilará:** uma promoção agendada que escolhe automaticamente o conteúdo com melhor desempenho.
**Recomendado para:** Profissionais de marketing · **Recurso:** Campanha agendada + experimentação de conteúdo

1. [Comece com campanhas](../campaigns/get-started-with-campaigns.md) e defina seu público.
1. Use a [geração de conteúdo](../content-management/gs-generative.md) para rascunhar variações de linha de assunto e cópia.
1. Configure um [experimento de conteúdo](../content-management/experiment-accelerator-gs.md) para testar variantes em uma amostra e, em seguida, envie o vencedor para o resto.

➡️ [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Personalizar ofertas por cliente {#flow-offers}

**Você criará:** uma decisão que mostra a melhor oferta para cada cliente.
**Recomendado para:** Profissionais de marketing · **Funcionalidade:** Decisão

1. [Comece a usar o Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) e crie suas ofertas e regras de qualificação.
1. Adicione a decisão a uma [jornada](../building-journeys/journey-gs.md) ou mensagem de campanha.
1. Camada em [recursos inteligentes](ai-features.md) para classificar e otimizar ofertas automaticamente.

➡️ [Introdução ao Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Exemplos de cenários {#example-scenarios}

Estes exemplos ilustram como os recursos do Journey Optimizer trabalham em conjunto em diferentes funções, setores e canais.

### Recuperação de remessa atrasada {#scenario-delayed-shipment}

**Função:** profissional de marketing | **Recurso principal:** [perfil unificado + exclusão de público-alvo](../audience/get-started-profiles.md)

Normalmente, uma loja de roupas envia pesquisas de satisfação pós-compra a todos os clientes que compraram produtos na última semana. Devido às intempéries, alguns carregamentos sofreram atrasos. Ao ver quais clientes não receberam suas remessas, a loja de roupas pode excluir essas pessoas do envio agendado da pesquisa de satisfação do cliente e, em vez disso, enviar um email personalizado pedindo desculpas pelo atraso e oferecendo um código de desconto com recomendações de produto baseadas em suas compras anteriores.

[Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Engajamento na loja em tempo real {#scenario-instore}

**Função:** profissional de marketing | **Recurso principal:** [Acionamento de geofence + push](../push/get-started-push.md)

O mesmo varejista pode interagir em tempo real com um cliente fiel que chega ao estacionamento da loja, enviando uma notificação por push sobre um suéter que voltou ao estoque no tamanho desejado.

[Introdução às notificações por push](../push/get-started-push.md)

### Recuperação de abandono de carrinho {#scenario-cart}

**Função:** profissional de marketing | **Recurso principal:** [jornada de várias etapas acionada por eventos](../building-journeys/journey-gs.md)

Quando um cliente adiciona itens a um carrinho online, mas sai sem concluir a compra, o Journey Optimizer detecta o evento em tempo real e inicia uma jornada de recuperação automaticamente. O cliente recebe um email personalizado lembrando sobre os itens deixados para trás. Se ele não clicar no dentro de 24 horas, uma notificação por push de acompanhamento será enviada, personalizada com base no histórico de navegação e no status de fidelidade.

[Crie a primeira jornada](../building-journeys/journey-gs.md)

### Série de boas-vindas do serviço de streaming {#scenario-welcome}

**Função:** profissional de marketing | **Recurso principal:** [jornada de boas-vindas acionada por evento](../building-journeys/journey-gs.md)

Quando um cliente assina um serviço de streaming, o Journey Optimizer detecta o evento de inscrição e inicia imediatamente uma jornada de boas-vindas de várias etapas. O cliente recebe um email de boas-vindas incentivando-o a abrir o aplicativo pela primeira vez. Se nenhuma atividade de logon for detectada em 48 horas, uma notificação por push de acompanhamento é enviada com recomendações de conteúdo personalizadas com base em seus interesses declarados durante a inscrição, transformando um assinante passivo em um usuário ativo e engajado desde o primeiro dia.

[Crie a primeira jornada](../building-journeys/journey-gs.md)

### Lembrete de reserva com instruções {#scenario-reservation}

**Função:** profissional de marketing | **Recurso principal:** [mensagens agendadas + com reconhecimento de local](../campaigns/get-started-with-campaigns.md)

Uma marca de hospitalidade envia a cada hóspede um lembrete oportuno uma hora antes de sua reserva. A notificação inclui o nome do hóspede, o horário da reserva e as indicações de como chegar ao local com base na localização, tudo isso reunido automaticamente a partir do perfil do cliente e dos dados da reserva, sem qualquer intervenção manual da equipe de marketing.

[Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Notificação proativa de interrupção de serviço {#scenario-outage}

**Função:** operações | **Recurso principal:** [seleção automática de público-alvo em grande escala](../audience/about-audiences.md)

Quando ocorre uma interrupção do serviço, o Journey Optimizer identifica automaticamente os clientes afetados com base nos dados da conta e nos padrões de uso. Esses clientes recebem uma notificação proativa confirmando o problema e descrevendo as próximas etapas, transformando uma experiência potencialmente negativa em um momento de transparência e confiança, entregue em grande escala.

[Crie a primeira jornada](../building-journeys/journey-gs.md)

### Campanha promocional inteligente {#scenario-ai-campaign}

**Função:** Profissional de marketing | **Recurso principal:** [Geração de conteúdo + experimentação](ai-features.md)

Um planejamento de marca de varejo em um lançamento de produto usa o Assistente de IA do Journey Optimizer para gerar variações de linha de assunto e texto em minutos, orientadas por um prompt de linguagem natural e suas diretrizes de marca carregadas. A experimentação de conteúdo integrada identifica automaticamente a variante com melhor desempenho entre uma amostra de público-alvo inicial. A mensagem vencedora é implantada nos destinatários restantes, maximizando o engajamento sem esforço adicional de redação.

[Explorar recursos inteligentes](ai-features.md) | [Saiba mais sobre a experimentação de conteúdo](../content-management/experiment-accelerator-gs.md)

### Alertas de manutenção por meio de aplicativo móvel {#scenario-maintenance}

**Função:** operações | **Recurso principal:** [orquestração de jornadas que não são de marketing](../building-journeys/journey-gs.md)

Profissionais que não atuam no marketing, como equipes de operações e suporte ao cliente, podem usar o [!DNL Adobe Journey Optimizer] para gerenciar notificações operacionais ou monitorar processos de integração. Por exemplo, um parque de diversões onde os visitantes baixam um aplicativo móvel como parte da experiência: a equipe de manutenção pode usar o Journey Optimizer para notificar os visitantes sobre as atrações que estão fechadas atualmente devido à manutenção.

[Crie a primeira jornada](../building-journeys/journey-gs.md)

## Biblioteca de vídeos {#videos}

Navegue por conteúdo de vídeo preparado por tópico. Cada guia está vinculada aos tutoriais e listas de reprodução relevantes no Experience League.

>[!BEGINTABS]

>[!TAB Introdução]

* [Introdução ao Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Conceitos principais e um tour pelo produto.
* [Visão geral dos tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — o catálogo completo de vídeos guiados.

>[!TAB Jornadas e campanhas]

* [Introdução à criação de uma jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Crie sua primeira jornada acionada por evento.
* [Criar jornadas com o Journey Agent](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — Crie jornadas a partir de um prompt em linguagem natural.

>[!TAB Personalization e inteligência]

* [Assistente de IA para geração de conteúdo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — Gerar cópia, imagens e variações.
* [Use o decisioning para personalizar ofertas da Web](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Personalize ofertas por cliente.

>[!TAB Relatórios e otimização]

* [Monitore e analise sua jornada com relatórios ao vivo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — Acompanhe o desempenho em tempo real.
* [Criar experimentos de conteúdo para campanhas de email](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Testar e otimizar conteúdo.

>[!ENDTABS]

## Escolha entre jornadas, campanhas e campanhas orquestradas {#choosing}

| Cenário | Usar |
|----------|-----|
| Orientado ao comportamento, em várias etapas, cada cliente se move em seu próprio ritmo | Jornada |
| Mensagem agendada simples ou acionada por API para um público-alvo | Campaign |
| Fluxo de trabalho de lote complexo com segmentação de várias entidades | Campanha orquestrada |

## Não tem certeza? {#not-sure}

Se sua meta mapear para um termo com o qual você não está familiarizado, ou se você não tiver certeza sobre qual recurso a tabela aponta, comece com a [terminologia da chave do Journey Optimizer](terminology.md) página para esclarecer os conceitos por trás de cada recurso.

Você também pode criar confiança prática com os exercícios completos nos [tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
