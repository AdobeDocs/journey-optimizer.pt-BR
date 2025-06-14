---
solution: Journey Optimizer
product: journey optimizer
title: Pausar uma jornada
description: Saiba como pausar e retomar uma jornada em tempo real
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilidade limitada" type="Informative"
keywords: publicar, jornada, ao vivo, validade, verificar
source-git-commit: 9d84a319497e833aa77416479dd019bab59aab55
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 0%

---

# Pausar uma jornada {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Pausar a jornada"
>abstract="Pausar uma jornada em tempo real para impedir a entrada de novos perfis. Escolha se deseja descartar os perfis que estão atualmente na jornada ou mantê-los no lugar. Se retidos, eles retomarão a execução na próxima atividade de ação depois que a jornada for reiniciada. Perfeito para atualizações ou interrupções de emergência sem perder o progresso."

Você pode pausar suas jornadas ativas, executar todas as alterações necessárias e retomá-las a qualquer momento.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Durante a pausa, você pode [aplicar filtros globais](#journey-global-filters) para excluir perfis com base em seus atributos. A jornada é retomada automaticamente no final do período de pausa. Você também pode [retomá-lo manualmente](#journey-resume-steps).

>[!AVAILABILITY]
>
>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.


## Principais benefícios {#journey-pause-benefits}

As jornadas de pausa e retomada oferecem aos profissionais de jornadas maior controle e flexibilidade, permitindo que as jornadas ativas sejam suspensas temporariamente sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.

Esse recurso reduz o risco de enviar mensagens não intencionais durante erros ou atualizações (por exemplo: alteração no conteúdo da mensagem), oferece suporte ao gerenciamento de jornadas mais seguro e aumenta a confiança do profissional. A visibilidade das jornadas pausadas e seu status diretamente na interface melhora ainda mais a transparência e a agilidade operacional.

>[!CAUTION]
>
>* As permissões para pausar e retomar jornadas estão restritas a usuários com a permissão de alto nível **[!DNL Publish journeys]**. Saiba mais sobre como gerenciar os direitos de acesso de [!DNL Journey Optimizer] usuários em [esta seção](../administration/permissions-overview.md).
>
>* Antes de começar a usar o recurso pausar/retomar, [leia as Medidas de Proteção e as Limitações](#journey-pause-guardrails).


## Como pausar uma jornada {#journey-pause-steps}

Você pode pausar qualquer jornada do **Live**.

Para pausar a jornada, siga estas etapas:

1. Abra a jornada que deseja pausar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Pausar**.

   ![Pausar o botão de jornada](assets/pause-journey-button.png){width="80%" align="left"}

1. Selecione como gerenciar os perfis que estão atualmente na jornada.

   ![Opções de pausa da jornada](assets/pause-confirm.png){width="50%" align="left"}

   É possível:

   * **Suspender** perfis - Os perfis aguardarão a jornada ser retomada
   * **Descartar** perfis - Os perfis serão excluídos da jornada no nó da próxima ação

1. Clique no botão **Pausar** para confirmar.

Na lista de suas jornadas, você pode pausar uma ou várias jornadas do **Live**. Para pausar um grupo de jornadas (_pausa em massa_), selecione-as na lista e clique no botão **Pausar** na barra azul na parte inferior da tela. O botão **Pausar** só estará disponível quando as jornadas do **Live** forem selecionadas.

![Pausar duas jornadas ativas em massa a partir da barra inferior](assets/bulk-pause-journeys.png)

### Comportamento em jornadas pausadas

Quando uma jornada é pausada, as entradas novas são sempre descartadas, independentemente do modo Manter/Descartar.

O gerenciamento de perfis quando uma jornada é pausada depende da atividade. Os comportamentos estão detalhados abaixo. Para obter uma compreensão completa, consulte também esta [Amostra completa](#journey-pause-sample).

| Atividade de Jornada | Gerenciamento de perfis |
|-------------------------|--------------------------------------------------|
| [Qualificação de público-alvo](audience-qualification-events.md) | No primeiro nó: Descartado <br> Em outros nós: Mesmo comportamento que em uma jornada em tempo real, no entanto, se a qualificação de público-alvo for após uma atividade <strong>Ação</strong> e o usuário estiver pausado nessa ação, a qualificação de público-alvo será descartada. |
| [Evento Unitário](general-events.md) | No primeiro nó: Descartado <br>Em outros nós: Mesmo comportamento de uma jornada em tempo real. No entanto, se o evento for após uma atividade <strong>Ação</strong> e o usuário estiver pausado nessa ação, o evento será descartado. |
| [Ler público-alvo](read-audience.md) | Mesmo comportamento de uma jornada em tempo real, com algumas especificidades:<br>1.  Se <strong>Pause</strong> foi pressionado após o início da atividade <strong>Read audience</strong>, os perfis que entraram na jornada continuarão (até a próxima atividade <strong>Action</strong>). À medida que o jornada lê os públicos-alvo em uma determinada velocidade, se o público-alvo completo ainda não tiver entrado, os perfis restantes na fila serão descartados.   <br>2. Para execuções únicas: não estamos mostrando nenhum erro no momento da retomada se a data programada for anterior à data da retomada. Esse cronograma seria ignorado. <br>3. Para jornadas incrementais: <br>- Se a pausa ocorrer antes da primeira ocorrência, no currículo o público-alvo completo será reproduzido. <br>- Se ocorrer uma pausa, por exemplo, no quarto dia de uma recorrência diária e a jornada permanecer pausada até o nono dia, todos os perfis que entraram do quarto ao nono dia serão incluídos |
| [Reação](reaction-events.md) | Mesmo comportamento de uma jornada em tempo real. No entanto, se a reação ocorrer após uma atividade <strong>Ação</strong> e o usuário estiver pausado nessa ação, o evento será descartado. |
| [Aguardar](wait-activity.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Condição](condition-activity.md) | Mesmo comportamento que em uma jornada em tempo real |
| Decisão de conteúdo | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Ação do canal](journeys-message.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Ação personalizada](../action/action.md) | Os perfis são estacionados ou descartados com base no que o usuário escolheu quando a jornada foi pausada |
| [Atualizar perfil](update-profiles.md) e [Pular](jump.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Source de Dados Externos](../datasource/external-data-sources.md) | Mesmo comportamento que em uma jornada em tempo real |
| [Critério de saída](journey-properties.md#exit-criteria) | Mesmo comportamento que em uma jornada em tempo real |

## Como retomar uma jornada pausada {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Retomar a jornada"
>abstract="Retome uma jornada pausada para permitir que novos perfis entrem novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar o jornada com segurança após atualizações ou pausas."

As jornadas pausadas são retomadas automaticamente no final do período máximo de pausa de 14 dias. Eles podem ser retomados manualmente a qualquer momento. Retomar uma jornada pausada permite que novos perfis sejam inseridos novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar o jornada com segurança após atualizações ou pausas.

Para retomar uma jornada pausada e começar a ouvir eventos de jornada novamente, siga estas etapas:

1. Abra a jornada que deseja retomar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Retomar**.

   A jornada alterna para o status **Retomando**. Quando a jornada for retomada, as novas entradas começarão em um minuto. A retomada dos perfis que foram mantidos pode levar algum tempo.  Como todos os perfis devem ser retomados para que a jornada seja **Ativa** novamente, a transição do status **Retomando** para **Ativa** pode levar algum tempo.

1. Clique no botão **Retomar** para confirmar.


Na lista de suas jornadas, você pode retomar uma ou várias jornadas **Pausadas**. Para retomar um grupo de jornadas (_retomada em massa_), selecione-as e clique no botão **Retomar**, localizado na barra azul na parte inferior da tela. Observe que o botão **Retomar** só estará disponível quando as jornadas **Pausadas** forem selecionadas.


## Aplicar um filtro global a perfis em uma jornada pausada {#journey-global-filters}

Quando uma jornada é pausada, você pode aplicar um filtro global com base em atributos de perfil. Esse filtro permite a exclusão de perfis que correspondem à expressão definida no momento da retomada. Depois que o filtro global é definido, ele é aplicado aos nós de ação, mesmo para a entrada de novos perfis. Os perfis que correspondem aos critérios e aos novos perfis que tentam entrar serão excluídos da jornada **no nó da próxima ação** que encontrarem.

Por exemplo, para excluir todos os clientes franceses de uma jornada pausada, siga estas etapas:

1. Navegue até a jornada pausada que você deseja modificar.

1. Clique no ícone **Critérios de saída e Filtro global**.

   ![Adicionar um filtro global a uma jornada pausada](assets/add-global-filter.png)

1. Nas configurações de **Critérios de saída e Filtro global**, clique em **Adicionar filtro global** para definir um filtro com base em atributos de perfil.

1. Defina a expressão para excluir perfis em que o atributo de país é igual a França.

   ![Adicionar um filtro global a uma jornada pausada](assets/add-country-filter.png)

1. Salve seu filtro e clique no botão **Atualizar jornada** para aplicar as alterações.

1. [Retomar a jornada](#journey-resume-steps).

   No momento da retomada, todos os perfis com o atributo de país definido como França serão automaticamente excluídos da jornada no nó da próxima ação. Qualquer novo perfil com o atributo de país definido como França ao tentar inserir a jornada será bloqueado no nó da próxima ação.

Esteja ciente de que as exclusões de perfil para perfis atualmente na jornada e para novos perfis só ocorrerão quando eles atingirem um nó de ação.

>[!CAUTION]
>
>* Você só pode definir **um** filtro global por jornada.
>
>* Você só pode criar, atualizar ou excluir um filtro global em **jornadas** em pausa.

## Medidas de proteção e limitações {#journey-pause-guardrails}

* Uma versão do jornada pode ser pausada por no máximo 14 dias.
* As jornadas pausadas são consideradas em todas as regras de negócios, da mesma forma como se estivessem ativas.
* Os perfis são &quot;descartados&quot; em uma jornada pausada quando atingem uma atividade de ação. Se eles permanecerem em espera durante o tempo em que uma jornada é pausada e saírem dessa espera depois que ela for retomada, eles continuarão a jornada e não serão descartados.
* Mesmo após a pausa, como os eventos continuam a ser processados, esses eventos são contados para o número de Eventos de Jornada por segundo de cota após o qual a limitação é considerada unitária.
* Os perfis que entraram na jornada, mas foram descartados durante a pausa, ainda seriam contados como perfis ativáveis.
* Quando os perfis são mantidos em uma jornada pausada, no momento da retomada, os atributos do perfil são atualizados
* As condições ainda são executadas em jornadas pausadas, portanto, se uma jornada tiver sido pausada devido a problemas de qualidade de dados, qualquer condição anterior a um nó de ação poderá ser avaliada com dados errados.
* Para uma jornada de público-alvo de leitura incremental com base no público-alvo, a duração pausada é levada em consideração. Por exemplo, para uma jornada diária, se ela foi pausada no dia 2 e retomada no dia 5 do mês, a execução no dia 6 levará todos os perfis que se qualificaram do dia 1 ao dia 6. Esse não é o caso para qualificação de público-alvo ou jornadas baseadas em eventos (se uma qualificação de público-alvo ou um evento for recebido durante uma pausa, esses eventos serão descartados).
* As jornadas pausadas são contadas em relação à cota de jornada ativa.
* O tempo limite global de Jornada ainda se aplica a jornadas pausadas. Por exemplo, se um perfil esteve em uma jornada por 90 dias e a jornada estiver pausada, esse perfil ainda sairá da jornada no 91º dia.
* Se os perfis forem mantidos em uma jornada jornada e ela for retomada automaticamente após alguns dias, os perfis continuarão a jornada e não serão descartados. Se quiser soltá-los, você deve parar a jornada.
* Em jornadas pausadas, os alertas não são acionados para alertas de segmentos em lote.
* Não há logs de auditoria no sistema quando o estado de pausa de 14 dias da jornada é encerrado.
* Alguns perfis descartados podem estar visíveis no Evento de etapa do Jornada, mas não podem estar visíveis nos relatórios. Por exemplo: Descartar eventos comerciais para Público-alvo de leitura, trabalhos de Público-alvo de leitura sendo descartados devido à jornada pausada, eventos descartados quando a atividade do evento estava após uma ação em que o perfil estava aguardando.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Amostra completa {#journey-pause-sample}

Vamos ver o exemplo da jornada abaixo:

![Amostra de uma jornada](assets/pause-journey-sample.png)

Ao pausar esta jornada, você seleciona se os perfis estão **Descartados** ou **Suspensos** e, em seguida, o gerenciamento de perfis é o seguinte:

1. Atividade **AddToCart**: todas as novas entradas de perfis estão bloqueadas. Se um perfil já tiver entrado na jornada antes de uma pausa, ele continuará até o nó da próxima ação.
1. Atividade **Wait**: os perfis continuam a aguardar normalmente no nó e vão sair dele, mesmo se a jornada estiver em pausa.
1. **Condição**: os perfis continuam a passar pelas condições e a mover para a ramificação direita com base na expressão definida na condição.
1. Atividades de **Push**/**Email**: durante uma jornada pausada, os perfis começam a aguardar ou são descartados (com base na escolha feita pelo usuário no momento da pausa) no nó da próxima ação. Os perfis começarão a aguardar ou serão descartados lá.
1. **Eventos** após os nós de ação: se um perfil estiver aguardando um nó de ação e houver um evento após ele, se esse evento for acionado, o perfil será descartado.

De acordo com esse comportamento, é possível ver o aumento dos números de perfil na jornada pausada, principalmente em atividades antes de Ações. Por exemplo, nesse exemplo, a variável Wait é ignorada, aumentando o número de perfis que passam pela atividade Condition.

Ao retomar esta jornada:

1. As novas entradas de jornada começam em um minuto
1. Os perfis que estavam aguardando atualmente nas atividades jornada on Action são retomados a uma taxa de 5 mil tps. Em seguida, eles entrarão na Ação que estavam esperando e continuarão a jornada.
