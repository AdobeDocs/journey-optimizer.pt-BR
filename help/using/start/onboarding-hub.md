---
solution: Journey Optimizer
product: journey optimizer
title: hub de integração do Journey Optimizer
description: Um hub de integração com curadoria para o Adobe Journey Optimizer que reúne instruções passo a passo, casos de uso reais e conteúdo de vídeo para que novos usuários possam crescer rapidamente e fornecer sua primeira experiência ao cliente.
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: jornada otimizer, integração, hub de integração, casos de uso, vídeos, tutoriais, introdução, aumento, primeira jornada
source-git-commit: 79337a0d2a65fa1e8aa1e5d47bcf39906d9887a7
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# hub de integração do Journey Optimizer {#onboarding-hub}


>[!BEGINSHADEBOX]

**Nesta página:** Acelere o Adobe Journey Optimizer rapidamente — assista a uma breve orientação, siga passo a passo as instruções para enviar sua primeira experiência, navegue em casos de uso reais e mergulhe em conteúdo de vídeo com curadoria.

>[!ENDSHADEBOX]

<!-- 
rebuild
-->

Novo em [!DNL Adobe Journey Optimizer]? Esse hub reúne os recursos que ajudam você a ir de zero até a sua primeira experiência ao vivo com instruções passo a passo para objetivos comuns, casos de uso reais que mostram o que é possível e conteúdo de vídeo com curadoria (tutoriais, apresentações e práticas práticas).

>[!TIP]
>
>Não tem certeza de qual recurso se encaixa em sua meta? Comece com a meta primeiro [Encontre a capacidade certa do Journey Optimizer para a meta](ajo-use-case-guide.md) do guia e volte aqui para obter instruções passo a passo.

## Comece aqui: assista e aprenda {#start-here}

Se você tiver dez minutos, comece com este vídeo de orientação. Ele aborda a interface do e destaca os principais recursos por função.

>[!VIDEO](https://video.tv.adobe.com/v/3430320?captions=por_br&quality=12)

Em seguida, crie confiança prática com estes recursos de aprendizagem:

* [Tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — vídeos passo a passo e apresentações guiadas para cada função.
* [Lista de reprodução de vídeo com curadoria especializada](https://experienceleague.adobe.com/pt-br/playlists?solution=Journey+Optimizer){target="_blank"} — Um conjunto sequenciado de pequenos vídeos para assistir em ordem.
* [Sandbox de treinamento](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} — um ambiente seguro com exemplos de dados para praticar.
* [Desafios práticos](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"} — aplique o que você aprende com exercícios guiados.

## Crie sua primeira experiência {#build-first}

Cada uma delas abaixo é um conjunto de etapas orientado a resultados: o que você vai construir, para quem é e como chegar lá. Escolha a meta que corresponde ao primeiro projeto e siga os links para a documentação detalhada.

### Dê as boas-vindas a novos clientes {#build-welcome}

**Você criará:** uma série de boas-vindas automatizada que saúda cada novo assinante e estimula os assinantes inativos.
**Recomendado para:** Profissionais de marketing · **Recurso:** jornada acionada por evento

1. Confirme se os [perfis e públicos-alvo unificados](../audience/get-started-profiles.md) estão recebendo o evento de inscrição.
2. [Crie sua primeira jornada](../building-journeys/journey-gs.md) e use o evento de inscrição como entrada.
3. Adicione um [email](../email/get-started-email.md) de boas-vindas, uma etapa de espera e uma [notificação por push](../push/get-started-push.md) de acompanhamento para perfis que não estejam envolvidos.
4. [Personalize o conteúdo](../personalization/personalize.md) com atributos de perfil, como nome e interesses declarados.

➡️ [Iniciar com jornadas](../building-journeys/journey-gs.md)

### Recuperar carrinhos abandonados {#build-cart}

**Você compilará:** um fluxo de recuperação em tempo real que lembra aos clientes os itens deixados para trás.
**Recomendado para:** Profissionais de marketing · **Recurso:** jornada acionada por evento

1. Certifique-se de que o evento de abandono do carrinho chegue à Journey Optimizer (trabalhe com sua [equipe de dados](../data/gs-data.md), se necessário).
2. [Criar uma jornada](../building-journeys/journey-gs.md) acionada pelo evento de abandono.
3. Envie um email de lembrete personalizado. Se não houver clique em 24 horas, ramifique para um acompanhamento de [push](../push/get-started-push.md).
4. [Personalize](../personalization/personalize.md) com os itens abandonados e o status de fidelidade.

➡️ [Iniciar com jornadas](../building-journeys/journey-gs.md)

### Enviar mensagens transacionais {#build-transactional}

**Você compilará:** Confirmações de pedidos, remessas ou compromissos sob demanda disparadas por um sistema externo.
**Recomendado para:** Profissionais de marketing e desenvolvedores · **Recurso:** campanha acionada por API

1. Revise como [campanhas acionadas por API](../campaigns/api-triggered-campaigns.md) funcionam e qual carga eles esperam.
2. Crie o modelo de mensagem e [personalize](../personalization/personalize.md) com os detalhes da transação.
3. Peça ao desenvolvedor para chamar o endpoint da campanha a partir do seu pedido ou sistema de atendimento.

➡️ [Trabalhar com campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)

### Iniciar uma campanha com teste A/B {#build-campaign}

**Você compilará:** uma promoção agendada que escolhe automaticamente o conteúdo com melhor desempenho.
**Recomendado para:** Profissionais de marketing · **Recurso:** Campanha agendada + experimentação de conteúdo

1. [Comece com campanhas](../campaigns/get-started-with-campaigns.md) e defina seu público.
2. Use a [geração de conteúdo de IA](../content-management/gs-generative.md) para rascunhar variações de linha de assunto e cópia.
3. Configure um [experimento de conteúdo](../content-management/experiment-accelerator-gs.md) para testar variantes em uma amostra e, em seguida, envie o vencedor para o resto.

➡️ [Introdução às campanhas](../campaigns/get-started-with-campaigns.md)

### Personalizar ofertas por cliente {#build-offers}

**Você criará:** uma decisão que mostra a melhor oferta para cada cliente.
**Recomendado para:** Profissionais de marketing · **Funcionalidade:** Decisão

1. [Comece a usar o Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) e crie suas ofertas e regras de qualificação.
2. Adicione a decisão a uma [jornada](../building-journeys/journey-gs.md) ou mensagem de campanha.
3. Camada em [recursos de IA](ai-features.md) para classificar e otimizar ofertas automaticamente.

➡️ [Introdução ao Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Casos de uso por meta {#use-cases}

Os exemplos acima abordam os pontos de partida mais comuns, mas o Journey Optimizer oferece suporte a muitos outros cenários — desde notificações de interrupção proativa e reengajamento do cliente até mensagens em tempo real com reconhecimento de local. Cada cenário combina um ou mais recursos trabalhando juntos.

Para encontrar a capacidade exata para a meta *sua*, use o índice completo e organizado por meta em [Encontre a capacidade correta do Journey Optimizer para a sua meta](ajo-use-case-guide.md). Para exemplos completos e trabalhados, consulte a [biblioteca de casos de uso do Jornada](../building-journeys/jo-use-cases.md).

## Biblioteca de vídeos {#videos}

Navegue por conteúdo de vídeo preparado por tópico. Cada guia está vinculada aos tutoriais e listas de reprodução relevantes no Experience League.

>[!BEGINTABS]

>[!TAB Introdução]

* [Introdução ao Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — Conceitos principais e um tour pelo produto.
* [Visão geral dos tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — o catálogo completo de vídeos guiados.

>[!TAB Jornadas e campanhas]

* [Introdução à criação de uma jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Crie sua primeira jornada acionada por evento.
* [Criar jornadas com o Journey Agent](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — Crie jornadas a partir de um prompt em linguagem natural.

>[!TAB Personalization e IA]

* [Assistente de IA para geração de conteúdo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — Gerar cópia, imagens e variações.
* [Use o decisioning para personalizar ofertas da Web](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Personalize ofertas por cliente.

>[!TAB Relatórios e otimização]

* [Monitore e analise sua jornada com relatórios ao vivo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — Acompanhe o desempenho em tempo real.
* [Criar experimentos de conteúdo para campanhas de email](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Testar e otimizar conteúdo.

>[!ENDTABS]

## Lista de verificação de integração por função {#checklist}

A integração abrange várias funções. Escolha sua função para ver um caminho inicial focalizado:

* **Administrador** — Configurar sandboxes, permissões e canais. [Introdução como Administrador](path/administrator.md)
* **Engenheiro de dados** — esquemas de modelo e assimilação de dados. [Introdução como Engenheiro de Dados](path/data-engineer.md)
* **Desenvolvedor** — integre SDKs e eventos de gatilho. [Introdução como Desenvolvedor](path/developer.md)
* **Profissional de marketing** — crie jornadas, conteúdo e públicos-alvo. [Introdução como profissional de marketing](path/marketer.md)

Para obter uma visão geral completa de como essas funções funcionam juntas, consulte [Funções e responsabilidades](quick-start.md).

## Recursos relacionados {#related-resources}

* [Encontre a capacidade certa do Journey Optimizer para sua meta](ajo-use-case-guide.md) — Guia de decisão de início de meta para todos os recursos.
* [Biblioteca de casos de uso do Jornada](../building-journeys/jo-use-cases.md) — Exemplos práticos e padrões de implementação.
* [Terminologia de chave](terminology.md) — Esclareça os conceitos por trás de cada recurso.
* [IA e recursos inteligentes](ai-features.md) — Explore o Assistente de IA, a otimização de tempo de envio e a geração de conteúdo.
* [Introdução ao gerenciamento de dados](../data/gs-data.md) — Como os dados são assimilados, unificados e ativados.
