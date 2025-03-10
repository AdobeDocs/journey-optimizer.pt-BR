---
product: Journey Optimizer
audience: end-user
user-guide-title: Guia do Journey Optimizer
user-guide-description: Use o Journey Optimizer para criar e fornecer experiências conectadas, contextuais e personalizadas aos clientes
type: Documentation
solution: Journey Optimizer
source-git-commit: 170dd966ae9fe9721a92bdebccd76305ad6fa1dc
workflow-type: tm+mt
source-wordcount: '2251'
ht-degree: 89%

---

# Ajuda do Adobe Journey Optimizer {#using}

+ [Documentação do Journey Optimizer](ajo-home.md)
+ Novidades {#whats-new}
   + [Notas de versão antecipadas](using/rn/e-release-notes.md)
   + [Notas de versão mais recentes](using/rn/release-notes.md)
   + Notas de versão anteriores {#previous-rn-new}
      + [2024](using/rn/release-notes-2024.md)
      + [2023](using/rn/release-notes-2023.md)
      + [2022](using/rn/release-notes-2022.md)
      + [2021](using/rn/release-notes-2021.md)
   + [Atualizações na documentação](using/rn/documentation-updates.md)
   + [Tela de jornada aprimorada](using/rn/new-canvas.md)
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
   + [Manuais de casos de uso ](using/start/playbooks.md)
   + [Trabalhar com o assistente de IA](using/start/ai-assistant.md)
   + [Medidas de proteção](using/start/guardrails.md)
   + [Práticas recomendadas](using/start/best-practices.md)
+ Jornadas {#orchestrate-journeys}
   + [Introdução a jornadas](using/building-journeys/journey.md)
   + Criar uma jornada{#create-journey}
      + [Criar a primeira jornada](using/building-journeys/journey-gs.md)
      + [Definir as propriedades da jornada](using/building-journeys/journey-properties.md)
      + [Projetar a jornada](using/building-journeys/using-the-journey-designer.md)
      + [Teste a jornada](using/building-journeys/testing-the-journey.md)
      + [Simular a jornada](using/building-journeys/journey-simulation.md)
      + [Publicar a jornada](using/building-journeys/publishing-the-journey.md)
      + [Relatório em tempo real na sua jornada](using/building-journeys/report-journey.md)
   + Gerenciar suas jornadas{#manage-journey}
      + [Procurar e filtrar suas jornadas](using/building-journeys/journey-ui.md)
      + [Gerenciamento de entrada de perfis](using/building-journeys/entry-management.md)
      + [Gerenciamento de fuso horário](using/building-journeys/timezone-management.md)
      + [Otimização de tempo de envio](using/building-journeys/send-time-optimization.md)
      + [Encerrar sua jornada](using/building-journeys/end-journey.md)
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
      + [Ações de canal integradas](using/building-journeys/journeys-message.md)
      + [Ações personalizadas](using/building-journeys/using-custom-actions.md)
      + [Ações do Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Ações do Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [Salto](using/building-journeys/jump.md)
      + [Atualizar perfil](using/building-journeys/update-profiles.md)
   + Criar expressões {#building-advanced-conditions-journeys}
      + [Trabalhar com o editor de expressão avançado](using/building-journeys/expression/expressionadvanced.md)
      + Sintaxe {#syntax}
         + [Sintaxe do editor de expressão avançado](using/building-journeys/expression/generalities.md)
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
            + [inAudience](using/building-journeys/functions/functioninaudience.md)
         + Agregação {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [contagem](using/building-journeys/functions/functioncount.md)
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
            + [currentTimeInMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
         + [Limitar a taxa de transferência com fontes de dados externas e ações personalizadas](using/building-journeys/limit-throughput.md)
         + [Usar ações personalizadas para gravar eventos de jornada no Experience Platform](using/building-journeys/custom-action-aep.md)
+ Campanhas em várias etapas {#ms-campaigns}
   + [Introdução a campanhas com várias etapas](using/ms/gs-ms-campaigns.md)
   + Crie sua primeira campanha em várias etapas {#create-ms-campaign}
      + [Princípios fundamentais](using/ms/gs-campaign-creation.md)
      + [Medidas de proteção e limitações](using/ms/guardrails.md)
      + [Criar a campanha](using/ms/create-ms-campaign.md)
      + [Orquestrar atividades](using/ms/orchestrate-activities.md)
      + [Definir configurações da campanha](using/ms/ms-campaign-settings.md)
      + [Iniciar e monitorar suas campanhas](using/ms/start-monitor-campaigns.md)
      + [Variáveis de evento em campanhas com várias etapas](using/ms/event-variables.md)
   + Atividades de campanha em várias etapas {#design-campaigns}
      + [Sobre atividades de campanha em várias etapas](using/ms/activities/about-activities.md)
      + [And-join](using/ms/activities/and-join.md)
      + [Criar público-alvo](using/ms/activities/build-audience.md)
      + [Mudar dimensão](using/ms/activities/change-dimension.md)
      + [Combinar](using/ms/activities/combine.md)
      + [Desduplicação](using/ms/activities/deduplication.md)
      + [Ações do canal](using/ms/activities/channels.md)
      + [Enriquecimento](using/ms/activities/enrichment.md)
      + [Bifurcação](using/ms/activities/fork.md)
      + [Carregar arquivo](using/ms/activities/load-file.md)
      + [Reconciliação](using/ms/activities/reconciliation.md)
      + [Salvar público-alvo](using/ms/activities/save-audience.md)
      + [Scheduler](using/ms/activities/scheduler.md)
      + [Divisão](using/ms/activities/split.md)
      + [Teste](using/ms/activities/test.md)
      + [Atualizar dados](using/ms/activities/update-data.md)
      + [Aguardar](using/ms/activities/wait.md)
+ Campanhas {#campaigns}
   + [Introdução às campanhas](using/campaigns/get-started-with-campaigns.md)
   + [Criar uma campanha](using/campaigns/create-campaign.md)
   + [Revisar e ativar uma campanha](using/campaigns/review-activate-campaign.md)
   + [Gerenciar campanhas](using/campaigns/modify-stop-campaign.md)
   + [Acione campanhas usando APIs](using/campaigns/api-triggered-campaigns.md)
+ Gerenciamento de conflitos e priorização {#conflict-prioritization}
   + [Introdução ao gerenciamento de conflitos e priorização](using/conflict-prioritization/gs-conflict-prioritization.md)
   + [Identificar possíveis conflitos](using/conflict-prioritization/conflicts.md)
   + [Atribuir pontuações de prioridade](using/conflict-prioritization/priority-scores.md)
   + [Limite e arbitragem de jornada](using/conflict-prioritization/journey-capping.md)
+ Testar e aprovar {#test}
   + Visualizar e testar o conteúdo {#preview-test}
      + [Introdução à visualização e teste](using/content-management/preview-test.md)
      + [Seleção de perfis de teste](using/content-management/test-profiles.md)
      + [Visualização do conteúdo](using/content-management/preview.md)
      + [Envio de provas de email](using/content-management/proofs.md)
      + [Teste da renderização do email](using/content-management/rendering.md)
      + [Teste o conteúdo usando exemplos de dados de entrada (Beta)](using/test-approve/simulate-sample-input.md)
      + [Relatório de spam de email](using/content-management/spam-report.md)
   + Aprovar jornadas e campanhas {#approve}
      + [Introdução a aprovações](using/test-approve/gs-approval.md)
      + [Criar e gerenciar políticas de aprovação](using/test-approve/approval-policies.md)
      + [Solicitar aprovação](using/test-approve/request-approval.md)
      + [Aprovar uma solicitação](using/test-approve/review-approve-request.md)
+ Canais de comunicação {#channels}
   + [Introdução a canais de comunicação](using/channels/gs-channels.md)
   + Canal de email {#email}
      + [Introdução a emails](using/email/get-started-email.md)
      + [Criar um email](using/email/create-email.md)
      + Projetar o conteúdo de email {#design-email}
         + [Introdução ao design de email](using/email/get-started-email-design.md)
         + Começar a criar conteúdo {#start-creating-content}
            + [Crie um conteúdo do zero](using/email/content-from-scratch.md)
            + [Importar seu conteúdo](using/email/existing-content.md)
            + [Programar seu próprio conteúdo](using/email/code-content.md)
            + [Usar modelos de email](using/email/use-email-templates.md)
         + Projetar o conteúdo {#add-content}
            + [Usar componentes de conteúdo](using/email/content-components.md)
            + [Aproveitar fragmentos visuais](using/email/use-visual-fragments.md)
            + [Adicionar links e rastrear mensagens](using/email/message-tracking.md)
            + [Inserir ofertas personalizadas](using/email/add-offers-email.md)
            + [Gerar a versão de texto](using/email/text-version-email.md)
            + [Adicionar um pré-cabeçalho](using/email/preheader.md)
         + Editar estilo {#edit-style}
            + [Introdução ao estilo de email](using/email/get-started-email-style.md)
            + [Editar configurações de fundo](using/email/backgrounds.md)
            + [Ajustar alinhamento vertical e preenchimento](using/email/alignment-and-padding.md)
            + [Adicionar atributos de estilo incorporado](using/email/inline-styling.md)
      + [Gerenciar opção de não participação de email](using/email/email-opt-out.md)
      + Configurar canal de email {#configure-email}
         + [Introdução à configuração de email](using/email/get-started-email-config.md)
         + [Definir a configuração de email](using/email/email-settings.md)
         + [Habilitar cancelamento de assinatura em lista](using/email/list-unsubscribe.md)
         + [Parâmetros de cabeçalho](using/email/header-parameters.md)
         + [Rastreamento de URL](using/email/url-tracking.md)
         + [Personalizar configurações de email](using/email/surface-personalization.md)
   + Canal no aplicativo{#in-app}
      + [Introdução ao canal no aplicativo](using/in-app/get-started-in-app.md)
      + [Pré-requisitos do canal no aplicativo](using/in-app/inapp-configuration.md)
      + [Criar uma mensagem para o aplicativo móvel](using/in-app/create-in-app.md)
      + [Criar uma mensagem para o aplicativo web](using/in-app/create-in-app-web.md)
      + [Criar seu conteúdo no aplicativo](using/in-app/design-in-app.md)
      + [Marque e envie sua notificação no aplicativo](using/in-app/send-in-app.md)
   + Canal de notificação por push{#push}
      + [Introdução à notificação por push](using/push/get-started-push.md)
      + [Criar uma notificação por push](using/push/create-push.md)
      + [Projetar a notificação por push](using/push/design-push.md)
      + [Marque e envie sua notificação por push](using/push/send-push.md)
      + Configuração de notificações por push{#push-config}
         + [Fluxo de notificação por push](using/push/push-gs.md)
         + [Configurar canal de notificação por push](using/push/push-configuration.md)
         + [Fluxo de trabalho de início rápido de integração para dispositivos móveis](using/push/mobile-onboarding-wf.md)
   + Canal SMS/MMS{#sms}
      + [Introdução a mensagem de texto](using/sms/get-started-sms.md)
      + [Criação de uma mensagem de texto (SMS/MMS)](using/sms/create-sms.md)
      + [Verificar e enviar suas mensagens de texto](using/sms/send-sms.md)
      + [Gerenciamento da opção de não participação de mensagem de texto](using/sms/sms-opt-out.md)
      + [Configurar os subdomínios de SMS](using/sms/sms-subdomains.md)
      + Configurar canal de SMS/MMS{#configure-sms}
         + [Introdução à configuração de SMS](using/sms/sms-configuration.md)
         + [Configurar provedor Sinch](using/sms/sms-configuration-sinch.md)
         + [Configurar provedor Infobip](using/sms/sms-configuration-infobip.md)
         + [Configurar provedor Twilio](using/sms/sms-configuration-twilio.md)
         + [Configurar um provedor personalizado (Beta)](using/sms/sms-configuration-custom.md)
         + [Criar uma configuração de SMS](using/sms/sms-configuration-surface.md)
   + Correspondência direta {#direct-mail}
      + [Introdução à correspondência direta](using/direct-mail/get-started-direct-mail.md)
      + [Criação de uma correspondência direta](using/direct-mail/create-direct-mail.md)
      + [Marque e envie uma mensagem de correspondência direta](using/direct-mail/test-send-direct-mail.md)
      + [Configurar correspondência direta](using/direct-mail/direct-mail-configuration.md)
   + Canal da Web {#web}
      + [Introdução ao canal Web](using/web/get-started-web.md)
      + Configurar o canal web {#configure-web-channel}
         + [Pré-requisitos do canal web](using/web/web-prerequisites.md)
         + [Configurar subdomínios da Web](using/web/web-delegated-subdomains.md)
         + [Criar configuração do canal da Web](using/web/web-configuration.md)
      + [Criação de experiências da web](using/web/create-web.md)
      + Criação de páginas da web {#author-web-pages}
         + [Trabalhar com o web designer](using/web/web-visual-editor.md)
         + [Usar o editor não visual](using/web/web-non-visual-editor.md)
         + [Gerenciar modificações](using/web/manage-web-modifications.md)
         + [Monitorar suas campanhas da Web](using/web/monitor-web-experiences.md)
         + [Criar aplicativos de página única](using/web/web-spa.md)
   + Experiência baseada em código {#code-based-experience}
      + [Introdução ao canal baseado em código](using/code-based/get-started-code-based.md)
      + Configurar canal baseado em código {#configure-code-based-channel}
         + [Medidas de proteção e pré-requisitos](using/code-based/code-based-prerequisites.md)
         + [Superfícies de experiência baseada em código](using/code-based/code-based-surface.md)
         + [Amostras de métodos de implementação](using/code-based/code-based-implementation-samples.md)
         + [Criar configuração de experiência baseada em código](using/code-based/code-based-configuration.md)
      + Criar experiências baseadas em código {#create-code-based-experiences}
         + [Criar e compor experiências baseadas em código](using/code-based/create-code-based.md)
         + [Testar experiências baseadas em código](using/code-based/test-code-based.md)
         + [Gerenciar experiências baseadas em código](using/code-based/publish-code-based.md)
   + Cartões de conteúdo{#content-card}
      + [Introdução aos cartões de conteúdo](using/content-card/get-started-content-card.md)
      + Configurar canal de cartão de conteúdo {#configure}
         + [Pré-requisitos dos cartões de conteúdo](using/content-card/content-card-configuration-prereq.md)
         + [Configurar canal de cartões de conteúdo no Journey Optimizer](using/content-card/content-card-configuration.md)
         + [Configurar o suporte a cartões de conteúdo no SDK da Web](using/content-card/content-card-configuration-sdk.md)
      + [Criar cartões de conteúdo](using/content-card/create-content-card.md)
      + [Design de cartões de conteúdo](using/content-card/design-content-card.md)
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
+ Gestão de conteúdo {#content-management}
   + Assistente de IA para geração de conteúdo{#ai-assistant}
      + [Introdução ao Assistente de IA](using/content-management/gs-generative.md)
      + [Geração de email com IA](using/content-management/generative-email.md)
      + [Geração de push com IA](using/content-management/generative-push.md)
      + [Geração de SMS com IA](using/content-management/generative-sms.md)
      + [Geração na Web com IA](using/content-management/generative-web.md)
      + [Experimento de conteúdo com IA](using/content-management/generative-experimentation.md)
      + [Página de aterrissagem com IA](using/content-management/generative-lp.md)
      + [Casos de uso do Assistente de IA](using/content-management/generative-uc.md)
      + [Criar e gerenciar suas marcas (Beta)](using/content-management/brands.md)
   + Trabalhar com conteúdo multilíngue{#content-multilingual}
      + [Introdução ao conteúdo multilíngue](using/content-management/multilingual-gs.md)
      + [Criar uma localização](using/content-management/multilingual-locale.md)
      + [Criar um provedor de idioma](using/content-management/multilingual-provider.md)
      + [Criação do conteúdo multilíngue com tradução manual](using/content-management/multilingual-manual.md)
      + [Criação do conteúdo multilíngue com tradução automática](using/content-management/multilingual-automated.md)
   + Trabalho com experimento de conteúdo {#content-experiment}
      + [Introdução ao experimento de conteúdo](using/content-management/get-started-experiment.md)
      + [Criar um experimento de conteúdo](using/content-management/content-experiment.md)
      + Notas técnicas {#technotes}
         + [Compreenda cálculos estatísticos](using/content-management/experiment-calculations.md)
         + [Compreenda cálculos estatísticos no Relatório de experimentação](using/content-management/experiment-report-calculations.md)
   + Personalização {#personalization}
      + [Introdução à personalização](using/personalization/personalize.md)
      + [Contextos de personalização](using/personalization/personalization-contexts.md)
      + [Sintaxe de personalização](using/personalization/personalization-syntax.md)
      + [Usar dados da Adobe Experience Platform para personalização (Beta)](using/personalization/lookup-aep-data.md)
      + Trabalhar com o editor de personalização {#expression-editor}
         + [Sobre o editor de personalização](using/personalization/personalization-build-expressions.md)
         + [Adicionar atributos aos favoritos](using/personalization/personalization-favorites.md)
         + [Usar fragmentos de expressão](using/personalization/use-expression-fragments.md)
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
      + Casos de uso de personalização{#personalization-use-cases}
         + [Notificação do status do pedido](using/personalization/personalization-use-case.md)
         + [Email de abandono do carrinho](using/personalization/personalization-use-case-helper-functions.md)
         + [Email de receitas do plano de saúde](using/personalization/perso-uc-plan-prescriptions.md)
   + Modelos de conteúdo {#content-templates}
      + [Introdução aos modelos de conteúdo](using/content-management/content-templates.md)
      + [Acessar e gerenciar modelos ](using/content-management/access-content-templates.md)
      + [Criar modelos de conteúdo](using/content-management/create-content-templates.md)
      + [Bloquear conteúdo em modelos de email](using/content-management/content-locking.md)
      + [Testar modelos de conteúdo](using/content-management/test-content-templates.md)
      + [Usar modelos de conteúdo](using/content-management/use-content-templates.md)
   + Fragmentos de conteúdo reutilizáveis {#fragments}
      + [Introdução a fragmentos](using/content-management/fragments.md)
      + [Criar um fragmento](using/content-management/create-fragments.md)
      + [Salvar conteúdo como fragmento](using/content-management/save-fragments.md)
      + [Fragmentos personalizáveis](using/content-management/customizable-fragments.md)
      + [Gerenciar fragmentos](using/content-management/manage-fragments.md)
   + Conteúdo dinâmico {#dynamic}
      + [Introdução ao conteúdo dinâmico](using/personalization/get-started-dynamic-content.md)
      + [Criar regras condicionais](using/personalization/create-conditions.md)
      + [Criar conteúdo dinâmico](using/personalization/dynamic-content.md)
+ Públicos, perfis e identidade{#audiences-profiles-identities}
   + Públicos-alvo {#audiences}
      + [Introdução aos públicos-alvo](using/audience/about-audiences.md)
      + Criar públicos-alvo {#create}
         + [Definições de segmento](using/audience/creating-a-segment-definition.md)
         + [Composição de público-alvo](using/audience/get-started-audience-orchestration.md)
         + [Upload personalizado](using/audience/custom-upload.md)
         + [Composição de público-alvo federado](using/audience/federated-audience-composition.md)
      + [Ativação de público-alvo em campanhas e jornadas](using/audience/target-audiences.md)
      + [Usar atributos de enriquecimento](using/audience/enrichment-attributes.md)
   + Perfis{#profiles}
      + [Introdução aos perfis](using/audience/get-started-profiles.md)
      + [Criar perfis de teste](using/audience/creating-test-profiles.md)
      + [Trabalhar com atributos computados](using/audience/computed-attributes.md)
   + [Identidades](using/audience/get-started-identity.md)
   + [Uso da licença](using/audience/license-usage.md)
+ Integrações{#assets-images}
   + [Integrações com outras soluções](using/integrations/ajo-integrations.md)
   + [Trabalho com o Experience Manager Assets](using/integrations/assets.md)
   + [Trabalho com o Adobe Stock](using/integrations/stock.md)
   + [Trabalhar com modelos do Experience Manager](using/integrations/aem-templates.md)
   + [Trabalhar com fragmentos de conteúdo do Experience Manager](using/integrations/aem-fragments.md)
   + [Trabalhar com o Dynamic Media](using/integrations/aem-dynamic.md)
+ Rastrear e monitorar {#reporting}
   + Relatório ao vivo {#live-report}
      + [Introdução aos relatórios em tempo real](using/reports/live-report.md)
      + [Lista de componentes](using/reports/live-report-components.md)
      + [Relatório da jornada em tempo real](using/reports/journey-live-report.md)
      + [Relatório em tempo real da campanha](using/reports/campaign-live-report.md)
      + [Relatório em tempo real da página de destino](using/reports/lp-report-live.md)
      + [Relatório em tempo real da lista de assinaturas](using/reports/subscription-report-live.md)
   + Relatório de tempo total{#channel-report}
      + [Introdução ao relatório de tempo total](using/reports/report-gs-cja.md)
      + [Configurar o Customer Journey Analytics manualmente](using/reports/cja-ajo.md)
      + [Gerenciar seus relatórios](using/reports/report-cja-manage.md)
      + [Pré-requisitos de relatórios e experimentação](using/reports/reporting-configuration.md)
      + Relatórios de campanha{#reporting}
         + [Relatório de campanha](using/reports/campaign-global-report-cja.md)
         + [Relatório de campanha baseada em código](using/reports/campaign-global-report-cja-code.md)
         + [Relatório de campanha de cartão de conteúdo](using/reports/campaign-global-report-cja-content.md)
         + [Relatório de campanha de correspondência direta](using/reports/campaign-global-report-cja-direct.md)
         + [Relatório de campanha por email](using/reports/campaign-global-report-cja-email.md)
         + [Relatório de campanha de experimentação](using/reports/campaign-global-report-cja-experimentation.md)
         + [Relatório de campanha no aplicativo](using/reports/campaign-global-report-cja-inapp.md)
         + [Relatório de campanha com notificação por push](using/reports/campaign-global-report-cja-push.md)
         + [Relatório de campanha por SMS](using/reports/campaign-global-report-cja-sms.md)
         + [Relatório de campanha na web](using/reports/campaign-global-report-cja-web.md)
      + Relatórios de jornada{#reporting}
         + [Relatório de jornada](using/reports/journey-global-report-cja.md)
         + [Relatório de jornada baseado em código](using/reports/journey-global-report-cja-code.md)
         + [Relatório de jornada de cartão de conteúdo](using/reports/journey-global-report-cja-content.md)
         + [Relatório de jornada de correspondência direta](using/reports/journey-global-report-cja-direct.md)
         + [Relatório de jornada por email](using/reports/journey-global-report-cja-email.md)
         + [Relatório de jornada no aplicativo](using/reports/journey-global-report-cja-inapp.md)
         + [Relatório de jornada por push](using/reports/journey-global-report-cja-push.md)
         + [Relatório de jornada de SMS](using/reports/journey-global-report-cja-sms.md)
         + [Relatório de jornada na web](using/reports/journey-global-report-cja-web.md)
      + [Relatório de visão geral](using/reports/channel-report-cja.md)
      + [Relatório de páginas de destino](using/reports/lp-report-global-cja.md)
      + [Relatório da lista de assinaturas](using/reports/subscription-report-global-cja.md)
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
      + [Novo requisito DMARC](using/configuration/dmarc-record-update.md)
   + [Alertas](using/reports/alerts.md)
   + [Motivos de exclusão](using/reports/exclusion-list.md)
+ Recursos de decisão {#decisioning}
   + [Introdução aos recursos de decisão](using/experience-decisioning/gs-decision.md)
   + Decisões {#experience-decisioning}
      + [Introdução ao serviço de Decisão](using/experience-decisioning/gs-experience-decisioning.md)
      + [Medidas de proteção e limitações da decisão](using/experience-decisioning/decisioning-guardrails.md)
      + Referência da API{#api-reference}
         + Criar e gerenciar itens de oferta {#create-manage}
            + Itens de decisão{#decision-items}
               + [Criar itens de decisão](using/experience-decisioning/api-reference/decisions-items/create.md)
               + [Lista de itens de decisão](using/experience-decisioning/api-reference/decisions-items/decision-items-list.md)
               + [Excluir itens de decisão](using/experience-decisioning/api-reference/decisions-items/delete.md)
               + [Pesquisar itens de decisão](using/experience-decisioning/api-reference/decisions-items/lookup.md)
               + [Atualizar itens de decisão](using/experience-decisioning/api-reference/decisions-items/update.md)
            + Coleções de itens{#items-collections}
               + [Criar coleções de itens](using/experience-decisioning/api-reference/items-collections/create.md)
               + [Excluir coleções de itens](using/experience-decisioning/api-reference/items-collections/delete.md)
               + [Lista de coleções de itens](using/experience-decisioning/api-reference/items-collections/items-collections-list.md)
               + [Pesquisar coleções de itens](using/experience-decisioning/api-reference/items-collections/lookup.md)
               + [Atualizar coleções de itens](using/experience-decisioning/api-reference/items-collections/update.md)
            + Estratégias de seleção{#selection-strategies}
               + [Criar estratégias de seleção](using/experience-decisioning/api-reference/selection-strategies/create.md)
               + [Excluir estratégias de seleção](using/experience-decisioning/api-reference/selection-strategies/delete.md)
               + [Pesquisar estratégias de seleção](using/experience-decisioning/api-reference/selection-strategies/lookup.md)
               + [Lista de estratégias de seleção](using/experience-decisioning/api-reference/selection-strategies/selection-strategies-list.md)
               + [Atualizar estratégias de seleção](using/experience-decisioning/api-reference/selection-strategies/update.md)
         + [Fornecer ofertas usando o canal de experiência baseada em código](using/experience-decisioning/api-reference/deliver.md)
      + Gerenciar itens de decisão {#decision-items}
         + [Configurar o catálogo de itens](using/experience-decisioning/catalogs.md)
         + [Criar itens de decisão](using/experience-decisioning/items.md)
         + [Gerenciar coleções de itens](using/experience-decisioning/collections.md)
      + Configurar a seleção de itens {#selection}
         + [Criar regras de decisão](using/experience-decisioning/rules.md)
         + [Criar métodos de classificação](using/experience-decisioning/ranking.md)
         + [Aproveitar dados de contexto](using/experience-decisioning/context-data.md)
      + [Criar estratégias de seleção](using/experience-decisioning/selection-strategies.md)
      + [Criar políticas de decisão](using/experience-decisioning/create-decision.md)
      + [Relatório de decisões](using/experience-decisioning/cja-reporting.md)
      + [Caso de uso de decisão](using/experience-decisioning/experience-decisioning-uc.md)
   + Gestão de decisões {#offer-decisioning}
      + Introdução ao Gestão de decisões {#get-started-decision}
         + [Sobre a Gestão de decisões](using/offers/get-started/starting-offer-decisioning.md)
         + [Medidas de proteção e limitações de gerenciamento de decisão](using/offers/decision-management-guardrails.md)
         + [Interface do usuário](using/offers/get-started/user-interface.md)
         + [Etapas principais para criar e gerenciar ofertas](using/offers/offer-library/key-steps.md)
         + [Usar públicos-alvo de upload personalizados para a tomada de decisão](using/offers/custom-upload-decisioning.md)
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
      + Aproveitar dados de contexto {#context-data}
         + [Introdução aos dados de contexto](using/offers/context-data.md)
         + [Dados de contexto e solicitações de decisão do Edge](using/offers/context-data-edge.md)
         + [Solicitação de decisão e dados de contexto](using/offers/context-data-decisioning.md)
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
            + Decisões {#decisions-api}
               + [Listar decisões](using/offers/api-reference/activities-api/activities/activities-list.md)
               + [Pesquisar uma decisão](using/offers/api-reference/activities-api/activities/lookup.md)
               + [Criar uma decisão](using/offers/api-reference/activities-api/activities/create.md)
               + [Atualizar uma decisão](using/offers/api-reference/activities-api/activities/update.md)
               + [Excluir uma decisão](using/offers/api-reference/activities-api/activities/delete.md)
            + APIs herdadas {#legacy-api}
               + [Sobre APIs herdadas](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
               + Posicionamentos {#placements}
                  + [Listar inserções](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
                  + [Pesquisar uma inserção](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
                  + [Criar uma inserção](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
                  + [Atualizar uma inserção](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
                  + [Excluir uma inserção](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
               + Regras de decisão {#decision-rules}
                  + [Listar de regras de decisão](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
                  + [Pesquisar uma regra de decisão](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
                  + [Criar uma regra de decisão](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
                  + [Atualizar uma regra de decisão](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
                  + [Excluir uma regra de decisão](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
               + Qualificadores de coleção {#tags}
                  + [Listar qualificadores de coleção](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
                  + [Pesquisar um qualificador de coleção](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
                  + [Criar um qualificador de coleção](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
                  + [Atualizar um qualificador de coleção](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
                  + [Excluir um qualificador de coleção](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
               + Ofertas personalizadas {#personalized-offers}
                  + [Listar ofertas personalizadas](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
                  + [Pesquisar uma oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
                  + [Criar uma oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
                  + [Atualizar uma oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
                  + [Excluir uma oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
               + Ofertas substitutas {#fallback-offers}
                  + [Listar ofertas substitutas](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
                  + [Pesquisar uma oferta substituta](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
                  + [Criar uma oferta substituta](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
                  + [Atualizar uma oferta substituta](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
                  + [Excluir uma oferta substituta](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
               + Coleções {#collections}
                  + [Listar coleções](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
                  + [Pesquisar uma coleção](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
                  + [Criar uma coleção](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
                  + [Atualizar uma coleção](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
                  + [Excluir uma coleção](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
               + Decisões {#decisions-api}
                  + [Listar decisões](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
                  + [Pesquisar uma decisão](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
                  + [Criar uma decisão](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
                  + [Atualizar uma decisão](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
                  + [Excluir uma decisão](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
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
      + [Proteções de TTL (Time-to-live) dos conjuntos de dados](using/data/datasets-ttl.md)
      + [Exportar conjuntos de dados do Journey Optimizer](using/data/export-datasets.md)
      + [Exemplos de consultas](using/data/datasets-query-examples.md)
      + [Esquemas incorporados >](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)
   + [Consultas](using/data/get-started-queries.md)
+ Configuração {#configuration}
   + [Introdução à configuração do Journey Optimizer](using/configuration/get-started-configuration.md)
   + [Definir configurações de canal](using/configuration/channel-surfaces.md)
   + Configuração de canal guiada {#guided-setup}
      + [Introdução à configuração de canal guiada](using/configuration/set-mobile-config.md)
      + [Criar uma configuração de canal](using/configuration/create-channel-set-up.md)
   + Delegar subdomínios de email {#delegate-subdomains}
      + [Introdução à delegação de subdomínio](using/configuration/about-subdomain-delegation.md)
      + [Delegar um subdomínio](using/configuration/delegate-subdomain.md)
      + [Configurar o registro DMARC](using/configuration/dmarc-record.md)
      + [Adicionar um registro TXT do Google](using/configuration/google-txt.md)
      + [Acessar e editar registros PTR](using/configuration/ptr-records.md)
      + [Criar pools de IP](using/configuration/ip-pools.md)
   + Implementar um plano de aquecimento de IP {#implement-ip-warmup-plan}
      + [Introdução aos planos de aquecimento de IP](using/configuration/ip-warmup-gs.md)
      + [Criar campanhas de aquecimento de IP](using/configuration/ip-warmup-campaign.md)
      + [Criar um plano de aquecimento de IP](using/configuration/ip-warmup-plan.md)
      + [Executar o plano de aquecimento de IP](using/configuration/ip-warmup-execution.md)
      + [Arquivos de plano de aquecimento de IP](using/configuration/ip-warmup-plan-files.md)
   + Monitorar endereços de email {#monitor-reputation}
      + [Lista de supressão](using/configuration/manage-suppression-list.md)
      + [Tentativas](using/configuration/retries.md)
      + [Lista de permissões](using/configuration/allow-list.md)
   + [Usar listas de seeds](using/configuration/seed-lists.md)
   + [Suporte para arquivamento](using/configuration/archiving-support.md)
   + [Alterar endereços de execução](using/configuration/primary-email-addresses.md)
   + [Configurar regra de negócios](using/configuration/frequency-rules.md)
   + [Trabalhar com conjuntos de regras](using/configuration/rule-sets.md)
   + Configurar jornadas {#configure-journeys}
      + [Configurar fontes de dados, eventos e ações](using/configuration/about-data-sources-events-actions.md)
      + Integração a sistemas externos {#external-systems}
         + [Integração das jornadas com sistemas externos](using/configuration/external-systems.md)
         + [API de limitação](using/configuration/capping.md)
         + [API de limitação](using/configuration/throttling.md)
      + Configuração de evento {#events-journeys}
         + [Trabalhar com eventos de jornada](using/event/about-events.md)
         + Configurar um evento unitário {#unitary-events}
            + [Introdução a eventos unitários](using/event/about-creating.md)
            + [Sobre schemas ExperienceEvent](using/event/experience-event-schema.md)
            + [Compatível com o Adobe Analytics](using/event/about-analytics.md)
         + [Configurar um evento comercial](using/event/about-creating-business.md)
         + [Etapas adicionais para enviar eventos](using/event/additional-steps-to-send-events-to-journey.md)
      + Configuração de fonte de dados{#data-source-journeys}
         + [Introdução a fontes de dados](using/datasource/about-data-sources.md)
         + [Configurar uma fonte de dados](using/datasource/configure-data-sources.md)
         + [Fonte de dados da Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Fontes de dados externas](using/datasource/external-data-sources.md)
      + Configuração de ação {#action-journeys}
         + [Introdução a ações personalizadas](using/action/action.md)
         + [Configurar uma ação personalizada](using/action/about-custom-action-configuration.md)
         + [Solução de problemas de uma ação personalizada](using/action/troubleshoot-custom-action.md)
         + [Usar as respostas de chamada da API em ações personalizadas](using/action/action-response.md)
         + [Integrar ao Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrar ao Adobe Campaign v7/v8](using/action/acc-action.md)
         + [Integrar com o Marketo Engage](using/action/marketo-engage.md)
   + [Origens](using/start/get-started-sources.md)
   + [Exportar objetos para outra sandbox](using/configuration/copy-objects-to-sandbox.md)
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
   + [Executar operações de ciclo de vida de dados](using/privacy/data-hygiene.md)
   + Gerenciar consentimento {#consent}
      + [Gerenciar recusa](using/privacy/opt-out.md)
      + [Trabalhar com políticas de consentimento](using/action/consent.md)
   + [Governança de dados](using/action/action-privacy.md)
   + [Configurar e gerenciar chaves gerenciadas pelo cliente](using/privacy/cmk.md)
