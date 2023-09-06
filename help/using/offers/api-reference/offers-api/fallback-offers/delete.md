---
title: Excluir uma oferta substituta
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 12%

---

# Excluir uma oferta substituta {#delete-fallback-offer}

Ocasionalmente, pode ser necessário remover (DELETE) uma oferta substituta. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando a id da oferta substituta que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja excluir. | `fallbackOffer1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a oferta e deve receber um status HTTP 404 (Não encontrado) porque a oferta de fallback foi removida.
