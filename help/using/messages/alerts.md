---
title: Alertas em mensagens
description: Saiba como verificar a validação do conteúdo da mensagem e a solução de problemas
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 3%

---

# Verificar alertas em suas mensagens {#messages-alerts}

## Verificações antes do envio {#message-alerting}

Ao projetar suas mensagens, os alertas são exibidos na interface quando as configurações principais estão ausentes.

Os alertas são exibidos na parte superior direita da tela, ao editar o conteúdo da mensagem.

![](assets/alerts-details.png)

>[!NOTE]
>
>Se você não vir este botão, nenhum alerta foi detectado.

Dois tipos de alertas podem acontecer:

* **Avisos** consulte recomendações e práticas recomendadas. Por exemplo, uma mensagem será exibida se o link de recusa estiver ausente.

* **Erros** impedir que você teste ou ative a jornada, desde que elas não sejam resolvidas. Por exemplo, uma mensagem avisará que a linha de assunto está ausente.

Todos os avisos e erros possíveis são detalhados [below](#alerts-and-warnings).

>[!CAUTION]
>
> Você precisa resolver tudo **erro** antes de testar ou ativar a jornada usando a mensagem.

## Lista de avisos e erros {#alerts-and-warnings}

As configurações e elementos verificados pelo sistema estão listados abaixo. Você também encontrará informações sobre como adaptar sua configuração para resolver os problemas correspondentes.

**Avisos**:

* **[!UICONTROL The opt-out link is not present in the email body]**: adicionar um link de unsubscription ao corpo do email é uma prática recomendada. Saiba como configurá-lo em [esta seção](consent.md#opt-out-management).

   >[!NOTE]
   >
   >As mensagens de email do tipo Marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais. A categoria da mensagem (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactional]**) é definido na variável [superfície do canal](../configuration/channel-surfaces.md#email-type) (ou seja, predefinição de mensagem) e quando [criação da mensagem](get-started-content.md#create-new-message).

* **[!UICONTROL Text version of HTML is empty]**: não se esqueça de definir uma versão de texto do corpo do email, pois ela será usada quando o conteúdo do HTML não puder ser exibido. Saiba como criar a versão de texto em [esta seção](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body]**: verifique se todos os links no seu email estão corretos. Saiba como gerenciar conteúdo e links no [esta seção](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: para obter o delivery ideal, verifique se o tamanho do seu email não excede 100 KB. Saiba como editar conteúdo de email no [esta seção](../design/create-email-content.md).

**Erros**:

* **[!UICONTROL The subject line is missing]**: a linha de assunto do email é obrigatória. Saiba como defini-lo e personalizá-lo em [esta seção](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**: esse erro é exibido quando o corpo ou o título da notificação por push está ausente. Saiba como definir o conteúdo de notificação por push em [esta seção](create-push.md).

* **[!UICONTROL The email version of the message is empty]**: esse erro é exibido quando o conteúdo do email não foi configurado. Saiba como criar conteúdo de email no [esta seção](../design/design-emails.md).

* **[!UICONTROL Surface doesn’t exist]**: não será possível usar a mensagem se a superfície selecionada for excluída após a criação da mensagem. Se este erro ocorrer, selecione outra superfície na mensagem **[!UICONTROL Properties]**. Saiba mais sobre as superfícies dos canais em [esta seção](../configuration/channel-surfaces.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: o tamanho da notificação por push não pode exceder 4 KB. Para respeitar esse limite, tente reduzir o uso de imagens ou emojis. Saiba como gerenciar o conteúdo de notificação por push no [esta seção](create-push.md).

>[!CAUTION]
>
> Para poder usar sua mensagem, você precisa resolver tudo **erro** alertas.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
