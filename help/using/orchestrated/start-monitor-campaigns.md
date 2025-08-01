---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 5e52573689ab06084441390299b01e112e699244
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 54%

---

# Inicie e monitore suas campanhas orquestradas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicar campanha orquestrada"
>abstract="Para iniciar a campanha, você deve publicá-la. Certifique-se de que todos os erros tenham sido resolvidos antes da publicação."

+++ Índice 

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/><b>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)</b><br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Depois de criar a campanha orquestrada e definir as tarefas a serem executadas na tela, você poderá publicá-la e monitorar como ela está sendo executada.

Você também poderá executar a campanha no modo de teste para verificar sua execução e o resultado das diferentes atividades.

## Testar a sua campanha antes de publicar {#test}

O [!DNL Journey Optimizer] permite que você teste campanhas Orquestradas antes de entrar no ar. Quando uma campanha é criada, ela entra no estado **Rascunho** por padrão. Nesse estado, é possível executar a campanha manualmente para testar o fluxo.

>[!IMPORTANT]
>
>Todas as atividades na tela são executadas, exceto **[!UICONTROL Salvar público-alvo]** atividades e atividades de canal. Não há impacto funcional nos seus dados ou público-alvo.**

Para testar uma campanha:

1. Abra a Campanha orquestrada.
2. Clique em **[!UICONTROL Iniciar]**.

![](assets/campaign-start.png){zoomable="yes"}

Cada atividade na campanha é executada sequencialmente até que o final do diagrama seja atingido.

Durante o teste, é possível controlar a execução da campanha usando a barra de ação na tela. Nela, você pode:

* **Parar** a execução a qualquer momento.
* **Iniciar** a execução novamente.
* **Retomar** a execução se ela tiver sido pausada anteriormente.

O ícone **[!UICONTROL Alertas]** / **[!UICONTROL Aviso]** na barra de ferramentas da tela notifica sobre problemas, incluindo avisos que podem aparecer de forma proativa antes da execução e erros que ocorrem durante ou após a execução.

![](assets/campaign-warning.png){zoomable="yes"}

Você também pode identificar rapidamente as atividades com falhas, usando os [indicadores visuais de status](#activities) exibidos diretamente em cada atividade. Para obter uma resolução de problemas detalhada, abra os [logs da campanha](#logs-tasks), que fornecem informações detalhadas sobre o erro e seu contexto.

Se você tiver adicionado atividades de canal na tela, poderá visualizar e testar o conteúdo de suas mensagens usando o botão **[!UICONTROL Simular Conteúdo]**. [Saiba como trabalhar com atividades de canal](activities/channels.md)

Depois de validada, a campanha pode ser publicada.

## Publicar a campanha {#publish}

Depois que a campanha for testada e estiver pronta, clique em **[!UICONTROL Publicar]** para colocá-la no ar.

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>Se o botão **[!UICONTROL Publicar]** estiver desabilitado (esmaecido), acesse os logs na barra de ações e verifique as mensagens de erro. Todos os erros devem ser corrigidos antes de poder publicar uma campanha.

O fluxo visual é reiniciado, e perfis reais começam a fluir pela jornada em tempo real.

Se a ação de publicação falhar (por exemplo, devido à falta de conteúdo da mensagem), você será alertado e deverá corrigir o problema antes de tentar novamente. Após a publicação bem-sucedida, a campanha começa a ser executada (imediatamente ou de acordo com o agendamento), muda do status de **Rascunho** para **Online** e torna-se &quot;Somente leitura&quot;.

## Monitorar execução da campanha {#monitor}

### Monitoramento do fluxo visual {#flow}

Durante a execução (no modo de teste ou em tempo real), o fluxo visual mostra como os perfis se movem pela jornada em tempo real. O número de perfis que estão fazendo a transição entre tarefas é exibido.

![](assets/workflow-execution.png){zoomable="yes"}

Os dados transportados de uma atividade para outra através de transições são armazenados em uma tabela de trabalho temporária. Esses dados podem ser exibidos para cada transição. Para inspecionar os dados transmitidos entre atividades:

1. Selecione uma transição.
1. No painel de propriedades, clique em **[!UICONTROL Visualizar esquema]** para visualizar o esquema da tabela de trabalho. Selecione **[!UICONTROL Visualizar resultados]** para ver os dados transportados.

![](assets/transition.png){zoomable="yes"}

### Indicadores de execução de atividades {#activities}

Os indicadores visuais de status ajudam a entender o desempenho de cada atividade:

| Indicador visual | Descrição |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | A atividade está sendo executada no momento. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | A atividade requer a sua atenção. Isso pode envolver confirmar o envio de uma entrega ou realizar uma ação necessária. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | A atividade encontrou um erro. Para resolver o problema, abra os logs da campanha Orquestrada para obter mais informações. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | A atividade foi executada com sucesso. |

### Logs e tarefas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs e tarefas"
>abstract="A tela **Logs and tasks** fornece um histórico da execução de campanha orquestrada, registrando todas as ações de usuário e encontrando erros."

O monitoramento de logs e tarefas é uma etapa essencial para analisar suas campanhas orquestradas e garantir que elas estejam sendo executadas corretamente. Os logs e tarefas podem ser acessados por meio do botão **[!UICONTROL Logs]**, que está disponível nos modos de teste e em tempo real, na barra de ferramentas da tela ou no painel de propriedades de cada atividade.

A tela **[!UICONTROL Logs e tarefas]** fornece um histórico completo da execução da sua campanha, registrando todas as ações dos usuários e erros encontrados.

![](assets/workflow-logs.png){zoomable="yes"}

Dois tipos de informação estão disponíveis:

* A guia **[!UICONTROL Log]** contém o histórico cronológico de todas as operações e erros.
* A guia **[!UICONTROL Tarefas]** detalha a sequência de execução passo a passo das atividades.

Em ambas as guias, você pode escolher as colunas exibidas e sua ordem, aplicar filtros e usar o campo de pesquisa para localizar rapidamente as informações desejadas.
