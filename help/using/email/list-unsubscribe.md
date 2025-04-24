---
solution: Journey Optimizer
product: journey optimizer
title: Configurar cancelamento de assinatura em lista
description: Saiba como incluir um URL para cancelar assinatura de um clique no cabeçalho dos emails ao configurar o canal
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: definições, email, configuração
exl-id: c6c77975-ec9c-44c8-a8d8-50ca6231fea6
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: ht
source-wordcount: '1371'
ht-degree: 100%

---

# Cancelar assinatura em lista{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

No [!DNL Adobe Journey Optimizer], ao definir uma nova configuração de canais de email, após [selecionar um subdomínio](email-settings.md#subdomains-and-ip-pools) da lista, a opção **[!UICONTROL Habilitar cancelamento de assinatura na lista]** é exibida. Esta opção está habilitada por padrão.

![](assets/preset-list-unsubscribe.png)

O “URL de cancelamento de assinatura de lista com um clique” é um link ou botão exibido ao lado das informações do remetente do email e permite que destinatários cancelem instantaneamente a assinatura de listas de recebimento de email com um único clique.

Por exemplo, no Gmail, o URL de cancelamento de assinatura com um clique exibe o seguinte link:

![](assets/preset-list-unsubscribe-header.png)

>[!IMPORTANT]
>
>Para exibir o URL de cancelamento de assinatura com um clique no cabeçalho do email, o cliente de email dos destinatários deve oferecer suporte a esse recurso.

Dependendo do cliente de email e das configurações de cancelamento de assinatura do email, clicar no link de cancelamento no cabeçalho do email pode ter os seguintes impactos:

* Quando o recurso **Mailto (cancelar assinatura)** está habilitado, a solicitação de cancelamento é enviada para o endereço de cancelamento padrão com base no subdomínio configurado.
* Quando o recurso **URL de cancelamento de iassinatura  com um clique** está habilitado, ou se você inseriu um URL de cancelamento de assinatura no conteúdo do corpo do email, a inscrição do destinatário é cancelada diretamente no nível do canal ou da ID (dependendo da configuração de consentimento) após clicar no URL de cancelamento de assinatura com um clique (com base no subdomínio configurado).

>[!NOTE]
>
>Aprenda como gerenciar as configurações de cancelamento de inscrição [nesta seção](#enable-list-unsubscribe) abaixo.

Em ambos os casos, quando um destinatário clica no link de opção de não participação, sua solicitação de cancelamento de assinatura é processada adequadamente. O perfil correspondente é imediatamente excluído da lista e essa escolha é atualizada na [Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target="_blank"}.

>[!NOTE]
>
>Ocasionalmente, eventos de cancelamento de assinatura podem demorar mais para serem aplicados no nível do perfil devido ao processamento de dados posteriores. Aguarde um tempo para que o sistema seja atualizado.

## Habilitar cancelamento de assinatura na lista {#enable-list-unsubscribe}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Adicionar um URL de cancelamento de assinatura nos emails"
>abstract="Habilite esta opção para adicionar automaticamente um URL de cancelamento de assinatura no cabeçalho do email. É possível também definir um URL de cancelamento de assinatura em uma mensagem ao inserir um link para opção de não participação com um clique no conteúdo do email."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Adicionar a opção de não participação com um clique no conteúdo do email"

Quando a opção **[!UICONTROL Habilitar cancelamento de assinatura na lista]** está habilitada, e se o recurso for compatível com o cliente de email dos destinatários, o cabeçalho do email incluirá por padrão um mailto e/ou um URL que permite cancelar a assinatura da lista de recebimento de emails.

>[!NOTE]
>
>Se desabilitar essa opção, nenhum URL para cancelar assinatura com um clique será exibido no cabeçalho do email.

O cabeçalho Cancelar assinatura em lista oferece duas opções que estão habilitadas por padrão, a menos que você desmarque uma ou ambas:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Um endereço **[!UICONTROL Mailto (cancelar assinatura)]**, que é o endereço de destino para onde as solicitações de cancelamento de assinatura são encaminhadas para processamento automático. No [!DNL Journey Optimizer], o endereço de email para cancelamento de assinatura é o endereço **[!UICONTROL Mailto (cancelar assinatura)]** padrão exibido na configuração de canais, com base no [subdomínio selecionado](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* O **[!UICONTROL URL de cancelamento de assinatura com um clique]**, que por padrão é o URL de opção de não participação adicionado ao cabeçalho de cancelamento de assinatura em lista, com base no [subdomínio selecionado](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Você pode selecionar o **[!UICONTROL Nível de consentimento]** na lista suspensa correspondente. Essa configuração pode ser específica para o canal ou para a identidade do perfil. Quando alguém cancelar a assinatura em lista usando o URL no cabeçalho de um email, essa configuração define se o consentimento é atualizado no [!DNL Adobe Journey Optimizer] no nível do canal ou no nível da ID.

## Medidas de proteção e recomendações {#list-unsubscribe-guardrails}

O recurso de URL de cancelamento de assinatura com um clique permite que seus destinatários cancelem facilmente o recebimento de suas comunicações. No entanto, como nem todos os clientes de email permitem a adição desse link no cabeçalho do email, a Adobe também recomenda adicionar um [link de opção de não participação com um clique](email-opt-out.md#one-click-opt-out) ou um [link de cancelamento de assinatura](email-opt-out.md#add-unsubscribe-link) no corpo do email.

Os recursos **[!UICONTROL Mailto (cancelar assinatura)]** e **[!UICONTROL URL de cancelamento de assinataura com um clique]** são opcionais.

* Se você tiver ativado a opção **[!UICONTROL Habilitar cancelamento de assinatura na lista]** nas [configurações de email](email-settings.md), recomendamos habilitar ambos os métodos: **Mailto (cancelar assinatura)** e **URL de cancelamento de assinataura com um clique**. Nem todos os clientes de email aceitam o método HTTP. Com o recurso de cancelamento de assinatura na lista de Mailto, que permite selecionar uma alternativa, é possível proteger melhor sua reputação de remetente e garantir que todos os seus destinatários tenham acesso à funcionalidade de cancelamento de assinatura.

* Se não quiser usar o URL de cancelamento de assinatura padrão gerado com um clique, você pode desmarcar o recurso.

   * Se a opção **[!UICONTROL Habilitar cancelamento de assinatura em lista]** estiver ativada, o recurso **[!UICONTROL URL de cancelamento de assinatura com um clique]** estiver desmarcado e você adicionar um [link para opção de não participação com um clique](../email/email-opt-out.md#one-click-opt-out) a uma mensagem criada usando essa configuração, o cabeçalho de cancelamento de assinatura em lista definirá o link de um clique inserido no corpo do email como o URL de cancelamento de assinatura.

     ![](assets/preset-list-unsubscribe-opt-out-url.png)

   * Se você não adicionar um link para opção de não participação com um clique no conteúdo da mensagem e o **[!UICONTROL URL para cancelar assinatura com um clique]** padrão estiver desmarcado nas configurações do canal, nenhum URL será associado ao cabeçalho de email para cancelar assinatura da lista.

  >[!NOTE]
  >
  >Saiba mais sobre como gerenciar recursos de cancelamento de assinatura em suas mensagens [nesta seção](../email/email-opt-out.md#unsubscribe-header).

No [!DNL Journey Optimizer], o consentimento é tratado pelo [Esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=pt-BR) da Experience Platform{target="_blank"}. Por padrão, o valor do campo de consentimento fica vazio e é tratado como consentimento para receber suas comunicações. É possível modificar esse valor padrão durante a integração para um dos valores possíveis listados [aqui](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=pt-BR#choice-values){target="_blank"}, ou usar [políticas de consentimento](../action/consent.md) para substituir a lógica padrão.

Atualmente, o [!DNL Journey Optimizer] não anexa uma tag específica aos eventos de cancelamento de assinatura acionados pelo recurso de cancelamento de assinatura na lista. Se você precisar diferenciar os cliques de cancelamento de asssinatura na lista de outras ações de cancelamento de assinatura, será necessário implementar a marcação personalizada externamente ou utilizar uma página de destino externa para rastreamento.

## Gerenciar dados de cancelamento de assinatura externamente {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definir como os dados de cancelamento de assinatura são gerenciados"
>abstract="**Gerenciado pela Adobe**: os dados de consentimento são gerenciados por você no sistema da Adobe.<br>**Gerenciado pelo cliente**: os dados de consentimento são gerenciados por você em um sistema externo e não são sincronizados com o sistema da Adobe, a menos que esse processo seja iniciado por você."

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom_url"
>title="Insira seu próprio URL de cancelamento de assinatura com um clique"
>abstract="O **URL de cancelamento de assinataura com um clique** deve usar o método de solicitação POST."

Se estiver gerenciando dados de consentimento fora da Adobe, selecione a opção **[!UICONTROL Gerenciado pelo cliente]** para inserir um endereço de email de cancelamento de assinatura personalizado e seu próprio URL de cancelamento de assinatura com um clique. 

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

O **[!UICONTROL URL de cancelamento de assinataura com um clique]** deve ser um URL POST.

>[!WARNING]
>
>Se estiver usando a opção **[!UICONTROL Gerenciado pelo cliente]**, a Adobe não armazenará dados de cancelamento de assinatura ou consentimento. Com a opção **[!UICONTROL Gerenciado pelo cliente]**, as organizações optam por usar um sistema externo e são responsáveis por gerenciar seus dados de consentimento nesse sistema. Não há sincronização automática de dados de consentimento entre o sistema externo e o [!DNL Journey Optimizer]. Ao sincronizar dados de consentimento do sistema externo com o [!DNL Journey Optimizer], o processo deve ser iniciado pela organização como uma transferência de dados para que os dados sejam enviados ao [!DNL Journey Optimizer].

### Configurar a API de descriptografia {#configure-decrypt-api}

Com a opção **[!UICONTROL Gerenciado pelo cliente]** selecionada, se você inserir pontos de acesso personalizados e usá-los em uma campanha ou jornada, o [!DNL Journey Optimizer] acrescentará alguns parâmetros específicos do perfil padrão ao evento de atualização de consentimento <!--sent to the custom endpoint --> quando seus destinatários clicarem no link de cancelamento de assinatura.

Esses parâmetros são enviados para o ponto de acesso de maneira criptografada. Assim, o sistema de consentimento externo precisa implementar uma API específica por meio do [Adobe Developer](https://developer.adobe.com){target="_blank"} para descriptografar os parâmetros enviados pela Adobe.

A chamada GET para recuperar esses parâmetros depende da opção de cancelamento de assinatura em lista que você utiliza: **[!UICONTROL URL de cancelamento de assinatura com um clique]** ou **[!UICONTROL Mailto (cancelar assinatura)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL para cancelar assinatura com um clique

Se você utiliza a opção **[!UICONTROL URL para cancelar assinatura com um clique]**, clicar no link cancelará diretamente a assinatura do usuário.

A chamada GET é a seguinte:

Ponto de acesso: https://platform.adobe.io/journey/imp/consent/decrypt

Parâmetros de consulta:

* **params**: contém o conteúdo criptografado
* **pid**: ID de perfil criptografada

Esses dois parâmetros serão incluídos no evento de atualização de consentimento enviado aos pontos de acesso personalizados.

Requisitos do cabeçalho:

* x-api-key
* x-gw-ims-org-id
* autorização (token de usuário da conta técnica)

Veja abaixo exemplos de parâmetros e a resposta de consentimento:

| Parâmetros de consulta | Conteúdo de exemplo |
|---------|----------|
| pid | {<br>&quot;pid&quot;  : &quot;5142733041546020095851529937068211571&quot;,<br>&quot;pns&quot;  : &quot;CRMID&quot;,<br>&quot;e&quot;    : &quot;john@google.com&quot;,<br>&quot;ens&quot;  : &quot;Email&quot;,<br>} |
| params | {<br>&quot;m&quot;  : &quot;messageExecutionId&quot;,<br>&quot;ci&quot;  : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;s&quot;  : &quot;sandboxId&quot;,<br>&quot;us&quot; : &quot;unsubscribeScope&quot;<br>} |

Resposta de consentimento:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++

+++ Mailto (cancelar assinatura)

Se você utiliza a opção **[!UICONTROL Mailto (cancelar assinatura)]**, clicar no link de cancelamento de assinatura enviará um email pré-preenchido para o endereço de cancelamento especificado.

A chamada GET é a seguinte.

Ponto de acesso: https://platform.adobe.io/journey/imp/consent/decrypt

Parâmetros de consulta:

* **emailParams**: string que contém os parâmetros **params** (conteúdo criptografado) e **pid** (ID do perfil criptografada).

Os parâmetros **params** e **pid** serão incluídos no evento de atualização de consentimento enviado aos pontos de acesso personalizados.

Requisitos do cabeçalho:

* x-api-key
* x-gw-ims-org-id
* autorização (token de usuário da conta técnica)

Veja abaixo exemplos de parâmetros e a resposta de consentimento:

| Parâmetros de consulta | Conteúdo de exemplo |
|---------|----------|
| emailParams | {<br>&quot;p&quot;  : &quot;profileId&quot;,<br>&quot;pn&quot;  : &quot;profileNamespace&quot;,<br>&quot;en&quot;  : &quot;emailNamespace&quot;,<br>&quot;ci&quot;  : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;si&quot;  : &quot;sandboxId&quot;,<br>&quot;us&quot;: &quot;unsubscribeScope&quot;<br>} |

Resposta de consentimento:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++
