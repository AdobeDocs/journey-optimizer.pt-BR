---
title: Gerenciar recusa
description: Saiba como gerenciar opções de rejeição e privacidade
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 5d1dc2d1711ba43b8270423acb1a5ca0ab862230
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 53%

---

# Gerenciar o consentimento {#consent}

Use o [!DNL Journey Optimizer] para rastrear o consentimento dos recipients para comunicação e entender como eles desejam se envolver com a marca gerenciando suas preferências e assinaturas.

Regulamentos como o GDPR afirmam que você deve estar em conformidade com requisitos específicos antes de poder usar informações de titulares de dados. Além disso, os titulares de dados devem poder modificar o consentimento a qualquer momento.

**Por que é importante?**

* O não cumprimento desses regulamentos traz riscos legais normativos para sua marca.
* Os regulamentos ajudam a evitar o envio de comunicações não solicitadas para seus recipients, o que pode fazer com que eles marquem suas mensagens como spam e prejudiquem sua reputação.

Saiba mais sobre como gerenciar a privacidade e os regulamentos aplicáveis na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Em [!DNL Journey Optimizer], o consentimento é tratado pelo Experience Platform [Esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. Por padrão, o valor do campo de consentimento fica vazio e é tratado como consentimento para receber suas comunicações. Você pode modificar esse valor padrão ao integrar a um dos valores possíveis listados [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.

## Gerenciamento de recusa de email {#opt-out-management}

Oferecer aos recipients a capacidade de cancelar a inscrição para receber comunicações de uma marca é um requisito legal. Saiba mais sobre a legislação aplicável na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=pt-BR#regulations){target=&quot;_blank&quot;}.

Portanto, você sempre deve incluir um **link para cancelar a inscrição** em cada email enviado aos recipients:

* Ao clicar nesse link, os recipients serão direcionados a uma landing page para confirmar a recusa.
* Após confirmar sua escolha, os dados dos perfis serão atualizados com essas informações.

### Opt out externo {#opt-out-external-lp}

Para fazer isso, você pode inserir um link para uma landing page externa em um email para permitir que os usuários cancelem a assinatura do recebimento de comunicações de sua marca.

#### Adicionar um link para cancelar a inscrição {#add-unsubscribe-link}

Primeiro, é necessário adicionar um link de cancelamento de subscrição em uma mensagem. Para fazer isso, siga as etapas abaixo:

1. Crie sua própria landing page de unsubscription.

1. Hospede-o no sistema de terceiros de sua preferência.

1. [Criar uma mensagem](create-message.md) no [!DNL Journey Optimizer].

1. Selecione o texto no seu conteúdo e [inserir um link](message-tracking.md#insert-links) usando a barra de ferramentas contextual.

   ![](assets/opt-out-insert-link.png)

1. Selecione o **[!UICONTROL External Opt-out/Unsubscription]** na lista suspensa **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. No **[!UICONTROL Link]** , cole o link na landing page de terceiros.

   ![](assets/opt-out-link-url.png)

1. Clique em **[!UICONTROL Save]**.

1. Salve o conteúdo e [publique a mensagem](publish-manage-message.md).

#### Implementar uma chamada de API para opção de não participação {#opt-out-api}

Para que seus recipients optem ao enviar sua escolha a partir da landing page, você deve implementar uma **Chamada da API de assinatura** no Adobe I/O para atualizar as preferências dos perfis correspondentes.

Essa chamada POST do Adobe I/O é a seguinte:

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

[!DNL Journey Optimizer] O usará esses parâmetros para atualizar a escolha do perfil correspondente por meio da chamada de Adobe I/O.

#### Enviar a mensagem com link de cancelamento de subscrição {#send-message-unsubscribe-link}

Depois de configurar o link de cancelamento de subscrição para a landing page e implementar a chamada à API, sua mensagem estará pronta para ser enviada.

1. Envie a mensagem incluindo o link por meio de um [jornada](../building-journeys/journey.md).

1. Depois que a mensagem for recebida, se o recipient clicar no link de cancelamento de inscrição, a página de aterrissagem será exibida.

   ![](assets/opt-out-lp-example.png)

1. Se o recipient enviar o formulário (aqui, pressionando o **Cancelar inscrição** na página de aterrissagem), os dados do perfil são atualizados por meio do [chamada de Adobe I/O](#opt-out-api).

1. O recipient que recusou a inscrição é então redirecionado para uma tela de mensagem de confirmação indicando que a recusa foi bem-sucedida.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, esse usuário não receberá a comunicação da sua marca, a menos que faça a assinatura novamente.

1. Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   Na guia **[!UICONTROL Attributes]**, é possível ver que o valor de **[!UICONTROL choice]** foi alterado para **[!UICONTROL no]**.

### Recusar com um clique {#one-click-opt-out}

À medida que muitos clientes buscam um processo mais fácil de cancelar inscrições, você também pode adicionar um link para opção de não participação com um clique no seu conteúdo de email. Esse link permitirá que seus recipients cancelem rapidamente a assinatura de suas comunicações, sem serem redirecionados para uma página de aterrissagem onde precisam confirmar sua escolha, o que acelera o processo de cancelamento de assinatura.

Para adicionar um link para opção de não participação no seu email, siga as etapas abaixo.

1. [Inserir um link](message-tracking.md#insert-links) e selecione **[!UICONTROL One click Opt-out]** como o tipo de link.

   ![](assets/message-tracking-opt-out.png)

1. Selecione como deseja aplicar a opção de rejeição: no canal, identidade ou nível de assinatura.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: A recusa se aplica a mensagens futuras enviadas ao destino do perfil (ou seja, endereço de email) do canal atual. Se vários destinos estiverem associados a um perfil, a recusa se aplica a todos os destinos (ou seja, endereços de email) no perfil desse canal.
   * **[!UICONTROL Identity]**: A recusa se aplica a mensagens futuras enviadas ao target específico (ou seja, endereço de email) que está sendo usado para a mensagem atual.
   * **[!UICONTROL Subscription]**: A recusa se aplica a mensagens futuras associadas a uma lista de assinaturas específica. Essa opção só poderá ser selecionada se a mensagem atual estiver associada a uma lista de assinaturas.

1. Insira o URL da landing page onde o usuário será redirecionado depois de cancelado a assinatura. Esta página está aqui somente para confirmar que a opção de rejeição foi bem-sucedida.

   ![](assets/message-tracking-opt-out-confirmation.png)

   Você pode personalizar seus links. Saiba mais sobre URLs personalizados em [esta seção](../personalization/personalization-syntax.md).

1. Salve as alterações.

Depois que a mensagem for enviada por meio de uma [jornada](../building-journeys/journey.md), se um recipient clicar no link, o perfil dele registrará imediatamente a opção de não participação.

### Cancelar assinatura do link no cabeçalho da mensagem {#unsubscribe-email}

Se o sistema de email dos destinatários suportar a exibição de um link de cancelamento de inscrição no cabeçalho do email, os emails enviados com o [!DNL Journey Optimizer] incluirão automaticamente este link.

Por exemplo, o link de cancelamento de inscrição será exibido assim no Gmail:

![](assets/unsubscribe-email.png)

Dependendo do sistema de email, clicar no link de cancelamento de inscrição no cabeçalho terá um dos seguintes resultados:

* O perfil correspondente é cancelado imediatamente e essa escolha é atualizada no Experience Platform. Saiba mais na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

* Isso tem o mesmo efeito que clicar no link de cancelamento de inscrição no conteúdo do email: o destinatário é redirecionado a uma página de aterrissagem, em que encontrará um botão para confirmar a recusa. Saiba mais sobre o gerenciamento de recusa [nesta seção](#opt-out-management).

## Encaminhar o gerenciamento de recusa {#push-opt-out-management}

Os recipients de push podem cancelar a inscrição por meio de seus próprios dispositivos.

Por exemplo, ao baixar ou ao usar seu aplicativo, eles podem optar por parar as notificações. Da mesma forma, é possível alterar as configurações de notificação por meio do sistema operacional móvel.
