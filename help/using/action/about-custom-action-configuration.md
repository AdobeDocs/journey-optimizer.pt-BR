---
solution: Journey Optimizer
title: Configure a custom action
description: Learn how to configure a custom action
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: a9c4bf20b170afd30ac17f6dec3778c1ae4be70c
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 6%

---

# Configure a custom action {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="If you are using a third-party system to send messages or if you want journeys to send API calls to a third-party system, use custom actions to configure its connection to your journey. [](https://developer.adobe.com/)"

If you are using a third-party system to send messages or if you want journeys to send API calls to a third-party system, use custom actions to configure its connection to your journey. [](https://developer.adobe.com)

Custom actions are additional actions defined by technical users and made available to marketers. **[!UICONTROL Action]** Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

[](../start/limitations.md)

In custom action parameters, you can pass a simple collection, as well as a collection of objects. [](../building-journeys/collections.md#limitations)

Also note that the custom actions parameters have an expected format (example: string, decimal, etc.). You must be careful to respect these expected formats. [](../building-journeys/collections.md)


## Etapas de configuração {#configuration-steps}

Here are the main steps required to configure a custom action:

1. **[!UICONTROL Configurations]** **[!UICONTROL Actions]****[!UICONTROL Manage]** **[!UICONTROL Create Action]** The action configuration pane opens on the right side of the screen.

   ![](assets/custom2.png)

1. Enter a name for your action.

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. Add a description to your action. Esta etapa é opcional.
1. **[!UICONTROL Used in]** **[!UICONTROL View journeys]**
1. **[!UICONTROL URL Configuration]** Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. **[!UICONTROL Authentication]** This configuration is the same as for data sources.  Consulte [esta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. **[!UICONTROL Action parameters]** Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Save]**.

   The custom action is now configured and ready to be used in your journeys. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >When a custom action is used in a journey, most parameters are read-only. **[!UICONTROL Name]****[!UICONTROL Description]****[!UICONTROL URL]****[!UICONTROL Authentication]**

## Configurar o URL {#url-configuration}

**[!UICONTROL URL Configuration]**

![](assets/journeyurlconfiguration.png)

1. **[!UICONTROL URL]**

   * If the URL is static, enter the URL in this field.

   * If the URL includes a dynamic path, enter only the static part of the URL, that is, the scheme, the host, the port, and, optionally, a static part of the path.

      Exemplo: `https://xxx.yyy.com/somethingstatic/`

      You will specify the dynamic path of the URL when adding the custom action to a journey. [Saiba mais](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >For security reasons, we strongly recommend that you use the HTTPS scheme for the URL. We don&#39;t allow the use of Adobe addresses that are not public and the use of IP addresses.
   >
   >Only the default ports are allowed when defining a custom action: 80 for http and 443 for https.

1. **[!UICONTROL Method]****[!UICONTROL POST]****[!UICONTROL PUT]**

   >[!NOTE]
   >
   > **** ****

1. **[!UICONTROL Headers]**
   1. **[!UICONTROL Add a header field]**
   1. Enter the key of the header field.
   1. **[!UICONTROL Variable]** **[!UICONTROL Constant]**

      For example, for a timestamp, you can set a dynamic value.

   1. **[!UICONTROL Constant]**

      **[!UICONTROL Variable]** [Saiba mais](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. **[!UICONTROL Delete]**
   **[!UICONTROL Content-Type]****[!UICONTROL Charset]** You cannot modify or delete these fields.

   After you have added the custom action to a journey, you can still add header fields to it if the journey is in draft status. If you do not want the journey to be affected by configuration changes, duplicate the custom action and add the header fields to the new custom action.

   >[!NOTE]
   >
   >Headers are validated according to field parsing rules. [](https://tools.ietf.org/html/rfc7230#section-3.2.4)

## Define the action parameters {#define-the-message-parameters}

![](assets/messageparameterssection.png)

**[!UICONTROL Action parameters]**

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Field names in the payload cannot contain a &quot;.&quot; caractere. They cannot start with a &quot;$&quot; character.

You will be able to define the parameter type (e.g.: string, integer, etc.).

You will also have a choice between specifying if a parameter is a constant or a variable:

* Constant means that the value of the parameter is defined in the action configuration pane by a technical persona. The value will be always the same across journeys. It will not vary and the marketer won’t see it when using the custom action in the journey. It could be for example an ID the third-party system expects. In that case, the field on the right of the toggle constant/variable is the value passed.
* Variable means the value of the parameter will vary. Marketers using this custom action in a journey will be free to pass the value they wants or to specify where to retrieve the value for this parameter (e.g. from the event, from Adobe Experience Platform, etc.). In that case, the field on the right of the toggle constant/variable is the label marketers will see in the journey to name this parameter.

![](assets/customactionpayloadmessage2.png)
