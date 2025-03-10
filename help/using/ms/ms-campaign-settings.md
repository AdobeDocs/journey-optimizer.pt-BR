---
solution: Journey Optimizer
product: journey optimizer
title: Definir configurações da campanha em várias etapas
description: Saiba como definir configurações de campanha em várias etapas com o Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 8%

---


# Definir configurações da campanha em várias etapas {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propriedades da campanha em várias etapas"
>abstract="Nesta tela, escolha o template a ser usado para criar a campanha de várias etapas e especifique um rótulo. Expanda a seção **Opções adicionais** para definir mais configurações, como o nome interno da campanha de várias etapas, sua pasta, fuso horário e grupo supervisor. É altamente recomendável selecionar um grupo supervisor, para que, se ocorrer um erro, os operadores sejam alertados."

Ao criar uma campanha em várias etapas ou organizar atividades de campanha em várias etapas na tela, você pode acessar configurações avançadas relacionadas à campanha em várias etapas. Por exemplo, você pode definir um fuso horário específico para a campanha em várias etapas, gerenciar como a campanha em várias etapas deve se comportar em caso de erro ou gerenciar o atraso após o qual o histórico da campanha em várias etapas deve ser removido.

Essas configurações são pré-definidas no template selecionado ao criar a campanha em várias etapas, mas podem ser editadas conforme necessário para essa campanha específica em várias etapas.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propriedades da campanha em várias etapas {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propriedades da campanha em várias etapas"
>abstract="Esta seção fornece propriedades de campanha genéricas em várias etapas que também podem ser acessadas ao criar a campanha em várias etapas. Você pode escolher o template a ser usado para criar a campanha de várias etapas e especificar um rótulo. Expanda a seção Opções adicionais para definir configurações específicas, como a pasta de armazenamento de campanha de várias etapas ou o fuso horário."

A seção **[!UICONTROL Propriedades]** fornece configurações genéricas que podem ser definidas ao criar uma campanha de várias etapas. Para acessar as propriedades de uma campanha em várias etapas existente, clique no botão **[!UICONTROL Configurações]** disponível na barra de ações acima da tela de campanha em várias etapas.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Essas propriedades são:

* O **[!UICONTROL Rótulo]** da campanha de várias etapas que é exibido na lista.
* O **[!UICONTROL Nome interno]** da campanha de várias etapas.
* A **[!UICONTROL Pasta]** onde a campanha de várias etapas deve ser salva.
* O **[!UICONTROL Fuso horário]** padrão a ser usado em todas as atividades de campanha de várias etapas. Por padrão, o fuso horário da campanha de várias etapas é aquele definido para o operador atual do Campaign.
Os valores possíveis são:
   * **Fuso horário do servidor** para usar o fuso horário de sua organização da Adobe Experience Platform
   * **Fuso horário do operador** para usar o fuso horário do operador que executa a campanha de várias etapas
   * **Fuso horário do banco de dados** para usar o fuso horário do servidor de banco de dados
   * Um fuso horário específico
* Quando uma campanha em várias etapas falha, os operadores pertencentes ao grupo de operadores selecionado no campo **[!UICONTROL Supervisor(es)]** são notificados por email.
* Você também pode inserir uma **[!UICONTROL Descrição]** da sua campanha em várias etapas.

## Configurações de segmentação  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configurações de segmentação"
>abstract="Nesta seção, você pode selecionar o targeting dimension para direcionar perfis na campanha em várias etapas e escolher manter os resultados do fluxo de trabalho entre duas execuções. Essa opção deve ser usada somente para fins de teste e nunca deve ser ativada em uma campanha de produção em várias etapas."

* **[!UICONTROL Targeting dimension]**: selecione a targeting dimension a ser usada para direcionar perfis: recipients, beneficiários de contrato, operadores, assinantes, etc.

* **[!UICONTROL Manter o resultado de populações interinas entre duas execuções]**: por padrão, somente as tabelas de trabalho da última execução da campanha de várias etapas são mantidas. As tabelas de trabalho das execuções anteriores são removidas por uma campanha técnica de várias etapas, executada diariamente.

  Se essa opção estiver ativada, as tabelas de trabalho serão mantidas mesmo após a execução da campanha de várias etapas. Você pode usá-lo para fins de teste e, portanto, deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Ele nunca deve ser verificado em uma campanha de produção em várias etapas.

## Configurações de execução  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, você pode definir configurações relacionadas à execução do fluxo de trabalho, como o número de dias em que o histórico da campanha em várias etapas é mantido."

* **[!UICONTROL Histórico em dias]**: especifica o número de dias após o qual o histórico deve ser limpo. O histórico contém elementos relacionados à campanha em várias etapas: logs, tarefas, eventos (objetos técnicos vinculados à operação da campanha em várias etapas). O valor padrão é de 30 dias para modelos de campanha de várias etapas prontos para uso. A limpeza do histórico é executada pela campanha técnica de várias etapas Database cleanup, que é executada por padrão todos os dias

  >[!IMPORTANT]
  >
  >Se o campo **[!UICONTROL Histórico em dias]** for deixado em branco, o valor “1” será considerado, o que significa que o histórico será removido após 1 dia.

* **[!UICONTROL Afinidade padrão]**: se a sua instalação incluir vários servidores de campanha de várias etapas, use este campo para especificar o servidor no qual a campanha de várias etapas será executada. Isso força a execução dessa campanha em várias etapas em um servidor específico. Você pode escolher qualquer nome de afinidade existente, mas não use espaços ou sinais de pontuação. Se você usar servidores diferentes, especifique nomes diferentes, separados por vírgulas.

  >[!IMPORTANT]
  >
  >Se o valor definido nesse campo não existir em nenhum servidor, a campanha de várias etapas permanecerá pendente.


* **[!UICONTROL Salvar consultas SQL no log]**: marque esta opção para salvar as consultas SQL da campanha de várias etapas do fluxo de trabalho agora nos logs. Essa operação é reservada para usuários avançados. Aplica-se a campanhas em várias etapas que contêm atividades de direcionamento como **[!UICONTROL Criar público-alvo]**. Quando essa opção está habilitada, as consultas SQL enviadas ao banco de dados durante a execução da campanha em várias etapas são exibidas nos logs da campanha em várias etapas, permitindo analisá-las para otimizar as consultas ou diagnosticar problemas.

## Configurações de gerenciamento de erros  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, você pode definir como a campanha em várias etapas deve gerenciar os erros durante sua execução. Você pode optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da campanha em várias etapas."

* **[!UICONTROL Gerenciamento de erros]**: este campo permite que você defina as ações a serem executadas se uma tarefa de campanha de várias etapas tiver erros. Há três opções possíveis:

   * **[!UICONTROL Suspender o processo]**: a campanha de várias etapas é pausada automaticamente e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, retome a campanha em várias etapas usando os botões **[!UICONTROL Retomar]**.
   * **[!UICONTROL Ignore]**: o status da tarefa que provocou o erro muda para **[!UICONTROL Failed]**, mas a campanha em várias etapas mantém o status **[!UICONTROL Started]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular o processo]**: a campanha de várias etapas é automaticamente interrompida e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, reinicie a campanha em várias etapas usando os botões **[!UICONTROL Iniciar]**.

* **[!UICONTROL Erros consecutivos]**: este campo fica disponível quando o valor **[!UICONTROL Ignorar]** é selecionado no campo **[!UICONTROL Em caso de erros]**. Você pode especificar quantos erros podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da campanha de várias etapas será alterado para **[!UICONTROL Failed]**. Se o valor desse campo for 0, a campanha em várias etapas nunca será interrompida, independentemente do número de erros.

## Script de inicialização {#initialization-script}

O **script de Inicialização** permite inicializar variáveis ou modificar propriedades da atividade. Clique no botão **Editar código** e digite o trecho de código a ser executado. O script é chamado quando a campanha em várias etapas é executada. Consulte a seção relacionada a [variáveis de evento](event-variables.md).

