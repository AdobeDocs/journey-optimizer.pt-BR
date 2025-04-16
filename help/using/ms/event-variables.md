---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com variáveis de evento em campanhas orquestradas
description: Saiba como aproveitar variáveis de evento em campanhas orquestradas
hide: true
hidefromtoc: true
exl-id: f86dd262-0209-42f6-a180-736f1de98d78
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 18%

---

# Trabalhar com variáveis de evento {#event-variables}

Algumas atividades de campanha orquestradas permitem editar scripts no editor de expressão para executar ações específicas, como recuperar dados provenientes de atividades anteriores, condições de criação ou computar nomes de arquivo com base em variáveis de evento.

## O que são variáveis de evento {#scripting}

Os scripts executados no contexto de uma campanha orquestrada acessam uma série de **objetos** globais adicionais, como a própria campanha orquestrada que está sendo executada (`ìnstance`), suas várias tarefas (`task`) ou os eventos que ativaram uma determinada tarefa (`event`).

A cada tipo de **objeto** está associada uma categoria de **variáveis** que podem ser aproveitadas no editor de expressão ao editar scripts em atividades como **[!UICONTROL código JavaScript]** ou **[!UICONTROL Teste]**.

* **As variáveis de instância** (`instance.vars.xxx`) são comparáveis às variáveis globais. Eles são compartilhados por todas as atividades.
* **As variáveis de tarefa** (`task.vars.xxx`) são comparáveis com as variáveis locais. São utilizadas somente pela tarefa atual. Essas variáveis são utilizadas por atividades persistentes para manter os dados e, às vezes, são utilizadas para troca de dados entre os diferentes scripts de uma mesma atividade.
* **As variáveis de evento** (`vars.xxx`) habilitam a troca de dados entre as tarefas primárias de um processo de campanha orquestrada. Essas variáveis são passadas pela tarefa que ativou a tarefa em andamento. Eles são passados para as atividades seguintes. **As variáveis de evento** são as variáveis usadas com mais frequência e devem ser usadas em detrimento de variáveis de instância.

## Aproveitar variáveis de evento no editor de expressão {#expression-editor}

As variáveis de evento predefinidas estão disponíveis para uso no painel do lado esquerdo do editor de expressão. Você também pode criar novas variáveis inicializando uma nova variável no código.

![](assets/event-variables.png)

Além dessas variáveis de evento, você também pode aproveitar o menu **[!UICONTROL Condições]** no painel esquerdo para criar condições e o menu **[!UICONTROL Adicionar data atual]** para usar funções relacionadas à formatação de data.
