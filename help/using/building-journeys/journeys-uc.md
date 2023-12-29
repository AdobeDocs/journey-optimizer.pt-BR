---
solution: Journey Optimizer
product: journey optimizer
title: Casos de uso do Jornada
description: Casos de uso do Jornada
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: caso de uso, vários canais, mensagens, jornada, canal, eventos, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Caso de uso: enviar mensagens multicanais{#send-multi-channel-messages}

Esta seção apresenta um caso de uso que combina um Público-alvo de leitura, um evento, eventos de reação e mensagens de email/push.

![](assets/jo-uc1.png)

## Descrição do caso de uso

Nesse caso de uso, queremos enviar uma primeira mensagem de email para todos os clientes pertencentes a um público-alvo específico.

Com base na reação deles à primeira mensagem, queremos enviar mensagens específicas.

Se o cliente abrir o email, aguardaremos uma compra e enviaremos uma mensagem por push para agradecer ao cliente.

Se não houver reação, enviamos um email de acompanhamento.

## Pré-requisitos

Para que esse caso de uso funcione, é necessário configurar o seguinte:

* um público-alvo para todos os clientes que moram em Atlanta, São Francisco ou Seattle e nasceram após 1980.
* um evento de compra

### Criar o público

Em nossa jornada, queremos aproveitar um público-alvo específico de clientes do. Todos os indivíduos pertencentes ao público entram na jornada e seguem as diferentes etapas. Em nosso exemplo, precisamos de um público-alvo que segmente todos os clientes que moram em Atlanta, São Francisco ou Seattle e nascidos após 1980.

Para saber mais sobre públicos-alvo, consulte esta [página](../audience/about-audiences.md).

1. Na seção de menu CLIENTE, selecione **[!UICONTROL Públicos-alvo]**.

1. Clique em **[!UICONTROL Criar público]** botão localizado na parte superior direita da lista de públicos-alvo.

1. No **[!UICONTROL Propriedades do público]** insira um nome para o público-alvo.

1. Arraste e solte os campos desejados do painel esquerdo no espaço de trabalho central e configure-os de acordo com suas necessidades. Neste exemplo, usamos o **Cidade** e **Ano de nascimento** campos de atributos.

1. Clique em **[!UICONTROL Salvar]**.

   ![](assets/add-attributes.png)

O público-alvo agora está criado e pronto para ser usado na jornada. Uso de um **Ler público-alvo** atividade, você pode fazer com que todos os indivíduos pertencentes ao público-alvo entrem na jornada.

### Configurar o evento

Você precisa configurar um evento que é enviado para sua jornada quando um cliente faz uma compra. Quando a jornada recebe o evento, ela aciona a mensagem de &quot;obrigado&quot;.

Para isso, usamos um evento com base em regras. Para obter mais informações sobre eventos, consulte esta [página](../event/about-events.md).

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]** e, em seguida, clique em **[!UICONTROL Eventos]**. Clique em **[!UICONTROL Criar evento]** para criar um novo evento.

1. Insira o nome do evento.

1. No **[!UICONTROL Tipo de ID do evento]** selecione **[!UICONTROL Baseado em regras]**.

1. Defina o **[!UICONTROL Esquema]** e carga útil **[!UICONTROL Campos]**. Você pode usar vários campos, por exemplo, o produto comprado, a data de compra e a ID da compra.

1. No **[!UICONTROL Condição de ID de evento]** defina a condição usada pelo sistema para identificar os eventos que acionam a jornada. Por exemplo, é possível adicionar um `purchaseMessage` e defina a seguinte regra: `purchaseMessage="thank you"`

1. Defina o **[!UICONTROL Namespace]** e **[!UICONTROL Identificador de perfil]**.

1. Clique em **[!UICONTROL Salvar]**.

   ![](assets/jo-uc2.png)

Agora o evento está configurado e pronto para ser usado no jornada. Usando a atividade de evento correspondente, você pode acionar uma ação toda vez que um cliente fizer uma compra.

## Projetar a jornada

1. Inicie a jornada com um **Ler público-alvo** atividade. Selecione o público-alvo criado anteriormente. Todos os indivíduos pertencentes ao público entram na jornada.

   ![](assets/jo-uc4.png)

1. Soltar um **E-mail** atividade de ação e definir o conteúdo da &quot;primeira mensagem&quot;. Essa mensagem é enviada a todos os indivíduos na jornada. Consulte esta [seção](../email/create-email.md) para saber como configurar e projetar um email.

   ![](assets/jo-uc5.png)

1. Adicionar um **Reação** e selecione **Email aberto**. O evento é acionado quando um indivíduo pertencente ao público-alvo abre o email.

1. Verifique a **Definir o tempo limite do evento** , defina uma duração (1 dia no exemplo) e marque **Definir um caminho de tempo limite**. Isso cria outro caminho para indivíduos que não abrem a primeira mensagem de push ou email.

1. No caminho de tempo limite, solte um **E-mail** ação e definir o conteúdo da mensagem de &quot;acompanhamento&quot;. Essa mensagem é enviada às pessoas físicas que não abrirem o email ou enviarem a primeira mensagem por push no dia seguinte. Consulte esta [seção](../email/create-email.md) para saber como configurar e projetar um email.

1. No primeiro caminho, adicione o evento de compra criado anteriormente. O evento é acionado quando um indivíduo faz uma compra.

1. Depois do evento, solte um **Push** atividade de ação e definir o conteúdo da mensagem de agradecimento. Consulte esta [seção](../push/create-push.md) para saber como configurar e projetar um push.

## Testar e publicar a jornada

1. Antes de testar a jornada, verifique se ela é válida e se não há erros.

1. Clique no link **Teste** alternar, localizado no canto superior direito, para ativar o modo de teste. Consulte esta [seção](testing-the-journey.md) para saber como usar o modo de teste.

1. Quando a jornada estiver pronta, publique-a usando o **Publish** localizado no canto superior direito.
