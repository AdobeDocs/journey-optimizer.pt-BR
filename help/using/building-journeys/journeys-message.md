---
title: Adicionar uma mensagem em uma jornada
description: Adicionar uma mensagem em uma jornada
source-git-commit: 364861beb52e5663389a254ba145b31431b696ac
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 4%

---

# Adicionar uma mensagem em uma jornada

![](../assets/do-not-localize/badge.png)

[!DNL Journey Optimizer] Os recursos de mensagem são integrados, basta criar o conteúdo e publicar a mensagem. Consulte [esta seção](../get-started-content.md). Em seguida, adicione na jornada uma mensagem de push ou email projetada com o Journey Optimizer.

Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md).

## Adição de uma atividade Message

1. Como sempre, inicie a jornada com um evento ou uma atividade **Read segment** .

   ![](../assets/jo-message0.png)

1. Na seção **Actions** da paleta, arraste e solte uma atividade **Message** na tela.

   ![](../assets/jo-message1.png)

1. Adicione um rótulo e uma descrição.

   ![](../assets/jo-message2.png)

1. Clique dentro do campo **Message**. A lista de mensagens disponíveis projetadas no Journey Optimizer é exibida. Você pode filtrar a lista por status.

   ![](../assets/jo-message3.png)

1. Escolha uma mensagem e clique em **Select**. Você também pode criar uma nova mensagem diretamente nessa tela clicando em **Create new**.

   ![](../assets/jo-message4-ter.png)

   Se quiser verificar sua mensagem, clique no ícone **Open the message** no campo **Message**. A mensagem será aberta em uma nova guia.

   ![](../assets/jo-message4-bis.png)

1. Adicione as próximas etapas à jornada.

## Parâmetros de canal

Os parâmetros **Channel** são exibidos. Esses campos são somente leitura. Essa configuração é executada ao criar a mensagem. Consulte [esta seção](../get-started-content.md).

![](../assets/jo-message4.png)

Você pode usar o ícone **Enable editing field** no lado direito do campo para forçar um valor específico. Isso pode ser útil para fins de teste. Por exemplo, para um email, você pode adicionar seu endereço de email. Ao publicar a jornada, o email será enviado para você.
