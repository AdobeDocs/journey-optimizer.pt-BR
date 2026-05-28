---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Medidas de proteção e limitações da gestão de decisões
description: Saiba mais sobre as medidas de proteção e limitações do gerenciamento de decisão.
badge: label="Legado" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/teZQ3GKXJoj05ZD7bCCzKSzwLdUbgF8DXp8csDostOw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 11%

---

# Medidas de proteção e limitações da gestão de decisões {#decision-management-guardrails}

>[!IMPORTANT]
>
>Esta página aborda as medidas de proteção para o recurso **Gerenciamento de decisão** herdado. Se você estiver usando a **Decisão** — o recurso de decisão atual do [!DNL Adobe Journey Optimizer] disponível através de experiência baseada em código e canais de email — consulte as [Medidas de proteção e limitações da decisão](../experience-decisioning/decisioning-guardrails.md).
>
>Não tem certeza de qual recurso você está usando? [Saiba mais sobre a Decisão](../experience-decisioning/gs-experience-decisioning.md).

Esta página se aplica aos usuários que ainda trabalham com o sistema herdado de Gestão de decisões. Para garantir o uso ideal, lembre-se das seguintes medidas de proteção e limitações.

A lista completa de [!DNL Journey Optimizer] medidas de proteção e limitações está disponível em [esta seção](../start/guardrails.md).

## Solicitações de decisão

A taxa de transferência de delivery corresponde ao número de respostas de decisão que podem ser entregues pelo serviço de aplicativos Gerenciamento de decisões em um período especificado.

| Grade de Proteção | Limite |
| ------- | ------- |
| Solicitações de API de decisão por segundo | 500 por organização |
| Solicitações de API do Edge Decisioning por segundo com a Segmentação do Edge | 1.500 por organização |
| Solicitações de API do Edge Decisioning por segundo sem segmentação do Edge | 5.000 por organização |
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
| Tamanho máximo de ofertas, incluindo atributos (1 KB), máximo de 30 atributos | 1KB |
| Tamanho máximo de representação da oferta (total para todos os posicionamentos) | 1KB |

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

## Configurações {#configurations}

O número total de configurações aceitas pelo Gerenciamento de decisão não pode exceder 20.000.

A contagem total de configurações é o número total de [regras de limitação](offer-library/add-constraints.md#capping) existentes em sua sandbox. Para cada regra de limitação aplicada em todos os [posicionamentos](offer-library/creating-placements.md), a regra deve ser multiplicada em todos os posicionamentos associados à oferta especificada.
