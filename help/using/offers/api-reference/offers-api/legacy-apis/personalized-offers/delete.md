---
title: Excluir ofertas personalizadas
description: Uma oferta personalizada é uma mensagem de marketing personalizável baseada em regras de elegibilidade e restrições.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 6ae37843-2679-48a3-96ef-bb93a5d4a333
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---

# Excluir uma oferta personalizada {#delete-personalized-offer}

Ocasionalmente, pode ser necessário remover (DELETE) uma oferta personalizada. Somente ofertas personalizadas que você criar no contêiner de locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a $id da oferta personalizada que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde as ofertas personalizadas estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a oferta personalizada. Você precisará incluir um cabeçalho Aceitar na solicitação, mas deverá receber um status HTTP 404 (Não encontrado) porque a oferta personalizada foi removida do container.
