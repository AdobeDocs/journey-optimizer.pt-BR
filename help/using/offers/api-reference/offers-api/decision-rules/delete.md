---
title: Excluir regras de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a elegibilidade.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 9%

---

# Excluir uma regra de decisão {#delete-decision-rule}

Ocasionalmente, pode ser necessário remover (DELETE) uma regra de decisão. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando o `id` da regra de decisão que deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `offerRule1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a regra de decisão e deve receber um status HTTP 404 (Não encontrado) porque a regra de decisão foi removida.
