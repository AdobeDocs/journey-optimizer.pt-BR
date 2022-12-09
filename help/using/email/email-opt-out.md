---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de recusa de email
description: Saiba como gerenciar a recusa com emails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Gerenciamento de recusa de email {#email-opt-out}

Para fornecer a capacidade de cancelar a assinatura dos recipients do recebimento de comunicações por email, você deve sempre incluir um **link de cancelamento de inscrição** em cada email enviado aos recipients. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

Para fazer isso, é possível:

* Insira um **link para uma página de aterrissagem externa** em um email para permitir que os usuários cancelem a assinatura do recebimento de comunicações de sua marca. [Saiba como adicionar um link de recusa externo](#opt-out-external-lp)

* Adicione um **link para opção de não participação com um clique** no seu conteúdo de email. Esse link permitirá que seus recipients cancelem rapidamente a assinatura de suas comunicações, sem serem redirecionados para uma página de aterrissagem onde precisam confirmar sua escolha, o que acelera o processo de cancelamento de assinatura. [Saiba como adicionar um link para opção de não participação com um clique](#one-click-opt-out)

Além disso, se a variável **[!UICONTROL List-Unsubscribe]** estiver ativada no nível da superfície do canal, os emails correspondentes enviados com o Journey Otimizer incluirão um link de cancelamento de subscrição no cabeçalho do email. [Saiba mais sobre a opção de não participação no cabeçalho do email](#unsubscribe-header)

>[!NOTE]
>
>As mensagens de email de tipo de marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais. A categoria da mensagem (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactional]**) é definido na variável [superfície do canal](../configuration/channel-surfaces.md#email-type) (ou seja, predefinição de mensagem) e ao criar a mensagem.

## Opt out externo {#opt-out-external-lp}

### Adicionar um link de cancelamento de subscrição {#add-unsubscribe-link}

Primeiro, é necessário adicionar um link de cancelamento de subscrição em uma mensagem. Para fazer isso, siga as etapas abaixo:

1. Crie sua própria landing page de unsubscription.

1. Hospede-o no sistema de terceiros de sua escolha.

1. Crie uma mensagem em uma jornada.

1. Selecione o texto no seu conteúdo e [inserir um link](../email/message-tracking.md#insert-links) usando a barra de ferramentas contextual.

   ![](assets/opt-out-insert-link.png)

1. Selecionar **[!UICONTROL External Opt-out/Unsubscription]** do **[!UICONTROL Link type]** lista suspensa.

   ![](assets/opt-out-link-type.png)

1. No **[!UICONTROL Link]** , cole o link na landing page de terceiros.

   ![](assets/opt-out-link-url.png)

1. Clique em **[!UICONTROL Save]**.

### Implementar uma chamada de API para opção de não participação {#opt-out-api}

Para que seus recipients optem ao enviar sua escolha a partir da landing page, você deve implementar uma **Chamada da API de assinatura** through [Desenvolvedor da Adobe](https://developer.adobe.com){target=&quot;_blank&quot;} para atualizar as preferências dos perfis correspondentes.

Essa chamada POST é a seguinte:

Endpoint: platform.adobe.io/journey/imp/consent/preferences

Parâmetros de consulta:

* **params**: contém a carga criptografada
* **sig**: assinatura
* **pid**: ID de perfil criptografada

Esses três parâmetros serão incluídos no URL da página de aterrissagem de terceiros enviado ao seu recipient:

![](assets/opt-out-parameters.png)

Requisitos do cabeçalho:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorização (token de usuário da sua conta técnica)

Corpo da solicitação:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] usará esses parâmetros para atualizar a escolha do perfil correspondente por meio do [Desenvolvedor da Adobe](https://developer.adobe.com){target=&quot;_blank&quot;} Chamada da API.

### Enviar a mensagem com link de cancelamento de subscrição {#send-message-unsubscribe-link}

Depois de configurar o link de cancelamento de subscrição para a landing page e implementar a chamada à API, sua mensagem estará pronta para ser enviada.

1. Envie a mensagem incluindo o link por meio de um [jornada](../building-journeys/journey.md).

1. Depois que a mensagem é recebida, se o recipient clicar no link de cancelamento de inscrição, sua landing page será exibida.

   ![](assets/opt-out-lp-example.png)

1. Se o recipient enviar o formulário (aqui, pressionando o **Cancelar inscrição** na página de aterrissagem), os dados do perfil são atualizados por meio do [Chamada de API](#opt-out-api).

1. O recipient que recusou a inscrição é então redirecionado para uma tela de mensagem de confirmação indicando que a recusa foi bem-sucedida.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, esse usuário não receberá a comunicação da sua marca, a menos que tenha feito a assinatura novamente.

1. Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [Documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   No **[!UICONTROL Attributes]** , você pode ver o valor de **[!UICONTROL choice]** mudou para **[!UICONTROL no]**.

## Cancelamento de um clique {#one-click-opt-out}

Para adicionar um link para opção de não participação no seu email, siga as etapas abaixo.

1. [Inserir um link](../email/message-tracking.md#insert-links) e selecione **[!UICONTROL One click Opt-out]** como o tipo de link.

   ![](assets/message-tracking-opt-out.png)

1. Selecione como deseja aplicar a opção de rejeição: no canal, identidade ou nível de assinatura.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: A recusa se aplica a mensagens futuras enviadas ao destino do perfil (ou seja, endereço de email) do canal atual. Se vários destinos estiverem associados a um perfil, a recusa se aplica a todos os destinos (ou seja, endereços de email) no perfil desse canal.
   * **[!UICONTROL Identity]**: A recusa se aplica a mensagens futuras enviadas ao target específico (ou seja, endereço de email) que está sendo usado para a mensagem atual.
   * **[!UICONTROL Subscription]**: A recusa se aplica a mensagens futuras associadas a uma lista de assinaturas específica. Essa opção só poderá ser selecionada se a mensagem atual estiver associada a uma lista de assinaturas.

1. Insira o URL da landing page onde o usuário será redirecionado depois de cancelado a assinatura. Esta página está aqui somente para confirmar que a opção de rejeição foi bem-sucedida.

   >[!NOTE]
   >
   >Se você ativou a variável **List-Unsubscribe** no nível da superfície do canal, esse URL também será usado quando os usuários clicarem no link de cancelamento de subscrição no cabeçalho do email. [Saiba mais](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Você pode personalizar seus links. Saiba mais sobre URLs personalizados em [esta seção](../personalization/personalization-syntax.md).

1. Salve as alterações.

Depois que a mensagem for enviada por meio de um [jornada](../building-journeys/journey.md), se um recipient clicar no link para opção de não participação, seu perfil será rejeitado imediatamente.

## Cancelar assinatura do link no cabeçalho do email {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Adicionar link de cancelamento de subscrição ao cabeçalho do email"
>abstract="Ative o List-Unsubscribe para adicionar um link de cancelamento de subscrição ao cabeçalho do email. Para definir um URL de cancelamento de inscrição, insira um link de recusa de um clique no conteúdo do email."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#one-click-opt-out" text="Cancelamento de um clique"

Se a variável [Opção List-Unsubscribe](../configuration/channel-surfaces.md#list-unsubscribe) estiver ativado no nível da superfície do canal, os emails correspondentes enviados com [!DNL Journey Optimizer] incluirá um link de cancelamento de subscrição no cabeçalho do email.

Por exemplo, o link de cancelamento de inscrição será exibido assim no Gmail:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Para exibir o link de cancelamento de subscrição no cabeçalho do email, o cliente de email dos recipients deve ser compatível com esse recurso.

O endereço de cancelamento de subscrição é o padrão **[!UICONTROL Mailto (unsubscribe)]** endereço exibido na superfície do canal correspondente. [Saiba mais](../configuration/channel-surfaces.md#list-unsubscribe).

Para definir um URL de cancelamento de inscrição personalizado, insira um link de recusa de um clique no conteúdo da mensagem de email e insira o URL de sua escolha. [Saiba mais](#one-click-opt-out)

Dependendo do cliente de email, clicar no link de cancelamento de inscrição no cabeçalho poderá ter os seguintes impactos:

* A solicitação de cancelamento de subscrição é enviada para o endereço de cancelamento de subscrição padrão.

* O recipient é direcionado para o URL da página de aterrissagem que você especificou ao adicionar o link de recusa à mensagem.

   >[!NOTE]
   >
   >Se você não adicionar um link para opção de não participação com um clique no conteúdo da mensagem, nenhuma landing page será exibida.

* O perfil correspondente é imediatamente rejeitado e essa opção é atualizada na Experience Platform. Saiba mais na [Documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.
