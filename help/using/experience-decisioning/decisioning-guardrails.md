---
title: Medidas de proteção e limitações do serviço de decisão
description: Saiba mais sobre as medidas de proteção e limitações da Decisão.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
source-git-commit: 5be6ecd85b0b45e01f7a27e0ffc55a2c6a22bcea
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 15%

---

# Medidas de proteção e limitações do serviço de decisão {#decisioning-guardrails}

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

## Configurações  {#configurations}

O número total de configurações que o Decisioning suporta não pode exceder 20.000.

A contagem total de configurações é o número total de [regras de limitação](items.md#capping) existentes em sua sandbox.
