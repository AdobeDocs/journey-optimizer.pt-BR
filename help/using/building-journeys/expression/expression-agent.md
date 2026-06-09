---
solution: Journey Optimizer
product: journey optimizer
title: Gerar expressões com o Assistente de expressão
description: Saiba como usar o Assistente de expressão no Adobe Journey Optimizer para gerar expressões diretamente no editor de expressão avançado do Jornada usando prompts de linguagem natural.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Beta público" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: d90f0ac22c107a51967316f078f359f067b70431
workflow-type: tm+mt
source-wordcount: 661
ht-degree: 10%

---


# Gerar expressões com o Assistente de expressão {#expression-agent}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="Gerar expressões com o Assistente de expressão"
>abstract="O Assistente de expressão usa a IA generativa para ajudar você a criar e gerar expressões diretamente no Editor de expressão avançado da jornada. Por exemplo, em condições, atividades de **Otimização** ou atividades de **Espera** que usam uma data personalizada. Quando você descreve o que precisa em linguagem simples, o assistente gera a expressão correspondente para você."

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta público**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../../rn/releases.md).
>
>Antes de usar o Assistente de Expressão, leia as [Medidas de Proteção e Limitações](../../content-management/gs-generative.md#generative-guardrails) relacionadas que se aplicam aos recursos de IA gerativa no Journey Optimizer.

O Assistente de expressão é um recurso alimentado por IA integrado ao editor de expressão avançado do Jornada. Ajuda a gerar expressões válidas a partir de prompts de linguagem simples.

Ela está disponível onde quer que o **[!UICONTROL editor de expressão avançado]** da Jornada seja aberto. Por exemplo, ao configurar condições e roteamento dentro de uma **[atividade de Otimização](../optimize.md)** ou ao configurar uma [**[!UICONTROL atividade de Espera &#x200B;]**](../wait-activity.md) que usa uma data personalizada e você precisa de uma expressão `dateTimeOnly`.

## Gerar uma expressão {#generate}

Para gerar uma expressão usando o Assistente de Expressão:

1. Abra o **[!UICONTROL editor de expressão avançado]** na sua jornada, por exemplo, de uma condição de ramificação, uma atividade **[!UICONTROL Otimizar]** ou uma atividade **[!UICONTROL Aguardar]** com uma data personalizada.

   ![](../assets/expression-assistant-pane.png)

1. No campo de texto, descreva a expressão que deseja gerar em linguagem simples. Por exemplo:

   * *&quot;Usuários dos EUA com mais de 18 anos&quot;*
   * *&quot;Clientes que fizeram uma compra nos últimos 30 dias&quot;*

   Consulte [Exemplos de prompts](#example-prompts) no final desta página para ver ideias.

1. Clique em **[!UICONTROL Gerar]** para enviar seu prompt.

   O assistente começa a gerar a expressão correspondente e exibe mensagens de status de progresso enquanto a geração está em andamento.

   >[!NOTE]
   >
   >Se o assistente não puder gerar uma expressão válida (por exemplo, se o prompt fizer referência a campos que não existem nas fontes de dados disponíveis), uma mensagem de erro será exibida. Quando isso acontecer, revise o prompt para usar nomes de campo e fontes de dados disponíveis na configuração do jornada e gere novamente.

1. Quando a expressão estiver pronta, revise o resultado no painel.

   ![](../assets/expression-assistant-result.png)

   * Clique no ícone ![Visualizar](../assets/do-not-localize/generation-preview.svg) antes de aplicar para revisar a saída do assistente para o cenário solicitado.

   * Clique em **[!UICONTROL Aplicar]** para inserir a expressão gerada diretamente no editor de expressão avançado (o mesmo posicionamento no qual você colaria manualmente).
   * Use o controle de cópia para coletar o texto de expressão sugerido e colá-lo em outro lugar, se necessário.

## Exemplo de prompts {#example-prompts}

As listas abaixo são apenas ideias de prompt. Eles não mostram a sintaxe de expressão gerada, a saída exata depende dos campos e atividades definidas na jornada.

### Jornada evento e ação personalizada {#example-prompts-event-action}

* *&quot;evento com preço total do pedido maior que 100&quot;*
* *&quot;evento em que o pedido foi criado nos últimos 7 dias&quot;*
* *&quot;evento em que o tipo de evento é uma compra comercial&quot;*
* *&quot;evento com pedido criado na última hora&quot;*
* *&quot;evento com preço total do pedido acima de 200 e resposta da ação com código de status&quot;*

### Expressões de atividade de espera {#example-prompts-datetime}

Quando uma atividade **[!UICONTROL Wait]** usa uma data personalizada, você define quando o perfil continua criando uma expressão `dateTimeOnly` no **[!UICONTROL Editor de expressão avançado]**. Por exemplo, de um atributo de perfil, um carimbo de data e hora de evento, dados de qualificação de segmento ou um deslocamento calculado em relação à hora atual. Para saber como configurar esperas personalizadas e limites aplicáveis, consulte [Espera personalizada](../wait-activity.md#custom).

* *&quot;usar a última data de pedido do cliente como data e hora apenas&quot;*
* *&quot;usar hora do email de consentimento somente como data e hora&quot;*
* *&quot;converter somente o horário da última qualificação de associação de segmento em data e hora&quot;*
* *&quot;nó de espera: uma semana após o Natal de 2024 somente como data e hora&quot;*
* *&quot;nó de espera: daqui a 30 dias às 22h como somente data e hora&quot;*
* *&quot;aguarde até as 9h de hoje no fuso horário UTC, retorne somente como data e hora&quot;*

## Recursos relacionados {#related}

* [Trabalhar com o editor de expressão avançado](expressionadvanced.md) — Visão geral da interface do editor de expressão e sintaxe com suporte.
* [Introdução ao Assistente de IA no Journey Optimizer](../../content-management/gs-generative.md) — Medidas de proteção gerais, acesso e configuração para recursos de IA generativa.
