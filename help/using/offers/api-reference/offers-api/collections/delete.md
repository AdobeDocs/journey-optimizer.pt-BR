---
title: Excluir uma coleção
description: Coleções são subconjuntos de ofertas com base em condições predefinidas definidas por um profissional de marketing, como a categoria da oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# Excluir uma coleção {#delete-collection}

Ocasionalmente, pode ser necessário remover (DELETE) uma coleção. Somente as coleções criadas no contêiner do locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para [!DNL Offer Library] API usando o $id da coleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as coleções estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | O ID da instância da coleção que você deseja atualizar. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a coleção. Você precisará incluir um cabeçalho Accept na solicitação, mas deve receber um status HTTP 404 (Not Found) porque a coleção foi removida do contêiner.
