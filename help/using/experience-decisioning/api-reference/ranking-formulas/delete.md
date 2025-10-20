---
title: Excluir uma fórmula de classificação
description: As fórmulas de classificação permitem definir as funções de pontuação, que são usadas para classificar itens.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ea50481-b1b9-4e0c-ad4e-c4139891bfdf
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# Excluir uma fórmula de classificação {#delete-selection-strategy}

Ocasionalmente, pode ser necessário remover (DELETE) uma fórmula de classificação. Isso é feito executando uma solicitação DELETE para a API da Biblioteca de ofertas usando a ID da fórmula de classificação que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `rankingFormula1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a fórmula de classificação. Você deve receber um status HTTP 404 (Não encontrado) porque a fórmula de classificação foi removida.
