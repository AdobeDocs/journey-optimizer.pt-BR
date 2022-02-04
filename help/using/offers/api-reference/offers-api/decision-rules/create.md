---
title: Criar regras de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a qualificação.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 12%

---

# Criar uma regra de decisão {#create-decision-rule}

As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a qualificação.

## Aceitar e digitar cabeçalhos de tipo de conteúdo {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* e *Aceitar* campos no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as regras de decisão estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sales rule",
        "description": "Decisioning rule for sales",
        "condition": {
            "type": "PQL",
            "format": "pql/text",
            "value": "profile.person.name.firstName.equals(\"Joe\", false)"
        },
        "xdm:definedOn": {
            "profile": {
                "xdm:schema": {
                    "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                    "version": "1"
                },
                "xdm:referencePaths": [
                    "person.name.firstName"
                ]
            }
        }
    }'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a regra de decisão recém-criada, incluindo a ID e a disposição da instância exclusiva `@id`. Você pode usar a ID da instância em etapas posteriores para atualizar ou excluir sua regra de decisão. Você pode usar sua regra de decisão exclusiva `@id` em um tutorial posterior para criar ofertas personalizadas.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
