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
source-git-commit: bb881f0257408ad70f3737c24d1caa28deea96e0
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---

# Pausar uma jornada {#journey-pause}

Você pode pausar suas jornadas ativas, executar todas as alterações necessárias e retomá-las a qualquer momento. <!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> A jornada é automaticamente retomada no final do período de pausa. Você também pode [retomá-lo manualmente](#journey-resume-steps).


>[!AVAILABILITY]
>
>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.


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

Você pode pausar qualquer jornada ativa.

Para pausar a jornada, siga estas etapas:

1. Abra a jornada que deseja pausar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Pausar**.

   ![Pausar o botão de jornada](assets/pause-journey-button.png)

1. Selecione como gerenciar os perfis que estão atualmente na jornada.

   ![Opções de pausa da jornada](assets/pause-confirm.png){width="50%" align="left"}

   É possível:

   * Perfis em espera - Os perfis aguardarão a retomada da jornada
   * Descartar perfis - os perfis serão excluídos da jornada no nó da próxima ação

1. Clique no botão **Pausar** para confirmar.

## Como retomar uma jornada pausada {#journey-resume-steps}

As jornadas pausadas são retomadas automaticamente no final do período máximo de pausa de 14 dias. Eles podem ser retomados manualmente a qualquer momento.

Para retomar uma jornada pausada e começar a ouvir eventos de jornada novamente, siga estas etapas:

1. Abra a jornada que deseja retomar.
1. Clique no botão **...Mais** na seção superior direita da tela de jornada e selecione **Retomar**.

   A jornada alterna para o status **Retomando**. A transição do status **Retomando** para **Ao Vivo** pode levar algum tempo: todos os perfis precisam ser retomados para que a jornada seja **Ao Vivo** novamente.




