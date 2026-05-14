---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Excluir uma oferta substituta
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/3SJmNX6JrEY07R4pePNPzdokJrK7Ye6e9gV5i1LlDJA
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
source-wordcount: 138
ht-degree: 24%

---

# Excluir uma oferta substituta {#delete-fallback-offer}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover uma oferta substituta do (DELETE). Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a ID da oferta substituta que você deseja excluir.

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
