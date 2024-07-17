---
title: Excluir qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: cc67519e-7a80-49c7-8c8b-c777be633026
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---

# Excluir um qualificador de coleção {#delete-tag}

Ocasionalmente, pode ser necessário remover (DELETE) um qualificador de coleção (anteriormente conhecido como &quot;tag&quot;). Somente qualificadores de coleção criados no contêiner de locatário podem ser excluídos. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a $id do qualificador de coleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde os qualificadores de coleta estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | A ID da instância do qualificador de coleta que você deseja atualizar. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

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

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o qualificador de coleção. Você precisará incluir um cabeçalho Aceitar na solicitação, mas deverá receber um status HTTP 404 (Não encontrado) porque o qualificador de coleção foi removido do container.
