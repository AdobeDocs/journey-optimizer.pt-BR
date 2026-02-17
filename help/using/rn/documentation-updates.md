---
solution: Journey Optimizer
product: journey optimizer
title: Atualizações de documentação
description: Conheça as atualizações de documentação mais recentes
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 7cfeabc85b9645be9d61ed6458e57e42ea319619
workflow-type: tm+mt
source-wordcount: '3330'
ht-degree: 84%

---

# Atualizações na documentação {#latest-updates}

Esta página lista todas as alterações mais recentes na documentação do [!DNL Journey Optimizer], além das atualizações relacionadas aos recursos e melhorias da versão mensal.

## Fevereiro de 2026 {#february-2026}

* A página Integração de sistemas externos foi atualizada com links para fontes de dados personalizadas e ações personalizadas, e esclarece que o proxy de saída fornece um IP estático para chamadas de saída de **Ações personalizadas** para seus sistemas externos. [Leia mais](../configuration/external-systems.md)

* A documentação do Jornada Dry run foi esclarecida: os atributos de evento de etapa `inDryRun` e `dryRunID` agora documentam que eles retornam `true`/ID de instância quando estão no modo Dry run e `null` para jornadas de teste ou ativas. As orientações para excluir eventos de etapa Dry run em consultas de relatório foram atualizadas adequadamente. [Leia mais](../building-journeys/journey-dry-run.md)

* **Push da Web** agora está disponível. A documentação de notificação por push foi reestruturada e atualizada adequadamente (começar, projetar, enviar, criar). [Leia mais](../push/get-started-push.md)

* A página de configuração de push da Web agora está disponível na documentação. [Leia mais](../push/push-configuration-web.md)

* A documentação sobre o uso de fragmentos no Decisioning foi atualizada: notas foram adicionadas nas seções Fragmentos e Decisão, e a página Fragmentos em políticas de decisão foi atualizada. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

* A documentação do webhook de SMS foi atualizada: o conteúdo do webhook do Twilio foi removido. [Leia mais](../sms/sms-webhook.md)

* A documentação da API de migração do Decisioning foi atualizada. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

* A atividade **Decisão de Conteúdo** agora está disponível. A página de atividade Decisão de conteúdo foi atualizada com uma seção sobre Dados de decisão disponíveis nos eventos de etapa. [Leia mais](../building-journeys/content-decision.md)

* Links para a documentação da API de desafio de fidelidade foram adicionados à seção Desafios de fidelidade (começar, criar desafios, criar tarefas, acessar desafios de fidelidade). [Leia mais](../loyalty-challenges/get-started.md)

* As informações de canais compatíveis na documentação do assistente de criação de campanha foram corrigidas. As páginas de perguntas frequentes sobre Introdução aos canais e Campanhas orquestradas foram atualizadas adequadamente. [Leia mais](../campaigns/get-started-with-campaigns.md)

* A documentação de permissões foi corrigida com relação às permissões **Gerenciador de Jornadas** e **Aprovar**. [Leia mais](../administration/ootb-permissions.md)

* A documentação de integrações do AEM (Adobe Experience Manager) foi atualizada com nomes revisados (conteúdo dinâmico do AEM e fragmentos do AEM). [Leia mais](../integrations/aem-fragments.md)

* Um novo motivo de exclusão foi adicionado à lista de exclusões: **UnsubscribeLinkNotValid** (código de erro 050081). Essa exclusão é gerada quando o tamanho do assunto do mailTo List-Unsubscribe é maior que o limite RFC de 998 caracteres. [Leia mais](../reports/exclusion-list.md)

* A documentação da função auxiliar formatDate foi aprimorada com uma observação de que a função requer um tipo de campo de data-hora (não uma sequência de caracteres) e com vários exemplos: formatação de um campo de data-hora, conversão de uma sequência de caracteres em data primeiro, data completa com nome de dia, data dinâmica a partir da hora do sistema e formato de dia da semana, incluindo saída em minúsculas. [Leia mais](../personalization/functions/dates.md#format-date)

* A documentação de email da versão em texto foi aprimorada com orientação abrangente para casos de uso, incluindo critérios de decisão para quando usar texto simples personalizado versus sincronização automática, exemplos práticos com cenários do mundo real e uma seção de perguntas frequentes com perguntas comuns. [Leia mais](../email/text-version-email.md#when-to-use)

* Uma limitação foi adicionada à documentação de ajuda Metadados de execução para esclarecer que os metadados não são capturados para perfis excluídos da ação. [Leia mais](../personalization/functions/helpers.md#execution-metadata)

* A documentação de amostras de implementação baseada em código foi atualizada para incluir o campo de tokens na propositionAction para rastreamento e atribuição precisos na Decisão. [Leia mais](../code-based/code-based-implementation-samples.md#client-side-how)

* Uma observação foi adicionada à documentação de rastreamento de URL e cancelamento de inscrição da lista para esclarecer que a ordem dos parâmetros de rastreamento de URL anexados aos URLs é aleatória e não pode ser controlada. [Leia mais](../email/url-tracking.md)

* A documentação Email Designer themes foi atualizada com informações sobre limitações de suporte a fontes da Web e a importância de fontes de fallback. [Leia mais](../email/apply-email-themes.md#themes-guardrails)

## Janeiro de 2026 {#january-2026}

* A documentação do painel de uso da licença foi esclarecida com orientações atualizadas sobre os **Perfis envolventes**, incluindo detalhes de definição e orientações para solução de problemas. [Leia mais](../audience/license-usage.md#what-is-engageable-profile)

* Uma observação foi adicionada à documentação de temas do Email Designer para esclarecer as limitações de suporte a fontes da Web. [Leia mais](../email/apply-email-themes.md#themes-guardrails)

* Uma nova seção de proteção foi adicionada ao documento validação do tamanho do conteúdo da jornada, incluindo limites de aviso e erro e orientação sobre como otimizar as jornadas. [Leia mais](../start/guardrails.md#journey-payload-size)

* A documentação de medidas de proteção do Decisioning foi atualizada para incluir limitações de tamanho de itens de decisão (1 KB para itens que incluem atributos com no máximo 30 atributos). [Leia mais](../experience-decisioning/decisioning-guardrails.md)

* Uma observação foi adicionada à documentação de criação de políticas de decisão para informar aos usuários que, uma vez criada uma política de decisão, qualquer alteração poderá levar até 15 minutos para se propagar em todas as regiões de dados e até 30 minutos para o Canadá. [Leia mais](../experience-decisioning/create-decision-policy.md#review)

* Uma observação foi adicionada à documentação de fragmentos para avisar que quando o rótulo do botão e o URL se tornam editáveis em um fragmento, o conjunto de dados de rastreamento registra o valor do URL em vez do valor do rótulo. [Leia mais](../content-management/customizable-fragments.md#visual)

* Uma nova página está disponível descrevendo os benefícios da migração da Gestão de decisões para o Decisioning, incluindo informações sobre as próximas APIs de ferramentas de migração. [Leia mais](../experience-decisioning/migrate-to-decisioning.md)

* Adição de uma medida de proteção para esclarecer que os conjuntos de dados de pesquisa estão disponíveis para ativação baseada na borda de entrada somente na região em que a sandbox do conjunto de dados reside. [Leia mais](../data/lookup-aep-data.md#guidelines)

* Uma nova seção foi adicionada à documentação de configuração de canais de Campanhas orquestradas explicando como usar atributos contextuais (como ID da campanha, nome e detalhes de ação) em parâmetros de rastreamento de URL para fins de análise e relatórios. [Leia mais](../orchestrated/channel-config.md#url-tracking)

* A documentação de otimização de conteúdo foi reestruturada para oferecer mais clareza. A página de otimização principal foi dividida em quatro subpáginas focadas: uma página de introdução, uma página dedicada ao direcionamento, uma para experimentação e outra para combinação de ambas as abordagens. [Leia mais](../content-management/gs-message-optimization.md)

* As notas de Disponibilidade limitada foram removidas dos três alertas de jornada (Jornada publicada, Jornada concluída e Limite de ação personalizada acionado), pois esses recursos agora estão disponíveis. [Leia mais](../reports/alerts.md)

* A página de destino Testar, validar e aprovar foi aprimorada com novas seções, incluindo: visão geral dos recursos de teste, perguntas frequentes comuns, árvore de decisão com links de navegação e terminologia aprimorada com links da documentação. [Leia mais](../../rp_landing_pages/test-landing-page.md)

* Uma nova seção foi adicionada à documentação da sintaxe de personalização para esclarecer como usar palavras-chave reservadas em expressões de personalização. Determinadas palavras-chave no PQL, como `next`, `last` e `this`, devem ser delimitadas com sinal grave quando usadas como nomes de campo no esquema XDM. [Leia mais](../personalization/personalization-syntax.md#reserved-keywords)

* As páginas [Introdução às campanhas](../campaigns/get-started-with-campaigns.md) e [Gerenciar campanhas](../campaigns/manage-campaigns.md) foram reestruturadas com uma arquitetura de informações aprimorada, incluindo um fluxo de trabalho abrangente com guias específicos de tipo, comparações aprimoradas de tipos de campanha e uma tabela de status consolidada.

* A página de destino Jornadas foi reprojetada para facilitar a integração com um novo fluxo de trabalho de 6 etapas, comparações melhoradas de tipos de jornada e a navegação aprimorada em toda a documentação. [Leia mais](../building-journeys/journey.md)

* Uma seção detalhada foi adicionada para ajudar os usuários a gerar chaves privadas OpenSSH codificadas em Base64 para autenticação SFTP ao configurar o roteamento de arquivos para Correspondência direta, evitando erros de conexão. [Leia mais](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Uma observação foi adicionada à documentação de delegação de subdomínio para orientar os usuários a permitir a propagação de DNS por 24 a 48 horas antes da tentativa de delegação à Adobe. [Leia mais](../configuration/delegate-subdomain.md#set-up-subdomain)

## Dezembro de 2025 {#december-2025}

* A documentação Públicos-alvo de upload personalizado para decisões foi atualizada com a inclusão de um sinalizador de API exigido para a recuperação de dados de enriquecimento. Ao usar públicos-alvo carregados em CSV na definição de ofertas, é necessário incluir `"xdm:enrichedAudience": true` no conteúdo da solicitação de API para recuperar atributos de enriquecimento na resposta de decisão da oferta. [Leia mais](../offers/custom-upload-decisioning.md#must-read)

* Uma observação foi adicionada na documentação de envio de prova para esclarecer que as regras de limite de frequência se aplicam às provas. A página agora inclui uma seção &quot;Leitura obrigatória&quot; com considerações importantes sobre o comportamento do limite de frequência, limitações da mirror page e regras de acessibilidade de ativos. [Leia mais](../content-management/proofs.md)

* Uma nova tabela de disponibilidade de canais de comunicação foi adicionada à página Introdução aos canais, exibindo quais canais são compatíveis com jornadas e campanhas (Campanhas de ação, Campanhas acionadas por API e Campanhas orquestradas). [Leia mais](../channels/gs-channels.md#channels)

* Uma nova página de destino de rastreamento abrangente foi criada para ajudar os usuários a descobrir e acessar todos os recursos de rastreamento e monitoramento disponíveis no Journey Optimizer. [Leia mais](../start/get-started-tracking.md)

* A página de gerenciamento da recusa de email foi aprimorada com informações detalhadas sobre o fluxo de cancelamento de assinatura, explicando a ordem esperada dos eventos para a recusa na página de destino. [Leia mais](../email/email-opt-out.md#send-message-unsubscribe-link)

* A documentação da lista de assinaturas foi atualizada para incluir informações sobre os critérios de elegibilidade do segmento de transmissão. [Leia mais](../landing-pages/subscription-list.md#define-subscription-list)

* Um novo guia de capacidade de entrega do aquecimento de IP está disponível, fornecendo orientação abrangente sobre fundamentos de reputação, preparação inicial, métricas de monitoramento e práticas recomendadas para a transição de uma reputação nula para um posicionamento bem-sucedido da caixa de entrada. [Leia mais](../configuration/ip-warmup-deliverability-guide.md)

* Um aviso foi adicionado às seções Página de destino e Recusa de email para esclarecer que clicar em um link de cancelamento de assinatura apenas abre a página de destino. Os usuários devem enviar o formulário para concluir o processo de recusa. [Leia mais](../landing-pages/lp-use-cases.md#configure-opt-out)

* Uma nova biblioteca de casos de uso de jornadas está disponível, reunindo uma coleção de casos de uso práticos, incluindo padrões táticos (lógica de supressão, técnicas de personalização, estratégias de saída de jornada) e cenários completos de ponta a ponta que abrangem fluxos de trabalho técnicos e de marketing. [Leia mais](../building-journeys/jo-use-cases.md)

* Um novo caso de uso está disponível demonstrando como configurar uma jornada para enviar emails somente em dias da semana (de segunda a sexta-feira), com enfileiramento automático para entradas do fim de semana a serem enviadas na segunda-feira em um horário especificado. [Leia mais](../building-journeys/weekday-email-uc.md)

* Uma nova página agora está disponível para explicar os recursos de decisão do Journey Optimizer, incluindo as diferenças entre a estrutura de decisão de última geração e a solução de Gestão de decisões estabelecida, além dos seus principais benefícios para o fornecimento de ofertas personalizadas nos canais. [Leia mais](../experience-decisioning/gs-decision.md)

* Uma nova seção foi adicionada à documentação de ativação de público-alvo, explicando como ativar tipos de público-alvo não compatíveis (como públicos-alvo do Customer Journey Analytics) no [!DNL Journey Optimizer], vinculando-os a uma nova definição de segmento no Portal de público-alvo. [Leia mais](../audience/target-audiences.md#activation-non-supported)

* Uma nova seção foi adicionada à documentação da atividade de espera, explicando como os perfis estacionados em uma atividade de espera nas jornadas de Público-alvo de leitura atualizam automaticamente seus atributos no Serviço de perfil unificado (UPS). Isso esclarece que os dados do perfil podem mudar durante a execução da jornada após um nó de espera, o que pode produzir resultados inesperados se houver a expectativa de dados de instantâneo consistentes em toda a jornada. [Leia mais](../building-journeys/wait-activity.md#profile-refresh)

* Uma observação de advertência foi adicionada à seção Experimentação de caminho, advertindo os usuários a não editar os metadados de um experimento de caminho depois de publicado, pois isso interromperá o cálculo e o relatório dos resultados do experimento. [Leia mais](../building-journeys/optimize.md#experimentation)

* Uma observação foi adicionada à seção Criar uma predefinição de formulário para especificar os requisitos das conexões de transmissão a serem exibidas na lista suspensa de seleção. [Leia mais](../landing-pages/lp-forms.md#create-form-preset)

* Uma nova página agora está disponível na seção Decisão, informando sobre como configurar a coleta de dados para rastrear impressões, cliques e eventos personalizados. [Leia mais](../experience-decisioning/data-collection/schema-requirement.md)

* A documentação da Geração de conteúdo com o Assistente de IA foi reorganizada para melhorar a clareza e a usabilidade. As cinco páginas específicas de canais anteriores (Email, Push, SMS, Web e Página de destino) foram consolidadas em três páginas por tipo de geração: [Gerar conteúdo completo](../content-management/generative-full-content.md), [Gerar texto](../content-management/generative-text.md) e [Gerar imagens](../content-management/generative-image.md).

## Novembro de 2025 {#november-2025}

* Uma nova página de Perguntas frequentes sobre decisões agora está disponível, abordando tópicos como regras de limites, configuração de modelo de IA, requisitos de tráfego e estratégias de otimização de ofertas. [Leia mais](../experience-decisioning/decisioning-faq.md)

* A página Introdução ao design de email foi atualizada para esclarecer como acessar o Designer de email. [Leia mais](../email/get-started-email-design.md)

* Uma seção de solução de problemas foi adicionada à página de registro DMARC para abordar a latência de propagação de DNS. [Leia mais](../configuration/dmarc-record.md#troubleshooting)

* A página Trabalhar com o GenStudio for Performance Marketing foi aprimorada com novas seções que incluem: recursos principais, casos de uso comuns, pré-requisitos e perguntas frequentes. [Leia mais](../integrations/genstudio.md)

* Uma medida de proteção sobre como direcionar perfis pseudônimos com canais de entrada foi adicionada à página Medidas de proteção e limitações: direcionar visitantes não autenticados aumenta a contagem total de perfis engajáveis, portanto, a Adobe recomenda definir um Tempo de vida (TTL) para a exclusão automática de perfis com o fim de gerenciar os custos associados. [Leia mais](../start/guardrails.md#profile-management-inbound)

* Dois tutoriais sobre como configurar o SDK da web para decisões e experiências baseadas em código agora são referenciados na página Amostras de métodos de implementação baseados em código. [Leia mais](../code-based/code-based-decisioning-implementations.md#tutorials)

* Uma observação foi adicionada para especificar que os ativos e as imagens permanecem acessíveis por até 2 anos (730 dias) a partir da primeira publicação e exigem uma nova publicação após a expiração. [Leia mais](../content-management/proofs.md)

* Um guia abrangente de prompts de conteúdo do Assistente de IA agora está disponível. Este guia ensina como elaborar prompts eficazes para criar conteúdo de marketing com alta capacidade de conversão e alinhado à marca. Conheça as práticas recomendadas para criar objetivos de marketing, usar ativos da marca e otimizar conteúdo para diferentes canais. [Leia mais](../content-management/ai-assistant-prompting-guide.md)

* Uma observação foi adicionada à documentação de definição de segmento para esclarecer que o atributo `frequencyMap` não é compatível para uso em definições de segmento e não pode ser usado como parte dos critérios de segmentação de público-alvo. Para direcionamento baseado em frequência, considere usar regras de limite de frequência em regras de negócios. [Leia mais](../audience/creating-a-segment-definition.md)
* Um novo exemplo que mostra como usar respostas de ação personalizadas em canais nativos foi adicionado à documentação de respostas de chamada da API. O exemplo demonstra como iterar sobre matrizes aninhadas de respostas de ação personalizadas com a sintaxe do Handlebars em mensagens de email, push e SMS. [Leia mais](../action/action-response.md#response-in-channels)

* Uma nova seção foi adicionada à documentação de integração do Campaign v7/v8 explicando como atualizar ações personalizadas existentes quando o ponto de acesso em tempo real (RT) mudar. A seção inclui instruções passo a passo para atualizar o URL do ponto de acesso, testar a conexão e validar as alterações antes de salvar. [Leia mais](../action/acc-action.md#update-action)

* Novas seções de limitações e práticas recomendadas foram adicionadas à documentação de fragmentos visuais para avisar os usuários sobre o aninhamento não compatível de fragmentos que contêm conteúdo dinâmico dentro de outros fragmentos desbloqueados com conteúdo dinâmico. As orientações incluem etapas de solução de problemas para o modo de compatibilidade e recomendações para o design adequado da estrutura do email. [Leia mais](../email/use-visual-fragments.md#fragment-dynamic-content)

* Uma seção de solução de problemas foi adicionada à documentação dos relatórios em tempo real da jornada para ajudar os usuários a resolver problemas com dados de relatórios ausentes. A seção abrange a sincronização do nome da jornada com conjuntos de dados de relatórios, cronograma de atualização de dados, verificação de permissões de acesso e requisitos de status da jornada. [Leia mais](../building-journeys/report-journey.md#troubleshooting-missing-data)

* Três novos itens de perguntas frequentes foram adicionados à documentação de ativos, explicando a expiração dos ativos e o gerenciamento do ciclo de vida. Os tópicos abordados incluem a política de tempo de vida (TTL) para ativos do AEM (730 dias), como corrigir imagens corrompidas devido à expiração de ativos e informações sobre melhorias futuras na lógica de expiração de ativos. [Leia mais](../integrations/assets.md#faq-assets)

* Uma seção abrangente de solução de problemas foi adicionada à documentação da atividade Público-alvo de leitura para solucionar as incompatibilidades na contagem de público-alvo de perfis estimados e reais que entram nas jornadas. A seção aborda problemas de cronograma e propagação de dados, técnicas de monitoramento e validação de dados e práticas recomendadas, incluindo o uso da opção “Acionar após a avaliação de público-alvo em lote”. [Leia mais](../building-journeys/read-audience.md#audience-count-mismatch)

* Uma observação foi adicionada à documentação de eventos de qualificação de público-alvo para esclarecer a latência da segmentação de transmissão (até 2 horas) e recomendar a adição de uma atividade Aguardar ou um tempo de buffer para jornadas urgentes. [Leia mais](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* Uma nova seção foi adicionada às medidas de proteção de email que documentam o limite de tamanho do conteúdo de mensagens de 2 MB para publicação na jornada, incluindo as práticas recomendadas para manter o conteúdo criado abaixo de 1 MB e permitir a sobrecarga do processamento de back-end. [Leia mais](../start/guardrails.md#message-content-size)

* Aprimoramento da documentação da opção de Leitura incremental nas atividades de público-alvo de leitura para esclarecer as dependências de cronograma de instantâneo e a limitação de retrospectiva de 24 horas, incluindo recomendações para evitar a perda de perfis. [Leia mais](../building-journeys/read-audience.md)

* Uma observação foi adicionada às medidas de proteção de pesquisa do conjunto de dados para especificar que as pesquisas não podem ser encadeadas. [Leia mais](../data/lookup-aep-data.md#guidelines)

* Os canais WhatsApp e LINE agora estão disponíveis para campanhas de ação. [Leia mais](../campaigns/campaign-content.md)

* Uma nova seção abrangente sobre a taxa de processamento da jornada foi adicionada à documentação de gerenciamento de entradas, abordando as taxas de entrada de perfil, os eventos e as qualificações de público-alvo dentro das jornadas, o impacto das atividades de espera e o impacto das atividades de ação. [Leia mais](../building-journeys/entry-management.md#journey-processing-rate)

* Ao projetar mensagens de email, o sistema agora verifica as principais configurações e exibe alertas de avisos e erros. Informações sobre alertas de email e requisitos de validação foram adicionadas à página Medidas de proteção. [Leia mais](../email/create-email.md#check-email-alerts)

* A nota de advertência informando que o limite de frequência não pode ser habilitado ou desabilitado para ofertas criadas anteriormente foi removida da página Adicionar restrições a uma oferta. [Leia mais](../offers/offer-library/add-constraints.md#capping)

* A documentação sobre como trabalhar com eventos de etapa da jornada agora está disponível. [Leia mais](../reports/journey-step-events-overview.md)

* Um novo guia abrangente sobre os critérios de entrada e saída da jornada está disponível, abordando práticas recomendadas, exemplos reais e orientação prática para gerenciar quando os perfis entram e saem das jornadas no Adobe Journey Optimizer. [Leia mais](../building-journeys/entry-exit-criteria-guide.md)

* Uma nova página que explica como iterar sobre dados contextuais em mensagens está disponível. Este guia aborda como usar a sintaxe Handlebars para exibir listas dinâmicas de eventos, respostas de ações personalizadas, pesquisas de conjuntos de dados e outras fontes de contexto na personalização. [Leia mais](../personalization/iterate-contextual-data.md)

* A consulta para identificar eventos descartados nas jornadas foi corrigida para incluir filtros adequados para erros do trabalho de exportação de segmento, descartes do Dispatcher e descartes da máquina de estados. [Leia mais](../reports/query-examples.md#common-queries)

* Frases introdutórias foram adicionadas a todos os 37 exemplos de consulta na documentação de exemplos de consulta para fornecer melhor contexto e explicar o que cada consulta faz antes de apresentar o código SQL. Isso melhora a compreensão do usuário e fornece uma orientação mais clara sobre quando usar cada consulta. [Leia mais](../reports/query-examples.md)

## Outubro de 2025 {#october-2025}

* Agora é possível converter imagens em modelos HTML usando o conversor de imagem para HTML. [Leia mais](../content-management/image-to-html.md)

* As informações sobre o ciclo de lançamento do Adobe Journey Optimizer agora estão disponíveis. [Leia mais](releases.md)

* Uma nova página de perguntas frequentes sobre jornadas agora está disponível. [Leia mais](../building-journeys/journey-faq.md)

* A funcionalidade Monitorar ações personalizadas agora está disponível. [Leia mais](../action/reporting.md)

* O modo de alta taxa de transferência para campanhas acionadas por API agora está disponível. [Leia mais](../campaigns/api-triggered-high-throughput.md)

* Uma referência de códigos de erro para jornadas está disponível. [Leia mais](../building-journeys/error-codes-reference.md)

* A documentação do Journey Optimizer Experimentation Accelerator agora está disponível. [Leia mais](../content-management/experiment-accelerator-gs.md)

* Uma nova seção foi adicionada à documentação da função auxiliar **formatDate**. Esta seção esclarece o significado dos principais símbolos de padrão como y, Y, M, d e D. [Leia mais](../personalization/functions/dates.md#pattern-characters)

* Um exemplo de PQL foi adicionado à seção Fórmula de classificação de decisão para mostrar como aumentar as ofertas com base no CEP e na receita anual de um perfil. [Leia mais](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* Uma limitação foi adicionada à seção modo de teste da jornada para mencionar que o modo de teste não é compatível com o enriquecimento de atributo de público-alvo com upload personalizado. [Leia mais](../building-journeys/testing-the-journey.md#important_notes)

* Uma nova seção foi adicionada às páginas [Medidas de proteção e limitações da Gestão de decisões](../offers/decision-management-guardrails.md#configurations) e [Medidas de proteção e limitações de decisão](../experience-decisioning/decisioning-guardrails.md#configurations) para especificar o número máximo de configurações com suporte (20.000) correspondente ao número total de regras de limite existentes na sandbox.

* Adição de uma observação na seção Atividade de condição da jornada para documentar que a avaliação da condição falhará para perfis que contenham mais de duas identidades entre dispositivos. [Leia mais](../building-journeys/condition-activity.md)

* Uma nova página foi adicionada para descrever como é possível usar as políticas de consentimento para considerar as preferências dos clientes com base em suas escolhas, respeitando o consentimento deles. [Leia mais](../action/preference-center.md)

* Uma observação foi adicionada às páginas “Introdução a perfis” e “Medidas de proteção” para especificar que, ao assimilar dados, os emails fazem distinção entre maiúsculas e minúsculas, o que significa que perfis duplicados podem ser criados e usados ao direcionar o destinatário correspondente. [Leia mais](../audience/get-started-profiles.md)

* Um novo atributo `render` foi introduzido no editor de personalização. Defina-o como `false` caso queira ocultar o conteúdo de um fragmento de expressão. [Leia mais](../personalization/use-expression-fragments.md#use-expression-fragment)

* Uma lista de medidas de proteção foi adicionada à seção que descreve como utilizar fragmentos anexados a itens de decisão nas políticas de decisão. [Leia mais](../experience-decisioning/use-decision-policy.md#fragments)

* Adição de práticas recomendadas para pesquisas de conjunto de dados: mantenha os botões ativados para evitar problemas de indexação e entenda como as exclusões em lote afetam os dados de pesquisa. [Leia mais](../data/lookup-aep-data.md#guidelines)

* Adição de uma limitação de que somente os públicos-alvo do serviço Perfil unificado são compatíveis ao usar as jornadas de público-alvo de leitura com identificadores complementares. [Leia mais](../building-journeys/supplemental-identifier.md#guardrails)

* A documentação do Experimentation Accelerator foi transferida para uma coleção separada. [Leia mais](https://experienceleague.adobe.com/pt-br/docs/experimentation-accelerator/using/overview)

## Setembro de 2025 {#september-2025}

* Uma nova seção Canal de entrada foi adicionada à página Medidas de proteção e limitações para coletar todas as limitações aplicáveis aos canais da web, no aplicativo, de experiências baseadas em código e de cartões de conteúdo. Inclui o limite máximo de volume de 5.000 solicitações de entrada por segundo para todas as solicitações de entrada e um máximo de 500 ações de entrada ativas. [Leia mais](../start/guardrails.md#inbound-guardrails)

* Uma página de Perguntas frequentes foi lançada para campanhas orquestradas. [Leia mais](../orchestrated/orchestrated-campaigns-faq.md)

* Uma seção de solução de problemas foi adicionada à documentação de eventos de Etapa da jornada com definições, causas comuns e etapas de solução de problemas para os eventTypes de descarte mais frequentes. [Leia mais](../reports/sharing-field-list.md#discarded-events)

* A documentação sobre como usar identificadores suplementares em jornadas agora inclui uma tabela que detalha como os perfis se comportam quando os critérios de saída são aplicados em jornadas usando IDs suplementares. [Leia mais](../building-journeys/supplemental-identifier.md#exit-criteria)

* Uma seção de solução de problemas foi adicionada para entender descartes de perfil em jornadas pausadas. [Leia mais](../building-journeys/journey-pause.md#discards-troubleshoot)

* Foram adicionadas informações na documentação de visão geral dos esquemas para diferenciar esquemas padrão e relacionais usados em campanhas orquestradas. [Leia mais](../data/gs-data.md)

* Foram adicionadas informações à documentação da Gestão de decisões e do serviço de Decisão sobre os requisitos para treinar com êxito os modelos de [otimização automática](../experience-decisioning/ranking/auto-optimization-model.md) e [otimização personalizada](../experience-decisioning/ranking/personalized-optimization-model.md).

* Foi esclarecido que as chamadas da API REST de execução de mensagens interativas têm um tempo-limite de 60 segundos, com novas tentativas internas para garantir a entrega. [Leia mais](../campaigns/trigger-campaigns.md)

* A página de coleções de itens de Decisão foi atualizada para esclarecer o comportamento do operador **CONTAINS** ao definir regras. [Leia mais](../experience-decisioning/collections.md)

* A página Atribuir pontuações de prioridade foi atualizada com as etapas específicas para definir uma pontuação de prioridade para ações de canal de entrada na atividade **Ação**. [Leia mais](../conflict-prioritization/priority-scores.md#priority-action)

<!--
## August 2025 {#august-2025}

* A new page listing the best practices for designing accessible email and landing page content with [!DNL Journey Optimizer] was added. [Read more](../email/accessible-content.md)

* The documentation for supplemental identifiers in journeys has been updated with the following clarifications:

    * After adding a supplemental identifier to a schema, a new event (for event-triggered journeys) or a new field group (for Read audience journeys) must be created. Existing entities do not refresh automatically and will not recognize the new identifier.

    * Supplemental identifiers are not validated against Data Usage Labeling & Enforcement (DULE) policies and are not considered during data governance checks in journeys.

        [Read more](../building-journeys/supplemental-identifier.md)

* The Optimization in campaigns page was updated to reflect the fact that optimization is now also available in journeys. [Read more](../content-management/gs-message-optimization.md)

* A link to the tutorial video describing how to leverage message optimization in a campaign was added. [Read more](../content-management/gs-message-optimization.md)

## July 2025 {#july-2025}

* The campaigns interface now features two separate tabs: **Action** and **API Triggered**. The documentation has been updated accordingly, with information for each campaign type organized into dedicated sections to improve clarity and usability. [Read more](../campaigns/get-started-with-campaigns.md)

* The [Get started with subdomain delegation](../configuration/about-subdomain-delegation.md) and [Delegate a subdomain](../configuration/delegate-subdomain.md) pages have been updated to better present the different delegation methods and the steps to set them up.

* A note has been added to the Fragments section, specifying that when tracking is enabled in a journey or a campaign, if links are present in a fragment and if this fragment is used in a message, these links are tracked such as all other links included in the message. [Learn more](../content-management/create-fragments.md#content)

* The guardrails and limitations applying to subdomain delegation in Journey Optimizer have been enriched and consolidated into one dedicated section. [Read more](../configuration/delegate-subdomain.md#guardrails)

* A note has been added to the Create fallback offers and Create decision pages to mention that fallback offers should contain all representations used within a decision. [Read more](../offers/offer-library/creating-fallback-offers.md)

* The guardrails applying to fragments have been enriched. [Read more](../start/guardrails.md#fragments-guardrails).

* A note has been added to specify that links added to messages expire after 25 months and links to mirror pages after 90 days. [Read more](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

<!--
## June 2025 {#june-2025}

* Added a new section on how to add and use rich text such as line breaks, bold, italics etc., to customizable fragments by using HTML components. [Read more](../content-management/customizable-fragments.md#rich-text)

* The Decisioning part has been updated with a specific section dedicated to building AI models. [Read more](../experience-decisioning/ranking/ai-models.md)

* Added a recommendation about the usage of the `actionExecutionTime` field in the journeyStep events action. [Read more](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Added a note about the `messageID` which may not be unique for each individual delivery. [Read more](../data/datasets-query-examples.md)

* Added a recommendation about historical events management in data hygiene operations. [Read more](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Added a guardrail about landing pages not being supported for migration between sandboxes. [Read more](../configuration/copy-objects-to-sandbox.md#global)

* Added a caution note about nested JSON objects not supported in custom authentication for custom actions. [Read more](../datasource/external-data-sources.md)

* Added a caution note about conditional content variant naming in the Email designer. [Read more](../personalization/create-conditions.md)

* Updated the "Undelegate a landing page subdomain" section. [Read more](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarified journey reentrance rules when using supplemental identifiers. [Read more](../building-journeys/supplemental-identifier.md#guardrails)

* Added a new note to clarify that you must use the expression editor in Advanced mode when selecting the supplemental identifier attribute during event configuration. [Learn more](../building-journeys/supplemental-identifier.md#add)

* Added clarification on how journey reentrance works with supplemental identifiers. [Learn more](../building-journeys/supplemental-identifier.md#guardrails)

## May 2025 {#may-2025}

* Adobe integrations available with Journey Optimizer are now listed in the "Connect your systems and environments" section. [Read more](../integrations/ajo-integrations.md)

* The content integrations are now grouped in the Content Management section. [Read more](../integrations/content-integrations.md)

* Architecture diagrams for Adobe Experience Platform and Journey Optimizer have been updated. [Read more](../start/get-started.md#architecture)

* Added a video about the personalization editor playground to help you learn how to write and test personalization code using sample data. [Read more](../personalization/personalize.md#video-perso)

* The maximum number of addresses in a seed list has been increased from 50 to 300. [Read more](../configuration/seed-lists.md#create-seed-list)

* A new step detailing how to wrap code when using decision policies in the code-based experience editor has been added to the Create decision policies page. [Read more](../experience-decisioning/create-decision.md#create-decision)

* A note has been added to the Code-based experiences documentation to specify that when you have multiple code-based experience actions running on the same surface, the campaign or journey's priority score determines what is delivered to the end-user if they qualify for more than one action. [Read more](../code-based/code-based-surface.md#surface-definition)

* A new page on troubleshooting inbound actions in journeys provides a step-by-step guide to identify and resolve issues independently before reaching out to support. [Read more](../building-journeys/troubleshooting-inbound.md)

* A new [page](../code-based/code-based-decisioning-implementations.md) has been added to describe how to add the following flags to your client implementation when using decisioning in code-based experiences:

    * Adding the `dryRun` flag to test decisioning in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

    * Apply deduplication to decisioning requests in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* The Configuration chapter is now split into three chapters: [Channel configuration](../configuration/get-started-configuration.md), [Journey configuration](../configuration/about-data-sources-events-actions.md), and [Connect your systems](../configuration/ajo-apis.md).
* Added a caution note about using experience events in journey expressions and conditions. [Read more](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Added a note on the Direct mail configuration page about temporary storage of the output file. [Read more](../direct-mail/direct-mail-configuration.md)
* Added a tip in the journey advanced expression editor section about the condition format guidelines. [Read more](../building-journeys/expression/expressionadvanced.md)
* Added a caution note in the `inAudience` function section about impacts and best practices when renaming an audience. [Read more](../building-journeys/functions/functioninaudience.md)
* Added a recommendation about the native keywords usage when using two-way SMS. [Read more](../sms/sms-opt-out.md)
* Updated the journey test page with a note about the need for including an identity namespace in the event used. [Read more](../building-journeys/testing-the-journey.md)
* Currently, you cannot undelegate subdomains through the [!UICONTROL Journey Optimizer] user interface - you must reach out to your Adobe representative. Steps to undelegate a subdomain are now detailed for [Emails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Web experiences](../web/web-delegated-subdomains.md#undelegate-subdomain), and [Landing pages](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
<!--
* Added clarification about the optional `maxHttpConnections` parameter in the journeys Capping API, including guidance on how to use it alongside throttling configurations for the same endpoint. [Read more](../configuration/throttling.md)
* In the Decisioning section, added guidance explaining that approved offer items cannot be deleted if they are used in a collection or a decision. Included steps to change their status to "Draft" using the **[!UICONTROL Undo approve]** option. [Read more](../experience-decisioning/items.md#manage)
* Information on sandboxes have been grouped together into a new "Sandboxes management" section. This new section provides information on how to use and assign sandboxes, and how to use package export and import capabilitie to copy objects such as journeys, content templates, or fragments, across multiple sandboxes. [Read more](../administration/sandboxes.md)

## March 2025 {#mar-2025}

* The page about Audience Qualification events has been updated with new recommendations. [Read more](../building-journeys/audience-qualification-events.md)
* Custom action troubleshooting capability is now available to all customers (GA). [Read more](../action/troubleshoot-custom-action.md)
* Data Hygiene is now Data Lifecycle in the product user interface. The documentation has been updated to reflect this change. [Read more](../privacy/data-hygiene.md)
* The missing Landing Page built-in permissions have been added to the documentation. [Read more](../administration/ootb-permissions.md)
* A note has been added about scheduling recurring campaigns. [Read more](../campaigns/create-campaign.md)
* The section about inserting links and enabling tracking in an email message has been updated and reorganized. [Read more](../email/message-tracking.md)
* The section about personalization capabilities into Adobe Journey Optimizer has been reorganized and improved. [Read more](../personalization/personalize.md)
* Decision management API to list personalized offers has been updated with a sample to perform pagination if multiple personalized offers are missing from the response. [Read more](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* A new page gathering all information regarding the List unsubscribe feature has been created for improved clarity. [Read more](../email/list-unsubscribe.md)
* The Frequency capping section has been updated with information on how the frequency capping counter is updated for the Decisioning and Batch Decisioning APIs, in addition to the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)

## February 2025 {#feb-2025}

* The Read Audience activity guardrails have been updated to specify that only one activity can be used in a journey and that it can target only one audience. [Read more](../building-journeys/read-audience.md)
* Journey guardrails when using Adobe Campaign activities have been updated. [Read more](../start/guardrails.md#ac-g)
* Steps to create your first journeys have been detailed, and links to documentation section have been added. [Read more](../building-journeys/journey-gs.md)
* A new page is now available to detail the journey dashboard and filtering user interface. [Read more](../building-journeys/journey-ui.md)
* Documentation for **[!UICONTROL Send-Time optimization]** and its related FAQ have been updated, improved and moved to a new dedicated page. [Read more](../building-journeys/send-time-optimization.md)
* New guardrails have been added for journey events. [Read more](../start/guardrails.md#events-g)
* The built-in channel actions page has been reorganized. [Read more](../building-journeys/journeys-message.md)
* Guardrails & limitations have been added in the Decisioning and Decision management sections.
    * [Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md)
    * [Decision management guardrails & limitations](../offers/decision-management-guardrails.md)
* A new section on context data has been added in the Decision management documentation. It provides information on how to leverage context data in the decisioning engine, for example to design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made. [Read more](../offers/context-data.md)

## January 2025 {#jan-2025}

* A new section on the **[!UICONTROL Execution address]** option in the email configuration has been added. The primary address is defined at the sandbox level, but the default setting can be overidden for a specific email configuration. [Read more](../email/email-settings.md#execution-address)

* The **Get started with deliverability** page has been updated with the possibility to create IP warmup workflows directly from the user interface. [Read more](../reports/deliverability.md#reputation)

* The **Header parameters** section has been updated to reflect the new labels and changes in the user interface. [Read more](../email/email-settings.md#email-header)

* The **Forward email** section has been updated to specify that all emails sent to the **From email** address are forwarded to the forward email address. If no forward email is specified, these emails are discarded. [Read more](../email/email-settings.md#email-settings)

* The maximum size of contextual attributes passed into an API-triggered campaign request has been updated to 200kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)

* A new section has been added to the **Manage fragments** page to describe how to add new attributes to a live fragment. The whole page has also been improved. [Read more](../content-management/manage-fragments.md#adding-new-attributes)

* A "Guardrails & limitations" section has been added to the conflict management & prioritizations tools documentation. [Read more](../conflict-prioritization/gs-conflict-prioritization.md)

* A new end-to-end use case has been added to present all the steps needed to use Decisioning in content experiments with the [!DNL Journey Optimizer] code-based experience channel. [Read more](../experience-decisioning/experience-decisioning-uc.md)

* The **Configure email settings** page has been divided into several sub-pages for improved readability, including new standalone pages dedicated to [List unsubscribe](../email/list-unsubscribe.md), [Header parameters](../email/header-parameters.md) and [URL tracking](../email/url-tracking.md).

## December 2024 {#nov-2024}

* A note has been added to help troubleshoot a potential error message when making an API call to enable datasets for personalization using Adobe Experience Platform data. [Read more](../personalization/aep-data-perso.md)

## October 2024 {#oct-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] October '24 release have been detailed in the documentation. [Read more](release-notes.md)
* All communication channels available in [!DNL Journey Optimizer] are now grouped in a dedicated section of the documentation. [Read more](../channels/gs-channels.md)
* The **Configure your code-based experience** page has been improved to make the process clearer, including the section explaining what a surface URI is. [Read more](../code-based/code-based-configuration.md)
* The **Create web channel configuration** page has been updated to clarify the steps when creating a pages matching rule, which also apply to Code-based experience configuration. [Read more](../web/web-configuration.md#web-page-matching-rule)
* A note about the upcoming time-to-live (TTL) guardrail for system-generated datasets has been added. [Read more](../data/get-started-datasets.md)
* A new section has been added to describe how to preview your code-based personalized experiences right on your browser or on your mobile devices, using the **Preview on device** option when simulating content in a journey or a campaign. [Read more](../code-based/test-code-based.md#preview-on-device)
* A new page has been added on how to leverage Custom upload audiences for decisioning. [Read more](../offers/custom-upload-decisioning.md)
* A new page has been added to introduce the decision capabilities available in Journey Optimizer. [Read more](../experience-decisioning/gs-decision.md)
* Guardrails and limitations have been added to the Decisioning documentation. [Read more](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] Sept '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a section about journey retry management. [Read more](../building-journeys/read-audience.md#read-audience-retry)
* The FAQ about Capping/throttling rule for custom actions has been updated to mention the default capping rule. [Read more](../configuration/external-systems.md#faq)
* The Control access section has been updated with permissions related to AI Assistant Content Generator. [Read more](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* A video about AI Assistant Content Generator for email generation has been added. [Read more](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `listObject` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=pt-BR){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=pt-BR)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
