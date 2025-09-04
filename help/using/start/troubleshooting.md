---
solution: Journey Optimizer
product: journey optimizer
title: Solução de problemas do Journey Optimizer
description: Perguntas de solução de problemas do Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# Solução de problemas {#ajo-troubleshooting}


Esta é uma lista de artigos de solução de problemas para o Adobe Journey Optimizer. Cada seção de solução de problemas fornece respostas a perguntas frequentes e soluções para problemas.

Consulte também a [documentação de Perguntas frequentes e Solução de Problemas do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## Canal de email {#ajo-troubleshooting-email}

### Design de email {#ajo-troubleshooting-design}

+++ Como evitar problemas de formatação de email no Adobe Journey Optimizer usando temas?

No Adobe Journey Optimizer (AJO), a modificação dos blocos CSS padrão no cabeçalho do email pode causar problemas inesperados de formatação, especialmente após a remoção de fragmentos de conteúdo. Esses problemas são mais visíveis em dispositivos móveis e podem resultar em mudanças de layout ou inconsistências de estilo. Para evitar isso, use o recurso Temas para aplicar CSS personalizado com segurança, sem alterar os estilos de CSS gerados pelo sistema.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre a formatação de email [nesta página](../email/get-started-email-design.md).

+++


+++ Por que os fragmentos com campos editáveis não estão funcionando?

No Adobe Journey Optimizer, os fragmentos com campos editáveis podem não ser carregados corretamente ou duplicados inesperadamente quando adicionados aos modelos. O problema normalmente afeta fragmentos específicos entre ambientes.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre os fragmentos personalizáveis [nesta página](../content-management/customizable-fragments.md).

+++

+++ Por que os modelos de email e o conteúdo estão desaparecendo das jornadas não publicadas?

Ao editar modelos de email em uma jornada não publicada, o conteúdo e os modelos de determinados emails podem desaparecer inesperadamente. Isso pode causar retrabalho e atrasos. Para reduzir o risco desse problema, evite edições simultâneas, limite o número de guias abertas e salve as alterações com frequência.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre os modelos [nesta página](../email/use-email-templates.md).

+++

+++ Um perfil pode ter vários tokens de push no Adobe Journey Optimizer?

Ao implementar notificações por push no Journey Optimizer, um único perfil pode realmente ter vários tokens de push associados a diferentes dispositivos. Durante uma campanha de notificação por push, o Journey Optimizer foi projetado para gerenciar esses tokens e garantir que o perfil direcionado possa ser acessado em todos os dispositivos associados.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para saber mais sobre o gerenciamento de token de push.

Saiba mais sobre a configuração de push [nesta página](../push/push-configuration.md).

+++

### Acompanhamento e relatórios de email {#ajo-troubleshooting-tracking}

+++ Como evitar a ausência de links de rastreamento de email nos relatórios?

O rastreamento de link ausente no Adobe Journey Optimizer ocorre quando URLs de email usam variáveis dinâmicas e não começam com http ou quando declarações lógicas são colocadas no campo URL. Para resolver isso, verifique se todos os URLs começam com http, evite usar lógica no campo URL e mova lógica de personalização complexa para o conteúdo do HTML ou atributos pré-processados.


Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre o rastreamento de email [nesta página](../email/message-tracking.md).

+++

### Envio de email {#ajo-troubleshooting-sending}

+++ Como resolver um erro do Mail Exchanger ao configurar campanhas de email transacionais acionadas por API? 

Se você encontrar um erro MX (Mail Exchanger) ao criar uma configuração de canal para uma campanha de email transacional acionada por API no Adobe Journey Optimizer, talvez seja devido a **configurações incorretas de DNS** ou **limitações de política da DMARC**. Para resolver isso, verifique se o DNS está configurado corretamente e se o domínio está em conformidade com os requisitos do **DMARC (Autenticação de Mensagens, Relatórios e Conformidade)**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre as políticas de email do DMARC [nesta página](../configuration/dmarc-record-update.md).

Consulte também a [documentação de campanhas acionadas por API](../campaigns/api-triggered-campaigns.md).
+++

## Canal de push {#ajo-troubleshooting-push}

+++ Um perfil pode ter vários tokens de push no Adobe Journey Optimizer?

Ao implementar notificações por push no Journey Optimizer, um único perfil pode realmente ter vários tokens de push associados a diferentes dispositivos. Durante uma campanha de notificação por push, o Journey Optimizer foi projetado para gerenciar esses tokens e garantir que o perfil direcionado possa ser acessado em todos os dispositivos associados.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para saber mais sobre o gerenciamento de token de push.

Saiba mais sobre a configuração de push [nesta página](../push/push-configuration.md).

+++

+++ Por que clicar em uma mensagem de push não me redireciona para o URL da Web configurado?  

Se as mensagens por push não estiverem redirecionando para o URL da Web pretendido, talvez seja devido à configuração incorreta da ação de clique ou às configurações desativadas de notificação por push. Verifique se a **ação de clique** para a mensagem de push está definida corretamente e se a **exibição e o rastreamento automáticos** das notificações por push estão habilitados para resolver esse problema.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} para saber mais sobre este problema.

Saiba mais sobre a configuração de push [nesta página](../push/push-configuration.md).

+++


## Canal de SMS {#ajo-troubleshooting-sms}

+++ Por que meu SMS transacional não é entregue mesmo que o consentimento esteja definido como `marketing.sms.value=y`?

Se um recipient responder **PARAR** a um SMS, todas as mensagens futuras desse número curto serão bloqueadas, incluindo mensagens transacionais. Para garantir a entrega ininterrupta de SMS transacional, configure-os e envie-os por meio de um **número curto separado** do qual os destinatários não tenham optado anteriormente.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} para saber mais sobre este problema.

Saiba mais sobre a configuração de recusa de SMS [nesta página](../sms/sms-opt-out.md).

+++


## Gerenciamento de dados {#ajo-troubleshooting-data-management}

+++ Como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados de Perfil e Data Lake ao criar uma nova sandbox?

As organizações que provisionam novas sandboxes na Adobe Journey Optimizer levantaram questões sobre como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados do Perfil e do Data Lake. Este artigo esclarece que as configurações de TTL não afetam as sandboxes existentes e são aplicadas automaticamente apenas às recém-provisionadas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para saber como lidar com TTL.

Saiba mais sobre o tempo de vida útil do conjunto de dados [nesta página](../data/datasets-ttl.md).

+++


## Gerenciamento de perfis e público-alvo {#ajo-troubleshooting-audiences}

+++ Como resolver discrepâncias na contagem de públicos-alvo?

O número de entradas processadas no recurso **Ler público-alvo** do Adobe Journey Optimizer pode ser menor do que a contagem de público-alvo esperada. Esse problema geralmente ocorre devido a configurações incorretas de namespace, levando à exclusão de perfis das jornadas. A resolução envolve verificar e corrigir configurações de namespace, revisar documentação relevante e ajustar prioridades para garantir operações mais suaves no Adobe Journey Optimizer.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para saber como resolver esse problema.

Consulte também [este artigo sobre contagens de público-alvo desatualizadas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Saiba mais sobre a atividade **Ler público** no jornada [nesta página](../building-journeys/read-audience.md).

+++

+++ Por que as atualizações de perfil estão falhando?

No Adobe Journey Optimizer, determinados valores de campo podem não ser atualizados corretamente após serem executados por uma atividade **Atualizar Perfil** em uma jornada. Em alguns casos, os campos atualizados podem desaparecer ou reverter para o estado anterior. Para resolver isso, verifique se há regras ou condições conflitantes, revise as configurações de permissões, use um conjunto de dados exclusivo para a atividade **Atualizar perfil** e verifique se nenhum outro processo de assimilação está gravando no mesmo perfil ao mesmo tempo.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre a atividade **Atualizar Perfil** no jornada [nesta página](../building-journeys/update-profiles.md).

Consulte também a [documentação do Adobe Experience Platform sobre assimilação de dados](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Por que há uma incompatibilidade na contagem de perfis ao inserir uma jornada em relação ao público-alvo associado?

A discrepância pode ocorrer quando a jornada usa um instantâneo de perfil de um dia anterior, se o instantâneo do dia atual não estiver disponível no momento da execução da jornada.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais em [esta publicação da Comunidade Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Consulte também a [documentação da API de Agendamentos do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} para verificar quando seu trabalho diário está agendado.

+++


+++ Como resolver problemas de preenchimento de público-alvo?

Problemas no preenchimento do público podem ocorrer quando componentes ou recursos estão ausentes, geralmente devido a erros de configuração de direito, provisionamento ou permissão. Para corrigir esses problemas, comece verificando os direitos, garantindo o provisionamento correto e revisando as permissões. Se o problema persistir, encaminhe o caso e fale com as equipes de suporte para obter uma resolução completa.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre a atividade **Atualizar Perfil** no jornada [nesta página](../building-journeys/update-profiles.md).

Consulte também a [documentação do Perfil do Adobe Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Como resolver problemas de acionador do jornada após alterações de público-alvo no Adobe Journey Optimizer? 

Se uma jornada parar de ser acionada após modificações no público-alvo associado, como alterações na política de mesclagem, você poderá enfrentar fluxos de campanha interrompidos. Para resolver isso, **duplique e republique a jornada** com as configurações de público atualizadas para garantir que os acionadores funcionem corretamente.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba como duplicar uma jornada [nesta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++


## Jornadas

### Eventos

+++ Por que meu evento não está acionando a jornada pretendida?  

Eventos podem deixar de disparar uma jornada, mesmo que todos os critérios sejam atendidos quando forem **criados por meio de serviços de consulta**, em vez de serem transmitidos para o **Serviço Principal de Coleta de Dados (DCCS)**. Para resolver isso, revise a configuração do evento, verifique se os eventos são **transmitidos diretamente para DCCS** e verifique a funcionalidade usando o **modo de teste**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre os eventos [nesta página](../event/about-events.md).

Consulte também [Jornada medidas de proteção de eventos](../start/guardrails.md#events).

+++

## Decisão {#ajo-troubleshooting-decisioning}

+++ Como resolver problemas ao criar coleções de ofertas?

Dificuldades para criar coleções de ofertas geralmente ocorrem quando **catálogos não foram provisionados** para sua organização. Para resolver isso, verifique se todos os catálogos necessários estão provisionados corretamente antes de tentar criar coleções de ofertas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre coleções de ofertas [nesta página](../offers/offer-library/creating-collections.md).

+++


## Multilíngue {#ajo-troubleshooting-multilingual}

+++ Como resolver este problema `Message validation error (CJMMAS - 1069-500)`?

No Adobe Journey Optimizer, um Erro de validação de mensagem (CJMAS - 1069-500) vinculado ao recurso multilíngue impede que as jornadas sejam definidas para o modo Teste ou Publicadas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre o conteúdo multilíngue [nesta página](../content-management/multilingual-gs.md).

++


## Configuração {#ajo-troubleshooting-config}

### Segurança {#ajo-troubleshooting-security}

+++ Como habilitar TLS v1.3 para Ações Personalizadas?  

Para manter a **integridade e a segurança dos dados** ao se conectar a sistemas de terceiros, verifique se o Transport Layer Security (**TLS**) v1.3 está habilitado para suas ações personalizadas. Isso ajuda a proteger as comunicações e evita possíveis vulnerabilidades de segurança.


Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} para saber mais.

Saiba mais sobre o conteúdo multilíngue [nesta página](../action/about-custom-action-configuration.md).

+++

### Painéis {#ajo-troubleshooting-dashboards}

+++ Por que não consigo criar um painel diretamente de um query no Adobe Journey Optimizer? 

No Adobe Journey Optimizer, os painéis não podem ser criados diretamente de consultas. Para criar painéis, use as **funcionalidades de criação de painel** disponíveis no Adobe Experience Platform, que permitem visualizar e analisar dados de consulta com eficiência.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} para saber mais.

++