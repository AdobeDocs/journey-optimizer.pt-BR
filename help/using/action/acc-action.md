---
solution: Journey Optimizer
product: journey optimizer
title: Integrar ao Adobe Campaign v7/v8
description: Saiba como integrar o Journey Optimizer ao Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campaign, acc, integração
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
TQID: https://experienceleague.adobe.com/Ho00nWReUS7S4PnmCzle6RbPzwt0DlZN43IQoF2918k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 9%

---

# Integrar ao Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!BEGINSHADEBOX]

**Nesta página:** conecte o Journey Optimizer ao Adobe Campaign v7 ou v8 para que seu jornada possa enviar emails, notificações por push e SMS por meio de mensagens transacionais do Campaign.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Ações do Adobe Campaign v7/v8"
>abstract="Essa integração está disponível para o Adobe Campaign v7 e v8. Ela permite enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign. A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento."

Se você tiver o Adobe Campaign Classic v7 ou o Campaign v8, uma ação personalizada específica estará disponível em suas jornadas para integrar o Adobe Journey Optimizer e o Adobe Campaign. Essa integração permite enviar emails, notificações por push e SMS usando recursos de mensagens transacionais do Adobe Campaign. Saiba mais neste [caso de uso completo](../building-journeys/ajo-ac.md).

Para cada ação configurada, uma [Atividade de ação de campanha](../building-journeys/using-adobe-campaign-v7-v8.md) está disponível na paleta do designer de jornada.

## Activation {#access}

Quando solicitado, a conexão entre os ambientes Journey Optimizer e Adobe Campaign é configurada pela Adobe no momento do provisionamento. Se você não solicitou a conexão no momento do provisionamento, entre em contato com o suporte da Adobe Journey Optimizer para solicitar a ativação. Você deve fornecer os seguintes detalhes:

>[!BEGINTABS]

>[!TAB Para Adobe Journey Optimizer]

* ID da organização (Adobe OrgID)
* Nome da sandbox

>[!TAB Para Adobe Campaign]

* URL do servidor do Campaign
* URL do servidor em tempo real
* Sua versão do Adobe Campaign

>[!ENDTABS]


## Medidas de proteção e limitações {#important-notes}

* Não há limitação de mensagens. O sistema limita o número de mensagens que podem ser enviadas a 4.000 a cada 5 minutos, com base no SLA do Campaign atual. Por esse motivo, o Journey Optimizer só deve ser usado em casos de uso unitários (eventos individuais, não públicos).

* Você deve configurar uma ação na tela por modelo a ser usado. É necessário configurar uma ação no Journey Optimizer para cada modelo que você deseja usar do Adobe Campaign.

* Recomendamos usar uma instância dedicada do Managed Services ou do Centro de mensagens hospedada para essa integração, a fim de evitar o impacto em outras operações do Campaign que você possa ter. O servidor de marketing pode ser hospedado ou no local.<!--The build required is 21.1 Release Candidate or greater. -->

* Não há validação para indicar que a carga ou mensagem da campanha está correta.

* Não é possível usar uma ação do Campaign com um evento de qualificação de público-alvo.

## Pré-requisitos {#prerequisites}

No Adobe Campaign, você deve criar e publicar uma mensagem transacional e seu evento associado. Consulte a [documentação do Adobe Campaign](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Você pode criar sua carga JSON correspondente a cada mensagem seguindo o padrão abaixo. Em seguida, você colará essa carga ao configurar a ação no Journey Optimizer (veja abaixo).

+++ Exemplo

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **canal**: o canal definido para o modelo transacional do Campaign
* **eventType**: o nome interno do evento do Campaign
* **ctx**: variável baseada na personalização que você tem em sua mensagem

+++

## Configurar a ação {#configure-action}

No Journey Optimizer, você deve configurar uma ação por mensagem transacional.

Para criar uma ação do Campaign, siga estas etapas:

1. Criar uma nova ação. [Saiba como criar ações personalizadas](../action/action.md).
1. Insira um nome e uma descrição.
1. No campo **[!UICONTROL Tipo de ação]**, selecione **[!UICONTROL Adobe Campaign Classic]**.
   ![](assets/accintegration1.png)
1. Clique no campo **[!UICONTROL Carga]** e cole um exemplo da carga JSON correspondente à mensagem do Campaign. Entre em contato com a Adobe para obter essa carga.
1. Defina cada campo como estático ou variável com base em se você deseja que ele seja mapeado na tela de Jornada. Por exemplo, campos como parâmetros de canal de email e campos de personalização (`ctx`) normalmente devem ser definidos como variáveis para que possam se adaptar dinamicamente na jornada.
1. Clique em **[!UICONTROL Salvar]**.

## Atualizar uma ação existente {#update-action}

Se precisar atualizar uma ação personalizada existente do Campaign v7/v8, por exemplo, quando o endpoint em tempo real (RT) for alterado após a configuração inicial, siga estas etapas:

1. No menu **[!UICONTROL Administração]**, selecione **[!UICONTROL Configurações]** e vá para **[!UICONTROL Ações]**.
1. Localize e selecione a ação de campanha que deseja atualizar na lista de ações.
1. Clique em **[!UICONTROL Editar]** para abrir a configuração da ação.
1. Atualize o campo **[!UICONTROL URL]** com a nova URL de ponto de extremidade RT. Verifique se o formato do endpoint está correto e acessível.
1. Se necessário, atualize a configuração **[!UICONTROL Carga]** para corresponder a quaisquer alterações na estrutura da mensagem transacional do Campaign.
1. Clique em **[!UICONTROL Testar]** para validar a conexão com o novo ponto de extremidade. Verifique se o teste retorna uma resposta bem-sucedida antes de continuar.
1. Depois de validado, clique em **[!UICONTROL Salvar]** para aplicar as alterações.

>[!NOTE]
>
>Qualquer jornada que use essa ação usará automaticamente a configuração atualizada. Se você tiver jornadas ativas usando essa ação, monitore-as cuidadosamente após atualizar o endpoint para garantir a entrega adequada da mensagem.

