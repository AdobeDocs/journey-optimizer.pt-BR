---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: excluir posicionamentos
description: Posicionamentos são contêineres usados para exibir suas ofertas.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 944efb12-6745-4bb2-be52-293e23925350
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/gPJcSwy-Z-hondA5knYpiR9OUlHXmSahDHTufmNC7gw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 17%

---

# Excluir uma inserção {#delete-placement}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover (DELETE) um posicionamento. Somente as disposições criadas no contêiner de locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a ID de instância do posicionamento que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde os posicionamentos estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | A ID da instância do posicionamento que você deseja atualizar. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Solicitação**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o posicionamento. Você precisará incluir um cabeçalho Aceitar na solicitação, mas deverá receber um status HTTP 404 (Não encontrado) porque o posicionamento foi removido do container.
