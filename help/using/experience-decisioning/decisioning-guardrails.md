---
title: Medidas de proteção e limitações do serviço de decisão
description: Saiba mais sobre as medidas de proteção e limitações da Decisão.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 15%

---

# Medidas de proteção e limitações do serviço de decisão {#decisioning-guardrails}

Para garantir o uso ideal do Decisioning, lembre-se das seguintes medidas de proteção e limitações.

A lista completa de [!DNL Journey Optimizer] medidas de proteção e limitações está disponível em [esta seção](../start/guardrails.md).

## Solicitações de decisão

| Grade de Proteção | Limite |
| ------- | ------- |
| Solicitação de API de experiência baseada em código com política de decisão utilizando a segmentação do Edge | 1500 |
| Solicitação de API de experiência baseada em código com política de decisão que não usa segmentação do Edge | 5000 |

## Coleções de itens

| Grade de Proteção | Limite |
| ------- | ------- |
| Coleções de itens | 10 K |
| Total de itens de oferta por coleção de itens | 500 |

## Política de decisão

| Grade de Proteção | Limite |
| ------- | ------- |
| Número de estratégias de seleção e itens manuais por política de decisão | 10 |
| Número máximo de itens de oferta retornados por política de decisão | 30 |

## Regras de elegibilidade

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de regras de decisão e fórmulas de classificação | 10K combinados |
| Número máximo de atributos de perfil por regra | 25 |
| Número máximo de atributos de dados de contexto por regra | 30 |
| Tamanho máximo da regra pql | 15K (UTF-8) |
| Número máximo de níveis de aninhamento | 30 |

## Fórmulas de classificação

| Grade de Proteção | Limite |
| ------- | ------- |
| Tamanho máximo do PQL de fórmula de classificação | 8K (UTF-8) |
| Número máximo de atributos de perfil | 25 |
| Número máximo de atributos de dados de contexto | 30 |
| Número máximo de níveis de aninhamento | 30 |

## Outros

| Grade de Proteção | Limite |
| ------- | ------- |
| Número de atributos personalizados por esquema de catálogo de Ofertas | 100 |
| Total de itens de oferta | 10 K |
| Total de posicionamentos | 1K |
| Modelo de classificação de IA | 5 |
| Regras de frequência - Número máximo de regras de limitação por oferta | 10 |
