---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao rastreamento no Journey Optimizer
description: Saiba mais sobre os recursos de rastreamento e monitoramento disponíveis no Journey Optimizer
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: rastreamento, monitoramento, analytics, relatórios, capacidade de entrega
source-git-commit: a326f6df3332519b2c3efc77a0a0f26e629f1145
workflow-type: tm+mt
source-wordcount: '1813'
ht-degree: 3%

---

# Introdução ao rastreamento no Journey Optimizer {#get-started-tracking}

O rastreamento e o monitoramento permitem medir a eficácia da campanha, otimizar as experiências do cliente e garantir que as mensagens cheguem aos recipients desejados. O Journey Optimizer oferece recursos abrangentes de rastreamento que capturam as interações do cliente, o desempenho do delivery e a integridade do sistema, ajudando você a tomar decisões orientadas por dados, respeitando a privacidade e mantendo a conformidade.

A maioria do rastreamento é configurada automaticamente ao criar mensagens e jornadas. Para cenários avançados, você pode configurar métricas personalizadas, configurar parâmetros de URL e integrar a plataformas de análise externas. Acesse seus dados de rastreamento por meio de relatórios integrados ou exporte-os para análise mais profunda no Customer Journey Analytics.

>[!BEGINSHADEBOX]

O que você pode rastrear no Journey Optimizer:

📧 **Interações de email** - Desempenho de aberturas, cliques e links

🌐 **Comportamento da Web** - Exibições de página, cliques e padrões de envolvimento

🛤️ **Desempenho da Jornada** - Métricas personalizadas, eventos de etapa e caminhos de conversão

📊 **Integridade da entrega** - Taxas de rejeição, reclamações de spam e reputação do remetente

⚙️ **Operações do sistema** - Alertas, erros e desempenho de ação personalizada

>[!ENDSHADEBOX]

Para ajudar você a começar, explore estes tópicos essenciais de rastreamento e monitoramento:

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Métricas" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Configurar métricas de sucesso</strong></a>
    </div>
    <p>
    <em>Rastrear KPIs personalizados alinhados aos seus objetivos comerciais</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Capacidade de entrega" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Monitorar a capacidade de entrega</strong></a>
    </div>
    <p>
    <em>Verifique se as mensagens chegam às caixas de entrada dos clientes</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Relatórios" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Explorar relatórios</strong></a>
    </div>
    <p>
    <em>Acesse relatórios dinâmicos e históricos das suas jornadas e campanhas</em>
    <p>
  </td>
</tr>
</table>

## Rastrear interações do cliente em canais {#tracking-by-channel}

O Journey Optimizer fornece recursos de rastreamento específicos de canal. Veja como configurar e usar o rastreamento para cada canal.

+++Acompanhamento de email

O rastreamento de email é ativado automaticamente ao criar uma mensagem de email. O Journey Optimizer rastreia aberturas, cliques e cancelamentos de assinatura por padrão; nenhuma configuração adicional é necessária.

**Configurar opções de rastreamento:**

* **Habilitar/desabilitar rastreamento** - Controle o rastreamento no nível da mensagem ao criar seu email. Você pode optar por rastrear aberturas, cliques ou ambos. [Saiba mais](../email/message-tracking.md)

* **Configurar parâmetros de rastreamento de URL** - Configure parâmetros de rastreamento no nível da superfície para anexar automaticamente identificadores de campanha (utm_campaign, utm_source etc.) a todos os links de email. Isso permite o rastreamento de atribuições em todo o ecossistema digital. [Saiba mais](../email/url-tracking.md)

* **Rastrear links em fragmentos salvos** - Quando o rastreamento é habilitado em uma jornada ou campanha, os links em um fragmento salvos do conteúdo dessa jornada ou campanha também são rastreados quando esse fragmento é reutilizado. [Saiba mais](../content-management/save-fragments.md)

* **Adicionar rastreamento de mirror page** - Habilite a opção de mirror page para criar uma versão da Web do seu email com rastreamento automático de quem o visualiza. [Saiba mais](../email/message-tracking.md#mirror-page)

**Monitorar o desempenho:** Exiba métricas em tempo real nos relatórios de campanha e jornadas, incluindo abertura, cliques e desempenho no nível do link. [Relatórios de campanha](../reports/campaign-global-report-cja-email.md) | [Jornada relatórios](../reports/journey-global-report-cja-email.md)

+++

+++Rastreamento web

O rastreamento web requer configuração explícita para rastrear as interações do usuário com as modificações da Web.

**Configurar o rastreamento de cliques:**

Ao criar uma modificação na Web, você pode selecionar elementos específicos (botões, imagens, links) que deseja rastrear. Isso permite o rastreamento de cliques para esses elementos sem a necessidade de código adicional. [Saiba mais](../web/monitor-web-experiences.md)

* **Rastrear qualquer elemento clicável** - Selecione botões, imagens, links ou qualquer elemento interativo na personalização da Web
* **Coleta de dados automática** - Uma vez configurada, a Journey Optimizer captura automaticamente eventos de clique e os associa a perfis
* **Monitorar em tempo real** - Rastreie as interações do usuário à medida que elas validam a eficácia da personalização

**Exibir dados de rastreamento:** Acesse métricas de exibição, taxas de click-through e desempenho em nível de elemento em relatórios. [Relatórios de campanha](../reports/campaign-global-report-cja-web.md) | [Jornada relatórios](../reports/journey-global-report-cja-web.md)

+++

+++Rastreamento de notificação por push

O rastreamento de push é ativado automaticamente e captura impressões (entregues), cliques (tocados) e aberturas (iniciadas pelo aplicativo). Para maximizar o valor de rastreamento, configure elementos clicáveis no conteúdo de push.

**Configurar elementos rastreados:**

* **Comportamento de clique no corpo** - Defina o que acontece quando os usuários tocam na notificação: abrir o aplicativo, navegar até um link profundo ou abrir uma URL da Web. Cada ação é rastreada automaticamente. [Saiba mais](../push/design-push.md#on-click-behavior)

* **Adicionar botões de ação** - Inclua até 3 botões (Android) ou vários botões (iOS) com rastreamento independente para cada ação de botão (aplicativo aberto, link profundo, URL da Web). [Saiba mais](../push/design-push.md#add-buttons-push)

* **Habilitar rastreamento** - Verifique se o rastreamento está habilitado na atividade de jornada por push ou nas configurações de rastreamento da campanha. [Saiba mais](../push/create-push.md#create)

>[!NOTE]
>
>O rastreamento de push requer a implementação do SDK móvel. Verifique se o aplicativo tem o Adobe Experience Platform Mobile SDK configurado corretamente. [Saiba mais](../push/push-configuration.md#integrate-mobile-app)

**Analisar engajamento:** Exiba taxas de click-through, desempenho do botão e detalhes do link rastreado em relatórios. [Relatórios de campanha](../reports/campaign-global-report-cja-push.md) | [Jornada relatórios](../reports/journey-global-report-cja-push.md)

+++

+++Rastreamento de mensagens no aplicativo

As mensagens no aplicativo rastreiam automaticamente as exibições e as interações do usuário. Configure acionadores e conteúdo para maximizar a eficácia do rastreamento.

**Configurar rastreamento:**

* **Configurar regras de exibição** - Defina quando e onde as mensagens no aplicativo aparecem usando acionadores (inicialização do aplicativo, carregamento da tela), regras de frequência e condições de público-alvo. A configuração adequada garante o rastreamento preciso de mensagens acionadas e exibidas. [Saiba mais](../in-app/create-in-app.md)

* **Adicionar elementos rastreados** - Inclua botões, links e elementos interativos no conteúdo da mensagem. Cada interação é automaticamente rastreada com rótulos detalhados.

* **Otimizar o tempo de exibição** - Configure as regras de dia da semana e hora do dia para maximizar a probabilidade de as mensagens disparadas serem realmente exibidas para os usuários.

**O que é rastreado:** o Journey Optimizer captura automaticamente exibições, cliques em botões, dispensas, métricas acionadas versus exibidas e desempenho do link. [Relatórios de campanha](../reports/campaign-global-report-cja-inapp.md) | [Jornada relatórios](../reports/journey-global-report-cja-inapp.md)

+++

+++Rastreamento de SMS e MMS

O rastreamento de SMS requer configuração mínima — o Journey Optimizer encurta e rastreia automaticamente os links incluídos nas mensagens.

**Como funciona:**

* **Rastreamento automático de links** - Adicione qualquer URL ao conteúdo do SMS usando a função auxiliar de URL. O Journey Optimizer reduz automaticamente o link e rastreia os cliques sem configuração adicional. Para usar a redução de URL, primeiro você deve configurar um subdomínio SMS. [Saiba mais](../sms/create-sms.md#sms-content)

* **Rastreamento de mensagens de entrada** - As respostas dos destinatários são capturadas automaticamente, permitindo que você monitore conversas bidirecionais e padrões de resposta.

**Exibir métricas:** Acesse dados de cliques em links, volumes de mensagens de entrada e desempenho do tipo de mensagem em relatórios. [Relatórios de campanha](../reports/campaign-global-report-cja-sms.md) | [Jornada relatórios](../reports/journey-global-report-cja-sms.md)

+++

+++Rastreamento de experiência baseado em código

Experiências baseadas em código exigem configuração de implementação para enviar dados de rastreamento ao Adobe Experience Platform.

**Pré-requisitos:**

Antes que o rastreamento funcione, é necessário configurar a implementação para enviar eventos de interação (exibições, cliques) para o Adobe Experience Platform. Isso requer:

* Configuração de uma sequência de dados configurada para o Adobe Experience Platform
* Implementação da coleção de eventos no código usando o Web SDK ou o SDK móvel
* Envio de eventos de exibição e interação quando o conteúdo é exibido ou clicado

[Saiba mais sobre os pré-requisitos de implementação](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**O que é rastreado:** depois de implementado, rastrear exibições, cliques, taxas de click-through e desempenho em nível de elemento em qualquer ponto de contato digital (sites, aplicativos móveis, dispositivos da IoT etc.). [Relatórios de campanha](../reports/campaign-global-report-cja-code.md) | [Jornada relatórios](../reports/journey-global-report-cja-code.md)

+++

+++Rastreamento de cartão de conteúdo

[Cartões de conteúdo](../content-card/create-content-card.md) rastreiam automaticamente as interações do usuário. Configure as regras de conteúdo e exibição para controlar o comportamento do rastreamento.

**Como implementar:**

* **Conteúdo rastreado do design** - Adicione botões e links ao seu cartão de conteúdo. Cada elemento interativo é rastreado automaticamente com rótulos e URLs.

* **Configurar persistência** - Os cartões de conteúdo persistem em todas as sessões do aplicativo, permitindo que você acompanhe padrões de engajamento de longo prazo. Defina as regras de expiração para controlar por quanto tempo os cartões permanecem rastreáveis.

* **Configurar regras de exibição** - Defina quando e onde os cartões são exibidos para garantir um rastreamento preciso de exibições vs. interações.

**Monitorar engajamento:** Rastrear exibições, cliques, taxas de click-through e padrões de engajamento em várias sessões. [Relatórios de campanha](../reports/campaign-global-report-cja-content.md) | [Jornada relatórios](../reports/journey-global-report-cja-content.md)

+++

+++Rastreamento da landing page

[As páginas de aterrissagem](../reports/lp-report-global-cja.md) vêm com acompanhamento interno que não requer configuração adicional. O Journey Optimizer captura automaticamente visitas, conversões e taxas de rejeição.

**O que é rastreado automaticamente:**

* **Visitas** - Visitas totais e exclusivas para medir o alcance
* **Conversões** - Envios de formulários, confirmações de assinatura ou outras ações definidas
* **Taxa de rejeição** - Porcentagem de visitantes que saem sem interagir
* **Tendências de desempenho** - Dados de série temporal que mostram como as métricas evoluem

**Otimizar o desempenho:** use dados de rastreamento para refinar campos de formulário, testar variações de conteúdo, identificar fontes de tráfego eficazes e reduzir o abandono.

+++

## Acompanhe suas atividades de jornada e campanha {#journey-campaign-tracking}

Além do rastreamento no nível do canal, configure o rastreamento para medir o desempenho geral e entender o comportamento do cliente em suas iniciativas de marketing.

* **Definir métricas de sucesso personalizadas** - Configure KPIs específicos alinhados aos seus objetivos de negócios (compras, inscrições, renovações, etc.) além das métricas de envolvimento padrão. [Saiba mais](../building-journeys/success-metrics.md)

* **Habilitar eventos de etapa do jornada** - Ative o rastreamento detalhado de cada ação que os clientes realizam ao percorrerem o jornada. Isso proporciona visibilidade granular dos pontos de entrada/saída, seleção de caminho e locais de devolução. [Saiba mais](../reports/journey-step-events-overview.md)

* **Configurar agendamento** - Configure a otimização de tempo de envio para acompanhar o desempenho em diferentes estratégias de tempo e identificar as janelas de envio ideais. [Saiba mais](../building-journeys/send-time-optimization.md)

* **Configurar o monitoramento de ações personalizadas** - Configurar o rastreamento de integrações com sistemas externos para monitorar chamadas de API, tempos de resposta e padrões de erro. [Saiba mais](../action/reporting.md)

* **Exportação personalizada de relatórios e dados** - Crie relatórios personalizados e exporte dados de rastreamento para sistemas externos para uma análise mais profunda. [Saiba mais](../reports/sharing-overview.md)

**Exiba o desempenho unificado** Acesse relatórios abrangentes para campanhas e jornadas para comparar o desempenho em email, push, SMS e outros canais e para entender quais combinações geram melhores resultados. [Relatórios de campanha](../reports/campaign-global-report-cja.md) | [Jornada relatórios](../reports/journey-global-report-cja.md)

## Rastrear o desempenho da otimização e da decisão {#optimization-decisioning-tracking}

O Journey Optimizer rastreia automaticamente experimentos de otimização, estratégias de direcionamento e desempenho de decisão. Defina as configurações para garantir a coleta de dados adequada.

**Configurar o rastreamento de otimização:**

* **Configurar experimentação** - Ao criar experimentos ou usar o direcionamento, defina quais métricas rastrear (conversões, cliques, eventos personalizados). O Journey Optimizer coleta automaticamente dados de desempenho para cada tratamento. [Saiba mais](../campaigns/campaigns-message-optimization.md)

* **Configurar a otimização de caminho** - Adicione uma atividade **Otimizar** à jornada e configure vários caminhos. O Journey Optimizer rastreia automaticamente quais caminhos os perfis tomam e mede o desempenho. [Saiba mais](../building-journeys/optimize.md)

**Analisar resultados:** Exiba taxas de conversão, significância estatística e aumento entre tratamentos nos relatórios de experimentação. [Relatórios de campanha](../reports/campaign-global-report-cja-experimentation.md) | [Jornada relatórios](../reports/journey-global-report-cja-experimentation.md)

**Rastrear desempenho de decisão:**

Ao usar a Decisão para personalizar o conteúdo, o Journey Optimizer rastreia automaticamente eventos de decisão, impressões e cliques sem a necessidade de configuração adicional.

* **Captura automática de evento** - O Journey Optimizer captura automaticamente eventos de decisão sempre que um item de decisão é selecionado para um perfil.
* **Rastreamento de impressão** - Para emails, as impressões são rastreadas automaticamente. Para experiências baseadas em código, é necessário implementar eventos de exibição de apresentação no código.
* **Rastreamento de cliques** - Os cliques nos itens de decisão são rastreados automaticamente em emails; experiências baseadas em código exigem a implementação de eventos de clique.

**Pré-requisitos para o rastreamento baseado em código** Para rastrear a decisão em experiências baseadas em código, verifique se a sua implementação envia eventos de interação de apresentação (exibições e cliques) para a Adobe Experience Platform usando o Web SDK ou o Mobile SDK. [Saiba mais](../experience-decisioning/data-collection/schema-requirement.md)

**Analisar o desempenho:** Exiba KPIs de decisão, compare itens de decisão, analise estratégias de seleção e monitore o desempenho do modelo de IA em relatórios. [Saiba mais](../experience-decisioning/cja-reporting.md)

## Controlar uso de dados de rastreamento {#data-governance}

As políticas de governança de dados permitem controlar como os dados de rastreamento podem ser usados em sua organização:

* **Dados de rastreamento sensíveis ao rótulo** - Aplique rótulos de governança aos dados comportamentais rastreados (por exemplo, cliques no conteúdo de integridade, interações com produtos financeiros) para marcá-los como confidenciais ou regulamentados.

* **Restringir o uso de dados** - Crie políticas que impeçam que os dados de rastreamento rotulados sejam usados em determinados canais, exportados para sistemas de terceiros ou usados para cenários de personalização específicos.

* **Imposição automática** - o Journey Optimizer verifica automaticamente as políticas de governança ao criar jornadas e campanhas, bloqueando a publicação se os dados rastreados estiverem sendo usados em violação das políticas definidas.

O controle de dados garante a conformidade com regulamentos como o GDPR e o CCPA, permitindo que você rastreie e analise o comportamento do cliente dentro dos limites aprovados. [Saiba mais](../action/action-privacy.md)

## Monitorar a capacidade de entrega e a integridade do sistema {#monitoring-capabilities}

Além do rastreamento do engajamento, configure o monitoramento para garantir que as mensagens cheguem às caixas de entrada e que os sistemas tenham ótimo desempenho.

**Configurar o monitoramento pró-ativo:**

* **Configurar alertas** - Configure notificações em tempo real sobre erros de jornada, falhas de ação personalizada e problemas críticos para responder rapidamente aos problemas. [Saiba mais](../reports/alerts.md)

* **Habilitar logs de auditoria** - Ative o log de auditoria para rastrear todas as ações nos recursos para fins de conformidade e solução de problemas. [Saiba mais](../privacy/audit-logs.md)

* **Monitorar integrações** - Rastreie o desempenho da ação personalizada e a conectividade do sistema externo para identificar problemas de integração antecipadamente. [Saiba mais](../action/reporting.md)

**Monitoramento da entregabilidade:**

* **Revise a lista de supressão** regularmente para entender por que os endereços são bloqueados e manter a higiene das listas. [Saiba mais](../reports/suppression-list.md)

* **Analise os erros de entrega** para diagnosticar falhas e tomar medidas corretivas. [Saiba mais](../configuration/email-error-types.md)

* **Siga as práticas recomendadas** para o DMARC, SPF e DKIM para maximizar o posicionamento da caixa de entrada. [Saiba mais](../reports/deliverability.md)

