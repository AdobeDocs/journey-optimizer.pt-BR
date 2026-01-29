---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer.
feature: Monitoring
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
version: Campaign Orchestration
source-git-commit: 478bd6df8a82c9e37ec9319dedb27d99c021ee99
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 29%

---


# Iniciar e monitorar campanhas orquestradas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicar campanha orquestrada"
>abstract="Para iniciar a campanha, você deve publicá-la. Certifique-se de que todos os erros tenham sido resolvidos antes da publicação."

Depois de criar sua campanha orquestrada e projetar as tarefas a serem executadas na tela, você pode publicá-la e monitorar como ela está sendo executada. Você também poderá executar a campanha no modo de teste para verificar sua execução e o resultado das diferentes atividades.

## Testar a sua campanha antes de publicar {#test}

O [!DNL Journey Optimizer] permite que você teste campanhas Orquestradas antes de entrar no ar. Quando uma campanha é criada, ela entra no estado **Rascunho** por padrão. Nesse estado, é possível executar a campanha manualmente para testar o fluxo.

>[!IMPORTANT]
>
>Todas as atividades na tela são executadas, exceto **[!UICONTROL Salvar público-alvo]** atividades e atividades de canal. Não há nenhum impacto funcional nos seus dados ou público-alvo.

Para testar uma campanha Orquestrada, abra a campanha e selecione **[!UICONTROL Iniciar]**.

![Botão Iniciar na barra de ferramentas da tela de campanha](assets/campaign-start.png){zoomable="yes"}

Cada atividade na campanha é executada sequencialmente até que o final da tela seja atingido. Durante o teste, é possível controlar a execução da campanha usando a barra de ação na tela. Nela, você pode:

* **Parar** a execução a qualquer momento.
* **Iniciar** a execução novamente.
* **Reinicie** a execução para redefinir e executar novamente o fluxo de trabalho em uma única ação. Isso é particularmente útil quando você deseja testar novamente o fluxo da campanha rapidamente depois de fazer modificações.
* **Retomar** a execução se ela tiver sido pausada anteriormente.

O ícone **[!UICONTROL Alertas]** / **[!UICONTROL Aviso]** na barra de ferramentas da tela notifica sobre problemas, incluindo avisos que podem aparecer de forma proativa antes da execução e erros que ocorrem durante ou após a execução.

![Ícone de aviso na barra de ferramentas da tela de campanha](assets/campaign-warning.png){zoomable="yes"}

Você também pode identificar rapidamente as atividades com falhas, usando os [indicadores visuais de status](#activities) exibidos diretamente em cada atividade. Para obter uma resolução de problemas detalhada, abra os [logs da campanha](#logs-tasks), que fornecem informações detalhadas sobre o erro e seu contexto.

Se você tiver adicionado atividades de canal na tela, poderá visualizar e testar o conteúdo de suas mensagens usando o botão **[!UICONTROL Simular Conteúdo]**. [Saiba como trabalhar com atividades de canal](activities/channels.md)

Depois de validada, a campanha pode ser publicada.

## Publicar a campanha {#publish}

Depois que a campanha for testada e estiver pronta, clique em **[!UICONTROL Publicar]** para colocá-la no ar.

![Botão Publicar na tela da campanha](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>Se o botão **[!UICONTROL Publicar]** estiver desabilitado (esmaecido), acesse os logs na barra de ações e verifique as mensagens de erro. Todos os erros devem ser corrigidos antes de poder publicar uma campanha.

O fluxo visual é reiniciado, e perfis reais começam a fluir pela jornada em tempo real.

Se a ação de publicação falhar (por exemplo, devido à falta de conteúdo da mensagem), você será alertado e deverá corrigir o problema antes de tentar novamente. Após a publicação bem-sucedida, a campanha começa a ser executada (imediatamente ou de acordo com o agendamento), muda do status de **Rascunho** para o status **Online** e torna-se &quot;Somente leitura&quot;.

## Reverter uma campanha de volta ao rascunho {#back-to-draft}

O recurso **[!UICONTROL Voltar ao rascunho]** permite desfazer a publicação e reverter uma campanha orquestrada para o status de rascunho em situações específicas. Ele foi projetado como um mecanismo de recuperação para corrigir problemas antes que qualquer mensagem seja enviada, mantendo a integridade do ciclo de vida da campanha.

Essa opção está disponível em dois cenários:

* **Campanhas agendadas aguardando execução**: quando uma campanha está agendada para ser executada em um horário específico e esse horário ainda não foi atingido, você pode usar de volta ao rascunho para revisar e modificar a campanha antes que ela comece a ser executada. No entanto, se a campanha for recorrente (como uma campanha agendada diariamente) e pelo menos uma execução já tiver ocorrido, a opção não estará mais disponível. Nesse caso, você deve [duplicar a campanha](../campaigns/manage-campaigns.md#duplicate-a-campaign).

* **Campanhas ativas com erros de execução**: quando uma campanha encontra um erro durante a execução e é pausada, e nenhuma execução de campanha é concluída ainda, você pode usar voltar para rascunhar para corrigir o erro e republicar a campanha.

Para retornar uma campanha ao status de rascunho, abra a campanha orquestrada e clique no botão **[!UICONTROL Voltar ao rascunho]** na barra de ferramentas da tela de campanha.

![](assets/back-to-draft.png)

A publicação da campanha é desfeita e o fluxo de trabalho é interrompido. A campanha retorna ao status **Rascunho**. Agora você pode corrigir os problemas identificados e [testar a campanha](#test) e [publicá-la](#publish) novamente quando estiver pronto.

## Confirmar envio de mensagem {#confirm-sending}

Por padrão, para campanhas orquestradas não recorrentes, a entrega de mensagens é pausada até que você aprove explicitamente o envio. Depois de publicar a campanha, confirme a solicitação de envio no painel de propriedades da atividade de canal. Até que seja confirmado, a atividade do canal permanece pendente e nenhuma mensagem é enviada.

![imagem mostrando o botão Confirmar](assets/confirm-sending.png)

Antes de publicar, você pode desativar o envio de confirmação do painel de propriedades de atividades do canal. Para obter detalhes, consulte [Confirmar envio de mensagem](activities/channels.md#confirm-message-sending).

## Monitorar execução da campanha {#monitor}

### Monitoramento do fluxo visual {#flow}

Durante a execução (no modo de teste ou em tempo real), o fluxo visual mostra como os perfis se movem pela jornada em tempo real. O número de perfis que estão fazendo a transição entre tarefas é exibido.

![Execução do fluxo de trabalho da campanha mostrando o fluxo do perfil](assets/workflow-execution.png){zoomable="yes"}

Os dados transportados de uma atividade para outra através de transições são armazenados em uma tabela de trabalho temporária. Esses dados podem ser exibidos para cada transição. Para inspecionar os dados transmitidos entre atividades:

1. Selecione uma transição.
1. No painel de propriedades, clique em **[!UICONTROL Visualizar esquema]** para visualizar o esquema da tabela de trabalho. Selecione **[!UICONTROL Visualizar resultados]** para ver os dados transportados.

   ![Visualização da transição mostrando o esquema da tabela de trabalho e os resultados](assets/transition.png){zoomable="yes"}

### Indicadores de execução de atividades {#activities}

Os indicadores visuais de status ajudam a entender o desempenho de cada atividade:

| Indicador visual | Descrição |
|-----|------------|
| ![Status pendente](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | A atividade está sendo executada no momento. |
| ![Status laranja](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | A atividade requer a sua atenção. Isso pode envolver confirmar o envio de uma entrega ou realizar uma ação necessária. |
| ![Status do erro](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | A atividade encontrou um erro. Para resolver o problema, abra os logs da campanha Orquestrada para obter mais informações. |
| ![Status de sucesso](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | A atividade foi executada com sucesso. |

### Logs e tarefas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs e tarefas"
>abstract="A tela **Logs and tasks** fornece um histórico da execução de campanha orquestrada, registrando todas as ações de usuário e encontrando erros."

O monitoramento de logs e tarefas é uma etapa essencial para analisar suas campanhas orquestradas e garantir que elas estejam sendo executadas corretamente. Os logs e as tarefas podem ser acessados pelo botão **[!UICONTROL Logs]**, que está disponível no modo de teste e ativo na barra de ferramentas da tela.

![Botão Logs na barra de ferramentas da tela de campanha](assets/logs-button.png){zoomable="yes"}

A tela **[!UICONTROL Logs e tarefas]** fornece um histórico completo da execução da sua campanha, registrando todas as ações dos usuários e erros encontrados.

![Tela de logs e tarefas mostrando o histórico de execução da campanha](assets/workflow-logs.png){zoomable="yes"}

Dois tipos de informação estão disponíveis:

* A guia **[!UICONTROL Log]** contém o histórico cronológico de todas as operações e erros.
* A guia **[!UICONTROL Tarefas]** detalha a sequência de execução passo a passo das atividades.

Em ambas as guias, você pode escolher as colunas exibidas e sua ordem, aplicar filtros e usar o campo de pesquisa para localizar rapidamente as informações desejadas.

## Próximas etapas {#next}

Depois de iniciar a tela de campanha Orquestrada, você pode usar os recursos de relatórios do Journey Optimizer para obter insights, como entender o comportamento do público-alvo e medir o desempenho de cada etapa na jornada do cliente. [Saiba mais sobre os relatórios de campanhas orquestradas](../orchestrated/reporting-campaigns.md)
