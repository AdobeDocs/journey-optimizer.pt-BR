---
solution: Journey Optimizer
product: journey optimizer
title: Solução de problemas do Journey Optimizer
description: Perguntas de solução de problemas do Journey Optimizer
feature: Get Started
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 45ebae048a748429a1918326526f3756a3e93c4c
workflow-type: tm+mt
source-wordcount: '2674'
ht-degree: 2%

---

# Resolução de problemas {#ajo-troubleshooting}

Esta é uma lista de artigos de solução de problemas para o Adobe Journey Optimizer. Cada seção de solução de problemas fornece respostas a perguntas frequentes e soluções para problemas.

Consulte também a [documentação de Perguntas frequentes e Solução de Problemas do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/troubleshooting){target="_blank"}.

## Canal de email {#ajo-troubleshooting-email}

+++ Como evitar problemas de formatação de email no Adobe Journey Optimizer usando temas?

No Adobe Journey Optimizer (AJO), a modificação dos blocos CSS padrão no cabeçalho do email pode causar problemas inesperados de formatação, especialmente após a remoção de fragmentos de conteúdo. Esses problemas são mais visíveis em dispositivos móveis e podem resultar em mudanças de layout ou inconsistências de estilo. Para evitar isso, use o recurso Temas para aplicar CSS personalizado com segurança, sem alterar os estilos de CSS gerados pelo sistema.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre a formatação de email [nesta página](../email/get-started-email-design.md).

+++


+++ Por que os fragmentos com campos editáveis não estão funcionando?

No Adobe Journey Optimizer, os fragmentos com campos editáveis podem não ser carregados corretamente ou duplicados inesperadamente quando adicionados aos modelos. O problema normalmente afeta fragmentos específicos entre ambientes.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre os fragmentos personalizáveis [nesta página](../content-management/customizable-fragments.md).

+++

+++ Por que os fragmentos do HTML não são exibidos corretamente nos emails?

Os fragmentos do HTML podem não ser renderizados corretamente em emails, frequentemente aparecendo como **IDs de fragmento** em vez do conteúdo real. Diferentemente dos fragmentos visuais, os fragmentos do HTML exigem uma configuração cuidadosa. Para resolver isso, siga as práticas recomendadas para usar **fragmentos de expressão visuais e do HTML** em suas campanhas de email.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre os fragmentos do HTML [nesta página](../content-management/fragments.md).

+++

+++ Por que os modelos de email e o conteúdo estão desaparecendo das jornadas não publicadas?

Ao editar modelos de email em uma jornada não publicada, o conteúdo e os modelos de determinados emails podem desaparecer inesperadamente. Isso pode causar retrabalho e atrasos. Para reduzir o risco desse problema, evite edições simultâneas, limite o número de guias abertas e salve as alterações com frequência.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre os modelos [nesta página](../email/use-email-templates.md).

+++

+++ Por que o campo Pré-cabeçalho de email não é exibido no modo &quot;Código seu próprio&quot;? 

No modo **&#39;Codifique você mesmo&#39;** sob o recurso **Editar Corpo do Email**, o campo de entrada do Pré-cabeçalho não é exibido. Para incluir texto de pré-cabeçalho, os usuários devem **codificar manualmente o pré-cabeçalho** no conteúdo personalizado de HTML.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre a configuração do pré-cabeçalho de email [nesta página](../email/header-parameters.md).

+++

+++ Por que há uma discrepância no comportamento do link ao usar um componente do HTML em modelos de email?  

Ao adicionar um **componente do HTML** a um modelo de email, os links podem ter um comportamento diferente, dependendo do **cliente de email**, do **modo de exibição** ou do **dispositivo/navegador**. Por exemplo, links de âncora podem funcionar de forma diferente na **exibição lado a lado do Outlook** em comparação à exibição em tela inteira. Esteja ciente dessas variações ao projetar modelos de email e testar em vários clientes e dispositivos.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"} para saber como resolver esse problema.

Consulte também Práticas recomendadas de design de email [nesta página](../email/get-started-email-design.md).

+++


+++ Como evitar a ausência de links de rastreamento de email nos relatórios?

O rastreamento de link ausente no Adobe Journey Optimizer ocorre quando URLs de email usam variáveis dinâmicas e não começam com http ou quando declarações lógicas são colocadas no campo URL. Para resolver isso, verifique se todos os URLs começam com http, evite usar lógica no campo URL e mova lógica de personalização complexa para o conteúdo do HTML ou atributos pré-processados.


Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} para saber como resolver esse problema.

Saiba mais sobre o rastreamento de email [nesta página](../email/message-tracking.md).

+++

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

## Canal no aplicativo

+++ Por que não posso criar relatórios no canal no aplicativo no Customer Journey Analytics?

As dificuldades para criar relatórios no **canal no aplicativo** no Adobe Customer Journey Analytics geralmente surgem de **visualizações de dados**, **conjuntos de dados** ou **atualizações de esquema** configuradas incorretamente. Verifique se essas configurações estão aplicadas corretamente para resolver o problema.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"} para saber mais sobre este problema.

Saiba mais sobre como integrar dados de análise do Journey Optimizer no Customer Journey Analytics [nesta página](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}.

Consulte também a [documentação dos Relatórios de tempo integral do Journey Optimizer](../reports/report-gs-cja.md)

+++


## Gerenciamento de dados {#ajo-troubleshooting-data-management}

+++ Como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados de Perfil e Data Lake ao criar uma nova sandbox?

As organizações que provisionam novas sandboxes na Adobe Journey Optimizer levantaram questões sobre como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados do Perfil e do Data Lake. Este artigo esclarece que as configurações de TTL não afetam as sandboxes existentes e são aplicadas automaticamente apenas às recém-provisionadas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para saber como lidar com TTL.

Saiba mais sobre o tempo de vida útil do conjunto de dados [nesta página](../data/datasets-ttl.md).

+++


## Gerenciamento de perfis e público-alvo {#ajo-troubleshooting-audiences}

+++ Como resolver discrepâncias na contagem de públicos-alvo?

O número de entradas processadas no recurso **Ler público-alvo** do Adobe Journey Optimizer pode ser menor do que a contagem de público-alvo esperada. Esse problema geralmente ocorre devido a configurações incorretas de namespace, levando à exclusão de perfis das jornadas. A resolução envolve verificar e corrigir configurações de namespace, revisar documentação relevante e ajustar prioridades para garantir operações mais suaves no Adobe Journey Optimizer.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para saber como resolver esse problema.

Consulte também [este artigo sobre contagens de público-alvo desatualizadas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Saiba mais sobre a atividade **Ler público** no jornada [nesta página](../building-journeys/read-audience.md).

+++

+++ Por que as atualizações de perfil estão falhando?

No Adobe Journey Optimizer, determinados valores de campo podem não ser atualizados corretamente após serem executados por uma atividade **Atualizar Perfil** em uma jornada. Em alguns casos, os campos atualizados podem desaparecer ou reverter para o estado anterior. Para resolver isso, verifique se há regras ou condições conflitantes, revise as configurações de permissões, use um conjunto de dados exclusivo para a atividade **Atualizar perfil** e verifique se nenhum outro processo de assimilação está gravando no mesmo perfil ao mesmo tempo.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre a atividade **Atualizar Perfil** no jornada [nesta página](../building-journeys/update-profiles.md).

Consulte também a [documentação do Adobe Experience Platform sobre assimilação de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Por que há uma incompatibilidade na contagem de perfis ao inserir uma jornada em relação ao público-alvo associado?

A discrepância pode ocorrer quando a jornada usa um instantâneo de perfil de um dia anterior, se o instantâneo do dia atual não estiver disponível no momento da execução da jornada.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais em [esta publicação da Comunidade Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998?profile.language=pt){target="_blank"}.

Consulte também a [documentação da API de Agendamentos do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} para verificar quando seu trabalho diário está agendado.

+++


+++ Como resolver problemas de preenchimento de público-alvo?

Problemas no preenchimento do público podem ocorrer quando componentes ou recursos estão ausentes, geralmente devido a erros de configuração de direito, provisionamento ou permissão. Para corrigir esses problemas, comece verificando os direitos, garantindo o provisionamento correto e revisando as permissões. Se o problema persistir, encaminhe o caso e fale com as equipes de suporte para obter uma resolução completa.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre a atividade **Atualizar Perfil** no jornada [nesta página](../building-journeys/update-profiles.md).

Consulte também a [documentação do Perfil do Adobe Real-Time CDP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Por que a contagem de perfis ativáveis aumentou significativamente em um curto período? 

A métrica **Perfis ativáveis** reflete o número de perfis exclusivos ativados por jornadas ou campanhas nos últimos 12 meses. Um aumento súbito pode resultar do direcionamento de públicos-alvo grandes ou de alterações nos conjuntos de dados. Para gerenciar isso, revise a **lógica de contagem de perfis**, investigue jornadas direcionadas a públicos-alvo grandes, **filtre públicos-alvo** no nível de jornada, reduza o **tamanho de público-alvo endereçável** e monitore **as alterações no conjunto de dados**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Monitore o uso de licenças da sua organização e perfis ativáveis usando o [Painel de Uso de Licenças](../audience/license-usage.md)

Consulte também a [visão geral do Adobe Experience Platform Query Service](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/home?lang=en){target="_blank"}.

+++

+++ Por que os emails são enviados para indivíduos fora do público-alvo com base nas funções de data?

Emails podem ser enviados a destinatários que **não atendem aos critérios de público-alvo especificados**. Por exemplo, os membros com datas de resgate **anteriores a 4 de julho de 2025** podem receber emails destinados somente àqueles após essa data. Este comportamento pode resultar de **segmentação de público configurada incorretamente** ou **alterações inesperadas na lógica de qualificação de perfil**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre funções de data [nesta página](../../rp_landing_pages/date-landing-page.md).

+++

+++ Como resolver problemas de seleção de público-alvo e erros do Chrome ao salvar jornadas?

A adição de públicos-alvo às condições de jornada pode, às vezes, causar **travamentos do aplicativo** ou exibir um **Erro do Aw Snap** no Chrome, incluindo erros ao salvar jornadas. Estes problemas estão frequentemente relacionados com os **serviços Chromium**. Para resolvê-los, aplique uma **atualização do navegador** ou use uma **solução alternativa** apropriada.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

+++

## Jornadas {#ajo-troubleshooting-journeys}

Para obter Jornadas, consulte as seguintes seções de solução de problemas:

* [Solucionar erros antes de testar a jornada](../building-journeys/troubleshooting.md)
* [Solucionar problemas de ações de entrada em jornadas](../building-journeys/troubleshooting-inbound.md)
* [Solucionar problemas de execução do Live jornada](../building-journeys/troubleshooting-execution.md)
* [Solução de problemas de ações personalizadas](../action/troubleshoot-custom-action.md)



+++ Por que as expressões são perdidas ao criar uma nova versão do jornada?  

Ao criar uma nova versão de uma jornada, **expressões em etapas específicas** podem ser perdidas, causando erros e exigindo reentrada manual. Para resolver isso, **duplique a jornada**, teste a reprodutibilidade, **evite recarregamentos de navegador** e use a **tela atualizada** para jornadas mais antigas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba como duplicar uma jornada [nesta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Por que os perfis saem do jornada prematuramente? 

Os perfis podem sair de uma jornada inesperadamente sem passar por um nó designado quando a **condição que verifica o status de feedback** das mensagens enviadas está configurada incorretamente. Para resolver isso, revise a **lógica de condição**, implemente a **lógica alternativa** ou consulte sua **equipe de implementação**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Consulte também [diretrizes de design do Jornada](../building-journeys/using-the-journey-designer.md).

+++


+++ Por que os perfis estão saindo das jornadas inesperadamente?

Perfis podem sair de uma jornada inesperadamente quando **event capping** ocorrer, fazendo com que alguns perfis sejam descartados se o número de eventos processados exceder a capacidade do sistema. Para reduzir saídas de perfil, compreenda os **limites de sistema**, monitore **picos de evento** e otimize o **fluxo de dados** para evitar limites excedidos.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Consulte também [medidas de proteção da Jornada](../start/guardrails.md#journey-guardrails).

+++


+++ Por que meu evento não está acionando a jornada pretendida?  

Eventos podem deixar de disparar uma jornada, mesmo que todos os critérios sejam atendidos quando forem **criados por meio de serviços de consulta**, em vez de serem transmitidos para o **Serviço Principal de Coleta de Dados (DCCS)**. Para resolver isso, revise a configuração do evento, verifique se os eventos são **transmitidos diretamente para DCCS** e verifique a funcionalidade usando o **modo de teste**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre os eventos [nesta página](../event/about-events.md).

Consulte também [Jornada medidas de proteção de eventos](../start/guardrails.md#events).

+++


+++ Como resolver problemas de acionador do jornada após alterações de público-alvo no Adobe Journey Optimizer? 

Se uma jornada parar de ser acionada depois de modificações no público-alvo associado, como alterações na política de mesclagem, você poderá enfrentar fluxos interrompidos. Para resolver isso, **duplique e republique a jornada** com as configurações de público atualizadas para garantir que os acionadores funcionem corretamente.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba como duplicar uma jornada [nesta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Por que uma ação personalizada que chama um ponto de extremidade de terceiros externo atinge o tempo limite?

Podem ocorrer erros de tempo limite quando uma **ação personalizada** chama um ponto de extremidade de terceiros externo. Para resolver isso, verifique se o **ponto de extremidade está acessível**, verifique os **logs do servidor**, verifique se há **nenhum bloqueio do Adobe**, atualize as configurações do ponto de extremidade conforme necessário e **teste após as atualizações**. Além disso, lembre-se de **especificações de tempo limite de chamada de API**.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre a API de Limitação do Jornada [nesta página](../configuration/throttling.md).

Consulte também a [documentação sobre integração com sistemas externos](../configuration/external-systems.md).

+++

## Regras {#ajo-troubleshooting-rules}

+++ Por que a lista suspensa Regras de limite não está funcionando?

Problemas com a **Lista suspensa de regras de limite** ocorrem frequentemente quando os conjuntos de regras estão **configurados incorretamente** ou **inacessíveis**. Verifique se todos os conjuntos de regras estão configurados corretamente e disponíveis para resolver o problema.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"} para saber mais.

Saiba como aplicar as regras de limitação [nesta seção](../conflict-prioritization/rule-sets.md).

+++

## Tomada de decisão {#ajo-troubleshooting-decisioning}

+++ Como resolver problemas ao criar coleções de ofertas?

Dificuldades para criar coleções de ofertas geralmente ocorrem quando **catálogos não foram provisionados** para sua organização. Para resolver isso, verifique se todos os catálogos necessários estão provisionados corretamente antes de tentar criar coleções de ofertas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre coleções de ofertas [nesta página](../offers/offer-library/creating-collections.md).

+++

+++ Por que não consigo acessar o Offer Decisioning?  

Ao integrar o Adobe Target em um aplicativo usando o Adobe Journey Optimizer, a opção **Offer Decisioning** pode estar inacessível na configuração de sequência de dados. Isso geralmente ocorre devido a **configurações de permissão** ou **restrições de provisionamento**. Para resolver o problema, verifique as permissões do usuário e se o provisionamento necessário está em vigor.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre as permissões necessárias para o Offer Decisioning [nesta página](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Multilíngue {#ajo-troubleshooting-multilingual}

+++ Como resolver este problema `Message validation error (CJMMAS - 1069-500)`?

No Adobe Journey Optimizer, um Erro de validação de mensagem (CJMAS - 1069-500) vinculado ao recurso multilíngue impede que as jornadas sejam definidas para o modo Teste ou Publicadas.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} para saber mais sobre as etapas para resolver esse problema.

Saiba mais sobre o conteúdo multilíngue [nesta página](../content-management/multilingual-gs.md).

+++


## Configuração {#ajo-troubleshooting-config}

+++ Como habilitar TLS v1.3 para Ações Personalizadas?  

Para manter a **integridade e a segurança dos dados** ao se conectar a sistemas de terceiros, verifique se o Transport Layer Security (**TLS**) v1.3 está habilitado para suas ações personalizadas. Isso ajuda a proteger as comunicações e evita possíveis vulnerabilidades de segurança.


Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} para saber mais.

Saiba mais sobre o conteúdo multilíngue [nesta página](../action/about-custom-action-configuration.md).

+++

+++ Por que não consigo criar um painel diretamente de um query no Adobe Journey Optimizer? 

No Adobe Journey Optimizer, os painéis não podem ser criados diretamente de consultas. Para criar painéis, use as **funcionalidades de criação de painel** disponíveis no Adobe Experience Platform, que permitem visualizar e analisar dados de consulta com eficiência.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} para saber mais.

+++

## APIs {#ajo-troubleshooting-apis}

+++ Como resolver problemas de acesso com a API do Serviço de consulta?  

Erros de acesso ao usar a **API de Serviço de Consulta** via Postman ou ferramentas semelhantes geralmente são causados por **permissões insuficientes**. Para resolver isso, verifique as permissões do usuário, as credenciais da API e forneça informações detalhadas de suporte, se necessário.

Consulte [este artigo de solução de problemas](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"} para saber mais.

Consulte também a [documentação sobre credenciais de API gerenciadas](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}.

+++
