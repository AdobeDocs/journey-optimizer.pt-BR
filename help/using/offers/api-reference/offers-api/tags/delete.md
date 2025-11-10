---
title: Excluir qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---


# Excluir um qualificador de coleção {#delete-tag}

Ocasionalmente, pode ser necessário remover (DELETE) um qualificador de coleção (anteriormente conhecido como &quot;tag&quot;). Isso é feito executando uma solicitação DELETE para a API da Biblioteca de ofertas usando a ID do qualificador de coleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja excluir. | `tag1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o qualificador de coleção. Você deve receber um status HTTP 404 (Não encontrado) porque o qualificador da coleção foi removido.