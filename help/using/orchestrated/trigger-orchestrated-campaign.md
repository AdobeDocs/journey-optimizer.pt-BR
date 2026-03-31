---
solution: Journey Optimizer
product: journey optimizer
title: Acionar uma campanha orquestrada usando um sinal
description: Saiba como acionar uma campanha Orquestrada usando um sinal no [!DNL Adobe Journey Optimizer].
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
source-git-commit: ec52b62c2d0626b9047eebb54e0a44fee096ec05
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%

---

# Acionar campanhas orquestradas usando um sinal {#trigger-signal}

Você pode acionar uma campanha Orquestrada enviando um sinal a ela em vez de executá-la de acordo com um agendamento. O sinal é enviado por uma chamada de API de um sistema ou aplicativo externo. Ao usar um sinal, você pode passar parâmetros. Eles são então disponibilizados na campanha orquestrada como variáveis de evento no contexto de execução — para uso em direcionamento, condições ou expressões.

Processo completo para acionar uma campanha orquestrada usando um sinal:

1. [Programar a campanha para ser acionada por um sinal](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [Adicionar parâmetros para a carga de sinal](#add-parameters-for-the-signal-payload-optional-parameters) (opcional)
1. [Criar e testar a campanha](#build-and-test-the-campaign-build-and-test)
1. [Publicar e acionar a campanha](#publish-and-trigger-the-campaign-publish)

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

Você pode passar parâmetros no sinal de acionador e usá-los em sua campanha no contexto de execução, por exemplo, em direcionamento, condições ou expressões. Primeiro, defina cada parâmetro nas configurações de agendamento e passe o respectivo valor ao chamar a API de acionador.

1. Abra o agendador de campanhas e selecione **[!UICONTROL Adicionar parâmetro]**.

1. Defina o nome de cada parâmetro e o tipo de dados que serão enviados na carga do sinal. Você também pode fornecer **Valores de teste** que serão usados quando você acionar a campanha no modo de teste. [Saiba como testar uma campanha acionada](#build-and-test).

   ![Adicionar parâmetro para definir parâmetros de carga para o sinal](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Se você passar um parâmetro na chamada à API que não foi definido no scheduler, a chamada à API ainda será bem-sucedida e o parâmetro será propagado e você poderá usá-lo em expressões. No entanto, a interface de campanha orquestrada não ajudará você a usá-la, por exemplo, a atividade Test não listará ou mostrará parâmetros que não foram definidos no scheduler.

## Criar e testar a campanha {#build-and-test}

Crie a campanha na tela e, opcionalmente, teste-a no rascunho acionando o sinal pela API antes de publicar.

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

1. Envie a chamada de API de acionador usando a solicitação de amostra copiada do scheduler. <!--For the complete API reference, refer to the [Journey Optimizer API documentation](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.-->

Quando estiver satisfeito com os resultados do teste, [publique a campanha](#publish).

## Publicar e acionar a campanha {#publish}

Depois de [criar e testar a campanha](#build-and-test), publique a campanha para que ela possa ser acionada pelo seu aplicativo.

1. Clique em **[!UICONTROL Publicar]** na tela da campanha. A campanha deve ser publicada antes de ser acionada a partir de um sistema externo. [Saiba mais sobre como iniciar e monitorar a campanha](start-monitor-campaigns.md#publish).

1. Abra o agendador de campanha, selecione **[!UICONTROL Copiar solicitação de API]** e escolha o formato (cURL ou Solicitação HTTP).

   As informações copiadas incluem a ID da campanha orquestrada, o nome da sandbox, a ID da organização e os parâmetros se você tiver adicionado alguns.

   ![Copiar solicitação de API na configuração de agendamento](assets/triggered-oc-copy.png)

1. Chame a API de acionador do seu sistema.

   >[!IMPORTANT]
   >
   >Para uma campanha orquestrada ao vivo, uma proteção de limitação impõe um **intervalo mínimo de uma hora** entre duas execuções de acionador de API. Se você chamar a API novamente antes que esse intervalo tenha decorrido, a API retornará o erro **HTTP 429** (muitas solicitações). Essa proteção não é aplicada quando você aciona uma versão de rascunho para testá-la.

   Se você adicionou parâmetros à carga do sinal, os valores transmitidos na chamada de API serão expostos como variáveis de evento da campanha quando a campanha for executada. Para inspecioná-los, abra os logs de campanha na barra de ferramentas da tela de campanha. Na guia **[!UICONTROL Tasks]**, identifique a tarefa correspondente ao sinal e clique no ícone de lápis para acessar as variáveis de evento relacionadas. [Saiba como acessar logs e tarefas](start-monitor-campaigns.md#logs-tasks).

   ![Tela de logs e tarefas em que as variáveis de evento da campanha estão disponíveis](assets/trigger-events-variables.png){zoomable="yes"}
