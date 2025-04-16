---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Update data em suas campanhas orquestradas
description: Saiba como usar a atividade Update data
hide: true
hidefromtoc: true
exl-id: 68e7c929-5f07-4d5a-9831-690e071947f8
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 24%

---

# Atualizar dados {#update-data}

A atividade **Atualizar dados** é uma atividade de **Gerenciamento de Dados**. Ele permite executar uma atualização em massa nos campos no banco de dados. Várias opções permitem personalizar a atualização de dados.

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## Configurar a atividade Update data{#update-data-configuration}

Para configurar a atividade **Atualizar dados**, comece adicionando a atividade à sua campanha orquestrada e defina um rótulo.

![](../assets/workflow-update-data.png)

### Tipo de operação

O campo **Operation type** permite escolher o processo que deve ser executado nos dados no banco de dados:

* **Inserir ou atualizar**: inserir dados ou atualizá-los se os registros já existirem no banco de dados.
* **Inserir**: inserir somente dados. Os registros que já existem não são atualizados. Se os critérios de reconciliação forem definidos, somente os registros não reconciliados serão adicionados.
* **Atualização**: atualiza os dados dos registros que já existem somente no banco de dados.
* **Delete**: excluir dados.

O campo **Batch size** permite selecionar o número de elementos de transição de entrada a serem atualizados. Por exemplo, se o número declarado for 500, os primeiros 500 registros serão atualizados.

### Identificação de registro

Esta seção permite especificar como identificar os registros no banco de dados:

* Se as entradas de dados se relacionam a uma dimensão de direcionamento existente, selecione a opção **Using the targeting dimension** e a selecione no campo **Targeting dimension to update**.
* Você também pode selecionar o **Usando links personalizados** e especificar um ou mais links que habilitarão a identificação dos dados no banco de dados
* Se o tipo de operação selecionado exigir uma atualização, você deverá usar a opção **Usando regras de reconciliação**.

### Campos a serem atualizados

Na seção **Campos a serem atualizados**, adicione os campos nos quais a atualização será aplicada e, se necessário, adicione condições para que essa atualização seja realizada. Para fazer isso, use o campo **Levado em consideração se**. As condições são aplicadas uma após a outra em ordem de lista. Use as setas à direita para alterar a ordem das atualizações. É possível usar o mesmo campo de destino várias vezes.

Você pode vincular campos automaticamente usando o botão **Mapeamento automático**. A vinculação automática detecta campos com o mesmo nome.

Durante um tipo de operação **Inserir ou atualizar**, você pode selecionar individualmente a operação a ser aplicada para cada campo. Para fazer isso, selecione o valor desejado no campo **Operation type**.

### Opções avançadas

As **Opções avançadas** permitem que você especifique opções adicionais para lidar com a atualização de dados, bem como gerenciar duplicatas.

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

As duas últimas opções permitem executar ações específicas:

* **Gerar uma transição de saída**: cria uma transição de saída que será ativada no final da execução. A atualização normalmente sinaliza o fim de uma campanha orquestrada por direcionamento e, portanto, a opção não é ativada por padrão.

* **Gerar uma transição de saída para as rejeições**: cria uma transição de saída contendo registros que não foram processados corretamente após a atualização (por exemplo, se houver uma duplicata). A atualização geralmente marca o fim de uma campanha orquestrada de direcionamento e, portanto, a opção não é ativada por padrão.
