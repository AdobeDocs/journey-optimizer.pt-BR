---
solution: Journey Optimizer
product: journey optimizer
title: Variáveis de evento de campanha em várias etapas
description: Saiba como aproveitar variáveis de evento em campanhas com várias etapas
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 17%

---

# Variáveis de evento de campanha em várias etapas {#event-variables}

Algumas atividades de campanha em várias etapas permitem editar scripts no editor de expressão para executar ações específicas, como recuperar dados provenientes de atividades anteriores, condições de criação ou calcular nomes de arquivos com base em variáveis de evento.

## O que são variáveis de evento {#scripting}

Os scripts executados no contexto de uma campanha em várias etapas acessam uma série de **objetos** globais adicionais, como a própria campanha em várias etapas que está sendo executada (`ìnstance`), suas várias tarefas (`task`) ou os eventos que ativaram uma determinada tarefa (`event`).

A cada tipo de **objeto** está associada uma categoria de **variáveis** que podem ser aproveitadas no editor de expressão ao editar scripts em atividades como **[!UICONTROL código JavaScript]** ou **[!UICONTROL Teste]**.

* **As variáveis de instância** (`instance.vars.xxx`) são comparáveis às variáveis globais. Eles são compartilhados por todas as atividades.
* **As variáveis de tarefa** (`task.vars.xxx`) são comparáveis com as variáveis locais. São utilizadas somente pela tarefa atual. Essas variáveis são utilizadas por atividades persistentes para manter os dados e, às vezes, são utilizadas para troca de dados entre os diferentes scripts de uma mesma atividade.
* **As variáveis de evento** (`vars.xxx`) habilitam a troca de dados entre as tarefas primárias de um processo de campanha de várias etapas. Essas variáveis são passadas pela tarefa que ativou a tarefa em andamento. Eles são passados para as atividades seguintes. **As variáveis de evento** são as variáveis usadas com mais frequência e devem ser usadas em detrimento de variáveis de instância.

## Aproveitar variáveis de evento no editor de expressão {#expression-editor}

As variáveis de evento predefinidas estão disponíveis para uso no painel do lado esquerdo do editor de expressão. Você também pode criar novas variáveis inicializando uma nova variável no código.

![](assets/event-variables.png)

Além dessas variáveis de evento, você também pode aproveitar o menu **[!UICONTROL Condições]** no painel esquerdo para criar condições e o menu **[!UICONTROL Adicionar data atual]** para usar funções relacionadas à formatação de data.
