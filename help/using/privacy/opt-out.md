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
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: ht
source-wordcount: '478'
ht-degree: 100%

---

# Gerenciar recusa {#consent}

Fornecer aos destinatários a capacidade de cancelar inscrição do recebimento de comunicações de uma marca é um requisito legal, bem como garantir que essa escolha seja respeitada. Saiba mais sobre a legislação aplicável na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=pt-BR#regulations){target="_blank"}.

**Por que é importante?**

* O não cumprimento desses regulamentos traz riscos legais normativos para sua marca.
* Os regulamentos ajudam a evitar o envio de comunicações não solicitadas para seus recipients, o que pode fazer com que eles marquem suas mensagens como spam e prejudiquem sua reputação.

## Gerenciar cancelamentos de inscrições em jornadas e campanhas {#opt-out-ajo}

Ao enviar mensagens de jornadas ou campanhas, você deve sempre garantir que os clientes possam cancelar a inscrição de comunicações futuras. Após o cancelamento da assinatura, os perfis serão removidos automaticamente do público-alvo de futuras mensagens de marketing.

Embora o **[!DNL Journey Optimizer]** forneça maneiras de gerenciar a opção de não participação em emails e mensagens SMS, as notificações por push não exigem nenhuma ação da sua parte, pois os destinatários podem cancelar a inscrição por meio dos seus próprios dispositivos. Por exemplo, ao baixar ou ao usar seu aplicativo, eles podem optar por parar as notificações. Da mesma forma, é possível alterar as configurações de notificação por meio do sistema operacional móvel.

Saiba como gerenciar a opção de não participação em emails e mensagens SMS do Journey Optimizer nestas seções:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Cliente potencial" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Gerenciamento de opção de não participação de email</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Pouco frequentes" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>Gerenciamento de opção de não participação de SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>No [!DNL Journey Optimizer], o consentimento é tratado pelo [Esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=pt-BR) da Experience Platform{target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=pt-BR#choice-values){target="_blank"}.

## Implementar consentimento de personalização {#opt-out-personalization}

Seus clientes também podem recusar a apresentação de conteúdo personalizado. Depois que um perfil recusar a personalização, será necessário garantir que seus dados não sejam usados para personalização, e qualquer conteúdo personalizado deve ser substituído por uma variante de fallback.

### Na Gestão de decisões

Ao usar ofertas, as preferências de personalização não são implementadas automaticamente nos [escopos de decisão](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) usados a partir de uma solicitação de API de [decisão](../offers/api-reference/offer-delivery-api/decisioning-api.md) ou de [decisão de borda](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md). Nesse caso, é necessário impor manualmente o consentimento da personalização. Para isso, siga as etapas abaixo.

>[!NOTE]
>
>Os escopos de decisão usados em canais de criação do [!DNL Journey Optimizer] atendem a esse requisito da jornada ou campanha a qual pertencem.



1. Crie um [segmento da Adobe Experience Platform](../segment/about-segments.md) usando um atributo de perfil como: *“Consentimentos para personalização = True”* para direcionar usuários que consentiram com a personalização.

1. Ao criar uma [decisão](../offers/offer-activities/create-offer-activities.md), adicione um escopo de decisão e defina uma restrição de elegibilidade com base nesse segmento para cada coleção de critérios de avaliação que contenha ofertas personalizadas.

1. Crie uma [oferta substituta](../offers/offer-library/creating-fallback-offers.md) que não inclua conteúdo personalizado.

1. [Atribua](../offers/offer-activities/create-offer-activities.md#add-fallback) a oferta substituta não personalizada à decisão.

1. [Revise e salve](../offers/offer-activities/create-offer-activities.md#review) a decisão.

Se um usuário:

* tiver consentido a personalização, o escopo da decisão determinará a melhor oferta para esse perfil.

* não tiver consentido a personalização, o perfil correspondente não será qualificado para nenhuma das ofertas que estão nos critérios de avaliação e, portanto, receberá a oferta substituta não personalizada.

>[!NOTE]
>
>O consentimento para que os dados do perfil sejam usados na [modelagem de dados](../offers/ranking/ai-models.md) ainda não é aceito no [!DNL Journey Optimizer].

