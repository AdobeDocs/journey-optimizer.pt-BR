---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar recusa
description: Saiba como gerenciar opções de rejeição e privacidade
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Gerenciar recusa {#consent}

## Sobre o gerenciamento de não participação {#about}

Fornecer a capacidade de cancelar a assinatura dos recipients ao receberem comunicações de uma marca é um requisito legal. Saiba mais sobre a legislação aplicável no [Documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**Por que é importante?**

* O não cumprimento desses regulamentos introduz riscos legais normativos para sua marca.
* Ajuda a evitar o envio de comunicações não solicitadas para seus recipients, o que pode fazer com que eles marquem suas mensagens como spam e prejudiquem sua reputação.

## Gerenciamento de rejeição no Journey Otimizer {#opt-out-ajo}

Ao enviar mensagens de jornadas ou campanhas, você deve sempre garantir que os clientes possam cancelar a assinatura de comunicações futuras. Após a unsubscription, os perfis serão removidos automaticamente do público-alvo de futuras mensagens de marketing.

Ao **[!DNL Journey Optimizer]** fornece maneiras de gerenciar a recusa em emails e mensagens SMS, as notificações por push não exigem nenhuma ação do seu lado, pois os recipients podem cancelar a assinatura por meio dos próprios dispositivos. Por exemplo, ao baixar ou ao usar seu aplicativo, eles podem optar por parar as notificações. Da mesma forma, é possível alterar as configurações de notificação por meio do sistema operacional móvel.

Saiba como gerenciar opções de rejeição em emails e mensagens SMS do Journey Otimizer nestas seções:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Líder" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Gerenciamento de recusa de email</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Pouco frequentes" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>Gerenciamento de recusa de SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>Em [!DNL Journey Optimizer], o consentimento é tratado pela Experience Platform [Esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. Por padrão, o valor do campo de consentimento fica vazio e é tratado como consentimento para receber suas comunicações. Você pode modificar esse valor padrão ao integrar a um dos valores possíveis listados [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.