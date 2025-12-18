---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Excluir uma coleção
description: Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.
feature: Decision Management, API, Collections
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 22%

---

# Excluir uma coleção {#delete-collection}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover (DELETE) uma coleção. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando o `id` da coleção que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `offerCollection1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' 
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a coleção. Você deve receber um status HTTP 404 (Não encontrado) porque a coleção foi removida.
