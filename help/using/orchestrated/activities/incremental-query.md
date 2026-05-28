---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Query incremental
description: Saiba como usar a atividade Query incremental no Adobe Journey Optimizer para direcionar somente novos perfis em campanhas orquestradas.
feature: Campaigns
topic: Building campaigns
role: User
level: Intermediate
version: Campaign Orchestration
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 518
ht-degree: 22%

---


# Consulta incremental {#incremental-query}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery"
>title="Consulta incremental"
>abstract="O Query incremental é uma atividade de direcionamento que executa um query de banco de dados sempre que a campanha orquestrada é executada. Retorna apenas novos registros e exclui qualquer pessoa já incluída em uma execução anterior, de modo a evitar o redirecionamento das mesmas pessoas ou a reexportação das mesmas linhas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_processeddata"
>title="Dados processados"
>abstract="Em Dados processados, escolha como excluir registros de execuções anteriores. Com a opção Use a date field, a atividade usa um campo de data selecionado em vez de rastrear IDs individuais e cada execução retorna somente linhas cuja data seja após a última execução."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_history"
>title="Histórico em dias"
>abstract="Essa configuração controla por quanto tempo essa lista é retida. Um valor de 0 significa retenção indefinida. Nenhum registro é removido."

A atividade de **[!UICONTROL Consulta incremental]** é uma atividade de **[!UICONTROL Direcionamento]** que executa uma consulta de banco de dados sempre que a campanha Orquestrada é executada. O importante é que ele só gera **novos** registros. Qualquer pessoa já selecionada em uma execução anterior é excluída, portanto, evite redirecionar as mesmas pessoas ou reexportar as mesmas linhas.

Use-a quando a campanha puder ser executada várias vezes, por exemplo, ao agendar a campanha, por exemplo, semanalmente ou quando for acionada por um sinal externo ou uma API. Cada execução direciona somente registros que não foram retornados em uma execução anterior, de modo que você evite duplicatas.

Utilizações típicas:

* **Mensagens e públicos-alvo**: obtenha somente novas inscrições, novos compradores ou outros segmentos &quot;novos desde a última execução&quot; para a próxima etapa (por exemplo, email, SMS).
* **Exportações em andamento**: envie somente linhas novas ou atualizadas para arquivos para ferramentas de BI ou relatório, sem duplicar o que você já exportou.

Quando uma execução não retorna nenhuma linha, a campanha Orquestrada é interrompida na **Consulta incremental**. As atividades após o Query incremental não são executadas até que haja dados, quando a campanha é executada novamente.

## Configurar a atividade de query incremental {#incremental-query-configuration}

Defina o targeting dimension, crie seu query e escolha como a atividade decide quais registros serão excluídos de execuções futuras.

1. Solte uma atividade de **[!UICONTROL Consulta incremental]** na sua campanha Orquestrada.

1. Em **[!UICONTROL Audience]**, escolha a **[!UICONTROL Targeting dimension]**, por exemplo, recipients, assinantes e clique em **[!UICONTROL Continue]**. Saiba mais sobre [Targeting dimensions](../target-dimension.md).

   ![](../assets/incremental-query.png)

1. Clique em **[!UICONTROL Adicionar condição]** para definir a consulta. [Saiba como usar o construtor de regras](../orchestrated-rule-builder.md).

   ![](../assets/incremental-query-2.png)

1. Em **[!UICONTROL Dados processados]**, escolha o **[!UICONTROL Caminho para o campo de data]**. O atributo deve usar o formato **Data e hora**. Cada execução retorna somente linhas cuja data seja posterior à última execução.

   ![Configuração de atividade de consulta incremental na tela de campanha orquestrada](../assets/incremental-query-3.png)

<!--
   * **[!UICONTROL Exclude results of previous execution]**: The activity maintains a list of records returned in prior runs. Each run excludes those records and returns only new ones. **[!UICONTROL History in days]** controls the retention period for that list. 0 indicates indefinite retention, no records are removed.

   >[!IMPORTANT]
   >
   >This mode stores the primary key of each processed record. Personally identifiable information (PII) must not be used as the primary key.

-->

## Exemplo {#incremental-query-example}

O exemplo a seguir envia um email de boas-vindas para perfis que acabaram de se tornar membros gold. A campanha pode ser agendada para ser executada semanalmente, às segundas-feiras. Cada execução direciona somente os perfis qualificados para associação gold desde a execução anterior, para que cada recipient receba o email de boas-vindas uma vez.

* **[!UICONTROL Consulta incremental]**: seleciona membros gold. Primeira execução: todos os membros gold atuais. Execuções posteriores: somente perfis que se tornaram membros gold desde a execução anterior.
* **[!UICONTROL Entrega de email]**: envia o email de boas-vindas para os perfis gerados pela consulta.

![Configuração de atividade de consulta incremental na tela de campanha orquestrada](../assets/incremental-query-example.png)

