---
product: experience platform
solution: Experience Platform
title: Sobre modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 0%

---

# Modelos de IA {#ai-models}

## Introdução a modelos de IA {#get-started-with-ai-rankings}

Você pode usar um sistema de modelo treinado que classifica ofertas para exibição em um determinado perfil.

>[!CAUTION]
>
>O uso de modelos de IA está disponível no momento somente para usuários selecionados.

Este recurso permite que você crie diferentes **Modelos de IA** com base em suas metas comerciais. Usando essas diferentes estratégias baseadas em objetivos em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

Por exemplo, você pode selecionar um modelo de IA para o canal de email e outro para o canal de push. Para cada canal, o sistema de modelo treinado aproveitará vários pontos de dados para determinar qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas ou uma [fórmula de classificação](create-ranking-formulas.md).

Depois que um modelo de IA for criado, atribua-o a uma disposição em uma decisão. Saiba mais em [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md).

>[!NOTE]
>
>Atualmente em [!DNL Journey Optimizer] o único tipo de modelo suportado para a classificação de AI é **otimização automática**.

## Modelo de otimização automática {#auto-optimization}

Um modelo de otimização automática tem como objetivo fornecer ofertas que maximizem o retorno (KPIs) definido pelos clientes comerciais. Esses KPIs podem estar na forma de taxas de conversão, receita etc. Neste ponto, a Otimização automática se concentra na otimização de cliques de oferta com a conversão de oferta como nossa meta. A otimização automática não é personalizada e otimiza com base no desempenho &quot;global&quot; das ofertas.

### Terminologia

Os seguintes termos são úteis quando falamos de Otimização automática:

* **Multi-armed bandit**: A [multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit)A abordagem {target=&quot;_blank&quot;} à otimização equilibra o aprendizado exploratório e o aproveitamento desse aprendizado.

* **Amostragem de Thomson**: a Amostragem de Thompson é um algoritmo para problemas de decisão online, onde as ações são executadas sequencialmente de uma maneira que deve equilibrar entre explorar o que é conhecido para maximizar o desempenho imediato e investir para acumular novas informações que podem melhorar o desempenho futuro. [Saiba mais](#thompson-sampling)

* [**Distribuição beta**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}: Conjunto contínuo [distribuições de probabilidade](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} definido no intervalo [0, 1] [parametrizado](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} por dois positivos [parâmetros de forma](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

### Amostragem de Thompson {#thompson-sampling}

O algoritmo subjacente à otimização automática é **Amostragem de Thompson**. Nesta seção, discutimos a intuição por trás da amostragem de Thompson.

[Amostragem de Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, ou bandidos bayesianos, é uma abordagem bayesiana do problema multi-armed bandit.  A ideia básica é tratar a recompensa média? de cada oferta como uma **variável aleatória** e usar os dados que coletamos até agora, para atualizar nossa &quot;crença&quot; sobre a recompensa média. Essa &quot;crença&quot; é representada matematicamente por um **distribuição de probabilidade posterior** - essencialmente uma gama de valores para a recompensa média, juntamente com a plausibilidade (ou probabilidade) de a recompensa ter esse valor para cada oferta. Então, para cada decisão, nós vamos **amostra de um ponto de cada uma dessas distribuições de recompensa posterior** e selecione a oferta cuja recompensa de amostra tinha o valor mais alto.

Esse processo é ilustrado na figura abaixo, onde temos 3 ofertas diferentes. Inicialmente, não temos provas dos dados e supomos que todas as ofertas têm uma distribuição posterior uniforme de recompensas. Desenvolvemos uma amostra da distribuição posterior de recompensa de cada oferta. A amostra selecionada da distribuição da Oferta 2 tem o valor mais alto. Este é um exemplo de **exploração**. Após mostrar a Oferta 2, coletamos qualquer recompensa potencial (por exemplo, conversão/não conversão) e atualizamos a distribuição posterior da Oferta 2 usando o Bayes Theorem, conforme explicado abaixo.  Continuamos esse processo e atualizamos as distribuições posteriores sempre que uma oferta é mostrada e a recompensa é coletada. Na segunda figura, a Oferta 3 é selecionada - apesar da Oferta 1 ter a recompensa média mais alta (sua distribuição de recompensa posterior é mais à direita), o processo de amostragem de cada distribuição nos levou a escolher uma Oferta 3 aparentemente subotimizada. Ao fazê-lo, damos a nós mesmos a oportunidade de aprender mais sobre a verdadeira distribuição de recompensas da Oferta 3.

À medida que mais amostras são coletadas, a confiança aumenta e uma estimativa mais precisa da possível recompensa é obtida (correspondente a distribuições de recompensa mais estreitas). Esse processo de atualização de nossas crenças à medida que mais evidências são disponibilizadas é conhecido como **Inferência Bayesiana**.

Eventualmente, se uma oferta (por exemplo, Oferta 1) for um vencedor claro, sua distribuição de recompensa posterior será separada de outras. Neste ponto, para cada decisão, a recompensa amostrada da Oferta 1 provavelmente será a mais alta, e nós a escolheremos com uma probabilidade maior. Isso é **exploração** - acreditamos fortemente que a Oferta 1 é a melhor, e por isso está sendo escolhida para maximizar recompensas.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Para cada decisão, damos uma amostra de um ponto das distribuições de recompensa posteriores. A oferta com o valor de amostra mais alto (taxa de conversão) será escolhida. Na fase inicial, todas as ofertas têm distribuição uniforme, já que não temos nenhuma evidência sobre as taxas de conversão das ofertas a partir dos dados. À medida que coletamos mais amostras, as distribuições posteriores tornam-se mais estreitas e precisas. Em última análise, a oferta com a taxa de conversão mais alta será escolhida todas as vezes.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Detalhes técnicos**

Para calcular/atualizar classificações contábeis, usamos **Bayes Theorem**. Para cada oferta ***i***, queremos calcular seus ***P(??i | dados)***, ou seja, para cada oferta ***i***, a probabilidade de um valor de recompensa **??i** , dados que coletamos até agora para essa oferta.

De Bayes Theorem:

***Posterior = Probabilidade * Anterior***

O **probabilidade anterior** é a suposição inicial sobre a probabilidade de produzir uma saída. A probabilidade, após a coleta de alguma evidência, é conhecida como **probabilidade posterior**. 

A otimização automática é projetada para considerar recompensas binantes (clique/sem clique). Neste caso, a probabilidade representa o número de sucessos de N ensaios e é modelada por um **Distribuição binomial**. Para algumas funções de probabilidade, se você escolher um determinado anterior, o posterior acaba sendo da mesma distribuição que o anterior. Tal anterior é chamado de **conjugar anterior**. Esse tipo de pré-requisito torna o cálculo de distribuição posterior muito simples. O **Distribuição beta** é um conjugado antes da probabilidade binomial (recompensas binantes) e, portanto, é uma escolha conveniente e sensata para as distribuições de probabilidade anterior e posterior. A distribuição Beta leva dois parâmetros, ***α*** e ***β***. Esses parâmetros podem ser considerados como a contagem de sucessos e falhas e o valor médio dado por:

![](../assets/ai-ranking-beta-distribution.png)

A função Probabilidade, como explicamos acima, é modelada por uma distribuição Binômica, com os sucessos de s (conversões) e de falhas (sem conversões) e q é um [variável aleatória](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} com um [distribuição beta](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

O anterior é modelado pela distribuição Beta e a distribuição posterior assume a seguinte forma:

![](../assets/ai-ranking-posterior-distribution.svg)

O posterior é calculado simplesmente adicionando o número de sucessos e falhas aos parâmetros existentes ***α***, ***β***.

Para otimização automática, como mostrado no exemplo acima, começamos com uma distribuição anterior ***Beta(1, 1)*** (distribuição uniforme) para todas as ofertas e depois de obter os sucessos e as falhas de uma determinada oferta, o posterior se torna uma distribuição Beta com parâmetros ***(s+α, f+β)*** para essa oferta.
+++

**Tópicos relacionados**:

Para aprofundar a amostragem de Thompson, leia os seguintes trabalhos de pesquisa:
* [Avaliação Empírica da Amostragem de Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Análise da Amostragem de Thompson para o Problema Multi-armed Bandit](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

### Problema de arranque a frio

O problema de &quot;inicialização imediata&quot; ocorre quando uma nova oferta é adicionada a uma campanha e não há dados disponíveis sobre a taxa de conversão da nova oferta. Durante esse período, precisamos criar uma estratégia com relação à frequência com que essa nova oferta é escolhida para que a queda de desempenho seja minimizada, enquanto coletamos informações sobre a taxa de conversão dessa nova oferta. Há várias soluções disponíveis para resolver esse problema. A chave é encontrar um equilíbrio entre a exploração dessa nova oferta enquanto não sacrificamos muito a exploração. Atualmente, usamos &quot;distribuição uniforme&quot; como nossa suposição inicial sobre a taxa de conversão da nova oferta (distribuição anterior). Basicamente, fornecemos todos os valores de taxa de conversão com probabilidade de ocorrência igual.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figura 2**: *Considere uma campanha com 3 ofertas. Enquanto a campanha está ao vivo, a Oferta 4 é adicionada à campanha. Inicialmente, não temos dados sobre a taxa de conversão da Oferta 4 e temos de lidar com o problema do arranque a frio. Usamos a distribuição uniforme como nossa suposição inicial sobre a taxa de conversão da Oferta 4, enquanto coletamos dados para essa nova oferta. Como explicado na seção [Amostragem de Thompson](#thompson-sampling) , para escolher qual oferta será exibida para um usuário, exemplificamos pontos das distribuições de recompensas posteriores das ofertas e selecionamos a oferta com o valor de amostra mais alto. No exemplo acima, a Oferta 4 é escolhida e posteriormente com base na recompensa coletada, a distribuição posterior dessa oferta é atualizada, conforme explicado no [Amostragem de Thompson](#thompson-sampling) seção.*

### Medição de incentivo

&quot;Aumento&quot; é a métrica usada para medir o desempenho de qualquer estratégia implantada no serviço de classificação, em comparação com a estratégia de linha de base (servindo ofertas aleatoriamente).

Por exemplo, se estivermos interessados em medir o desempenho de uma estratégia de Amostragem de Thompson (TS) usada no serviço de classificação, e o KPI for a taxa de conversão (CVR), o &quot;aumento&quot; da estratégia de TS em relação à estratégia de linha de base será definido como:

![](../assets/ai-ranking-lift.png)

