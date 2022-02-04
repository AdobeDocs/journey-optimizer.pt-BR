---
title: Excluir uma oferta substituta
description: Uma oferta de fallback é enviada para os clientes se eles não estiverem qualificados para outras ofertas
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 9%

---

# Excluir uma oferta substituta {#delete-fallback-offer}

Ocasionalmente, pode ser necessário remover (DELETE) uma oferta de fallback. Somente as ofertas de fallback que você criar no contêiner do locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para [!DNL Offer Library] API usando o $id da oferta de fallback que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as ofertas de fallback estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | O ID da instância da oferta de fallback. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

É possível confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a oferta de fallback. Você precisará incluir um cabeçalho Accept na solicitação, mas deve receber um status HTTP 404 (Not Found) porque a oferta de fallback foi removida do contêiner.
