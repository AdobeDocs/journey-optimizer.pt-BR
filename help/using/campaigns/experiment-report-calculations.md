---
title: Cálculos estatísticos usados no relatório de Experimentação
description: Saiba mais sobre os cálculos estatísticos usados ao executar relatórios de experiência
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: b3336381-bc73-4c8f-938f-f10fe37305b0
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# Cálculos estatísticos no relatório de Experimentação {#experiment-report-calculations}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao experimento de conteúdo](get-started-experiment.md)
* [Criar um experimento de conteúdo](content-experiment.md)
* [Compreender cálculos estatísticos](experiment-calculations.md)
* [Configurar relatórios de experimentação](reporting-configuration.md)
* **[Cálculos estatísticos no relatório de Experimentação](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

Esta página documenta os cálculos estatísticos detalhados usados no relatório de Experimentação para Campanhas no Adobe Journey Optimizer.

Observe que esta página se destina a usuários técnicos.

## Taxa de conversão

A taxa de conversão ou **média**, μ<sub>ν</sub> para cada tratamento `ν` em um Experimento é definido como uma proporção da soma da métrica ao número de perfis atribuídos a essa métrica, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Aqui, Y<sub>iν</sub> é o valor da métrica de objetivo para cada perfil `i`, que foi atribuída a uma determinada variante *ν*. Quando a métrica de objetivo é uma métrica &quot;exclusiva&quot;, ou seja, é uma contagem do número de perfis que fazem uma ação específica, ela é exibida como uma taxa de conversão e formatada como uma porcentagem. Quando a métrica é uma métrica de &quot;contagem&quot; ou &quot;valor total&quot; (por exemplo, aberturas de email, receita respectivamente), a estimativa média da métrica é exibida como uma &quot;Contagem por perfil&quot; ou &quot;Valor por perfil&quot;.

Sempre que necessário, o desvio padrão da amostra é usado com a expressão:

![](assets/statistical_2.png){width="225" align="center"}

## Aumento {#lift}

O aumento entre uma variante  *ν* e a variante de controle  *ν<sub>0</sub>* é o &quot;delta&quot; relativo nas taxas de conversão, definido como o cálculo abaixo, onde as taxas de conversão individuais são definidas acima. Isso é exibido como uma porcentagem.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalos de confiança válidos a qualquer momento para tratamentos individuais

O painel Experimentação do Jornada exibe intervalos de confiança &quot;válidos a qualquer momento&quot; (sequências de confiança) para tratamentos individuais em um experimento.

A sequência de confiança de uma variante individual `ν` é fundamental para a metodologia estatística utilizada pelo Adobe. Você pode encontrar sua definição em [esta página](https://doi.org/10.48550/arXiv.2103.06476) (reproduzido a partir de [Waudby-Smith et al.]).

Se você estiver interessado em estimar um parâmetro de meta `ψ` como a taxa de conversão de uma variante em um Experimento, a dicotomia entre uma sequência de Intervalos de Confiança (CIs) de &quot;tempo fixo&quot; e uma Sequência de Confiança (CS) uniforme em tempo real pode ser resumida da seguinte maneira:

![](assets/statistical_4.png){width="500" align="center"}

Para um Intervalo de confiança regular, a garantia probabilística de que o parâmetro target está dentro do intervalo de valores Ċ<sub>n</sub> é válido somente em um único valor fixo de `n` em que `n` é o número de amostras). Por outro lado, para uma Sequência de confiança, temos garantias de que em todas as ocasiões/em todos os valores do tamanho da amostra `t`, o valor &quot;true&quot; do parâmetro de interesse está dentro dos limites.

Isso tem algumas implicações profundas que são muito importantes para testes online:

* O CS pode ser atualizado opcionalmente sempre que novos dados estiverem disponíveis.
* Os experimentos podem ser continuamente monitorados, interrompidos de forma adaptável ou continuados.
* O erro de tipo I é controlado em todos os momentos de interrupção, incluindo tempos dependentes de dados.

O Adobe usa Sequências de confiança assintótica, que para uma variante individual com estimativa média `μ` tem o formato :

![](assets/statistical_5.png){width="300" align="center"}

Em que:

* `N` é o número de unidades para essa variante.
* `σ` é uma amostra de estimativa do desvio padrão (definido acima).
* `α` é o nível desejado de erro de tipo I (ou probabilidade de incobertura). Isso é sempre definido como 0,05.
* z<sup>2</sup> é uma constante que ajusta o tamanho da amostra em que o CS é mais apertado. Adobe escolheu um valor universal de p.<sup>2</sup> = 10<sup>-2,8</sup>, que é adequado para os tipos de taxas de conversão observadas em experiências em linha.

## Confiança {#confidence}

A confiança utilizada pelo Adobe é uma confiança &quot;válida em qualquer altura&quot;, que é obtida invertendo a sequência de confiança para o efeito médio do tratamento.

Para ser preciso, em uma amostra de dois *t* teste para a diferença entre médias entre duas variantes, há um mapeamento 1:1 entre a variável *p*-valor para esse teste e o intervalo de confiança para a diferença entre meios. Por analogia, um valor em qualquer hora *p*- o valor pode ser obtido invertendo a sequência de confiança (sempre que válida) para o avaliador do efeito médio de tratamento:

![](assets/statistical_6.png){width="200" align="center"}

Aqui, *E* é uma expectativa. O estimador usado é um estimador de propensão inversa (IPW) ponderada. Considere N = N<sub>0</sub> +N<sub>1</sub> unidades, as atribuições de variante para cada unidade `i` rotulado por A<sub>i</sub>=0,1 se a unidade estiver atribuída à variante `ν`=0,1. Se os usuários forem atribuídos com probabilidade fixa (propensão)<sub>0</sub>, (1-λ<sub>0</sub>) e sua métrica de resultado é Y<sub>i</sub>, o estimador de IPW para o efeito médio do tratamento é:

![](assets/statistical_12.png){width="400" align="center"}

Registrando que *f* é a função de influência, Waudby-Smith et al. mostrou que a Sequência de Confiança desse avaliador é:

![](assets/statistical_7.png){width="500" align="center"}

Substituição da probabilidade da atribuição pelas suas estimativas empíricas: ì<sub>0</sub> = N<sub>0</sub>/N, o termo da variação pode ser expresso em termos de estimativas médias individuais da amostra μ<sub>0,1</sub> e estimativas de desvio-padrão, σ<sub>0,1</sub> como:

![](assets/statistical_8.png){width="500" align="center"}

Em seguida, lembre-se de que para um teste de hipótese regular com a estatística de teste z = (μ<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>existe uma correspondência entre `p`-valores e intervalos de confiança:

![](assets/statistical_9.png){width="500" align="center"}

em que `Φ` é a distribuição cumulativa do normal padrão. Para qualquer hora válida `p`- valores, considerando a sequência de confiança para o efeito médio de tratamento definido acima, podemos inverter essa relação:

![](assets/statistical_10.png){width="600" align="center"}

Finalmente, o **confiança válida em qualquer momento** é:

![](assets/statistical_11.png){width="200" align="center"}

## Declarando uma experiência como conclusiva

Para um Experimento com dois braços, o painel Experimentação do Journey Optimizer exibe uma mensagem declarando que um Experimento é **conclusivo** quando a confiança válida em qualquer momento exceder 95% (ou seja, o valor em qualquer momento `p`-valor é inferior a 5%).

Quando estão presentes mais de duas variantes, a correção de Bonferonni é aplicada para controlar a taxa de erro em termos de família. Para um experimento com `K` terapêuticas e um único tratamento de base (controlo), existem `K-1` testes de hipótese independentes. A correção de Bonferonni significa que rejeitamos a hipótese nula de que o controle e uma determinada variante têm meios iguais, se a qualquer momento for válida `p`-value (definido acima) for inferior a um limite de `α/(K-1)`.

## Braço de melhor desempenho

Quando um experimento é declarado conclusivo, aparece o braço com melhor desempenho. Este é o braço com o melhor desempenho (média ou taxa de conversão mais alta), entre o Conjunto que inclui o controle e todos os braços com um `p`-valor que está abaixo do limite de Bonferonni.
