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
source-git-commit: 8dae895f33d8e95424bc96c8050b8f52d7c02b50
workflow-type: tm+mt
source-wordcount: '1199'
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


## Principais benefícios {#journey-dry-run-benefits}

As jornadas de pausa e retomada oferecem aos profissionais de jornadas maior controle e flexibilidade, permitindo que as jornadas ativas sejam suspensas temporariamente sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.

Esse recurso reduz o risco de enviar mensagens não intencionais durante erros ou atualizações (por exemplo: alteração no conteúdo da mensagem), oferece suporte ao gerenciamento de jornadas mais seguro e aumenta a confiança do profissional. A visibilidade das jornadas pausadas e seu status diretamente na interface melhora ainda mais a transparência e a agilidade operacional.

>[!CAUTION]
>
>As permissões para pausar e retomar jornadas estão restritas a usuários com a permissão de alto nível **[!DNL Publish journeys]**. Saiba mais sobre como gerenciar os direitos de acesso de [!DNL Journey Optimizer] usuários em [esta seção](../administration/permissions-overview.md).

## Medidas de proteção e recomendações

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
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

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

![Pausar duas jornadas ativas em massa a partir da barra inferior](assets/bulk-pause-journeys.png){width="80%" align="left"}


## Como retomar uma jornada pausada {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Retomar a jornada"
>abstract="Retome uma jornada pausada para permitir que novos perfis entrem novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar o jornada com segurança após atualizações ou pausas."

As jornadas pausadas são retomadas automaticamente no final do período máximo de pausa de 14 dias. Eles podem ser retomados manualmente a qualquer momento. Retomar uma jornada pausada permite que novos perfis sejam inseridos novamente. Se os perfis estavam aguardando durante a pausa, eles continuarão sua jornada. Ideal para reiniciar o jornada com segurança após atualizações ou pausas.

Para retomar uma jornada pausada e começar a ouvir eventos de jornada novamente, siga estas etapas:

1. Abra a jornada que deseja retomar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Retomar**.

   A jornada alterna para o status **Retomando**. A transição do status **Retomando** para **Ao Vivo** pode levar algum tempo: todos os perfis precisam ser retomados para que a jornada seja **Ao Vivo** novamente.

1. Clique no botão **Retomar** para confirmar.


Na lista de suas jornadas, você pode retomar uma ou várias jornadas **Pausadas**. Para retomar um grupo de jornadas (_retomada em massa_), selecione-as e clique no botão **Retomar**, localizado na barra azul na parte inferior da tela. Observe que o botão **Retomar** só estará disponível quando as jornadas **Pausadas** forem selecionadas.


## Aplicar um filtro global a perfis em uma jornada pausada  {#journey-global-filters}

Quando uma jornada é pausada, você pode aplicar um filtro global com base em atributos de perfil. Esse filtro permite a exclusão de perfis que correspondem à expressão definida no momento da retomada. Os perfis que correspondem aos critérios atualmente na jornada serão fechados, e os novos perfis que tentarem entrar serão bloqueados.

Por exemplo, para excluir todos os clientes franceses das comunicações de marketing para a França, siga estas etapas:

1. Navegue até a jornada pausada que você deseja modificar.

1. Clique no ícone **Critérios de saída e Filtro global**.

   ![Adicionar um filtro global a uma jornada pausada](assets/add-global-filter.png){width="50%" align="left"}

1. Nas configurações de **Critérios de saída e Filtro global**, defina um filtro com base em atributos de perfil.

1. Defina a expressão para excluir perfis em que o atributo de país é igual a França.

   ![Adicionar um filtro global a uma jornada pausada](assets/add-country-filter.png){width="50%" align="left"}

1. Salve seu filtro e clique no botão **Atualizar jornada** para aplicar as alterações.

1. [Retomar a jornada](#journey-resume-steps).

   No momento da retomada, todos os perfis com o atributo de país definido como França serão excluídos automaticamente da jornada. Qualquer novo perfil com o atributo de país definido como França tentando inserir a jornada será bloqueado.

Esteja ciente de que as exclusões de perfil para perfis atualmente na jornada e para novos perfis só ocorrerão quando eles atingirem um nó de ação.

>[!CAUTION]
>
>* Você só pode definir **um** filtro global por jornada.
>
>* Você só pode criar, atualizar ou excluir um filtro global em **jornadas** em pausa.