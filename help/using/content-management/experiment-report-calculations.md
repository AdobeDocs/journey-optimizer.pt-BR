---
title: Cálculos estatísticos usados no relatório de experimentação
description: Saiba mais sobre cálculos estatísticos usados ao executar relatórios de experimento
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 67ba8861-be6f-42ae-b9b8-96168d0dd15c
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---

# Compreenda cálculos estatísticos no Relatório de experimentação {#experiment-report-calculations}

Esta página documenta os cálculos estatísticos detalhados usados no relatório Experimentação para campanhas no Adobe Journey Optimizer.

Observe que esta página é destinada a usuários técnicos.

## Índice de conversão

A taxa de conversão ou a **média**, μ<sub>ν</sub> para cada tratamento `ν` em um Experimento é definida como uma proporção da soma da métrica em relação ao número de perfis atribuídos a essa métrica, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Aqui, Y<sub>iewer</sub> é o valor da métrica de objetivo para cada perfil `i` atribuído a uma determinada variante *ν*. Quando a métrica de objetivo é uma métrica &quot;única&quot;, ou seja, é uma contagem do número de perfis que realizam uma ação específica, isso é exibido como uma taxa de conversão e formatado como uma porcentagem. Quando a métrica é uma métrica de &quot;contagem&quot; ou &quot;valor total&quot; (por exemplo, aberturas de email, receita respectivamente), a estimativa média da métrica é exibida como &quot;Contagem por perfil&quot; ou &quot;Valor por perfil&quot;.

Sempre que necessário, o desvio-padrão da amostra é utilizado com a expressão:

![](assets/statistical_2.png){width="225" align="center"}

## Elevação {#lift}

O aumento entre uma variante *ν* e a variante de controle *ν<sub>0</sub>* é o &quot;delta&quot; relativo em taxas de conversão, definido como o cálculo abaixo onde as taxas de conversão individuais são conforme definido acima. Isso é exibido como uma porcentagem.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalos de confiança válidos a qualquer momento para tratamentos individuais

O painel Experimentação do Jornada exibe intervalos de confiança &quot;válidos a qualquer momento&quot; (sequências de confiança) para tratamentos individuais em um experimento.

A sequência de confiança para uma variante individual `ν` é central para a metodologia estatística usada pelo Adobe. Você pode encontrar sua definição em [esta página](https://doi.org/10.48550/arXiv.2103.06476) (reproduzida de [Waudby-Smith et al.]).

Se você estiver interessado em estimar um parâmetro de destino `ψ`, como o índice de conversão de uma variante em um Experimento, a dicotomia entre uma sequência de Intervalos de confiança (CIs) de &quot;tempo fixo&quot; e uma Sequência de confiança (CS) uniforme no tempo poderá ser resumida da seguinte maneira:

![](assets/statistical_4.png){width="500" align="center"}

Para um Intervalo de Confiança regular, a garantia probabilística de que o parâmetro do público alvo está dentro do intervalo de valores⌘<sub>n</sub> é válida somente em um único valor fixo de `n` (onde `n` é o número de amostras). Por outro lado, para uma Sequência de confiança, garantimos que, em todos os momentos/ todos os valores do tamanho da amostra `t`, o valor &quot;true&quot; do parâmetro de interesse esteja dentro dos limites.

Isso tem algumas implicações profundas que são muito importantes para o teste online:

* O CS pode ser atualizado opcionalmente sempre que novos dados estiverem disponíveis.
* Os experimentos podem ser monitorados continuamente, interrompidos adaptativamente ou continuados.
* O erro de tipo I é controlado em todos os horários de interrupção, incluindo horários dependentes de dados.

Adobe usa Sequências de Confiança Assíntota, que para uma variante individual com estimativa média `μ` tem a forma:

![](assets/statistical_5.png){width="300" align="center"}

Em que:

* `N` é o número de unidades dessa variante.
* `σ` é uma amostra de estimativa do desvio padrão (definido acima).
* `α` é o nível desejado de erro do tipo I (ou probabilidade de cobertura incorreta). Isso sempre é definido como 0,05.
* ρ<sup>2</sup> é uma constante que ajusta o tamanho da amostra na qual o CS é mais rigoroso. Adobe escolheu um valor universal de ρ<sup>2</sup> = 10<sup>-2.8</sup>, que é apropriado para os tipos de taxas de conversão vistos em experimentos online.

## Confiança {#confidence}

A confiança usada por Adobe é uma confiança &quot;válida a qualquer momento&quot;, que é obtida invertendo a sequência de confiança para o efeito médio do tratamento.

Para ser mais preciso, em um teste de duas amostras *t* para a diferença em médias entre duas variantes, há um mapeamento 1:1 entre o valor *p* para este teste e o intervalo de confiança para a diferença em médias. Por analogia, um valor de *p* válido a qualquer momento pode ser obtido invertendo a sequência de confiança (válida a qualquer momento) para o estimador de efeito médio de tratamento:

![](assets/statistical_6.png){width="200" align="center"}

Aqui, *E* é uma expectativa. O estimador usado é um estimador de propensão inversa ponderada (IPW). Considere N = N<sub>0</sub> +N<sub>1</sub> unidades, as atribuições de variante para cada unidade `i` rotuladas por A<sub>i</sub>=0,1 se a unidade for atribuída à variante `ν`=0,1. Se for atribuída aos usuários uma probabilidade fixa (propensão) π<sub>0</sub>, (1-π<sub>0</sub>), e sua métrica de resultado for Y<sub>i</sub>, o avaliador de IPW para o efeito médio de tratamento será:

![](assets/statistical_12.png){width="400" align="center"}

Observando que *f* é a função de influência, Waudby-Smith et al. A mostrou que a Sequência de confiança para este estimador é:

![](assets/statistical_7.png){width="500" align="center"}

Substituindo a probabilidade de atribuição pelas suas estimativas empíricas: π<sub>0</sub> = N<sub>0</sub>/N, o termo de variância pode ser expresso em termos de estimativas individuais da média da amostra μ<sub>0,1</sub> e estimativas do desvio-padrão, σ<sub>0,1</sub> como:

![](assets/statistical_8.png){width="500" align="center"}

Em seguida, lembre-se de que para um teste de hipótese regular com estatística de teste z = (μ<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>) há uma correspondência entre `p` valores e intervalos de confiança:

![](assets/statistical_9.png){width="500" align="center"}

onde `Φ` é a distribuição cumulativa do normal padrão. Para valores de `p` válidos a qualquer momento, dada a sequência de confiança para o efeito de tratamento médio definido acima, podemos inverter essa relação:

![](assets/statistical_10.png){width="600" align="center"}

Finalmente, a **confiança válida a qualquer momento** é:

![](assets/statistical_11.png){width="200" align="center"}

## Declarar um experimento como conclusivo

Para um Experimento com dois braços, o painel Experimentação do Journey Optimizer exibe uma mensagem informando que um Experimento é **conclusivo** quando a confiança válida a qualquer momento excede 95% (ou seja, o valor de `p` válido a qualquer momento está abaixo de 5%).

Quando mais de duas variantes estão presentes, a correção de Bonferonni é aplicada para controlar a taxa de erro da família. Para um experimento com `K` tratamentos e um único tratamento de linha de base (controle), existem `K-1` testes de hipótese independentes. A correção de Bonferonni significa que rejeitamos a hipótese nula de que o controle e uma determinada variante tenham meios iguais, se o valor `p` válido a qualquer momento (definido acima) estiver abaixo de um limite de `α/(K-1)`.

## Braço com melhor desempenho

Quando um experimento é declarado conclusivo, o braço com melhor desempenho é exibido. Este é o braço com o melhor desempenho (maior média ou taxa de conversão), entre o Conjunto que inclui o controle, e todos os braços que têm um valor de `p` abaixo do limite de Bonferonni.
