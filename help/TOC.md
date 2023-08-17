---
product: Journey Optimizer
audience: end-user
user-guide-title: Guia do Journey Optimizer
user-guide-description: Use o Journey Optimizer para criar e fornecer experiências conectadas, contextuais e personalizadas aos clientes
type: Documentation
solution: Journey Optimizer
source-git-commit: 98e9d4530feb584ddcbf460714f1302b87d7822a
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 100%

---

# Ajuda do Adobe Journey Optimizer {#using}

+ [Documentação do Journey Optimizer](ajo-home.md)
+ Novidades {#whats-new}
   + [Notas de versão antecipadas](using/rn/e-release-notes.md)
   + [Notas de versão mais recentes](using/rn/release-notes.md)
   + Notas de versão anteriores {#previous-rn-new}
      + [Notas de versão de 2022](using/rn/release-notes-2022.md)
      + [Notas de versão de 2021](using/rn/release-notes-2021.md)
   + [Atualizações de documentação](using/rn/documentation-updates.md)
+ Introdução{#get-started}
   + [O que é o Journey Optimizer](using/start/get-started.md)
   + Guias de início rápido{#quick-start}
      + [Visão geral](using/start/quick-start.md)
      + [Introdução para profissionais de marketing](using/start/path/marketer.md)
      + [Introdução para engenheiros de dados](using/start/path/data-engineer.md)
      + [Introdução para administradores](using/start/path/administrator.md)
      + [Introdução para desenvolvedores](using/start/path/developer.md)
   + [Interface do usuário](using/start/user-interface.md)
   + [Pesquisar, filtrar, categorizar](using/start/search-filter-categorize.md)
   + [Acessibilidade](using/start/accessibility.md)
   + [Integrações](using/start/ajo-integrations.md)
   + [Medidas de proteção](using/start/guardrails.md)
+ Jornadas {#orchestrate-journeys}
   + [Introdução a jornadas](using/building-journeys/journey.md)
   + Criar uma jornada{#create-journey}
      + [Criar a primeira jornada](using/building-journeys/journey-gs.md)
      + [Projetar a jornada](using/building-journeys/using-the-journey-designer.md)
      + [Teste a jornada](using/building-journeys/testing-the-journey.md)
      + [Publicar a jornada](using/building-journeys/publishing-the-journey.md)
   + Gerenciar suas jornadas{#manage-journey}
      + [Encerrar sua jornada](using/building-journeys/end-journey.md)
      + [Gerenciamento de fuso horário](using/building-journeys/timezone-management.md)
      + [Gerenciamento de entrada de perfis](using/building-journeys/entry-management.md)
      + [Copiar uma jornada para outra sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Solucionar problemas da jornada](using/building-journeys/troubleshooting.md)
      + [Integrar a serviços inteligentes](using/building-journeys/ai-services-overview.md)
   + Atividades {#about-journey-building}
      + [Introdução às atividades de jornada](using/building-journeys/about-journey-activities.md)
      + [Eventos gerais](using/building-journeys/general-events.md)
      + [Reação](using/building-journeys/reaction-events.md)
      + [Qualificação de público-alvo](using/building-journeys/audience-qualification-events.md)
      + [Condição](using/building-journeys/condition-activity.md)
      + [Aguardar](using/building-journeys/wait-activity.md)
      + [Público-alvo de leitura](using/building-journeys/read-audience.md)
      + [Email, no aplicativo, push, SMS](using/building-journeys/journeys-message.md)
      + [Ações personalizadas](using/building-journeys/using-custom-actions.md)
      + [Ações do Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Ações do Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Salto](using/building-journeys/jump.md)
      + [Atualizar perfil](using/building-journeys/update-profiles.md)
   + Criar expressões {#building-advanced-conditions-journeys}
      + [Visão geral](using/building-journeys/expression/expressionadvanced.md)
      + Sintaxe {#syntax}
         + [Generalidades](using/building-journeys/expression/generalities.md)
         + [Instrução condicional](using/building-journeys/expression/conditional-instruction.md)
         + [Tipos de dados](using/building-journeys/expression/data-types.md)
         + [Referências de campo](using/building-journeys/expression/field-references.md)
         + [Funções de gerenciamento de coleções](using/building-journeys/expression/collection-management-functions.md)
         + [Operadores](using/building-journeys/expression/operators.md)
         + [Propriedades da jornada](using/building-journeys/expression/journey-properties.md)
         + [Exemplos](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Funções {#main-functions-journey}
         + [Funções principais](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + Agregação {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Conversão {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Data {#date}
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Lista {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filtro](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [no](using/building-journeys/functions/functionin.md)
            + [interseção](using/building-journeys/functions/functionintersect.md)
            + [limite](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Matemática {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + String {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [comprimento](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Casos de uso {#journey-use-cases}
      + Casos de uso comercial {#business-use-cases}
         + [Enviar mensagens de vários canais](using/building-journeys/journeys-uc.md)
         + [Enviar uma mensagem usando o Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Enviar uma mensagem aos assinantes](using/building-journeys/message-to-subscribers-uc.md)
      + Casos de uso técnicos {#technical-use-cases}
         + [Envio dinâmico de coleções usando ações personalizadas](using/building-journeys/collections.md)
         + [Incrementar entregas](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limite a taxa de transferência com Fontes de dados externas e Ações personalizadas](using/building-journeys/limit-throughput.md)
+ Campanhas{#campaigns}
   + [Introdução às campanhas](using/campaigns/get-started-with-campaigns.md)
   + [Criar uma campanha](using/campaigns/create-campaign.md)
   + [Revisar e ativar uma campanha](using/campaigns/review-activate-campaign.md)
   + [Gerenciar campanhas](using/campaigns/modify-stop-campaign.md)
   + Experimento de conteúdo {#content-experiment}
      + [Introdução ao experimento de conteúdo](using/campaigns/get-started-experiment.md)
      + [Criar um experimento de conteúdo](using/campaigns/content-experiment.md)
      + [Configurar relatórios de experimentação](using/campaigns/reporting-configuration.md)
      + Notas técnicas {#technotes}
         + [Compreenda cálculos estatísticos](using/campaigns/experiment-calculations.md)
         + [Compreenda cálculos estatísticos no Relatório de experimentação](using/campaigns/experiment-report-calculations.md)
   + [Acione campanhas usando APIs](using/campaigns/api-triggered-campaigns.md)
+ Canal de email {#email}
   + [Introdução a emails](using/email/get-started-email.md)
   + [Criar um email](using/email/create-email.md)
   + Projetar o conteúdo de email {#design-email}
      + [Introdução ao design de email](using/email/get-started-email-design.md)
      + Começar a criar conteúdo {#start-creating-content}
         + [Crie um conteúdo do zero](using/email/content-from-scratch.md)
         + [Importar seu conteúdo](using/email/existing-content.md)
         + [Programar seu próprio conteúdo](using/email/code-content.md)
         + [Trabalhar com modelos](using/email/email-templates.md)
      + Projetar o conteúdo {#add-content}
         + [Usar componentes de conteúdo](using/email/content-components.md)
         + [Adicionar links e rastrear mensagens](using/email/message-tracking.md)
         + Gerenciar ativos {#manage-asset}
            + [Trabalhar com o Assets Essentials](using/email/assets-essentials.md)
            + [Trabalhar com o Adobe Stock](using/email/stock.md)
         + [Inserir ofertas personalizadas](using/email/add-offers-email.md)
         + [Gerar a versão de texto](using/email/text-version-email.md)
         + [Adicionar um pré-cabeçalho](using/email/preheader.md)
      + Editar estilo {#edit-style}
         + [Introdução ao estilo de email](using/email/get-started-email-style.md)
         + [Editar configurações de fundo](using/email/backgrounds.md)
         + [Ajustar o alinhamento vertical e o preenchimento](using/email/alignment-and-padding.md)
         + [Adicionar atributos de estilo incorporado](using/email/inline-styling.md)
   + [Visualizar e testar o email](using/email/preview.md)
   + [Criar modelos de conteúdo](using/email/content-templates.md)
   + [Usar modelos do Experience Manager](using/email/aem-templates.md)
   + [Trabalhar com fragmentos](using/email/fragments.md)
   + [Gerenciar opção de não participação de email](using/email/email-opt-out.md)
   + Configurar canal de email {#configure-email}
      + [Introdução à configuração de email](using/email/get-started-email-config.md)
      + [Definir configurações de superfície de email](using/email/email-settings.md)
+ Canal no aplicativo{#in-app}
   + [Introdução ao canal no aplicativo](using/in-app/get-started-in-app.md)
   + [Criação de uma mensagem no aplicativo](using/in-app/create-in-app.md)
   + [Criar uma mensagem no aplicativo em uma jornada](using/in-app/create-in-app-journey.md)
   + [Criar seu conteúdo no aplicativo](using/in-app/design-in-app.md)
   + [Teste e envie a sua notificação no aplicativo](using/in-app/send-in-app.md)
   + [Configuração do canal no aplicativo](using/in-app/inapp-configuration.md)
+ Canal de notificação por push{#push}
   + [Introdução à notificação por push](using/push/get-started-push.md)
   + [Criar uma notificação por push](using/push/create-push.md)
   + [Projetar a notificação por push](using/push/design-push.md)
   + [Enviar a notificação por push](using/push/send-push.md)
   + Configurar notificações por push{#push-config}
      + [Fluxo de notificação por push](using/push/push-gs.md)
      + [Configurar canal de notificação por push](using/push/push-configuration.md)
      + [Fluxo de trabalho de início rápido de integração para dispositivos móveis](using/push/mobile-onboarding-wf.md)
+ Canal SMS{#sms}
   + [Introdução a SMS](using/sms/get-started-sms.md)
   + [Criar uma mensagem de SMS.](using/sms/create-sms.md)
   + [Visualizar e testar o SMS](using/sms/send-sms.md)
   + [Gerenciar opção de não participação de SMS](using/sms/sms-opt-out.md)
   + [Configurar canal de SMS](using/sms/sms-configuration.md)
   + [Configurar os subdomínios de SMS](using/sms/sms-subdomains.md)
+ Correspondência direta {#direct-mail}
   + [Introdução à correspondência direta](using/direct-mail/get-started-direct-mail.md)
   + [Criação de uma correspondência direta](using/direct-mail/create-direct-mail.md)
   + [Teste e envio de uma mensagem de correspondência direta](using/direct-mail/test-send-direct-mail.md)
   + [Configurar correspondência direta](using/direct-mail/direct-mail-configuration.md)
+ Canal da Web{#web}
   + [Introdução ao canal Web](using/web/get-started-web.md)
   + [Pré-requisitos do canal web](using/web/web-prerequisites.md)
   + [Criação de experiências da Web](using/web/create-web.md)
   + [Páginas da Web de autor](using/web/author-web.md)
   + [Configurar subdomínios da Web](using/web/web-delegated-subdomains.md)
+ Páginas de destino {#landing-pages}
   + [Introdução às páginas de destino](using/landing-pages/get-started-lp.md)
   + [Criar uma página de destino](using/landing-pages/create-lp.md)
   + Criação de conteúdo {#landing-pages-design}
      + [Sobre modelos de página de destino](using/landing-pages/design-lp.md)
      + [Criar o conteúdo da página de destino](using/landing-pages/lp-content.md)
      + [Criar modelos](using/landing-pages/lp-templates.md)
      + [Adicionar JavaScript personalizado](using/landing-pages/lp-custom-js.md)
   + [Criar uma lista de assinaturas](using/landing-pages/subscription-list.md)
   + [Aprenda mais por meio de casos de uso](using/landing-pages/lp-use-cases.md)
   + Configurar páginas de destino {#lp-configuration}
      + [Configurar subdomínios de página de destino](using/landing-pages/lp-subdomains.md)
      + [Definir predefinições da página de destino](using/landing-pages/lp-presets.md)
+ Personalização e conteúdo dinâmico {#personalized-dynamic-content}
   + Personalização {#personalization}
      + [Introdução à personalização](using/personalization/personalize.md)
      + [Contextos de personalização](using/personalization/personalization-contexts.md)
      + Criar expressões {#build-expressions}
         + [Sintaxe de personalização](using/personalization/personalization-syntax.md)
         + Trabalhar com o editor de expressão {#expression-editor}
            + [Sobre o editor de expressão](using/personalization/personalization-build-expressions.md)
            + [Adicionar atributos aos favoritos](using/personalization/personalization-favorites.md)
            + [Trabalhar com expressões salvas](using/personalization/personalization-library.md)
            + [Validação de personalização](using/personalization/personalization-validation.md)
         + Funções auxiliares {#functions}
            + [Introdução a funções auxiliares](using/personalization/functions/functions.md)
            + [Funções de agregação](using/personalization/functions/aggregation.md)
            + [Funções aritméticas](using/personalization/functions/arithmetic-functions.md)
            + [Matrizes e funções de lista](using/personalization/functions/arrays-list.md)
            + [Funções de data](using/personalization/functions/dates.md)
            + [Funções booleanas e de comparação](using/personalization/functions/operators.md)
            + [Auxiliares](using/personalization/functions/helpers.md)
            + [Funções do mapa](using/personalization/functions/maps.md)
            + [Funções matemáticas](using/personalization/functions/math.md)
            + [Funções do objeto](using/personalization/functions/objects.md)
            + [Funções de string](using/personalization/functions/string.md)
      + Casos de uso{#personalization-use-cases}
         + [Notificação do status do pedido](using/personalization/personalization-use-case.md)
         + [Email de abandono do carrinho](using/personalization/personalization-use-case-helper-functions.md)
   + Conteúdo dinâmico {#dynamic}
      + [Introdução ao conteúdo dinâmico](using/personalization/get-started-dynamic-content.md)
      + [Criar regras condicionais](using/personalization/create-conditions.md)
      + [Criar conteúdo dinâmico](using/personalization/dynamic-content.md)
+ Públicos-alvo, perfis e identidade{#audiences-profiles-identities}
   + Públicos-alvo {#audiences}
      + [Introdução aos públicos](using/audience/about-audiences.md)
      + [Criar definições de segmento](using/audience/creating-a-segment-definition.md)
      + Compor públicos-alvo {#audience-orchestration}
         + [Introdução à composição de público](using/audience/get-started-audience-orchestration.md)
         + [Criar workflows de composição](using/audience/create-compositions.md)
         + [Trabalhar com a tela de composição](using/audience/composition-canvas.md)
         + [Acessar e gerenciar públicos-alvo](using/audience/access-audiences.md)
   + Perfis{#profiles}
      + [Introdução aos perfis](using/audience/get-started-profiles.md)
      + [Criar perfis de teste](using/audience/creating-test-profiles.md)
   + [Identidades](using/audience/get-started-identity.md)
   + [Uso da licença](using/audience/license-usage.md)
+ Rastrear e monitorar {#reporting}
   + Relatório ao vivo {#live-report}
      + [Introdução aos relatórios em tempo real](using/reports/live-report.md)
      + [Lista de componentes](using/reports/live-report-components.md)
      + [Relatório da jornada em tempo real](using/reports/journey-live-report.md)
      + [Relatório em tempo real da campanha](using/reports/campaign-live-report.md)
      + [Relatório em tempo real da página de destino](using/reports/lp-report-live.md)
      + [Relatório em tempo real da lista de assinaturas](using/reports/subscription-report-live.md)
   + Relatório global {#global-report}
      + [Introdução aos relatórios globais](using/reports/global-report.md)
      + [Lista de componentes](using/reports/global-report-components.md)
      + [Relatório global da jornada](using/reports/journey-global-report.md)
      + [Relatório global da campanha](using/reports/campaign-global-report.md)
      + [Relatório de objetivo](using/reports/objective-report.md)
      + [Relatório global da página de destino](using/reports/lp-report-global.md)
      + [Relatório global da lista de assinaturas](using/reports/subscription-report-global.md)
   + Relatórios de jornada {#reports}
      + [Criar relatórios de jornada](using/reports/sharing-overview.md)
      + [Lista de campos de evento de etapa](using/reports/sharing-field-list.md)
      + Campos de evento de etapa herdado {#legacy-step-event-fields}
         + [Sobre campos herdados](using/reports/sharing-legacy-fields.md)
         + [Campos de jornada](using/reports/sharing-journey-fields.md)
         + [Campos comuns](using/reports/sharing-common-fields.md)
         + [Campos de execução de ação](using/reports/sharing-execution-fields.md)
         + [Campos de busca de dados](using/reports/sharing-fetch-fields.md)
         + [Campos de identidade](using/reports/sharing-identity-fields.md)
      + [Exemplos de consultas](using/reports/query-examples.md)
   + Capacidade de entrega {#deliverability}
      + [Introdução à capacidade de entrega](using/reports/deliverability.md)
      + [Sobre a lista de supressão](using/reports/suppression-list.md)
   + [Alertas](using/reports/alerts.md)
   + [Trabalhar com o Customer Journey Analytics](using/reports/cja-ajo.md)
+ Gestão de decisões {#offer-decisioning}
   + Introdução ao Gestão de decisões {#get-started-decision}
      + [Sobre a Gestão de decisões](using/offers/get-started/starting-offer-decisioning.md)
      + [Interface do usuário](using/offers/get-started/user-interface.md)
      + [Etapas principais para criar e gerenciar ofertas](using/offers/offer-library/key-steps.md)
      + [Caso de uso: inserir ofertas em um email](using/offers/offers-e2e.md)
   + Criar componentes {#create-components}
      + [Criar inserções](using/offers/offer-library/creating-placements.md)
      + [Criar regras de decisão](using/offers/offer-library/creating-decision-rules.md)
      + [Criar qualificadores de coleção](using/offers/offer-library/creating-tags.md)
   + Criar classificações {#rankings}
      + [Introdução às classificações](using/offers/ranking/get-started-rankings.md)
      + [Fórmulas de classificação](using/offers/ranking/create-ranking-formulas.md)
      + Modelos de IA {#ai-models}
         + [Sobre modelos de IA](using/offers/ranking/ai-models.md)
         + Tipos de modelo de IA {#ai-model-types}
            + [Modelo de otimização automática](using/offers/ranking/auto-optimization-model.md)
            + [Modelo de otimização personalizado](using/offers/ranking/personalized-optimization-model.md)
         + [Criar modelos de IA](using/offers/ranking/create-ranking-strategies.md)
   + Criar e gerenciar ofertas {#managing-offers-in-the-offer-library}
      + Configurar ofertas {#configure-offers}
         + [Criar ofertas personalizadas](using/offers/offer-library/creating-personalized-offers.md)
         + [Adicionar representações](using/offers/offer-library/add-representations.md)
         + [Adicionar restrições](using/offers/offer-library/add-constraints.md)
      + [Criar ofertas substitutas](using/offers/offer-library/creating-fallback-offers.md)
      + [Criar coleções](using/offers/offer-library/creating-collections.md)
   + Criar e gerenciar decisões {#create-manage-activities}
      + [Criar decisões](using/offers/offer-activities/create-offer-activities.md)
      + [Configurar seleção de ofertas em decisões](using/offers/offer-activities/configure-offer-selection.md)
      + [Criar simulações](using/offers/offer-activities/simulation.md)
   + [Usar decisões em lote](using/offers/batch-delivery.md)
   + Coletar dados do evento {#collect-event-data}
      + [Introdução à coleta de dados](using/offers/data-collection/data-collection.md)
      + [Criar um conjunto de dados para coletar eventos](using/offers/data-collection/create-dataset.md)
      + [Configurar captura de eventos](using/offers/data-collection/schema-requirement.md)
   + Criar relatórios de gestão de decisões {#create-reports}
      + [Trabalhar com eventos de gestão de decisões](using/offers/reports/get-started-events.md)
      + [Acessar campos XDM de eventos](using/offers/reports/xdm-fields.md)
   + Exportar seu catálogo de ofertas {#export-catalog}
      + [Introdução à exportação do catálogo de ofertas](using/offers/export-catalog/get-started-export.md)
      + [Acessar o catálogo de ofertas exportado](using/offers/export-catalog/access-dataset.md)
      + [Conjunto de dados de ofertas personalizadas](using/offers/export-catalog/export-offers.md)
      + [Conjunto de dados de decisões](using/offers/export-catalog/export-decisions.md)
      + [Conjunto de dados de inserções](using/offers/export-catalog/export-placements.md)
      + [Conjunto de dados substitutos](using/offers/export-catalog/export-fallback.md)
   + Referência da API {#api-reference}
      + [Introdução](using/offers/api-reference/getting-started.md)
      + Criar e gerenciar ofertas usando APIs {#offers-api}
         + Posicionamentos {#placements}
            + [Listar inserções](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Pesquisar uma inserção](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Criar uma inserção](using/offers/api-reference/offers-api/placements/create.md)
            + [Atualizar uma inserção](using/offers/api-reference/offers-api/placements/update.md)
            + [Excluir uma inserção](using/offers/api-reference/offers-api/placements/delete.md)
         + Regras de decisão {#decision-rules}
            + [Listar de regras de decisão](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Pesquisar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Criar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Atualizar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Excluir uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Qualificadores de coleção {#tags}
            + [Listar qualificadores de coleção](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Pesquisar um qualificador de coleção](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Criar um qualificador de coleção](using/offers/api-reference/offers-api/tags/create.md)
            + [Atualizar um qualificador de coleção](using/offers/api-reference/offers-api/tags/update.md)
            + [Excluir um qualificador de coleção](using/offers/api-reference/offers-api/tags/delete.md)
         + Ofertas personalizadas {#personalized-offers}
            + [Listar ofertas personalizadas](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [Pesquisar uma oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [Criar uma oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [Atualizar uma oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [Excluir uma oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + Coleções {#collections}
            + [Listar coleções](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [Pesquisar uma coleção](using/offers/api-reference/offers-api/collections/lookup.md)
            + [Criar uma coleção](using/offers/api-reference/offers-api/collections/create.md)
            + [Atualizar uma coleção](using/offers/api-reference/offers-api/collections/update.md)
            + [Excluir uma coleção](using/offers/api-reference/offers-api/collections/delete.md)
         + Ofertas substitutas {#fallback-offers}
            + [Listar ofertas substitutas](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Pesquisar uma oferta substituta](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Criar uma oferta substituta](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Atualizar uma oferta substituta](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Excluir uma oferta substituta](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Criar e gerenciar decisões usando APIs {#activities-api}
         + [Listar decisões](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Pesquisar uma decisão](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Criar uma decisão](using/offers/api-reference/activities-api/activities/create.md)
         + [Atualizar uma decisão](using/offers/api-reference/activities-api/activities/update.md)
         + [Excluir uma decisão](using/offers/api-reference/activities-api/activities/delete.md)
      + Entregar ofertas usando APIs {#offer-delivery-api}
         + [Introdução às APIs de entrega de ofertas](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [API de decisão](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API de decisão do Edge](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API de decisão em lote](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Gerenciamento de dados {#data-management}
   + [Introdução ao gerenciamento de dados](using/data/gs-data.md)
   + [Trabalhar com esquemas](using/data/get-started-schemas.md)
   + Conjuntos de dados do Journey Optimizer {#datasets}
      + [Introdução aos conjuntos de dados](using/data/get-started-datasets.md)
      + [Exportar conjuntos de dados do Journey Optimizer](using/data/export-datasets.md)
      + [Exemplos de consultas](using/data/datasets-query-examples.md)
      + [Esquemas incorporados >](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)
   + [Consultas](using/data/get-started-queries.md)
+ Configuração {#configuration}
   + [Introdução à configuração do Journey Optimizer](using/configuration/get-started-configuration.md)
   + Delegar subdomínios de email {#delegate-subdomains}
      + [Introdução à delegação de subdomínio](using/configuration/about-subdomain-delegation.md)
      + [Delegar um subdomínio](using/configuration/delegate-subdomain.md)
      + [Adicionar um registro TXT do Google](using/configuration/google-txt.md)
      + [Acessar e editar registros PTR](using/configuration/ptr-records.md)
      + [Criar pools de IP](using/configuration/ip-pools.md)
   + [Configurar superfícies do canal](using/configuration/channel-surfaces.md)
   + Monitorar endereços de email {#monitor-reputation}
      + [Lista de supressão](using/configuration/manage-suppression-list.md)
      + [Tentativas](using/configuration/retries.md)
      + [Lista de permissões](using/configuration/allow-list.md)
   + [Suporte para arquivamento](using/configuration/archiving-support.md)
   + [Configurar regras de frequência](using/configuration/frequency-rules.md)
   + [Gerenciar endereços de execução](using/configuration/primary-email-addresses.md)
   + Configurar jornadas {#configure-journeys}
      + [Sobre fontes de dados, eventos e ações](using/configuration/about-data-sources-events-actions.md)
      + Integrar a sistemas externos {#external-systems}
         + [Integração das jornadas com sistemas externos](using/configuration/external-systems.md)
         + [API de limitação](using/configuration/capping.md)
         + [API de limitação](using/configuration/throttling.md)
      + Configuração de evento {#events-journeys}
         + [Princípio geral](using/event/about-events.md)
         + Configurar um evento unitário {#unitary-events}
            + [Introdução a eventos unitários](using/event/about-creating.md)
            + [Sobre schemas ExperienceEvent](using/event/experience-event-schema.md)
            + [Compatível com o Adobe Analytics](using/event/about-analytics.md)
         + [Configurar um evento comercial](using/event/about-creating-business.md)
         + [Etapas adicionais para enviar eventos](using/event/additional-steps-to-send-events-to-journey.md)
      + Configuração de fonte de dados{#data-source-journeys}
         + [Sobre fontes de dados](using/datasource/about-data-sources.md)
         + [Configurar uma fonte de dados](using/datasource/configure-data-sources.md)
         + [Fonte de dados da Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Fontes de dados externas](using/datasource/external-data-sources.md)
      + Configuração de ação {#action-journeys}
         + [Sobre ações](using/action/action.md)
         + [Configurar uma ação](using/action/about-custom-action-configuration.md)
         + [Integrar ao Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrar ao Adobe Campaign v7/v8](using/action/acc-action.md)
         + [Sobre ações](using/action/action-response.md)
   + [Fontes](using/start/get-started-sources.md)
+ Controle de acesso {#access-control}
   + Visão geral do controle de acesso {#privacy}
      + [Introdução ao gerenciamento de usuários](using/administration/permissions-overview.md)
      + [Funções integradas](using/administration/ootb-product-profiles.md)
      + [Permissões integradas](using/administration/ootb-permissions.md)
      + [Níveis de permissão](using/administration/high-low-permissions.md)
   + [Gerenciar usuários e funções](using/administration/permissions.md)
   + [Controle de acesso baseado em atributos](using/administration/attribute-based-access.md)
   + [Controle de acesso no nível do objeto](using/administration/object-based-access.md)
   + [Gerenciamento de sandboxes](using/administration/sandboxes.md)
+ Privacidade {#privacy}
   + [Introdução à privacidade](using/privacy/get-started-privacy.md)
   + [Solicitações de privacidade](using/privacy/requests.md)
   + [Ações de auditoria em recursos](using/privacy/audit-logs.md)
   + [Executar operações de higiene de dados](using/privacy/data-hygiene.md)
   + Gerenciar consentimento {#consent}
      + [Gerenciar recusa](using/privacy/opt-out.md)
      + [Trabalhar com políticas de consentimento](using/action/consent.md)
   + [Governança de dados](using/action/action-privacy.md)
   + [Configurar e gerenciar Customer Managed Keys](using/privacy/cmk.md)