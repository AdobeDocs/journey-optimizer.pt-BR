---
title: Excluir um item de decisão
description: Itens de decisão são ofertas de marketing que podem ser criadas e organizadas em coleções e catálogos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 6%

---

# Excluir um item de decisão {#delete-decision-item}

Para remover um item de decisão, execute uma solicitação DELETE para a API da Biblioteca de ofertas com a ID do item de decisão que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `offerItem1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o item de decisão. Você deve receber um status HTTP 404 (Não encontrado) porque o item de decisão foi removido.
