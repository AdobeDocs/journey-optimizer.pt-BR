---
product: experience platform
solution: Experience Platform
title: Modelo de otimização personalizado
description: Saiba mais sobre modelos de otimização personalizados
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Modelo de otimização personalizada {#personalized-optimization-model}

>[!CAUTION]
>
>O uso de modelos de Otimização personalizada está disponível no momento somente para usuários selecionados.

## Visão geral {#overview}

Ao utilizar as tecnologias de ponta no aprendizado de máquina supervisionado e no profundo aprendizado, a personalização automática permite que um usuário empresarial (profissional de marketing) defina objetivos de negócios e utilize seus dados de clientes para treinar modelos orientados a negócios para fornecer ofertas personalizadas e maximizar KPIs.

## Pressupostos e limitações do modelo principal {#key}

Para maximizar a vantagem do uso da personalização automática, há algumas suposições e limitações importantes que devem ser levadas em conta.

* **As ofertas são diferentes o suficiente para que os usuários tenham preferências diferentes entre as ofertas em consideração**. Se as ofertas forem muito semelhantes, um modelo resultante terá menos impacto, pois as respostas são aparentemente aleatórias.
Por exemplo, se um banco tem duas ofertas de cartões de crédito com a única diferença de cor, talvez não seja importante qual cartão é recomendado, mas se cada cartão tem termos diferentes, isso fornece uma razão para determinados clientes escolherem um e fornecerem diferença suficiente entre ofertas para criar um modelo mais impactante.
* **A composição do tráfego do usuário é estável**. Se a composição do tráfego do usuário mudar drasticamente durante o treinamento e a previsão do modelo, o desempenho do modelo poderá degradar-se. Por exemplo, suponha que na fase de treinamento do modelo, somente os dados para usuários no segmento A estejam disponíveis, mas o modelo treinado é usado para gerar previsões para usuários no segmento B, então o desempenho do modelo pode ser afetado.
* **O desempenho das ofertas não muda drasticamente em um curto período** como esse modelo é atualizado semanalmente e as alterações no desempenho são transmitidas conforme o modelo é atualizado. Por exemplo, um produto era muito popular antes, mas um relatório público identifica o produto como prejudicial para nossa saúde, e esse produto se torna impopular extremamente rápido. Nesse cenário, o modelo pode continuar a prever esse produto até que o modelo seja atualizado com alterações no comportamento do usuário.

## Como funciona {#how}

A personalização automática aprende interações complexas de recursos entre ofertas, informações dos usuários e informações contextuais para recomendar ofertas personalizadas para usuários finais. Os recursos são entradas no modelo.

Há três tipos de recursos:

| Tipos de recursos | Como adicionar recursos aos modelos |
|--------------|----------------------------|
| Objetos de decisão (placementID, activityID, decisionScopeID) | Parte do feedback do gerenciamento de decisões Eventos de experiência enviados para a AEP |
| Segmentos | 0 a 50 segmentos podem ser adicionados como recursos ao criar o modelo de API de classificação |
| Dados de contexto | Parte dos eventos de experiência de feedback de decisão enviados para a AEP. Dados de contexto disponíveis para adicionar ao schema: Detalhes de comércio, Detalhes do canal, Detalhes do aplicativo, Detalhes da Web, Detalhes do ambiente, Detalhes do dispositivo, placeContext |

O modelo tem duas fases:

* No **treinamento de modelo offline** , um modelo é treinado pelo aprendizado e pela memorização de interações de recursos em dados históricos.
* No **inferência online** , as ofertas de candidatos são classificadas com base nas pontuações em tempo real geradas pelo modelo. Ao contrário das técnicas tradicionais de filtragem colaborativa, que são difíceis de incluir recursos para usuários e ofertas, a personalização automática é um método de recomendação baseado em aprendizado profundo e pode incluir e aprender padrões complexos e não lineares de interação de recursos.

Este é um exemplo simplificado para ilustrar a ideia básica por trás da personalização automática. Suponha que tenhamos um conjunto de dados que armazene interações históricas entre usuários e ofertas, que é mostrado na Figura 1. Há:
* Duas ofertas, offer_1 e offer_2,
* Dois recursos, feature_1 e feature_2,
* Uma coluna de resposta.

O valor de feature_1, feature_2 e response é 0 ou 1. Quando olhamos para as caixas azuis e laranja na Figura 1, podemos descobrir que para a oferta_1, as respostas têm mais probabilidade de ser 1 quando feature_1 e feature_2 têm os mesmos valores, enquanto para offer_2, os rótulos têm mais probabilidade de ser 1 quando feature_1 for 0 e feature_2 for 1. Também podemos ver que na caixa vermelha, offer_1 é veiculada quando feature_1 é 0 e feature_2 é 1 e a resposta é 0. Com base no padrão que vemos em caixas laranja, quando feature_1 é 0 e feature_2 é 1, offer_2 é provavelmente uma recomendação melhor.

Basicamente, essa é a ideia de aprender e memorizar interações de recursos históricos e aplicá-las para gerar previsões personalizadas.

![](../assets/perso-ranking-schema.png)

## Problema de inicialização a frio {#cold-start}

O problema de inicialização a frio ocorre quando não há dados suficientes para fazer recomendações. Para a personalização automática, há dois tipos de problemas de início frio.

* **Depois de criar uma nova estratégia de classificação sem dados históricos**, as ofertas serão fornecidas aleatoriamente por um período de tempo para coletar dados, e os dados serão usados para treinar o primeiro modelo.
* A **Depois que o primeiro modelo for lançado**, 10% do tráfego total será alocado para serviços aleatórios, enquanto 90% do tráfego será usado para recomendações de modelo. Portanto, se novas ofertas fossem adicionadas à estratégia de classificação, elas seriam entregues como parte dos 10% do tráfego. Os dados coletados nessas ofertas determinam o número de vezes que são selecionados entre os 90% do tráfego à medida que o modelo continua sendo atualizado.

## Retreino {#re-training}

Os modelos serão treinados novamente para conhecer as interações de recursos mais recentes e reduzir a degradação semanal do desempenho do modelo.
