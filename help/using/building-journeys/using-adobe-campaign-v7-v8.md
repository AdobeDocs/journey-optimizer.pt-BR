---
solution: Journey Optimizer
product: journey optimizer
title: Ações do Adobe Campaign v7/v8
description: Saiba mais sobre as ações do Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: jornada, integração, campaign, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 28%

---

# Ações do [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Ações personalizadas"
>abstract="Uma integração está disponível caso você tenha o [!DNL Adobe Campaign] v7 ou v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do [!DNL Adobe Campaign]."

Uma integração está disponível caso você tenha o [!DNL Adobe Campaign] v7 ou v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do [!DNL Adobe Campaign].

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento. Entre em contato com a Adobe.

**Quando usar**: usar ações do Campaign v7/v8 quando suas mensagens dependerem de modelos transacionais do Campaign, modelos de dados específicos do Campaign ou fluxos de trabalho de entrega do Campaign existentes.

**Pré-requisitos**

* Sua instância do [!DNL Adobe Campaign] v7/v8 foi provisionada e conectada ao Journey Optimizer pela Adobe.
* Você tem acesso a Mensagens transacionais do Campaign e as permissões necessárias.

Para que isso funcione, é necessário configurar uma ação dedicada. Consulte esta [seção](../action/acc-action.md).

Um caso de uso completo é apresentado nesta [seção](../building-journeys/ajo-ac.md).

1. Projete sua jornada, começando com um evento. Consulte esta [seção](../building-journeys/journey.md).
1. Na seção **Ação** da paleta, selecione uma ação de Campanha e adicione-a à sua jornada.
1. Nos **Parâmetros de ação**, todos os campos esperados na carga da mensagem são exibidos. Você precisa mapear cada um desses campos com o campo que deseja usar, seja do evento ou da fonte de dados. Isso é semelhante às ações personalizadas. Consulte esta [seção](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* As ações do Campaign v7/v8 podem ser usadas junto a ações de canal nativo na mesma jornada. Isso não se aplica às ações do Campaign Standard. Consulte [Medidas de proteção de atividades de campanha](../start/guardrails.md#ac-g).
>* As ações do Campaign v7/v8 não podem ser usadas com atividades Ler público ou Qualificar público. Consulte as medidas de proteção Ler público-alvo e qualificação de público-alvo na página Medidas de proteção.

![[!DNL Adobe Campaign] configurações de ação e integração v7/v8](assets/accintegration2.png)
