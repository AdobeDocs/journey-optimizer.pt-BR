---
title: Casos de uso do Jornada
description: Casos de uso do Jornada
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 2%

---

# Caso de uso de jornada

![](../assets/do-not-localize/badge.png)

Esta seção apresenta um caso de uso que combina um segmento Lido, um evento, eventos de reação e mensagens de email/push.

![](../assets/jo-uc1.png)

## Descrição do caso de uso

Nesse caso de uso, queremos enviar uma primeira mensagem (email e push) para todos os clientes que pertencem a um segmento específico.

Com base na reação deles à primeira mensagem, queremos enviar mensagens específicas.

Após a primeira mensagem, esperamos um dia para que os clientes abram o push ou email. Se não houver reação, enviamos um email de acompanhamento.

Em seguida, aguardamos uma compra e enviamos uma mensagem de push para agradecer ao cliente.

## Pré-requisitos

Para que esse caso de uso funcione, é necessário configurar o seguinte:

* um segmento para todos os clientes que moram em Atlanta, São Francisco ou Seattle e nascem após 1980.
* um evento de compra
* três mensagens

### Criar o segmento

Em nossa jornada, queremos aproveitar um segmento específico de clientes. Todos os indivíduos pertencentes ao segmento entram na jornada e seguem as diferentes etapas. Em nosso exemplo, precisamos de um segmento direcionado a todos os clientes que moram em Atlanta, São Francisco ou Seattle e nasceram depois de 1980.

Para obter mais informações sobre segmentos, consulte esta [página](../segment/about-segments.md).

1. No menu **[!UICONTROL Segments]**, clique em **[!UICONTROL Create segment]**.

1. No painel **[!UICONTROL Segment properties]**, insira um nome para o segmento.

1. Arraste e solte os campos desejados do painel esquerdo para o espaço de trabalho central e configure-os de acordo com suas necessidades. Neste exemplo, usamos os campos de atributos **City** e **Birth year**.

1. Clique em **[!UICONTROL Save]**.

   ![](../assets/add-attributes.png)

O segmento agora é criado e pronto para ser usado em sua jornada. Usando uma atividade **Read segment** , é possível fazer com que todos os indivíduos pertencentes ao segmento entrem na jornada.

### Configurar o evento

Você precisa configurar um evento enviado para sua jornada quando um cliente fizer uma compra. Quando a jornada recebe o evento, ela aciona a mensagem &quot;obrigado&quot;.

Para isso, usamos um evento com base em regras. Para obter mais informações sobre eventos, consulte esta [página](../event/about-events.md).

1. Na seção ADMINISTRATION , navegue até **[!UICONTROL Configurations]** e clique em **[!UICONTROL Events]**. Clique em **[!UICONTROL Add]** para criar um novo evento.

1. Insira o nome do evento.

1. No campo **[!UICONTROL Event ID type]**, selecione **[!UICONTROL Rule Based]**.

1. Defina o **[!UICONTROL Schema]** e a carga **[!UICONTROL Fields]**. Você pode usar vários campos, por exemplo, o produto comprado, a data de compra e a id de compra.

1. No campo **[!UICONTROL Event ID condition]**, defina a condição usada pelo sistema para identificar os eventos que acionam sua jornada. Por exemplo, você pode adicionar um campo `purchaseMessage` e definir a seguinte regra: `purchaseMessage="thank you"`

1. Defina os **[!UICONTROL Namespace]** e **[!UICONTROL Key]**.

1. Clique em **[!UICONTROL Save]**.

   ![](../assets/jo-uc2.png)

O evento agora está configurado e pronto para ser usado em sua jornada. Usando a atividade de evento correspondente, você pode acionar uma ação sempre que um cliente fizer uma compra.

### Criar as mensagens

Para esse caso de uso, precisamos criar três mensagens:

* uma primeira mensagem por push e email
* uma mensagem de push &quot;obrigado&quot;
* uma mensagem de acompanhamento por email

![](../assets/jo-uc3.png)

Consulte esta [seção](../segment/about-segments.md) para saber como criar e publicar essas mensagens.

## Projetar a jornada

1. Inicie a jornada com uma atividade **Read segment** . Selecione o segmento criado anteriormente. Todos os indivíduos pertencentes ao segmento entram na jornada.

   ![](../assets/jo-uc4.png)

1. Solte uma atividade **Message** e selecione a primeira mensagem por push e email. Esta mensagem é enviada a todos os indivíduos na jornada.

   ![](../assets/jo-uc5.png)

1. Coloque o cursor na atividade da mensagem e clique no símbolo &quot;+&quot; para criar um novo caminho.

1. No primeiro caminho, adicione um evento **Reaction** e selecione **Push opened**. O evento é acionado quando um indivíduo pertencente ao segmento abre a versão de push da primeira mensagem.

1. No segundo caminho, adicione um evento **Reaction** e selecione **Email opened**. O evento é acionado quando o indivíduo abre o email.

1. Em uma das atividades de reação, marque a caixa **Define the event timeout**, defina uma duração (1 dia no nosso exemplo) e marque **Set a timeout path**. Isso cria outro caminho para indivíduos que não abrem a primeira mensagem de push ou email.

   >[!NOTE]
   >
   >Ao configurar um tempo limite em vários eventos (as duas reações, neste caso), é necessário apenas configurar o tempo limite em um desses eventos.

1. No caminho de tempo limite, solte uma atividade **Message** e selecione a mensagem de acompanhamento de email. Esta mensagem é enviada aos indivíduos que não abrem o email ou enviam a primeira mensagem no dia seguinte.

1. Conecte os três caminhos ao evento de compra criado anteriormente. O evento é acionado quando um indivíduo faz uma compra.

1. Depois do evento, solte uma atividade **Message** e selecione a mensagem de email &quot;obrigado&quot;.

1. Adicione uma atividade **End**.

## Testar e publicar a jornada

1. Antes de testar sua jornada, verifique se ela é válida e se não há erro.

1. Clique no botão **Test**, localizado no canto superior direito, para ativar o modo de teste. Defina como deseja que os perfis de teste insiram o teste: um único perfil, ou até 100 de uma só vez. Consulte esta [seção](testing-the-journey.md) para saber como usar o modo de teste.

1. Quando a jornada estiver pronta, publique-a usando o botão **Publish**, localizado no canto superior direito.
