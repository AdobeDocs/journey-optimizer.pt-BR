---
solution: Journey Optimizer
product: journey optimizer
title: Artigos de solução de problemas do Journey Optimizer
description: Artigos de solução de problemas do Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
TQID: https://experienceleague.adobe.com/-E1vLZQv8dDZqejyh944at7jHheePuzXybU4lCyMris
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d2e8a157-b3b0-4143-9ff3-809bf400be56id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 4714
ht-degree: 0%

---

# Perguntas frequentes sobre solução de problemas {#ajo-troubleshooting}

Esta é uma lista de artigos de solução de problemas para o Adobe Journey Optimizer. Cada seção de solução de problemas fornece respostas a perguntas frequentes e soluções para problemas.

Ao entrar em contato com o suporte da Adobe para resolver problemas, inclua detalhes do ambiente, nível de impacto, etapas de replicação, registros ou capturas de tela e IDs relevantes. [Saiba o que incluir nos tíquetes de suporte](user-interface.md#support-ticket-guidelines).

## Canal de email {#ajo-troubleshooting-email}

+++ Como evitar problemas de formatação de email no Adobe Journey Optimizer usando temas?

No Adobe Journey Optimizer (AJO), a modificação dos blocos CSS padrão no cabeçalho do email pode causar problemas inesperados de formatação, especialmente após a remoção de fragmentos de conteúdo. Esses problemas são mais visíveis em dispositivos móveis e podem resultar em mudanças de layout ou inconsistências de estilo. Para evitar isso, use o recurso Temas para aplicar CSS personalizado com segurança, sem alterar os estilos de CSS gerados pelo sistema.

Saiba mais sobre a formatação de email [nesta página](../email/get-started-email-design.md).

+++


+++ Por que os fragmentos com campos editáveis não estão funcionando?

No Adobe Journey Optimizer, os fragmentos com campos editáveis podem não ser carregados corretamente ou duplicados inesperadamente quando adicionados aos modelos. O problema normalmente afeta fragmentos específicos entre ambientes. Para resolver isso, verifique a configuração do fragmento, verifique se há definições de campo editáveis conflitantes e teste em uma sandbox de desenvolvimento antes de republicar.

Saiba mais sobre os fragmentos personalizáveis [nesta página](../content-management/customizable-fragments.md).

+++

+++ Por que os fragmentos do HTML não são exibidos corretamente nos emails?

Os fragmentos do HTML podem não ser renderizados corretamente em emails, frequentemente aparecendo como **IDs de fragmento** em vez do conteúdo real. Diferentemente dos fragmentos visuais, os fragmentos do HTML exigem uma configuração cuidadosa. Para resolver isso, siga as práticas recomendadas para usar **fragmentos de expressão visuais e do HTML** em suas campanhas de email.

Saiba mais sobre os fragmentos do HTML [nesta página](../content-management/fragments.md).

+++

+++ Por que os modelos de email e o conteúdo estão desaparecendo das jornadas não publicadas?

Ao editar modelos de email em uma jornada não publicada, o conteúdo e os modelos de determinados emails podem desaparecer inesperadamente. Isso pode causar retrabalho e atrasos. Para reduzir o risco desse problema, evite edições simultâneas, limite o número de guias abertas e salve as alterações com frequência.

Saiba mais sobre os modelos [nesta página](../email/use-email-templates.md).

+++

+++ Por que o campo Pré-cabeçalho de email não é exibido no modo &quot;Código seu próprio&quot;? 

No modo **&#39;Codifique você mesmo&#39;** sob o recurso **Editar Corpo do Email**, o campo de entrada do Pré-cabeçalho não é exibido. Para incluir texto de pré-cabeçalho, os usuários devem **codificar manualmente o pré-cabeçalho** no conteúdo personalizado de HTML.

Saiba mais sobre a configuração do pré-cabeçalho de email [nesta página](../email/header-parameters.md).

+++

+++ Por que há uma discrepância no comportamento do link ao usar um componente do HTML em modelos de email?  

Ao adicionar um **componente do HTML** a um modelo de email, os links podem ter um comportamento diferente, dependendo do **cliente de email**, do **modo de exibição** ou do **dispositivo/navegador**. Por exemplo, links de âncora podem funcionar de forma diferente na **exibição lado a lado do Outlook** em comparação à exibição em tela inteira. Esteja ciente dessas variações ao projetar modelos de email e testar em vários clientes e dispositivos.

Consulte também Práticas recomendadas de design de email [nesta página](../email/get-started-email-design.md).

+++


+++ Como evitar a ausência de links de rastreamento de email nos relatórios?

O rastreamento de link ausente no Adobe Journey Optimizer ocorre quando URLs de email usam variáveis dinâmicas e não começam com http ou quando declarações lógicas são colocadas no campo URL. Para resolver isso, verifique se todos os URLs começam com http, evite usar lógica no campo URL e mova lógica de personalização complexa para o conteúdo do HTML ou atributos pré-processados.

Saiba mais sobre o rastreamento de email [nesta página](../email/message-tracking.md).

+++

+++ Como resolver um erro do Mail Exchanger ao configurar campanhas de email transacionais acionadas por API? 

Se você encontrar um erro MX (Mail Exchanger) ao criar uma configuração de canal para uma campanha de email transacional acionada por API no Adobe Journey Optimizer, talvez seja devido a **configurações incorretas de DNS** ou **limitações de política da DMARC**. Para resolver isso, verifique se o DNS está configurado corretamente e se o domínio está em conformidade com os requisitos do **DMARC (Autenticação de Mensagens, Relatórios e Conformidade)**.

Saiba mais sobre as políticas de email do DMARC [nesta página](../configuration/dmarc-record-update.md).

Consulte também a [documentação de campanhas acionadas por API](../campaigns/api-triggered-campaigns.md).
+++

## Canal de push {#ajo-troubleshooting-push}

+++ Um perfil pode ter vários tokens de push no Adobe Journey Optimizer?

Ao implementar notificações por push no Journey Optimizer, um único perfil pode realmente ter vários tokens de push associados a diferentes dispositivos. Durante uma campanha de notificação por push, o Journey Optimizer foi projetado para gerenciar esses tokens e garantir que o perfil direcionado possa ser acessado em todos os dispositivos associados.

Saiba mais sobre a configuração de push [nesta página](../push/push-configuration.md).

Consulte também [fluxo de dados de notificação por push](../push/push-gs.md) para entender como os tokens são registrados e gerenciados de ponta a ponta.

+++

+++ Por que clicar em uma mensagem de push não me redireciona para o URL da Web configurado?  

Se as mensagens por push não estiverem redirecionando para o URL da Web pretendido, talvez seja devido à configuração incorreta da ação de clique ou às configurações desativadas de notificação por push. Verifique se a **ação de clique** para a mensagem de push está definida corretamente e se a **exibição e o rastreamento automáticos** das notificações por push estão habilitados para resolver esse problema.

Saiba mais sobre a configuração de push [nesta página](../push/push-configuration.md).

+++

+++ Por que as notificações por push estão falhando depois de atualizar as credenciais do aplicativo?

Credenciais de push expiradas ou configuradas incorretamente — como um certificado APNs para iOS ou uma chave FCM para Android — causam falhas de delivery silenciosamente. O Journey Optimizer não pode enviar notificações se as credenciais armazenadas na configuração do canal de push não corresponderem mais às registradas na plataforma do dispositivo. Atualize as credenciais na configuração do canal de push e verifique se a superfície de aplicativo móvel associada foi republicada.

Saiba como configurar credenciais de push [nesta página](../push/push-gs.md).

Consulte também a [documentação de configuração do canal de push](../push/push-configuration.md).

+++


## Canal de SMS {#ajo-troubleshooting-sms}

+++ Por que meu SMS transacional não é entregue mesmo que o consentimento esteja definido como `marketing.sms.value=y`?

Se um recipient responder **PARAR** a um SMS, todas as mensagens futuras desse número curto serão bloqueadas, incluindo mensagens transacionais. Para garantir a entrega ininterrupta de SMS transacional, configure-os e envie-os por meio de um **número curto separado** do qual os destinatários não tenham optado anteriormente.

Saiba mais sobre a configuração de recusa de SMS [nesta página](../sms/sms-opt-out.md).

+++

+++ Por que o delivery de SMS está falhando mesmo que o canal esteja configurado?

As falhas de delivery de SMS após a configuração do canal são causadas mais comumente por credenciais incorretas da API do provedor, uma incompatibilidade entre a ID do remetente e o que o provedor registrou ou restrições de roteamento no nível do provedor. Verifique se a chave da API, a senha e os detalhes do remetente inseridos no Journey Optimizer correspondem exatamente ao que o provedor de SMS provisionou. Em seguida, envie uma mensagem de teste para confirmar a conectividade antes de iniciar uma campanha.

Saiba como configurar seu provedor de SMS [nesta página](../sms/sms-configuration.md).

+++

+++ Como verificar se um perfil recusou comunicações SMS?

Quando um texto de perfil é PARADO, o Journey Optimizer atualiza o atributo de consentimento SMS do perfil. Para verificar o status atual de recusa, abra o perfil na interface do usuário do Experience Platform e inspecione os campos de consentimento em **Privacidade** > **Consentimentos**. Para solucionar problemas da campanha, verifique também os motivos de exclusão no relatório da campanha — os perfis recusados aparecem na contagem **Excluídos** com o motivo &quot;Recusado&quot;.

Saiba mais sobre como lidar com a recusa de SMS [nesta página](../sms/sms-opt-out.md).

+++

## Canal no aplicativo {#ajo-troubleshooting-inapp}

+++ Por que não posso criar relatórios no canal no aplicativo no Customer Journey Analytics?

As dificuldades para criar relatórios no **canal no aplicativo** no Adobe Customer Journey Analytics geralmente surgem de **visualizações de dados**, **conjuntos de dados** ou **atualizações de esquema** configuradas incorretamente. Verifique se essas configurações estão aplicadas corretamente para resolver o problema.

Consulte também a [documentação dos Relatórios de tempo integral do Journey Optimizer](../reports/report-gs-cja.md).

+++

+++ Por que minha mensagem no aplicativo não é exibida para os usuários?

As mensagens no aplicativo exigem que o Adobe Experience Platform Mobile SDK seja instalado corretamente e a extensão Mensagens seja registrada em seu aplicativo. Se a mensagem não estiver aparecendo, verifique se o SDK foi inicializado antes que o aplicativo tente buscar mensagens no aplicativo, se a superfície correta do aplicativo (ID do pacote) está configurada no Journey Optimizer e se a campanha está no status **Ativa**. Confirme também que o perfil atende aos critérios de público-alvo e ainda não foi limitado por uma regra de frequência.

Saiba como configurar o canal no aplicativo [nesta página](../in-app/inapp-configuration.md).

+++

+++ Por que minha campanha no aplicativo não está sendo acionada no evento esperado?

As campanhas no aplicativo são acionadas com base em nomes de evento que devem corresponder exatamente entre a implementação do SDK do aplicativo e a condição do acionador definida no Journey Optimizer. Uma incompatibilidade de maiúsculas, ortografia ou estrutura de conteúdo de evento impedirá o disparo do acionador. Use a ferramenta Adobe Experience Platform Assurance para inspecionar eventos SDK ao vivo e compará-los com a configuração de acionador da campanha.

Saiba como criar e configurar uma mensagem no aplicativo [nesta página](../in-app/create-in-app.md).

+++


## Cartões de conteúdo {#ajo-troubleshooting-content-cards}

+++ Por que os cartões de conteúdo não são exibidos no aplicativo?

Os cartões de conteúdo exigem que o Adobe Experience Platform Mobile SDK e o **Messaging SDK** sejam instalados, registrados e configurados no aplicativo. Diferentemente de mensagens por push ou no aplicativo, os cartões de conteúdo não são renderizados automaticamente. Seu aplicativo deve chamar explicitamente as APIs do SDK de mensagens para buscar os cartões disponíveis e renderizá-los na interface do usuário. Se os cartões não estiverem aparecendo, use o **Adobe Experience Platform Assurance** para verificar se as solicitações de decisão estão sendo enviadas quando o evento de destino for disparado e se as respostas estão voltando do Edge Network.

Saiba como configurar o suporte a cartões de conteúdo no Mobile SDK [nesta página](../content-card/content-card-configuration-sdk.md).

+++

+++ Os cartões de conteúdo exigem que o usuário conceda permissões de notificação por push?

Não. Os cartões de conteúdo são silenciosos e persistentes — eles não dependem das permissões de push no nível do SO e não são afetados pelo status de aceitação de notificação de um usuário. Isso os torna um canal de fallback útil para alcançar usuários que desativaram as notificações por push. Os cartões são obtidos do Edge Network enquanto o usuário está em sessão e exibidos na interface do usuário do seu aplicativo.

Saiba mais sobre o canal de cartão de conteúdo [nesta página](../content-card/get-started-content-card.md).

+++

+++ Por que as impressões do cartão de conteúdo não aparecem nos relatórios de campanha?

As impressões e interações do cartão de conteúdo (cliques, rejeições) não são rastreadas automaticamente. Seu aplicativo deve enviar eventos de rastreamento explicitamente de volta para o Adobe por meio da SDK de mensagens após renderizar um cartão e após qualquer interação do usuário com ele. Se essas chamadas de rastreamento estiverem ausentes na implementação do, os relatórios mostrarão zero impressões mesmo quando os cartões estiverem sendo fornecidos corretamente. Verifique se as chamadas de rastreamento estão sendo acionadas no **Assurance** antes de investigar a configuração da campanha.

Saiba como acessar relatórios de cartão de conteúdo [nesta página](../content-card/content-card-report.md).

Consulte também a [configuração de SDK do cartão de conteúdo](../content-card/content-card-configuration-sdk.md) para as chamadas de rastreamento necessárias.

+++

## WhatsApp {#ajo-troubleshooting-whatsapp}

+++ Por que minhas mensagens de WhatsApp não estão sendo enviadas?

A entrega de mensagens do WhatsApp requer o cumprimento de duas condições: o destinatário deve ter optado explicitamente por receber comunicações do WhatsApp da sua marca, e a mensagem deve usar um **modelo de mensagem pré-aprovado** registrado com a API de Negócios do WhatsApp. Se qualquer condição não for atendida, a mensagem será silenciosamente bloqueada pela plataforma WhatsApp antes do delivery. Verifique o status de aceitação nos atributos de consentimento do perfil do destinatário e confirme se o modelo está no status **Aprovado** na sua conta do WhatsApp Business.

Saiba como configurar o canal do WhatsApp [nesta página](../whatsapp/whatsapp-configuration.md).

+++

+++ Por que minha mensagem de WhatsApp é rejeitada com um erro de modelo?

A API de negócios do WhatsApp permite apenas modelos de mensagem pré-aprovados para mensagens de saída iniciadas por negócios. As mensagens de forma livre só são permitidas em uma janela de atendimento ao cliente de **24 horas**, ou seja, dentro de 24 horas após o cliente enviar uma mensagem primeiro para sua marca. Se a mensagem estiver sendo rejeitada, verifique se o modelo foi enviado e aprovado pelo Meta, se as variáveis de modelo (espaços reservados) na mensagem do Journey Optimizer correspondem exatamente à estrutura do modelo aprovado e se o modelo correto está selecionado na campanha ou ação de jornada.

Saiba como criar mensagens de WhatsApp [nesta página](../whatsapp/create-whatsapp.md).

+++

+++ Como coletar e verificar a aceitação do WhatsApp dos usuários?

O WhatsApp requer aceitação explícita antes de você enviar mensagens de marketing. O Opt-in pode ser coletado por meio de qualquer canal que sua marca controle — como um formulário da Web, aceitação dupla de SMS ou tela de consentimento no aplicativo — desde que o processo seja claro e documentado. Depois de coletado, atualize o atributo de consentimento do WhatsApp do perfil no Adobe Experience Platform. Para verificar o status de consentimento atual de um perfil, abra o perfil na interface do usuário do Experience Platform e inspecione a seção **Consentimentos**. Enviar para perfis sem consentimento válido viola as políticas de negócios do WhatsApp e pode resultar na suspensão da sua conta.

Saiba como começar a usar o canal do WhatsApp [nesta página](../whatsapp/get-started-whatsapp.md).

+++

## Gerenciamento de dados {#ajo-troubleshooting-data-management}

+++ Como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados de Perfil e Data Lake ao criar uma nova sandbox?

As organizações que provisionam novas sandboxes na Adobe Journey Optimizer levantaram questões sobre como as configurações de Tempo de vida (TTL) se aplicam aos conjuntos de dados do Perfil e do Data Lake. As configurações de TTL não afetam as sandboxes existentes e são aplicadas automaticamente apenas às recém-provisionadas.

Saiba mais sobre o tempo de vida útil do conjunto de dados [nesta página](../data/datasets-ttl.md).

+++

+++ Por que um conjunto de dados não está sendo ativado para o Perfil do cliente em tempo real?

Para que um conjunto de dados habilite a personalização baseada em perfil e as condições de jornada no Journey Optimizer, dois requisitos devem ser atendidos: o esquema XDM subjacente deve ter o **Perfil** habilitado e o próprio conjunto de dados deve ser ativado para o **Perfil de cliente em tempo real** na interface do usuário do Experience Platform. Se um deles estiver ausente, os dados serão assimilados no Data Lake, mas não serão mesclados em perfis unificados. Além disso, verifique se o conjunto de dados contém pelo menos um campo de identidade mapeado a um namespace reconhecido.

Saiba como configurar conjuntos de dados [nesta página](../data/get-started-datasets.md).

Consulte também a [visão geral do gerenciamento de dados](../data/gs-data.md) para obter a lista de verificação de instalação completa.

+++

+++ Como monitorar e resolver falhas de assimilação de dados?

As falhas de assimilação aparecem no painel de **Monitoramento** do Adobe Experience Platform em **Fontes** > **Fluxos de dados**. Causas comuns incluem erros de validação de esquema (um campo nos dados de origem não corresponde ao esquema XDM), campos de identidade obrigatórios ausentes ou cargas JSON malformadas. Abra o registro de lote com falha para ver o código de erro específico e as linhas afetadas. Corrija os dados de origem e assimile novamente ou ajuste o mapeamento do schema se o formato de origem tiver alterado.

Saiba mais sobre esquemas e configuração de dados [nesta página](../data/gs-data.md).

+++


## Gerenciamento de perfis e público-alvo {#ajo-troubleshooting-audiences}

+++ Como resolver discrepâncias de contagem de público-alvo?

O número de entradas processadas no recurso **Ler Público** do Adobe Journey Optimizer pode ser menor que o contagem de público-alvo esperado. Esse problema geralmente ocorre devido a configurações incorretas de namespace, levando à exclusão de perfis das jornadas. A resolução envolve verificar e corrigir configurações de namespace, revisar documentação relevante e ajustar prioridades para garantir operações mais suaves no Adobe Journey Optimizer.

Saiba mais sobre a atividade **Ler público** no jornada [nesta página](../building-journeys/read-audience.md).

+++

+++ Por que as atualizações de perfil estão falhando?

No Adobe Journey Optimizer, determinados valores de campo podem não ser atualizados corretamente após serem executados por uma atividade **Atualizar Perfil** em uma jornada. Em alguns casos, os campos atualizados podem desaparecer ou reverter para o estado anterior. Para resolver isso, verifique se há regras ou condições conflitantes, revise as configurações de permissões, use um conjunto de dados exclusivo para a atividade **Atualizar perfil** e verifique se nenhum outro processo de assimilação está gravando no mesmo perfil ao mesmo tempo.

Saiba mais sobre a atividade **Atualizar Perfil** no jornada [nesta página](../building-journeys/update-profiles.md).

+++

+++ Por que há uma incompatibilidade na contagem de perfis ao inserir uma jornada em relação ao público-alvo associado?

A discrepância pode ocorrer quando a jornada usa um instantâneo de perfil de um dia anterior, se o instantâneo do dia atual não estiver disponível no momento da execução da jornada. Para investigar, verifique quando seu trabalho diário de segmentação foi executado pela última vez e se a jornada foi acionada antes que o instantâneo estivesse pronto.

Saiba mais sobre a atividade **Ler público** e o comportamento do agendamento [nesta página](../building-journeys/read-audience.md).

+++

+++ Por que o seletor de público-alvo mostra contagens de perfis diferentes em Campanhas e Jornadas?

Você pode notar que o mesmo público-alvo exibe contagens de perfil diferentes quando visualizado em Campanhas, em comparação com Jornadas. Isso acontece porque cada recurso usa APIs diferentes para recuperar dados de público-alvo, que podem retornar valores diferentes.

Esse é um comportamento esperado e não afeta a execução da campanha. Os perfis corretos ainda serão segmentados. Para verificar o tamanho real do público, vá para **[!UICONTROL Cliente]** > **[!UICONTROL Públicos-alvo]** e selecione seu público-alvo.

+++


+++ Como resolver problemas de preenchimento de público-alvo?

Problemas no preenchimento do público podem ocorrer quando componentes ou recursos estão ausentes, geralmente devido a erros de configuração de direito, provisionamento ou permissão. Para corrigir esses problemas, comece verificando os direitos, garantindo o provisionamento correto e revisando as permissões. Se o problema persistir, encaminhe o caso e fale com as equipes de suporte para obter uma resolução completa.

Saiba mais sobre como gerenciar públicos-alvo [nesta página](../audience/about-audiences.md).

+++

+++ Por que a contagem de perfis ativáveis aumentou significativamente em um curto período? 

A métrica **Perfis ativáveis** reflete o número de perfis exclusivos ativados por jornadas ou campanhas nos últimos 12 meses. Um aumento súbito pode resultar de jornadas ou campanhas direcionadas a públicos-alvo grandes que não foram envolvidos recentemente, ou de alterações nos conjuntos de dados habilitados para o Serviço de perfil.

Para investigar e resolver esse problema, você precisa entender a lógica de contagem de perfis, investigar jornadas e campanhas direcionadas a públicos-alvo grandes, filtrar públicos-alvo adequadamente, monitorar alterações no conjunto de dados e possivelmente reduzir o tamanho do público-alvo endereçável.

Saiba como solucionar problemas e resolver aumentos de Perfis envolventes e monitorar o uso de licença da sua organização na [documentação do Painel de Uso de Licenças](../audience/license-usage.md#troubleshooting-engageable-profiles).

+++

+++ Por que os emails são enviados para indivíduos fora do público-alvo com base nas funções de data?

Emails podem ser enviados a destinatários que **não atendem aos critérios de público-alvo especificados**. Por exemplo, os membros com datas de resgate **anteriores a 4 de julho de 2025** podem receber emails destinados somente àqueles após essa data. Este comportamento pode resultar de **segmentação de público configurada incorretamente** ou **alterações inesperadas na lógica de qualificação de perfil**. Revise a definição do público-alvo e teste com perfis de amostra para verificar se a lógica de data é aplicada corretamente.

Saiba mais sobre funções de data [nesta página](../building-journeys/functions/date-functions.md).

+++

+++ Por que Entregas + Exclusões excedem meu tamanho de público-alvo nos relatórios de campanha?

Nos relatórios de campanha, você pode notar que a soma de **Entregues** e **Exclusões** excede o tamanho original do público-alvo direcionado. Isso ocorre porque a métrica **Exclusões** conta todos os eventos de exclusão, incluindo eventos de exclusão duplicados para o mesmo perfil. Se um perfil for excluído várias vezes durante uma campanha, cada evento será contado separadamente.

**Exemplo**: uma campanha direcionada a 94.000 perfis mostra 69.000 entregas e 37.000 exclusões, totalizando 106.000 — o que excede os 94.000 perfis direcionados originais. Esse é o comportamento esperado.

Para entender a diferença entre os eventos de exclusão total e as exclusões de perfil exclusivas, consulte a [Explicação da contagem de exclusões](../reports/exclusion-list.md#exclusion-list).

Saiba mais sobre [Relatórios de campanha](../reports/campaign-global-report-cja.md) e [Métricas de relatório](../reports/global-report-components-cja.md).

+++

+++ Como resolver problemas de seleção de público-alvo e erros do Chrome ao salvar jornadas?

A adição de públicos-alvo às condições de jornada pode, às vezes, causar **travamentos do aplicativo** ou exibir um **Erro do Aw Snap** no Chrome, incluindo erros ao salvar jornadas. Estes problemas estão frequentemente relacionados com os **serviços Chromium**. Para resolvê-los, aplique uma **atualização do navegador**, limpe o cache do navegador ou tente outra sessão do navegador.

Saiba mais sobre [navegação na interface do Journey Optimizer](user-interface.md).

+++

## Jornadas {#ajo-troubleshooting-journeys}

Para obter Jornadas, consulte as seguintes seções de solução de problemas:

* [Solucionar erros antes de testar a jornada](../building-journeys/troubleshooting.md)
* [Solucionar problemas de ações de entrada em jornadas](../building-journeys/troubleshooting-inbound.md)
* [Solucionar problemas de execução do Live jornada](../building-journeys/troubleshooting-execution.md)
* [Solução de problemas de ações personalizadas](../action/troubleshoot-custom-action.md)


+++ Por que as expressões são perdidas ao criar uma nova versão do jornada?  

Ao criar uma nova versão de uma jornada, **expressões em etapas específicas** podem ser perdidas, causando erros e exigindo reentrada manual. Para resolver isso, **duplique a jornada**, teste a reprodutibilidade, **evite recarregamentos de navegador** e use a **tela atualizada** para jornadas mais antigas.

Saiba como duplicar uma jornada [nesta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Por que os perfis saem do jornada prematuramente? 

Os perfis podem sair de uma jornada inesperadamente sem passar por um nó designado quando a **condição que verifica o status de feedback** das mensagens enviadas está configurada incorretamente. Para resolver isso, revise a **lógica de condição**, implemente a **lógica alternativa** ou consulte sua **equipe de implementação**.

Consulte também [diretrizes de design do Jornada](../building-journeys/using-the-journey-designer.md).

+++


+++ Por que os perfis estão saindo das jornadas inesperadamente?

Perfis podem sair de uma jornada inesperadamente quando **event capping** ocorrer, fazendo com que alguns perfis sejam descartados se o número de eventos processados exceder a capacidade do sistema. Para reduzir saídas de perfil, compreenda os **limites de sistema**, monitore **picos de evento** e otimize o **fluxo de dados** para evitar limites excedidos.

Consulte também [medidas de proteção da Jornada](../start/guardrails.md#decisioning-guardrails).

+++


+++ Por que meu evento não está acionando a jornada pretendida?  

Eventos podem deixar de disparar uma jornada, mesmo que todos os critérios sejam atendidos quando forem **criados por meio de serviços de consulta**, em vez de serem transmitidos para o **Serviço Principal de Coleta de Dados (DCCS)**. Para resolver isso, revise a configuração do evento, verifique se os eventos são **transmitidos diretamente para DCCS** e verifique a funcionalidade usando o **modo de teste**.

Saiba mais sobre os eventos [nesta página](../event/about-events.md).

Consulte também [Jornada medidas de proteção de eventos](../start/guardrails.md#events-g).

+++


+++ Como resolver problemas de acionador do jornada após alterações de público-alvo no Adobe Journey Optimizer? 

Se uma jornada parar de ser acionada depois de modificações no público-alvo associado, como alterações na política de mesclagem, você poderá enfrentar fluxos interrompidos. Para resolver isso, **duplique e republique a jornada** com as configurações de público atualizadas para garantir que os acionadores funcionem corretamente.

Saiba como duplicar uma jornada [nesta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Por que uma ação personalizada que chama um ponto de extremidade de terceiros externo atinge o tempo limite?

Podem ocorrer erros de tempo limite quando uma **ação personalizada** chama um ponto de extremidade de terceiros externo. Para resolver isso, verifique se o **ponto de extremidade está acessível**, verifique os **logs do servidor**, verifique se há **nenhum bloqueio do Adobe**, atualize as configurações do ponto de extremidade conforme necessário e **teste após as atualizações**. Além disso, lembre-se de **especificações de tempo limite de chamada de API**.

Saiba mais sobre a API de Limitação do Jornada [nesta página](../configuration/throttling.md).

Consulte também a [documentação sobre integração com sistemas externos](../configuration/external-systems.md).

+++

+++ Que etapas seguir se você encontrar um erro 403 com a mensagem **invalid_access** ou **No access to this dataId=XX granted** ao publicar um público-alvo de uma jornada?

Para resolver esse erro, peça ao administrador para verificar se o perfil do usuário tem acesso às visualizações de dados necessárias para publicação do público-alvo e tente publicar o público novamente.

Consulte [a documentação de permissões](../administration/permissions.md) para saber mais sobre as etapas para resolver esse problema.

+++

## Regras {#ajo-troubleshooting-rules}

+++ Por que a lista suspensa Regras de limite não está funcionando?

Problemas com a **Lista suspensa de regras de limite** ocorrem frequentemente quando os conjuntos de regras estão **configurados incorretamente** ou **inacessíveis**. Verifique se todos os conjuntos de regras estão configurados corretamente e disponíveis para resolver o problema.

Saiba como aplicar as regras de limitação [nesta seção](../conflict-prioritization/rule-sets.md).

+++

+++ Por que uma regra de limite de frequência não está sendo aplicada à minha campanha ou jornada?

As regras de limite de frequência só têm efeito quando o conjunto de regras é explicitamente anexado à campanha ou jornada. Se o limite não estiver funcionando, verifique se o conjunto de regras correto está selecionado nas configurações de campanha ou jornada, se o tipo de canal da regra corresponde ao canal que está sendo usado e se a regra está no status **Ativo**. Verifique também se o perfil já atingiu o limite em uma execução anterior, o que impediria mais mensagens, mesmo se a regra aparecesse configurada corretamente.

Saiba como configurar as regras de limite de canal [nesta página](../conflict-prioritization/channel-capping.md).

+++

+++ Como configurar horários de silêncio para impedir que mensagens sejam enviadas à noite?

As horas de silêncio são regras de exclusão baseadas em tempo configuradas em um **Conjunto de regras de canal**. Defina a janela de blecaute (por exemplo, 22h às 8h) e aplique o conjunto de regras às campanhas ou jornadas relevantes. Quando uma mensagem é programada para ser enviada durante as horas de silêncio, o Journey Optimizer retém a mensagem até a próxima janela permitida ou a descarta, dependendo da configuração da regra.

Saiba como configurar o horário de silêncio [nesta página](../conflict-prioritization/quiet-hours.md).

+++

## Tomada de decisão {#ajo-troubleshooting-decisioning}

+++ Como resolver problemas ao criar coleções de ofertas?

Dificuldades para criar coleções de ofertas geralmente ocorrem quando **catálogos não foram provisionados** para sua organização. Para resolver isso, verifique se todos os catálogos necessários estão provisionados corretamente antes de tentar criar coleções de ofertas.

Saiba mais sobre coleções de ofertas [nesta página](../offers/offer-library/creating-collections.md).

+++

+++ Por que não consigo acessar o Offer Decisioning?  

Ao integrar o Adobe Target em um aplicativo usando o Adobe Journey Optimizer, a opção **Offer Decisioning** pode estar inacessível na configuração de sequência de dados. Isso geralmente ocorre devido a **configurações de permissão** ou **restrições de provisionamento**. Para resolver o problema, verifique as permissões do usuário e se o provisionamento necessário está em vigor.

Saiba mais sobre as permissões necessárias para o Offer Decisioning [nesta página](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++

+++ Por que uma oferta não é retornada mesmo que atenda aos critérios de qualificação?

Se uma oferta qualificada não estiver aparecendo em uma resposta de decisão, verifique a seguinte ordem: verifique se a oferta está no status **Aprovado** (não Rascunho); confirme se a ID de posicionamento na solicitação corresponde à superfície de representação da oferta; verifique se algum limite (total ou por perfil) foi atingido para essa oferta; e verifique se o escopo de coleta e decisão está configurado corretamente. Use a ferramenta **Simulação** no Experience Decisioning para testar as respostas da oferta em relação a um perfil específico sem enviar tráfego direto.

Saiba como começar a usar o Experience Decisioning [nesta página](../experience-decisioning/gs-experience-decisioning.md).

+++


## Multilíngue {#ajo-troubleshooting-multilingual}

+++ Como resolver este problema `Message validation error (CJMMAS - 1069-500)`?

No Adobe Journey Optimizer, um Erro de validação de mensagem (CJMAS - 1069-500) vinculado ao recurso multilíngue impede que as jornadas sejam definidas para o modo Teste ou Publicadas. Verifique se todo o conteúdo da localidade está concluído, se o idioma principal está definido corretamente e se nenhum campo de tradução necessário está vazio antes de tentar publicar.

Saiba mais sobre o conteúdo multilíngue [nesta página](../content-management/multilingual-gs.md).

+++

+++ Por que o provedor de tradução não está se conectando no Journey Optimizer?

As falhas de conexão do provedor de tradução geralmente são causadas por credenciais de API incorretas ou por uma configuração de provedor ausente nas configurações multilíngues. Verifique se a chave da API, o URL do endpoint e os tokens de autenticação necessários inseridos no Journey Optimizer correspondem exatamente ao que o fornecedor de tradução provisionou. Se as credenciais estiverem corretas, verifique se a conta do provedor tem cota suficiente ou status de assinatura ativo, salve e teste a conexão novamente.

Saiba como configurar um provedor de tradução [nesta página](../content-management/multilingual-provider.md).

+++

+++ O que acontece quando uma tradução está ausente em um local?

Se uma tradução não tiver sido fornecida para uma localidade específica, o Journey Optimizer voltará ao conteúdo definido no **idioma principal** (localidade de fallback) definido nas configurações de idioma. Se nenhum fallback estiver configurado, a mensagem poderá ser renderizada como vazia ou falhar na validação antes do envio. Para evitar isso, sempre defina um local de fallback nas configurações do projeto multilíngue e verifique se todos os locais aprovaram traduções antes de ativar a campanha ou a jornada.

Saiba mais sobre a configuração de conteúdo multilíngue [nesta página](../content-management/multilingual-gs.md).

+++


## Configuração {#ajo-troubleshooting-config}

+++ Como habilitar TLS v1.3 para Ações Personalizadas?  

Para manter a **integridade e a segurança dos dados** ao se conectar a sistemas de terceiros, verifique se o Transport Layer Security (**TLS**) v1.3 está habilitado para suas ações personalizadas. Isso ajuda a proteger as comunicações e evita possíveis vulnerabilidades de segurança.

Saiba mais sobre a configuração de ação personalizada [nesta página](../action/about-custom-action-configuration.md).

+++

+++ Por que não consigo criar um painel diretamente de um query no Adobe Journey Optimizer? 

No Adobe Journey Optimizer, os painéis não podem ser criados diretamente de consultas. Para criar painéis, use as **funcionalidades de criação de painel** disponíveis no Adobe Experience Platform, que permitem visualizar e analisar dados de consulta com eficiência.

Saiba mais sobre consultas no Journey Optimizer [nesta página](../data/get-started-queries.md).

+++

+++ Por que minhas mensagens estão sendo bloqueadas pela lista de supressão?

Os endereços são adicionados automaticamente à lista de supressão após devoluções permanentes, reclamações de spam ou adições manuais por um administrador. Depois de suprimido, um perfil não receberá mensagens desse canal, independentemente do direcionamento de campanha ou jornada. Para investigar, abra **Administração** > **Canais** > **Lista de supressão** e procure o endereço. Se a supressão tiver sido adicionada com erro, ela poderá ser removida diretamente da interface. Para supressões de rejeição permanente, revise também o problema subjacente de capacidade de entrega antes de remover o endereço.

Saiba como gerenciar a lista de supressão [nesta página](../configuration/manage-suppression-list.md).

+++

## APIs {#ajo-troubleshooting-apis}

+++ Como resolver problemas de acesso com a API do Serviço de consulta?  

Erros de acesso ao usar a **API de Serviço de Consulta** via Postman ou ferramentas semelhantes geralmente são causados por **permissões insuficientes**. Para resolver isso, verifique as permissões do usuário, as credenciais da API em relação às funções configuradas em sua organização e forneça informações detalhadas para suporte, se necessário.

Saiba mais sobre permissões no Journey Optimizer [nesta página](../administration/permissions.md).

+++

+++ Como resolver erros de 429 muitas solicitações ao chamar APIs do Journey Optimizer?

Uma resposta 429 significa que sua integração excedeu o limite de taxa da API para o endpoint. Cada API do Journey Optimizer definiu limites de taxa de transferência. Para resolver isso, implemente a lógica de **retirada exponencial** na sua integração: aguarde a duração especificada no cabeçalho de resposta `Retry-After` antes de tentar novamente. Para casos de uso de alto volume contínuo, revise a configuração de limitação e limite para suas ações personalizadas e fontes de dados para alinhar as taxas de chamada da API aos limites do sistema.

Saiba mais sobre a limitação do Journey Optimizer [nesta página](../configuration/throttling.md).

Consulte também a [documentação de integração de sistemas externos](../configuration/external-systems.md).

+++

+++ Por que minha campanha acionada por API não é executada após a chamada de API?

Se uma campanha acionada por API não estiver em execução, verifique o seguinte: a campanha está no status **Live** (não é rascunho ou foi interrompida); a chamada de API inclui a ID de campanha correta no caminho do ponto de extremidade; a carga da solicitação corresponde ao esquema do identificador de perfil esperado pela campanha; e as credenciais de API usadas têm a permissão **Gerenciar Campanhas**. Verifique os logs de execução da campanha no painel de relatórios para identificar se o perfil foi recebido, mas excluído, ou se a chamada não chegou à campanha.

Saiba mais sobre campanhas acionadas por API [nesta página](../campaigns/api-triggered-campaigns.md).

+++
