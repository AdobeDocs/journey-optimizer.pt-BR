---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação em uma campanha orquestrada
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 39%

---

# Reconciliação {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A atividade **Reconciliation** é uma atividade **Targeting** que permite definir o vínculo entre o Adobe Journey Optimizer e os dados em uma tabela de trabalho."

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

A atividade **Reconciliation** é uma atividade **Targeting** que permite definir o vínculo entre os dados no Adobe Journey Optimizer e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.

## Práticas recomendadas {#reconciliation-best-practices}

Embora a atividade **Enrichment** permita a definição de dados adicionais para serem processados na campanha orquestrada (você pode usar uma atividade **Enrichment** para combinar dados provenientes de vários conjuntos ou para criar links para um recurso temporário), a atividade **Reconciliation** permite vincular dados não identificados aos recursos existentes.

>[!NOTE]
>A operação de reconciliação implica que os dados das dimensões vinculadas já estão no banco de dados.  Por exemplo, se você importar um arquivo de compras que mostre qual produto foi comprado, em que momento, por qual cliente, etc., o produto e o cliente já deverão existir no banco de dados.

## Configurar a atividade de reconciliação {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimensão de direcionamento"
>abstract="Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, a dimensão de direcionamento atual é selecionada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar sua própria condição de reconciliação usando o modelador de consultas, selecione a opção **Condições de reconciliação avançadas**."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/campaign-web/v8/query-database/query-modeler-overview" text="Trabalhar com o modelador de consultas"

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

Siga estas etapas para configurar a atividade **Reconciliação**:

1. Adicione uma atividade de **Reconciliação** à campanha orquestrada.

1. Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: recipients, assinantes de aplicativos, operadores, assinantes, etc.

1. Selecione os campos a serem usados para a reconciliação. É possível usar um ou mais critérios de reconciliação.

   1. Para usar atributos para reconciliar dados, selecione a opção **Atributos simples**. O campo **Source** lista os campos disponíveis na transição de entrada, que devem ser reconciliados. O campo **Destination** corresponde aos campos da targeting dimension selecionada. Os dados são reconciliados quando a origem e o destino são iguais. Por exemplo, selecione os campos **Email** para desduplicar perfis com base em seus endereços de email.

      Para adicionar outro critério de reconciliação, clique no botão **Adicionar regra**. Se várias condições de associação forem especificadas, TODAS elas deverão ser verificadas para que os dados possam ser vinculados.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Para usar outros atributos para reconciliar dados, selecione a opção **Condições avançadas de reconciliação**. Em seguida, você pode criar sua própria condição de reconciliação usando o modelador de consultas.

1. Você pode filtrar dados para reconciliar usando o botão **Criar filtro**. Isso permite criar uma condição personalizada usando o modelador de consultas.

Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**.

## Exemplo {#reconciliation-example}

O exemplo a seguir demonstra uma campanha orquestrada que cria um público-alvo de perfis diretamente de um arquivo importado que contém novos clientes. Ele é composto pelas seguintes atividades:

A campanha orquestrada foi projetada da seguinte maneira:

![](../assets/workflow-reconciliation-sample-1.0.png)


Ele é criado com as seguintes atividades:

* Uma atividade [Load file](load-file.md) faz upload de um arquivo contendo dados de perfis que foram extraídos de uma ferramenta externa.

  Por exemplo:

  ```
  lastname;firstname;email;birthdate;
  JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
  PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
  WEAVER;Justin;justin_w@testmail.com;11/15/1990;
  MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
  REESE;Richard;rreese@testmail.com;02/08/1987;
  ```

* Uma atividade de **Reconciliação** que identifica os dados recebidos como perfis usando os campos **email** e **Data de nascimento** como critérios de reconciliação.

  ![](../assets/workflow-reconciliation-sample-1.1.png)

* Uma atividade [Save audience](save-audience.md) para criar um novo público-alvo com base nessas atualizações. Você também pode substituir a atividade **Salvar público-alvo** por uma atividade **Fim** se nenhum público-alvo específico precisar ser criado ou atualizado. Os perfis de recipient são atualizados em qualquer caso quando você executa a campanha orquestrada.
