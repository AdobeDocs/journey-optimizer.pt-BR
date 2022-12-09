---
product: Journey Optimizer
audience: end-user
user-guide-title: Guia do Journey Otimizer
user-guide-description: Use o Journey Otimizer para criar e entregar experiências conectadas, contextuais e personalizadas para seus clientes
type: Documentation
solution: Journey Optimizer
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 0%

---

# Ajuda do Adobe Journey Otimizer {#using}

+ [Documentação do Journey Otimizer](ajo-home.md)
+ Quais são as novidades? {#whats-new}
   + [Notas de versão mais recentes](using/rn/release-notes.md)
   + Notas de versão anteriores {#previous-rn-new}
      + [Notas de versão de 2022](using/rn/release-notes-2022.md)
      + [Notas de versão de 2021](using/rn/release-notes-2021.md)
   + [Atualizações de documentação](using/rn/documentation-updates.md)
+ Introdução{#get-started}
   + [O que é o Journey Otimizer](using/start/get-started.md)
   + Guias de início rápido{#quick-start}
      + [Visão geral](using/start/quick-start.md)
      + [Introdução como profissional de marketing](using/start/path/marketer.md)
      + [Comece como um engenheiro de dados](using/start/path/data-engineer.md)
      + [Comece como um administrador](using/start/path/administrator.md)
      + [Introdução ao Developer](using/start/path/developer.md)
   + [Interface do usuário](using/start/user-interface.md)
   + [Integrações](using/start/ajo-integrations.md)
   + [Medidas de proteção](using/start/guardrails.md)
+ Jornadas {#orchestrate-journeys}
   + [Introdução a jornadas](using/building-journeys/journey.md)
   + Criar uma jornada{#create-journey}
      + [Criar sua primeira jornada](using/building-journeys/journey-gs.md)
      + [Projetar a jornada](using/building-journeys/using-the-journey-designer.md)
      + [Testar sua jornada](using/building-journeys/testing-the-journey.md)
      + [Publicar sua jornada](using/building-journeys/publishing-the-journey.md)
   + Gerenciar suas jornadas{#mannage-journey}
      + [Encerrar sua jornada](using/building-journeys/end-journey.md)
      + [Gerenciamento de fuso horário](using/building-journeys/timezone-management.md)
      + [Gerenciamento de entrada do perfil](using/building-journeys/entry-management.md)
      + [Copiar uma jornada para outra sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Solucionar problemas da sua jornada](using/building-journeys/troubleshooting.md)
      + [Integração com serviços inteligentes](using/building-journeys/ai-services-overview.md)
   + Atividades {#about-journey-building}
      + [Introdução às atividades de jornada](using/building-journeys/about-journey-activities.md)
      + [Eventos gerais](using/building-journeys/general-events.md)
      + [Reação](using/building-journeys/reaction-events.md)
      + [Qualificação do segmento](using/building-journeys/segment-qualification-events.md)
      + [Condição](using/building-journeys/condition-activity.md)
      + [Aguardar](using/building-journeys/wait-activity.md)
      + [Ler segmento](using/building-journeys/read-segment.md)
      + [Email, SMS, Push](using/building-journeys/journeys-message.md)
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
            + [currentTime &#x200B; InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [em](using/building-journeys/functions/functionin.md)
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
            + [length](using/building-journeys/functions/functionlength.md)
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
      + Casos de uso de negócios {#business-use-cases}
         + [Enviar mensagens de vários canais](using/building-journeys/journeys-uc.md)
         + [Enviar uma mensagem usando o Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Enviar uma mensagem aos assinantes](using/building-journeys/message-to-subscribers-uc.md)
      + Casos de uso técnico {#technical-use-cases}
         + [Envie coleções dinamicamente usando ações personalizadas](using/building-journeys/collections.md)
         + [Aumentar entregas](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limite a taxa de transferência com fontes de dados externas e ações personalizadas](using/building-journeys/limit-throughput.md)
+ Campanhas{#campaigns}
   + [Introdução a campanhas](using/campaigns/get-started-with-campaigns.md)
   + [Criar uma campanha](using/campaigns/create-campaign.md)
   + [Revisar e ativar uma campanha](using/campaigns/review-activate-campaign.md)
   + [Gerenciar campanhas](using/campaigns/modify-stop-campaign.md)
   + Experiência de conteúdo {#content-experiment}
      + [Introdução ao experimento de conteúdo](using/campaigns/get-started-experiment.md)
      + [Criar um experimento de conteúdo](using/campaigns/content-experiment.md)
      + [Entender cálculos estatísticos](using/campaigns/experiment-calculations.md)
      + [Configurar relatórios de experimentação](using/campaigns/reporting-configuration.md)
   + [Acione campanhas usando APIs](using/campaigns/api-triggered-campaigns.md)
+ Canal de email {#email}
   + [Comece a usar emails](using/email/get-started-email.md)
   + [Criar um email](using/email/create-email.md)
   + Projetar o conteúdo de email {#design-email}
      + [Introdução ao design de email](using/email/get-started-email-design.md)
      + Comece a criar conteúdo {#start-creating-content}
         + [Iniciar do zero](using/email/content-from-scratch.md)
         + [Importe o conteúdo do email](using/email/existing-content.md)
         + [Programe seu próprio conteúdo](using/email/code-content.md)
         + [Trabalhar com modelos](using/email/email-templates.md)
      + Projetar o conteúdo {#add-content}
         + [Usar componentes de conteúdo](using/email/content-components.md)
         + [Adicionar links e rastrear mensagens](using/email/message-tracking.md)
         + Gerenciar ativos {#manage-asset}
            + [Trabalhar com o Assets Essentials](using/email/assets-essentials.md)
            + [Trabalhar com o Adobe Stock](using/email/stock.md)
         + [Inserir ofertas personalizadas](using/email/add-offers-email.md)
         + [Gerar a versão de texto](using/email/text-version-email.md)
         + [Adicionar um precabeçalho](using/email/preheader.md)
      + Editar estilo {#edit-style}
         + [Introdução ao estilo de email](using/email/get-started-email-style.md)
         + [Editar configurações de fundo](using/email/backgrounds.md)
         + [Ajustar o alinhamento vertical e o preenchimento](using/email/alignment-and-padding.md)
         + [Definir um estilo para links](using/email/styling-links.md)
         + [Adicionar atributos de estilo em linha](using/email/inline-styling.md)
   + [Visualizar e testar seu email](using/email/preview.md)
   + [Gerenciar opção de não participação por email](using/email/email-opt-out.md)
   + Configurar canal de email {#configure-email}
      + [Introdução à configuração de email](using/email/get-started-email-config.md)
      + [Definir configurações de superfície de email](using/email/email-settings.md)
+ Canal no aplicativo{#in-app}
   + [Introdução ao canal no aplicativo](using/in-app/get-started-in-app.md)
   + [Configurar canal no aplicativo](using/in-app/inapp-configuration.md)
   + [Criar uma mensagem no aplicativo](using/in-app/create-in-app.md)
   + [Projetar o conteúdo no aplicativo](using/in-app/design-in-app.md)
   + [Relatório no aplicativo](using/in-app/inapp-report.md)
+ Canal de notificação por push{#push}
   + [Introdução à notificação por push](using/push/get-started-push.md)
   + [Criar uma notificação por push](using/push/create-push.md)
   + [Projetar a notificação por push](using/push/design-push.md)
   + [Enviar sua notificação por push](using/push/send-push.md)
   + Configurar notificações por push{#push-config}
      + [Notificações por push e Adobe Journey Otimizer](using/push/push-gs.md)
      + [Configurar canal de notificação por push](using/push/push-configuration.md)
+ Canal SMS{#sms}
   + [Introdução ao SMS](using/sms/get-started-sms.md)
   + [Criar uma mensagem SMS](using/sms/create-sms.md)
   + [Enviar uma mensagem SMS](using/sms/send-sms.md)
   + [Gerenciar a não participação no SMS](using/sms/sms-opt-out.md)
   + [Configurar canal SMS](using/sms/sms-configuration.md)
+ Correspondência direta {#direct-mail}
   + [Criar uma correspondência direta](using/direct-mail/create-direct-mail.md)
   + [Configurar correspondência direta](using/direct-mail/direct-mail-configuration.md)
+ Canal da Web{#web}
   + [Introdução ao canal da Web](using/web/get-started-web.md)
   + [Criar experiências da Web](using/web/create-web.md)
   + [Páginas da Web do autor](using/web/author-web.md)
   + [Extensão do Visual Editing Helper](using/web/visual-editing-helper.md)
   + [Relatórios da Web](using/web/web-report.md)
+ Landing pages {#landing-pages}
   + [Introdução às landing pages](using/landing-pages/get-started-lp.md)
   + [Criar uma landing page](using/landing-pages/create-lp.md)
   + Conteúdo do design {#landing-pages-design}
      + [Sobre o design da página de aterrissagem](using/landing-pages/design-lp.md)
      + [Criar o conteúdo da página de aterrissagem](using/landing-pages/lp-content.md)
      + [Criar modelos](using/landing-pages/lp-templates.md)
      + [Adicionar JavaScript personalizado](using/landing-pages/lp-custom-js.md)
   + [Criar uma lista de assinaturas](using/landing-pages/subscription-list.md)
   + [Saiba mais por meio de casos de uso](using/landing-pages/lp-use-cases.md)
   + Configurar landing pages {#lp-configuration}
      + [Configurar subdomínios de página de aterrissagem](using/landing-pages/lp-subdomains.md)
      + [Definir predefinições da landing page](using/landing-pages/lp-presets.md)
+ Personalização e conteúdo dinâmico {#personalized-dynamic-content}
   + Personalização {#personalization}
      + [Introdução à personalização](using/personalization/personalize.md)
      + [contextos de personalização](using/personalization/personalization-contexts.md)
      + Criar expressões {#build-expressions}
         + [Sintaxe de personalização](using/personalization/personalization-syntax.md)
         + Trabalhar com o Editor de expressão {#expression-editor}
            + [Sobre o Editor de expressão](using/personalization/personalization-build-expressions.md)
            + [Adicionar atributos aos favoritos](using/personalization/personalization-favorites.md)
            + [Trabalhar com expressões salvas](using/personalization/personalization-library.md)
            + [Validação de personalização](using/personalization/personalization-validation.md)
         + Funções auxiliares{#functions}
            + [Introdução a funções auxiliares](using/personalization/functions/functions.md)
            + [Funções de agregação](using/personalization/functions/aggregation.md)
            + [Funções aritméticas](using/personalization/functions/arithmetic-functions.md)
            + [Matrizes e funções de lista](using/personalization/functions/arrays-list.md)
            + [Funções de data](using/personalization/functions/dates.md)
            + [Funções booleanas e de comparação](using/personalization/functions/operators.md)
            + [Ajudantes](using/personalization/functions/helpers.md)
            + [Funções do mapa](using/personalization/functions/maps.md)
            + [Funções do objeto](using/personalization/functions/objects.md)
            + [Funções da string](using/personalization/functions/string.md)
      + Casos de uso{#personalization-use-cases}
         + [Notificação do status do pedido](using/personalization/personalization-use-case.md)
         + [Email de abandono do carrinho](using/personalization/personalization-use-case-helper-functions.md)
   + Conteúdo dinâmico {#dynamic}
      + [Introdução ao conteúdo dinâmico](using/personalization/get-started-dynamic-content.md)
      + [Criar regras condicionais](using/personalization/create-conditions.md)
      + [Criar conteúdo dinâmico](using/personalization/dynamic-content.md)
+ Segmentos, perfis e identidade{#segment}
   + Segmentos {#segments}
      + [Introdução a segmentos](using/segment/about-segments.md)
      + [Construir segmentos](using/segment/creating-a-segment.md)
   + Perfis{#profiles}
      + [Introdução a perfis](using/segment/get-started-profiles.md)
      + [Criar perfis de teste](using/segment/creating-test-profiles.md)
   + [Identidades](using/segment/get-started-identity.md)
   + Compor públicos-alvo {#audience-orchestration}
      + [Introdução à composição do público-alvo](using/segment/get-started-audience-orchestration.md)
      + [Criar workflows de composição](using/segment/create-compositions.md)
      + [Trabalhar com a tela de composição](using/segment/composition-canvas.md)
      + [Acessar e gerenciar públicos](using/segment/access-audiences.md)
   + [Uso da licença](using/segment/license-usage.md)
+ Rastrear e monitorar {#reporting}
   + Relatório ao vivo {#live-report}
      + [Introdução ao Relatório ao vivo](using/reports/live-report.md)
      + [Relatório de jornada ao vivo](using/reports/journey-live-report.md)
      + [Relatório ao vivo da campanha](using/reports/campaign-live-report.md)
      + [Relatório ao vivo da página de aterrissagem](using/reports/lp-report-live.md)
      + [Relatório ao vivo da lista de assinaturas](using/reports/subscription-report-live.md)
   + Relatório global {#global-report}
      + [Introdução ao Relatório global](using/reports/global-report.md)
      + [Relatório de jornada global](using/reports/journey-global-report.md)
      + [Relatório de campanha global](using/reports/campaign-global-report.md)
      + [Relatório global da página de aterrissagem](using/reports/lp-report-global.md)
      + [Relatório Global da Lista de Subscrições](using/reports/subscription-report-global.md)
   + Relatórios de jornada {#reports}
      + [Criar relatórios de jornada](using/reports/sharing-overview.md)
      + [Lista de campos de evento de etapa](using/reports/sharing-field-list.md)
      + Campos de evento de etapa herdada {#legacy-step-event-fields}
         + [Sobre campos herdados](using/reports/sharing-legacy-fields.md)
         + [Campos de jornada](using/reports/sharing-journey-fields.md)
         + [Campos comuns](using/reports/sharing-common-fields.md)
         + [Campos de execução de ação](using/reports/sharing-execution-fields.md)
         + [Campos de busca de dados](using/reports/sharing-fetch-fields.md)
         + [Campos de identidade](using/reports/sharing-identity-fields.md)
      + [Exemplos de consultas](using/reports/query-examples.md)
   + Capacidade de entrega {#deliverability}
      + [Introdução à capacidade de entrega](using/reports/deliverability.md)
      + [Entender a lista de supressão](using/reports/suppression-list.md)
   + [Alertas](using/reports/alerts.md)
   + [Trabalhar com o Customer Journey Analytics](using/reports/cja-ajo.md)
+ Gestão de decisões {#offer-decisioning}
   + Introdução ao Gerenciamento de decisões {#get-started-decision}
      + [Sobre o Gerenciamento de decisões](using/offers/get-started/starting-offer-decisioning.md)
      + [Interface do usuário](using/offers/get-started/user-interface.md)
      + [Etapas principais para criar e gerenciar ofertas](using/offers/offer-library/key-steps.md)
      + [Caso de uso: inserir ofertas em um email](using/offers/offers-e2e.md)
   + Criar componentes {#create-components}
      + [Criar disposições](using/offers/offer-library/creating-placements.md)
      + [Criar regras de decisão](using/offers/offer-library/creating-decision-rules.md)
      + [Criar tags](using/offers/offer-library/creating-tags.md)
   + Criar classificações {#rankings}
      + [Introdução às classificações](using/offers/ranking/get-started-rankings.md)
      + [Fórmulas de classificação](using/offers/ranking/create-ranking-formulas.md)
      + Modelos de IA {#ai-models}
         + [Sobre modelos de IA](using/offers/ranking/ai-models.md)
         + Tipos de modelo de IA {#ai-model-types}
            + [Modelo de otimização automática](using/offers/ranking/auto-optimization-model.md)
            + [Modelo de otimização personalizado](using/offers/ranking/personalized-optimization-model.md)
         + Criar modelos de IA {#configure-ai-model}
            + [Criar um conjunto de dados para coletar eventos](using/offers/ranking/create-dataset.md)
            + [Criar um modelo de IA](using/offers/ranking/create-ranking-strategies.md)
            + [Configurar captura de eventos](using/offers/ranking/schema-requirement.md)
   + Criar e gerenciar ofertas {#managing-offers-in-the-offer-library}
      + Configurar ofertas {#configure-offers}
         + [Criar ofertas personalizadas](using/offers/offer-library/creating-personalized-offers.md)
         + [Adicionar representações](using/offers/offer-library/add-representations.md)
         + [Adicionar restrições](using/offers/offer-library/add-constraints.md)
      + [Criar ofertas de fallback](using/offers/offer-library/creating-fallback-offers.md)
      + [Criar coleções](using/offers/offer-library/creating-collections.md)
   + Criar e gerenciar decisões {#create-manage-activities}
      + [Criar decisões](using/offers/offer-activities/create-offer-activities.md)
      + [Configurar seleção de ofertas em decisões](using/offers/offer-activities/configure-offer-selection.md)
      + [Criar simulações](using/offers/offer-activities/simulation.md)
   + [Decisão em lote](using/offers/batch-delivery.md)
   + Criar relatórios do Gerenciamento de decisões {#create-reports}
      + [Introdução aos eventos de gerenciamento de decisões](using/offers/reports/get-started-events.md)
      + [Informações-chave sobre eventos do Gerenciamento de decisões](using/offers/reports/key-information.md)
      + [Acessar campos XDM de eventos](using/offers/reports/xdm-fields.md)
   + Exportar seu catálogo de ofertas {#export-catalog}
      + [Introdução à exportação de catálogo de ofertas ](using/offers/export-catalog/get-started-export.md)
      + [Acessar o catálogo de ofertas exportado](using/offers/export-catalog/access-dataset.md)
      + [Conjunto de dados de ofertas personalizadas](using/offers/export-catalog/export-offers.md)
      + [Conjunto de dados Decisões](using/offers/export-catalog/export-decisions.md)
      + [Conjunto de dados Disposições](using/offers/export-catalog/export-placements.md)
      + [Conjunto de dados de fallback](using/offers/export-catalog/export-fallback.md)
   + Referência da API {#api-reference}
      + [Introdução](using/offers/api-reference/getting-started.md)
      + Criar e gerenciar ofertas usando APIs {#offers-api}
         + Posicionamentos {#placements}
            + [Listar disposições](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Pesquisar uma inserção](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Criar uma disposição](using/offers/api-reference/offers-api/placements/create.md)
            + [Atualizar uma inserção](using/offers/api-reference/offers-api/placements/update.md)
            + [Excluir uma disposição](using/offers/api-reference/offers-api/placements/delete.md)
         + Regras de decisão {#decision-rules}
            + [Lista de regras de decisão](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Pesquisar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Criar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Atualizar uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Excluir uma regra de decisão](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Tags {#tags}
            + [Listar tags](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Pesquisar uma tag](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Criar uma tag](using/offers/api-reference/offers-api/tags/create.md)
            + [Atualizar uma tag](using/offers/api-reference/offers-api/tags/update.md)
            + [Excluir uma tag](using/offers/api-reference/offers-api/tags/delete.md)
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
         + Ofertas de fallback {#fallback-offers}
            + [Listar ofertas de fallback](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Pesquisar uma oferta de fallback](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Criar uma oferta de fallback](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Atualizar uma oferta de fallback](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Excluir uma oferta de fallback](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Criar e gerenciar decisões usando APIs {#activities-api}
         + [Listar decisões](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Pesquisar uma decisão](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Criar uma decisão](using/offers/api-reference/activities-api/activities/create.md)
         + [Atualizar uma decisão](using/offers/api-reference/activities-api/activities/update.md)
         + [Excluir uma decisão](using/offers/api-reference/activities-api/activities/delete.md)
      + Fornecer ofertas usando APIs {#offer-delivery-api}
         + [Introdução às APIs de entrega de oferta](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [API de decisão](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API do Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API de decisão em lote](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Gestão de dados {#data-management}
   + [Introdução ao gerenciamento de dados](using/data/gs-data.md)
   + [Trabalhar com esquemas](using/data/get-started-schemas.md)
   + Conjuntos de dados do Journey Otimizer {#datasets}
      + [Introdução a conjuntos de dados](using/data/get-started-datasets.md)
      + [Exemplos de query](using/data/datasets-query-examples.md)
   + [Queries](using/data/get-started-queries.md)
+ Configuração{#configuration}
   + [Introdução à configuração do Journey Otimizer](using/configuration/get-started-configuration.md)
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
      + [Lista permitida](using/configuration/allow-list.md)
   + [Suporte para arquivamento](using/configuration/archiving-support.md)
   + [Configurar regras de frequência](using/configuration/frequency-rules.md)
   + [Gerenciar endereços de execução](using/configuration/primary-email-addresses.md)
   + Configurar jornadas {#configure-journeys}
      + [Sobre fontes de dados, eventos e ações](using/configuration/about-data-sources-events-actions.md)
      + [Integração com sistemas externos](using/configuration/external-systems.md)
      + Configuração do evento {#events-journeys}
         + [Princípio geral](using/event/about-events.md)
         + Configurar um evento unitário {#unitary-events}
            + [Introdução a eventos unitários](using/event/about-creating.md)
            + [Sobre schemas ExperienceEvent](using/event/experience-event-schema.md)
            + [Aproveite o Adobe Analytics](using/event/about-analytics.md)
         + [Configurar um evento comercial](using/event/about-creating-business.md)
         + [Etapas adicionais para enviar eventos](using/event/additional-steps-to-send-events-to-journey.md)
      + Configuração da fonte de dados{#data-source-journeys}
         + [Sobre fontes de dados](using/datasource/about-data-sources.md)
         + [Configurar uma fonte de dados](using/datasource/configure-data-sources.md)
         + [Fonte de dados da Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Fontes de dados externas](using/datasource/external-data-sources.md)
      + Configuração de ação {#action-journeys}
         + [Sobre ações](using/action/action.md)
         + [Configurar uma ação](using/action/about-custom-action-configuration.md)
         + [Integração com o Adobe Campaign Standard](using/action/acs-action.md)
         + [Integração com o Adobe Campaign v7/v8](using/action/acc-action.md)
   + [Fontes](using/start/get-started-sources.md)
+ Controle de acesso {#access-control}
   + [Visão geral do controle de acesso](using/administration/permissions-overview.md)
   + [Perfis de produto incorporados](using/administration/ootb-product-profiles.md)
   + [Gerenciar usuários e perfis de produtos](using/administration/permissions.md)
   + [Níveis de permissão](using/administration/high-low-permissions.md)
   + [Gerenciamento de sandboxes](using/administration/sandboxes.md)
   + [Controle de acesso baseado em atributos](using/administration/attribute-based-access.md)
   + [Controle de acesso no nível do objeto](using/administration/object-based-access.md)
+ Privacidade {#privacy}
   + [Introdução à privacidade](using/privacy/get-started-privacy.md)
   + [Solicitações de privacidade](using/privacy/requests.md)
   + [Ações de auditoria sobre recursos](using/privacy/audit-logs.md)
   + Gerenciar consentimento {#consent}
      + [Gerenciar recusa](using/privacy/opt-out.md)
      + [Trabalhar com políticas de consentimento](using/action/consent.md)
   + [Governança de dados](using/action/action-privacy.md)
