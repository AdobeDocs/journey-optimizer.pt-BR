---
solution: Journey Optimizer
product: Journey Optimizer
title: Modelos de otimização automática
description: Saiba mais sobre os modelos de otimização automática
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 8a8b66cb-dd96-4373-bbe0-a67e0dc0b2c0
version: Journey Orchestration
source-git-commit: ca31e819b0d120f54adfe2035ecacb21ac4f1f15
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# Modelos de otimização automática {#auto-optimization-model}

O modelo de Otimização automática de [!DNL Adobe Journey Optimizer] é um modelo de aprendizado de reforço que maximiza a taxa de cliques (CTR) da oferta explorando todas as ofertas (ou conteúdo) e, em seguida, classificando os itens com base na CTR prevista, após a aplicação das regras de elegibilidade e dos limites de frequência.

## Casos de uso e benefícios {#use-cases-benefits}

A otimização automática pode ser usada a qualquer momento em que você quiser configuração rápida e fácil, quiser encontrar ofertas vencedoras gerais e maximizar cliques em ofertas em um único canal. Por exemplo:

* Escolha as melhores ofertas a serem inseridas em uma página da Web para maximizar os cliques na oferta.
* Escolha as melhores ofertas a serem inseridas em um email para maximizar os cliques na oferta.
* Escolha as melhores ofertas para inserir em uma tela de aplicativo móvel para maximizar os cliques na oferta.

A otimização automática é uma boa escolha quando:

* As ofertas mudam com o tempo ou com frequência: o modelo de otimização automática é retreinado a cada seis horas.

## Requisitos e limitações {#requirements-limitations}

A otimização automática tem os seguintes requisitos e limites:

* A otimização automática requer um conjunto de dados de treinamento contendo eventos de exibição de oferta, eventos de clique de oferta e o grupo de campos Evento de experiência - Interações de apresentação.
* Os modelos de otimização automática não podem ser utilizados em solicitações para a API de decisão em lote.
* A otimização automática sempre otimiza para cliques de oferta. Para maximizar para um objetivo diferente dos cliques na oferta, use o modelo [Otimização personalizada](personalized-optimization-model.md).
* A otimização automática tenta encontrar ofertas vencedoras gerais e não encontra uma classificação personalizada para cada cliente. Para encontrar classificações personalizadas para cada cliente, use o modelo [Otimização personalizada](personalized-optimization-model.md).

Para treinar um modelo de otimização automática, o conjunto de dados deve atender aos seguintes requisitos mínimos:

* Pelo menos 2 ofertas no conjunto de dados devem ter pelo menos 100 eventos de exibição e 5 eventos de clique nos últimos 14 dias.
* As ofertas com menos de 100 exibições e/ou eventos de 5 cliques nos últimos 14 dias serão tratadas pelo modelo como novas ofertas e só estarão qualificadas para serem atendidas pelo bandido de exploração.
* Ofertas com mais de 100 exibições e eventos de 5 cliques nos últimos 14 dias serão tratadas pelo modelo como ofertas existentes e estão qualificadas para serem atendidas por bandidos de exploração e pesquisa.

Até a primeira vez que um modelo de otimização automática for treinado, as ofertas em uma estratégia de seleção que utiliza um modelo de otimização automática serão atendidas aleatoriamente.

## Equilíbrio entre otimização e aprendizagem {#balancing-optimization-learning}

A otimização automática é um modelo de [aprendizado de reforço](https://en.wikipedia.org/wiki/Reinforcement_learning){target="_blank"} que aprende sobre o desempenho click-through de ofertas com base no comportamento real do cliente. O reforço dos modelos de aprendizagem procura maximizar um objetivo ao escolher ações com resultados mais previsíveis. No entanto, um modelo que sempre apresentasse a cada cliente os itens com os melhores resultados previstos nunca aprenderia sobre o desempenho de novos itens introduzidos ao longo do tempo (o chamado &quot;problema de inicialização a frio&quot;), nem sobre as alterações no desempenho de outros itens existentes resultantes de alterações no comportamento dos clientes ao longo do tempo. Os modelos de aprendizado de reforço devem, portanto, gerenciar o que é comumente chamado de [equilíbrio entre otimização e aprendizado](https://en.wikipedia.org/wiki/Exploration%E2%80%93exploitation_dilemma){target="_blank"}.

A otimização automática usa uma abordagem comum chamada [bandit multi-armed](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} para gerenciar o trade-off. O bandido multi-armado toma decisões de classificação baseadas em:

* a taxa de cliques prevista de cada item
* as diferenças na taxa de click-through prevista de cada item
* o grau de incerteza do modelo sobre suas previsões para cada item.

Bandidos multi-armados utilizam essa informação, juntamente com variabilidade aleatória, para escolher as ações a serem tomadas. A otimização automática é um [algoritmo de conjunto](https://en.wikipedia.org/wiki/Ensemble_learning){target="_blank"} que contém vários bandidos com vários braços para garantir que todas as ofertas sejam exploradas adequadamente e, ao mesmo tempo, maximizar o desempenho geral.

Ao responder a um pedido de classificação, um bandido multi-armado &quot;supervisor&quot; primeiro faz uma escolha sobre se este pedido deve ser tendencioso para a exploração ou tendencioso para a exploração. Essa decisão é tomada usando uma abordagem &quot;epsilon-greedy&quot;.

A segunda camada de classificação é executada por um de dois bandidos [Thompson sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}:

* 10% do tráfego é alocado para um bandit focado em exploração que tem mais probabilidade de recomendar novas ofertas ou aquelas com dados limitados, sob o pressuposto de que o modelo se beneficiaria de aprender mais sobre o comportamento do cliente em resposta a essas ofertas.
* 90% do tráfego é alocado para um bandit focado em exploração, que tem mais probabilidade de recomendar consistentemente ofertas de alto desempenho ao longo do tempo, sob o pressuposto de que ofertas de dados novos ou baixos têm mais probabilidade de ter desempenho insatisfatório até prova em contrário.

Em um sentido técnico, essas suposições são parâmetros da distribuição de probabilidade anterior, também referidos como [antecedentes](https://en.wikipedia.org/wiki/Prior_probability){target="_blank"}. À medida que as ofertas reúnem mais dados de exibição e cliques, a influência dos antecedentes escolhidos torna-se menor, e as previsões feitas pelos dois bandidos tendem a convergir ao longo do tempo.

Nossa abordagem de combinar vários bandidos e alocar algum tráfego dedicado para exploração oferece vários benefícios:

* o modelo aprende mais rapidamente sobre as ofertas mais recentes com menos dados
* o modelo continua a conhecer todas as ofertas e responde às mudanças no comportamento do cliente ao longo do tempo
* o modelo não exagera ao favorecer agressivamente ofertas com CTR aparente mais alta, mas poucas observações, ou desfavorecer agressivamente ofertas com CTR aparente mais baixa, mas poucas observações
* o modelo é robusto para lidar com decisões de alocação de tráfego em centenas de ofertas com dados de cliques esparsos e com quantidades muito diferentes de dados históricos

## Amostragem de Thompson {#thompson-sampling}

[Amostragem de Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}, ou bandidos Bayesianos, é uma abordagem Bayesiana para o problema do bandido multi-armado. O modelo trata a recompensa média 𝛍 de cada oferta como uma variável aleatória e usa os dados que coletamos até agora para atualizar nossa &quot;crença&quot; sobre a recompensa média. Esta &quot;crença&quot; é representada matematicamente por uma distribuição de probabilidade posterior - essencialmente um intervalo de valores para a recompensa média, juntamente com a plausibilidade (ou probabilidade) que a recompensa tem esse valor para cada oferta. Em seguida, para cada decisão, faremos a amostragem de um ponto de cada uma dessas distribuições de recompensa posteriores e selecionaremos a oferta cuja recompensa amostrada teve o valor mais alto.

Esse processo é ilustrado na figura abaixo, onde temos 3 ofertas diferentes. Inicialmente, não temos nenhuma evidência dos dados e assumimos que todas as ofertas têm uma distribuição de recompensa posterior uniforme. Tiramos uma amostra da distribuição de recompensa posterior de cada oferta. A amostra selecionada na distribuição da Oferta 2 tem o valor mais alto. Este é um exemplo de exploração. Depois de mostrar a Oferta 2, coletamos qualquer recompensa potencial (por exemplo, conversão/sem conversão) e atualizamos a distribuição posterior da Oferta 2 usando o Teorema de Bayes como explicado abaixo. Continuamos esse processo e atualizamos as distribuições posteriores sempre que uma oferta é exibida e a recompensa é coletada. Na segunda figura, a Oferta 3 é selecionada - apesar de a Oferta 1 ter a maior recompensa média (sua distribuição de recompensa posterior é a mais à direita), o processo de amostragem de cada distribuição levou-nos a escolher uma Oferta 3 aparentemente abaixo do ideal. Ao fazer isso, oferecemos a nós mesmos a oportunidade de saber mais sobre a verdadeira distribuição de recompensa da Oferta 3.

À medida que mais amostras são coletadas, a confiança aumenta e uma estimativa mais precisa da possível recompensa é obtida (correspondendo a distribuições de recompensa mais estreitas). Esse processo de atualização de nossas crenças à medida que mais evidências se tornam disponíveis é conhecido como **Inferência Bayesiana**.

Eventualmente, se uma oferta (por exemplo, Oferta 1) for um vencedor claro, sua distribuição de recompensa posterior será separada das outras. Neste ponto, para cada decisão, a recompensa amostrada da Oferta 1 provavelmente será a mais alta, e nós a escolheremos com uma probabilidade mais alta. Trata-se de exploração — acreditamos que a Oferta 1 é a melhor e, portanto, está sendo escolhida para maximizar as recompensas.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Para cada decisão, analisamos um ponto das distribuições posteriores da recompensa. A oferta com o valor de amostra mais alto (taxa de conversão) será escolhida. Na fase inicial, todas as ofertas têm distribuição uniforme, já que não temos nenhuma evidência sobre as taxas de conversão das ofertas com base nos dados. À medida que coletamos mais amostras, as distribuições posteriores ficam mais estreitas e precisas. Por fim, a oferta com a maior taxa de conversão será escolhida sempre.*

+++ Detalhes do cálculo

Para calcular/atualizar distribuições, usamos o Teorema de **Bayes&#39;**. Para cada oferta ***i***, queremos calcular seus ***P(𝛍i | dados)***, ou seja, para cada oferta ***i***, a probabilidade de um valor de recompensa **𝛍i**, dados os dados coletados até o momento para essa oferta.

A partir do Teorema de Bayes:

***Posterior = Probabilidade * Anterior***

A **probabilidade anterior** é a estimativa inicial sobre a probabilidade de produzir uma saída. A probabilidade, após a coleta de algumas evidências, é conhecida como **probabilidade posterior**.

A otimização automática foi projetada para considerar recompensas binárias (clique/sem clique). Nesse caso, a probabilidade representa o número de sucessos de N tentativas e é modelada por uma distribuição binomial. Para algumas funções verossímeis, se você escolher um determinado anterior, o posterior acaba ficando na mesma distribuição que o anterior. O anterior então é chamado de **conjugado anterior**. Esse tipo de análise prévia torna muito simples o cálculo da distribuição posterior. A [distribuição de Beta](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"} é um conjugado antes da probabilidade binomial (recompensas binárias), e assim é uma escolha conveniente e sensata para as distribuições de probabilidade anterior e posterior. A distribuição do Beta usa dois parâmetros, ***α*** e ***β***. Esses parâmetros podem ser considerados como a contagem de sucessos e falhas e o valor médio fornecido por:

![](../assets/ai-ranking-beta-distribution.png)

A função Probabilidade, como explicado acima, é modelada por uma distribuição binomial, com s sucessos (conversões) e f falhas (sem conversões) e q é uma variável aleatória com uma distribuição Beta.

O anterior é modelado pela distribuição do Beta e a distribuição posterior assume a seguinte forma:

![](../assets/ai-ranking-posterior-distribution.svg)

+++

### Viés de exploração e viés de exploração {#exploration-exploitation-bias}

Um valor inicial deve ser escolhido para os parâmetros ***α***, ***β***. A otimização automática inclui um bandit de amostragem de Thompson com viés de exploração e um bandit de amostragem de Thompson com viés de exploração que utilizam diferentes ***α*** iniciais, ***β*** anteriores em suas distribuições beta.

Em uma abordagem geral de amostragem de Thompson, a posterior é calculada simplesmente adicionando o número de sucessos e falhas aos parâmetros existentes ***α***, ***β***. A otimização automática utiliza diferentes fatores de ponderação para novos sucessos e falhas para modificar o impacto de novos dados em comparação aos dados anteriores em bandidos com tendência à exploração e com tendência à exploração.

## Referências {#references}

Para um mergulho mais profundo em Thompson sampling bandits, consulte os seguintes artigos de pesquisa:

* [Uma Avaliação Empírica da Amostragem de Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [Análise de Amostragem de Thompson para o problema do Multi-armed Bandit](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}
