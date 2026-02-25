---
solution: Journey Optimizer
product: journey optimizer
title: Pausar uma jornada
description: Saiba como pausar e retomar uma jornada em tempo real
feature: Journeys
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: a2892f0a-5407-497c-97af-927de81055ac
version: Journey Orchestration
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '2512'
ht-degree: 5%

---

# Pausar uma jornada {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Pausar sua jornada"
>abstract="Pause uma jornada em tempo real para impedir a entrada de novos perfis. Escolha se deseja descartar os perfis que estão atualmente na jornada ou mantê-los no lugar. Se retidos, eles retomarão a execução na próxima atividade de ação depois que a jornada for reiniciada. Perfeito para atualizações ou interrupções de emergência sem perder o progresso."

Você pode pausar suas jornadas ativas, executar todas as alterações necessárias e retomá-las a qualquer momento.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Durante a pausa, você pode [aplicar os critérios de saída do atributo de perfil](#journey-exit-criteria) para excluir perfis com base em seus atributos. A jornada é retomada automaticamente no final do período de pausa. Você também pode [retomá-lo manualmente](#journey-resume-steps).

## Principais benefícios {#journey-pause-benefits}

As jornadas de pausa e retomada oferecem aos profissionais de jornadas maior controle e flexibilidade, permitindo que as jornadas ativas sejam suspensas temporariamente sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.

Esse recurso reduz o risco de enviar mensagens não intencionais durante erros ou atualizações (por exemplo: alteração no conteúdo da mensagem), oferece suporte ao gerenciamento de jornadas mais seguro e aumenta a confiança do profissional. A visibilidade das jornadas pausadas e seu status diretamente na interface melhora ainda mais a transparência e a agilidade operacional.

>[!CAUTION]
>
>* As permissões para pausar e retomar jornadas estão restritas a usuários com a permissão de alto nível **[!DNL Publish journeys]**. Saiba mais sobre como gerenciar os direitos de acesso de [!DNL Journey Optimizer] usuários em [esta seção](../administration/permissions-overview.md).
>
>* Antes de começar a usar o recurso pausar/retomar, [leia as Medidas de Proteção e as limitações](#journey-pause-guardrails).


## Como pausar uma jornada {#journey-pause-steps}

Você pode pausar qualquer jornada do **Live**.

Para pausar a jornada, siga estas etapas:

1. Abra a jornada que deseja pausar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Pausar**.

   ![Pausar o botão de jornada](assets/pause-journey-button.png)

1. Selecione como gerenciar os perfis que estão atualmente na jornada.

   ![Opções de pausa da jornada](assets/pause-confirm.png){width="50%" align="left"}

   É possível:

   * **Reter** perfis - Os perfis aguardarão no próximo nó **Ação** para que a jornada seja retomada
   * **Descartar** perfis - Os perfis serão excluídos da jornada no próximo nó **Ação**

   Quando você pausa uma jornada, presume-se que planeja retomá-la em algum momento. No entanto, uma jornada não pode permanecer pausada indefinidamente. Para evitar isso, você pode definir por quanto tempo a jornada deve permanecer pausada (entre 1 e 14 dias). Após o número selecionado de dias, a jornada é retomada automaticamente.

1. Clique no botão **Pausar** para confirmar.

O número máximo de perfis que podem ser mantidos em jornadas pausadas para sua Organização está visível no inventário de jornadas. Ela só é visível quando pelo menos uma jornada está pausada. Esse indicador também mostra o número total de jornadas pausadas. Ele é atualizado a cada 30 minutos. Saiba mais em [Medidas de proteção e limitações](#guardrails-and-limitations).

![Número de jornadas e perfis pausados no momento](assets/profiles-in-paused-journeys.png){width="50%" align="left"}

Na lista de suas jornadas, você pode pausar uma ou várias jornadas do **Live**. Para pausar um grupo de jornadas (_pausa em massa_), selecione-as na lista e clique no botão **Pausar** na barra azul na parte inferior da tela. O botão **Pausar** só estará disponível quando as jornadas do **Live** forem selecionadas.

![Pausar duas jornadas ativas em massa a partir da barra inferior](assets/bulk-pause-journeys.png)

## Lógica de execução do jornada pausada {#journey-pause-exec}

Quando uma jornada é pausada, as entradas novas são sempre descartadas, independentemente do modo Manter/Descartar.

Quando uma jornada é pausada, o gerenciamento de perfil e a execução da atividade dependem dessa atividade. Os comportamentos estão detalhados abaixo. Para obter uma compreensão completa, consulte também esta [Amostra completa](#journey-pause-sample).


| Atividade de Jornada | Quando a jornada está em pausa |
|-------------------------|--------------------------------------------------|
| [Qualificação de público-alvo](audience-qualification-events.md) | <ul> <li>No primeiro nó da tela: qualquer qualificação de perfil para o público-alvo é descartada </li><li>Em outros nós: Mesmo comportamento de uma jornada em tempo real. No entanto, se a qualificação de público-alvo for após uma atividade de <strong>Ação</strong> e o usuário estiver pausado nessa ação, a qualificação de público-alvo será descartada. </li></ul> |
| [Evento Unitário](general-events.md) | <ul> <li>No primeiro nó da tela: o evento é descartado</li><li>Em outros nós: Mesmo comportamento de uma jornada em tempo real. No entanto, se o evento ocorrer após uma atividade <strong>Ação</strong> e o usuário estiver pausado nessa ação, o evento será descartado. </li></ul> |
| [Ler público-alvo](read-audience.md) | Mesmo comportamento que em uma jornada em tempo real, com algumas especificidades: <ol> <li> Se <strong>Pause</strong> foi pressionado após o início da atividade <strong>Read audience</strong>, os perfis que entraram na jornada continuarão (até a próxima atividade <strong>Action</strong>). À medida que o jornada lê os públicos-alvo em uma determinada velocidade, se o público-alvo completo ainda não tiver entrado, os perfis restantes na fila serão descartados.</li><li> Para execuções únicas: nenhum erro será exibido na hora de retomada se a data programada for anterior à data de retomada. Esse cronograma seria ignorado.</li><li>Para jornadas incrementais: <ul><li>Se a pausa ocorrer antes da primeira ocorrência, o público-alvo completo será reproduzido ao retomar. </li><li>Se ocorrer uma pausa, por exemplo, no quarto dia de uma recorrência diária e a jornada permanecer pausada até o nono dia, todos os perfis que entraram do quarto ao nono dia serão incluídos no currículo  </li></ul></ol> |
| [Reação](reaction-events.md) | Mesmo comportamento de uma jornada em tempo real. No entanto, se a reação ocorrer após uma atividade <strong>Ação</strong> e o usuário estiver pausado nessa ação, o evento de reação será descartado. |
| [Aguardar](wait-activity.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Condição](condition-activity.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Decisão de conteúdo](content-decision.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Ação do canal](journey-action.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Ação personalizada](../action/action.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Atualizar perfil](update-profiles.md) e [Pular](jump.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Source de Dados Externos](../datasource/external-data-sources.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Critério de saída](journey-properties.md#exit-criteria) | Mesmo comportamento que em uma jornada em tempo real |


Saiba como solucionar problemas de descartes em [esta seção](#discards-troubleshoot).

## Como retomar uma jornada pausada {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Retomar sua jornada"
>abstract="Retome uma jornada pausada para permitir que novos perfis entrem novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar as jornadas com segurança após atualizações ou pausas."

As jornadas pausadas são retomadas automaticamente no final do período máximo de pausa de 14 dias. Eles podem ser retomados manualmente a qualquer momento. Retomar uma jornada pausada permite que novos perfis sejam inseridos novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar as jornadas com segurança após atualizações ou pausas.

Para retomar uma jornada pausada e começar a ouvir eventos de jornada novamente, siga estas etapas:

1. Abra a jornada que deseja retomar.
1. Selecione o botão **...Mais** na seção superior direita da tela de jornada e depois **Retomar**.

   A jornada alterna para o status **Retomando**. Quando a jornada for retomada, as novas entradas começarão em um minuto. A retomada dos perfis que foram mantidos pode levar algum tempo - os perfis são retomados a uma taxa de 5 mil tps.  Como todos os perfis devem ser retomados para que a jornada seja **Ativa** novamente, a transição do status **Retomando** para **Ativa** pode levar algum tempo.

1. Clique no botão **Retomar** para confirmar.


Na lista de suas jornadas, você pode retomar uma ou várias jornadas **Pausadas**. Para retomar um grupo de jornadas (_retomada em massa_), selecione-as e clique no botão **Retomar**, localizado na barra azul na parte inferior da tela. Observe que o botão **Retomar** só estará disponível quando as jornadas **Pausadas** forem selecionadas.


## Aplicar um critério de saída em uma jornada pausada {#journey-exit-criteria}

Quando uma jornada é pausada, você pode aplicar um critério de saída com base nos atributos do perfil. Esse filtro permite a exclusão de perfis que correspondem à expressão definida no momento da retomada. Depois que os critérios de saída baseados em atributo de perfil forem definidos, eles serão aplicados nos nós de ação, mesmo para a entrada de novos perfis. Os perfis existentes que correspondem aos critérios e os novos perfis que entram na jornada serão excluídos da jornada **no próximo nó de ação** que encontrarem.

Por exemplo, para excluir todos os clientes franceses de uma jornada pausada, siga estas etapas:

1. Navegue até a jornada pausada que você deseja modificar.

1. Selecione o ícone **Critérios de saída**.

   ![Adicionar um critério de saída de atributo de perfil a uma jornada pausada](assets/add-exit-criteria.png)

1. Nas configurações de **Critério de saída**, clique em **Adicionar critério de saída** para definir um filtro com base em atributos de perfil.

1. Defina a expressão para excluir perfis em que o atributo de país é igual a França.

   ![Adicionar um critério de saída de atributo de perfil a uma jornada pausada](assets/add-country-filter.png)

1. Salve seu filtro e clique no botão **Atualizar jornada** para aplicar as alterações.

1. [Retomar a jornada](#journey-resume-steps).

   No momento da retomada, todos os perfis com o atributo de país definido como França serão automaticamente excluídos da jornada no nó da próxima ação. Quaisquer novos perfis com o atributo de país definido como França, ao tentar inserir a jornada, também serão bloqueados no nó da próxima ação.

Esteja ciente de que as exclusões de perfil para perfis atualmente na jornada e para novos perfis só ocorrerão **quando eles atingirem um nó de ação**.

>[!CAUTION]
>
>* Você só pode definir **um** critérios de saída baseados em atributo de perfil por jornada.
>
>* Você só pode criar, atualizar ou excluir um critério de saída baseado em atributo de perfil nas jornadas **Pausadas**.
>
>* Saiba mais sobre os critérios de saída baseados em Atributo de perfil [nesta seção](journey-properties.md#profile-exit-criteria).

## Medidas de proteção e limitações {#journey-pause-guardrails}

* Uma versão do jornada pode ser pausada por até **14 dias**, com um máximo de **10 milhões de perfis** permitidos em jornadas pausadas em sua organização.
Esse limite conta o número total de perfis mantidos em todas as jornadas pausadas, não perfis distintos. Por exemplo, se os mesmos perfis 5M forem mantidos em duas jornadas pausadas, o limite de 10M será atingido.
Esse limite é verificado a cada 30 minutos. Isso significa que você pode exceder temporariamente o limite de 10 milhões, mas assim que o sistema detectá-lo, quaisquer perfis adicionais serão automaticamente descartados.

  Se você retomar as jornadas para retornar o número de perfis retidos para o limite, a jornada será retomada imediatamente, mas pode levar até 30 minutos para que a contagem de perfis seja atualizada. Durante esse tempo, o sistema ainda poderá considerar esses perfis como pausados.

* Para jornadas que incluem [atividades de entrada](../channels/gs-channels.md#inbound-channels) (por exemplo, no aplicativo, na Web etc.), pausar a jornada não interrompe as comunicações que já foram acionadas. Se um perfil tiver se qualificado para uma atividade de entrada antes da pausa, a mensagem correspondente ainda será entregue. Para interromper completamente todas as comunicações de entrada, você deve interromper a jornada.
* As jornadas pausadas são contadas para a cota de jornada ativa
* Os perfis que tinham entrado na jornada, mas foram descartados durante a pausa, ainda seriam contados como perfis ativáveis
* As jornadas pausadas são consideradas em todas as regras de negócios, da mesma forma como se estivessem ativas
* O tempo limite global de Jornada ainda se aplica a jornadas pausadas. Por exemplo, se um perfil esteve em uma jornada por 90 dias e a jornada estiver pausada, esse perfil ainda sairá da jornada no 91º dia
* Os perfis são **descartados** em uma jornada pausada quando atingem uma atividade de ação. Se eles permanecerem em espera durante o tempo em que uma jornada é pausada e saírem dessa espera depois que ela for retomada, eles continuarão a jornada e não serão descartados. [Consulte a amostra completa](#journey-pause-sample)
* Mesmo após a pausa, como os eventos continuam a ser processados, esses eventos são contados para o número de Eventos de Jornada por segundo de cota após o qual a limitação é considerada unitária
* Quando os perfis são mantidos em uma jornada pausada, no momento da retomada, os atributos do perfil são atualizados
* As condições ainda são executadas em jornadas pausadas, portanto, se uma jornada tiver sido pausada devido a problemas de qualidade de dados, qualquer condição anterior a um nó de ação poderá ser avaliada com dados errados
* Para jornadas de **Leitura de público** baseadas em público incremental, a duração pausada é levada em consideração. Esse não é o caso para qualificação de público ou jornadas baseadas em eventos (se uma qualificação de público ou um evento for recebido durante uma pausa e for a primeira atividade na jornada, esses eventos serão descartados)
* Se os perfis forem mantidos em uma jornada jornada e ela for retomada automaticamente após alguns dias, os perfis continuarão a jornada e não serão descartados. Se quiser soltá-los, você deve interromper a jornada
* No jornada pausado, os alertas não são acionados para [alertas de segmento em lote](../reports/alerts.md#alert-read-audiences)
* Não há logs de auditoria no sistema quando o estado de pausa de 14 dias da jornada é encerrado
* Alguns perfis descartados podem estar visíveis no Evento de etapa do Jornada, mas não podem estar visíveis nos relatórios. Por exemplo:
   * Descartar eventos comerciais para **Ler público**
   * **Ler público-alvo** trabalhos sendo ignorados devido à jornada pausada
   * Eventos descartados quando a atividade **Event** era posterior a uma ação em que o perfil estava aguardando



## Amostra completa {#journey-pause-sample}

Vamos ver o exemplo da jornada abaixo:

![Amostra de uma jornada](assets/pause-journey-sample.png){zoomable="yes"}

Ao pausar esta jornada, você seleciona se os perfis estão **Descartados** ou **Suspensos**. Em seguida, o gerenciamento de perfis é o seguinte:

1. Atividade **AddToCart**: todas as novas entradas de perfis estão bloqueadas. Se um perfil já tiver entrado na jornada antes de uma pausa, ele continuará até o nó da próxima ação.
1. Atividade **Wait**: os perfis continuam a aguardar normalmente no nó e vão sair dele, mesmo se a jornada estiver em pausa.
1. **Condição**: os perfis continuam a passar pelas condições e a mover para a ramificação direita com base na expressão definida na condição.
1. Atividades de **Push**/**Email**: durante uma jornada pausada, os perfis começam a aguardar ou são descartados (com base na escolha feita pelo usuário no momento da pausa) no nó da próxima ação. Os perfis começarão a aguardar ou serão descartados lá.
1. **Eventos** após nós de **Ação**: se um perfil estiver aguardando um nó de **Ação** e houver uma atividade de **Evento** após ele, se esse evento for acionado, o evento será descartado.

De acordo com esse comportamento, você pode ver números de perfil aumentando em jornadas pausadas, principalmente em atividades antes de **Ações**. Por exemplo, nesse exemplo, a atividade **Wait** ainda está habilitada, aumentando o número de perfis que passam pela atividade **Condition**, à medida que eles saem dela.

Ao retomar esta jornada:

1. As novas entradas de jornada começam em um minuto.
1. Os perfis que estavam aguardando na jornada em **Atividades de ação** são retomados a uma taxa de 5 mil tps. Eles podem inserir a **Ação** que estavam esperando e continuar a jornada.

## Solução de problemas de descartes de perfis em jornadas pausadas {#discards-troubleshoot}

Você pode usar o [[!DNL Adobe Experience Platform] Serviço de consulta](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=pt-BR){target="_blank"} para consultar eventos de etapa, que podem fornecer mais informações sobre descartes de perfil, dependendo de quando eles ocorreram.

* Para descartes que ocorrem antes que o perfil entre na jornada, use o seguinte código:

  ```sql
  SELECT
  TIMESTAMP,
  _experience.journeyOrchestration.profile.ID,
  to_json(_experience.journeyOrchestration)
  FROM
  journey_step_events
  WHERE
  _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'PAUSED_JOURNEY_VERSION'
  AND _experience.journeyOrchestration.journey.versionID=<jvId>  
  ```

  Isso listará as descartes que ocorreram no ponto de entrada da jornada:

   1. Quando uma jornada de público-alvo está em execução e o primeiro nó ainda está em processamento, se a jornada estiver pausada, todos os perfis não processados serão descartados.

   1. Quando um novo evento unitário chega ao nó de início (para acionar uma entrada) enquanto a jornada está pausada, o evento é descartado.

* Para que os descartes ocorram quando o perfil já estiver na jornada, use o seguinte código:

  ```sql
  SELECT
  TIMESTAMP,
  _experience.journeyOrchestration.profile.ID,
  to_json(_experience.journeyOrchestration)
  FROM
  journey_step_events
  WHERE
  _experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'JOURNEY_IN_PAUSED_STATE'
  AND _experience.journeyOrchestration.journey.versionID=<jvId> 
  ```

  Esse comando lista as descartes que ocorrem quando perfis estão em uma jornada:

   1. Se a jornada estiver pausada com a opção de descarte ativada e um perfil já tiver sido inserido antes da pausa, esse perfil será descartado quando atingir o nó da próxima ação.

   1. Se a jornada foi pausada com a opção de suspensão selecionada, mas os perfis foram descartados porque excederam a cota de 10 milhões, esses perfis ainda serão descartados quando atingirem o próximo nó de ação.



