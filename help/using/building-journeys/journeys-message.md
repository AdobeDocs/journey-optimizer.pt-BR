---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma mensagem em uma jornada
description: Saiba como adicionar uma mensagem em uma jornada
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: jornada, mensagem, push, sms, email, no aplicativo
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: f2037f559826d7cca243092de200c97841c49b35
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 15%

---

# Enviar mensagens de email, no aplicativo, push e texto {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Atividade de mensagem"
>abstract="O Journey Optimizer vem com recursos de mensagem incorporados. Você pode simplesmente adicionar, em sua jornada, um push, uma mensagem de texto (SMS/MMS), uma atividade no aplicativo ou de mensagem de email e definir configurações e conteúdo. Em seguida, ela é executada e enviada no contexto da jornada."

[!DNL Journey Optimizer] O vem com recursos de mensagem incorporados. Você pode simplesmente adicionar, em sua jornada, um push, um SMS/MMS, uma atividade de mensagem no aplicativo ou por email e definir configurações e conteúdo. Em seguida, ela é executada e enviada no contexto da jornada.

Você também pode configurar ações específicas para enviar mensagens para você:

* Se você estiver usando um sistema de terceiros para enviar mensagens, poderá criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md).

* Se estiver trabalhando com o Campaign e o Journey Optimizer, consulte estas seções:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e CAMPAIGN STANDARD](../action/acs-action.md)

Para adicionar uma mensagem em uma jornada, siga as etapas abaixo:

1. Inicie sua jornada com um [Evento](general-events.md) ou um [Ler público-alvo](read-audience.md) atividade.

1. No **Ações** da paleta, arraste e solte uma **email**, um **No aplicativo**, um **SMS** ou um **Push** atividade na tela.

1. Configure sua atividade. Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Lead" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>Criar emails</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../in-app/create-in-app.md">
   <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>Criar mensagens no aplicativo</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Pouco frequente" src="../assets/do-not-localize/push.jpg">
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
   <a href="../sms/create-sms.md"><strong>Criar mensagens de texto (SMS/MMS)</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Atualizar conteúdo ao vivo{#update-live-content}

Você pode atualizar o conteúdo de uma mensagem (email, No aplicativo, Push, SMS) em uma jornada em tempo real.

Para fazer isso, abra a jornada em tempo real, selecione a atividade de mensagem e clique em **Editar conteúdo**.

![](assets/add-a-message2.png)

No entanto, não é possível alterar os atributos usados na personalização, sejam eles atributos de perfil ou dados contextuais (de propriedades de evento ou jornada).

Se você modificou dados contextuais, a seguinte mensagem de erro será exibida: ERR_AUTHORING_JOURNEYVERSION_201

Se você modificou atributos de perfil, a seguinte mensagem de erro será exibida: ERR_AUTHORING_JOURNEYVERSION_202

Observe que, para a atividade no aplicativo, qualquer alteração pode ser feita no conteúdo enquanto a jornada está ativa, mas os acionadores no aplicativo não podem ser modificados.

## Otimização de tempo de envio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Sobre a otimização da hora de envio"
>abstract="O recurso Otimização da hora de envio do Adobe Journey Optimizer, desenvolvido pelos serviços de IA da Adobe, pode prever o melhor momento para enviar um email ou uma mensagem por push para maximizar o engajamento com base nas taxas históricas de abertura e clique."

### Sobre a otimização de tempo de envio {#about-send-time}

O recurso de Otimização de tempo de envio da Adobe Journey Optimizer, viabilizado pelos serviços de IA de Adobe, pode prever o melhor momento para enviar um email ou mensagem por push. Isso maximiza o engajamento com base no histórico das taxas de abertura e de clique. Use nosso modelo de aprendizado de máquina para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e de clique de suas mensagens.

O modelo de Otimização de tempo de envio assimila os dados do Adobe Journey Optimizer e observa as taxas de abertura (para email e push) e de clique (para email) no nível do usuário para determinar quando seus clientes têm maior probabilidade de interagir com suas mensagens. A Otimização de tempo de envio requer no mínimo um mês de dados de rastreamento de mensagens para fazer recomendações informadas. Para cada usuário, o sistema escolherá automaticamente o melhor momento usando as seguintes pontuações:

* A melhor hora de cada dia da semana para maximizar o engajamento
* O melhor dia da semana para maximizar o envolvimento
* A melhor hora do melhor dia da semana para maximizar o engajamento

O modelo varia se você estiver falando sobre pontuação ou treinamento. O treinamento é realizado inicialmente semanalmente e depois trimestralmente. A pontuação é inicialmente semanal e depois mensal.

* Treinamento - o desenvolvimento do algoritmo usado para fazer a pontuação
* Pontuação - a aplicação de uma pontuação a perfis individuais com base no modelo treinado

Essas informações são armazenadas com o perfil do usuário e são referenciadas na execução da jornada para informar ao Adobe Journey Optimizer quando enviar sua mensagem.

>[!CAUTION]
>
>Este recurso não é compatível com o modo de intermitência.

### Perguntas frequentes {#faq-send-time}

O que a Otimização de tempo de envio pode fazer? Como ele lida com novos perfis? Ele espalha o envio por uma janela de 12/6/24 horas?

A Otimização de tempo de envio tenta prever o melhor momento para interagir com os clientes e otimizar as taxas de abertura/clique de emails. A pontuação está em um formato de `3*7*24` atributos para cada perfil. A variável `7*24` os atributos descrevem a classificação do melhor momento previsto para enviar emails para o recipient e o 3 é para otimizar a taxa de abertura de emails, a taxa de cliques de email e a taxa de abertura de push.

Onde posso ver o tempo de envio esperado para cada perfil?

Você pode ver a pontuação geral no **Perfis** interface. Para cada um dos três conjuntos de 168 pontuações, as posições vão de -83 a 84. Quanto maior a classificação, melhor o tempo foi escolhido para interagir com o recipient. Como é possível definir o início e a duração de uma jornada, a melhor classificação (84) pode não cair nessa janela de tempo. Nesse caso, recomendamos escolher uma hora com o valor de classificação mais alto.

Quais relatórios estão disponíveis?

Acesse sua jornada, clique no link **Exibir relatório** no canto superior direito e selecione o botão **Jornada** à esquerda. [Leia mais](../reports/journey-global-report.md)

Como os dados da Otimização de tempo de envio afetam a riqueza do perfil?

A Otimização de tempo de envio adiciona a pontuação/atributos a cada perfil, mas nenhum perfil novo é criado.

### Ativar otimização da hora de envio{#activate-send-time-optimization}

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

Para mensagens de email, escolha se deseja otimizar as aberturas de email ou click-throughs de email selecionando o botão de opção apropriado. As mensagens de push assumem o padrão da opção de aberturas, pois os cliques não se aplicam às mensagens de push.

Você também pode optar por colocar entre colchetes os tempos de envio usados pelo sistema inserindo um valor para a variável **Enviar no próximo** opção. Se você escolher &quot;seis horas&quot; como o valor, [!DNL Journey Optimizer] O verificará cada perfil de usuário e escolherá o tempo de envio ideal dentro de seis horas a partir do tempo de execução da jornada.

**O que acontece se o horário ideal estiver fora da janela?**

Vamos ver um exemplo com a seguinte configuração:

* Otimizar em cliques
* A ação deve começar às 10h
* A janela é de 3 horas

Um perfil pode ter um tempo de abertura ideal, que está fora da janela. Por exemplo, a abertura ideal de John ao clicar é às 17h.

No nível do perfil, há pontuações para cada hora da semana. Neste exemplo, o email sempre será enviado dentro da janela. No tempo de execução, o sistema verifica a lista de pontuações nessa janela (janela de 3 horas começando às 10h). Em seguida, o sistema compara as pontuações de 10, 11 e meio-dia e seleciona a mais alta. O email é enviado nesse momento.
