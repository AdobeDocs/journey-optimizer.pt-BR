---
title: Excluir uma estratégia de seleção
description: As estratégias de seleção consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---

# Excluir uma estratégia de seleção {#delete-selection-strategy}

Ocasionalmente, pode ser necessário remover (DELETE) uma estratégia de seleção. Isso é feito executando uma solicitação do DELETE para a API da Biblioteca de ofertas usando a ID da estratégia de seleção que você deseja excluir.

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
