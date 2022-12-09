---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma mensagem em uma jornada
description: Saiba como adicionar uma mensagem em uma jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Email, SMS, Push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] O vem com recursos de mensagem integrados. Você pode simplesmente adicionar, em sua jornada, uma atividade de push, SMS ou mensagem de email e definir configurações e conteúdo. Em seguida, é executado e enviado no contexto da jornada.

Você também pode configurar ações específicas para enviar mensagens:

* Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta seção [seção](../action/action.md).

* Se estiver trabalhando com o Campaign e o Journey Otimizer, consulte estas seções:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

Para adicionar uma mensagem em uma jornada, siga as etapas abaixo:

1. Inicie sua jornada com uma [Evento](general-events.md) ou [Ler segmento](read-segment.md) atividade .

1. No **Ações** seção da paleta, arraste e solte uma **email**, um **SMS** ou **Empurrar** atividade na tela.

1. Configure sua atividade. Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Líder" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>Criar emails</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Pouco frequentes" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>Criar notificações por push<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="Validação" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>Criar mensagens SMS</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Atualizar conteúdo ao vivo{#update-live-content}

Você pode atualizar o conteúdo de uma mensagem (email, sms, push) em uma jornada ao vivo.

Para fazer isso, abra a jornada ao vivo, selecione a atividade da mensagem e clique em **Editar conteúdo**.

![](assets/add-a-message2.png)

No entanto, não é possível alterar os atributos usados na personalização, sejam eles atributos de perfil ou dados contextuais (das propriedades de evento ou jornada).

## Otimização de tempo de envio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Sobre a otimização de tempo enviado"
>abstract="O recurso de Otimização de tempo de envio do Adobe Journey Otimizer, desenvolvido pelos serviços de IA da Adobe, pode prever o melhor momento para enviar um email ou uma mensagem de push para maximizar o envolvimento com base nas taxas de abertura e cliques do histórico."

### Sobre a otimização por tempo de envio {#about-send-time}

O recurso de Otimização de tempo de envio do Adobe Journey Otimizer, desenvolvido pelos serviços de IA da Adobe, pode prever o melhor momento para enviar um email ou uma mensagem de push para maximizar o envolvimento com base nas taxas de abertura e cliques do histórico. Use nosso modelo de aprendizado de máquina para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e cliques de suas mensagens.

O modelo de Otimização de tempo de envio assimila seus dados do Adobe Journey Otimizer e verifica as taxas de abertura no nível do usuário (para email e push) e de clique (para email) para determinar quando seus clientes têm maior probabilidade de se envolver com suas mensagens. A otimização de tempo de envio requer no mínimo um mês de dados de rastreamento de mensagem para fazer recomendações informadas. Para cada usuário, o sistema selecionará automaticamente o melhor horário usando as seguintes pontuações:

* A melhor hora de cada dia da semana para maximizar o envolvimento
* O melhor dia da semana para maximizar o envolvimento
* A melhor hora do melhor dia da semana para maximizar o envolvimento

O modelo varia se você estiver falando de pontuação ou treinamento. O treinamento é feito semanalmente, inicialmente e depois trimestralmente. A pontuação é semanal inicialmente e mensal.

* Treinamento - o desenvolvimento do algoritmo usado para fazer a pontuação
* Pontuação - a aplicação de uma pontuação a perfis individuais com base no modelo treinado

Essas informações são armazenadas com o perfil do usuário e são referenciadas na execução da jornada para informar ao Adobe Journey Otimizer quando enviar sua mensagem.

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
