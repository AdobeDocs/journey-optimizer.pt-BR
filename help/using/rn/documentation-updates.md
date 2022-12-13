---
solution: Journey Optimizer
product: journey optimizer
title: Atualizações de documentação
description: Saiba mais sobre as atualizações mais recentes da documentação
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 3adcd750089d81e6216316dc3d39f6a7982033f4
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# Atualizações de documentação {#latest-updates}

Esta página lista todas as atualizações de documentação do [!DNL Journey Optimizer].

## Dezembro de 2022 {#december-2022}

* O guia Mensagens foi reorganizado e dividido em guias dedicados para cada canal:

   * [Canal de email](../email/get-started-email.md)
   * [Canal de notificação por push](../push/get-started-push.md)
   * [Canal SMS](../sms/get-started-sms.md)

* O guia Configuração foi reorganizado para melhorar a legibilidade. [Leia mais](../configuration/get-started-configuration.md)

## Novembro de 2022 {#november-2022}

* Adição de uma nova página sobre integrações do Journey Otimizer. [Leia mais](../start/ajo-integrations.md)
* Adição de uma recomendação sobre o comprimento dos URLs de mirror pages. [Leia mais](../email/message-tracking.md)
* Uma nova subseção na configuração das configurações de email foi adicionada na resposta ao endereço de email, incluindo recomendações para garantir o gerenciamento de resposta adequado. [Leia mais](../email/email-settings.md#reply-to-email)
* Adição de uma seção sobre como modificar o conteúdo de uma mensagem em uma jornada ao vivo. [Leia mais](../building-journeys/journeys-message.md#update-live-content)

## Outubro de 2022 {#october-2022}

* Foi adicionado um caso de uso de jornada sobre como limitar a taxa de transferência usando Fontes de dados externas e Ações personalizadas. [Leia mais](../building-journeys/limit-throughput.md)
* A seção do caso de uso da jornada foi reorganizada em duas categorias: [Casos de uso de negócios](../building-journeys/journeys-uc.md) e [Casos de uso técnico](../building-journeys/collections.md).
* O **Conjunto de dados da entidade** foi atualizada com mais detalhes. [Leia mais](../data/datasets-query-examples.md#entity-dataset)
* As seções de gerenciamento de recusa e políticas de consentimento foram reorganizadas. [Leia mais](../privacy/opt-out.md)
* A seção sobre parâmetros avançados nas mensagens de jornada foi esclarecida e agora especifica que a substituição de endereço de email só deve ser usada para casos de uso específicos. Na maioria das vezes, o valor é definido como o endereço principal na variável **Campos de execução** é o que deve ser usado.
* Adição de uma observação ao **Configurar subdomínios de página de aterrissagem** para especificar que letras maiúsculas não são permitidas em subdomínios de página de aterrissagem. [Leia mais](../landing-pages/lp-subdomains.md)

## Setembro de 2022 {#september-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de setembro foi detalhada na documentação. [Leia mais](release-notes.md)
* Adição de uma prática recomendada relacionada ao uso de atividades de espera em jornadas de segmentos de leitura recorrentes. [Leia mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Adição de novos exemplos de consulta de evento de etapa, bem como informações sobre a diferença entre id, instanceid e profileid. [Leia mais](../reports/query-examples.md).
* Atualização das páginas relacionadas ao [toDateOnly](../building-journeys/functions/functiontodateonly.md) e [toString](../building-journeys/functions/functiontostring.md) funções.
* Adição de detalhes sobre os parâmetros da condição de tempo. [Leia mais](../building-journeys/condition-activity.md#time_condition)
* Adição de informações sobre conjuntos de dados incorporados. [Leia mais](../data/get-started-datasets.md#access-datasets)
* As seções Relatório global e Relatório ao vivo foram aprimoradas e reorganizadas. [Leia mais](../reports/global-report.md)
* Uma lista de cada métrica de relatório disponível no Adobe Journey Otimizer foi adicionada.
   [Leia mais](../reports/global-report.md#email-and-sms-metrics)
* A seção de email CCO foi movida para a nova página Suporte para arquivamento . [Leia mais](../configuration/archiving-support.md)

## Agosto de 2022 {#august-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de agosto foi detalhada na documentação. [Leia mais](release-notes.md)
* A seção Regras de frequência foi atualizada para refletir o novo fluxo de mensagens em linha. [Leia mais](../configuration/frequency-rules.md#apply-frequency-rule)
* Um vídeo que mostra como configurar assinaturas e criar landing pages agora é referenciado na seção Introdução às landing pages . [Leia mais](../landing-pages/get-started-lp.md#video)
* Uma limitação foi adicionada para jornadas que usam atividades Ler segmento . [Leia mais](../building-journeys/read-segment.md)
* A página de operadores do editor de expressão foi aprimorada. [Leia mais](../building-journeys/expression/operators.md)
* Uma seção sobre como agendar uma campanha foi adicionada. [Leia mais](../campaigns/create-campaign.md)
* A seção de regras de sintaxe gerais do editor de expressão foi atualizada para considerar a nova regra relacionada ao escape do símbolo de barra invertida em funções literais. As mensagens publicadas existentes não são afetadas por essa alteração. Somente as mensagens novas ou de rascunho devem ser atualizadas. [Leia mais](../personalization/personalization-syntax.md#general-rules)

## Julho de 2022 {#july-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de julho foi detalhada na documentação. [Leia mais](release-notes.md)
* O **Configurar superfícies do canal** A seção foi esclarecida e atualizada com links para a página que descrevem como configurar o canal SMS. [Leia mais](../configuration/channel-surfaces.md#create-channel-surface)
* Nas propriedades da jornada, a variável **Fuso horário do perfil** agora está desativada por padrão. [Leia mais](../building-journeys/timezone-management.md#timezone-from-profiles)
* No **Aguardar** , a atividade **Data fixa** não está mais disponível. [Leia mais](../building-journeys/wait-activity.md)
* Foram adicionadas mais informações sobre o **Leitura incremental** na **Ler segmento** atividade . [Leia mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Recomendações adicionadas sobre a **Tampa do perfil** tipo de condição. [Leia mais](../building-journeys/condition-activity.md#profile_cap)
* Adição de uma limitação em eventos comerciais. [Leia mais](../start/guardrails.md#events-g)

## Junho de 2022 {#june-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de junho foi detalhada na documentação. [Leia mais](release-notes.md)
* Uma nova seção sobre solicitações de privacidade foi adicionada à documentação. [Leia mais](../privacy/requests.md)
* Uma nova seção sobre Logs de auditoria em recursos foi adicionada à documentação. [Leia mais](../privacy/audit-logs.md)
* Uma nova seção sobre como adicionar conteúdo HTML ou JSON proveniente da biblioteca do Adobe Experience Cloud Asset a uma representação de oferta foi adicionada à documentação. [Leia mais](../offers/offer-library/add-representations.md#html-json)
* Adição de uma nova página sobre o ciclo de vida da jornada. [Leia mais](../building-journeys/journey.md#journey-versions)
* Atualização da página da atividade Wait . [Leia mais](../building-journeys/wait-activity.md)
* Adição da lista de conjuntos de dados do Adobe Journey Otimizer com exemplos de consulta. [Leia mais](../data/datasets-query-examples.md)
* A página Lista de permissões foi movida para a seção Configuração . [Leia mais](../configuration/allow-list.md)
* A página da lista Supressão foi atualizada para esclarecer algumas informações, incluindo o fato de que todos os caracteres ASCII incluídos entre 32 e 126 são permitidos no motivo do campo de supressão. [Leia mais](../configuration/manage-suppression-list.md)
* Foi adicionada a ligação às medidas de proteção e aos limites estáticos para a gestão de decisões. [Leia mais](../start/guardrails.md)
* A Otimização de tempo de envio agora está disponível para todos os clientes. A menção beta foi removida. [Leia mais](../building-journeys/journeys-message.md#send-time-optimization)
* A API de decisão em lote foi adicionada à lista de APIs disponíveis para fornecer ofertas personalizadas. [Leia mais](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Maio de 2022 {#may-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de maio foi detalhada na documentação. [Leia mais](release-notes.md)
* Novos exemplos de query relacionados a [qualificação de segmento](../reports/query-examples.md#segment-qualification-queries) e [events](../reports/query-examples.md#event-based-queries) foram adicionados.
* A seção de design de email agora menciona novos modelos integrados disponíveis para iniciar o conteúdo. As capturas de tela relacionadas foram atualizadas. [Leia mais](../email/get-started-email-design.md)
* Os links para recursos principais foram atualizados na página inicial da documentação do Journey Otimizer.
* As capturas de tela para relatórios de landing page e subscrição foram atualizadas. [Leia mais](../reports/live-report.md)
* Uma observação foi adicionada informando que o método Excluir não é compatível com ações personalizadas. [Leia mais](../action/about-custom-action-configuration.md)
* Os links para vídeos de instruções foram atualizados.
* O [Configuração de email](../configuration/about-subdomain-delegation.md), [Predefinições de mensagem](../configuration/channel-surfaces.md) e [Configurar landing pages](../landing-pages/lp-subdomains.md) foram reorganizadas para melhorar a legibilidade.
* A seção Rastreamento de URL foi atualizada e aprimorada com exemplos. [Leia mais](../email/email-settings.md#url-tracking)
* Uma nova subseção sobre como configurar um endereço de email de encaminhamento foi adicionada. Observe que não é possível fazer isso por meio da interface do usuário. [Leia mais](../email/email-settings.md#forward-email)

## Abril de 2022 {#april-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de abril foi detalhada na documentação. [Leia mais](release-notes.md)
* O **reações** a página de documentação do evento foi atualizada. [Leia mais](../building-journeys/reaction-events.md)
* Os vídeos dos recursos de Gerenciamento de decisões foram atualizados para refletir a interface do usuário do Journey Otimizer. [Leia mais](../offers/get-started/starting-offer-decisioning.md)
* O **Introdução aos conjuntos de dados** A seção foi aprimorada para detalhar como acessar e criar conjuntos de dados. [Leia mais](../data/get-started-datasets.md)
* Links para guias de ajuda e notas de versão do produto foram adicionados ao **Documentação do Adobe Journey Otimizer** página inicial. [Leia mais](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* O **Criar predefinições de mensagem** A seção agora especifica que você não pode continuar com a criação predefinida enquanto o pool de IP selecionado estiver na edição (**[!UICONTROL Processing]** e nunca foi associado ao subdomínio selecionado. [Leia mais](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* As predefinições de mensagem **Rastreamento de URL** foi atualizada para refletir pequenas alterações na interface do usuário. [Leia mais](../configuration/channel-surfaces.md#url-tracking)

## Março de 2022 {#march-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de março foi detalhada na documentação. [Leia mais](release-notes.md)
* Uma nova página sobre a introdução aos modelos de IA foi adicionada ao **Offer Decisioning** , incluindo uma descrição completa da [modelo de otimização automática](../offers/ranking/auto-optimization-model.md), o algoritmo usado e mais detalhes técnicos. [Leia mais](../offers/ranking/ai-models.md)
* A página de criação do perfil de teste foi movida para  **Segmento, perfis e identidade** seção. [Leia mais](../segment/creating-test-profiles.md)
* Adição de um exemplo sobre como adicionar uma expressão como valor padrão no editor de expressão. [Leia mais](../building-journeys/expression/field-references.md#default-value)
* O **Criar ofertas personalizadas** foi reorganizada para melhorar a legibilidade. [Leia mais](../offers/offer-library/creating-personalized-offers.md)
* Uma nova seção foi adicionada para descrever os impactos que a alteração das datas de início e/ou término de uma oferta pode ter no limite de frequência dessa oferta. [Leia mais](../offers/offer-library/add-constraints.md#capping-change-date)
* O **Alterar os endereços de email principais** foi atualizada para refletir as alterações na interface do usuário. [Leia mais](../configuration/primary-email-addresses.md)

## Fevereiro de 2022 {#feb-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de fevereiro foi detalhada na documentação. [Leia mais](release-notes.md)
* O [replace](../building-journeys/functions/functionreplace.md#example_2) e [replaceAll](../building-journeys/functions/functionreplaceall.md#example) as páginas de documentação da função foram atualizadas com informações adicionais e exemplos relacionados ao parâmetro target .
* As práticas recomendadas foram adicionadas ao [Operadores](../building-journeys/expression/operators.md#important-notes) página.

## Janeiro de 2022 {#january-2022}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 22 de janeiro foi detalhada na documentação. [Leia mais](release-notes.md)
* O **Classificações da AI de decisão de oferta** A seção foi atualizada com uma descrição mais detalhada do modelo de otimização automática. [Leia mais](../offers/ranking/auto-optimization-model.md)
* Uma nova seção sobre os requisitos do schema necessários para enviar os tipos de evento ao usar uma estratégia de classificação foi adicionada. [Leia mais](../offers/ranking/schema-requirement.md)
* A seção relacionada ao [!DNL Journey Optimizer] os recursos de personalização foram reorganizados para melhorar a legibilidade. [Leia mais](../personalization/personalize.md)
* O **Criar predefinições de mensagem** A seção foi dividida em várias seções para maior clareza. [Leia mais](../configuration/channel-surfaces.md#create-channel-surface)
* O **Gerenciamento de não participação** foi esclarecida e ligeiramente reorganizada. [Leia mais](../privacy/opt-out.md#opt-out-management)
* O **Inserir links** foi atualizada para refletir as alterações recentes na interface do usuário. [Leia mais](../email/message-tracking.md#insert-links)

## Novembro de 2021 {#november-2021}

* Uma descrição completa da **editor de expressão avançado** usado em jornadas agora está disponível. [Leia mais](../building-journeys/expression/expressionadvanced.md)
* Uma nova seção sobre **Método de delegação de subdomínio CNAME** foi adicionada. [Leia mais](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## Outubro de 2021 {#october-2021}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 21 de outubro foi detalhada na documentação. [Leia mais](release-notes.md)
* Adicionado **Função de hora da data** lista. [Leia mais](../personalization/functions/dates.md)
* Novo **seções Introdução por persona de usuário**. Siga seu próprio caminho para atingir seus objetivos mais rapidamente! [Leia mais](../start/quick-start.md)
* Novo **Editar uma predefinição de mensagem** seção. [Leia mais](../configuration/channel-surfaces.md#edit-channel-surface)
* Novo **Editar um registro PTR** seção. [Leia mais](../configuration/ptr-records.md#edit-ptr-record)
* Novo **Desativar uma predefinição de mensagem** seção. [Leia mais](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Novas limitações adicionadas à **Guia do desenvolvedor da API de gerenciamento de decisões** em restrições de oferta não suportadas com o dispositivo móvel [!DNL Experience Edge] fluxos de trabalho. [Leia mais](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Novo **Criar simulações** seção. [Leia mais](../offers/offer-activities/simulation.md)
* Atualizado **Adicionar escopos de decisão** seção. [Leia mais](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Atualizado **Definir conteúdo para suas representações** , incluindo uma nova [subseção](../offers/offer-library/creating-personalized-offers.md#custom-text) sobre como definir e personalizar texto personalizado. [Leia mais](../offers/offer-library/creating-personalized-offers.md#content)

## Setembro de 2021 {#september-2021}

* As seguintes páginas de função foram atualizadas: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* As seguintes funções foram adicionadas: [filter](../building-journeys/functions/functionfilter.md), [interseção](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* O tipo de data dateOnly foi adicionado na documentação do editor de expressão. [Leia mais](../building-journeys/expression/data-types.md)

* Adição de detalhes sobre a duração do cache de ação personalizada. [Leia mais](../datasource/external-data-sources.md#custom-authentication-mode)

* Foram adicionadas informações sobre as portas padrão de ação personalizada. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)

* Foram adicionadas informações sobre vários casos de uso de eventos comerciais. [Leia mais](../event/about-creating-business.md#multiple-business-events)

* Adição de exemplos comumente usados para consultar Eventos de etapa da jornada no Data Lake. [Leia mais](../reports/query-examples.md)

* Adicionou um novo **Limitações** página. [Leia mais](../start/guardrails.md)

* Melhoria no **Início rápido** página com etapas para diferentes personas. [Leia mais](../start/quick-start.md)

* Agora, todos os recursos de Gerenciamento de decisões descritos na seção dedicada também se aplicam aos usuários da Adobe Experience Platform que usam o serviço de aplicativo Offer Decisioning. [Leia mais](../offers/get-started/starting-offer-decisioning.md)

* Adição de uma subseção para esclarecer as diferenças entre o uso de segmentos versus regras de decisão ao aplicar uma restrição para restringir a seleção de ofertas para uma determinada disposição. [Leia mais](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Foram adicionados exemplos de fórmulas de classificação específicas para ilustrar alguns casos de uso reais. [Leia mais](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Adição de uma subseção sobre como editar pools de IP. [Leia mais](../configuration/ip-pools.md#edit-ip-pool)


## Agosto de 2021 {#august-2021}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 21 de agosto foi detalhada na documentação. [Leia mais](release-notes.md)
* Permissões de gerenciamento de decisões atualizadas. [Leia mais](../administration/ootb-product-profiles.md)
* Capturas de tela do Designer de email atualizadas com a interface do usuário mais recente.
* Atualização do procedimento de configuração para ações personalizadas com caminhos dinâmicos de URL e cabeçalhos dinâmicos. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)
* Adição de uma seção sobre recursos e atalhos de acessibilidade. [Leia mais](../start/user-interface.md#accessibility)
* Adição de uma seção sobre métodos de avaliação de segmento. [Leia mais](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* Adição de observações à lista Supressão, Lista de permissões e seções Relatório global/ao vivo de email para especificar que os perfis com status Suprimido e Não permitido são excluídos do relatório de email Métricas enviadas. [Leia mais](../reports/global-report.md)
* Adição de uma nova seção para descrever como recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. [Leia mais](../configuration/allow-list.md#reporting)
* Atualização da seção Ativar a lista de permissões . [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* Atualização da seção Monitorar predefinições da mensagem com os possíveis motivos de falha de criação predefinida e detalhes sobre esses erros. [Leia mais](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Atualização e renomeação da seção Repetir período de tempo para refletir o fato de que agora é possível ajustar a configuração de nova tentativa de email nas predefinições de mensagem. [Leia mais](../configuration/retries.md#retry-duration)
* Uma nova seção foi adicionada para descrever como inserir um link de opção de não participação com um clique no conteúdo do email. [Leia mais](../privacy/opt-out.md#one-click-opt-out-link)
* A seção Delegar um subdomínio foi atualizada com informações mais detalhadas sobre o processo de validação executado pela Adobe. [Leia mais](../configuration/delegate-subdomain.md#subdomain-validation)
* Adição de uma seção para descrever como adicionar manualmente endereços de email e domínios à lista de supressão. [Leia mais](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Atualização do [Acessar a lista de supressão](../configuration/manage-suppression-list.md#access-suppression-list) seção e [Tentativas](../configuration/retries.md) para refletir a nova interface do usuário.
* O novo fluxo para adicionar e configurar representações ao criar uma oferta foi documentado. [Leia mais](../offers/offer-library/creating-personalized-offers.md#representations)


## Julho de 2021 {#july-2021}

* Todos os novos recursos e aprimoramentos estão surgindo com [!DNL Journey Optimizer] A versão de 21 de julho foi detalhada na documentação. [Leia mais](release-notes.md)
* Links diretos adicionados à documentação dos serviços da Experience Platform em [!DNL Journey Optimizer] página inicial e índice
* Novas páginas de aterrissagem para os serviços da Experience Platform disponíveis em [!DNL Journey Optimizer]
* Links adicionados a [!DNL Journey Optimizer] descrição do produto na página inicial
* Vídeos tutoriais adicionados em várias páginas
* Imagem otimizada da página inicial
* Seção &quot;Rastreamento de mensagens&quot; movida, aprimorada e renomeada para &quot;Adicionar links e rastrear mensagens&quot;. [Leia mais](../email/message-tracking.md)
* Adição de uma subseção em mirror pages. [Leia mais](../email/message-tracking.md#mirror-page)
* As &quot;atividades de oferta&quot; foram renomeadas como &quot;decisões&quot; e &quot;decisões&quot; como &quot;escopos de decisão&quot; na documentação e nas telas. [Leia mais](../offers/get-started/starting-offer-decisioning.md)
* Novo caso de uso: [personalizar uma mensagem com funções auxiliares](../personalization/personalization-use-case-helper-functions.md)
* Atualização da documentação do segmento Lido para refletir os impactos de segmentos materializados. [Leia mais](../building-journeys/read-segment.md)
* Atualização das limitações de Jornada. [Leia mais](../start/guardrails.md)
* Atualização da seleção Configurar ofertas na seção decisões . [Leia mais](../offers/offer-activities/configure-offer-selection.md)
* Adição de um aviso para mencionar que as ofertas baseadas em eventos não são suportadas no momento. [Leia mais](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documentação da nova gestão de decisões **[!UICONTROL Overview]** guia . [Leia mais](../offers/get-started/user-interface.md#overview)
* Adição de novas seções para descrever as ações disponíveis nas listas de oferta e decisão: [Lista de ofertas](../offers/offer-library/creating-personalized-offers.md#offer-list) e [Lista de decisões](../offers/offer-activities/create-offer-activities.md#decision-list).

