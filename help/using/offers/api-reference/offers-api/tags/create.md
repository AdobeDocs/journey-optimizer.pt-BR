---
title: Criar um qualificador de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 9b9ca28b185a342d908eeb53d772f9d011105aba
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 14%

---

# Criar um qualificador de coleção {#create-tag}

Você pode criar um qualificador de coleção (anteriormente conhecido como &quot;tag&quot;) fazendo uma solicitação POST para o [!DNL Offer Library] API.

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/tags
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre o qualificador de coleta recém-criado, incluindo suas `id`. Você pode usá-lo em etapas posteriores para atualizar ou deletar o qualificador de coleta. Você pode usar seu qualificador de coleta exclusivo `id` em tutoriais posteriores, para criar coleções e ofertas personalizadas.

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
