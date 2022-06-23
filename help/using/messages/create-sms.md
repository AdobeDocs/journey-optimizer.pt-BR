---
title: Criar uma mensagem de SMS.
description: Saiba como criar uma mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 9%

---

# Criar uma mensagem de SMS. {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Criação de SMS"
>abstract="Adicione a mensagem de texto e comece a personalizá-la com o Editor de expressão."

Uma vez [criou uma mensagem](get-started-content.md), use o **[!UICONTROL SMS]** para definir as configurações e o conteúdo da mensagem SMS.


>[!AVAILABILITY]
>
>No momento, o canal SMS está disponível apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o representante do Adobe.

![](assets/sms_1.png)

Se esta for a primeira vez que você cria uma mensagem SMS, verifique se o canal SMS foi configurado. [Saiba mais](../configuration/sms-configuration.md).

## Definir o conteúdo do SMS{#sms-content}

Para começar a personalizar a mensagem SMS, siga estas etapas:

1. Clique no botão **[!UICONTROL Add text message]** para abrir o editor de expressão.

   ![](assets/sms_3.png)

1. Use o Editor de expressão para definir o conteúdo. Você pode usar qualquer atributo para personalizar o conteúdo, como o nome do perfil ou a cidade. Saiba mais sobre a personalização no Editor de expressão em [esta seção](../personalization/personalize.md)

   >[!NOTE]
   >
   > Uma mensagem SMS pode ter até 160 caracteres, incluindo espaços e quebras de linha.

   ![](assets/sms_2.png)

1. Clique em **[!UICONTROL Save]** quando sua mensagem estiver pronta.

## Validar o SMS{#sms-preview}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu [conteúdo personalizado](../personalization/personalize.md), é possível verificar como esse conteúdo é exibido na mensagem, aproveitando os dados do perfil de teste.

Para visualizar como sua mensagem SMS é exibida em dispositivos móveis, navegue até o **[!UICONTROL Preview]** guia .

Para obter mais informações, consulte [esta seção](../design/preview.md).

## Publicar seu SMS {#sms-publish}

Quando a mensagem estiver pronta, você poderá publicá-la para disponibilizá-la para execução com a **[!UICONTROL Publish]** botão. Esta ação publica a nova versão da mensagem que será usada para as próximas execuções em suas jornadas.

Sua mensagem SMS agora pode ser usada em uma jornada. [Saiba como criar jornadas](../building-journeys/journey-gs.md).

## Aceitação e recusa{#sms-opt-in-out}

Para todas as mensagens de marketing, o SMS deve conter uma maneira de os recipients cancelarem a assinatura facilmente. Após a unsubscription, os perfis serão removidos automaticamente do público-alvo de futuras mensagens de marketing. A adição de um link de unsubscription não é obrigatória para mensagens transacionais.

Os recipients do SMS podem responder com palavras-chave de aceitação e recusa. De acordo com os padrões e regulamentos do setor, o Adobe Journey Optimizer processa automaticamente as seguintes palavras-chave nas mensagens recebidas: INICIAR, PARAR e DESPARAR. Essas palavras-chave acionam respostas padrão automáticas do provedor de SMS.

**Tópicos relacionados**

* [Configurar canal de SMS](../configuration/sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)
* [Criar uma nova mensagem](get-started-content.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
