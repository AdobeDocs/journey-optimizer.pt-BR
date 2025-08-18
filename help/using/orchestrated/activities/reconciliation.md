---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação em uma campanha orquestrada
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 87%

---


# Reconciliação {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A Atividade **reconciliação** é uma atividade de **direcionamento** que permite definir o vínculo entre o Adobe Journey Optimizer e os dados em uma tabela de trabalho."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Campo de seleção de reconciliação"
>abstract="Campo de seleção de reconciliação"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condição de criação de reconciliação"
>abstract="Condição de criação de reconciliação"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complemento de geração de reconciliação"
>abstract="Complemento de geração de reconciliação"

A atividade **[!UICONTROL Reconciliação]** é uma atividade de **[!UICONTROL Direcionamento]** que permite definir o vínculo entre os dados do banco de dados do Adobe Journey Optimizer e os dados de uma tabela de trabalho, como, por exemplo, dados carregados de um arquivo externo. 

A atividade **[!UICONTROL Enrichment]** permite adicionar dados adicionais à campanha orquestrada, por exemplo, combinando dados de várias fontes ou vinculando a um recurso temporário. Em contraste, a atividade **[!UICONTROL Reconciliação]** é usada para corresponder dados não identificados ou externos a recursos existentes no banco de dados.

A **[!UICONTROL Reconciliação]** exige que os registros relacionados já existam no sistema. Por exemplo, se você importar um arquivo de compra listando produtos, carimbos de data/hora e informações dos clientes, os produtos e os clientes já precisam estar presentes no banco de dados para estabelecer o vínculo.

## Configurar a atividade de reconciliação {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimensão de direcionamento"
>abstract="Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, a dimensão de direcionamento atual é selecionada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar a sua própria condição de reconciliação com o construtor de regras, selecione a opção **Condições de reconciliação avançadas**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Selecione a dimensão de direcionamento"
>abstract="Selecione a dimensão de direcionamento com a qual seus dados de entrada devem se reconciliar."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=pt-BR#targeting-dimensions" text="Dimensões de direcionamento"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Manter dados não reconciliados"
>abstract="Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Atributo de reconciliação"
>abstract="Selecione o atributo a ser usado para reconciliar dados e clique em Confirmar."

Siga estas etapas para configurar a atividade **[!UICONTROL Reconciliação]**:

1. Adicione uma atividade de **[!UICONTROL Reconciliação]** à tela.

1. Escolha uma nova dimensão de direcionamento para definir a quem você está direcionando, como destinatários ou assinantes.

1. Defina os campos a serem usados para corresponder os seus dados de entrada a perfis existentes.

1. Para corresponder os dados por meio de campos básicos, selecione **[!UICONTROL Atributos simples]**.

1. Defina os campos de correspondência:

   * **[!UICONTROL Origem]**: lista os campos dos dados de entrada.

   * **[!UICONTROL Destino]**: refere-se aos campos na dimensão de direcionamento selecionada.

   Uma correspondência ocorre quando ambos os valores são iguais, como, por exemplo, quando o **[!UICONTROL Email]** corresponde ao identificar perfis.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Para adicionar mais regras de correspondência, clique em **[!UICONTROL Adicionar regra]**. Para que uma correspondência ocorra, todas as condições precisam ser satisfeitas.

1. Para condições mais complexas, escolha **[!UICONTROL Condições de reconciliação avançadas]**. Use o [construtor de regras](../orchestrated-rule-builder.md) para definir uma lógica personalizada.

1. Para filtrar quais dados reconciliar, clique em **[!UICONTROL Criar filtro]** e defina sua condição no construtor de regras.

1. Por padrão, registros sem correspondência são mantidos na transição de saída e armazenados na tabela de trabalho. Para removê-los, habilite a opção **[!UICONTROL Manter dados não reconciliados]**.

## Exemplo {#example-reconciliation}

Este exemplo usa a atividade **[!UICONTROL Reconciliação]** no Adobe Journey Optimizer para garantir que os emails sejam enviados somente a clientes reconhecidos. Os dados fluem por meio de uma atividade **[!UICONTROL Público-alvo de leitura]** direcionada a usuários com pedidos anteriores. Então, a atividade **[!UICONTROL Reconciliação]** corresponde esses dados de entrada aos perfis existentes no banco de dados, usando o campo de email.

![](../assets/workflow-reconciliation-sample-1.0.png)
