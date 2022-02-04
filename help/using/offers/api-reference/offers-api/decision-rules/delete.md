---
title: Excluir regras de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a qualificação.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---

# Excluir uma regra de decisão {#delete-decision-rule}

Por vezes, pode ser necessário remover (DELETE) uma regra de decisão. Somente as regras de decisão criadas no contêiner do locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para [!DNL Offer Library] API usando a ID da instância da regra de decisão que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as regras de decisão estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | O ID da instância da regra de decisão que você deseja atualizar. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a regra de decisão. Você precisará incluir um cabeçalho Accept na solicitação, mas deve receber um status HTTP 404 (Not Found) porque a regra de decisão foi removida do contêiner.
