---
title: Gerenciar recusa
description: Saiba como gerenciar opções de rejeição e privacidade
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 98%

---

# Gerenciar recusa {#consent}

Use o [!DNL Journey Optimizer] para rastrear o consentimento dos recipients para comunicação e entender como eles desejam se envolver com a marca gerenciando suas preferências e assinaturas.

Regulamentos como o GDPR afirmam que você deve estar em conformidade com requisitos específicos antes de poder usar informações de titulares de dados. Além disso, os titulares de dados devem poder modificar o consentimento a qualquer momento.

**Por que é importante?**

* O não cumprimento desses regulamentos traz riscos legais normativos para sua marca.
* Os regulamentos ajudam a evitar o envio de comunicações não solicitadas para seus recipients, o que pode fazer com que eles marquem suas mensagens como spam e prejudiquem sua reputação.

Saiba mais sobre como gerenciar a privacidade e os regulamentos aplicáveis na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

## Gerenciamento de recusa {#opt-out-management}

Oferecer aos recipients a capacidade de cancelar a inscrição para receber comunicações de uma marca é um requisito legal. Saiba mais sobre a legislação aplicável na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=pt-BR#regulations){target=&quot;_blank&quot;}.

Portanto, você sempre deve incluir um **link para cancelar a inscrição** em cada email enviado aos recipients:

* Ao clicar nesse link, os recipients serão direcionados a uma página de aterrissagem que inclui um botão para confirmar a recusa.
* Ao clicar no botão de recusa, será feita uma chamada do Adobe I/O para atualizar os dados do perfil com essas informações. [Saiba mais](#consent-service-api).

### Adicionar um link para cancelar a inscrição {#add-unsubscribe-link}

Para adicionar um link de cancelamento de inscrição, siga as etapas abaixo:

1. Crie sua página de aterrissagem de unsubscription.

1. Hospede-o no sistema de terceiros de sua preferência.

1. [Criar uma mensagem](create-message.md) no [!DNL Journey Optimizer].

1. Selecione o texto no seu conteúdo e insira um link usando a barra de ferramentas contextual.

   ![](assets/opt-out-insert-link.png)

1. Selecione o **[!UICONTROL Unsubscription link]** na lista suspensa **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. No campo **[!UICONTROL Link]** cole o link para a sua página de aterrissagem.

   ![](assets/opt-out-link-url.png)

1. Clique em **[!UICONTROL Save]**.

1. Salve o conteúdo e [publique a mensagem](publish-manage-message.md).

   >[!NOTE]
   >
   >O URL da página de aterrissagem de terceiros incluirá três parâmetros que serão usados para atualizar as preferências dos perfis por meio de uma chamada do Adobe I/O. [Saiba mais nesta seção](#consent-service-api).

1. Envie sua mensagem com o link para a página de aterrissagem por meio de uma [jornada](../building-journeys/journey.md).

1. Depois que a mensagem for recebida, se o recipient clicar no link de cancelamento de inscrição, a página de aterrissagem será exibida.

   ![](assets/opt-out-lp-example.png)

1. Se o recipient clicar no botão de recusa na página de aterrissagem (aqui, o botão **Cancelar inscrição**), os dados do perfil serão atualizados por meio de uma [chamada do Adobe I/O](#opt-out-api).

   O recipient que recusou a inscrição é então redirecionado para uma tela de mensagem de confirmação indicando que a recusa foi bem-sucedida.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, esse usuário não receberá a comunicação da sua marca, a menos que faça a assinatura novamente.

Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target=&quot;_blank&quot;}.

![](assets/opt-out-profile-choice.png)

Na guia **[!UICONTROL Attributes]**, é possível ver que o valor de **[!UICONTROL choice]** foi alterado para **[!UICONTROL no]**.

### Chamada de API de recusa {#opt-out-api}

Depois que o recipient optar por cancelar a inscrição, uma API do Adobe I/Oserá chamada para atualizar a preferência do perfil correspondente.

Essa chamada POST do Adobe I/O é a seguinte:

Endpoint: platform.adobe.io/journey/imp/consent/preferences

Parâmetros de consulta:

* **params**: contém a carga criptografada
* **sig**: assinatura
* **pid**: ID de perfil criptografada

Esses parâmetros estão disponíveis no link de cancelamento de inscrição enviado para o recipient, ou seja, o URL que abrirá a página de aterrissagem de terceiros para determinado recipient:

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

[!DNL Journey Optimizer] usará esses parâmetros para atualizar a escolha do perfil correspondente.

## Recusar com um clique {#one-click-opt-out}

À medida que muitos clientes buscam um processo mais fácil de cancelar inscrições, você também pode adicionar um link para opção de não participação com um clique no seu conteúdo de email. Esse link permitirá que os seus recipients cancelem rapidamente a inscrição de suas comunicações, sem ser redirecionados para uma página de aterrissagem em que precisam confirmar o cancelamento.

Saiba como adicionar um link de opção de não participação ao conteúdo da sua mensagem [nesta seção](message-tracking.md#one-click-opt-out-link).

Depois que a mensagem for enviada por meio de uma [jornada](../building-journeys/journey.md), se um recipient clicar no link, o perfil dele registrará imediatamente a opção de não participação.

## Link de cancelamento de inscrição no cabeçalho {#unsubscribe-email}

Se o sistema de email dos destinatários suportar a exibição de um link de cancelamento de inscrição no cabeçalho do email, os emails enviados com o [!DNL Journey Optimizer] incluirão automaticamente este link.

Por exemplo, o link de cancelamento de inscrição será exibido assim no Gmail:

![](assets/unsubscribe-email.png)

Dependendo do sistema de email, clicar no link de cancelamento de inscrição no cabeçalho terá um dos seguintes resultados:

* O perfil correspondente é cancelado imediatamente e essa escolha é atualizada no Experience Platform. Saiba mais na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

* Isso tem o mesmo efeito que clicar no link de cancelamento de inscrição no conteúdo do email: o destinatário é redirecionado a uma página de aterrissagem, em que encontrará um botão para confirmar a recusa. Saiba mais sobre o gerenciamento de recusa [nesta seção](#opt-out-management).

## Encaminhar o gerenciamento de recusa {#push-opt-out-management}

Os recipients de push podem cancelar a inscrição por meio de seus próprios dispositivos.

Por exemplo, ao baixar ou ao usar seu aplicativo, eles podem optar por parar as notificações. Da mesma forma, é possível alterar as configurações de notificação por meio do sistema operacional móvel.
