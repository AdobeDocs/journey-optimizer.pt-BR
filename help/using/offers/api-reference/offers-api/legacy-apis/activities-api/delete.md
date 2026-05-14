---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Excluir decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 36a87d98-fd61-416e-83a1-e267a7b4d455
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-NdP9Eia9rQR-PKVEESckF-pk8XA8-Zyy-2trkJLHhc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 19%

---

# Excluir uma decisão {#delete-decision}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover (DELETE) uma decisão. Somente decisões criadas no contêiner de locatário podem ser excluídas. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a $id da oferta substituta que você deseja excluir.

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
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 202 (Sem conteúdo) e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a decisão. Você precisará incluir um cabeçalho Aceitar na solicitação, mas deverá receber um status HTTP 404 (Não encontrado) porque a decisão foi removida do container.
