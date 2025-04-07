---
solution: Journey Optimizer
product: journey optimizer
title: Solicitações de privacidade
description: Saiba mais sobre solicitações de privacidade e o Privacy Service.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 98%

---

# Solicitações de privacidade {#track-changes}

O **Privacy Service** da Adobe Experience Platform fornece uma API RESTful e uma interface para ajudar você a gerenciar solicitações de dados do cliente. Com o Privacy Service, você pode enviar solicitações para acessar e excluir dados pessoais dos clientes por meio dos aplicativos da Adobe Experience Cloud, facilitando a conformidade automatizada com as regulamentações legais e organizacionais de privacidade.

As solicitações de privacidade podem ser criadas e gerenciadas no menu **[!UICONTROL Solicitações]**.

![](assets/requests.png)

Para obter mais informações sobre o Privacy Service e como criar e gerenciar solicitações de privacidade, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target="_blank"}.

<!--* [Privacy Service overview](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)
* [Managing privacy jobs in the Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)-->

## Gerencie solicitações individuais de privacidade de dados que você pode enviar ao Adobe Journey Optimizer {#data-privacy-requests}

Você pode enviar solicitações individuais para acessar e excluir dados do consumidor do Adobe Journey Optimizer de duas maneiras:

* Por meio da **Interface do Privacy Service**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"}
* Por meio da **API do Privacy Service**. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"}
  <!--More specific information on Privacy Service API [here](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank).-->

O Privacy Service oferece suporte a dois tipos de solicitações: **acesso a dados** e **exclusão de dados**.

Para **solicitações de acesso**, especifique “**Adobe Journey Optimizer**” na interface (ou “**CJM**” como um código de produto na API).

Para **solicitações de exclusão**, além da solicitação “**Adobe Journey Optimizer**”, também é necessário enviar solicitações de exclusão para **três serviços upstream** para impedir que o Journey Optimizer reinjete os dados excluídos. Se esses serviços upstream não forem especificados, a solicitação do “Adobe Journey Optimizer” permanecerá no estado “processando” até que as solicitações de exclusão dos serviços upstream sejam criadas.

Os três serviços upstream são:

* Perfil (código do produto: “profileService”)
* Data Lake da AEP (código do produto: “AdobeCloudPlatform”)
* Identidade (código do produto: “identity”)

>[!NOTE]
>
>Este guia aborda apenas como criar solicitações de privacidade para o [!UICONTROL Adobe Journey Optimizer].
>
>* Se você também planeja criar solicitações de privacidade para o data lake da Platform, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/catalog/privacy) além deste tutorial.
>
>* Para informações sobre o perfil do cliente em tempo real, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/privacy).
>* Para informações sobre o serviço de identidade, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/privacy).
>
>Para solicitações de exclusão e acesso, é necessário chamar esses sistemas individuais para garantir que as solicitações sejam tratadas por cada um deles. Criar uma solicitação de privacidade para o [!DNL Adobe Journey Optimizer] não removerá dados de todos esses sistemas.

## Criar solicitações de acesso e exclusão

### Pré-requisitos

Para fazer solicitações de acesso e exclusão de dados para o Adobe Journey Optimizer, você deve ter:

* uma ID de organização da Adobe
* um Identificador de identidade da pessoa com quem você deseja atuar e os namespaces correspondentes. Para obter mais informações sobre namespaces de identidade no Adobe Journey Optimizer e na Experience Platform, consulte a [visão geral do namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces).

>[!IMPORTANT]
>
>Ao enviar solicitações de privacidade, certifique-se de especificar “[!DNL '**Adobe Journey Optimizer**]” como o nome do produto direcionado e **todos os namespaces de identidade** (como “Email”, “ECID” ou “ID de fidelidade”) associados aos dados de perfil que precisam ser acessados ou removidos. Faça isso especialmente em solicitações de exclusão, pois se você não incluir explicitamente o nome do produto e todos os namespaces aplicáveis nesse caso, os dados não serão removidos do [!DNL Adobe Journey Optimizer].

### Valores de campo obrigatórios no Journey Optimizer para solicitações de API

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your Adobe Organization ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### Exemplo de solicitação de acesso ao RGPD:

Na interface:

![](assets/accessrequest.png){width="60%" align="center"}

Por meio da API:

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### Exemplo de solicitação de exclusão do RGPD:

Na interface:

![](assets/deleterequest.png){width="60%" align="center"}

Por meio da API:

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
