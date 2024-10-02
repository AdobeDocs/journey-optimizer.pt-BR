---
title: Excluir uma estratégia de seleção
description: As estratégias de seleção consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---

# Excluir uma estratégia de seleção {#delete-selection-strategy}

Ocasionalmente, pode ser necessário remover (DELETE) uma estratégia de seleção. Isso é feito executando uma solicitação DELETE para a API da Biblioteca de ofertas usando a id da estratégia de seleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `selectionStrategy1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a estratégia de seleção. Você deve receber um status HTTP 404 (Não encontrado) porque a estratégia de seleção foi removida.
