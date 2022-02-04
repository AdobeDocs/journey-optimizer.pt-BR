---
title: Criar simulações
description: Saiba como criar simulações
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

---

# Criar simulações {#create-simulations}

## Sobre a simulação

Para validar sua lógica de decisão, você pode simular quais ofertas serão entregues a um perfil de teste para uma determinada disposição.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Isso permite testar e refinar várias versões das ofertas sem afetar os recipients alvos.

>[!NOTE]
>
>Esse recurso simula uma única solicitação para o [!DNL Decisions] API. Saiba mais sobre [Fornecer ofertas usando a API de decisões](../api-reference/decisions-api/deliver-offers.md).

Para acessar esse recurso, selecione o **[!UICONTROL Simulation]** na guia do **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Selecionar perfis de teste

Primeiro, é necessário selecionar os perfis de teste que serão usados para simulação.

1. Clique em **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Selecione o namespace de identidade que deseja usar para identificar os perfis de teste. Neste exemplo, usaremos a variável **Email** namespace.

   >[!NOTE]
   >
   >Um namespace de identidade define o contexto de um identificador, como um endereço de email ou ID de CRM. Saiba mais sobre os namespaces de identidade da Adobe Experience Platform [nesta seção](../../start/get-started-identity.md){target=&quot;_blank&quot;}.

1. Insira o valor de identidade e clique em **[!UICONTROL View]** para listar os perfis disponíveis.

   ![](../../assets/offers_simulation-add-profile.png)

1. Adicione outros perfis se desejar testar dados de perfil diferentes e salve sua seleção.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Depois de adicionados, todos os perfis são listados na lista suspensa em **[!UICONTROL Test profile]**. Você pode alternar entre os perfis de teste salvos para exibir os resultados de cada perfil selecionado.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Você pode clicar no botão **[!UICONTROL Profile details]** link para exibir os dados de perfil selecionados.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Adicionar escopos de decisão

Em seguida, selecione as decisões de oferta que deseja simular nos perfis de teste.

1. Selecione **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Selecione uma disposição na lista.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. As decisões disponíveis são exibidas.

   * Você pode usar o campo de pesquisa para refinar a seleção.
   * Você pode clicar no botão **[!UICONTROL Open offer decisions]** para abrir a lista de todas as decisões criadas. Saiba mais sobre [decisões](create-offer-activities.md).

   Selecione a decisão de sua escolha e clique em **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. O escopo de decisão que você acabou de definir é exibido no espaço de trabalho principal.

   É possível ajustar o número de ofertas que deseja solicitar. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para esse escopo de decisão.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Você pode solicitar até 30 ofertas.

1. Repita as etapas acima para adicionar quantas decisões forem necessárias.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Mesmo que você defina vários escopos de decisão, apenas uma solicitação de API é simulada.
   >
   >Por padrão, todos os sinalizadores de Desduplicação são ativados para simulação, o que significa que o mecanismo de decisão permite duplicatas e, portanto, pode fazer a mesma apresentação em várias decisões/disposições. Saiba mais sobre o [!DNL Decisions] Propriedades da solicitação de API em [esta seção](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Exibir resultados da simulação {#simulation-results}

Depois de adicionar um escopo de decisão e selecionar um perfil de teste, você poderá visualizar os resultados.

1. Clique em **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. As melhores ofertas disponíveis são exibidas de acordo com o perfil selecionado para cada decisão.

   Selecione uma oferta para exibir seus detalhes.

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. Selecione outro perfil na lista para exibir os resultados das decisões de oferta para um perfil de teste diferente.

1. Você pode adicionar, remover ou atualizar os escopos de decisão quantas vezes forem necessárias.

>[!NOTE]
>
>Sempre que alterar perfis ou atualizar escopos de decisão, será necessário atualizar os resultados usando o **[!UICONTROL View results]** botão.

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

