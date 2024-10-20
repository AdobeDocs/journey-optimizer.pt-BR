---
title: Excluir uma coleção de itens
description: Saiba como categorizar suas decisões de grupo em coleções.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# Excluir uma coleção de itens {#delete-decision-item}

Ocasionalmente, pode ser necessário remover (DELETE) uma coleção de itens. Isso é feito executando uma solicitação DELETE para a API da Biblioteca de ofertas usando a ID da coleção de itens que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `itemCollections1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a coleção de itens. Você deve receber um status HTTP 404 (Não encontrado) porque a coleção de itens foi removida.
