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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 11%

---

# Ações do [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a integração do Adobe Campaign v7 e v8 para enviar emails, notificações por push e SMS de suas jornadas por meio de mensagens transacionais do Campaign.

>[!ENDSHADEBOX]

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como usar o Adobe Campaign v7/v8 como uma ação no Journey Optimizer jornada para enviar emails, notificações por push e SMS via Mensagens Transacionais do Campaign.

**Intenções:**

* Adicionar uma ação do Campaign v7/v8 a uma jornada para enviar mensagens transacionais
* Mapear campos de evento de jornada ou fonte de dados para os parâmetros de carga da mensagem do Campaign
* Combinar ações do Campaign v7/v8 com ações de canal nativas do Journey Optimizer na mesma jornada
* Configurar a ação dedicada necessária para a integração do Campaign v7/v8

**Glossário:**

* **Mensagens Transacionais de Campanha**: recurso do Adobe Campaign v7/v8 para enviar mensagens acionadas (email, SMS, push) por meio de uma ação dedicada integrada ao Journey Optimizer *(específico do produto)*
* **Parâmetros de ação**: campos no painel de atividades de jornada que mapeiam dados de jornada para a carga de mensagem de Campanha esperada *(específico do produto)*

**Medidas de Proteção:**

* A conexão entre o Journey Optimizer e a instância do Campaign é configurada pela Adobe no momento do provisionamento; entre em contato com a Adobe para habilitá-la.
* Uma ação dedicada deve ser configurada antes que as ações do Campaign v7/v8 estejam disponíveis na paleta de jornadas.
* As ações do Campaign v7/v8 não podem ser usadas com atividades Ler público ou Qualificar público.
* O acesso a mensagens transacionais do Campaign e as permissões necessárias no Campaign são pré-requisitos.

**Terminologia:**

* Nome canônico: Adobe Campaign v7/v8 — Acrônimo: ACC — variantes: Campaign v7, Campaign v8, Campaign Classic
* Não confunda: &quot;Ações do Campaign v7/v8&quot; (podem ser usadas ao lado de ações nativas) ≠ &quot;Ações do Campaign Standard&quot; (não pode ser combinado com ações nativas na mesma jornada)

**Perguntas frequentes:**

* **P: Quem configura a conexão entre o Journey Optimizer e o Campaign v7/v8?** — a Adobe configura a conexão no momento do provisionamento; você deve entrar em contato com a Adobe para configurá-la.
* **P: As ações do Campaign v7/v8 podem ser combinadas com ações de canal nativas do Journey Optimizer na mesma jornada?** — Sim, ações do Campaign v7/v8 podem ser usadas junto a ações de canal nativo; esse não é o caso para ações do Campaign Standard.
* **P: As ações do Campaign v7/v8 podem ser usadas com atividades Ler Público ou Qualificar Público?** — Não, as ações do Campaign v7/v8 não podem ser usadas com as atividades Ler público ou Qualificar público.
* **P: Como mapear dados do jornada para a carga da mensagem do Campaign?** — No painel Parâmetros de ação, mapeie cada campo de carga esperado para o campo correspondente do evento de jornada ou fonte de dados, da mesma forma que as ações personalizadas.

+++
