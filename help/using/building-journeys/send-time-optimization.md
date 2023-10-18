---
solution: Journey Optimizer
product: journey optimizer
title: Otimização do tempo de envio
description: Saiba como definir parâmetros para a otimização de tempo de envio em suas mensagens
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: send-time, send, message, otimization, jornada, AI, Intelligent
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 36%

---

# Otimização de tempo de envio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Sobre a otimização da hora de envio"
>abstract="O recurso Otimização da hora de envio do Adobe Journey Optimizer, desenvolvido pelos serviços de IA da Adobe, pode prever o melhor momento para enviar um email ou uma mensagem por push para maximizar o engajamento com base nas taxas históricas de abertura e clique."

O recurso Otimização da hora de envio do Adobe Journey Optimizer, desenvolvido pelos serviços de IA da Adobe, pode prever o melhor momento para enviar um email ou uma mensagem por push para maximizar o engajamento com base nas taxas históricas de abertura e clique. Use nosso modelo de aprendizado de máquina para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e de clique de suas mensagens.

O modelo de Otimização de tempo de envio assimila os dados do Adobe Journey Optimizer e observa as taxas de abertura (para email e push) e de clique (para email) no nível do usuário para determinar quando seus clientes têm maior probabilidade de interagir com suas mensagens. A Otimização de tempo de envio requer no mínimo um mês de dados de rastreamento de mensagens para fazer recomendações informadas. Para cada usuário, o sistema escolherá automaticamente o melhor momento usando as seguintes pontuações:

* A melhor hora de cada dia da semana para maximizar o engajamento
* O melhor dia da semana para maximizar o envolvimento
* A melhor hora do melhor dia da semana para maximizar o engajamento

O modelo varia se você estiver falando sobre pontuação ou treinamento. O treinamento é realizado inicialmente semanalmente e depois trimestralmente. A pontuação é inicialmente semanal e depois mensal.

* Treinamento - o desenvolvimento do algoritmo usado para fazer a pontuação
* Pontuação - a aplicação de uma pontuação a perfis individuais com base no modelo treinado

Essas informações são armazenadas com o perfil do usuário e são referenciadas na execução da jornada para informar ao Adobe Journey Optimizer quando enviar sua mensagem.

## Ativar otimização da hora de envio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Ativar otimização da hora de envio"
>abstract="Escolha se deseja otimizar nas aberturas de email ou em click-throughs de email selecionando o botão de opção apropriado. Você também pode optar por agrupar as horas de envio usadas pelo sistema inserindo um valor para Enviar na próxima opção."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Ativar otimização da hora de envio"
>abstract="O padrão das mensagens por push é a opção de abertura, pois cliques não são aplicáveis para mensagens por push. Você também pode optar por agrupar as horas de envio usadas pelo sistema inserindo um valor para Enviar na próxima opção."

Ative a Otimização de hora de envio em um email ou mensagem por push selecionando o **Otimização de tempo de envio** alterne entre os parâmetros da atividade.

![](../building-journeys/assets/jo-message5.png)

Para mensagens de email, escolha se deseja otimizar as aberturas de email ou click-throughs de email selecionando o botão de opção apropriado. O padrão das mensagens por push é a opção de abertura, pois cliques não são aplicáveis para mensagens por push.

Você também pode optar por colocar entre colchetes os tempos de envio usados pelo sistema inserindo um valor para a variável **Enviar no próximo** opção. Se você escolher &quot;seis horas&quot; como o valor, [!DNL Journey Optimizer] O verificará cada perfil de usuário e escolherá o tempo de envio ideal dentro de seis horas a partir do tempo de execução da jornada.
