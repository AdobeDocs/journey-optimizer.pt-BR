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
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 42%

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

1. Criar um [Público-alvo do Adobe Experience Platform](../audience/access-audiences.md) usando o [Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"} e usar um atributo de perfil, como **[!UICONTROL Personalizar conteúdo = Sim (aceitação)]** para direcionar usuários que consentiram com a personalização.

   ![](assets/perso-consent-od-audience.png)

1. Ao criar uma [decisão](../offers/offer-activities/create-offer-activities.md), adicione um escopo de decisão e defina uma restrição de qualificação com base nesse público-alvo para cada coleção de critérios de avaliação que contenha ofertas personalizadas.

   ![](assets/perso-consent-od-audience-decision.png)

1. Crie uma [oferta substituta](../offers/offer-library/creating-fallback-offers.md) que não inclua conteúdo personalizado.

1. [Atribua](../offers/offer-activities/create-offer-activities.md#add-fallback) a oferta substituta não personalizada à decisão.

   ![](assets/perso-consent-od-audience-fallback.png)

1. [Revise e salve](../offers/offer-activities/create-offer-activities.md#review) a decisão.

Se um usuário:

* tiver consentido a personalização, o escopo da decisão determinará a melhor oferta para esse perfil.

* não tiver consentido a personalização, o perfil correspondente não será qualificado para nenhuma das ofertas que estão nos critérios de avaliação e, portanto, receberá a oferta substituta não personalizada.

>[!NOTE]
>
>O consentimento para que os dados do perfil sejam usados na [modelagem de dados](../offers/ranking/ai-models.md) ainda não é aceito no [!DNL Journey Optimizer].

## No editor de expressão

<!--Expressions Editor while personalizing images, text, subject line  ( Segment in Campaigns) - UI and Headless -->

A variável [Editor de expressão](../personalization/personalization-build-expressions.md) O não executa, por si só, nenhuma verificação de consentimento ou imposição, pois não está envolvido na entrega de mensagens.

No entanto, o uso de rótulos de controle de acesso baseados na direita permite restringir quais campos podem ser usados para personalização. A variável [pré-visualização de mensagem](../email/preview.md#preview-email) e [serviço de renderização de email](../email/preview.md#email-rendering) mascarará os campos identificados com informações confidenciais.

>[!NOTE]
>
>Saiba mais sobre o Controle de acesso em nível de objeto (OLAC) em [nesta seção](../administration/object-based-access.md).


Entrada [!DNL Journey Optimizer] , a política de consentimento é imposta da seguinte maneira:

* É possível incluir definições de política de consentimento como parte da criação do público-alvo para garantir que o público-alvo selecionado para a campanha já tenha **perfis filtrados que não correspondem aos critérios de consentimento**.

* [!DNL Journey Optimizer] realizará uma verificação de consentimento geral no nível do canal para **verifique se os perfis aceitaram** para receber comunicações de marketing no canal correspondente.

  >[!NOTE]
  >
  >A variável [!DNL Journey Optimizer] o próprio objeto campaign não executa verificações adicionais de aplicação da política de consentimento no momento.

Para aplicar manualmente o consentimento de personalização em campanhas, siga uma das opções abaixo.

### Uso do construtor de regras de segmento

Você pode usar o construtor de regras de segmento para criar um público-alvo contendo perfis de recusa.

1. Criar um [Público-alvo do Adobe Experience Platform](../audience/access-audiences.md) usando o [Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/perso-consent-audience-build-rule.png)

1. Selecione um atributo de perfil, como **[!UICONTROL Personalizar conteúdo = Não (recusar)]** para excluir usuários que não consentiram com a personalização.

   ![](assets/perso-consent-audience-no.png)

1. Clique em **[!UICONTROL Salvar]**.

Agora você pode usar esse público para filtrar os perfis que não consentiram com a personalização de suas campanhas.

### Uso de uma atividade Split em um fluxo de trabalho de composição

Você também pode adicionar uma verificação de consentimento de personalização a um público-alvo adicionando uma atividade dividida a um fluxo de trabalho de composição.

1. Criar um público-alvo usando o **[!UICONTROL Compor público]** opção. [Saiba mais sobre como criar um fluxo de trabalho de composição](../audience/create-compositions.md)

   ![](assets/perso-consent-audience-compose.png)

1. Adicione o público inicial usando o botão dedicado à direita.

1. Clique no ícone + e selecione **[!UICONTROL Split]** para criar um público-alvo dividido. [Saiba mais sobre a atividade de Split](../audience/composition-canvas.md#split)

   ![](assets/perso-consent-audience-split.png)

1. Selecionar **[!UICONTROL Divisão de atributo]** como o tipo de divisão no painel direito.

   ![](assets/perso-consent-audience-attribute-split.png)

1. Clique no ícone de lápis ao lado da **[!UICONTROL Atributo]** campo para exibir a **[!UICONTROL Selecionar um atributo de perfil]** janela.

1. Pesquisar o atributo de consentimento de personalização (`profile.consents.personalize.content.val`) e selecione-o.

   ![](assets/perso-consent-audience-consent-attribute.png)

1. **[!UICONTROL Caminho 1]** será o público-alvo não personalizado. Escolha um rótulo relevante.

1. Escolha o valor apropriado entre este [lista](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=pt-BR#choice-values){target="_blank"}.

   Nesse caso, usaremos `n` para indicar que os usuários não consentiram com o uso de seus dados para personalização.

   ![](assets/perso-consent-audience-path-1-n.png)

1. Você pode criar um caminho separado para outros valores de escolha. Você também pode optar por excluir os caminhos restantes e ativar **[!UICONTROL Outros perfis]** para incluir todos os outros perfis que não tinham um valor de opção de `n`.

1. Quando terminar, clique em **[!UICONTROL Salvar público-alvo]** para cada caminho para salvar o resultado do fluxo de trabalho em um novo público-alvo. Um público-alvo será salvo no Adobe Experience Platform para cada caminho.

1. Depois de concluído, publique o fluxo de trabalho de composição.

Agora você pode usar esse público para filtrar os perfis que não consentiram com a personalização de suas campanhas.

>[!NOTE]
>
>Se você criar um público-alvo que não consentiu com a personalização e depois selecionar esse público-alvo em uma campanha, as ferramentas de personalização permanecerão disponíveis. Cabe aos usuários de marketing entender que, se estiverem trabalhando com um público-alvo que não deve receber personalização, eles não devem usar ferramentas de personalização.
