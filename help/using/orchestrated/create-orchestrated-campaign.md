---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas orquestradas com o Journey Optimizer
description: Saiba como criar uma campanha orquestrada com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '1739'
ht-degree: 21%

---


# Criar uma campanha orquestrada {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campanhas orquestradas"
>abstract="A guia **várias etapas** lista todas as campanhas orquestradas. Clique no nome de uma campanha orquestrada para editá-la. Use o botão **Criar campanha orquestrada** para adicionar uma nova campanha orquestrada. "

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/><b>[Criar e configurar a campanha](create-orchestrated-campaign.md)</b><br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Criar a campanha {#create}

Para criar uma campanha orquestrada, siga estas etapas:

1. Para criar uma **campanha orquestrada**, navegue até o menu **Campanhas**.

1. Clique no botão **[!UICONTROL Criar campanha orquestrada]**, no canto superior direito da tela.

1. Na caixa de diálogo **Propriedades** da campanha orquestrada, selecione o modelo a ser usado para criar a campanha orquestrada (você também pode usar o modelo interno padrão). [Saiba mais sobre modelos de campanha orquestradas](#campaign-templates).

1. Insira um rótulo para a campanha orquestrada. Além disso, recomendamos que você adicione uma descrição à sua campanha orquestrada, no campo dedicado da seção **[!UICONTROL Opções adicionais]** da tela.

1. Expanda a seção **[!UICONTROL Opções adicionais]** para definir mais configurações para a campanha orquestrada.

1. Clique no botão **[!UICONTROL Criar campanha orquestrada]** para confirmar a criação da campanha orquestrada.

Sua campanha orquestrada agora está criada e disponível na lista de workflows. Agora é possível acessar a tela visual e começar a adicionar, configurar e orquestrar as tarefas que serão executadas. [Saiba como organizar atividades de campanha orquestradas](orchestrate-activities.md).

## Definir as configurações da campanha {#settings}

<!--Overview of new admin settings> schemas, execution fields, merge policy. [Learn more](configuration-steps.md)-->

Ao criar uma campanha orquestrada ou orquestrar atividades de campanha orquestrada na tela, você pode acessar configurações avançadas relacionadas à campanha orquestrada. Por exemplo, é possível definir um fuso horário específico para a campanha orquestrada, gerenciar como ela deve se comportar em caso de erro ou gerenciar o atraso após o qual o histórico da campanha orquestrada deve ser removido.

Essas configurações são pré-definidas no template selecionado ao criar a campanha orquestrada, mas podem ser editadas conforme necessário para essa campanha orquestrada específica.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

### Propriedades da campanha orquestrada {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propriedades da campanha orquestrada"
>abstract="Esta seção fornece propriedades genéricas da campanha orquestrada que também podem ser acessadas ao criá-la. É possível escolher o modelo a ser usado para criar a campanha orquestrada e especificar um rótulo. Expanda a seção Opções adicionais para definir configurações específicas, como a pasta de armazenamento da campanha orquestrada ou o fuso horário."

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

### Configurações de segmentação  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configurações de segmentação"
>abstract="Nesta seção, é possível selecionar a dimensão de direcionamento para direcionar perfis na campanha orquestrada e escolher manter os resultados do fluxo de trabalho entre duas execuções. Essa opção deve ser usada somente para fins de teste e nunca deve ser habilitada em uma campanha orquestrada de produção."

* **[!UICONTROL Targeting dimension]**: selecione a targeting dimension a ser usada para direcionar perfis: recipients, beneficiários de contrato, operadores, assinantes, etc.

* **[!UICONTROL Manter o resultado de populações interinas entre duas execuções]**: por padrão, somente as tabelas de trabalho da última execução da campanha orquestrada são mantidas. As tabelas de trabalho das execuções anteriores são removidas por uma campanha técnica orquestrada, executada diariamente.

  Se essa opção estiver ativada, as tabelas de trabalho serão mantidas mesmo após a execução da campanha orquestrada. Você pode usá-lo para fins de teste e, portanto, deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Ele nunca deve ser verificado em uma campanha orquestrada por produção.

### Configurações de execução  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, é possível definir configurações relacionadas à execução do fluxo de trabalho, como o número de dias no qual o histórico da campanha orquestrada será mantido."

* **[!UICONTROL Histórico em dias]**: especifica o número de dias após o qual o histórico deve ser limpo. O histórico contém elementos relacionados à campanha orquestrada: logs, tarefas, eventos (objetos técnicos vinculados à operação da campanha orquestrada). O valor padrão é de 30 dias para modelos de campanha orquestradas prontos para uso. A limpeza do histórico é executada pela campanha orquestrada técnica de limpeza do banco de dados, que é executada diariamente por padrão

  >[!IMPORTANT]
  >
  >Se o campo **[!UICONTROL Histórico em dias]** for deixado em branco, o valor “1” será considerado, o que significa que o histórico será removido após 1 dia.

* **[!UICONTROL Afinidade padrão]**: se a sua instalação incluir vários servidores de campanha orquestrada, use este campo para especificar o servidor no qual a campanha orquestrada será executada. Isso força a execução dessa campanha orquestrada em um servidor específico. Você pode escolher qualquer nome de afinidade existente, mas não use espaços ou sinais de pontuação. Se você usar servidores diferentes, especifique nomes diferentes, separados por vírgulas.

  >[!IMPORTANT]
  >
  >Se o valor definido nesse campo não existir em nenhum servidor, a campanha orquestrada permanecerá pendente.


* **[!UICONTROL Salvar consultas SQL no log]**: marque esta opção para salvar as consultas SQL da campanha de várias etapas do fluxo de trabalho agora nos logs. Essa operação é reservada para usuários avançados. Aplica-se a campanhas orquestradas que contêm atividades de direcionamento como **[!UICONTROL Criar público-alvo]**. Quando essa opção é habilitada, as consultas SQL enviadas ao banco de dados durante a execução da campanha orquestrada são exibidas nos logs da campanha orquestrada, permitindo que você as analise para otimizar as consultas ou diagnosticar problemas.

### Configurações de gerenciamento de erros  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, é possível definir como a campanha orquestrada deve gerenciar erros durante sua execução. É possível optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da campanha orquestrada."

* **[!UICONTROL Gerenciamento de erros]**: este campo permite que você defina as ações a serem executadas se uma tarefa de campanha orquestrada tiver erros. Há três opções possíveis:

   * **[!UICONTROL Suspender o processo]**: a campanha orquestrada é pausada automaticamente e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, retome a campanha orquestrada usando os botões **[!UICONTROL Retomar]**.
   * **[!UICONTROL Ignore]**: o status da tarefa que provocou o erro muda para **[!UICONTROL Failed]**, mas a campanha orquestrada mantém o status **[!UICONTROL Started]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular o processo]**: a campanha orquestrada é automaticamente interrompida e seu status muda para **[!UICONTROL Failed]**. Quando o problema for resolvido, reinicie a campanha orquestrada usando os botões **[!UICONTROL Start]**.

* **[!UICONTROL Erros consecutivos]**: este campo fica disponível quando o valor **[!UICONTROL Ignorar]** é selecionado no campo **[!UICONTROL Em caso de erros]**. Você pode especificar quantos erros podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da campanha orquestrada será alterado para **[!UICONTROL Failed]**. Se o valor desse campo for 0, a campanha orquestrada nunca será interrompida, independentemente do número de erros.

## Trabalhar com modelos de campanha orquestrada {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modelos de campanha orquestrada"
>abstract="Os modelos de campanha orquestrada contêm configurações e atividades predefinidas que podem ser reutilizadas para criar novas campanhas orquestradas."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propriedades da campanha orquestrada"
>abstract="Os modelos de campanha orquestrada contêm configurações e atividades predefinidas que podem ser reutilizadas para criar novas campanhas orquestradas. Nessa tela, insira o rótulo do modelo da campanha orquestrada e defina suas configurações, como nome interno, pasta, pastas de execução, fuso horário e grupo de supervisão."

Os modelos de campanha orquestrada contêm configurações e atividades predefinidas que podem ser reutilizadas para criar novas campanhas orquestradas. Você pode selecionar o template da sua campanha orquestrada nas propriedades da campanha orquestrada, ao criar uma campanha orquestrada. Um template vazio é fornecido por padrão.

Você pode criar um modelo a partir de uma campanha orquestrada existente ou criar um novo modelo do zero. Ambos os métodos são detalhados abaixo.

>[!BEGINTABS]

>[!TAB Criar um modelo a partir de uma campanha orquestrada existente]

Para criar um template de campanha orquestrada a partir de uma campanha orquestrada existente, siga estas etapas:

1. Abra o menu **Campanha** e navegue até a campanha orquestrada para salvar como um modelo.
1. Clique nos três pontos à direita do nome da campanha orquestrada e escolha **Copiar como modelo**.
1. Na janela pop-up, confirme a criação do template.
1. Na tela do template de campanha orquestrada, verifique, adicione e configure as atividades conforme necessário.
1. Navegue até as configurações, no botão **Configurações**, para alterar o nome do modelo de campanha orquestrada e insira uma descrição.
1. Selecione a **pasta** e a **pasta de execução** do modelo. A pasta é o local onde o template de campanha orquestrada é salvo. A pasta de execução é a pasta onde as campanhas orquestradas criadas com base nesse template são salvas.
1. Salve as alterações.

O template de campanha orquestrada agora está disponível na lista de templates. Você pode criar uma campanha orquestrada com base nesse template. Essa campanha orquestrada será pré-configurada com as configurações e atividades definidas no template.


>[!TAB Criar um modelo do zero]


Para criar um template de campanha orquestrado do zero, siga estas etapas:

1. Abra o menu **Campanha** e navegue até a guia **Modelos**. Você pode ver a lista de templates de campanha orquestrada disponíveis.
1. Clique no botão **[!UICONTROL Criar modelo]** no canto superior direito da tela.
1. Insira o rótulo e abra as opções adicionais para inserir uma descrição do template de campanha orquestrada.
1. Selecione a pasta e a pasta de execução do modelo. A pasta é o local onde o template de campanha orquestrada é salvo. A pasta de execução é a pasta onde as campanhas orquestradas criadas com base nesse template são salvas.
1. Clique no botão **Criar** para confirmar suas configurações.
1. Na tela do template de campanha orquestrada, adicione e configure as atividades conforme necessário.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Salve as alterações.

O template de campanha orquestrada agora está disponível na lista de templates. Você pode criar uma campanha orquestrada com base nesse template. Essa campanha orquestrada será pré-configurada com as configurações e atividades definidas no template.

>[!ENDTABS]
