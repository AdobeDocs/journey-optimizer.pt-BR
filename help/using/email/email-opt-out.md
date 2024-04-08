---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de opção de não participação de email
description: Saiba como gerenciar a opção de não participação com emails
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: recusar, email, link, cancelar inscrição
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 76%

---

# Gerenciamento de opção de não participação de email {#email-opt-out}

Para fornecer aos recipients a capacidade de cancelar a inscrição para receber comunicações por email, você deve sempre incluir um **link para cancelar inscrição** em cada email enviado aos recipients. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

Para fazer isso, é possível:

* Inserir um **link para uma landing page** em um email para permitir que os usuários cancelem a inscrição do recebimento de comunicações da sua marca. Pode ser:

   * A **[!DNL Journey Optimizer]landing page**. [Saiba como adicionar uma página de aterrissagem de recusa](../landing-pages/lp-use-cases.md#opt-out)

   * A **uma landing page externa**. [Saiba como adicionar um link externo para opção de não participação](#opt-out-external-lp)

* Adicionar um **link para opção de não participação com um clique** no seu conteúdo de email. Esse link permitirá que seus destinatários cancelem rapidamente a inscrição de suas comunicações, sem ser redirecionados para uma página de destino em que precisam confirmar o cancelamento, agilizando o processo de cancelamento de inscrição. [Saiba como adicionar um link para opção de não participação com um clique](#one-click-opt-out)

* Adicione um link para cancelar a inscrição no cabeçalho do email. Se a variável **[!UICONTROL List-Unsubscribe]** estiver ativada no nível da superfície de canal, os emails correspondentes enviados com o Journey Optimizer incluirão um link de cancelamento de inscrição no cabeçalho do email. [Saiba mais sobre a opção de não participação no cabeçalho do email](#unsubscribe-header)

>[!NOTE]
>
>As mensagens de email do tipo Marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais. A categoria da mensagem (**[!UICONTROL Marketing]** ou **[!UICONTROL Transacional]**) é definida no [superfície de canal](../configuration/channel-surfaces.md#email-type) e ao criar a mensagem).

## Opção de não participação externa {#opt-out-external-lp}

### Adicionar link para cancelar inscrição {#add-unsubscribe-link}

Primeiro, é necessário adicionar um link para cancelar inscrição em uma mensagem. Para fazer isso, siga as etapas abaixo:

1. Crie sua página de destino de cancelamento de inscrição.

1. Hospede-o no sistema de terceiros de sua preferência.

1. Criar uma mensagem em uma jornada.

1. Selecione o texto no seu conteúdo e [insira um link](../email/message-tracking.md#insert-links) usando a barra de ferramentas contextual.

   ![](assets/opt-out-insert-link.png)

1. Selecione **[!UICONTROL Não participação/cancelamento de assinatura externa]** na lista suspensa **[!UICONTROL Tipo de link]**.

   ![](assets/opt-out-link-type.png)

1. No campo **[!UICONTROL Link]**, cole o link para a sua página de destino de terceiros.

   ![](assets/opt-out-link-url.png)

1. Clique em **[!UICONTROL Salvar]**.

### Implementar uma chamada de API para opção de não participação {#opt-out-api}

Para efetivar a opção de não participação dos seus recipients ao enviarem suas escolhas a partir da landing page, é necessário implementar uma **Chamada de API de assinatura** até [Adobe Developer](https://developer.adobe.com){target="_blank"} para atualizar as preferências dos perfis correspondentes.

Essa chamada POST é a seguinte:

Endpoint: https://platform.adobe.io/journey/imp/consent/preferences

Parâmetros de consulta:

* **params**: contém o conteúdo criptografado
* **pid**: ID de perfil criptografada

Esses três parâmetros serão incluídos no URL da página de destino de terceiros enviado ao seu destinatário:

![](assets/opt-out-parameters.png)

Requisitos do cabeçalho:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorização (token de usuário da conta técnica)

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

[!DNL Journey Optimizer] usará esses parâmetros para atualizar a escolha do perfil correspondente por meio da [Adobe Developer](https://developer.adobe.com){target="_blank"} chamada à API.

### Enviar a mensagem com link para cancelar inscrição {#send-message-unsubscribe-link}

Depois de configurar o link para cancelar inscrição para a página de destino e implementar a chamada de API, sua mensagem estará pronta para ser enviada.

1. Enviar a mensagem incluindo o link por meio de uma [jornada](../building-journeys/journey.md).

1. Depois que a mensagem for recebida, se o destinatário clicar no link de cancelamento de inscrição, a página de destino será exibida.

   ![](assets/opt-out-lp-example.png)

1. Se o destinatário enviar o formulário (aqui, pressionando o botão **Cancelar inscrição** na página de destino), os dados do perfil serão atualizados por meio da [chamada de API](#opt-out-api).

1. O destinatário que recusou a inscrição é então redirecionado para uma tela de mensagem de confirmação indicando que a recusa foi bem-sucedida.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, esse usuário não receberá a comunicação da sua marca, a menos que faça a assinatura novamente.

1. Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   Na guia **[!UICONTROL Atributos]**, é possível ver que o valor de **[!UICONTROL escolha]** foi alterado para **[!UICONTROL não]**.

## Recusar com um clique {#one-click-opt-out}

Para adicionar um link para opção de não participação no seu email, siga as etapas abaixo.

1. [Insira um link](../email/message-tracking.md#insert-links) e selecione **[!UICONTROL Opção de não participação em um clique]** como o tipo de link.

   ![](assets/message-tracking-opt-out.png)

1. Insira o URL da página de destino para onde o usuário será redirecionado após cancelar a inscrição. Esta página está aqui somente para confirmar a não participação.

   >[!NOTE]
   >
   >Se você ativou a opção **Lista-Cancelar inscrição** no nível de superfície de canal, esse URL também será usado quando os usuários clicarem no link de cancelamento de inscrição no cabeçalho do email. [Saiba mais](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Você pode personalizar seus links. Saiba mais sobre URLs personalizados [nesta seção](../personalization/personalization-syntax.md).

1. Selecione como deseja aplicar a opção de não participação: no nível de canal, identidade ou inscrição.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canal]**: a opção de não participação se aplica a mensagens futuras enviadas ao público-alvo do perfil (ou seja, endereço de email) do canal atual. Se vários destinos estiverem associados a um perfil, a opção de não participação se aplica a todos os destinos (ou seja, endereços de email) no perfil desse canal.
   * **[!UICONTROL Identidade]**: a opção de não participação se aplica a mensagens futuras enviadas ao público-alvo específico (ou seja, endereço de email) que está sendo usado para a mensagem atual.
   * **[!UICONTROL Assinatura]**: a opção de não participação se aplica a mensagens futuras associadas a uma lista de assinaturas específica. Essa opção só poderá ser selecionada se a mensagem atual estiver associada a uma lista de inscrições.

1. Salve as alterações.

Depois que a mensagem for enviada por meio de uma [jornada](../building-journeys/journey.md), se um destinatário clicar no link para opção de não participação, o perfil dele registrará imediatamente a opção de não participação.

## Link para cancelar inscrição no cabeçalho do email {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Adicionar link para cancelar inscrição ao cabeçalho do email"
>abstract="Ative o List-Unsubscribe para adicionar um link para cancelar inscrição ao cabeçalho do email. Para definir um URL para cancelar a inscrição, insira um link para opção de não participação de um clique no conteúdo da mensagem de email."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=pt-BR#one-click-opt-out" text="Recusar com um clique"

Se a [opção Lista-Cancelar inscrição](email-settings.md#list-unsubscribe) estiver ativada no nível da superfície de canal, os emails correspondentes enviados com o [!DNL Journey Optimizer] incluirão um link de cancelamento de inscrição no cabeçalho do email.

Por exemplo, o link para cancelar a inscrição será exibido assim no Gmail:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Para exibir o link para cancelar a inscrição no cabeçalho do email, o cliente de email dos destinatários deve ser compatível com esse recurso.

O endereço para cancelar a inscrição é o endereço **[!UICONTROL Mailto (cancelar assinatura)]** padrão exibido na superfície de canal correspondente. [Saiba mais](email-settings.md#list-unsubscribe)

Para definir um URL personalizado para cancelar a inscrição, insira um link de recusa de um clique no conteúdo da mensagem de email e insira o URL de sua escolha. [Saiba mais](#one-click-opt-out)

Dependendo do cliente de email, clicar no link para cancelar a inscrição no cabeçalho terá um dos seguintes resultados:

* A solicitação para cancelar a inscrição é enviada para o endereço de cancelamento de inscrição padrão.

* O destinatário é direcionado para o URL da página de destino que você especificou ao adicionar o link de opção de não participação à mensagem.

  >[!NOTE]
  >
  >Se você não adicionar um link de recusa de um clique no conteúdo da mensagem, nenhuma página de destino será exibida.

* O perfil correspondente é cancelado imediatamente e essa escolha é atualizada na Experience Platform. Saiba mais na [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target="_blank"}.
