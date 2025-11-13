---
solution: Journey Optimizer
product: journey optimizer
title: Enviar uma mensagem usando o Campaign v7/v8
description: Saiba como enviar uma mensagem usando o Campaign v7/v8
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: jornada, mensagem, campanha, integração
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 1%

---

# Enviar uma mensagem com o Campaign v7/v8 {#campaign-v7-v8-use-case}

Esse caso de uso explica todas as etapas necessárias para enviar um email usando a integração com o Adobe Campaign v7 e o Adobe Campaign v8.

>[!NOTE]
>
>Para usar essa integração, você deve ter o Campaign v7/v8 build 9125 ou superior.

Primeiro, crie um template de email transacional no Campaign. Em seguida, no Journey Optimizer, crie o evento, a ação e crie a jornada.

Para saber mais sobre a integração do Campaign, consulte estas páginas:

* [Criar uma ação de campanha](../action/acc-action.md)
* [Usando a ação em uma jornada](../building-journeys/using-adobe-campaign-v7-v8.md).

**Adobe Campaign**

A instância do Campaign deve ser provisionada para essa integração. O recurso de mensagens transacionais deve ser configurado.

1. Faça logon na instância de controle do Campaign.

1. Em **Administração** > **Plataforma** > **Enumerações**, selecione a enumeração **Tipo de evento** (eventType). Crie um novo tipo de evento (&quot;jornada-evento&quot;, em nosso exemplo). Use o nome interno do tipo de evento ao gravar o arquivo JSON posteriormente.

   ![Configurar um evento no Adobe Journey Optimizer com seleção de esquema e campo](assets/accintegration-uc-1.png)

1. Desconecte e reconecte à instância para que a criação entre em vigor.

1. Em **Centro de Mensagens** > **Modelos de mensagens transacionais**, crie um novo modelo de email com base no tipo de evento criado anteriormente.

   ![Configuração de evento mostrando as configurações de identificador de perfil e namespace](assets/accintegration-uc-2.png)

1. Projete seu modelo. Neste exemplo, a personalização é aplicada ao nome do perfil e ao número do pedido. O nome está na fonte de dados do Adobe Experience Platform e o número do pedido é um campo do evento do Journey Optimizer. Use os nomes de campo corretos no Campaign.

   ![Visualização da carga do evento mostrando a estrutura JSON com dados de perfil e evento](assets/accintegration-uc-3.png)

1. Publique seu template transacional.

   ![Botão de cópia de evento para copiar a ID da carga para integração com a API](assets/accintegration-uc-4.png)

1. Escreva a carga JSON correspondente ao modelo.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Para o canal, é necessário digitar &quot;email&quot;.
* Para eventType, use o nome interno do tipo de evento criado anteriormente.
* O endereço de email será uma variável, para que você possa digitar qualquer rótulo.
* No ctx, os campos de personalização também são variáveis.

**Journey Optimizer**

1. Criar um evento. Inclua o campo &quot;purchaseOrderNumber&quot;.

   ![Tela de configuração de ação personalizada para integração com o Adobe Campaign Classic](assets/accintegration-uc-5.png)

1. Crie uma ação no Journey Optimizer correspondente ao seu template de Campanha. No menu suspenso **Tipo de ação**, selecione **Adobe Campaign Classic**.

   ![Seleção do tipo de ação mostrando a opção Adobe Campaign Classic](assets/accintegration-uc-6.png)

1. Clique no **campo de carga** e cole o JSON criado anteriormente.

   ![Lista suspensa de seleção de conta de campanha para integração de ações](assets/accintegration-uc-7.png)

1. Para o endereço de email e os dois campos de personalização, altere **Constante** para **Variável**.

   ![Configuração de carga de ação com mapeamento de campo para integração com o Campaign](assets/accintegration-uc-8.png)

1. Agora crie uma nova jornada e comece com o evento criado anteriormente.

   ![Jornada tela com evento e ação de campanha configurados](assets/accintegration-uc-9.png)

1. Adicione a ação e mapeie cada campo para o campo correto no Journey Optimizer.

   ![Mapeamento de parâmetro de ação com o editor de expressão para valores dinâmicos](assets/accintegration-uc-10.png)

1. Teste a jornada.

   ![Concluir o fluxo de jornadas com o disparador de eventos e a execução da ação de Campanha](assets/accintegration-uc-11.png)

1. Agora você pode publicar sua jornada.
