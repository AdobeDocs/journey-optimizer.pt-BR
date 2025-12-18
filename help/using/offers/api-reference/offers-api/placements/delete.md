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
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 22%

---

# Excluir uma inserção {#delete-placement}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover (DELETE) um posicionamento. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando a ID do posicionamento que você deseja excluir.

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

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para o posicionamento e deve receber um status HTTP 404 (Não encontrado) porque o posicionamento foi removido.
