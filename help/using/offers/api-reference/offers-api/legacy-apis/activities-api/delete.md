---
title: Excluir decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: ef22b6183c7646cca8636f4a7e4dd87c8f88e8ce
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---


# Excluir uma decisão {#delete-decision}

Ocasionalmente, pode ser necessário remover (DELETE) uma decisão. Somente decisões criadas no contêiner de locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando a $id da oferta substituta que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | A ID da instância da decisão. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
	@@ -37,6 +35,6 @@ curl -X DELETE \

**Response**

A successful response returns HTTP status 202 (No Content) and a blank body.

You can confirm the deletion by attempting a lookup (GET) request to the decision. You will need to include an Accept header in the request, but should receive an HTTP status 404 (Not Found) because the decision has been removed from the container.

