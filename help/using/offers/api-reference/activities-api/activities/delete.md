---
title: Excluir decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 9%

---

# Excluir uma decisão {#delete-decision}

Ocasionalmente, pode ser necessário remover (DELETE) uma decisão. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando o `id` da decisão que deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja excluir. | `offerDecision1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a decisão. Você deve receber um status HTTP 404 (Não encontrado) porque a decisão foi removida.
