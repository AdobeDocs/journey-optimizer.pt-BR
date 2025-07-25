---
solution: Journey Optimizer
product: journey optimizer
title: Criar e programar campanhas orquestradas com o Journey Optimizer
description: Saiba como criar e programar uma campanha orquestrada com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 00e7ede1d8576aeef411caffd9c4251a6957f0ad
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 84%

---


# Criar e agendar uma campanha orquestrada {#create-first-campaign}

+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | <b>[Criar e programar a campanha](create-orchestrated-campaign.md)</b><br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++
<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Crie uma campanha orquestrada no [!DNL Adobe Journey Optimizer] e configure o cronograma de sua execução para controlar quando ela começará e com que frequência será executada. Opte por iniciar a campanha imediatamente, em uma data e hora específicas, ou de forma recorrente, usando as opções de programação flexíveis, como frequência diária, semanal ou mensal.

## Criar a campanha {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campanhas orquestradas"
>abstract="A guia **Orquestração** lista todas as campanhas orquestradas. Clique no nome de uma campanha orquestrada para editá-la. Use o botão **Criar campanha orquestrada** para adicionar uma nova campanha orquestrada. "

Para criar uma campanha orquestrada, siga estas etapas:

1. Navegue até o menu **[!UICONTROL Campanhas]** e selecione a guia **[!UICONTROL Orquestração]**.

1. Clique no botão **[!UICONTROL Criar campanha]** e selecione o tipo de campanha **[!UICONTROL Orquestração - Marketing]**.

   ![](assets/create-modal.png)

1. Defina as propriedades da campanha. Para fazer isso, clique no botão ![Configurações da campanha](assets/do-not-localize/campaign-settings.svg) ao lado do nome da campanha.

   ![](assets/inventory-create.png)

   1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** para a campanha.

   1. Selecione uma **[!UICONTROL Política de mesclagem]** para sua campanha.

      No [!DNL Adobe Experience Platform], cada público-alvo está vinculado a uma política de mesclagem específica, que define como as informações de perfil são combinadas para formar um perfil mesclado. Ao selecionar uma política de mesclagem na atividade Ler público, somente os públicos-alvo com base na mesma política de mesclagem ficam disponíveis. Por padrão, o sistema usa a política de mesclagem padrão, mas você pode alterá-la se necessário. Para obter mais informações sobre políticas de mesclagem, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

   1. Use o campo **[!UICONTROL Tags]** para atribuir Tags unificadas do Adobe Experience Platform à sua campanha. Isso permite classificá-las facilmente e melhorar a pesquisa a partir da lista de campanhas orquestradas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags).

   1. Clique em **[!UICONTROL Salvar]**.

## Agendar a campanha {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Scheduler"
>abstract="Como gerente de campanha, é possível agendar o início automático de campanhas em horários específicos, permitindo o início no tempo adequado e dados de direcionamento precisos para comunicações de marketing."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validade do Scheduler"
>abstract="É possível definir um período de validade para o Scheduler. Pode ser permanente (padrão) ou pode ser válido até uma data específica."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opções do Scheduler"
>abstract="Defina a frequência do scheduler. Pode ser executado em um momento específico, uma ou várias vezes por dia, semana ou mês."

Por padrão, as campanhas orquestradas começam quando ativadas manualmente e terminam após a execução de suas atividades associadas. Se preferir atrasar a execução ou executar a campanha de forma recorrente, é possível definir um cronograma para a campanha.

Considere as seguintes práticas recomendadas ao programar campanhas orquestradas para garantir o desempenho ideal e o comportamento esperado:

* Não agende uma campanha orquestrada para ser executada com uma frequência maior que a cada 15 minutos, pois isso pode prejudicar o desempenho geral do sistema e criar bloqueios no banco de dados.
* Se quiser enviar uma mensagem instantânea na sua campanha orquestrada, é possível configurá-la para ser executada **Uma vez**.
* Para enviar uma mensagem recorrente na sua campanha orquestrada, use as opções de **Agendamento** e defina a frequência de execução. A atividade de entrega recorrente não permite definir um cronograma.

Para configurar o cronograma da campanha, siga estas etapas:

1. Abra a campanha e clique no botão **[!UICONTROL Assim que possível]**.

   ![](assets/create-schedule.png)

1. Selecione uma frequência de execução para a campanha e configure as opções disponíveis. As configurações variam de acordo com a frequência selecionada:

   +++Uma vez

   Execute a campanha uma vez em uma data e hora especificadas.

   * **[!UICONTROL Data]**: selecione a data em que a campanha deve ser executada.
   * **[!UICONTROL Hora]**: selecione a hora específica em que a campanha deve ser executada.

   +++

   +++Diariamente

   Execute a campanha todos os dias ou em dias selecionados.

   * **[!UICONTROL Recorrência diária]**: escolha a frequência de execução da campanha:
      * **[!UICONTROL Todos os dias]**: executa a campanha todos os dias da semana, inclusive fins de semana.
      * **[!UICONTROL Nos dias de semana]**: executa a campanha somente de segunda a sexta.
      * **[!UICONTROL Até um período específico]**: executa a campanha diariamente dentro de um intervalo de datas definido (por exemplo, de 1.º a 15 de julho). A campanha não será executada fora desse intervalo.
      * **[!UICONTROL Em dias da semana selecionados]**: executa a campanha somente nos dias da semana especificados (por exemplo, segunda, quarta, sexta).

   * **[!UICONTROL Hora inicial]**: defina a hora em que a campanha deve ser executada a cada dia.

   +++

   +++Várias vezes ao dia

   Execute a campanha várias vezes no mesmo dia. Você pode escolher horários específicos ou definir uma frequência periódica.

   * **[!UICONTROL Horas selecionadas]**: selecione as horas específicas em que a campanha deve ser executada e configure sua recorrência diária (executar em todos os dias da semana ou em determinados dias).
   * **[!UICONTROL Periódico]**: opte por executar a campanha a cada n minutos ou horas. Você também pode definir o intervalo de tempo no dia em que as execuções são permitidas.

   +++

   +++Semanalmente

   Execute a campanha semanalmente, com opções de dias específicos.

   * **[!UICONTROL Frequência]**: escolha a frequência de execução da campanha (por exemplo, toda semana, a cada duas semanas).
   * **[!UICONTROL A partir da data]**: selecione a data em que a recorrência deve começar.
   * **[!UICONTROL Recorrência diária]**: escolha dias da semana específicos para a execução (por exemplo, toda segunda e quinta).
   * **[!UICONTROL Hora inicial]**: defina a hora em que a campanha deve ser executada nos dias selecionados.

   +++

   +++Mensalmente

   Execute a campanha mensalmente, com opções de dias específicos.

   * **[!UICONTROL Recorrência mensal]**: selecione se a campanha será executada a cada mês ou somente durante meses específicos.
   * **[!UICONTROL Recorrência diária]**:
      * **[!UICONTROL Todos os dias]**: executa a campanha em todos os dias do mês, inclusive fins de semana.
      * **[!UICONTROL Último dia do mês]**: executa a campanha somente no último dia de cada mês (por exemplo, 31 de janeiro, 28/29 de fevereiro).
      * **[!UICONTROL Dia específico do mês (por exemplo, dia 15)]**: executa a campanha em um dia especificado (por exemplo, o dia 15 de cada mês).
      * **[!UICONTROL Primeiro/último ou um dia específico da semana]** (por exemplo, primeira segunda-feira): executa a campanha em um dia da semana especificado (por exemplo, o dia 15 de cada semana).
      * **[!UICONTROL Dias da semana selecionados]**: executa a campanha em um dia especificado.

   * **[!UICONTROL Hora inicial]**: defina a hora em que a campanha deve ser executada.

   +++

1. Use a configuração **[!UICONTROL Período de validade]** para definir uma data inicial e uma data final específicas, restringindo a execução da campanha a uma janela de tempo limitada.

1. Para programações recorrentes, clique no botão **[!UICONTROL Visualizar horas de inicialização]** para visualizar as datas e horas exatas de execuções futuras com base na configuração atual. Isso ajuda a validar o cronograma antes da ativação e garante que a campanha seja executada conforme esperado.

>[!NOTE]
>
>Ao agendar campanhas no [!DNL Adobe Journey Optimizer], verifique se a data/hora inicial está de acordo com a primeira entrega desejada. Para campanhas recorrentes, se o horário programado inicial já tiver passado, as campanhas serão transferidas para o próximo período disponível, de acordo com as suas regras de recorrência.

No exemplo a seguir, a atividade é configurada para que a campanha orquestrada seja executada duas vezes por dia, às 9h e às 12h, todos os dias da semana, de 1.º de outubro de 2025 a 1.º de janeiro de 2026.

![Scheduler configurado para executar a campanha duas vezes por dia, às 9h e às 12h](assets/scheduler-sample.png){width="50%" align="left"}

## Próximas etapas {#next}

Depois de definir as configurações e o cronograma da campanha, você já pode começar a orquestrar as diferentes tarefas que ele executará. [Saiba como orquestrar as atividades da campanha](../orchestrated/orchestrate-activities.md)
