---
solution: Journey Optimizer
product: journey optimizer
title: Definir configurações de campanha orquestrada
description: Saiba como definir configurações de campanha orquestrada com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 3d33d0bdbaf5b56a68d4ea708ce023c6aaae4811
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 8%

---

# Definir configurações de campanha orquestrada {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propriedades da campanha orquestrada"
>abstract="Nesta tela, escolha o template a ser usado para criar a campanha orquestrada e especifique um rótulo. Expanda a seção **Opções adicionais** para definir mais configurações, como o nome interno da campanha orquestrada, sua pasta, fuso horário e grupo supervisor. É altamente recomendável selecionar um grupo supervisor, para que, se ocorrer um erro, os operadores sejam alertados."

Ao criar uma campanha orquestrada ou orquestrar atividades de campanha orquestrada na tela, você pode acessar configurações avançadas relacionadas à campanha orquestrada. Por exemplo, é possível definir um fuso horário específico para a campanha orquestrada, gerenciar como ela deve se comportar em caso de erro ou gerenciar o atraso após o qual o histórico da campanha orquestrada deve ser removido.

Essas configurações são pré-definidas no template selecionado ao criar a campanha orquestrada, mas podem ser editadas conforme necessário para essa campanha orquestrada específica.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propriedades da campanha orquestrada {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propriedades da campanha orquestrada"
>abstract="Esta seção fornece propriedades de campanha orquestrada genéricas que também estão acessíveis ao criar a campanha orquestrada. Você pode escolher o template a ser usado para criar a campanha orquestrada e especificar um rótulo. Expanda a seção Opções adicionais para definir configurações específicas, como a pasta de armazenamento de campanha orquestrada ou o fuso horário."

A seção **[!UICONTROL Properties]** fornece configurações genéricas que podem ser definidas ao criar uma campanha orquestrada. Para acessar as propriedades de uma campanha orquestrada existente, clique no botão **[!UICONTROL Configurações]** disponível na barra de ações acima da tela de campanha orquestrada.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Essas propriedades são:

* O **[!UICONTROL Label]** da campanha orquestrada que é exibido na lista.
* O **[!UICONTROL Nome interno]** da campanha orquestrada.
* A **[!UICONTROL Pasta]** onde a campanha orquestrada deve ser salva.
* O **[!UICONTROL Fuso horário]** padrão a ser usado em todas as atividades orquestradas da campanha. Por padrão, o fuso horário da campanha orquestrada é aquele definido para o operador atual do Campaign.
Os valores possíveis são:
   * **Fuso horário do servidor** para usar o fuso horário de sua organização da Adobe Experience Platform
   * **Fuso horário do operador** para usar o fuso horário do operador que executa a campanha orquestrada
   * **Fuso horário do banco de dados** para usar o fuso horário do servidor de banco de dados
   * Um fuso horário específico
* Quando uma campanha orquestrada falha, os operadores pertencentes ao grupo de operadores selecionado no campo **[!UICONTROL Supervisor(es)]** são notificados por email.
* Você também pode inserir uma **[!UICONTROL Descrição]** da sua campanha orquestrada.

## Configurações de segmentação  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configurações de segmentação"
>abstract="Nesta seção, você pode selecionar o targeting dimension para direcionar perfis na campanha orquestrada e escolher manter os resultados do fluxo de trabalho entre duas execuções. Essa opção deve ser usada somente para fins de teste e nunca deve ser ativada em uma campanha orquestrada de produção."

* **[!UICONTROL Targeting dimension]**: selecione a targeting dimension a ser usada para direcionar perfis: recipients, beneficiários de contrato, operadores, assinantes, etc.

* **[!UICONTROL Manter o resultado de populações interinas entre duas execuções]**: por padrão, somente as tabelas de trabalho da última execução da campanha orquestrada são mantidas. As tabelas de trabalho das execuções anteriores são removidas por uma campanha técnica orquestrada, executada diariamente.

  Se essa opção estiver ativada, as tabelas de trabalho serão mantidas mesmo após a execução da campanha orquestrada. Você pode usá-lo para fins de teste e, portanto, deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Ele nunca deve ser verificado em uma campanha orquestrada por produção.

## Configurações de execução  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, você pode definir as configurações relacionadas à execução do fluxo de trabalho, como o número de dias em que o histórico da campanha orquestrada é mantido."

* **[!UICONTROL Histórico em dias]**: especifica o número de dias após o qual o histórico deve ser limpo. O histórico contém elementos relacionados à campanha orquestrada: logs, tarefas, eventos (objetos técnicos vinculados à operação da campanha orquestrada). O valor padrão é de 30 dias para modelos de campanha orquestradas prontos para uso. A limpeza do histórico é executada pela campanha orquestrada técnica de limpeza do banco de dados, que é executada diariamente por padrão

  >[!IMPORTANT]
  >
  >Se o campo **[!UICONTROL Histórico em dias]** for deixado em branco, o valor “1” será considerado, o que significa que o histórico será removido após 1 dia.

* **[!UICONTROL Afinidade padrão]**: se a sua instalação incluir vários servidores de campanha orquestrada, use este campo para especificar o servidor no qual a campanha orquestrada será executada. Isso força a execução dessa campanha orquestrada em um servidor específico. Você pode escolher qualquer nome de afinidade existente, mas não use espaços ou sinais de pontuação. Se você usar servidores diferentes, especifique nomes diferentes, separados por vírgulas.

  >[!IMPORTANT]
  >
  >Se o valor definido nesse campo não existir em nenhum servidor, a campanha orquestrada permanecerá pendente.


* **[!UICONTROL Salvar consultas SQL no log]**: marque esta opção para salvar as consultas SQL da campanha de várias etapas do fluxo de trabalho agora nos logs. Essa operação é reservada para usuários avançados. Aplica-se a campanhas orquestradas que contêm atividades de direcionamento como **[!UICONTROL Criar público-alvo]**. Quando essa opção é habilitada, as consultas SQL enviadas ao banco de dados durante a execução da campanha orquestrada são exibidas nos logs da campanha orquestrada, permitindo que você as analise para otimizar as consultas ou diagnosticar problemas.

## Configurações de gerenciamento de erros  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, você pode definir como a campanha orquestrada deve gerenciar erros durante sua execução. Você pode optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da campanha orquestrada."

* **[!UICONTROL Gerenciamento de erros]**: este campo permite que você defina as ações a serem executadas se uma tarefa de campanha orquestrada tiver erros. Há três opções possíveis:

   * **[!UICONTROL Suspender o processo]**: a campanha orquestrada é pausada automaticamente e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, retome a campanha orquestrada usando os botões **[!UICONTROL Retomar]**.
   * **[!UICONTROL Ignore]**: o status da tarefa que provocou o erro muda para **[!UICONTROL Failed]**, mas a campanha orquestrada mantém o status **[!UICONTROL Started]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular o processo]**: a campanha orquestrada é automaticamente interrompida e seu status muda para **[!UICONTROL Failed]**. Quando o problema for resolvido, reinicie a campanha orquestrada usando os botões **[!UICONTROL Start]**.

* **[!UICONTROL Erros consecutivos]**: este campo fica disponível quando o valor **[!UICONTROL Ignorar]** é selecionado no campo **[!UICONTROL Em caso de erros]**. Você pode especificar quantos erros podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da campanha orquestrada será alterado para **[!UICONTROL Failed]**. Se o valor desse campo for 0, a campanha orquestrada nunca será interrompida, independentemente do número de erros.


