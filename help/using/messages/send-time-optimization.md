---
title: Enviar otimização de tempo
description: Saiba como definir parâmetros para a otimização de tempo de envio em suas mensagens
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

## Otimização de tempo de envio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Sobre a otimização de tempo enviado"
>abstract="O recurso de Otimização de tempo de envio da Adobe Journey Optimizer, desenvolvido pelos serviços de IA do Adobe, pode prever o melhor momento para enviar um email ou mensagem de push para maximizar o engajamento com base nas taxas de abertura e cliques do histórico."

O recurso de Otimização de tempo de envio da Adobe Journey Optimizer, desenvolvido pelos serviços de IA do Adobe, pode prever o melhor momento para enviar um email ou mensagem de push para maximizar o engajamento com base nas taxas de abertura e cliques do histórico. Use nosso modelo de aprendizado de máquina para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e cliques de suas mensagens.

O modelo de Otimização de tempo de envio assimila seus dados do Adobe Journey Optimizer e verifica as taxas de abertura no nível do usuário (para email e push) e de clique (para email) para determinar quando os clientes têm maior probabilidade de se envolver com suas mensagens. A otimização de tempo de envio requer no mínimo um mês de dados de rastreamento de mensagem para fazer recomendações informadas. Para cada usuário, o sistema selecionará automaticamente o melhor horário usando as seguintes pontuações:

* A melhor hora de cada dia da semana para maximizar o envolvimento
* O melhor dia da semana para maximizar o envolvimento
* A melhor hora do melhor dia da semana para maximizar o envolvimento

O modelo varia se você estiver falando de pontuação ou treinamento. O treinamento é feito semanalmente, inicialmente e depois trimestralmente. A pontuação é semanal inicialmente e mensal.

* Treinamento - o desenvolvimento do algoritmo usado para fazer a pontuação
* Pontuação - a aplicação de uma pontuação a perfis individuais com base no modelo treinado

Essas informações são armazenadas com o perfil do usuário e são referenciadas na execução do jornada para informar ao Adobe Journey Optimizer quando enviar a mensagem.

>[!CAUTION]
>
>Este recurso não é compatível com o modo de interrupção.

### Ativar otimização de tempo de envio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Ativar otimização de tempo de envio"
>abstract="Escolha se deseja otimizar nas aberturas de email ou click-throughs por email selecionando o botão de opção apropriado. Você também pode optar por colar os tempos de envio usados pelo sistema, inserindo um valor para a opção Enviar na próxima."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Ativar otimização de tempo de envio"
>abstract="O padrão das mensagens de push é a opção de abertura, pois os cliques não são aplicáveis às mensagens de push. Você também pode optar por colar os tempos de envio usados pelo sistema, inserindo um valor para a opção Enviar na próxima."

Ative a Otimização de tempo de envio em um email ou mensagem de push selecionando o **Otimização de tempo de envio** alterne dos parâmetros da atividade.

![](../building-journeys/assets/jo-message5.png)

Para mensagens de email, escolha se deseja otimizar as aberturas de email ou click-throughs de email selecionando o botão de opção apropriado. O padrão das mensagens de push é a opção de abertura, pois os cliques não são aplicáveis às mensagens de push.

Você também pode optar por colchar os tempos de envio usados pelo sistema, inserindo um valor para a variável **Enviar na próxima** opção. Se você escolher &quot;seis horas&quot; como o valor, [!DNL Journey Optimizer] O verificará cada perfil de usuário e selecionará o tempo de envio ideal em seis horas a partir do tempo de execução da jornada.
