---
title: excluir posicionamentos
description: Posicionamentos são contêineres usados para exibir suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 9%

---

# Excluir uma inserção {#delete-placement}

Ocasionalmente, pode ser necessário remover (DELETE) uma inserção. Isso é feito executando uma solicitação DELETE para o [!DNL Offer Library] API usando a id do posicionamento que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da instância do posicionamento que você deseja atualizar. | `offerPlacement1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a inserção e deve receber um status HTTP 404 (Não encontrado) porque a inserção foi removida.