---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: Descubra os principais recursos e casos de uso do Adobe Journey Optimizer
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: jornada otimizer, o que é o ajo, adobe jornada otimizer, introdução, omnicanal, personalização, jornada do cliente
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: cccc064de7f05b6502c54ae539b4cf1cc722f212
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 14%

---

# Introdução ao Journey Optimizer {#cjm-gs}

Esta página apresenta o Adobe Journey Optimizer: para que ele é, para quem ele serve, seus principais recursos e como ele se encaixa na arquitetura do Adobe Experience Platform. É o ponto de partida recomendado para novos usuários.

## O que é o [!DNL Adobe Journey Optimizer]?{#about-cjm}

O [!DNL Adobe Journey Optimizer] é um aplicativo corporativo para criar e fornecer experiências conectadas, contextuais e personalizadas ao cliente em todos os canais e pontos de contato. Ele é construído nativamente no [!DNL Adobe Experience Platform] e aproveita um perfil de cliente em tempo real unificado, uma estrutura aberta de priorização de API, um Offer Decisioning centralizado e recursos de IA/ML. O Journey Optimizer permite que as marcas orquestrem campanhas de marketing programadas e comunicações acionadas por eventos em tempo real — a partir de um único aplicativo, em escala. O resultado são experiências de marca significativas que aumentam a fidelidade do cliente e o valor vitalício.

Este guia se aplica a profissionais de marketing, equipes de operações e administradores novatos no Journey Optimizer.

➡️ [Descubra o Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=pt-BR){target="_blank"} (vídeo)


<!--
 Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.
-->


## Casos de uso {#use-cases}

Estes exemplos ilustram como os recursos do Journey Optimizer trabalham em conjunto em diferentes funções, setores e canais.

### Recuperação de remessa atrasada {#uc-delayed-shipment}

**Função:** Profissional de marketing | **Recurso principal:** [Perfil unificado + exclusão de público-alvo](../audience/get-started-profiles.md)

Uma loja de roupas normalmente envia pesquisas pós-compra para todos os clientes que compraram produtos na última semana. Devido às intempéries, alguns carregamentos sofreram atrasos. Ao ver quais clientes não receberam suas remessas, a loja de roupas pode excluir essas pessoas do envio agendado da pesquisa de satisfação do cliente e, em vez disso, enviar um email personalizado pedindo desculpas pelo atraso e oferecendo um código de desconto com recomendações de produto baseadas em suas compras anteriores.

[Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Engajamento na loja em tempo real {#uc-instore}

**Função:** Profissional de marketing | **Recurso principal:** [Acionamento por geofence + push](../push/get-started-push.md)

O mesmo retailer pode engajar um cliente fiel que entra no estacionamento da loja em tempo real enviando a ele uma notificação por push sobre um suéter que está de volta em estoque no tamanho do cliente.

[Introdução às notificações por push](../push/get-started-push.md)

### Recuperação de abandono do carrinho {#uc-cart}

**Função:** Profissional de marketing | **Recurso principal:** [jornada de várias etapas acionada por eventos](../building-journeys/journey-gs.md)

Quando um cliente adiciona itens a um carrinho on-line, mas sai sem concluir a compra, o Journey Optimizer detecta o evento em tempo real e inicia uma jornada de recuperação automaticamente. O cliente recebe um email personalizado lembrando sobre os itens deixados para trás. Se ele não clicar no dentro de 24 horas, uma notificação por push de acompanhamento será enviada — personalizada com base no histórico de navegação e no status de fidelidade.

[Crie sua primeira jornada](../building-journeys/journey-gs.md)

### Série de boas-vindas do serviço de streaming {#uc-welcome}

**Função:** Profissional de marketing | **Recurso principal:** [jornada de boas-vindas acionada por evento](../building-journeys/journey-gs.md)

Quando um cliente assina um serviço de transmissão, o Journey Optimizer detecta o evento de inscrição e inicia imediatamente uma jornada de boas-vindas de várias etapas. O cliente recebe um email de boas-vindas incentivando-o a abrir o aplicativo pela primeira vez. Se nenhuma atividade de logon for detectada em 48 horas, uma notificação por push de acompanhamento será enviada com recomendações de conteúdo personalizadas com base em seus interesses declarados durante a inscrição — transformando um assinante passivo em um usuário ativo e engajado desde o primeiro dia.

[Crie sua primeira jornada](../building-journeys/journey-gs.md)

### Lembrete de reserva com direções {#uc-reservation}

**Função:** Profissional de marketing | **Recurso principal:** [Mensagens agendadas + com reconhecimento de local](../campaigns/get-started-with-campaigns.md)

Uma marca de hospitalidade envia a cada hóspede um lembrete oportuno uma hora antes de sua reserva. A notificação inclui o nome do convidado, o tempo de reserva e as direções baseadas na localização para o local — automaticamente montadas a partir do perfil do cliente e dos dados de reserva, sem esforço manual da equipe de marketing.

[Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Notificação de interrupção proativa do serviço {#uc-outage}

**Função:** Operações | **Recurso principal:** [Seleção automática de público-alvo em escala](../audience/about-audiences.md)

Quando ocorre uma interrupção do serviço, a Journey Optimizer identifica automaticamente os clientes afetados com base nos dados da conta e nos padrões de uso. Esses clientes recebem uma notificação proativa confirmando o problema e descrevendo as próximas etapas — transformando uma experiência potencialmente negativa em um momento de transparência e confiança, entregue em escala.

[Crie sua primeira jornada](../building-journeys/journey-gs.md)

### Campanha promocional alimentada por IA {#uc-ai-campaign}

**Função:** Profissional de marketing | **Recurso principal:** [Geração de conteúdo de IA + experimentação](ai-features.md)

Um planejamento de marca de varejo em um lançamento de produto usa o Assistente de IA da Journey Optimizer para gerar várias variações de linha de assunto e cópia de corpo em minutos, orientadas por um prompt de linguagem natural e suas diretrizes de marca carregadas. A experimentação de conteúdo integrada identifica automaticamente a variante com melhor desempenho entre uma amostra de público-alvo inicial. A mensagem vencedora é então implantada nos recipients restantes, maximizando o engajamento sem esforço adicional de copywriting.

[Explorar recursos inteligentes e de IA](ai-features.md) | [Saiba mais sobre a experimentação de conteúdo](../content-management/experiment-accelerator-gs.md)

### Alertas de manutenção por meio de aplicativo móvel {#uc-maintenance}

**Função:** Operações | **Recurso principal:** [Orquestração de jornadas sem marketing](../building-journeys/journey-gs.md)

Os não profissionais de marketing, como as equipes de operações e suporte ao cliente, podem usar o [!DNL Adobe Journey Optimizer] para gerenciar notificações operacionais ou monitorar processos de integração. Por exemplo, um parque de diversões onde os visitantes baixam um aplicativo móvel como parte de sua experiência: a equipe de manutenção pode usar o Journey Optimizer para notificar os visitantes sobre as atrações que estão fechadas atualmente devido à manutenção.

[Crie sua primeira jornada](../building-journeys/journey-gs.md)


## Principais recursos {#key-capabilities}

O [!DNL Adobe Journey Optimizer] é um aplicativo ágil e escalonável para a criação e o fornecimento de experiências personalizadas, conectadas e oportunas ao cliente por meio de qualquer aplicativo, dispositivo ou canal.

![Diagrama que mostra as três principais áreas de recursos da Journey Optimizer: Insights e envolvimentos do cliente em tempo real, Orquestração e execução modernas do Omnichannel e Decisão inteligente e Personalization, tudo integrado no Adobe Experience Platform.](assets/ajo-capabilities.png)

Os principais recursos incluem:

### Insights e envolvimentos do cliente em tempo real

Um perfil integrado usa dados ao vivo de todas as fontes nos pontos de contato do cliente, incluindo dados comportamentais, transacionais, financeiros e operacionais para otimizar experiências pessoais e contextuais para os clientes em seu tempo. [Saiba mais sobre perfis e públicos](../audience/get-started-profiles.md)

### Orquestração e execução modernas do Omnichannel

Uma tela única na qual se pode harmonizar e otimizar a jornada do cliente para 1:1 de engajamento do cliente e alcance de marketing — para ajudar as marcas a agregar mais valor ao longo do ciclo de vida do cliente. As jornadas do cliente criadas no [!DNL Adobe Journey Optimizer] podem ser dinâmicas e baseadas em eventos para ajudar as marcas a reagir a sinais em tempo real, bem como conectar essas interações com campanhas agendadas, para que sejam tomadas as decisões corretas com respeito a quais comunicações devem ser enviadas a um cliente, quando e por quais canais. As ferramentas de criação de conteúdo incorporadas — incluindo um designer visual arrastar e soltar, modelos reutilizáveis, fragmentos de conteúdo e um editor de personalização — permitem que as equipes criem, personalizem e gerenciem mensagens para cada canal diretamente no mesmo fluxo de trabalho. [Criar a primeira jornada](../building-journeys/journey-gs.md) | [Projetar o conteúdo](../../rp_landing_pages/content-management-landing-page.md)

### Decisão inteligente e Personalization

As marcas podem aplicar decisões centralizadas e incorporar inteligência artificial e aprendizado de máquina para configurar insights preditivos no decorrer da experiência do cliente, facilitando a automatização das decisões e a otimização da experiência em escala. A Decisão possibilita ofertas centralizadas em canais em escala por meio do [!DNL Adobe Journey Optimizer]. [Explorar o Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) | [Descubra recursos de IA](ai-features.md)


## Disponibilidade e licenciamento {#availability}

Esta documentação abrange a versão atual do Journey Optimizer e se aplica a usuários B2C e B2B edition, salvo indicação em contrário. Os componentes e recursos disponíveis no ambiente dependem de suas [permissões](../administration/permissions.md) e do seu [pacote de licenciamento](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Em caso de dúvida, entre em contato com o(a) gerente de sucesso do cliente da Adobe ou com o(a) representante da Adobe.

As diretrizes e procedimentos gerais de privacidade da Adobe Experience Cloud se aplicam ao [!DNL Journey Optimizer]. [Saiba mais sobre a privacidade da Adobe Experience Cloud](https://www.adobe.com/br/privacy/experience-cloud.html){target="_blank"}.


## Arquitetura {#architecture}

O Journey Optimizer é construído nativamente na Adobe Experience Platform, compartilhando sua base de dados, seu gráfico de identidade e seus serviços de governança. Para obter uma apresentação detalhada sobre como esses sistemas funcionam juntos, consulte [Noções básicas sobre o Journey Optimizer](understanding-ajo.md).


>[!MORELIKETHIS]
>
>* [Etapas principais para iniciar](quick-start.md) — Guias de início rápido baseados em função para administradores, profissionais de marketing e engenheiros de dados.
>* [Introdução ao gerenciamento de dados](../data/gs-data.md) — Saiba como os dados são assimilados, unificados e ativados no Journey Optimizer.
>* [Crie jornadas e envie mensagens](../building-journeys/journey-gs.md) — Crie sua primeira jornada de cliente e configure as ações do canal.
>* [Relatórios ao vivo](../reports/live-report.md) — Monitore o desempenho da campanha e do jornada em tempo real.
>* [Tutorial de Introdução ao Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Uma apresentação guiada em vídeo dos principais conceitos do Journey Optimizer.
>* [Visão geral sobre a segurança do Journey Optimizer](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF) — Arquitetura de segurança, proteção de dados e detalhes de conformidade.
>* [Descrição do Produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} — Detalhamento oficial dos termos de licenciamento e recursos de edição.
