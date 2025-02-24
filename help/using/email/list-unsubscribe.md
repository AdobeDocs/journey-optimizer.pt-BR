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
source-git-commit: b3655506dff97756a59a63d5b8f0c358dc7c7510
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 100%

---

# Cancelar assinatura em lista{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Ao criar uma nova configuração de canal de email, após [selecionar um subdomínio](email-settings.md#subdomains-and-ip-pools) na lista, a opção **[!UICONTROL Habilitar cancelamento de assinatura em lista]** é exibida.

![](assets/preset-list-unsubscribe.png)

## Habilitar cancelamento de assinatura em lista {#enable-list-unsubscribe}

Essa opção está habilitada por padrão para incluir um URL para cancelar inscrição com um clique no cabeçalho do email, como:

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Se desabilitar essa opção, nenhum URL para cancelar assinatura com um clique será exibido no cabeçalho do email.

O cabeçalho Cancelar assinatura em lista oferece duas opções que estão habilitadas por padrão, a menos que você desmarque uma ou ambas:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Um endereço **[!UICONTROL Mailto (cancelar assinatura)]**, que é o endereço de destino para o qual as solicitações para cancelar assinatura são encaminhadas para processamento automático.

  No [!DNL Journey Optimizer], o endereço de email para cancelamento de assinatura é o endereço **[!UICONTROL Mailto (cancelar assinatura)]** padrão exibido na configuração do canal, que se baseia no [subdomínio selecionado](#subdomains-and-ip-pools). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* O **[!UICONTROL URL para cancelar assinatura com um clique]**, que por padrão é o gerado para o cabeçalho para cancelar assinatura em lista com base no subdomínio definido nas configurações do canal.  <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Você pode selecionar o **[!UICONTROL Nível de consentimento]** na lista suspensa correspondente. Essa configuração pode ser específica para o canal ou para a identidade do perfil. Quando alguém cancelar a assinatura em lista usando o URL no cabeçalho de um email, essa configuração define se o consentimento é atualizado no [!DNL Adobe Journey Optimizer] no nível do canal ou no nível da ID.

Os recursos **[!UICONTROL Mailto (cancelar assinatura)]** e **[!UICONTROL URL para cancelar assinatura com um clique]** são opcionais.

Se não quiser usar o URL para cancelar assinatura com um clique gerado por padrão, é possível desmarcar o recurso. Se a opção **[!UICONTROL Habilitar cancelamento de assinatura em lista]** estiver ativada, o recurso **[!UICONTROL URL de cancelamento de assinatura com um clique]** estiver desmarcado e você adicionar um [link para opção de não participação com um clique](../email/email-opt-out.md#one-click-opt-out) a uma mensagem criada usando essa configuração, o cabeçalho de cancelamento de assinatura em lista definirá o link de um clique inserido no corpo do email como o URL de cancelamento de assinatura.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Se você não adicionar um link para opção de não participação com um clique no conteúdo da mensagem e o **[!UICONTROL URL para cancelar assinatura com um clique]** padrão estiver desmarcado nas configurações do canal, nenhum URL será associado ao cabeçalho de email para cancelar assinatura da lista.

Saiba mais sobre como gerenciar recursos para cancelar assinatura em suas mensagens [nesta seção](../email/email-opt-out.md#unsubscribe-header).

## Gerenciar dados de cancelamento de assinatura externamente {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definir como os dados de cancelamento de assinatura são gerenciados"
>abstract="**Gerenciado pela Adobe**: os dados de consentimento são gerenciados por você no sistema da Adobe.<br>**Gerenciado pelo cliente**: os dados de consentimento são gerenciados por você em um sistema externo e não são sincronizados com o sistema da Adobe, a menos que esse processo seja iniciado por você."

Se estiver gerenciando dados de consentimento fora da Adobe, selecione a opção **[!UICONTROL Gerenciado pelo cliente]** para inserir um endereço de email de cancelamento de assinatura personalizado e seu próprio URL de cancelamento de assinatura com um clique. 

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Se estiver usando a opção **[!UICONTROL Gerenciado pelo cliente]**, a Adobe não armazenará dados de cancelamento de assinatura ou consentimento. Com a opção **[!UICONTROL Gerenciado pelo cliente]**, as organizações optam por usar um sistema externo e são responsáveis por gerenciar seus dados de consentimento nesse sistema. Não há sincronização automática de dados de consentimento entre o sistema externo e o [!DNL Journey Optimizer]. Ao sincronizar dados de consentimento do sistema externo com o [!DNL Journey Optimizer], o processo deve ser iniciado pela organização como uma transferência de dados para que os dados sejam enviados ao [!DNL Journey Optimizer].

### Configurar a API de descriptografia {#configure-decrypt-api}

Com a opção **[!UICONTROL Gerenciado pelo cliente]** selecionada, se você inserir pontos de acesso personalizados e usá-los em uma campanha ou jornada, o [!DNL Journey Optimizer] anexará por padrão alguns parâmetros específicos do perfil ao evento de atualização de consentimento <!--sent to the custom endpoint --> quando os destinatários clicarem no link para cancelar assinatura.

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

+++
