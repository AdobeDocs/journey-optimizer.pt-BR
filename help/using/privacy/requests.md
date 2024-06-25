---
solution: Journey Optimizer
product: journey optimizer
title: Solicitações de privacidade
description: Saiba mais sobre solicitações de privacidade e o Privacy Service.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: ht
source-wordcount: '457'
ht-degree: 100%

---

# Solicitações de privacidade {#track-changes}

O **Privacy Service** da Adobe Experience Platform fornece uma API RESTful e uma interface para ajudar você a gerenciar solicitações de dados do cliente. Com o Privacy Service, você pode enviar solicitações para acessar e excluir dados pessoais dos clientes por meio dos aplicativos da Adobe Experience Cloud, facilitando a conformidade automatizada com as regulamentações legais e organizacionais de privacidade.

As solicitações de privacidade podem ser criadas e gerenciadas no menu **[!UICONTROL Solicitações]**.

![](assets/requests.png)

Para obter mais informações sobre o Privacy Service e como criar e gerenciar solicitações de privacidade, consulte a documentação da Adobe Experience Platform:

* [Visão geral do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR)
* [Gerenciamento de processos de privacidade na interface do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR)



## Gerenciamento de solicitações individuais de privacidade de dados que você pode enviar para o Adobe Journey Optimizer {#data-privacy-requests}

Você pode enviar solicitações individuais para acessar e excluir dados do consumidor do Adobe Journey Optimizer de duas maneiras:

* Por meio da **Interface do Privacy Service**. Consulte a documentação [aqui](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/ui/user-guide#_blank).
* Por meio da **API do Privacy Service**. Consulte a documentação [aqui](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) e informações da API [aqui](https://developer.adobe.com/experience-platform-apis/#_blank).

O Privacy Service aceita dois tipos de solicitações: **acesso a dados** e **exclusão de dados**.

>[!NOTE]
>
>Este guia aborda apenas como fazer solicitações de privacidade no Adobe Journey Optimizer. Se você também planeja fazer solicitações de privacidade para o data lake da Platform, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/catalog/privacy) além desse tutorial. Para Perfil do cliente em tempo real, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/privacy), e para o Serviço de identidade, consulte este [guia](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/privacy). Para solicitações de exclusão e acesso, é necessário chamar esses sistemas individuais para garantir que as solicitações sejam tratadas por cada um deles. Fazer uma solicitação de privacidade para o Adobe Journey Optimizer não removerá dados de todos esses sistemas.

Para **solicitações de acesso**, especifique “Adobe Journey Optimizer” na interface (ou “CJM” como um código de produto na API).

Para **solicitações de exclusão**, além da solicitação do “Adobe Journey Optimizer”, você também deve enviar solicitações de exclusão para três serviços upstream para impedir que o Journey Optimizer reinjete os dados excluídos. Se esses serviços upstream não forem especificados, a solicitação do “Adobe Journey Optimizer” permanecerá no estado “processando” até que as solicitações de exclusão dos serviços upstream sejam criadas.

Os três serviços upstream são:

* Perfil (código do produto: “profileService”)
* Data Lake da AEP (código do produto: “AdobeCloudPlatform”)
* Identidade (código do produto: “identity”)

## Como criar solicitações de acesso e exclusão

### Pré-requisitos

Para fazer solicitações de acesso e exclusão de dados para o Adobe Journey Optimizer, você deve ter:

* uma ID de organização IMS
* um Identificador de identidade da pessoa com quem você deseja atuar e os namespaces correspondentes. Para obter mais informações sobre namespaces de identidade no Adobe Journey Optimizer e na Experience Platform, consulte a [visão geral do namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces).

### Valores de campo obrigatórios no Adobe Journey Optimizer para solicitações de API

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

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


### Exemplo de solicitação de acesso ao GDPR:

Na interface:

![](assets/accessrequest.png)

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

### Exemplo de solicitação de exclusão do GDPR:

Na interface:

![](assets/deleterequest.png)

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
