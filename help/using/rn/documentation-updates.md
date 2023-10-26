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
source-git-commit: b2a9a118b663c757a026c62b18e00d1f53e26317
workflow-type: tm+mt
source-wordcount: '4011'
ht-degree: 93%

---

# Atualizações de documentação {#latest-updates}

Esta página lista todas as atualizações na documentação do [!DNL Journey Optimizer].

## Outubro de 2023 {#oct-2023}

* Todos os novos recursos e aprimoramentos que acompanham o [!DNL Journey Optimizer] A versão de outubro de 2023 foi detalhada na documentação. [Leia mais](release-notes.md)
* Adição de GIF para ilustrar alguns recursos principais, como: [Modelos de conteúdo](../content-management/content-templates.md), [Fragmentos](../content-management/fragments.md), [Atributos computados](../audience/computed-attributes.md), [Correspondência direta](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Modelos de otimização de gestão de decisão](../offers/ranking/personalized-optimization-model.md), [Campanhas acionadas por API](../campaigns/api-triggered-campaigns.md), e [Experimento de conteúdo](../campaigns/content-experiment.md).
* O processo de criação do Schema foi atualizado para refletir as atualizações mais recentes na interface, que vêm com alterações do Adobe Experience Platform. [Leia mais](../audience/creating-test-profiles.md)
* As medidas de proteção do Gerenciamento de decisão foram adicionadas à página Medidas de proteção e limitações. [Leia mais](../start/guardrails.md#decision-management)
* A seção Parâmetros de cabeçalho foi atualizada para refletir como as notificações de ausência do escritório e as respostas de desafio são tratadas (elas são recebidas no **[!UICONTROL Email de erro]**). [Leia mais](../email/email-settings.md#email-header)
* Uma nova seção sobre como pré-visualizar e testar seu conteúdo foi criada. [Leia mais](../content-management/preview-test.md)
* A página Implementar aplicativos de página única foi movida para a documentação do SDK da Web da Adobe Experience Platform. [Leia mais](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* A seção Limite foi atualizada para refletir as alterações de rótulo relacionadas ao limite de oferta na interface da gestão de decisões. [Leia mais](../offers/offer-library/add-constraints.md#capping)
* A seção Adicionar conteúdo dinâmico a emails foi atualizada com detalhes sobre como excluir uma variante. [Leia mais](../personalization/dynamic-content.md#emails)
* O exemplo de para configurações de limitação e limitação foi atualizado. [Leia mais](../configuration/external-systems.md)
* A limitação relacionada aos arrays escalares foi removida da seção fonte de dados externa. [Leia mais](../datasource/external-data-sources.md)
* O caso de uso da jornada de vários canais foi atualizado. [Leia mais](../building-journeys/journeys-uc.md)
* O conjunto de documentação do Journey Optimizer foi atualizado para refletir o novo processo de criação do esquema Experience Platform.

## Setembro de 2023 {#september-2023}

* Todos os novos recursos e aprimoramentos da versão de setembro de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foi adicionada uma nova página com práticas recomendadas de dimensionamento e orientação de compilação em tempo real. [Leia mais](../start/best-practices.md)

  <!--  * The maximum wait duration has been changed from 30 to 29 days. [Read more](../building-journeys/wait-management.md) -->

* Foi adicionada uma seção de Perguntas frequentes para a Otimização do tempo de envio. [Leia mais](../building-journeys/journeys-message.md#faq-send-time)
* Foi adicionada uma nota para a atividade de qualificação de público-alvo. Pode levar até 10 minutos para ficar ativa e ouvir os perfis que entram ou saem do público-alvo. [Leia mais](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* Uma lista de limitações que devem ser observadas ao criar regras de decisão foi adicionada à documentação da Gestão de decisões. [Leia mais](../offers/offer-library/creating-decision-rules.md)
* Os links para a documentação do controle de acesso foram atualizados. [Leia mais](../administration/permissions.md)
* Os pré-requisitos do canal no aplicativo foram atualizados com os detalhes da Coleção de dados da Adobe Experience Platform. [Leia mais](../in-app/inapp-configuration.md)
* Algumas expressões apresentadas em exemplos de fórmulas de classificação foram atualizadas para evitar erros de validação. [Leia mais](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* Um aviso foi adicionado à seção Definir escopos de decisão para especificar que, se o modelo de IA for usado em um grupo de critérios de avaliação, todos os critérios de avaliação desse grupo deverão usar o método de classificação de IA, com o mesmo modelo de IA específico. Além disso, apenas um grupo de critérios de avaliação pode utilizar o modelo de IA. [Leia mais](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## Agosto de 2023 {#august-2023}

* Todos os novos recursos e melhorias chegando com a versão de agosto de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* A observação sobre o **gerenciamento de cache de autenticação** na jornada foi atualizada para mencionar que o token não é compartilhado entre jornadas diferentes. [Leia mais](../datasource/external-data-sources.md#custom-authentication-mode)
* A página sobre o **gerenciamento de entradas** da jornada foi atualizada para esclarecer comportamentos. [Leia mais](../building-journeys/entry-management.md)
* A **exportação de conjuntos de dados** do Offer Decisioning agora está habilitada por padrão. A observação sobre o comportamento anterior foi removida.  [Leia mais](../offers/export-catalog/get-started-export.md)
* Várias **métricas de relatórios de campanha**, nos relatórios dinâmicos e globais, foram renomeadas. [Leia mais](../reports/campaign-global-report.md)
* Uma nova seção foi adicionada sobre os pré-requisitos do experimento de conteúdo para o canal da Web. [Leia mais](../web/web-prerequisites.md#experiment-prerequisites)
* Um aviso foi adicionado à página **Trabalhar com modelos de conteúdo** para indicar que o rastreamento atual não é compatível ao testar modelos de conteúdo de email. Para testar o rastreamento, você deve usar o modelo de conteúdo em um email e enviar uma prova. [Leia mais](../content-management/content-templates.md#test-template)
* Vários avisos foram adicionados à seção **Criar e publicar páginas de destino** para especificar que você não pode acessar sua página de destino simplesmente copiando e colando em um navegador da web o URL definido ao criar a página, mesmo que esteja publicada. Em vez disso, você pode testá-lo usando a função de visualização. [Leia mais](../landing-pages/create-lp.md)
* Uma nova seção foi adicionada informando como **gerenciar o consentimento** no canal de correspondência direta. [Leia mais](../direct-mail/test-send-direct-mail.md)

## Julho de 2023 {#july-2023}

* Todos os novos recursos e aprimoramentos da versão de 23 de julho do [!DNL Journey Optimizer] estão detalhados na documentação. [Leia mais](release-notes.md)
* A página de documentação da atividade de espera foi aprimorada com informações adicionais e práticas recomendadas relacionadas ao tempo limite global e ao uso de reentrada. [Leia mais](../building-journeys/wait-activity.md)
* A página sobre o gerenciamento de entradas foi aprimorada. [Leia mais](../building-journeys/entry-management.md)
* Adição de mais informações sobre a taxa de limitação na documentação de atividade do público-alvo de leitura. [Leia mais](../building-journeys/read-audience.md)
* Foram adicionadas informações adicionais sobre novas tentativas. [Leia mais](../start/guardrails.md#general-actions-g)
* A seção **Implementar consentimento de personalização** foi atualizada para descrever como aplicar manualmente o consentimento de personalização em campanhas: é possível usar o construtor de regras de segmento para criar um público-alvo contendo os perfis que recusaram ou adicionar uma atividade de divisão a um fluxo de trabalho de composição. [Leia mais](../privacy/opt-out.md#opt-out-expression-editor)

## Junho de 2023 {#june-2023}

* Todos os novos recursos e aprimoramentos da versão de junho de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foram adicionadas informações sobre a taxa de descarte na tela de visão geral das jornadas. [Leia mais](../building-journeys/journey-gs.md#journey-access)
* Foi adicionada uma nota com as etapas a serem seguidas caso modifique o esquema com novos valores de enumeração após criar um evento [Leia mais](../event/about-creating.md)
* Foi adicionada uma recomendação para usar journeyVersionID em vez de journeyVersionName ao consultar jornadas. [Leia mais](../reports/sharing-common-fields.md#journeyversionid-field)
* Exemplos adicionais na ordem de critérios de avaliação foram adicionados à seção **Criar decisões** para ilustrar os casos em que vários critérios e escopos de decisão são usados. [Leia mais](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A documentação da Gestão de decisões foi esclarecida com uma nota especificando que o uso do Controle de acesso em nível de objeto não está disponível para coleções dinâmicas. [Leia mais](../offers/offer-library/creating-collections.md)

## Maio de 2023 {#may-2023}

* Todos os novos recursos e aprimoramentos da versão de maio de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Uma nova página foi adicionada para descrever como configurar o subdomínio que será usado para publicar o conteúdo proveniente do Adobe Experience Manager Assets Essentials em suas experiências da Web. [Leia mais](../web/web-delegated-subdomains.md)
* Uma nova subseção foi adicionada para explicar como adicionar parâmetros de rastreamento personalizados a URLs no designer de email. [Leia mais](../email/message-tracking.md#url-tracking)
* Uma nova seção foi adicionada para descrever como garantir que a escolha de seus clientes que optam por não terem seus dados de perfil usados para personalização seja respeitada. [Leia mais](../privacy/opt-out.md#opt-out-personalization)
* Foi adicionada uma nota sobre o uso de caracteres internacionais especiais em URLs incluídos em conteúdos de email. [Leia mais](../email/message-tracking.md#insert-links)
* A permissão necessária para testar e publicar páginas de destino foi adicionada. [Leia mais](../landing-pages/create-lp.md)
* Foi adicionada uma nota sobre os ponto de acesso da Adobe Experience Platform necessários para contabilizar seus eventos personalizados no limite de frequência da Gestão de decisões. [Leia mais](../offers/data-collection/schema-requirement.md#track-custom-events)

## Abril de 2023 {#apr-2023}

* Todos os novos recursos e aprimoramentos da versão de abril de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foi adicionada uma nota para especificar que as ações incorporadas não podem ser removidas. [Leia mais](../start/guardrails.md#custom-actions-g)
* Foram adicionadas informações sobre serviceEvents, bem como um exemplo de consulta para verificar os detalhes de um serviceEvent. [Leia mais](../reports/query-examples.md#common-queries)
* Foi adicionada uma nota para especificar que não é possível executar consultas em séries cronológicas. [Leia mais](../building-journeys/condition-activity.md)
* O Adobe Experience Manager Assets Essentials e o Adobe Stock foram adicionados à página de integração de várias soluções. [Leia mais](../start/ajo-integrations.md)
* O aviso sobre subdomínios de email de vários níveis não serem permitidos foi removido, pois eles agora são compatíveis. [Leia mais](../configuration/delegate-subdomain.md)
* Uma observação foi adicionada para especificar que, se forem feitas alterações em uma decisão de oferta que esteja sendo usada em uma mensagem da jornada, será necessário desfazer a publicação da jornada e republicá-la. [Leia mais](../building-journeys/publishing-the-journey.md)
* A explicação sobre como se certificar de que os eventos foram corretamente contabilizados no contador de limites foi esclarecida na seção **Evento de limitação** da gestão de decisões. [Leia mais](../offers/offer-library/add-constraints.md#capping-event)
* Uma nova seção foi adicionada à página **Alterar endereços de execução**. Ela especifica que é possível sobrepor o campo de execução definido globalmente nos parâmetros avançados da jornada, mas que a sobreposição de endereços de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, o valor é definido como o endereço principal nos **Campos de execução** é o que deve ser usado. [Leia mais](../configuration/primary-email-addresses.md#journey-parameters)
* A seção **Rastreamento de URL** agora fornece a lista e a descrição de todos os atributos contextuais que podem ser definidos para rastreamento de URL em uma superfície de canal de email. [Leia mais](../email/email-settings.md#url-tracking)

## Março de 2023 {#march-2023}

* O dicionário de esquemas do Journey Optimizer está disponível agora. Você encontrará a lista completa de campos e atributos para cada esquema.  [Leia mais](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)
* Todos os novos recursos e aprimoramentos da versão de março de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Adição de uma etapa para ativar os eventos do Adobe Analytics em suas jornadas. [Leia mais](../event/about-analytics.md)
* Uma nova seção foi criada no guia da gestão de decisões sobre como coletar feedback das definições de ofertas na Adobe Experience Platform, incluindo quais ofertas são exibidas e como os usuários interagem com elas. [Leia mais](../offers/data-collection/data-collection.md)
* Uma nova subseção foi adicionada à seção **Criar decisão** para explicar a diferença entre avaliar critérios em uma ordem sequencial ou simultaneamente. [Leia mais](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Uma medida de proteção foi adicionada para jornadas de público-alvo de leitura com leitura incremental. Não é possível criar uma nova versão. É necessário duplicar a jornada. [Leia mais](../start/guardrails.md#journey-versions-g)
* O caso de uso sobre como limitar a taxa de transferência foi atualizado com informações sobre recursos de limitação. [Leia mais](../building-journeys/limit-throughput.md)
* Foi adicionada uma nota para especificar que matrizes escalares não são compatíveis com a definição de conteúdo de resposta. [Leia mais](../datasource/external-data-sources.md)
* A seção sobre condições de limite de perfis foi atualizada. [Leia mais](../building-journeys/condition-activity.md#profile_cap)

## Fevereiro de 2023 {#feb-2023}

* Todos os novos recursos e aprimoramentos da versão de fevereiro de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foram adicionadas informações sobre a barra de ferramentas da tela. [Leia mais](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Foram adicionadas informações para indicar que endereços internos da Adobe não são permitidos em URLs e APIs. [Leia mais](../start/guardrails.md)
* Uma observação foi adicionada na documentação de campanhas acionadas pela API para especificar que os atributos contextuais passados na solicitação não podem exceder 50 KB. [Leia mais](../campaigns/api-triggered-campaigns.md#contextual)
* Adição de detalhes sobre como as informações de recusa são armazenadas no **conjunto de dados do serviço de consentimento** depois que os destinatários cancelam sua inscrição por meio de uma página de destino. [Leia mais](../landing-pages/lp-use-cases.md#configure-opt-out)

## Janeiro de 2023 {#jan-2023}

* Todos os novos recursos e aprimoramentos da versão de janeiro de 2023 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foram adicionadas informações sobre pontos de acesso de autenticação personalizados na documentação de limite. [Leia mais](../configuration/external-systems.md)
* Um novo exemplo de autenticação personalizada foi adicionado na seção fontes de dados externas. [Leia mais](../datasource/external-data-sources.md#custom-authentication-mode)
* Foi adicionada uma nota sobre o Serviço Principal de Coleção de Dados (DCCS) para jornadas acionadas por eventos. [Leia mais](../start/guardrails.md#events-g)
* Foi adicionada uma nota sobre a recuperação do namespace de identidade nas seções [Público-alvo de leitura](../building-journeys/read-audience.md), [Qualificação de público-alvo](../building-journeys/audience-qualification-events.md) e [Criação de evento](../event/about-creating.md).
* Os recursos de acessibilidade no [!DNL Journey Optimizer] agora estão agrupados em uma página dedicada. [Leia mais](../start/accessibility.md)
* Os exemplos foram atualizados na seção Operadores da documentação do editor de expressão avançado. [Leia mais](../building-journeys/expression/operators.md)
* Foi adicionada uma nota sobre a limitação na pesquisa com a matriz de objetos. [Leia mais](../event/experience-event-schema.md#relationships_limitations)
* Adição de uma nova página sobre o gerenciamento de dados no [!DNL Journey Optimizer]. [Leia mais](../data/gs-data.md)
* Adição de uma tabela listando todos os códigos que podem ser retornados na resposta ao entregar ofertas usando a API de decisão. [Leia mais](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++ 2022

## Dezembro de 2022 {#december-2022}

* O guia de mensagens foi reorganizado e dividido em manuais dedicados para cada canal:

   * [Canal de email](../email/get-started-email.md)
   * [Canal de notificação por push](../push/get-started-push.md)
   * [Canal de SMS](../sms/get-started-sms.md)

* O guia Configuração foi reorganizado para melhorar a legibilidade. [Leia mais](../configuration/get-started-configuration.md)

## Novembro de 2022 {#november-2022}

* Uma nova página sobre as integrações do Journey Optimizer foi adicionada. [Leia mais](../start/ajo-integrations.md)
* Uma recomendação sobre o comprimento dos URLs de mirror pages foi adicionada. [Leia mais](../email/message-tracking.md)
* Uma nova subseção nas configurações de email foi adicionada na resposta ao endereço de email, incluindo recomendações para garantir o gerenciamento de resposta adequado. [Leia mais](../email/email-settings.md#reply-to-email)
* Adição de uma seção sobre como modificar o conteúdo de uma mensagem em uma jornada em tempo real. [Leia mais](../building-journeys/journeys-message.md#update-live-content)

## Outubro de 2022 {#october-2022}

* Foi adicionado um caso de uso de jornada sobre como limitar a taxa de transferência usando Fontes de dados externas e Ações personalizadas. [Leia mais](../building-journeys/limit-throughput.md)
* A seção caso de uso de jornada foi reorganizada em duas categorias: [Casos de uso de negócios](../building-journeys/journeys-uc.md) e [Casos de uso técnico](../building-journeys/collections.md).
* A seção **Conjunto de dados da entidade** foi atualizada com mais detalhes. [Leia mais](../data/datasets-query-examples.md#entity-dataset)
* As seções de gerenciamento de recusa e políticas de consentimento foram reorganizadas. [Leia mais](../privacy/opt-out.md)
* A seção sobre parâmetros avançados nas mensagens da jornada foi esclarecida e agora especifica que a substituição de endereço de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, o valor definido como o endereço principal nos **Campos de execução** é o que deve ser usado.
* Uma observação foi adicionada à seção **Configurar subdomínios da página de destino** para especificar que letras maiúsculas não são permitidas nos subdomínios da página de destino. [Leia mais](../landing-pages/lp-subdomains.md)

## Setembro de 2022 {#september-2022}

* Todos os novos recursos e aprimoramentos da versão de setembro de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Adição de uma prática recomendada relacionada ao uso de atividades de espera em jornadas de público-alvo de leitura recorrentes. [Leia mais](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Adição de novos exemplos de consulta de evento de etapa, bem como informações sobre a diferença entre id, instanceid e profileid. [Leia mais](../reports/query-examples.md).
* Atualização das páginas relacionadas às funções [toDateOnly](../building-journeys/functions/functiontodateonly.md) e [toString](../building-journeys/functions/functiontostring.md).
* Adição de detalhes sobre os parâmetros da condição de tempo. [Leia mais](../building-journeys/condition-activity.md#time_condition)
* Adição de informações sobre conjuntos de dados incorporados. [Leia mais](../data/get-started-datasets.md#access-datasets)
* As seções Relatório global e Relatório ao vivo foram aprimoradas e reorganizadas. [Leia mais](../reports/global-report.md)
* Uma lista de cada métrica de relatório disponível no Adobe Journey Optimizer foi adicionada.
  [Leia mais](../reports/global-report.md#email-and-sms-metrics)
* A seção sobre CCO de email foi movida para a nova página Suporte para arquivamento. [Leia mais](../configuration/archiving-support.md)

## Agosto de 2022 {#august-2022}

* Todos os novos recursos e aprimoramentos chegando com a versão de agosto de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* A seção Regras de frequência foi atualizada para refletir o novo fluxo de mensagens integrado. [Leia mais](../configuration/frequency-rules.md#apply-frequency-rule)
* Um vídeo que mostra como configurar assinaturas e criar páginas de destino agora é referenciado na seção Introdução às páginas de destino. [Leia mais](../landing-pages/get-started-lp.md#video)
* Uma limitação foi adicionada para jornadas que usam atividades de público-alvo de leitura. [Leia mais](../building-journeys/read-audience.md)
* A página de operadores do editor de expressão foi aprimorada. [Leia mais](../building-journeys/expression/operators.md)
* Uma seção sobre como programar uma campanha foi adicionada. [Leia mais](../campaigns/create-campaign.md)
* A seção de regras de sintaxe gerais do editor de expressão foi atualizada para considerar a nova regra relacionada ao escape do símbolo de barra invertida em funções literais. As mensagens publicadas existentes não são afetadas por essa alteração. Somente as mensagens novas ou de rascunho devem ser atualizadas. [Leia mais](../personalization/personalization-syntax.md#general-rules)

## Julho de 2022 {#july-2022}

* Todos os novos recursos e aprimoramentos chegando com a versão de [!DNL Journey Optimizer] 22 de julho estão detalhados na documentação. [Leia mais](release-notes.md)
* A seção **Criar superfícies de canal** foi esclarecida e atualizada com links para a página que descreve como configurar o canal de SMS. [Leia mais](../configuration/channel-surfaces.md#create-channel-surface)
* Nas propriedades da jornada, a opção **Fuso horário do perfil** agora está desativada por padrão. [Leia mais](../building-journeys/timezone-management.md#timezone-from-profiles)
* Na atividade **Aguardar**, a opção **Data fixa** não está mais disponível. [Leia mais](../building-journeys/wait-activity.md)
* Foram adicionadas mais informações sobre a opção **Leitura incremental** na atividade de **público-alvo de leitura**. [Leia mais](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Recomendações adicionadas sobre o tipo de condição **Limite de perfil**. [Leia mais](../building-journeys/condition-activity.md#profile_cap)
* Adição de uma limitação em eventos comerciais. [Leia mais](../start/guardrails.md#events-g)

## Junho de 2022 {#june-2022}

* Todos os novos recursos e aprimoramentos da versão de junho de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Uma nova seção sobre solicitações de privacidade foi adicionada à documentação. [Leia mais](../privacy/requests.md)
* Uma nova seção sobre logs de auditoria em recursos foi adicionada à documentação. [Leia mais](../privacy/audit-logs.md)
* Uma nova seção sobre como adicionar conteúdo HTML ou JSON provenientes da biblioteca de ativos da Adobe Experience Cloud a uma representação de oferta foi adicionada à documentação. [Leia mais](../offers/offer-library/add-representations.md#html-json)
* Nova página adicionada ao ciclo de vida da jornada. [Leia mais](../building-journeys/journey.md#journey-versions)
* Atualização da página da atividade de espera. [Leia mais](../building-journeys/wait-activity.md)
* Adição da lista de conjuntos de dados do Adobe Journey Optimizer com exemplos de consulta. [Leia mais](../data/datasets-query-examples.md)
* A página Lista de permissões foi movida para a seção Configuração. [Leia mais](../configuration/allow-list.md)
* A página Lista de supressão foi atualizada para esclarecer algumas informações, incluindo o fato de que todos os caracteres ASCII entre 32 e 126 são permitidos no campo de motivo da supressão. [Leia mais](../configuration/manage-suppression-list.md)
* Foi adicionado o link para as medidas de proteção e limites estáticos para a gestão de decisões. [Leia mais](../start/guardrails.md)
* A Otimização de tempo de envio agora está disponível para todos os clientes. A menção ao beta foi removida. [Leia mais](../building-journeys/journeys-message.md#send-time-optimization)
* A API de decisão em lote foi adicionada à lista de APIs disponíveis para ofertas personalizadas de entrega. [Leia mais](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Maio de 2022 {#may-2022}

* Todos os novos recursos e aprimoramentos da versão de maio de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* Foram adicionados novos exemplos de consulta relacionados a [qualificação de público-alvo](../reports/query-examples.md#segment-qualification-queries) e [eventos](../reports/query-examples.md#event-based-queries).
* A seção de design de email agora menciona novos modelos integrados disponíveis para iniciar o conteúdo. As capturas de tela relacionadas foram atualizadas. [Leia mais](../email/get-started-email-design.md)
* Os links para recursos principais foram atualizados na página inicial da documentação do Journey Optimizer.
* As capturas de tela para relatórios de página de destino e subscrição foram atualizadas. [Leia mais](../reports/live-report.md)
* Uma observação foi adicionada informando que o método DELETE não é compatível com ações personalizadas. [Leia mais](../action/about-custom-action-configuration.md)
* Os links para vídeos de instrução foram atualizados.
* As seções [Configuração de email](../configuration/about-subdomain-delegation.md), [Predefinições de mensagem](../configuration/channel-surfaces.md) e [Configurar páginas de destino](../landing-pages/lp-subdomains.md) foram reorganizadas para facilitar a leitura.
* A seção Rastreamento de URL foi atualizada e aprimorada com exemplos. [Leia mais](../email/email-settings.md#url-tracking)
* Uma nova subseção sobre como configurar um endereço de email de encaminhamento foi adicionada. Observe que não é possível fazer isso por meio da interface. [Leia mais](../email/email-settings.md#forward-email)

## Abril de 2022 {#april-2022}

* Todos os novos recursos e aprimoramentos da versão de abril de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* A página de documentação do evento **reações** foi atualizada. [Leia mais](../building-journeys/reaction-events.md)
* Os vídeos dos recursos da Gestão de decisões foram atualizados para refletir a interface do Journey Optimizer. [Leia mais](../offers/get-started/starting-offer-decisioning.md)
* A seção **Introdução aos conjuntos de dados** foi aprimorada para detalhar como acessar e criar conjuntos de dados. [Leia mais](../data/get-started-datasets.md)
* Links para guias de ajuda e notas de versão do produto foram adicionados à página inicial da **Documentação do Adobe Journey Optimizer**. [Leia mais](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=pt-BR)
* A seção **Criar predefinições de mensagem** agora especifica que você não pode continuar com a criação da predefinição enquanto o pool de IP selecionado estiver em edição (status **[!UICONTROL Processando]**) e não tiver sido associado ao subdomínio selecionado. [Leia mais](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* A seção **Rastreamento de URL** das predefinições de mensagem foi atualizada para refletir pequenas alterações na interface. [Leia mais](../configuration/channel-surfaces.md#url-tracking)

## Março de 2022 {#march-2022}

* Todos os novos recursos e aprimoramentos da versão de março de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Saiba mais](release-notes.md)
* Uma nova página de introdução aos modelos de IA foi adicionada à seção **Offer Decisioning**, incluindo uma descrição completa do [modelo de otimização automática](../offers/ranking/auto-optimization-model.md), o algoritmo que ele utiliza, entre outros detalhes técnicos. [Saiba mais](../offers/ranking/ai-models.md)
* A página de criação do perfil de teste foi movida para a seção **Público-alvo, perfis e identidade**. [Saiba mais](../audience/creating-test-profiles.md)
* Adição de um exemplo sobre como adicionar uma expressão como valor padrão no editor de expressão. [Saiba mais](../building-journeys/expression/field-references.md#default-value)
* A seção **Criar ofertas personalizadas** foi reorganizada para melhorar a leitura. [Saiba mais](../offers/offer-library/creating-personalized-offers.md)
* Uma nova seção foi adicionada para descrever os impactos que a alteração das datas de início e/ou término de uma oferta pode ter no limite de frequência dessa oferta. [Saiba mais](../offers/offer-library/add-constraints.md#capping-change-date)
* A seção **Alterar os endereços de email principais** foi atualizada para refletir as alterações na interface. [Saiba mais](../configuration/primary-email-addresses.md)

## Fevereiro de 2022 {#feb-2022}

* Todos os novos recursos e aprimoramentos da versão de fevereiro de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* As páginas de documentação das funções [replace](../building-journeys/functions/functionreplace.md#example_2) e [replaceAll](../building-journeys/functions/functionreplaceall.md#example) foram atualizadas com informações adicionais e exemplos relacionados ao parâmetro de público-alvo.
* As práticas recomendadas foram adicionadas à página [Operadores](../building-journeys/expression/operators.md#important-notes).

## Janeiro de 2022 {#january-2022}

* Todos os novos recursos e aprimoramentos da versão de janeiro de 2022 do [!DNL Journey Optimizer] foram detalhados na documentação. [Leia mais](release-notes.md)
* A seção **Classificações de IA do Offer Decisioning** foi atualizada com uma descrição mais detalhada do modelo de otimização automática. [Leia mais](../offers/ranking/auto-optimization-model.md)
* Foi adicionada uma nova seção sobre os requisitos de esquema necessários para poder enviar tipos de eventos ao usar um modelo de IA. [Leia mais](../offers/data-collection/schema-requirement.md)
* A seção relacionada aos recursos de personalização do [!DNL Journey Optimizer] foi reorganizada para melhorar a compreensão. [Leia mais](../personalization/personalize.md)
* A seção **Criar predefinições de mensagem** foi dividida em várias seções para maior clareza. [Leia mais](../configuration/channel-surfaces.md#create-channel-surface)
* A seção **Gerenciamento de opção de não participação** foi esclarecida e levemente reorganizada. [Leia mais](../privacy/opt-out.md#opt-out-management)
* A seção **Inserir links** foi atualizada para refletir as alterações recentes na interface do usuário. [Leia mais](../email/message-tracking.md#insert-links)

+++

+++ 2021

## Novembro de 2021 {#november-2021}

* Uma descrição completa do **editor de expressão avançado** usado em jornadas está disponível. [Leia mais](../building-journeys/expression/expressionadvanced.md)
* Foi adicionada uma nova seção sobre o **método de delegação de subdomínio CNAME**. [Leia mais](../configuration/delegate-subdomain.md#cname-subdomain-delegation)

## Outubro de 2021 {#october-2021}

* Todos os novos recursos e aprimoramentos chegando junto com [!DNL Journey Optimizer] a versão de outubro de 2021 foram detalhados na documentação. [Leia mais](release-notes.md)
* Lista **Função de data e hora** adicionada. [Leia mais](../personalization/functions/dates.md)
* Novas seções de **Introdução por personalidade de usuário**. Siga seu próprio caminho para atingir seus objetivos com mais rapidez! [Leia mais](../start/quick-start.md)
* Nova seção **Editar uma predefinição de mensagem**. [Leia mais](../configuration/channel-surfaces.md#edit-channel-surface)
* Nova seção **Editar um registro PTR**. [Leia mais](../configuration/ptr-records.md#edit-ptr-record)
* Nova seção **Desativar uma predefinição de mensagem**. [Leia mais](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Adicionadas novas limitações à **Guia do desenvolvedor da API de Gestão de decisões** sobre restrições de oferta não compatíveis com os fluxos de trabalho [!DNL Experience Edge] de dispositivo móvel. [Leia mais](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nova seção **Criar simulações**. [Leia mais](../offers/offer-activities/simulation.md)
* Seção **Adicionar escopos de decisão** atualizada. [Leia mais](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Seção **Definir conteúdo para suas representações** atualizada, incluindo uma nova [subseção](../offers/offer-library/creating-personalized-offers.md#custom-text) sobre como definir e personalizar texto. [Leia mais](../offers/offer-library/creating-personalized-offers.md#content)

## Setembro de 2021 {#september-2021}

* As seguintes páginas de função foram atualizadas: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* As seguintes funções foram adicionadas: [filtro](../building-journeys/functions/functionfilter.md), [interseção](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* O tipo de data dateOnly foi adicionado na documentação do editor de expressão. [Leia mais](../building-journeys/expression/data-types.md)

* Foram adicionados detalhes sobre a duração do cache de ação personalizada. [Leia mais](../datasource/external-data-sources.md#custom-authentication-mode)

* Foram adicionadas informações sobre as portas padrão de ação personalizada. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)

* Foram adicionadas informações sobre vários casos de uso de eventos comerciais. [Leia mais](../event/about-creating-business.md#multiple-business-events)

* Foram adicionados exemplos usados com frequência para consultar eventos de etapa da jornada no Data Lake. [Leia mais](../reports/query-examples.md)

* Nova página sobre **Limitações** adicionada. [Leia mais](../start/guardrails.md)

* Página de **Início rápido** aprimorada com etapas para diferentes personalidades. [Leia mais](../start/quick-start.md)

* Agora, todos os recursos da Gestão de decisões descritos na seção dedicada também se aplicam aos usuários da Adobe Experience Platform que usam o serviço de aplicativos do Offer Decisioning. [Leia mais](../offers/get-started/starting-offer-decisioning.md)

* Subseção adicionada para elucidar as diferenças entre o uso de públicos-alvo e o uso de regras de decisão ao aplicar uma restrição contra a seleção de ofertas para um determinado posicionamento. [Leia mais](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Exemplos específicos de fórmulas de classificação adicionados para ilustrar alguns casos de uso reais. [Leia mais](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Subseção sobre como editar pools de IP adicionada. [Leia mais](../configuration/ip-pools.md#edit-ip-pool)

## Agosto de 2021 {#august-2021}

* Todos os novos recursos e aprimoramentos chegando com [!DNL Journey Optimizer] a versão de agosto de 2021 foram detalhados na documentação. [Leia mais](release-notes.md)
* Permissões da Gestão de decisões atualizadas. [Leia mais](../administration/ootb-product-profiles.md)
* Capturas de tela do Designer de email atualizadas com a interface mais recente.
* Atualização do procedimento de configuração para ações personalizadas com caminhos dinâmicos de URL e cabeçalhos dinâmicos. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)
* Seção sobre recursos e atalhos de acessibilidade adicionada. [Leia mais](../start/user-interface.md#accessibility)
* Adição de uma seção sobre métodos de avaliação de público-alvo. [Leia mais](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Observações adicionadas às seções Lista de supressão, Lista de permissões e Relatório de email global/em tempo real para especificar que os perfis com status Suprimido e Não permitido estão excluídos das métricas do relatório de emails enviados. [Leia mais](../reports/global-report.md)
* Nova seção adicionada para descrever como recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. [Leia mais](../configuration/allow-list.md#reporting)
* Seção Ativar a lista de permissões atualizada. [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* Seção Monitorar predefinições de mensagem atualizada com os possíveis motivos de falha na criação de predefinições e detalhes sobre esses erros. [Leia mais](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Seção Repetir período de tempo atualizada e renomeada para refletir o fato de que agora é possível ajustar as configurações de nova tentativa de email nas predefinições de mensagem. [Leia mais](../configuration/retries.md#retry-duration)
* Nova seção adicionada para descrever como inserir no conteúdo do email um link de opção de não participação com um clique. [Leia mais](../privacy/opt-out.md#one-click-opt-out-link)
* Seção Delegar um subdomínio atualizada com informações mais detalhadas sobre o processo de validação executado pela Adobe. [Leia mais](../configuration/delegate-subdomain.md#subdomain-validation)
* Seção adicionada para descrever como adicionar manualmente endereços de email e domínios à lista de supressão. [Leia mais](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Seções [Acessar a lista de supressão](../configuration/manage-suppression-list.md#access-suppression-list) e [Tentativas](../configuration/retries.md) atualizadas para refletir a nova interface de usuário.
* O novo fluxo para adicionar e configurar representações ao criar uma oferta foi documentado. [Leia mais](../offers/offer-library/creating-personalized-offers.md#representations)

## Julho de 2021 {#july-2021}

* Todos os novos recursos e aprimoramentos chegando com a versão de [!DNL Journey Optimizer] 21 de julho estão detalhados na documentação. [Leia mais](release-notes.md)
* Links diretos para a documentação dos serviços da Experience Platform adicionados na [!DNL Journey Optimizer] página inicial e índice
* Novas páginas de destino para serviços da Experience Platform disponíveis em [!DNL Journey Optimizer]
* Links adicionados à [!DNL Journey Optimizer] descrição do produto na página inicial
* Vídeos tutoriais adicionados em várias páginas
* Imagens da página inicial otimizadas
* Seção &quot;Rastreamento de mensagens&quot; deslocada, aprimorada e renomeada para &quot;Adicionar links e rastrear mensagens&quot;. [Leia mais](../email/message-tracking.md)
* Subseção sobre mirror pages adicionada. [Leia mais](../email/message-tracking.md#mirror-page)
* As &quot;atividades de oferta&quot; foram renomeadas como &quot;decisões&quot;, e as &quot;decisões&quot; como &quot;escopos de decisão&quot; na documentação e nas telas. [Leia mais](../offers/get-started/starting-offer-decisioning.md)
* Novo caso de uso: [personalizar uma mensagem com funções auxiliares](../personalization/personalization-use-case-helper-functions.md)
* Atualização da documentação relativa a público-alvo de leitura para refletir os impactos materializados sobre segmentos. [Leia mais](../building-journeys/read-audience.md)
* Limitações da jornada atualizadas. [Leia mais](../start/guardrails.md)
* Seleção Configurar ofertas atualizada na seção de decisões. [Leia mais](../offers/offer-activities/configure-offer-selection.md)
* Adicionado um aviso para mencionar que as ofertas baseadas em eventos não são compatíveis no momento. [Leia mais](../offers/offer-library/creating-personalized-offers.md#eligibility)
* A nova guia **[!UICONTROL Visão geral]** da gestão de decisões foi documentada. [Leia mais](../offers/get-started/user-interface.md#overview)
* Novas seções adicionadas para descrever as ações disponíveis nas listas de oferta e decisão: [Lista de ofertas](../offers/offer-library/creating-personalized-offers.md#offer-list) e [Lista de decisões](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
