---
product: experience platform
solution: Experience Platform
title: Modelo de otimização personalizado
description: Saiba mais sobre modelos de otimização personalizados
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: 9188b144d1f98f57c585c3828420b9cd48d1d90a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Modelo de otimização personalizado {#personalized-optimization-model}

## Visão geral {#overview}

Ao aproveitar as tecnologias de ponta em aprendizagem de máquina e aprendizagem profunda supervisionadas, a otimização personalizada permite que um usuário empresarial (profissional de marketing) defina objetivos de negócios e utilize os dados de clientes para treinar modelos orientados a negócios a fim de fornecer ofertas personalizadas e maximizar KPIs.

![](../../rn/assets/do-not-localize/ai-ranking.gif)

## Principais premissas e limitações do modelo {#key}

Para maximizar a vantagem de usar a otimização personalizada, há algumas suposições e limitações importantes a serem observadas.

* **As ofertas são diferentes o suficiente para que os usuários tenham preferências diferentes entre as ofertas em consideração**. Se as ofertas forem muito semelhantes, um modelo resultante terá menos impacto, pois as respostas são aparentemente aleatórias.
Por exemplo, se um banco tiver duas ofertas de cartões de crédito com a única diferença sendo a cor, pode não importar qual cartão é recomendado, mas se cada cartão tiver termos diferentes, isso fornece uma explicação para por que determinados clientes escolheriam um e forneceriam diferença suficiente entre as ofertas para criar um modelo mais impactante.
* **A composição do tráfego de usuário está estável**. Se a composição do tráfego do usuário mudar drasticamente durante o treinamento e a previsão do modelo, o desempenho do modelo poderá diminuir. Por exemplo, suponha que, na fase de treinamento do modelo, apenas os dados para usuários no público-alvo A estejam disponíveis, mas o modelo treinado seja usado para gerar previsões para usuários no público-alvo B, então o desempenho do modelo pode ser afetado.
* **O desempenho das ofertas não é alterado drasticamente em um curto período**, pois esse modelo é atualizado semanalmente e as alterações no desempenho são transmitidas como as atualizações do modelo. Por exemplo, um produto era muito popular antes, mas um relatório público identifica o produto como prejudicial à nossa saúde, e esse produto se torna impopular extremamente rápido. Nesse cenário, o modelo pode continuar a prever esse produto até que o modelo seja atualizado com alterações no comportamento do usuário.

## Como funciona {#how}

O modelo aprende interações de recursos complexos entre ofertas, informações dos usuários e informações contextuais para recomendar ofertas personalizadas aos usuários finais. Os recursos são entradas no modelo.

Há três tipos de recursos:

| Tipos de recursos | Como adicionar recursos aos modelos |
|--------------|----------------------------|
| Objetos de decisão (placementID, activityID, decisionScopeID) | Parte dos eventos de experiência de feedback da gestão de decisões enviados para a AEP |
| Públicos-alvo | De 0 a 50 públicos-alvo podem ser adicionados como recursos ao criar o modelo de IA de classificação |
| Dados de contexto | Parte dos Eventos de experiência de feedback de decisão enviados para a AEP. Dados de contexto disponíveis para adicionar ao esquema: Detalhes do Commerce, Detalhes do canal, Detalhes do aplicativo, Detalhes da Web, Detalhes do ambiente, Detalhes do dispositivo, placeContext |

O modelo tem duas fases:

* Na fase **treinamento de modelo offline**, um modelo é treinado ao aprender e memorizar interações de recursos em dados históricos.
* Na fase **inferência online**, as ofertas de candidatos são classificadas com base nas pontuações em tempo real geradas pelo modelo. Ao contrário das técnicas tradicionais de filtragem colaborativa, que é difícil incluir recursos para usuários e ofertas, a otimização personalizada é um método de recomendação baseado em deep learning, além de ser capaz de incluir e aprender padrões de interação de recursos complexos e não lineares.

Este é um exemplo simplificado para ilustrar a ideia básica por trás da otimização personalizada. Suponha que tenhamos um conjunto de dados que armazena interações históricas entre usuários e ofertas, o que é mostrado na Figura 1. Há:
* Duas ofertas, offer_1 e offer_2,
* Dois recursos, feature_1 e feature_2,
* Uma coluna de resposta.

O valor de feature_1, feature_2 e resposta é 0 ou 1. Quando observamos as caixas azuis e as caixas laranja na Figura 1, podemos descobrir que, para offer_1, as respostas são mais propensas a serem 1 quando feature_1 e feature_2 têm os mesmos valores, enquanto para offer_2, os rótulos são mais propensos a serem 1 quando feature_1 é 0 e feature_2 é 1. Também podemos ver que na caixa vermelha, offer_1 é exibido quando feature_1 é 0 e feature_2 é 1, e a resposta é 0. Com base no padrão que vemos em caixas laranja, quando feature_1 é 0 e feature_2 é 1, offer_2 provavelmente é uma recomendação melhor.

Basicamente, essa é a ideia de aprender e memorizar interações com características históricas e aplicá-las para gerar previsões personalizadas.

![](../assets/perso-ranking-schema.png)

## Problema de inicialização a frio {#cold-start}

O problema de partida a frio ocorre quando não há dados suficientes para fazer a recomendação. Para otimização personalizada, há dois tipos de problemas de inicialização a frio.

* **Depois de criar um novo modelo de IA sem dados históricos**, as ofertas serão fornecidas aleatoriamente por um período para coletar dados, e os dados serão usados para treinar o primeiro modelo.
* **Depois que o primeiro modelo for lançado**, 10% do tráfego total será alocado para serviço aleatório, enquanto 90% do tráfego será usado para recomendações de modelo. Portanto, se novas ofertas fossem adicionadas ao modelo de IA, elas seriam entregues como parte dos 10% do tráfego. Os dados coletados nessas ofertas determinariam o número de vezes que são selecionados entre os 90% do tráfego à medida que o modelo continua a ser atualizado.

## Retreinamento {#re-training}

Os modelos serão treinados novamente para aprender as interações de recursos mais recentes e atenuar a degradação do desempenho do modelo semanalmente.
