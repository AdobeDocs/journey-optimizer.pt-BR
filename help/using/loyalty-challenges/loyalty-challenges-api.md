---
solution: Journey Optimizer
product: journey optimizer
title: APIs de desafios de fidelidade
description: Saiba como usar as REST APIs do Loyalty Challenges para gerenciar de forma programática os desafios e consultar o estado de participação do perfil no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# APIs de desafios de fidelidade {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar as APIs REST de Desafios de Fidelidade para criar e gerenciar desafios de forma programática e consultar e atualizar o estado de participação de desafio para perfis individuais.

>[!ENDSHADEBOX]

## Acesso rápido {#quick-access}

Duas REST APIs estão disponíveis para desafios de fidelidade:

* **[API de metadados de desafio de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}** — Crie, recupere, atualize, publique, arquive e duplique desafios de forma programática.
* **[API de estado de desafio de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}** — consulte e atualize o estado de participação de desafio para perfis individuais.

## API de metadados do desafio de fidelidade {#metadata-api}

A API de metadados do desafio de fidelidade permite gerenciar todo o ciclo de vida dos desafios fora da interface do usuário do Journey Optimizer. Use-o para automatizar operações de desafio ou integrar o gerenciamento do programa de fidelidade a suas próprias ferramentas e fluxos de trabalho. Você pode, por exemplo, criar, publicar e arquivar desafios, recuperar todos os desafios com filtragem e classificação ou duplicar um desafio existente, incluindo metadados e campanhas de jornada.

➡️ [Referência da API de metadados do desafio de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## API de estado de desafio de fidelidade {#state-api}

A API de estado de desafio de fidelidade permite interagir com registros de participação de desafio no nível do perfil. Use-a para consultar o status de participação atual, o andamento e a conclusão de uma tarefa de um perfil — por exemplo, recuperar todos os registros de participação de um perfil, verificar o estado de uma tarefa específica em um desafio ou retirar um perfil de um ou mais desafios.

➡️ [Referência da API do estado do desafio de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## Autenticação {#authentication}

Todas as chamadas de API de desafios de fidelidade exigem os seguintes cabeçalhos:

| Header | Descrição |
|---|---|
| `Authorization` | Token de portador do token de acesso IMS |
| `x-gw-ims-org-id` | Sua ID da organização IMS |
| `x-api-key` | Sua ID de cliente (chave de API) |
| `x-sandbox-name` | O nome da sandbox para direcionamento |

Siga o [tutorial de autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para recuperar essas credenciais.
