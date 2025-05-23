---
solution: Journey Optimizer
product: journey optimizer
title: Cálculos estatísticos usados pela experimentação do Adobe Journey Optimizer
description: Saiba mais sobre cálculos estatísticos usados ao executar experimentos
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: conteúdo, experimento, estatístico, cálculo
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Compreenda cálculos estatísticos {#experiment-calculations}

Este artigo descreve os cálculos estatísticos usados quando você executa experimentos no Adobe Journey Optimizer.

A experimentação usa [métodos estatísticos avançados](../content-management/assets/confidence_sequence_technical_details.pdf) para calcular **Sequências de confiança** e **Confiança**, que permitem executar os experimentos enquanto for necessário e monitorar os resultados continuamente.

Este artigo descreve como a experimentação funciona e fornece uma introdução intuitiva às **Sequências de confiança válidas a qualquer momento** da Adobe.

Para usuários especialistas, os detalhes técnicos e as referências estão detalhados em [esta página](../content-management/assets/confidence_sequence_technical_details.pdf).

## Teste estatístico e controle de erros {#statistical-testing}

Quando você executa um experimento você está tentando determinar se há uma diferença entre duas populações e a probabilidade de que a diferença se deve ao acaso.

Geralmente, há duas hipóteses:

* a **Hipótese Nula**, que significa que não há efeito no tratamento.
* a **Hipótese alternativa**, que significa que há um efeito no tratamento.

Em significância estatística, o objetivo é tentar avaliar a força da evidência para rejeitar a hipótese nula. Um ponto importante a ser observado é que significância estatística é usada para julgar quão provável os tratamentos são diferentes, não quão provável eles são para ser bem sucedidos. É por isso que a significância estatística é usada em combinação com **Lift**.

A experimentação eficaz requer que sejam considerados os diferentes tipos de erros que podem causar inferências incorretas.

![](assets/technote_1.png)

A tabela acima ilustra os diferentes tipos de erros:

* **Falsos Positivos (erros do Tipo I)**: são uma rejeição incorreta da hipótese nula, quando na verdade ela é verdadeira. No contexto de experimentos online, isso significa que concluímos falsamente que a métrica de resultado é diferente entre cada tratamento, embora seja a mesma.
  </br>Antes de executarmos o experimento, normalmente escolhemos um limite `\alpha`. Após a execução do experimento, o `p-value` é calculado, e rejeitamos o `null if p < \alpha`. Escolher um `/alpha` é baseado nas consequências de obter a resposta errada, por exemplo, em um ensaio clínico em que a vida de alguém pode ser afetada, você pode decidir ter um `\alpha = 0.005`. Um limite comumente usado em experimentos online é `\alpha = 0.05`, o que significa que, a longo prazo, esperamos que 5 em cada 100 experimentos sejam falsos positivos.

* **Negativos Falsos (Erros de Tipo II)**: significa que não rejeitamos a hipótese nula, embora ela seja falsa. Para experimentos, isso significa que não rejeitamos a hipótese nula, quando na verdade ela é diferente. Para controlar esse tipo de erro, geralmente precisamos ter usuários suficientes em nosso experimento para garantir uma determinada Potência, definida como `1 - \beta` (ou seja, um menos a probabilidade de um erro tipo II).

A maioria das técnicas de inferência estatística exigirá que você corrija o tamanho da amostra antecipadamente, com base no tamanho do efeito que deseja determinar, bem como na tolerância a erros (`\alpha` e `\beta`) antecipadamente. No entanto, a metodologia da Adobe Journey Optimizer foi projetada para permitir que você verifique continuamente seus resultados, para qualquer tamanho de amostra.

## Metodologia Estatística da Adobe: Sequências de confiança válidas a qualquer momento

Uma **Sequência de confiança** é um análogo sequencial de um **Intervalo de confiança**, por exemplo, se você repetir seus experimentos cem vezes e calcular uma estimativa da métrica média e sua sequência associada de 95% de confiança para cada novo usuário que entra no experimento. Uma sequência de confiança de 95% incluirá o valor real da métrica em 95 dos 100 experimentos executados. Um intervalo de confiança de 95% só pode ser calculado uma vez por experimento a fim de dar a mesma garantia de cobertura de 95%; não com cada novo usuário. As Sequências de confiança permitem, portanto, monitorar continuamente os experimentos sem aumentar as taxas de erro de falso positivo.

A diferença entre as sequências de confiança e os intervalos de confiança para um único experimento é mostrada na animação abaixo:

![](assets/technote_2.gif)

**As sequências de confiança** deslocam o foco das experimentos para a estimativa em vez do teste de hipótese, ou seja, focalizando na estimativa precisa da diferença nas médias entre tratamentos, em vez de rejeitar ou não uma hipótese nula com base em um limite de significância estatística.

No entanto, de maneira semelhante à relação entre `p-values`, ou **Confiança**, e **Intervalos de Confiança**, também há uma relação entre **Sequências de Confiança** e qualquer `p-values` válido ou qualquer Confiança válida. Dada a familiaridade de quantidades como a Confiança, a Adobe fornece as **Sequências de confiança** e, a qualquer momento, a Confiança válida em seus relatórios.

Os fundamentos teóricos de **Sequências de confiança** vêm do estudo de sequências de variáveis aleatórias conhecidas como martingales. Alguns resultados principais foram incluídos abaixo para leitores especialistas, mas os argumentos dos profissionais são claros:

>[!NOTE]
>
>Sequências de confiança podem ser interpretadas como análogos sequenciais seguros de intervalos de confiança. Com intervalos de confiança, só é possível interpretar o experimento depois de atingir o tamanho predeterminado da amostra. No entanto, com sequências de confiança, você pode observar e interpretar os dados em seus Experimentos a qualquer momento que desejar e interromper ou continuar com os experimentos com segurança. A Confiança válida a qualquer momento correspondente, ou `p-value`, também pode ser interpretada a qualquer momento.

É importante observar que, como as sequências de confiança são &quot;válidas a qualquer momento&quot;, elas serão mais conservadoras do que uma metodologia de horizonte fixo usada no mesmo tamanho de amostra. Os limites da sequência de confiança geralmente são mais amplos do que um cálculo de intervalo de confiança, enquanto a confiança válida a qualquer momento será menor do que um cálculo de confiança de horizonte fixo. O benefício deste conservadorismo é que você pode interpretar com segurança seus resultados em todos os momentos.

## Declarar um experimento como conclusivo

![](assets/experimentation_report_2.png)

Toda vez que você visualiza o relatório de experimentação, a Adobe analisa os dados acumulados no experimento até o momento e declara um experimento como &quot;Conclusivo&quot; quando a confiança válida a qualquer momento ultrapassa um limite de 95% para pelo menos um dos tratamentos.

Neste ponto, o tratamento que está tendo o melhor desempenho (com base na taxa de conversão ou no valor da métrica normalizada do perfil) será destacado na parte superior da tela do relatório e indicado com uma estrela no relatório tabular. Somente tratamentos que tenham uma confiança maior que 95%, juntamente com a linha de base, são considerados nesta determinação.

Quando há mais de dois tratamentos, o link de correção de Bonferroni é usado para corrigir vários problemas de comparação e controla a taxa de erro na família. Nesse cenário também é possível que existam tratamentos múltiplos cuja confiança é maior que 95% e cujos intervalos de confiança se sobrepõem. Nesse caso, o Adobe Journey Optimizer declarará aquela com a taxa de conversão mais alta (ou valor de métrica normalizado por perfil) como o melhor desempenho.
