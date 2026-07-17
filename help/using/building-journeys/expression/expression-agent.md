---
solution: Journey Optimizer
product: journey optimizer
title: Gerar expressões com o Assistente de expressão
description: Saiba como usar o Assistente de expressão no Adobe Journey Optimizer para gerar expressões diretamente no editor de expressão avançado do Jornada usando prompts de linguagem natural.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta público" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: 9551133fab06cfa5e056ba98da73dcbf066916fc
workflow-type: tm+mt
source-wordcount: 1090
ht-degree: 2%

---


# Gerar expressões com o Assistente de expressão {#expression-agent}

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta público**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../../rn/releases.md).
>
>Antes de usar o Assistente de Expressão, leia as [Medidas de Proteção e Limitações](../../content-management/gs-generative.md#generative-guardrails) relacionadas que se aplicam aos recursos de IA gerativa no Journey Optimizer.

O Assistente de expressão é um recurso alimentado por IA integrado ao editor de expressão avançado do Jornada. Ajuda a gerar expressões válidas a partir de prompts de linguagem simples.

Ela está disponível onde quer que o **[!UICONTROL editor de expressão avançado]** da Jornada seja aberto. Por exemplo, ao configurar condições e roteamento dentro de uma **[atividade de Otimização](../optimize.md)** ou ao configurar uma [**[!UICONTROL atividade de Espera ]**](../wait-activity.md) que usa uma data personalizada e você precisa de uma expressão `dateTimeOnly`.

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica o Assistente de Expressão, um recurso habilitado para IA no editor de expressão avançado de Jornada que gera expressões de jornada válidas a partir de prompts de linguagem simples.

**Intenções:**

* Gerar uma expressão de jornada a partir de uma descrição em linguagem natural usando o Assistente de Expressão
* Aplique uma expressão gerada diretamente no editor de expressão avançado com o botão Aplicar
* Use o Assistente de expressão dentro de Atividades de otimização, Atividades de condição e Atividades de espera com data personalizada
* Forneça exemplos de solicitações para condições baseadas em eventos e `dateTimeOnly` expressões de espera
* Solucionar problemas de geração com falha, revisando os prompts para fazer referência a nomes de campos e fontes de dados válidos

**Glossário:**

* **Assistente de Expressão**: um recurso generativo habilitado por IA incorporado no editor de expressão avançada do Jornada que converte prompts de linguagem simples em expressões de jornada válidas *(específico do produto)*
* **Editor de expressão avançado**: a interface Journey Optimizer para gravar expressões complexas em condições, atividades Wait e mapeamento de parâmetros de ação *(específico do produto)*
* **dateTimeOnly**: um tipo de expressão date-time sem fuso horário, necessário para atividades Wait de data personalizada *(específico do produto)*
* **Atividade de otimização**: uma atividade de jornada que oferece suporte a condições de ramificação configuráveis por meio do editor de expressão avançado *(específico do produto)*

**Medidas de Proteção:**

* O Assistente de Expressão está atualmente em **beta público** — a disponibilidade e o comportamento podem mudar
* As medidas de proteção e limitações da IA geradora da documentação principal do Assistente de IA se aplicam a este recurso
* Se o assistente referenciar campos que não estão presentes nas fontes de dados da sua jornada, retornará um erro: revise o prompt para usar os nomes de campo disponíveis
* A sintaxe de expressão gerada exata depende dos campos e atividades configurados em sua jornada específica

**Terminologia:**

* Nome canônico: Assistente de expressão — Acrônimo: none — variantes: IA de expressão, gerador de expressão de jornada
* Sinônimos: &quot;Assistente de expressão&quot; = &quot;Gerador de expressão de IA&quot;
* Não confunda: Assistente de expressão (gerador alimentado por IA) ≠ Editor de expressão avançado (o próprio editor de código manual)

**Perguntas frequentes:**

* **P: Onde está disponível o Assistente de Expressão?** — Estará disponível onde o editor de expressão avançado de Jornada for aberto, incluindo atividades de Condição, atividades de Otimização e atividades de Espera com uma data personalizada.
* **P: O que acontece se o assistente não puder gerar uma expressão válida?** — Uma mensagem de erro é exibida; você deve revisar seu prompt para usar nomes de campos e fontes de dados existentes na configuração do jornada.
* **P: Como inserir uma expressão gerada no editor?** — Clique no botão **Aplicar** no painel assistente para inseri-lo diretamente na posição atual do cursor no editor de expressão avançado.
* **P: O Assistente de Expressão pode gerar `dateTimeOnly` expressões para atividades de Espera?** — Sim; por exemplo, solicitar &quot;daqui a 30 dias às 22h como somente data e hora&quot; gera a expressão `dateTimeOnly` apropriada.
* **P: O Assistente de Expressão está disponível?** — Não; atualmente está em beta público. Verifique a página do ciclo de lançamento do Journey Optimizer para obter atualizações de disponibilidade.

+++
