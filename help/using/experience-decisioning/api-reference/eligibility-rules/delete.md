---
title: Excluir uma regra de elegibilidade
description: As Regras de elegibilidade permitem definir os candidatos elegíveis com base no que você deseja direcionar, como atributos de perfil e públicos-alvo.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
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
