---
title: Excluir uma coleção de itens
description: As coleções permitem categorizar e agrupar itens de decisão de acordo com suas preferências.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

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
