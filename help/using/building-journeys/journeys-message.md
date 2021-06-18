---
title: Adicionar uma mensagem em uma jornada
description: Adicionar uma mensagem em uma jornada
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# Adicionar uma mensagem em uma jornada

[!DNL Journey Optimizer] Os recursos de mensagem são integrados, basta criar o conteúdo e publicar a mensagem. Consulte [esta seção](../get-started-content.md). Em seguida, adicione na jornada uma mensagem de push ou email projetada com o Journey Optimizer.

Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md).

## Adição de uma atividade Message

1. Como sempre, inicie a jornada com um evento ou uma atividade **Ler segmento** .

   ![](../assets/jo-message0.png)

1. Na seção **Actions** da paleta, arraste e solte uma atividade **Message** na tela.

   ![](../assets/jo-message1.png)

1. Adicione um rótulo e uma descrição.

   ![](../assets/jo-message2.png)

1. Clique dentro do campo **Message**. A lista de mensagens disponíveis projetadas no Journey Optimizer é exibida. Você pode filtrar a lista por status.

   ![](../assets/jo-message3.png)

1. Escolha uma mensagem e clique em **Select**. Você também pode criar uma nova mensagem diretamente nessa tela clicando em **Create message**.

   ![](../assets/jo-message4-ter.png)

   Se quiser verificar sua mensagem, clique no ícone **Open the message** no campo **Message**. A mensagem será aberta em uma nova guia.

   ![](../assets/jo-message4-bis.png)

1. Adicione as próximas etapas à jornada.

## Parâmetros de email e parâmetros de push

As seções **[!UICONTROL Email parameters]** e **[!UICONTROL Push parameters]** mostram campos somente leitura. Normalmente, você executa essa configuração ao criar a mensagem. Consulte [esta seção](../get-started-content.md).

![](../assets/jo-message4.png)

Para forçar um valor específico, você pode usar o ícone **Enable parameter override** à direita do campo. Essa opção pode ser útil para fins de teste. Por exemplo, para um email, você pode adicionar seu endereço de email. Após publicar a jornada, o email será enviado para você.
