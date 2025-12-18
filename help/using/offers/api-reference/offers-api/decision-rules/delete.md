---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Excluir regras de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a elegibilidade.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 21%

---

# Excluir uma regra de decisão {#delete-decision-rule}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Ocasionalmente, pode ser necessário remover (DELETE) uma regra de decisão. Isso é feito executando uma solicitação DELETE para a API [!DNL Offer Library] usando o `id` da regra de decisão que você deseja excluir.

**Formato da API**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja excluir. | `offerRule1234` |

**Solicitação**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna o status HTTP 200 e um corpo em branco.

Você pode confirmar a exclusão tentando uma solicitação de pesquisa (GET) para a regra de decisão e deve receber um status HTTP 404 (Não encontrado) porque a regra de decisão foi removida.
