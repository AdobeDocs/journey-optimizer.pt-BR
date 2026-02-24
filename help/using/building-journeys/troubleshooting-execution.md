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
source-git-commit: 63fb247449dfb989b191254ec6d117a403edd29d
workflow-type: tm+mt
source-wordcount: '1938'
ht-degree: 13%

---

# Solucionar problemas de execução de jornada em tempo real {#troubleshooting-execution}

Nesta seção, saiba como solucionar problemas de eventos de jornada, verificar se os perfis inseriram sua jornada, como eles navegam por ela e se as mensagens são enviadas.

Você também pode solucionar problemas de erros antes de testar ou publicar uma jornada. Saiba mais sobre [nesta página](troubleshooting.md).

Se você estiver usando ações de entrada, saiba como solucionar problemas deles [nesta página](troubleshooting-inbound.md).

## Verifique se os eventos foram enviados corretamente {#checking-that-events-are-properly-sent}

O ponto de partida de uma jornada é sempre um evento. Você pode fazer testes usando ferramentas como o Postman.

Você pode verificar se a chamada à API enviada por meio dessas ferramentas foi corretamente enviada. Se ocorrer um erro, significa que a chamada tem um problema. Verifique novamente o payload, o cabeçalho (e principalmente a ID da organização) e o URL de destino. Você pode perguntar ao administrador qual é o URL correto para a ocorrência.

Eventos não são levados diretamente da origem para jornadas. Na verdade, o jornada depende das APIs de assimilação de streaming de [!DNL Adobe Experience Platform]. Como resultado, no caso de problemas relacionados ao evento, consulte a [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=pt-BR){target="_blank"} para obter a solução de problemas de APIs de assimilação de streaming.

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

&#x200B;>>
**Para jornadas de qualificação de público-alvo com públicos-alvo de streaming**: se estiver usando uma atividade de qualificação de público-alvo como ponto de entrada de jornada, esteja ciente de que nem todos os perfis qualificados para o público-alvo necessariamente entrarão na jornada devido a fatores de tempo, saídas rápidas do público-alvo ou se os perfis já estiverem no público-alvo antes da publicação. Saiba mais sobre [considerações de tempo de qualificação de público de streaming](audience-qualification-events.md#streaming-entry-caveats).

### Verificar identidade do evento {#verify-event-identity-and-rule-data-types}

Ao configurar uma jornada baseada em eventos, confirme se o campo de identidade da carga corresponde ao [namespace selecionado no evento](../event/about-creating.md#select-the-namespace). Se o evento incluir campos para correspondência de perfil, verifique se a **letra maiúscula** e o **tipo de dados** na condição do evento correspondem exatamente aos dados de entrada. Por exemplo, se o esquema de evento definir `roStatus` como uma cadeia de caracteres, a regra de jornada também deverá avaliá-la como uma cadeia de caracteres. Tipos de dados incompatíveis (por exemplo, sequência de caracteres vs. número inteiro) fazem com que a avaliação da regra falhe e eventos válidos sejam descartados. Da mesma forma, se o evento tiver uma **condição de qualificação** (por exemplo, um campo não deve estar vazio), os eventos que não satisfizerem essa condição serão **descartados** e não acionarão a jornada; os logs poderão mostrar códigos de descarte como `notSuitableInitialEvent`.

Para validar a condição do evento em [!DNL Journey Optimizer], use a pré-visualização de carga na configuração do evento e verifique se os tipos e valores na regra correspondem à estrutura de carga. Saiba como [visualizar a carga](../event/about-creating.md#preview-the-payload) e [configurar eventos baseados em regras](../event/about-creating.md).

## Solução de problemas de transições do modo de teste {#troubleshooting-test-transitions}

Se os perfis de teste não avançarem na jornada no modo de teste ou o fluxo visual não exibir setas verdes indicando a progressão da etapa, o problema pode estar relacionado à validação da transição. Esta seção fornece orientação sobre como diagnosticar e resolver problemas comuns de modo de teste.

### Os perfis de teste não estão progredindo

Se os perfis de teste entrarem na jornada, mas não avançarem além da etapa inicial, verifique o seguinte:

* **Data de início da Jornada** - A causa mais comum é quando a data de início da jornada é definida no futuro. Os perfis de teste são descartados imediatamente se a hora atual estiver fora da janela [datas/hora de início e término](journey-properties.md#dates) configurada da jornada. Para resolver:
   * Verificar se a data de início da jornada não está definida no futuro
   * Garantir que a hora atual esteja na janela de datas ativa da jornada
   * Se necessário, atualize as propriedades da jornada para ajustar a data de início

* **Configuração do perfil de teste** - Confirme se o perfil está sinalizado corretamente como um perfil de teste em [!DNL Adobe Experience Platform]. Consulte [como criar perfis de teste](../audience/creating-test-profiles.md) para obter mais informações.

* **Namespace de identidade** - Verifique se o namespace de identidade usado na configuração do evento corresponde ao namespace do seu perfil de teste.

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
>Lembre-se de que os eventos enviados fora da janela de data ativa da jornada são descartados silenciosamente sem mensagem de erro. Sempre verifique a configuração de tempo da jornada primeiro ao solucionar problemas de progressão do perfil de teste.

## Verificar como as pessoas navegam pela jornada {#checking-how-people-navigate-through-the-journey}

O relatório de jornada mede o progresso das pessoas físicas dentro de uma jornada. É fácil identificar onde e por que uma pessoa foi parada.

Veja algumas coisas que devem ser verificadas:

* A interrupção se deve a uma condição que exclui a pessoa? Por exemplo, a condição é &quot;gênero = homem&quot; e a pessoa é uma mulher. Essa verificação pode ser feita por um usuário empresarial se a condição não for muito complexa.
* A interrupção se deve a uma chamada a uma fonte de dados que não está respondendo? Quando a jornada está em teste, essas informações podem ser vistas nos registros do modo de teste. Quando a jornada é em tempo real, um administrador pode testar chamadas diretas para a fonte de dados e verificar a resposta recebida. Um administrador também pode duplicar a jornada e testá-la.

## Verificar se as mensagens foram enviadas com êxito {#checking-that-messages-are-sent-successfully}

Se as pessoas físicas continuarem percorrendo o caminho certo na jornada, mas não receberem as mensagens esperadas, você poderá verificar se:

* [!DNL Journey Optimizer] levou em consideração corretamente a solicitação para enviar a mensagem. Os usuários empresariais podem acessar a mensagem que deve ser enviada e verificar se a hora da execução mais recente corresponde ao tempo de execução da sua jornada. Eles também podem verificar as chamadas/eventos de API mais recentes recebidos.
* [!DNL Journey Optimizer] enviou a mensagem com êxito. Verifique os relatórios do jornada para garantir que não haja erros.

No caso de uma mensagem enviada por meio de uma ação personalizada, a única coisa que pode ser verificada durante o teste de jornada é o fato de a chamada do sistema da ação personalizada causar ou não um erro. Se a chamada para o sistema externo associada à ação personalizada não causar um erro, mas não enviar a mensagem, algumas investigações devem ser feitas por parte do sistema externo.

## Noções básicas sobre entradas duplicadas em Eventos de etapa de Jornada {#duplicate-step-events}

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

**Não.** O impacto está limitado apenas ao registro em log. [!DNL Adobe Journey Optimizer] tem mecanismos de desduplicação internos na camada de execução da mensagem que garantem:

* Somente uma mensagem (email, SMS, notificação por push etc.) é enviada para cada perfil
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
