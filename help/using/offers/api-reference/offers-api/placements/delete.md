---
title: excluir disposições
description: As disposições são contêineres usados para mostrar suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---

# Excluir uma inserção {#delete-placement}

Ocasionalmente, pode ser necessário remover (DELETE) uma disposição. Somente as disposições criadas no contêiner do locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para [!DNL Offer Library] API usando a ID da instância da disposição que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as disposições estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | A ID da instância da disposição que você deseja atualizar. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

É possível confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a disposição. Você precisará incluir um cabeçalho Accept na solicitação, mas deve receber um status HTTP 404 (Not Found) porque a disposição foi removida do contêiner.
