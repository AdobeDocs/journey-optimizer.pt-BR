---
title: Excluir uma estratégia de seleção
description: As estratégias de seleção consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/KnyhVoNWfjSIIMw2q7OZkBG--wgaBU4JXn7A9i41Vf8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 121
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
