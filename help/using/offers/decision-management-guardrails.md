---
title: Medidas de proteção e limitações da gestão de decisões
description: Saiba mais sobre as medidas de proteção e limitações do gerenciamento de decisão.
feature: Decisioning
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 15%

---

# Medidas de proteção e limitações da gestão de decisões {#decision-management-guardrails}

Para garantir o uso ideal da Gestão de decisões, lembre-se das seguintes medidas de proteção e limitações.

A lista completa de [!DNL Journey Optimizer] medidas de proteção e limitações está disponível em [esta seção](../start/guardrails.md).

## Solicitações de decisão

A taxa de transferência de delivery corresponde ao número de respostas de decisão que podem ser entregues pelo serviço de aplicativos Gerenciamento de decisões em um período especificado.

| Grade de Proteção | Limite |
| ------- | ------- |
| Solicitações de API de decisão por segundo | 500 |
| Solicitações de API do Edge Decisioning por segundo com a Segmentação do Edge | 1.500 |
| Solicitações de API do Edge Decisioning por segundo sem segmentação do Edge | 5.000 |
| Ofertas retornadas por resposta | Até 30 por escopo de decisão ou 100 no total |
| Número máximo de regras de oferta envolvidas por solicitação | 100 |

## Decisões

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de decisões | 10 K |
| Decisões em tempo real | 1K |
| Posicionamentos por decisão | 30 |

## Coleções

| Grade de Proteção | Limite |
| ------- | ------- |
| Ofertas por coleção | 500 |
| Coleções | 10 K |
| Coleções por decisão | 30 |

## Qualificadores de coleção

| Grade de Proteção | Limite |
| ------- | ------- |
| Qualificador de coleção por oferta ou coleção | 20 |
| Qualificadores da coleção total | 1.000 |

## Ofertas

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de ofertas | 10 K |
| Número máximo de **ofertas** ativas por sandbox | 10 K |
| Tamanho máximo de ofertas, incluindo atributos (1 KB), máximo de 30 atributos | 1 KB |
| Tamanho máximo de representação da oferta (total para todos os posicionamentos) | 1 KB |

## Regras de elegibilidade

| Grade de Proteção | Limite |
| ------- | ------- |
| Total de regras de decisão e fórmulas de classificação | 10K combinados |
| Número máximo de atributos de perfil por regra | 25 |
| Número máximo de atributos de dados de contexto por regra | 30 |
| Tamanho máximo da regra do PQL | 15K (UTF-8) |
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
| Posicionamentos | 1000 |
| Modelo de classificação de IA | 5 |
| Limite de frequência - Número máximo de regras de limite por oferta | 10 |
