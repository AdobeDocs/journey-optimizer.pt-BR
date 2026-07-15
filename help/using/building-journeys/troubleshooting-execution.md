---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar problemas de execução de jornada em tempo real
description: Saiba como solucionar erros na execução de jornada em tempo real
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: solução de problemas, solução de problemas, jornada, verificação, erros
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/2YZ6Cjph9Le-HtwKdz4GBgEdhwIMPpVtj9yWKlV3hQ4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 8d9c09a7be3757624c72a0a9d2739d0dbb48adeb
workflow-type: tm+mt
source-wordcount: 3051
ht-degree: 8%

---

# Solucionar problemas de execução de jornada em tempo real {#troubleshooting-execution}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como solucionar problemas de execução de uma jornada ao vivo, incluindo a verificação de que eventos são enviados, a confirmação da entrada de perfis e o progresso pela jornada, além da verificação de que as mensagens são entregues.

>[!ENDSHADEBOX]

Nesta seção, saiba como solucionar problemas de eventos de jornada, verificar se os perfis inseriram sua jornada, como eles navegam por ela e se as mensagens são enviadas.

Você também pode solucionar problemas de erros antes de testar ou publicar uma jornada. Saiba mais sobre [nesta página](troubleshooting.md).

Se você estiver usando ações de entrada, saiba como solucionar problemas deles [nesta página](troubleshooting-inbound.md).

## Verifique se os eventos foram enviados corretamente {#checking-that-events-are-properly-sent}

O ponto de partida de uma jornada é sempre um evento. Você pode fazer testes usando ferramentas como o Postman.

Você pode verificar se a chamada à API enviada por meio dessas ferramentas foi corretamente enviada. Se ocorrer um erro, significa que a chamada tem um problema. Verifique novamente o payload, o cabeçalho (e principalmente a ID da organização) e o URL de destino. Você pode perguntar ao administrador qual é o URL correto para a ocorrência.

Eventos não são levados diretamente da origem para jornadas. Na verdade, o jornada depende das APIs de assimilação de streaming de [!DNL Adobe Experience Platform]. Como resultado, no caso de problemas relacionados ao evento, consulte a [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} para obter a solução de problemas de APIs de assimilação de streaming.

Se a jornada não conseguir habilitar o modo de teste com erro `ERR_MODEL_RULES_16`, verifique se o evento usado inclui um [namespace de identidade](../audience/get-started-identity.md) ao usar uma ação de canal.

O namespace de identidade é usado para identificar exclusivamente os perfis de teste. Por exemplo, se o email for usado para identificar os perfis de teste, o namespace de identidade **Email** deverá ser selecionado. Se o identificador exclusivo for o número de telefone, o namespace de identidade **Telefone** deverá ser selecionado.

## Verificar se as pessoas entram na jornada {#checking-if-people-enter-the-journey}

O relatório de Jornada mede a entrada das pessoas em uma jornada em tempo real.

Se você enviar o evento com êxito, mas não vir nenhuma entrada na jornada, significa que há algo de errado entre o envio do evento e a recepção do evento na jornada.

Você pode começar a solucionar problemas com as perguntas abaixo:

* Você tem certeza de que a jornada em que você espera o evento de entrada está no modo de teste ou ativa?
* Você salvou o evento antes de copiar o payload da pré-visualização de payload?
* O payload do evento contém uma ID do evento?
* Você digitou o URL correto?
* Você seguiu a estrutura de payload das APIs de ingestão de transmissão usando a pré-visualização da estrutura de payload no painel de configuração do evento? Consulte [esta página](../event/about-creating.md#preview-the-payload).
* Você usou os pares de valor chave corretos no cabeçalho do evento?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

* **Condição de evento e tipos de dados de esquema** - Verifique se os tipos de dados usados na condição (regra) do evento correspondem ao esquema do evento. Tipos incompatíveis (por exemplo, sequência de caracteres vs. número inteiro) fazem com que a avaliação da regra falhe e os eventos sejam descartados. Consulte [Verificar identidade do evento](#verify-event-identity-and-rule-data-types).

* **Evento descartado - condição de qualificação não atendida** - Para eventos baseados em regras, se a **condição de qualificação** não for atendida pela carga do evento (por exemplo, um campo obrigatório está vazio ou ausente ou uma condição como `isNotEmpty` em um campo falha), o evento será **recebido, mas descartado** e a jornada não será acionada. Registros e rastreamentos do Splunk podem mostrar que o evento foi recebido, mas descartado porque não atendia à condição de qualificação, com códigos de descarte como `notSuitableInitialEvent`. Esse é o comportamento esperado: se a condição de qualificação não for atendida, o evento será descartado e a jornada não será acionada para esse perfil. Verifique se a carga do evento contém os campos e valores esperados e se a regra na configuração do evento corresponde aos dados enviados. Se o evento for acionado por uma **ação personalizada** de outra jornada, consulte [Manipulação de eventos de descarte e tempos limite ociosos](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts) na solução de problemas de ação personalizada.

>>
**Para jornadas de qualificação de público-alvo com públicos-alvo de streaming**: se estiver usando uma atividade de qualificação de público-alvo como ponto de entrada de jornada, esteja ciente de que nem todos os perfis qualificados para o público-alvo necessariamente entrarão na jornada devido a fatores de tempo, saídas rápidas do público-alvo ou se os perfis já estiverem no público-alvo antes da publicação. Saiba mais sobre [considerações de tempo de qualificação de público de streaming](audience-qualification-events.md#streaming-entry-caveats).

### Verificar identidade do evento {#verify-event-identity-and-rule-data-types}

Ao configurar uma jornada baseada em eventos, confirme se o campo de identidade da carga corresponde ao [namespace selecionado no evento](../event/about-creating.md#select-the-namespace). Se o evento incluir campos para correspondência de perfil, verifique se a **letra maiúscula** e o **tipo de dados** na condição do evento correspondem exatamente aos dados de entrada. Por exemplo, se o esquema de evento definir `roStatus` como uma cadeia de caracteres, a regra de jornada também deverá avaliá-la como uma cadeia de caracteres. Tipos de dados incompatíveis (por exemplo, sequência de caracteres vs. número inteiro) fazem com que a avaliação da regra falhe e eventos válidos sejam descartados. Da mesma forma, se o evento tiver uma **condição de qualificação** (por exemplo, um campo não deve estar vazio), os eventos que não satisfizerem essa condição serão **descartados** e não acionarão a jornada; os logs poderão mostrar códigos de descarte como `notSuitableInitialEvent`.

Para validar a condição do evento em [!DNL Journey Optimizer], use a pré-visualização de carga na configuração do evento e verifique se os tipos e valores na regra correspondem à estrutura de carga. Saiba como [visualizar a carga](../event/about-creating.md#preview-the-payload) e [configurar eventos baseados em regras](../event/about-creating.md).

## Solução de problemas de transições do modo de teste {#troubleshooting-test-transitions}

Se os perfis de teste não avançarem na jornada no modo de teste ou o fluxo visual não exibir setas verdes indicando a progressão da etapa, o problema pode estar relacionado à validação da transição. Esta seção fornece orientação sobre como diagnosticar e resolver problemas comuns de modo de teste.

### Os perfis de teste não estão progredindo

Se os perfis de teste entrarem na jornada, mas não avançarem além da etapa inicial, verifique o seguinte:

* **Data de início da Jornada** - A causa mais comum é quando a data de início da jornada é definida no futuro. Os perfis de teste são imediatamente descartados se a hora atual estiver fora da janela [datas/hora de início e término](journey-properties.md#dates) configurada da jornada, produzindo a entrada de log: `DISPATCHER DISCARD #16 — unqualified on journey version enablements`. Para resolver:
   * Verificar se a data de início da jornada não está definida no futuro
   * Garantir que a hora atual esteja na janela de datas ativa da jornada
   * Se necessário, defina temporariamente a data de início para uma hora antes do momento atual para testes e, em seguida, restaure-a antes de publicar

* **Configuração do perfil de teste** - Confirme se o perfil está sinalizado corretamente como um perfil de teste em [!DNL Adobe Experience Platform]. Consulte [como criar perfis de teste](../audience/creating-test-profiles.md) para obter mais informações.

* **Incompatibilidade de namespace de identidade** - Uma incompatibilidade de namespace causa uma queda silenciosa: o evento é aceito e retorna uma resposta bem-sucedida, mas o perfil nunca entra na jornada e nenhum erro é exibido na interface. Verifique se o namespace no **Identificador de Perfil** corresponde exatamente ao namespace definido no esquema de evento (diferencia maiúsculas de minúsculas). Consulte o [formato de expressão do Identificador de Perfil](testing-the-journey.md#trigger-events-prerequisites) para obter detalhes.

### Indicadores de transição nulos

Durante a solução de problemas técnicos, você pode encontrar uma propriedade `isValidTransition` definida como nula nos detalhes técnicos da jornada. Essa propriedade somente de interface do usuário não afeta o processamento de back-end ou o desempenho da jornada. No entanto, um valor nulo pode indicar:

* **Configuração incorreta da Jornada** - A data de início da jornada está definida no futuro, fazendo com que os eventos de teste sejam descartados silenciosamente
* **Transição corrompida** - Em casos raros, talvez seja necessário reconectar os nós de jornada

Se você encontrar problemas de transição persistentes:

1. Verifique se a data de início da jornada é a atual
1. Desativar e reativar o modo de teste
1. Se o problema persistir, considere duplicar os nós de jornada afetados e reconectá-los
1. Para casos não resolvidos, [contate o suporte](../start/user-interface.md#support-ticket-guidelines) com os logs do jornada, as IDs de perfil afetadas e os detalhes sobre a transição nula

>[!NOTE]
>
>Eventos enviados fora da janela de data ativa da jornada são silenciosamente descartados com a entrada de log `DISPATCHER DISCARD #16 — unqualified on journey version enablements` e nenhum erro de interface. Sempre verifique a configuração de tempo da jornada primeiro ao solucionar problemas de progressão do perfil de teste.

## Verificar como as pessoas navegam pela jornada {#checking-how-people-navigate-through-the-journey}

O relatório de jornada mede o progresso das pessoas físicas dentro de uma jornada. É fácil identificar onde e por que uma pessoa foi parada.

Veja algumas coisas que devem ser verificadas:

* A interrupção se deve a uma condição que exclui a pessoa? Por exemplo, a condição é &quot;gênero = homem&quot; e a pessoa é uma mulher. Essa verificação pode ser feita por um usuário empresarial se a condição não for muito complexa.
* A interrupção se deve a uma chamada a uma fonte de dados que não está respondendo? Quando a jornada está em teste, essas informações podem ser vistas nos registros do modo de teste. Quando a jornada é em tempo real, um administrador pode testar chamadas diretas para a fonte de dados e verificar a resposta recebida. Um administrador também pode duplicar a jornada e testá-la.

## Eventos descartados devido a uma instância de jornada bloqueada {#max-instance-stack-events-reached}

Se você vir eventos descartados com o motivo `maxInstanceStackEventsReached`, o tempo de execução da jornada atingiu seu limite interno de pilha de eventos por perfil de 10 eventos para uma versão específica do jornada. Essa é uma proteção de segurança que impede o empilhamento de muitos eventos pendentes enquanto outro evento do mesmo perfil ainda está sendo processado.

Este é **não** uma janela de tempo ou um limite de taxa de transferência. Isso ocorre quando a instância do jornada do perfil é bloqueada em uma etapa de longa duração (por exemplo, uma longa espera, um enriquecimento ou tentativas de ação personalizada) e eventos para o mesmo perfil, que também está sendo usado nessa jornada, se acumulam além do limite de 10 eventos.

Para identificá-la, consulte os eventos de etapa de jornada em que o motivo do descarte é igual a `maxInstanceStackEventsReached` (por exemplo, em `serviceEvents.stateMachine.eventType` ou campos semelhantes). Saiba mais sobre tipos de eventos descartados na [lista de campos de eventos de etapa](../reports/sharing-field-list.md#discarded-events).

**O que você pode fazer**

* Reduza longas esperas ou etapas lentas em caminhos que podem ser acionados novamente com frequência.
* Elimine duplicatas ou evite eventos upstream quando possível.
* Divida os cenários de longa duração em várias jornadas para evitar o empilhamento.

## Verificar se as mensagens foram enviadas com êxito {#checking-that-messages-are-sent-successfully}

Se as pessoas físicas continuarem percorrendo o caminho certo na jornada, mas não receberem as mensagens esperadas, você poderá verificar se:

* [!DNL Journey Optimizer] levou em consideração corretamente a solicitação para enviar a mensagem. Os usuários empresariais podem acessar a mensagem que deve ser enviada e verificar se a hora da execução mais recente corresponde ao tempo de execução da sua jornada. Eles também podem verificar as chamadas/eventos de API mais recentes recebidos.
* [!DNL Journey Optimizer] enviou a mensagem com êxito. Verifique os relatórios do jornada para garantir que não haja erros.

No caso de uma mensagem enviada por meio de uma ação personalizada, a única coisa que pode ser verificada durante o teste de jornada é o fato de a chamada do sistema da ação personalizada causar ou não um erro. Se a chamada para o sistema externo associada à ação personalizada não causar um erro, mas não enviar a mensagem, algumas investigações devem ser feitas por parte do sistema externo.

## Noções básicas de entradas duplicadas em eventos de etapa de Jornada {#duplicate-step-events}

Use esta seção para entender por que as linhas duplicadas podem aparecer nos Eventos de etapa de Jornada.

### Por que vejo várias entradas com a mesma instância, perfil, nó e IDs de solicitação do jornada?

Ao consultar os dados de Eventos de etapa de Jornada, você pode observar ocasionalmente o que parece ser entradas de log duplicadas para a mesma execução de jornada. Essas entradas compartilham valores idênticos para:

* `profileID` - A identidade do perfil
* `instanceID` - O identificador de instância do jornada
* `nodeID` - O nó de jornada específico
* `requestID` - O identificador da solicitação

No entanto, essas entradas têm **valores `_id` diferentes**, que é o indicador principal que distingue este cenário da duplicação de dados real.

### O que causa esse comportamento?

Isso ocorre devido a operações de dimensionamento automático de back-end (também chamadas de &quot;rebalanceamento&quot;) na arquitetura de microsserviços do [!DNL Adobe Journey Optimizer]. Durante períodos de alta carga ou otimização do sistema:

1. Um evento de etapa de jornada começa a ser processado e é registrado no conjunto de dados de Eventos de etapa de Jornada
2. Uma operação de dimensionamento automático redistribui a carga de trabalho entre instâncias de serviço
3. O mesmo evento pode ser reprocessado por outra instância de serviço, criando uma segunda entrada de log com um `_id` diferente

Este é um comportamento de sistema esperado e **está funcionando como projetado**.

### Há algum impacto na execução da jornada ou na entrega de mensagens?

**Não.** O impacto é limitado apenas ao registro em log. [!DNL Adobe Journey Optimizer] tem mecanismos de desduplicação internos na camada de execução da mensagem que garantem:

* Somente uma mensagem (email, SMS, notificação por push etc.) é enviado para cada perfil
* As ações são executadas apenas uma vez
* A execução da jornada continua corretamente

Você pode verificar isso consultando o `ajo_message_feedback_event_dataset` ou verificando os logs de execução da ação. Você verá que apenas uma mensagem foi realmente enviada, apesar das entradas de evento de etapa de jornada duplicadas.

### Como posso identificar esses casos em minhas consultas?

Ao analisar os dados de Eventos de etapa do Jornada:

1. **Verifique o campo `_id`**: duplicatas reais no nível do sistema teriam o mesmo `_id`. Valores `_id` diferentes indicam entradas de log separadas do cenário de rebalanceamento descrito acima.

2. **Verificar entrega de mensagem**: cruzar referência com dados de feedback da mensagem para confirmar se apenas uma mensagem foi enviada:

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Agrupar por identificadores exclusivos**: ao contar execuções, use `_id` para obter contagens precisas:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### O que devo fazer se eu observar isso?

Este é um comportamento normal do sistema e **nenhuma ação é necessária**. O registro em log duplicado não indica um problema com a configuração da jornada ou com o delivery da mensagem.

Se você estiver criando relatórios ou análises com base nos Eventos de etapa do Jornada:

* Use `_id` como chave primária para contar eventos únicos
* Referência cruzada com conjuntos de dados de feedback de mensagem ao analisar a entrega de mensagens
* Esteja ciente de que a análise de tempo pode mostrar entradas agrupadas em poucos segundos

Para obter mais informações sobre a consulta de Eventos de Etapa de Jornada, consulte [Exemplos de consultas](../reports/query-examples.md).

## Solução de problemas de discrepâncias de métricas do painel {#dashboard-metrics}

Se as métricas exibidas no painel **Visão geral** não corresponderem ao número real de jornadas na guia **Procurar**, verifique o seguinte:

* Verifique se as jornadas em questão tiveram tráfego nas últimas 24 horas, pois as jornadas sem atividade recente são excluídas do painel.
* Verifique se você tem as permissões de acesso apropriadas para exibir todas as jornadas na organização.
* Aguarde até 30 minutos para que as métricas sejam atualizadas depois de fazer alterações nas jornadas.

Se as discrepâncias persistirem, [contate o Suporte da Adobe](../start/user-interface.md#support-ticket-guidelines) com as capturas de tela das guias Visão geral e Procurar para investigação.

## Parâmetros de rastreamento que mostram espaços reservados vazios em jornadas fechadas {#tracking-parameters-closed-journeys}

Se as URLs de rastreamento nos emails enviados contiverem espaços reservados vazios, como `cid=em-acou-adob{}`, isso pode indicar que um campo de contexto, como `context.system.source.actionId`, não pôde ser resolvido. Isso normalmente acontece quando uma jornada foi fechada e não foi republicada após uma alteração de produto relevante — somente jornadas republicadas preenchem corretamente esses campos de contexto em URLs de rastreamento.

Para resolver isso, publique novamente a jornada ([crie uma nova versão e publique-a](publish-journey.md#journey-create-new-version)) ou remova a referência ao campo de contexto afetado dos [parâmetros de rastreamento de URL](../email/url-tracking.md) na configuração de canal ou no conteúdo de email.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página é uma referência abrangente de solução de problemas para execução de jornada em tempo real no Adobe Journey Optimizer, cobrindo a entrega de eventos, falhas de entrada de perfil, problemas de transição de modo de teste, eventos descartados, logs de eventos de etapas duplicadas, verificações de entrega de mensagens e discrepâncias de métricas de painel.

**Intenções:**
* Diagnosticar por que os eventos não estão acionando a entrada de jornada verificando a estrutura de carga, os cabeçalhos e as condições de qualificação
* Verifique se os perfis estão entrando e avançando em uma jornada em tempo real ou em modo de teste
* Resolver falhas de transição do modo de teste causadas por datas de início futuras ou namespaces de identidade mal configurados
* Entender e manipular o motivo de descarte `maxInstanceStackEventsReached` para instâncias de jornada bloqueadas
* Identifique e consulte corretamente as entradas duplicadas do log de eventos de etapa de Jornada causadas pelo dimensionamento automático de back-end
* Investigue as mensagens ausentes verificando os relatórios do jornada e os resultados da chamada de ação personalizada
* Corrigir espaços reservados para URL de rastreamento vazios em emails de jornadas fechadas

**Glossário:**
* **Eventos de Etapa de Jornada**: um conjunto de dados que registra cada etapa que um perfil executa em uma jornada, usado para relatórios e depuração *(específico do produto)*
* **notSuitableInitialEvent**: um código de descarte indicando que um evento foi recebido, mas descartado porque a condição de qualificação não foi atendida *(específico do produto)*
* **maxInstanceStackEventsReached**: um código de descarte indicando o limite de 10 da pilha de eventos da instância de jornada por perfil foi excedido *(específico do produto)*
* **isValidTransition**: uma propriedade somente de interface do usuário nos detalhes técnicos da jornada; um valor nulo pode indicar uma data de início futura ou uma conexão de nó corrompida, mas não afeta o processamento de back-end *(específico do produto)*
* **Condição de qualificação**: uma regra definida em um evento que deve ser atendida para que o evento acione uma jornada; os eventos que falharem nessa condição serão descartados
* **Rebalanceamento**: Uma operação de dimensionamento automático de back-end nos microsserviços AJO que pode criar entradas de log de Eventos de Etapa de Jornada duplicadas com valores `_id` diferentes

**Medidas de Proteção:**
* Eventos enviados fora da janela de data/hora ativa da jornada são silenciosamente descartados sem mensagem de erro
* O limite de pilha de eventos de instância de jornada por perfil é de 10 eventos; se isso for excedido, os eventos serão descartados com `maxInstanceStackEventsReached`
* Entradas de Evento de Etapa de Jornada duplicadas com valores `_id` diferentes são comportamento esperado do sistema e não indicam duplicação de mensagem
* As métricas de Visão geral do painel incluem apenas jornadas com tráfego nas últimas 24 horas; as métricas podem levar até 30 minutos para serem atualizadas
* Jornadas fechadas que não foram republicadas após uma alteração de produto podem produzir espaços reservados vazios em URLs de rastreamento

**Terminologia:**
* Nome canônico: Eventos de etapa de Jornada — Acrônimo: none — variantes: eventos de etapa, logs de execução de jornada
* Nome canônico: Condição de qualificação — Acrônimo: none — variantes: regra de qualificação de evento, condição de evento
* Sinônimos: &quot;rebalanceamento&quot; = &quot;dimensionamento automático&quot; (operação de backend que causa entradas de log duplicadas)
* Não confunda: &quot;duplicate `_id`&quot; ≠ &quot;entradas de log duplicadas a partir de rebalanceamento&quot; — duplicatas verdadeiras compartilham o mesmo `_id`; rebalanceamento de duplicatas têm valores `_id` diferentes

**Perguntas frequentes:**
* **P: Por que meus eventos não estão acionando uma jornada mesmo que estejam sendo enviados com êxito?** — Verifique se a jornada está ativa ou em modo de teste, se a carga corresponde à estrutura do esquema do evento, se a condição de qualificação foi atendida e se os cabeçalhos corretos (`X-gw-ims-org-id`, `Content-type`) foram incluídos.
* **P: Por que os perfis de teste entram na jornada, mas não avançam além da primeira etapa?** — A causa mais comum é uma data de início de jornada definida no futuro; os eventos são silenciosamente descartados fora da janela de data ativa. Verifique também se o sinalizador de perfil de teste e o namespace de identidade correspondem.
* **P: O que `maxInstanceStackEventsReached` significa?** — O tempo de execução do jornada atingiu o limite interno de 10 eventos da pilha para uma instância de perfil específica, normalmente porque uma etapa de longa duração está bloqueando o processamento. Reduza longas esperas, desduplique eventos de upstream ou divida o cenário em várias jornadas.
* **P: Vejo linhas duplicadas em Eventos de Etapa de Jornada — há algo errado?** — Não. Entradas duplicadas com diferentes valores `_id` são esperadas e resultam do dimensionamento automático de back-end. Apenas uma mensagem é realmente enviada; verifique com o `ajo_message_feedback_event_dataset`.
* **P: Por que as URLs de rastreamento em emails mostram espaços reservados vazios como `cid=em-acou-adob{}`?** — A jornada foi fechada e não foi republicada após uma alteração de produto; os campos de contexto não podem ser resolvidos. Publique novamente a jornada ou remova a referência do campo de contexto afetado dos parâmetros de rastreamento de URL.
* **P: Por que o painel Visão geral mostra números diferentes da guia Procurar?** — o painel conta apenas jornadas com tráfego nas últimas 24 horas, as métricas levam até 30 minutos para serem atualizadas e as permissões de acesso podem limitar a visibilidade.

+++
