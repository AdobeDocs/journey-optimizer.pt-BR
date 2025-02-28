---
solution: Journey Optimizer
product: journey optimizer
title: Usar um público em uma jornada
description: Saiba como usar um público em uma jornada
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: atividade, jornada, leitura, público-alvo, plataforma
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 85a8d0713f87a8b3505a2294402156ba6598c8bb
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 12%

---

# Usar um público em uma jornada {#segment-trigger-activity}

## Adicionar uma atividade Ler público-alvo {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Atividade Ler público-alvo"
>abstract="A atividade Ler público-alvo permite que todas as pessoas pertencentes a um público-alvo da Adobe Experience Platform entrem em uma jornada. A entrada em uma jornada pode ser efetuada uma vez ou regularmente."

Use a atividade **Ler público-alvo** para fazer com que todos os indivíduos de um público-alvo entrem na jornada. A entrada em uma jornada pode ser efetuada uma vez ou regularmente.

Vamos ver como exemplo o público-alvo &quot;Abertura e finalização do aplicativo Luma&quot; criado no caso de uso [Criar públicos-alvo](../audience/about-audiences.md). Com a atividade Ler público-alvo, você pode fazer com que todos os indivíduos pertencentes a esse público-alvo insiram uma jornada e façam com que eles fluam para jornadas individualizadas que aproveitarão todas as funcionalidades da jornada: condições, temporizadores, eventos, ações.

➡️ [Descubra este recurso no vídeo](#video)

## Medidas de proteção e práticas recomendadas {#must-read}

* Para jornadas que usam uma atividade de **público-alvo de leitura**, há um número máximo de jornadas que podem ser iniciadas ao mesmo tempo. As tentativas serão executadas pelo sistema, mas evite ter mais de cinco jornadas (com **Ler público**, agendado ou iniciando &quot;o mais rápido possível&quot;) iniciando exatamente ao mesmo tempo. A prática recomendada é espalhá-las ao longo do tempo, por exemplo, com intervalos de 5 a 10 minutos.

* Os grupos de campos de evento de experiência não podem ser usados em jornadas que comecem com uma atividade **Ler público-alvo**, uma atividade **[Qualificação de público-alvo](audience-qualification-events.md)** ou uma atividade de evento comercial.

* Como prática recomendada, você só deve usar públicos-alvo em lote em uma atividade **Ler público-alvo**. Isso fornecerá uma contagem confiável e consistente para os públicos-alvo usados em uma jornada. O público-alvo de leitura foi projetado para casos de uso em lote. Se o seu caso de uso precisa de dados em tempo real, use a atividade **[Qualificação de público-alvo](audience-qualification-events.md)**.

* Os públicos-alvo [importados de um arquivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) ou resultantes de [fluxos de trabalho de composição](../audience/get-started-audience-orchestration.md) podem ser selecionados na atividade **Ler Público**. Estes públicos-alvo não estão disponíveis na atividade **Qualificação de público-alvo**.


As medidas de proteção relacionadas à atividade **Ler público** estão listadas em [esta página](../start/guardrails.md#read-segment-g).


## Configurar a atividade {#configuring-segment-trigger-activity}

As etapas para configurar a atividade Ler público-alvo são as seguintes:

1. Expanda a categoria **[!UICONTROL Orquestração]** e solte uma atividade **[!UICONTROL Ler público]** na tela.

   A atividade deve ser posicionada como a primeira etapa de uma jornada.

1. Adicione um **[!UICONTROL Rótulo]** à atividade (opcional).

1. No campo **[!UICONTROL Público-alvo]**, escolha o público-alvo da Adobe Experience Platform que inserirá a jornada e clique em **[!UICONTROL Salvar]**. Você pode selecionar qualquer público-alvo do Adobe Experience Platform gerado usando [definições de segmento](../audience/creating-a-segment-definition.md).

   >[!NOTE]
   >
   >Além disso, você também pode direcionar públicos-alvo da Adobe Experience Platform criados com o uso de [composições de público-alvo](../audience/get-started-audience-orchestration.md) ou [carregados de um arquivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.

   Observe que é possível personalizar as colunas exibidas na lista e classificá-las.

   ![](assets/read-segment-selection.png)

   Depois que o público-alvo é adicionado, o botão **[!UICONTROL Copiar]** permite copiar seu nome e ID:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >Somente os indivíduos com o status de participação de público **Realizado** entrarão na jornada. Para obter mais informações sobre como avaliar um público, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. No campo **[!UICONTROL Namespace]**, escolha o namespace a ser usado para identificar os indivíduos. Por padrão, o campo é pré-preenchido com o último namespace usado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Os indivíduos pertencentes a um público-alvo que não tem a identidade (namespace) selecionada entre suas diferentes identidades não podem entrar na jornada. Você só pode selecionar um namespace de identidade com base em pessoas. Se você tiver definido um namespace para uma tabela de pesquisa (por exemplo: namespace ProductID para uma pesquisa de Produto), ele não estará disponível na lista suspensa **Namespace**.

1. Defina a **[!UICONTROL Taxa de leitura]**. Esse é o número máximo de perfis que podem entrar na jornada por segundo. Essa taxa se aplica somente a essa atividade e nenhuma outra na jornada. Se você deseja definir uma taxa de limitação em ações personalizadas, por exemplo, é necessário usar a API de limitação. Consulte esta [página](../configuration/throttling.md).

   Esse valor é armazenado na carga da versão do jornada. O valor padrão é de 5.000 perfis por segundo. Você pode modificar esse valor de 500 para 20.000 perfis por segundo.

   >[!NOTE]
   >
   >A taxa de leitura geral por sandbox está definida como 20.000 perfis por segundo. Portanto, a taxa de leitura de todos os públicos-alvo de leitura executados simultaneamente na mesma sandbox totaliza no máximo 20.000 perfis por segundo. Não é possível modificar esse limite.

1. A atividade **[!UICONTROL Ler público-alvo]** permite especificar a hora em que o público-alvo inserirá a jornada. Para fazer isso, clique no link **[!UICONTROL Editar agendamento de jornada]** para acessar as propriedades da jornada e configure o campo **[!UICONTROL Tipo de agendador]**.

   ![](assets/read-segment-schedule.png)

   Por padrão, os públicos-alvo entram na jornada **[!UICONTROL Assim que possível]**. Se você quiser que o público-alvo insira a jornada em uma data/hora específica ou de forma recorrente, selecione o valor desejado na lista.

   >[!NOTE]
   >
   >Observe que a seção **[!UICONTROL Agenda]** só estará disponível quando uma atividade **[!UICONTROL Ler Público]** for descartada na tela.

   ![](assets/read-segment-schedule-list.png)

   Opção **Leitura incremental**: quando uma jornada com uma **Leitura de público** recorrente é executada pela primeira vez, todos os perfis da audiência entram na jornada. Essa opção permite direcionar, após a primeira ocorrência, somente os indivíduos que entraram no público-alvo desde a última execução da jornada.

       >[!NOTE]
       >
       >Se você estiver direcionando um [público-alvo de carregamento personalizado](../audience/about-audiences.md#segments-in-jornada-otimizer) em sua jornada, os perfis só serão recuperados na primeira recorrência se esta opção estiver habilitada em uma jornada recorrente, já que esses públicos-alvo estão corrigidos.
   
   **Forçar reentrada na recorrência**: essa opção permite fazer com que todos os perfis ainda presentes na jornada saiam automaticamente na próxima execução. Por exemplo, se você tiver 2 dias de espera em uma jornada recorrente diária, ao ativar essa opção os perfis sempre serão movidos na próxima execução da jornada (ou seja, no dia seguinte), estejam ou não no público da próxima execução. Se a duração dos perfis nesta jornada for maior que a frequência de recorrência, não ative essa opção para garantir que os perfis possam concluir a jornada.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>As jornadas de público-alvo de Leitura Única são movidas para o status **Concluído** 91 dias ([Tempo limite global da jornada](journey-properties.md#global_timeout)) após a execução da jornada. Para públicos-alvo de leitura agendados, isso acontece 91 dias após a execução da última ocorrência.

## Testar e publicar a jornada {#testing-publishing}

A atividade **[!UICONTROL Ler público-alvo]** permite testar a jornada em um perfil unitário.

Para fazer isso, ative o modo de teste.

![](assets/read-segment-test-mode.png)

Configure e execute o modo de teste como de costume. [Saiba como testar uma jornada](testing-the-journey.md).

Depois que o teste estiver em execução, o botão **[!UICONTROL Mostrar logs]** permitirá que você veja os resultados do teste. Para obter mais informações, consulte [esta seção](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

Depois que os testes forem concluídos com êxito, você poderá publicar sua jornada (consulte [Publicando a jornada](publishing-the-journey.md)). Os indivíduos pertencentes ao público inserirão a jornada na data/hora especificada na seção **[!UICONTROL Scheduler]** das propriedades da jornada.

>[!NOTE]
>
>Para jornadas recorrentes baseadas em público-alvo, a jornada será fechada automaticamente assim que sua última ocorrência for executada. Se nenhuma data/hora final tiver sido especificada, será necessário fechar a jornada para novas entradas manualmente para encerrá-la.

## Direcionamento de público em jornadas baseadas em público

As jornadas baseadas em público-alvo sempre começam com uma atividade **Ler público-alvo** para recuperar indivíduos que pertencem a um público da Adobe Experience Platform.

O público-alvo pertencente ao público-alvo é recuperado uma vez ou regularmente.

Depois de inserir a jornada, você pode criar casos de uso de orquestração de público, fazendo com que os indivíduos do público inicial fluam para diferentes ramificações da jornada.

**Segmentação**

Você pode usar condições para executar a segmentação usando a atividade **Condição**. Por exemplo, você pode fazer com que as pessoas da VIP tomem um determinado caminho e o fluxo não-VIP em outro caminho.

A segmentação pode ser baseada em:

* dados da fonte de dados
* o contexto de eventos que faz parte dos dados de jornada, por exemplo: uma pessoa clicou na mensagem recebida há uma hora?
* uma data, por exemplo: estamos em junho quando uma pessoa passa pela jornada?
* uma hora, por exemplo: é de manhã no fuso horário da pessoa?
* um algoritmo que divide o público-alvo fluindo na jornada com base em uma porcentagem, por exemplo: 90% - 10% para excluir um grupo de controle

![](assets/read-segment-audience1.png)

**Exclusão**

A mesma atividade **Condition** usada para segmentação (veja acima) também permite excluir parte da população. Por exemplo, você pode excluir pessoas do VIP fazendo com que elas fluam para uma ramificação com uma etapa final logo após.

Essa exclusão pode ocorrer logo após a recuperação do público-alvo, para fins de contagem de população ou ao longo de uma jornada em várias etapas.

![](assets/read-segment-audience2.png)

**União**

As jornadas permitem criar N ramificações e juntá-las após uma segmentação.

Como resultado, você pode fazer com que dois públicos-alvo retornem a uma experiência comum.

Por exemplo, depois de seguir uma experiência diferente durante dez dias em uma jornada, os clientes da VIP VIP e de terceiros podem retornar ao mesmo caminho.

Após uma união, é possível dividir o público novamente executando uma segmentação ou exclusão.

![](assets/read-segment-audience3.png)


## Tentativas {#read-audience-retry}

As novas tentativas são aplicadas por padrão em jornadas acionadas por público-alvo (começando com um **público-alvo de leitura** ou um **evento de negócios**) ao recuperar o trabalho de exportação. Se ocorrer um erro durante a criação do trabalho de exportação, as novas tentativas serão realizadas a cada 10 minutos por, no máximo, 1 hora. Depois disso, vamos considerá-la como uma falha. Esses tipos de jornada podem, portanto, ser executados até 1 hora após o horário agendado.

Os acionadores **Read Audience** malsucedidos são capturados e exibidos em **Alertas**. O **alerta de Leitura de público** avisa se uma atividade de **Leitura de público** não processou nenhum perfil 10 minutos após o horário agendado de execução. Essa falha pode ser causada por problemas técnicos ou porque o público-alvo está vazio. Se essa falha for causada por problemas técnicos, esteja ciente de que ainda podem ocorrer tentativas, dependendo do tipo de problema (por exemplo: se a criação do trabalho de exportação falhar, tentaremos novamente a cada 10mn para um máximo de 1h). [Saiba mais](../reports/alerts.md#alert-read-audiences)

## Vídeo explicativo {#video}

Entenda os casos de uso aplicáveis para uma jornada acionada pela atividade de leitura de público-alvo. Saiba como criar jornadas baseadas em lote e quais práticas recomendadas devem ser aplicadas.

>[!VIDEO](https://video.tv.adobe.com/v/3424997?quality=12)
