---
title: Excluir qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 7%

---

# Excluir um qualificador de coleção {#delete-tag}

Ocasionalmente, pode ser necessário remover (DELETE) um qualificador de coleção (anteriormente conhecido como &quot;tag&quot;). Somente os qualificadores de coleção criados no contêiner do locatário podem ser excluídos. Isso é feito executando uma solicitação DELETE para [!DNL Offer Library] API usando o $id do qualificador de coleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde os qualificadores de coleção estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | A ID da instância do qualificador de coleção que você deseja atualizar. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o qualificador da coleção. Você precisará incluir um cabeçalho Accept na solicitação, mas deve receber um status HTTP 404 (Not Found), pois o qualificador de coleção foi removido do contêiner.
