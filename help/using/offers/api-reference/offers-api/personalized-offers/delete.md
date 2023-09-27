---
title: Excluir ofertas personalizadas
description: Uma oferta personalizada é uma mensagem de marketing personalizável baseada em regras de elegibilidade e restrições.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 9%

---

# Excluir uma oferta personalizada {#delete-personalized-offer}

Ocasionalmente, pode ser necessário remover (DELETE) uma oferta personalizada. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando a id da oferta personalizada que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja excluir. | `personalizedOffer1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a oferta personalizada e deve receber um status HTTP 404 (Não encontrado) porque a oferta personalizada foi removida.
