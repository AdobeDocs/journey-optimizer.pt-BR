---
title: Excluir uma regra de elegibilidade
description: As Regras de elegibilidade permitem definir os candidatos elegíveis com base no que você deseja direcionar, como atributos de perfil e públicos-alvo.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---

# Excluir uma regra de elegibilidade {#delete-eligibility-rule}

Ocasionalmente, pode ser necessário remover (DELETE) uma regra de elegibilidade. Isso é feito executando uma solicitação do DELETE para a API da Biblioteca de ofertas usando a ID da regra de elegibilidade que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `rule1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a regra. Você deve receber um status HTTP 404 (Não encontrado) porque a regra foi removida.
