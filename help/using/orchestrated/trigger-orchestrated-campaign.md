---
solution: Journey Optimizer
product: journey optimizer
title: Acionar uma campanha orquestrada usando um sinal
description: Saiba como acionar uma campanha Orquestrada com um sinal da API REST ou da atividade End de outra campanha e como transmitir parâmetros para a campanha.
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 1429
ht-degree: 0%

---

# Acionar campanhas orquestradas usando um sinal {#trigger-signal}

Você pode iniciar uma campanha Orquestrada com um sinal em vez de uma programação fixa. Quando a campanha recebe o sinal, ele é executado e você pode passar parâmetros na carga. Elas se tornam disponíveis como variáveis para direcionamento, condições ou expressões.

O sinal pode vir de um dos seguintes:

* API REST — Seu aplicativo ou integração chama o ponto de extremidade do acionador (consulte [Publicar e acionar a campanha](#publish) e a [Referência da API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}).
* Outra campanha Orquestrada — A atividade **[!UICONTROL End]** de uma campanha upstream envia o mesmo tipo de sinal quando uma ramificação é concluída. [Saiba como configurar a atividade End](#signal-end).

Esta página explica como configurar a campanha que recebe o sinal (agendamento, parâmetros, teste, publicação) e, em seguida, como acioná-la pela API ou por uma atividade **[!UICONTROL End]**. Quando as variáveis estiverem disponíveis, para obter detalhes sobre como usá-las em regras e condições de **[!UICONTROL Teste]**, consulte [Usar variáveis em campanhas orquestradas](variables-orchestrated-campaigns.md).

Para obter a especificação REST completa do ponto de extremidade do acionador (caminhos, cabeçalhos, corpo, respostas e erros), consulte [Acionar API de campanhas orquestradas](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} na documentação da API do Adobe Journey Optimizer.

Processo completo para acionar uma campanha orquestrada usando um sinal:

1. [Programar a campanha para ser acionada por um sinal](#configure-signal)
1. [Adicionar parâmetros para a carga de sinal](#parameters) (opcional)
1. [Criar e testar a campanha](#build-and-test)
1. [Publicar e acionar a campanha](#publish)

>[!NOTE]
>
>Para acionar uma campanha Orquestrada usando um sinal, você precisa da permissão **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish`). Consulte [Permissões internas](../administration/ootb-permissions.md).

## Programar a campanha para ser acionada por um sinal {#configure-signal}

Para definir uma campanha orquestrada para iniciar em um sinal em vez de um agendamento, siga estas etapas:

1. Abra a campanha Orquestrada que deseja acionar usando um sinal.

1. Abra a configuração do cronograma. [Saiba como agendar uma campanha orquestrada](create-orchestrated-campaign.md#schedule).

1. Selecione **[!UICONTROL Acionado por um sinal]** para que a campanha aguarde um sinal em vez de ser executada de acordo com um agendamento.

   ![Menu Agendar com opção de sinal disparado por](assets/triggered-oc-scheduler.png){zoomable="yes"} selecionada

## Adicionar parâmetros para a carga útil do sinal (opcional) {#parameters}

Você pode passar parâmetros no sinal de acionador e usá-los em sua campanha no contexto de execução — por exemplo, em direcionamento, condições ou expressões. Defina cada parâmetro nas configurações de agendamento primeiro e passe o respectivo valor ao chamar a API de acionador ou ao mapear parâmetros da atividade **[!UICONTROL End]** de uma campanha upstream ([veja abaixo](#signal-end)).

1. Abra o agendador de campanhas e selecione **[!UICONTROL Adicionar parâmetro]**.

1. Defina o nome de cada parâmetro e o tipo de dados que serão enviados na carga do sinal. Você também pode fornecer **Valores de teste** que serão usados quando você acionar a campanha no modo de teste. [Saiba como testar uma campanha acionada](#build-and-test).

   ![Adicionar parâmetro para definir parâmetros de carga para o sinal](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Para campanhas orquestradas acionadas pela API REST, se você passar um parâmetro na chamada de API que não foi definido no scheduler, a chamada de API ainda será bem-sucedida e o parâmetro será propagado, e você poderá usá-lo em expressões. No entanto, a interface de campanha orquestrada não ajudará você a usá-la; por exemplo, a atividade Test não listará ou mostrará parâmetros que não foram definidos no scheduler.

## Testar a campanha {#build-and-test}

Crie sua campanha na tela e teste-a no **[!UICONTROL Rascunho]** antes de publicar enviando o sinal pela API REST.

* **Campanhas orquestradas acionadas pela API REST** — Use as etapas abaixo para executar a campanha em rascunho e validar a definição de metas, os parâmetros e a lógica de entrega antes da publicação.

* **Campanhas orquestradas acionadas por uma atividade End** — Não é possível executar a cadeia completa de ponta a ponta no rascunho: depois que a campanha upstream é publicada, sua atividade **[!UICONTROL End]** inicia apenas uma campanha downstream publicada. Para testar o downstream antes que ambas as campanhas sejam publicadas, mantenha essa campanha no **[!UICONTROL Rascunho]**, defina **[!UICONTROL Valores de teste]** para seus parâmetros de sinal no scheduler ([Adicionar parâmetros para a carga de sinal](#parameters)) e siga as etapas de API abaixo. A chamada de API de gatilho usa a mesma carga que uma atividade **[!UICONTROL End]** no tempo de execução, portanto, você pode validar o roteamento de parâmetros e a lógica da tela antes de publicar a campanha downstream e configurar a atividade upstream **[!UICONTROL End]** ([Acionar a partir da atividade End de outra campanha](#signal-end)).

1. Adicione e conecte atividades (público-alvo, direcionamento, deliveries) na tela. [Saiba como orquestrar as atividades da campanha](orchestrate-activities.md)

1. Se você tiver definido parâmetros no sinal, é possível conectá-los à lógica da tela (por exemplo, em condições ou direcionamento). Neste exemplo, o parâmetro &quot;channel&quot; é usado como uma condição em uma atividade **[!UICONTROL Test]**.

   ![Parâmetro de canal usado como condição na atividade Test](assets/triggered-oc-use-parameters.png)

   Para usar um parâmetro de sinal no editor de expressão (por exemplo, para criar uma consulta em uma atividade **[!UICONTROL Criar público]**), digite `$(vars/@<parameterName>)` no campo de expressão. Substitua `<parameterName>` pelo nome de parâmetro definido no agendador; por exemplo, `$(vars/@channel)`. [Saiba como trabalhar com o editor de expressão](edit-expressions.md).

1. Abra o agendador de campanha, selecione **[!UICONTROL Copiar solicitação de API]** e escolha o formato (cURL ou Solicitação HTTP).

   As informações copiadas incluem a ID da campanha orquestrada, o nome da sandbox, a ID da organização e os valores de teste dos parâmetros, se você tiver adicionado alguns.

   ![Opção Copiar solicitação de API na configuração de agendamento](assets/triggered-oc-copy.png)

   +++Exemplo de solicitação de cURL com um parâmetro e um valor de teste

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Clique em **[!UICONTROL Iniciar]** para iniciar a campanha.

1. Envie a chamada de API de acionador usando a solicitação de amostra copiada do scheduler. Consulte [Acionar API de campanhas orquestradas](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} para obter detalhes sobre solicitações e respostas.

Quando estiver satisfeito com os resultados do teste, [publique a campanha](#publish).

## Publicar e acionar a campanha {#publish}

Depois de [testar a campanha](#build-and-test), publique-a para que ela possa receber um sinal do seu aplicativo ou da atividade **[!UICONTROL End]** de outra campanha. [Saiba mais sobre como iniciar e monitorar a campanha](start-monitor-campaigns.md#publish).

Em seguida, você pode acioná-lo a partir da API REST ou da atividade **[!UICONTROL End]** de outra campanha. Consulte as seções abaixo.

### Enviar o sinal com a API REST {#publish-api}

Após a publicação, siga estas etapas sempre que acionar a campanha a partir de seu próprio aplicativo:

1. Abra o agendador de campanha, selecione **[!UICONTROL Copiar solicitação de API]** e escolha o formato (cURL ou Solicitação HTTP).

   As informações copiadas incluem a ID da campanha orquestrada, o nome da sandbox, a ID da organização e os parâmetros se você tiver adicionado alguns.

   ![Copiar solicitação de API na configuração de agendamento](assets/triggered-oc-copy.png)

1. Chame a API de acionador do seu sistema. Consulte [Acionar API de campanhas orquestradas](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} para obter a especificação de ponto de extremidade ativo.

   >[!IMPORTANT]
   >
   >Para uma campanha orquestrada ao vivo, uma proteção de limitação impõe um intervalo mínimo de uma hora entre duas execuções de acionador de API. Se você chamar a API novamente antes que esse intervalo tenha decorrido, a API retornará HTTP 429 (muitas solicitações). Essa proteção não é aplicada quando você aciona uma versão de rascunho para testá-la.

   Se você adicionou parâmetros à carga do sinal, os valores transmitidos na chamada de API serão expostos como variáveis de evento da campanha quando a campanha for executada. Para inspecioná-los, abra os logs de campanha na barra de ferramentas da tela de campanha. Na guia **[!UICONTROL Tasks]**, identifique a tarefa correspondente ao sinal e clique no ícone de lápis para acessar as variáveis de evento relacionadas. [Saiba como acessar logs e tarefas](start-monitor-campaigns.md#logs-tasks).

   ![Tela de logs e tarefas em que as variáveis de evento da campanha estão disponíveis](assets/trigger-events-variables.png){zoomable="yes"}

### Enviar o sinal da atividade End de outra campanha {#signal-end}

Use este caminho para encadear campanhas orquestradas: quando a campanha upstream conclui uma ramificação, a atividade **[!UICONTROL End]** envia um sinal para uma campanha downstream que já está definida como **[!UICONTROL Acionada por um sinal]**. Isso permite reutilizar campanhas menores e transmitir uma carga diferente de cada chamador.

>[!NOTE]
>
>* Você pode usar várias atividades **[!UICONTROL End]** na mesma tela e configurar cada uma delas para acionar uma campanha downstream diferente.
>* Várias campanhas podem acionar a mesma campanha downstream. Cada chamada pode enviar uma carga diferente.

Siga estas etapas na campanha que deve ser executada primeiro:

1. Abra a campanha Orquestrada que deve enviar o sinal e selecione uma atividade **[!UICONTROL End]** ao final da ramificação que deve ser concluída antes do início da campanha downstream.
1. Na seção **[!UICONTROL Sinal externo]**, selecione a campanha downstream a ser acionada.

1. Opcionalmente, adicionar parâmetros: use os mesmos nomes do agendamento da campanha downstream e defina cada valor.

   ![](assets/end-signal.png)

1. Para testar a campanha downstream no modo de rascunho antes de publicá-la, siga as etapas na seção [testar a campanha](#build-and-test) para acioná-la no rascunho com a API REST.

A campanha downstream deve ser publicada antes que a campanha upstream seja executada o suficiente para alcançar a atividade **[!UICONTROL End]** que a aciona. Se o sinal for enviado enquanto a campanha de target não for publicada, a execução falhará. Publique a campanha downstream e, em seguida, retome ou reinicie conforme necessário.
