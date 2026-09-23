---
title: Medidas de proteção e limitações do serviço de decisão
description: Saiba mais sobre as medidas de proteção e limitações da Decisão.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/oTljriepwffzR-LIAc2kWjTQx9Oj0QMgJpbghkSEsmY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
    internal-label: Guardrails and limitations
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
    internal-label: Decisioning
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
    internal-label: Edge Decisioning
source-git-commit: 4f3312974e2533c97954e887b4371de6fc80595a
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 13%
---
# Medidas de proteção e limitações do serviço de decisão {#decisioning-guardrails}

>[!BEGINSHADEBOX]

**Nesta página:** Revise as medidas de proteção e os limites que se aplicam à Decisão em solicitações de decisão, itens, políticas, regras de qualificação e fórmulas de classificação, para que você possa projetar configurações de decisão que permaneçam dentro dos limites com suporte.

>[!ENDSHADEBOX]

Para garantir o uso ideal do Decisioning, lembre-se das seguintes medidas de proteção e limitações.

A lista completa de [!DNL Journey Optimizer] medidas de proteção e limitações está disponível em [esta seção](../start/guardrails.md).

## Solicitações de decisão {#decision-requests}

| Grade de Proteção | Limite |
| ------- | ------- |
| Solicitação de API de experiência baseada em código com política de decisão usando segmentação do Edge | 1500 |
| Solicitação de API de experiência baseada em código com política de decisão sem usar a segmentação do Edge | 5000 |
| Número máximo de URIs de superfície por solicitação de decisão do Edge | 30 |

## Itens de decisão {#decision-items}

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de itens de decisão | 10 K |
| Tamanho máximo de itens, incluindo atributos (1 KB), máximo de 30 atributos | 1KB |
| Regras de frequência - Número máximo de regras de limite por item de decisão | 10 |
| Número máximo de Fragmentos de conteúdo do AEM por item de decisão | 5 |

## Coleções de itens {#item-collections}

| Grade de Proteção | Limite |
| ------- | ------- |
| Coleções de itens | 10 K |
| Total de itens de decisão por coleção | 500 |

## Política de decisão {#decision-policy}

| Grade de Proteção | Limite |
| ------- | ------- |
| Número de estratégias de seleção e itens manuais por política de decisão | 10 |
| Número máximo de itens de decisão retornados por política de decisão | 30 |
| Máximo de políticas de decisão por email | 10 |

## Regras de elegibilidade {#eligibility-rules}

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de regras de decisão e fórmulas de classificação | 10K combinados |
| Número máximo de atributos de perfil por regra | 25 |
| Número máximo de atributos de dados de contexto por regra | 30 |
| Tamanho máximo da regra pql | 15K (UTF-8) |
| Número máximo de níveis de aninhamento | 30 |

## Fórmulas de classificação {#ranking-formulas}

| Grade de Proteção | Limite |
| ------- | ------- |
| Tamanho máximo do PQL de fórmula de classificação | 8K (UTF-8) |
| Número máximo de atributos de perfil | 25 |
| Número máximo de atributos de dados de contexto | 30 |
| Número máximo de níveis de aninhamento | 30 |

## Outros {#others}

| Grade de Proteção | Limite |
| ------- | ------- |
| Número de atributos personalizados por esquema de catálogo de itens | 100 |
| Total de posicionamentos | 1K |
| Modelo de classificação de IA | 5 |
| Tamanho da carga de resposta do canal da Web | 64 KiB |

## Configurações {#configurations}

O número total de configurações que o Decisioning suporta não pode exceder 20.000.

A contagem total de configurações é o número total de [regras de limitação](items.md#capping) existentes em sua sandbox.
